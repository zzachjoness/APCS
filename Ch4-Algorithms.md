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

## 3. Solving Hard Problems

### Using Heurists

- The hardest problems in cs are those that run in superpolynomial time, doubling the number of steps required each time the input size increases, or more than doubling
- When n is small these problems may be solveable, but as n increases computing time increases exponentially
- Instead of creating an exact solution, an approximation must be calculated for
- Using **heuristics** is one way to compute appoximations, a heuristic is a technique that guides an algorithm to find good choices
- When an algorithm uses a heuristic, it no longer needs to exhaustively search every possible solution, approximations can be solved for more quickly
- A heuristic is a shortcut that sacrifices accuracy and comleteness

### Traveling Salespoerson Problem (TSP)

> Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?

- The TSP problem was originally faced by traveling salesmen, but is actually relevent to many areas:
  - routing data around a network
  - manufacturing microchips
  - observing locations with a telescope
  - sequencing DNA
    **_in all of these cases we want a solution that will find an efficient path between multiple locations_**
- TSP is a combinatorial problem, which makes it difficutl
- The only way a computer can find the optimal solution is the "brute force approach": try every possible path between cities, measure the difference of each path, and pick the shortest path

### Developing a heuristic

- Start by considering how you would approach the problem
- Can we create shortcuts that will lead to a 'good enough solution'

### Knapsack problem

> You have a knapsack and a set of item types, each with a weight and value. How many of each item can you pack so that the total weight doesn't exceed the limit and the total value is maximized?

- One heuristic is to sort by value/weight ratio when selecting the next item to pack (optimize)

### Game Playing

- For a game engine to predict success, the computer needs to calculate the _entire game_ tree from current move to final move
- The chess tree would need to calculate 10<sup>120</sup> situations
- Fortunately, heuristics like "minimax" help prune down the tree of possibilities
  - Under the **Minimax** heuristic, the computer further assumes that its advesary will use the same evaluation faunction as it does, and will make the best move possible for it, resulting in the worst possible position for the computer
  - Minimax assumes that its opponent will try to minimize the evaluation function, so minimax looks to 'damage control' instead of optimize for position strength

### Facility Location

> Imagine a supermaket chain that has 20 locations in a state and wants to build 5 warehouses to deliver food to the supermarkets. Their goal is to minimize cost and maximize delivery speed.

- This problem looks to find the optimal location for the 5 warehouses
- This same problem is faced by web apps that want to distribute their backend servers to respond to user requests quickly
- Heuristics like "local search" help narrow down the array of possible locations
  - **Local search** is a heuristic method for solving computationally hard optimization problems
  - Local search can be used on problems that can be formulated as finding a solution maximizing a criterion among a number of candidate solutions
  - Local search algorithms move from solution to solution in the space of candidate solutions by applying local changes until a solution deemed optimal is found or a time bound is elapsed
  - Examples of local search algorithms:
    - WalkSAT
    - 2-opt algorithm for TSP
    - Metropolis-Hastings algorithm

### Undecidable Problems

- Some problems take a very long time to solve, so we use algorithms that give approx solutions
- There are some problems that a computer can _never_ solve, even the world's most powerful computer with infinite time: the undecidable problems
- An **undecidable problem** is one that should give a "yes" or "no" answer, but yet no algorithm exists that can answer correctly on all inputs

### The Halting Problem

- Alan Turning proved the existence of undecidable problems in 1936 by finding an example, the now famous "halting problem":

> Based on its code and an input, will a particular program ever finish running?
