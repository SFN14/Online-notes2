---
Type: College Notes
Subject: cc103
---
Date: 08-23-2023
Time: 16:29
Status: #✏️
Tags: [[Computer Programming 1]]

----
# Basics of Computer Programming 

## What is computer programming?
It is the process of writing instructions that are to be executed by computers. This can be written through an Integrated Development Environment or Pen and paper.
These instructions are called 'code', it is written in programming languages which is translated by a complier and understood by a computer. Examples of programming languages are Java, C++, C# Python, etc.

### Machine Language
It uses binary digits 0 and 1. It  is the natural language of a computer thus they are machine dependent. 
Examples:
10111000
00000101
00000000

### Assembly Languages
It uses mnemonics or symbols to represent instructions and data. They used assemblers to convert the source code to machine language then loaded and run by a loader. These are also  known as low-level programming languages.  
Examples:
MOV AX, D6
MOV BX, 02
ADD AX, BX

### High-level Languages
They  use English-like statements and it uses compliers or interpreters to translate the source code to machine language.

Note: Computers are not smarter than humans, because computers can only understand 1s and 0s, and they use it in complex ways, so that's why they look smarter. 

# Programming Basics

## Debugging 
The process of eliminating mistakes in your program.
### 3 Types of errors
#### Syntax Error 
-> Grammatical mistake in your program. 
Ex: Missing comma or a quotation mark, or misspelling a word. 
#### Run-time Error
-> Detected when the program is run.
Ex: Attempts to perform operations (Such as math operations) on data of the wrong type (ex. attempting to subtract two variables that hold string values).
#### Logic Error
-> The output of your program is wrong.
-> These  are the errors done by programmers.
-> Also known as a logic error.
-> The programs with these error run but do not produce the desired results.
Ex: Getting a division of two numbers as an output but the expected is multiplication of numbers. 

Note: a great way to see how your program will flow, use a flowchart. This is the story board of the computer. 

# History of Java
## In 1991 James Gosling and his team began designing the first version of Java.
-> its first name was Oak, it was named this because there was an oak tree outside of their HQ.
-> The main goal of Java back then was to be used for home appliances
-> Java Byte Code or Byte Code.
## 1994: Ideal for Web browse, then was produced by Patrick  Naughton and Jonathan Payne.
-> Evolved into the browser known as Hot Java
-> Start of Oak's Connection to the internet.
## 1995: Netscape Inc. released its browser capable of running Java Programs
-> 1st Public implementation was Java 1.0
-> Oak's name was changed to Java due to a company previously having a trade mark on the name.
## Java became popular with the advent of Java 2
-> Has multiple configurations built for different types of platforms.

# What is program variable?
- It represents a location or a set of locations in the computer's main memory.
  -> Values are placed in these locations known as variables. 
- Different values are placed in the storage depends on the type of value stored.
  -> The values may be changed from time to time. 
- Variable should be declared prior to storage of any values, these are known as data types.
  Ex: Int, Float, Bool, Char, String, etc.
- When declaring variables, in Java rules must be followed accordingly. 

## Values that can be placed in variables
1. Numeric Values
- Real
	-> 3,  8, 50 
- integer
	-> 10, -23 ,100
1. Character Values
   - Standard ASCII Characters
	-> A, B, b, x, Y
   - Special Characters
	-> &, !, %
## Variable Names
A variable is used to refer to those spaces in memory
Basic rules to follow when assign name variable
	Use Only Alphanumeric characters and underscore
	Do not use Java reserved words
	Cannot contain spaces
	Do not duplicate variable name
	Upper- and lower case characters are different

### Some examples of variable name
#### Valid
Total
TOTAL
gross_pay
GrossPay

#### Invalid
2total (starts with a number)
float (reserved word used)
gross pay (contain space)
amt$ (contain '$' symbol)

Note: Use capital declaration in java for class names. Use small case when one word, and in convention, use camel case (Gross_Pay) when two words.

## Data Types and Declarations
Data type is some reserve words used to specify the values whether they are integral, real, character, etc. 
Different storage space would be allocated depends on the Data Type.
Declaration is a process of reserving storage area in order to store different values temporarily.

Ex:
```java
String surname; //(New data type)

int age; //(old data type)

double computedGrade; //(old data type)
computedGrade = 90.88; //(the value of computedGrade variable)

char middleInitial; //(old data type)

int day, number, total; //(old data type) (you can declare multiple variable names by using comma as a separator)

String surname = "Samson"; //(You can assign a value while defining a data type)

char middleInitial = 'C'; //(String uses " " while char uses ' ')
```

