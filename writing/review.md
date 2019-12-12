# Chapter 1

A computer system is made up of hardware and software.

### Hardware (physical pieces)

* central processing unit (CPU): interprets instructions
* input/output (I/O) devices: keyboard/mouse
* main memory devices: temporary storage
* secondary memory devices: permanent storage

### Software Categories
The operating system is the core software of a computer and that provides two important functions:
* User interface: allows user to interact with the machine
* Manages computer resources such as CPU and main memory

Examples of operating systems:
* Windows
* Unix
* Mac OS

### Binary Numbers

All information on a computer is stored and managed as binary values. The binary number system has only two digits, 0 & 1. A single binary digit is called a bit. 1 bit can represent 2 possible items. For example, on or off. 2 bits can represent 4 possible items, 3 bits represent 8 items, 4 bits 16 items, 5 bits 32 items, and so on.

On many computers, each memory location consists of 8 bits or one byte. (see chart on pg. 14)

### The Java Programming Language

Programs are written in program languages that use specific words and symbols to define a set of rules for the language. We use the java language.

### A Java Program
* `//` is a single line comment: doesn't affect the Program but helps organize them     
* Class definition: runs from the first opening brace `{` to the final closing brace `}`. All java programs are defined using class definitions
* Main method: where the processing begins
* Method: a group of programming statements that is a given name

### Identifiers and Reserved words
* Identifiers are the names of variables, methods, classes, packages and interfaces : public, static, void, main, string, args, System, out, println
* Reserved words are identifiers that have a special meaning in a programming language and can only be used in predefined ways :  class, public, static, and void.
* Identifiers can be made of any combinations of letters, digits, the underscore character _ , and the dollar sign $, but it can't begin with a digit. They can be any length.
* Both uppercase and lowercase letters can be used in identifiers. Java is case sensitive

### White Space
* Java programs use white space to separate the words and symbols used in a program : consists of blanks, tabs and newline characters.

### Editors, Compilers, and Interpreters
* Use editor as you type a program into a computer : Atom
* A compiler is a program that translates code in one language to equivalent code in another.
* Interpreter is similar to compiler but an interpreter interweaves the translation and execution activities

### Object-Oriented programming
* java is an object-oriented language: an object is a fundamental entity in a java program.
* object-oriented program requires understanding of following things:
  * Object: represents a real object in our problem (Bank Account)
  * Attribute: values stored internally (primitive data or other objects)
  * Method: group of programming statements
  * Class: defines the object
  * Encapsulation: protects and manages its own information
  * Inheritance: one class is based on another class that already exists


# Chapter 2

### Character Strings

* A character string is an object in java defined by the class String.
* String literals are anything inside "  "
* They are in print lines
* String literals can't span multiple lines

### Variables

* A Variable is a name for a location in memory used to hold a data value

### The Assignment statement

* Assignment statement assigns a value to a variable with =

### Constants

* Constants are identifiers and are similar to variable except that they hold a particular value for the duration of their existence.

### Primitive Data Types

* Java has 2 basic kinds of numeric values: integers, which have no fractional part and floating points, which do
* 4 integer data types: byte, short, int, and long
* 2 floating point types: float and double
* Need to pick the correct size data type in order for them to work(see chart on pg. 69)

### Characters

* Characters are another fundamental type of data used and managed on a computer
* A character is expressed in Java with single quotes like `'a'` or `'b'`
* The character we can manage are defined by a character set which is simply a list of characters in a particular order

### Booleans

* defined in java using the word boolean
* has only 2 values: `true` and `false`

### Arithmetic Operators

* Addition (`+`)
* Subtraction (`-`)
* multiplication (`*`)
* Division (`/`)
* Remainder or modulus (`%`)

### Increment and Decrement Operators

* Increment operator(`++`) adds 1 to any integer or floating point value
* Decrement operator(`:`) Subtracts 1

### Assignment Operators

* `+=`
* can be used like this `total += 5`: actually means total = total + 5
* Also `-=`, `/=`, and `*=`

## Chapter 3

### Creating objects

### Definition of an Object

> Objects have states and behaviors. For example. A dog has a states such as breed, color and name. Dogs also have certain behaviors such as wagging its tail, being energetic, barking and eating.

