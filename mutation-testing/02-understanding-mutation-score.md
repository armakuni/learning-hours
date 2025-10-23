# Understanding Mutation Score

## Learning Goals
  - To understand the concept of a mutation score
  - To run mutation testing on a project
  - understand the difference between code coverage and mutation score
  - To discuss the different metrics you can use to measure the quality of your code

## Session Outline
  - **5 min connect**: Do our tests give us enough confidence?
  - **6 min concept**: What is a Mutation Score?
  - **34 min do**: Run mutation testing on your project
  - **10 min reflect**: Code Coverage vs Mutation Score

### Connect - Do our tests give us enough confidence?

Invite all attendees to the session to write down what level of confidence they have in their tests.
  - 1 = Least Confident
  - 5 = Most Confident

Get each person to share:
  - level of confidence
  - why they gave that number?
  - What would make you more confident?

### Concept - What is a Mutation Score?

A lot of teams use Code Coverage to measure the quality of their of their testing and whilst this tell you how much of your
code is executed by tests, it doesn't tell you how much of your code is actually tested. This is one of the reasons why 
mutation testing is so popular. It will give you a metric to measure how much of your code is actually tested. that you 
can aim to improve on over time.

All mutation testing frameworks report a mutation score. This can be calculated using the following formula: 

$$\text{Mutation Score} = \frac{\text{Killed Mutants}}{\text{Total Mutants} - \text{Equivalent Mutants}} \times 100$$

Like with code coverage, the higher the mutation score the better.

**Low Mutation Score Example**
with 200 killed mutants of a possible 920 we have a mutation score of: 21.73913043 which is not particularly good. 
$$21.73913043 = \frac{200}{1000 - 80} \times 100$$

**High Mutation Score Example**
with 895 killed mutants of a possible 920 we have a mutation score of: 97.283 which is very good.
$$97.283 = \frac{895}{1000 - 80} \times 100$$

Where:
  - **Killed Mutants** is the number of mutants that have been killed by the tests.
  - **Total Mutants** is the total number of mutants in the project.
  - **Equivalent Mutants** are mutants that produce the exact same observable behavior as the original code (even though 
    the syntax is different) and can therefore never be killed. They are excluded from the denominator to give an 
    accurate score.

### Do - Run mutation testing on your project

**Note:** The facilitator should install and configure the mutation testing framework on the chosen project before the 
session, and push the setup to a branch so everyone can clone and run it easily.

In pairs run mutation testing on your project. Look at areas of the code that you have worked on recently and see if you 
can find any mutants that have not been killed. Do this for both people in the pair.

Discuss the results with your partner. Discuss what surprised you and what you think is useful to know about the results.

Did you find any escaped mutants that you think should been killed?
Write does some tests you could add that would catch the escaped mutants.

### Reflect - Code Coverage vs Mutation Score

In Pairs discussion what you think about all the different metrics you can use to measure the quality of your tests.

  - Are you currently tracking code coverage?
  - Does it give you confidence that your tests?

Also discuss the different metrics you can use to measure the quality of your code.

  - Which other metrics do you track? 
  - Which metric do you find most useful?
  - Which metric do you find least useful?
  - Which metric do you trust?
  - Which metric do you not trust?

