# String Handling
This file will go through what you can do within string in Python, as part of this, you will cover the following commands:
- replace()
- count()
- split()
- String Slicing

Additional details on all of the types of string handling that you can do within Python, can be found on the following link: [W3Schools - String Methods](https://www.w3schools.com/python/python_ref_string.asp)

## Replace()
This method will look to take a current string and replace all values that are provided, for instance, let's say that you had the below:
```python
myString = "Hello word, welcome to the program"
```
We can use the .replace() method to change **word** to **world**. Replace() will take the following parameters:
> *string.replace(old,new,count)*
- old = What word you want to look for/replace
- new = What you are replacing old with
- count = An optional additional, but will allow you to specify how many occurrances you want to replace.

In our case, this would look like the following:
```python
myString = "Hello word, welcome to the program"

newString = myString.replace("word", "world")
print(newString)
```
This would output:
```
Hello world, welcome to the program
```

## Count()
This method will look to count the amount of instances that there are within a string. For instance we can look at counting the amount of "i"s within the below:
```python
enteredString = "This is an example string"

print(enteredString.count("i"))
```
This will output the following
```
3
```
This can also be done with whole words, however be cautious of this, an example is below:

```python
enteredString = "Polly the parrot is poor at getting under par in golf"

print(enteredString.count("par"))
```
This will output the below:
```
2
```
This is because "par" is within that string twice, once for **par**ot, another for **par**. This is where other methods such as **.split()** can come in useful.

Further details on count can be found here [W3Schools - Count() String](https://www.w3schools.com/python/ref_string_count.asp)

## Split()
Split will take a string and convert this into a list. This will take the following parameters:
> *string.split(separator, maxsplit)*
> 
> If you do not provide a separator, the default will be a white space. 

For instance, looking at the following code:
```python
enteredString = "Polly the parrot is poor at getting under par in golf"

print(enteredString.split())
```
This will output:
```
['Polly', 'the', 'parrot', 'is', 'poor', 'at', 'getting', 'under', 'par', 'in', 'golf']
```
If we put this within a variable, we can use *.count()* to accurately count the amount the word "par" is within that string. This will look like the following:
```python
enteredString = "Polly the parrot is poor at getting under par in golf"

splitString = enteredString.split()

print(splitString.count("par"))
```
This will output the following:
```
3
```
## String Slicing
We are able to take a string and grab specific parts of it using the technique of string slicing, this looks like the following:
![String Slicing Syntax](https://www.learnbyexample.org/wp-content/uploads/python/Python-String-Slicing-Syntax.png)

We can provide values within the square brackets to obtain certain pieces of a string, some challenges looking at this are available within the string handling document:

![String Slicing Example](https://i1.faceprep.in/Companies-1/string-slicing-in-python.png)