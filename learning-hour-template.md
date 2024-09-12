# Mutation Testing: What is a Mutant?

Now that we are using test driven development our code coverage should always be 100% however bugs can still creep in. 
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
fail. When a mutation does not make any tests fail is it said to have escaped and show there is a potential bug in your 
code. 

Describe some of the type of mutation that can be made by a mutation testing framework

### Do - Simple Mutation Testing Kata

In pairs complete the Simple Mutation Testing Kata making a note of all the types of mutations you see.

### Reflect - What mutations did you see?

List all the types of mutations that found bugs in you code. 
Tell the group which one you found most interesting