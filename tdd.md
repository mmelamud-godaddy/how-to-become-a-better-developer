# Test Driven Development (TDD)
---

## What is TDD?

TDD refers to Test Driven Development. TDD is used to design and develop the tests for the functionality of the product. We don’t have to write duplicate code if we are working with TDD. If an automated test case fails then the developer has to write the new code.

The purpose of TDD is to make code bug-free, simple and clearer. The work of TDD is to fix the failed test cases before writing the new test cases. It is also called Test First Development.

<p align="center">
  <img width="454" height="258" src="https://user-images.githubusercontent.com/81258448/189261785-6e96fa39-8933-48e1-b91d-f6dcae71a9a1.png">
</p>

## The three Laws of TDD
1. You are not allowed to write any production code unless it is to make a failing unit test fail.
2. You are not allowed to write any more of unit tests than is sufficient to fail; and compilation failures are failures.
3. You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

_by Robert Martin_

## TDD Cycle

TDD in practice is actually a cycle, where we first write tests that fail, then we write the minimum amount of functionality to make that test pass, then finally we refactor the program to improve it without changing its external behaviour.

<p align="center">
  <img width="500" height="465" src="https://user-images.githubusercontent.com/81258448/184520566-fe657b4f-8d5c-429a-a209-65d7c23ce15c.png">
</p>

### RED

Red is the first of the three cycles of TDD. In red, we need to write the tests necessary in order to achieve the goal of the current feature.

So how do we write good tests that not only accomplish the user story, but is also clean and readable for you and others working with you?

Thankfully, from the book _Clean Code by Bob Martin_, we have the **F.I.R.S.T** principle for testing:

- **Fast:** Your tests should be fast enough that it doesn’t deter you or other programmers to initialize the testing procedure.

- **Independent:** Each test should be independent, it should not depend on tests that have happened previously. If the tests require data, then that data has to be set up at the very beginning of that test, not the one before.

- **Repeatable:** Tests should be able to run in any environment, whether it is at your local machine, other people’s machines, or at the git repository. If the tests fail, it is because the functionality of the program is not correct, nothing else.

- **Self-Validating:** The tests should tell you whether or not it succeeds. It should not require the developers to manually check the output of the test in order to dictate whether or not the test is successful. We can do this by returning a boolean, or by using the assert method available in most programming languages or test frameworks.

- **Timely:** Tests should be written just before the programmer writes the code to make it pass, not after. This is especially true if we are following TDD.

### GREEN

After writing our tests and committing it to our repository, we now need to begin the implementation of our code. In this phase, our goal is to make all tests that previously failed in the Red section pass.

That’s the only goal we have at this stage, to write the bare minimum code necessary to pass our tests and accomplish the user story.

Once you are done, commit your code with the commit message starting with [GREEN], indicating that the tests you made should pass by now.

### REFACTOR

Once we have written the code, this is the opportunity to [refactor](https://github.com/mmelamud-godaddy/how-to-become-a-better-developer/blob/main/refactoring.md) it. Remember that at the Green step in the TDD cycle, we are tasked to write the minimum implementation in order to pass the tests we wrote at Red.

So what can we do at this stage? Well, we can start by getting rid of unused variables and imports, renaming unclear variables and functions, and cleaning up our code.
