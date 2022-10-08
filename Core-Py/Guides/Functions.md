# Python Functions
Functions within programming are essentially pieces of pre-written code that you can use as many times as you want. To do this

## Function Fundamentals
```python
# Creating a function:

def funcName():
    # Do something
    return

# Runs the function
funcName()
```

- Consider the def keyword as “defining” a function​
- The funcName represents what you want to call it, this can be anything you want; although this should be relevant to what you are wanting to use it for.​
- Unlike variables, all functions must have ()​
- Defining a function is finished by using a colon​

Example of a function being used:
```python
# FUNCTION AREA # 
def displayHello():
    print("Hello World")
    return

# MAIN AREA #
displayHello()
```

Output:
> Hello World

## Parameter/Argument Passing
If a variable is created within a function, in most languages it is only accessible within that function. This is what is known as encapsulation.
In order for us to be able to use a variable from "main" within our function, it is good practice to pass it through using parameter passing methods:

```python
def addNumbers(x,y):
    print(x+y)

# We can use functions more than once:
addNumbers(2,7) # Outputs 9
addNumbers(17,3) # Outputs 20
addNumbers(11,364) # Outputs 375
```

## Sample Program:
Create a function that asks the user to input in their name.​

Return this to the main program, put this into a variable and output to the screen.

Answer:
```python
def getName():
    return input("Enter your name: ")

returnedName = getName()
print("Using the function, you inputted: " + returnedName)
```