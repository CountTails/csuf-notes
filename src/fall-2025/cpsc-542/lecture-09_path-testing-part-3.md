# Lecture 9: path testing (part 3)

## Path example

- Forward learning strategy is hard to explain
- Let's try reversed learning strategy by observing a case

### Code under test

```java
public class PathExample {
  public int returnInput(int x, boolean condition1, boolean condition2, boolean condition3) {
    if (condition1) {
      x++;
    }
    if (condition2) {
      x--;
    }
    if (condition3) {
      x=x;
    }
    return x;
  }
}
```

- The output should equal its input

### Statement coverage

- The test case `(0, true, true, true)`
  - Traverses all statements
  - Passes
- With this single test case, we can claim we have achieved 100% statement coverage

### Branch coverage

- One test case is not enough for branch coverage
- The test case `(0, false, false, false)` 
  - Traverses the missing branches
  - Passes
- With 2 test cases, we can claim we have achieved 100% branch coverage

### Level of confidence

- We achieved 100% statement coverage with 1 test case
- We achieved 100% branch coverage with 2 test cases
- The test cases pass (with flying colors)
- Why does the level of confidence feel low despite the coverage statistics?
  - Careful observations would show `(0, true, false, true)` and `(0, false, true, true)` would fail and reveal a bug
  - 100% statement and branch coverage is not good enough
  - We want (at least try) to get 100% path coverage

## Paths

> A path is a unique traversal from entry to exit

### How many

- A program with three 2-way decision nodes will have 8 possible paths
- 100% path coverage will reveal the bug in the path example code

### Is 100% really necessary

- If we have ten 2-way decision nodes, we will need to cover 1024 possible paths
- This is just way to many

### Equivalent path classes

- Promotes the idea that some paths are more special/important/significant than others
- Treat each path as a vector and it may reveal that a group of vectors can be used to construct all other vectors
  - The vectors in this special group are called independent vectors
  - Since the rest of the paths are mathematically dependent on the independent vectors, testing all independent vectors implies testing of all paths
- Testing of all independent paths may give a sense of completeness of testing all possible paths since all the rest of the paths are mathematically dependent on the independent paths
- Follows a similar line of thinking in our treatment of equivalence class testing
- This is commonly known as basis path testing

## Basis path testing

- How many basis paths are there?
- How do you find them?

### Finding basis paths

- If a program has no decisions
  - You have 1 path (just from start to exit)
  - That one path is for sure an independent path
- If you have one 2-way decision in your program
  - You have 2 paths
  - Both of those paths are independent
- If you have two 2-way decisions in your program
  - You have 4 possible paths
  - Only 3 of those paths are independent

### Insights

- Mathematically, basis paths are special
- By testing the basis paths, we avoid testing all possible paths (which is economically infeasible in most cases)
- Calculating the number of basis paths for a given program is called Cyclomatic complexity
  - Simply $\text{number of 2-way decisions} + 1$
  - Or $e - n + 2p$ where
    - $e$ is the number of edges for the given program graph
    - $n$ is the number of nodes
    - $p$ is the number of connected regions (usually 1 in most cases)