An object is created from a class because a class creates the blueprint for a object.

There are three steps when creating an object from a class.

1. Declaration - A variable declaration with a variable name with an object type
2. Instantiation - the new keyword used to create the object
3. Initialization - The new keyword is followed by a call to a constructor. This call initializes the new object.

* **Null**- variable that does not have any value
* **Instantiation**- creates object using "new"
  - new = ``name = new type;``
  - gives that object the power of that Class
* Constructor- special method use to initialize object
  - has the same name as class

### Data Conversion

* If one method requires a certain data type, you must convert your current data type into the one that is required.
* Ways of converting data types
1. Assignment- this is how you would normally assign a type to a variable
  - Example: ``int a = 6;``
2. Casting- just write the desired type in parenthesis in front of the variable.
  - Example: ``(double)count;``
3. Parsing- use following format:
  - Example: ``int count = Integer.parseInt(args[0])``

### Packages

* **Packages**: Group of classes which contain methods, used at the top of the java file so that other files in program do not need to be imported.
  - Example: ``package jmpplinko``

#### Importing

* There are certain Classes and methods that "plain" java does not have already in java.lang (which is automatically imported). These methods need to be **imported**.
  - Example: to get the Scanner class, you need to ``import java.util.Scanner;``
  - This goes after you declare your package

Packages in java are used to encapsulate  group of classes, sub packages, and interfaces.

Packages are used for:
1. Preventing name conflicts
2. making searching, using, and locating classes, interfaces, enumerations and annotations easier
3. providing controlled access
4. packages can be considered to be data encapsulation or data hiding

### Classes

A class is a template for which specific objects or types of objects are created.

Classes can contain local and global variables. Local variables exist within class methods and are created and destroyed within the method each time it runs. Global variables are defined outside of the methods and can be called by the other methods in the program.

An object is a specific instance of a class. Objects require constructors with the same name of the class.

In the following example, marathon exists as a reference variable. The next line declares a value for marathon.

Creating an object in reference to a class requires declaration, instantiation, and initialization. Declaration is the object type followed by the new variable name (`Runner exampleName` in the example). Instantiation is the creation of a new instance of the object (`new`). Initialization is when the constructor is called (`Runner(marathon)`) to have a value.

Example:

```java
String marathon;
marathon = new String(marathon);
Runner exampleName = new Runner(marathon);
```

Let's say, for example, the Runner class in the previous example has a method called `startRun()`. By using something called a dot operator (using the period character), we can call any method we want from the Runner class with our newly created exampleName object by writing `exampleName.startRun()`. This runs the `startRun` method from the Runner class in reference to the exampleName object.

* **Classes** are basically "blue prints" that form objects
* Creating a class is done after declaring your package title and importing everything that needs to be imported
* "Visibility" is defined by whether the class contains `private` or `public`
  * Classes can either be **public** or **private** depending on whether or not you want it to be visible/usable by other java files. But they are most always **public** because they must be visible.
  - Example: ``public class Board``
 

#### String Class

Definition of the String Class:

> The String class represents character strings. All strings within java, such as "abc," are implemented as instances of this class. Strings are constant and their values cannot be changed after created.

`String()`

This initializes a newly created String object. It will represent an empty character sequence.

#### Scanner Class

* **Scanner** reads information from either a file or takes user input
* You need to ``import java.util.Scanner;``
* Scanner has powers (methods) that can look for a certain type of input from the file or user input.
  - Example: ``input.nextInt();`` scans/ looks for the user to input an integer.

#### The Random Class

* First, you need to import ``java.util.Random``
* This Class contains methods that gives you a random number depending on what data type you use
  - Example: if you want to create a 13 sided die (from the practical), you would say: ``d13.nextInt(13) + 1;`` which gives you a random number between 1 and 13. If you do not add the 1 at the end, the range of numbers will be between 0 and 12.
nextInt is a power of the Random Class.

#### The Math Class

* Similar to the Random Class, the Math Class has special powers which are methods which allow you to do calculations by calling those methods.
  - Example: ``Math.abs(amount)`` would return the absolute value of amount.


