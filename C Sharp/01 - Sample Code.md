# Sample Code Workthrough

Slash slash is a comment, that the program will not run

## Outputting within CSharp
```csharp
// Outputting within C#
Console.WriteLine("Hello World");

// To run your programs, press F5 or the "Play" button at the top

Console.WriteLine(3 + 4); // WriteLine will also allow us to use Maths!!

Console.WriteLine("3 + 4");
```
Unlike Python, C# does not automatically convert our data types. So for example, age = 22 will NOT work

## INPUT:
> Console.ReadLine();

Data is stored in a variable, this is a location/box in memory where data is stored
> dataType varName = dataToStore

## Data Types
All variables that we store are assigned a data type (this is manual in C#):
- int - Whole number
- double - Floating Point
- char - Single character/symbol
- string - Text and numbers surrounded in double quotes
- bool - True or False

```csharp
int age = 22;
Console.WriteLine(age);
string myName = "Barry";

Console.WriteLine("Your name is: ");
Console.WriteLine(myName);
// We can simplify the above into one line!

Console.Write("Your name is: ");
Console.Write(myName);

// GETTING AN INPUT WITHIN C# (we use ReadLine())
// string shoeSize = "";
Console.WriteLine("Enter in your shoe size: ");
string shoeSize = Console.ReadLine();

Console.WriteLine("Your shoe size is: ", shoeSize);
```