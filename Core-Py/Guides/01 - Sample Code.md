# Sample Code Workthrough

Hashtag is a comment, that the program will not run

## Outputting within Python
```python
print("Hello World")
```

> To run your programs, press F5 or the "Play" button at the top

```python
print(3+4) # Print will also allow us to use Maths!!

print("3+4")
```

Python does not "require" semi-colon at the end of lines

## INPUT:
> input()

Data is stored in a variable, this is a location/box in memory where data is stored
> variableName = dataToStore

```python
age = 22 # This is automatically given a data type of integer due to this storing a whole number

print(age) # This will display the value that I stored above
```
## Data Types
All variables that we store are assigned a data type (this is automatic in Python)

- String = Bunch of letters and numbers, in quotation marks
- Boolean = True or False value
- Integer = Whole Number (no decimal point)
- Float = "Floating Point" value, this includes decimal points
- Char = Character (one letter/symbol)

```python
myName = "Barry"
print("Your name is: ")
print(myName)

# We can simplify the above into one line!
print("Your name is: ", myName)

# GETTING AN INPUT WITHIN PYTHON (we use input())
shoeSize = input("Enter in your shoe size: ")
print("Your shoe size is: ", shoeSize)

# In Python, by default, any inputs will be a string automatically, to change this, we can do the following. Putting int() around the input will convert it to an int value, this is called PARSING:
heightEnter = int(input("Enter in your height as a number: "))
```