#### Wrapper Class

* Converts primitive data types into objects
* Uses a capital letter instead of lower classes
  - Example ``Integer maya = 20;``

### Methods

* Like Classes, a **Method Declaration or signature** can either be private or public. But in this case, it depends on whether or not you want to the method to be visible or not.
* Methods can also have a return type listed after the visibility declaration. These types can include:
  - primitive types (int, double, char)
  - any object that you create
  - void (nothing)
* Methods are also named something. If there are two words in the method name, the second one is capitalized
  - Example: ``public void modifyBoard`` (from JMP Plinko)

#### Method Calls

* You can call another method from another file or even with in the file you are working on.
* This will look like: Name of object.method call
  - Example: ``Board.printBoard()``
* inside of the parenthesis, you can pass a parameter to that method which will be accepted in that method declaration.  

## Chapter 4

### Classes and Objects Revisited

  Classes are like blueprints for a type of object. Classes define the attributes that an object from that class would have. Each object's state is determined by values of its attributes. Objects can also have behaviors that are determined by the operations they can preform. Their behaviors are shaped by what an object is able to do.

* Class is a blueprint for the object
* Objects have states that are defined by the attributes that are associated with them
* The behavior of an object is defined by the operations associated with it

### Anatomy of a Class

   Classes can contain method declarations and data declarations. Examples of data declarations could be `int count = 0;` or `double balance = 3.45;
   
   Both of these declaration types are used to define the state and behavior of the objects that can be created from it. Constructors are methods that have the same name as their class. Constructors are called when `new` is used to create a new instance of a class. If more than one class is stored in a single file, only one can be declared using `public` and that class must share a name with the file. When a variable is declared at the class level, it can be referenced in any method the class.
   
  UML Diagrams can be used to show the relationship between files. UML class diagrams can be used to show the contents of classes and how they interact. They typically represent classes as rectangles divided into 3 parts: class name, attributes (data), and operations (methods).
  
* Classes have the ability to contain data declarations (stored data) and method declarations (provided services)
* Scope is the area in a program where a variable will be referenced
* Instance data makes new space for a variable with each use of that class
* UML diagrams (Unified Modeling Language) are used to show the relationship between objects and classes

### Encapsulation

  Encapsulation is the characteristic of a variable within a class being unable to be changed from outside code. This means that code that uses an object should not be able to access or change variables directly. Instead, the code can use the object's methods to be able to interact with its data. Visibility modifiers such as public and private control whether data can be directly altered by outside code or not respectively. Public variables violate encapsulation because they allow coding from outside the class to access it directly.
  
  Accessor methods, also known as "getters", allow for read-only access to values. Mutator methods, also known as "setters", allow a user to change a value.
  
* Encapsulation is used to prevent code outside of the class to alter declared variables inside the class
* A Modifier is used to specify characteristics of a programming language construct
* Visibility modifiers are used to control access to members of a class (public/private)

### Anatomy of a Method

  Method declarations contain a visibility statement such as private or public, a return type, an identifier, and possibly parameters. When a method is called, the program goes through it step by step. A called method is able to be within the same class the calling method is. Return types can be privatives, class names, or void. Methods that return a values must contain a statement using the reserved word return. Parameters are the types of values that are passed to a method; a method does not have to have parameters.
  
* When a method is called, it is given control until the method is done
* The header of a method contains: type of the return value, method name, and a list of parameters accepted by the method
* When a method doesn't return a value, void is the return type
* A return statement has the word "return" and an expression that makes sure a value is returned
* A variable can be declared inside of a method which makes it local data (as opposed to instance data)

### Constructors Revisited

  As mentioned in 4.2, constructors are the same name as their class. Constructors cannot have a return type. Constructors are used to initialize a new instantiated object.

* The name of a constructor is the same as the class
* A constructor can't have a return type
* A constructor doesn't have to be defined for each class because they have a default constructor with no parameters

## Chapter 5

## Conditions

Conditional statements are statements that are tested to be true or false. Once tested, they either allow a program to continue or terminate. These statements are called booleans. They are used in several statements and all types of loops. In `if` statements, the conditional statement is tested. If true, the program continues with the code directly below the `if`. If the statement is false, the program either continues with the 'else' statement, or exits the `if` statement altogether and continues on the with the code that follows.

Conditionals and loops allow us to control the flow of execution through a method.

### Logical operators

Operator | Description | Example|          Result                              |
---------|-------------|--------|----------------------------------------------|
    !    | logical NOT | ! a    | true if a is false and false if a is true    |
   &&    | logical AND | a && b | true if both a and b true or false otherwise |
   ||    | logical OR  | a || b | true if a or b or both are true or false     |

### Switch Statement

* Program follows one of several paths depending on a value
* Could be constructed by multiple if statements, but it is easier with a switch statement
* Evaluates the value and determines which "case" the value should fit into. This determines which path it takes
* the break statement separates cases
* Cannot use relational operations such as > or < unless other processing is done

### The Conditional (Ternary) Operator

* Similar to an if-else statement
* Requires three commands
* Uses ? as its symbol
* If a given condition is true, gives the value on one side of the ? and if it is false, gives the value on the other side
* Can work as an abbreviated if-else statmement


### Loops

Loops use conditional statements to iterate over certain amount of code, until the statement returns false. These loops, in essence, are just repeated `if` statements in various forms. A `while` loop for example tests a statement continuously. Every time the statement returns true, the code within the loop runs. Once the statement returns false, the program exits the loop, and continues on to the code that follows. There are several other loops, such as for loops and `do...while` loops, that have this same basis. The for loop allows for the program to iterate over something of known length. For loops can have self contained variables that are declared in the for conditional statement. The do-while loop runs a certain part of code while some statement is true. The difference between this loop and a regular while loop is that the code is run at least once in a do-while loop even if the conditional is false.

#### Definition and Function

##### `while`

`while` statements are loops that evaluate a boolean condition just as an `if` statement does. However, after the body is executed, the condition is evaluated again, until the condition becomes false.

###### Example

```java
int count = 1;
while (count <= 5) {
  System.out.println(count);
  count++;
}

