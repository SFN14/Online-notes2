---
Subject: CC103
Type: College Notes
---
Date: 09-13-2023
Time: 16:43
Status: #✏️
Tags:

----

# How can you make Java Programs with?
## GUI (Graphical User Interface) 
Has graphics and buttons the usual we see 
This is refers to IDE like VS Code and 

## Console Based (Terminal I/O Interface)
- Uses the Notepad++
- Command Prompt
### JRE (Java Runtime Environment)
This is what loads the code after it has been complied

### JDK (Java Development Kit)
Complies the code that you made that it can be handed to the JRE

# Using Terminal I/O Interface
cd.. - Change Directory
cls - clear screen
javac (Program Name).java - java compile

# Syntax
System.out.print - print the text in the ()
System.out.print - print the text in a new line after the text

# Structure of Java Program

```Java
// This is a comment

public class add
{
	public static void main(String[] args)
	{
		System.out.println("Computer Programming");
	}
}
```

![[Pasted image 20230920162946.png]]

Line 1 is a single line comment (2 forward slashes)
Comment
-> Programmers use comments to explain or clarify the meaning of some section of a program.
These are optional, they don't affect how the program works, and may be placed anywhere. Well placed comments helps with readability and clarity of the program.
Multi-line comments begins with
```Java
/*  and ends with 
*/
```

class name must be a valid Java identifier.
A vail java identifier is a word composed of letters, and/or digits, and/or two special characters & and _ Where the first character must be a letter. Class names are case sensitive.

Java adding special meaning to certain words called keywords or reserved words, and may not be used as Java identifiers. Like int,  boolean, long, etc.

By convention, a class begins with an uppercase letter. This is just etiquette. There shouldn't be any spaces, instead use _ to separate them.

Lines 4 and 9, the curly braces {} mark the beginning and end of the program, the statement enclosed by curly braces are called a block.

Line 5, public static void main(String[] args) is the heading of the class' main method.

Enclosed in the () is called a method.
A method is a section of a class that performs a task, which contains single statement or more. A statement is an instruction or directive. 

When a java program starts, the main method is automatically executed, because its the 'main' function. 

Line 7: System.out.print("Computer Programming");
The quoted text is the string literal or string. The quotation marks indicate the beginning and the end of the string.

The newline Character (println), causes the cursor to advance to the start of the next line.

println is a method that Java provides for ouput.

The string supplied to the println method is called argument.

println("Hello");
println is the method, while the inside the () is the argument, so the ("Hello") is the argument.

so you are passing the ("Hello") to the println.

Staructure of Java Program
Java dicvtates that all statements are terminated with a semicolon.
To include quotation marks within a string literal, use the escape sequence, \" (Backslash, quote)
```Java
System.out.println("\"ABC"\""); //This is so that you can do a quote in the string literal
// or
System.out.print("\t\tABC"); //This is so that you can tab automatically in output
```

# Using operations to do calculations in programs
## 4 primative data types
### int
the values associated with the data type int are integers in the range of -2,147,483,648 to 2,147,483,647

The associated operators that manipulate integers are:
+
addition
-
subtraction
*
multiplication
/
division - gets the quotient and discards any remainder.
%
modulus - evaluates the remainder after diving any two integers.

May contain several operators and follows the MDAS rule. (Operator preceedance)
```
* / %
Left to right (High)

+ -
Left to right (Low)
```

You can use a parenthesis to prioritize calculating a certain thing first.

Example:
Write a program that calculates the number of calories burned using weight and distance as integer data type.

Formula: calories = 0.653 x weight x distance 

![[Calories Burned]]


### double
The values associated with the data type double are decimal numbers  in the range -1.7x10<sup>308</sup> to -1.7x10<sup>308</sup>
you can also use MDAS operators same as Int.

division operator / denotes decimal or floating-point division rather than integer division.
ex. 
double = 5.0 / 2.0; is 2.5

double  = 5/2 is; 2.0

### char
Type char  is the set of all characters found on the  standard keyboard.
The value of type char is enclosed in single quotes.
'5' is a value of type char.
"5" is a string literal.
1 + 5 has a value of 6 .
1 + '5' has a value of 54 or 1 + the ASCII value of 5, which is 53, so 1 + 53.
1 + "5" has a value of 15, 1 concutination 5.

ASCII is American standard code of information interchange.

Rype char also inclused several special characters that are represented by an escape sequrence or escape character. 

Common escape sequences are:
```
\n newline
\t tab
\b 
\r
\' single qoute
\" doube qoute
\\
```

### boolean
Type boolean has  two values: true  and false.
The associated operators are:
&& and
|| or
! not
Simple assertions that we accept as either true or false:



&& if one if false, all is false .
|| if one is True then all is true, if both are false then all are false.
! not, opposite.

Order
! && ||


Relational Operators
```
<
<=
>
>=
==
!=
```

Order of booleans
True or False
x=3; y=1; z=8; a=8; b=4; c=2; d=3; e=12;

```java
import java.util.Scanner;
```

java - package
util - library
Scanner - object


### This is process is called instantiate 
![[Pasted image 20230920181753.png]]
The Scanner is the command that you borrowed
input is the name you designate to the command that you borrow
'new' is the instantiation that you will do a new Scanner.
Scanner is the method inside the () is telling what you want to to do, which is System.in or getting the user's input and placing it in the system.

![[Pasted image 20230921081914.png]]

![[Pasted image 20230921081926.png]]

answer:
1. True && True = **True**
2. False || False (False && False) = False
3. True && True || True = True
4. 

There would be 2 batches
1st batch then 2nd batch, in the second Lab the 2nd batch would be made then 1st batch.