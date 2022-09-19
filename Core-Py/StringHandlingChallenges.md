# String Handling Challenges
Below are some string handling challenges that you can work towards completing, each will range in complexity:
## First, middle and end
Create a program which looks to create a new string that grabs the first, middle and last character of a name that is entered in by the end user. For example, if the user were to enter in:

```python
enteredName = "Bandicoot"
```
Then the program will output the following:
```
Bit
```
## First 3 letters of a country
Create a program which will output the first 3 characters of a country that is entered in by the user; these should be outputted in capital letters. To extend this program further, consider importing these details from a file e.g. a text or csv file. For instance:
```python
countryName = "Europe"
```
The program will output:
```
EUR
```

## Counting Digits, Letters and Symbols
Create a secure password checker which will ask the user to enter in a password of their choice, the program will then display back the amount of characters, digits and special characters that are within the entered password. For instance:
```python
enteredPassword = "L932$aS2"
```
Would output the following:
```
Total Length = 8
Characters = 3
Digits = 4
Symbol = 1
```

> As an extension to this program, add in details that will display the number of capital and lowercase characters

## Counting Names from a file
You have been provided with a .txt file on Teams (nameslist.txt) that has a list of a bunch of names, count how many of each name there are in the file, and print out the results to the screen.​

You have been provided with a subsection of the code below: the parts in comments are pieces of code that you will need to create:​

```python
# Dictionary that stores current words​

#Open file using context manager​

line = f.readline()​
while line:​
    line = line.strip()​

# IF LINE IN DICTIONARY, ADD 1 to that dictionary location; ELSE dictionary location = 1
```

## Pig Latin Converter
A challenging program that looks at creating a program to convert a word into Pig Latin. You should make sure that the outputted word is displayed in lower case.

Pig Latin is a concept which takes the first consonant of a word, moves it to the end of the word and adds on an “ay”. 

If the first letter is a vowel, just “way” needs to be put on the end of the word.

Some example outputs are below:
```
Hello = ellohay
Me = emay
Latin = atinlay

Excuse = excuseway
Egg = eggway
Eat = eatway
always = alwaysway
```