```
##### Infinite Loops

When the condition is never false, the loop will be executed forever. This loop is called an `infinite loop.`
We must design our program carefully to avoid infinite loops.

###### Example

```java
int count = 1;
while (count != 50) {
  count += 2; // This condition is never wrong
}
```
##### Nested Loops

The body of a loop can contain another loop. This situation is called `nested loop`.

###### Example

```java
int count1, count2;
count1 = 1;
while (count1 <= 10) {
  count2 = 1;
  while (count2 <= 50) {
    System.out.println("Here again");
    count2++;
  }
  count1++;
}
```

##### The `do` Statement

* Similar to the while statement
* ends at the end of the loop body
* Executes command until loop becomes false
* Always executed at least once
* begins with the word "do"

##### The `for` Statement

* Another repetition statement similar to do and while
* Useful for when you know how many times you want to perform a loop
* Used for performing a loop a certain number of times rather than until a condition is met
* starts with "for"
* Three separated parts
  1. Initialization- determines where to start
  2. Boolean condition- evaluates before the loop body occurs. When this is true, performs the loop
  3. Incremenet- Executed multiple times after each iteration, can also perform a decrement
* Can be somewhat difficult to read at first because it does not read top too bottom exactly
* for-each loop is a variant that is helpful with iterators, those with hasNext and next in them

##### Iterators

An _iterator_ is an object that has methods that allow you to process a group of related items. It provides a consistent and simple mechanism for systematically processing a group of items.

* Example:
 `hasNext()` in Scanner class: Class returns true if there is another input token to process.

## Chapter 7

### Everything is an object

What is an object? 

In this instance, an object is a method that stores data. For instance, if you wanted to make a point object that held an x and y coordinate, it might look something like this:

```
private int x;
private int y;

public Points(int x, int y){
  this.x = x;
  this.y = y;
}

public int getX(){
  return this.x;
}

public int getY(){
  return this.y;
}

public void setX(int x){
  this.x = x;
}

