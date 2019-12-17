# Assignment07: Pickling and Exception Handling
**Dev:** *Nicholas Goodwin*  
**Date:** *12/16/2016*  

## Introduction:
For this assignment, we were tasked with understanding, practicing and demonstrating execution of effective code for Pickling and 
Exception Handling Statements. As we progress into more detailed coding with Python, we are also learning that there are unique aspects 
to Python code. More importantly, we need to understand the importance of these unique coding aspects as well as when and why we should 
use them in our code.

## Pickling:
Pickling is a means of storing data in its entirety in a file that can be retrieved later. Pickling allows you to convert data into bytes 
of memory to be used at a later time and is a good technique to utilize when utilizing persistent data. Something to be cautious of is 
that pickling is a technique that is specific to Python, thus may not be compatible across other languages.  

## Exception Handling:
When Python encounters an error in the code, it stops at that spot and generates an error message to the user. The use of exception 
handling allows the code to continue to run even if it came across an error in the code. Python has many built-in exceptions or you can 
use self-generated exception handling through ‘try’ and ‘except’ clauses. The try and except clauses are blocks of code that will handle 
any exceptions in the code by catching the issue, generating an error message (or not if there wasn’t an error) and then continue on with 
the next block of code without halting. Exception handling is a great tool to utilize if you think there are blocks of code that could 
experience errors with certain data entries, so it makes functionality smooth along with allow the developer to write specific error 
statements that will aid the user in adapting.

## Summary:
For this lesson, we continued to outfit our toolbox with different tools and techniques to enhance our code while also making it more user 
friendly. Pickling is a great data retention technique for data that we want to access again in which I demonstrated a technique to write 
and store data in a low storage binary file. Lastly, the use of exception handling teaches a developer to add that extra step of 
consideration when writing code in which they can add exception handling within blocks of code that they feel may have a potential of 
generating errors from certain data entries. All in all, more foundational blocks to strengthen our foundation.

```
# ------------------------------------------------------------------------ #
# Title: Assignment 07
# Description: Pickling and Exception Handling
# ChangeLog (Who,When,What):
# Nicholas Goodwin, 12/08/2019
# ------------------------------------------------------------------------ #


# Pickling #
import pickle
baseballHR_dict = {'Ruth': 61,'Maris': 69, 'Bonds': 73, 'Ozzie': 1}
filename = "Homerun"
outfile = open(filename, 'wb')
pickle.dump(baseballHR_dict, outfile)
outfile.close()


# Exception Handling 1 #
try:
    print(2/0)
except ZeroDivisionError:
    print("You cannot divide by zero!")

# Exception Handling 2 #
try:
    a = int(input("Enter a positive integer: "))
    if a <= 0:
        raise ValueError("This is not a positive integer!")
except ValueError as ve:
    print(ve)
```    

#### Pickling and Exception Handling Command Script

![Assignment07_Command Script](docs/Assignment07_Command%20Script.png "Assignment07_Command Script")

#### Figure Assignment07_Command Script

