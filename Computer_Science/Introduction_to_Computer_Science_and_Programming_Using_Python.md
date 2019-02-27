# Introduction to Computer Science and Programming Using Python
## Intruduction

[MIT 6.00.1x course on edx](https://www.edx.org/course/introduction-to-computer-science-and-programming-using-python-0).
Textbook is "Introduction to Computer Science and Programming Using Python"; However, this course used to use SICP, so may
read it after the course.

## Week4. Good Programming Practice

### Testing and Debugging

High quality code:

- defensive programming: Write specifications for functions, Modularize programs, check IO condtions
- testing/validation: compare input/output to except
- debugging: study events leading up to bug

#### set up for easy testing and debugging
- from the start
- modules
- document constraints (input / output)
- document assumptions before code design

#### Classes of tests
- unit test: each function
- regression test: catch reintroduced bug
- integration test: overall program (_most people tend to rush to this_)

#### Approaches
- random testing
- black box testing: 
  - only look on the specification, not code
  - can be done by others to avoid implemente biases
  - reused test
  - paths through specificaiton
     - different natural space partitions
     - corner case (boudary condition)
- glass box testing
  - use code directly
  - path-complete: every potential path tested
  - can go through same loops many times, missing path 

