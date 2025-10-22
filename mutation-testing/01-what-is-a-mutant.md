# Mutation Testing: What is a Mutant?

Now that we are using test driven development our code coverage should always be 100%, however bugs can still creep in. 
There is a chance we miss edge cases in our test. This is where Mutation Testing comes in. 

## Learning Goals
  - Understand what Mutation Testing can show us about our tests
  - Experiencing using Mutation Testing to discover simple bugs in our code

## Session Outline
  - **10 min connect**: How do you judge test quality?
  - **15 min concept**: What is a Mutation?
  - **25 min do**: Simple Mutation Testing Kata
  - **10 min reflect**: What mutations did you see?

### Connect - How do you judge test quality?

Write down the ways you judge the quality of your tests.
Discuss the ways with the group.

### Concept - What is a Mutation?

Mutation testing changes our code under test (Mutates) and then executes the test against the code expecting tests to 
fail. When a mutation does not make any tests fail, is it said to have escaped and show there is a potential bug in your 
code. 

Describe some of the types of mutation that can be made by a mutation testing framework

### Types of Mutation

#### Statement mutation

Statement mutation is a category of mutation testing that focuses on modifying the program's control flow and structure 
at the statement level. This involves introducing defects by performing basic edits such as deleting a statement, 
duplicating a statement, reordering a sequence of statements, or replacing a statement with a NO-OP (no operation) 
equivalent. The primary goal of statement mutation is to evaluate the test suite's ability to detect structural and 
control flow defects. By confirming that the tests fail when necessary code statements are altered or removed, it 
verifies that each line of code is genuinely necessary for correct program execution, thereby helping to ensure 
comprehensive test coverage and identify redundant code.

##### Example - Removing a statement

###### Before
The code below checks if the username and password are equal to admin and secret.
```java
public boolean checkCredentials(String username, String password) {
    if (Objects.equals(username, "admin") && Objects.equals(password, "secret")) {
        return true;
    } else {
        return false;
    }
}
```

###### After
The mutation testing framework has removed the else statement.
```java
public boolean checkCredentials(String username, String password) {
    if (Objects.equals(username, "admin")) {
        return true;
    } 
}
```

#### Value mutation
Value mutation is a mutation testing technique that focuses on altering the data used within the program. It involves 
introducing defects by modifying constant numerical or string literal values used in assignments, calculations, or 
comparisons. 

The goal is to test the test suite's sensitivity to boundary conditions and data-specific logic. By ensuring the tests 
fail (i.e., "kill" the mutant) when a value is subtly changed, this mutation type verifies that the tests are not only 
covering the code but are also validating the program's logic against correct and specific input data, thereby improving 
the robustness of the test suite.

##### Example - Changing a numerical value

###### Before
The code will multiply a value by 2
```java
public int multiplyByTwo(int value) {
    return value * 2;
}
```

###### After
The mutation testing framework has changed the multiplier value to 5.
```java
public int multiplyByTwo(int value) {
    return value * 5;
}
```

#### Decision mutation
Decision mutation (often referred to as Relational Operator Replacement or Conditional Operator Mutation) is a key 
technique that specifically targets the Boolean logic and conditional statements that dictate a program's control flow. 
It introduces defects by systematically changing the relational or logical operators within a condition.

The purpose of decision mutation is to evaluate the test suite's ability to cover and distinguish between adjacent 
logical conditions. By confirming that tests fail when a decision boundary is slightly altered, this technique ensures 
the test suite is not only executing the conditional code but is also adequately testing the specific logic of the 
decisions, thus validating that the code behaves correctly under various boundary and logical scenarios.

##### Example - Changing Mathematical Operator

###### Before
The code will return whether value `a` is greater than value `b`.
```java
public int greaterThan(int a, int b) {
    return a > b;
}
```

###### After
The mutation testing framework has changed the greater than operator `>` to a greater than or equal to operator `>=`.
```java
public int greaterThan(int a, int b) {
    return a >= b;
}
```

### Do - Simple Mutation Testing Kata

In pairs complete the [Simple Mutation Testing Kata](https://github.com/armakuni/simple-mutation-testing-kata) making a 
note of all the types of mutations you see.

### Reflect - What mutations did you see?

List all the types of mutations that found bugs in your code.
Tell the group how you fixed the missing tests and which one you found easiest to fix.
Tell the group which one you found most interesting