public void setY(int y){
  this.y = y;
}
```

In the constructor, we set the values of the point. In the "get" method, it returns the int value that you are looking for. In the "set" methods, it modifies the value.

Now in the main method we might have something like this:
```
Points point = new Points(inputX,inputY);
point.setX(4);
System.out.println(point.getX() + "," + point.getY());
```

This may not seem very useful, but if there are a lot of points that you need to keep track of, sometimes using objects like this make it a whole lot easier to keep track of things and make it easier to call things.

Objects can also be dependent on other objects.
Assume that in "Points" there is another method.

```
public Point modifyPoint(Point point){
  int x = point.getX + 1;
  int y = point.getY + 1;
  return new Points(x,y);
}
```

As you can see, an object can be used as the return type as well as be the parameters.

In the main method, it may look like this.

```
point = point.modifyPoint(point);
```

### Objects vs Classes

#### What is a class?

A class is like a blue print for code itself. For instance, in real life a car is an object. The car in this scenario has different attribute and methods. Attribute like its size, color and its weight. Methods is describing its driving capability and brakes.
Below is an example of a class. The class is named Die, but it really could be anything.(I don't have any creativity so I used die from lab 5)

```java
  public class Die {
    int = 6;
  }
```

#### What is a method?

A method is just a block of code that can be run if called on. Data can be passed through it, those type of data is called parameters. We used methods because it allows us to reuse codes. If methods didn't exist, we will be tired out or our hands will fall off. So to prevent this, we used methods.
Below is an example of a method.  from Lab 5 Die.java

```java
public void roll() {
  value = dieObject.nextInt(sides) + 1;
}
```

#### Static

`static` is a key word in java. By key word I mean that it has its own job. For instance int stores numbers and doubles stores decimal numbers. Static is also called a reserve key word, you cannot name a class static. There are four places that static can be used. The word `static` can be used during the creation of a new variable, block and methods.

##### Static block example
```java
static {
  a = c * 4;
}
// note that all these examples start with static.
```

##### Static variable example
```
static int = 12;
static double = 233.22;
```

##### Static method example
```
public static void main(String[] args) {
  int a = 12;
  int b = 22;
}
```

* Instance variables are variables declared in the class. New copies of instance variables are created for each instance of an object. Instance variables can be specifically accessed using the this reference, which allows an object to refer to its own instance variables specifically.
* Members of a class (methods, variables) can be static. Static class members are shared across all instances of a class. Static variables can only be referenced in a static environment, meaning that static methods can only access static variables and not instance variables. Static methods are invoked through their class name instead of an object of that class.
    * Static examples: main methods, all methods of Math class, methods of Integer class, etc.
* Classes may be dependent on one another, meaning that one class uses the in some way. In general, dependencies should be avoided when possible, because dependencies can make issues in one section of code impact the program as a whole.
    * Classes may even be dependent on themselves; our rational number code depended on itself to generate a reciprocal.
    * An object that has dependencies on many objects may be called an aggregate object. One example of an aggregate object could be a BankAccount object, which may contain references to a CheckingAccount object, a SavingsAccount object, etc.
    
## Chapter 8

### Data structures

#### `ArrayList`

_ArrayList_ Class belong to java.until. package. An ArrayList object stores a list of object and lets you access them using an integer index.
When an _ArrayList_ object is created, you specify the type of element that will be store in the list.

##### Some methods of _ArrayList<E>_ Class:

Method                     |                             Functions                                    |
---------------------------|--------------------------------------------------------------------------|
ArrayList<E>               | Constructor: Create an empty list                                        |
boolean add (E object)     | Inserts the specified object to the end of this list                     |
void add(int index, E obj) | Inserts the specified object into this list at the specified index       |
void clear()               | Removes all element from the list                                        |
E remove (int index)       | Removes element at the specific index                                    |
E get (int index)          | Returns the object at the specific index                                 |
int size()                 | Returns the number of elements in this list                              |

* Example

```
ArrayList<String> band = new ArrayList<String>;
```

#### Arrays

An `array` is a simple yet very useful construct in java. Its used to group an organize data.

Arrays are useful for listing things. Arrays in java always begin at zero. To access a value in the array,
use the name the array followed by the index in square brackets. Arrays are objects, a reference to an array
must be declared.

```java
public class Array {

public static void main(String[] args) {
  final int limit = 8, multiple = 10;
  int[] list = new int[limit];
  for (int index = 0; index < limit; index++)
    list[index] = index * multiple;

  list[3] = 500;

  for (int value : list)
    System.out.print(value + "");
  }
}
```

* An array is simple and powerful, used to organize or group things
* Allow declaration of one variable that holds multiple accesible values
* Always begin at 0
* Values are stored in a specific numbered position of the array
* Value of index is not equal to value stored
* Can use integer expressions to specify the index used to access the array (arrays indexes are integers)
* Reference to array must be declared
* can be created with the "new" operator
* Can hold different data types, but all data types in an array must be the same type (Ex. must be all strings or all integers)
* Often helpful to use for loops because arrays have a constant number of positions
* Square brackets ([]) are used to indicate the array index
* Java automatically checks bounds of Arrays
  * Must be greater than or equal to 0 and less than the size of the array
  * ArrayIndexOutOfBoundsException indicates the chosen value is not valid for the array
* Maximum number of things an array can actually hold is length-1, as everything is off by one because the array starts at 0.
  * Example: in an array of the alphabet, z's location would be 25, as it is the 26th letter but 26 - 1 = 25.
* length stores the size of the array and allows you to check an array's size
* Two potential ways to syntax an array:

```java
int[] grades;
int grades[];
```
* Using an initializer can provide initial values for the array
* Items in an initializer are separated by commas and deliminated by braces:

```java
int[] scores = {87, 89, 214, 616, 2};
```

* Arrays can be used as a parameter to a method
* Methods that receieve an array as a parameter can change them permanently, rules are consistent with any object type's rules

##### Arrays of Objects

* Arrays can store primitives as well as objects
* Each element of an array is a separate object
* An array of objects is actually an array of object references

##### Command-Line Arguments

* Parameter to a method of a Java app is an array of strings
* Typically this is called "args"

##### Variable Length Parameter Lists

* You can create a method using arrays that processes different amounts of data throughout
* Java allows us to define methods that accept varied-length parameters that automatically puts them into an array
* ... indicates that the method accepts variable parameter numbers
* If a method accepts varied numbers of parameters, it also can accept other parameters.

##### Two Dimensional Arrays

* Arrays can have multiple dimensions
* This allows one to create a table-like array with a row and collumn
* BRackets are used to indicate separate dimensions in an array:

```
int[][]
```

* For loops are used to load an array with values and print the arrays into a table-like
* initializers can still be used
* Arrays can have more than even three dimensions potentially

### Iteration and Recursion

#### Math behind the examples 

```
n! = n * (n-1) * (n-2) * ... 3 * 2 * 1
```

In explaining recursion, it is better to describe it in a mathematical factorial term as it simplifies what recursion is to the simplest degree. As seen with the equation, you start out with a number and then it moves on to the next number that is one less than the previous one and continues down that path until it reaches 1.

Example:

> 5! = 5 * 4 * 3 * 2 * 1

The example demonstrates that with each number that goes down the factorial it returns a value from the end which is multiplied by the previous number. By taking the previous number and multiplying it by the number that has one less value, this demonstrates a recursion as with every value that decreases by one, you get a recusion.

#### Iteration

Iterative methods go through a task one item at a time often using structures such as for and while loops. These utilize conditional statements to define their termination point. Iterative methods typically require less processing time compared to recursive methods.

```java
public static int iterativeFactorial(int factorial) {
  int num = 1;
  int result = 1;
  while (num < factorial) {
    result * = num;
    num++;
  }
  return result;
}
```
Ex. To calculate a factorial with iteration

#### Recursion

Methods calling themselves in order to complete a task. Recursive methods also have a base case to terminate so that the method does not infinitely recur. In the below example the if statement represents the base case. Notice that this requires an additional parameter compared to the iterative method above. Recursive methods are typically easier to read and require fewer lines of code.

```java
public static int recursiveFactorial(int factorial, int result) {
  if (factorial == 1) {
    return result;
  }
  result * = factorial;
  factorial = factorial - 1;
  return recursiveFactorial(factorial, result);
}
```
Ex. To calculate a factorial with recursion