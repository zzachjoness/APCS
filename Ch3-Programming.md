# Chapter 3. Programming

Start: _December 14, 2022_<br />
Finish: _December 13, 2022_

## 1. Introduction

- All programs are made up of **statements**, instructions that inform the computer of what to do
- print() command is a function, method, or **procedure** which calls the function that knows how to display output in a console
- print() expects a single **parameter** which specifies what text the computer should display

## 2. Variables

- Programs store data in **variables**, each variable has a name, value, and type
- score = 0 is a statement

## 3. Math Overview

- pi
- % modulo

## 4. String Overview

- concat
- substring

## 5. Conditionals

- Boolean
- If...else
- Compond booleans
  - JS -> || Python or
  - JS -> && Python and
  - JS -> !(expression) Python not

## 6. Logical equivalence

- NOT true equivalent false
- NOT (speedLimit = carSpeed)
- NOT (A AND B) equivalent NOT A OR NOT B

## 7. Procedures

- DRY

## 8. Repetition

- JS -> `for(let x = 0; x < 10; x++):`
- Python -> `for x in range(10):`

## 9. Lists

- Append (list, item)
  - JS -> `fruits.push("apple")`
  - Python -> `fruits.appned("apple")`
- Instert (list, i, item)
  - JS, insert "pear" @ index 1 -> `fruits.splice(1,0,"pear")`
  - Python -> `fruits.insert(1,"pear")`
- Reomve (list, i)
  - JS, remove(index,length) -> `fruits.splice(1,1)`
  - Python , remove first item -> `fruits.pop(1)`
- Itterate over list
  - JS -
  ```
  for (var i = 0 ; i < list.length ; i++) {
    # do something special
  }
  ```
  - Python -
  ```
  for i in list:
    # do something special
  ```
