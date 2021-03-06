# React the complete guide

[Udemy cource](https://www.udemy.com/react-the-complete-guide-incl-redux/) by Maximilian Schwarzmüller. (Took note from Section 16).

## Redux

Redux is not a part of React.

Reducer must be the only place control state. Put logic in reducer.

### Leaner Reducer
#### Utlity function
This is just a good practice.
Create an update functoin in sepearate file to reuse:

```Javascript
// utility.js

export const updateObject = (oldObject, updateValues) => {
  return {
    ...oldObject,
    ...updatedValues
  }
}

// in reducer
switch(action.type) {
  case Some action type:
    updateObject(state, {prop: state.prop})
}
```
#### Leaner Switch
Extract the `case some case: do something`, `do something` part to a sepearte function.

### Aync
[redux-thunk](https://github.com/reduxjs/redux-thunk)

Put that in action：

```JavaScript

export const setIngredient = (ingredients) => {
  return {
    ...
  };
};

export const fetchIngredientsFailed = () => {
  return {
    ...
  };
};

export const initIngredients = () => {
  return dispatch => {
    axios.get('https://reactburger-d37b5.firebaseio.com/ingredients.json')
      .then(response => {
        dispatch(setIngredient(response.data));
      })
      .catch(error => {
        dispatch(fetchIngredientsFailed());
      });
  };
};


```

### Combine Reducers

```JavaScript
import combineReducers from 'redux';
const rootReducer = combineReducers({
  burgerBuilder: burgerBuilderReducer,
  order: orderReducer
});
```

## Test
Jest + Enzyme
### What to Test
- Don't test library
- Don't test complex connections
- test isolated units
- test conditional outputs
- what change 




