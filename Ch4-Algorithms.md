# Chapter 3. Algorithms

Start: _January 02, 2023_<br />
Finish: _January 02, 2023_

## 1. Introduction

- An **algorithm** is a step by step process that describes how to solve a problem in a way that always give a correct answer
- There are often multiple algorithms that solve a particular problem, the best suited algorithm is typically the fastest solver
- There are three (3) basic building blocks of algorithms:
  - **Sequencing** of an algorithm is a step-by-step process, and the order of those steps is critical to esnure correctness
  - **Selection** can be used to determine a different set of steps to execute based on a Boolean expression
  - **Itteration** is used to execute steps a certain number of times or until a certain condition is met

## 2. Evaluation of Algorithms

- It is difficult to prove that an algorithm is correct
- Programmers often use:
  - **Emprical analysis** to find faults in an algorithm
    - Based on actual experimentation and observation of the results
    - Can only be used to prove that an implemented algorithm is _not_ correct, by discovering inputs where the output is unexpected
    - However, it **_cannot_ prove that an algorithm is correct**
  - Only **formal reasoning** can prove total correctness
    - One form of reasoning is a "proof by induction", a technique that's also used by mathematicians to prove properties of numerical sequences
    -
- **Linear Search** finds a value in a list, by looking through each item in the list and checking to see if the value is equavalent to the target value
- **Binary Search** utilizeds a sorted list, in which the algorithms starts by checking the middle of the list in attempts to 1/2 the list size, this process will continue until the value has been located or determined to not exist in the list

### Categorizing Run Times

- **Constant Time** will always require a fixed number of steps no matter the input size
- **Logarithmic Time** increases proportionally to the logarithms of the input size
  - Binary Search impliments a halfing of the samples size every loop, which specifies log<sub>2</sub>n
- **Linear Time** increases in size in direct proportion to the input size i.e. Linear Search
- **Quadratic Time** algorithms increase in proportion to the input size squared
  - Several list sorting algorithms run in quadratic time i.e. selection sort
  - Selection Sort starts from the front of the list, and keeps finding the next smallest value in the list and swapping it with the current value which specifies 1/2(n<sup>2</sup>-n)
- **Exponential Time** algorithms grow in superpolynomial time, its number of steps increase faster than a polynomial function of the input size

  - An algorithms often requires superpolynomial time when it must look at every permutation of values i.e. an algorithms that generates all possible numerical passwords for a given password length which specifies 10<sup>n</sup> steps

  #### Polynomial vs. superpolynomial

  - Polynomial time describes any run time that does not increase faster than n<sup>k</sup>, which includes constant time (n<sup>0</sup>), logarithmic time (log<sub>2</sub>n), linear time (n<sup>1</sup>), quadratic time (n<sup>2</sup>), and other higher degree polynomials (like n<sup>3</sup>)
  - Superpolynomial time describes any run time that does increase faster than n<sup>k</sup>, and includes exponential time (2<sup>n</sup>), factorial time(n!), and anything else faster
