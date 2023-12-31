---
toc: false
comments: false
layout: post
title: Bollean If
description: Week 8 accomplishments
type: tangibles
courses: { compsci: {week: 8}}
---

Conditional (“if”) statements: Affect the sequential flow of control by executing different statements based on the value of a Boolean expression.

IF (condition)
{
	<block of statements>
}

The code in <block of statements> is executed if the Boolean expression condition evaluates to true; no action is taken if condition evaluates to false.

IF (condition)
{
	<block of statements>
}
ELSE
{
	<second block of statements>
}

The code in the first <block of statements> is executed if the Boolean expression condition evaluates to true; otherwise, the code in <second block of statements> is executed.

Question: Calculate the sum of 2 numbers. If the sum is greater than 10, display 10; otherwise, display the sum.

num1 ← INPUT
num2 ← INPUT
sum ← num1 + num2
IF (sum > 10)
{
	DISPLAY (10)
}
ELSE
{
	DISPLAY (sum)
}



```python
# Hack 1

# Add a variable that represents an age.

# Add an 'if' and 'print' function that says "You are an adult" if your age is greater than or equal to 18.

# Make a function that prints "You are a minor" with the else function.
```

Relational operators: Used to test the relationship between 2 variables, expressions, or values. These relational operators are used for comparisons and they evaluate to a Boolean value (true or false).

Ex. a = b evaluates to true if a and b are equal, otherwise evaluates to false

a == b (equals)	
a != b (not equal to)
a > b (greater than)
a < b (less than)
a >= b (greater than or equal to)
a <= b (less than or equal to)

Question: The legal age to work in California is 14 years old. How would we write a Boolean expression to check if someone is at least 14 years old?

age ≥ 14

Question: Write a Boolean expression to check if the average of height1, height2, and height3 is at least 65 inches.

(height1 + height2 + height3) / 3 ≥ 65



```python
# Hack 2

# Make a variable called 'is_raining' and set it to 'True".

# Make an if statement that prints "Bring an umbrella!" if it is true

# Make an else statement that says "The weather is clear".
```

Logical operators: Used to evaluate multiple conditions to produce a single Boolean value.

NOT	evaluates to true if condition is false, otherwise evaluates to false
AND	evaluates to true if both conditions are true, otherwise evaluates to false
OR	evaluates to true if either condition is true or if both conditions are true, otherwise evaluates to false

Question: You win the game if you score at least 10 points and have 5 lives left or if you score at least 50 points and have more than 0 lives left. Write the Boolean expression for this scenario.

(score ≥ 10 AND lives = 5) OR (score = 50 AND lives > 0)

Relational and logical operators:

Example: These expressions are all different but will produce the same result.

age ≥ 16 	 	age > 16 OR age = 16		NOT age < 16


```python
# Hack 3

import random

# Make a function to randomize numbers between 0 and 100 to be assigned to variables a and b using random.randint

# Print the values of the variables

# Print the relationship of the variables; a is more than, same as, or less than b
```


```python
import getpass, sys
def question_with_response(prompt):
    print("Question: " + prompt)
    msg = input()
    return msg
questions = 3
correct = 0
print('Hello, ' + getpass.getuser() + " running " + sys.executable)
print("You will be asked " + str(questions) + " questions.")
answer = input("Are you ready to take a test?")
rsp = question_with_response("What's my name?")
if rsp == "Lakshanya":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")
rsp = question_with_response("What is an interest I mentioned in my data tables?")
if rsp == "books":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")
rsp = question_with_response("What day is today?")
if rsp == "Thursday":
    print(rsp + " is correct!")
    correct += 1
else:
    print(rsp + " is incorrect!")
print(getpass.getuser() + " you scored " + str(correct) +"/" + str(questions))
```


```python
#HOMEWORK


# The quiz contains questions related to Boolean values, Boolean expressions,
# conditional statements, relational operators, and logical operators.

# Import necessary modules
import getpass  # Module to get the user's name
import sys  # Module to access system-related information

# Function to ask a question and get a response
def question_with_response(prompt):
    # Print the question
    print("Question: " + prompt)
    # Get user input as the response
    msg = input()
    return msg

# Define the number of questions and initialize the correct answers counter
questions = 5
correct = 0

# Personalized greeting message
# Collect the student's name
user_name = input("Enter your name: ")
print('Hello, ' + user_name + " running " + sys.executable)
print("You will be asked " + str(questions) + " questions.")
answer = input("Are you ready to take a test?")

# Question 1: Boolean Basics 
# Ask a question about Boolean values and check the response
# Provide feedback based on the correctness of the response

# Question 2: Boolean Expressions
# Ask a question about Boolean expressions and their importance in programming
# Provide feedback based on the correctness of the response

# Question 3: Conditional Statements
# Ask a question about the purpose of conditional (if-else) statements in programming
# Provide feedback based on the correctness of the response

# Question 4: Relational Operators
# Ask a question about common relational operators in programming and provide examples
# Provide feedback based on the correctness of the response

# Question 5: Logical Operators
# Ask a question about the use of logical operators in programming and provide examples
# Provide feedback based on the correctness of the response

# Display the final score
# Calculate the percentage of correct answers and provide feedback
print(user_name + ", you scored " + str(correct) + "/" + str(questions))

```
