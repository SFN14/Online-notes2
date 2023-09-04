---
Type: personalnotes
---
Date: 07-23-2023
Time: 12:39
Status: #✏️
Tags: [[CS50]]

----
# Programming with any Language
When programming focus on on:
Correctness - Solving the problem correctly.
Design - How well the program is structured, and how easy it is to read and understand.
Style - How pretty your code looks like.

# From Blocks into Programming Language
This block:
![[Pasted image 20230723143915.png]]
means this in the C programming language:
answer = get_string("What's your name? ")

= is not equal sign anymore, its assignment operator, we equate value of the right to the left one.

we also have to tell the computer what type of value the integer is:

string answer = get_string("What's your name? ")

This is so that the computer knows how to interpret the set of binary things.

The semi-colon denotes the close of the line.
string answer = get_string("What's your name? ");

## Libraries
Some functions come with the program, but most of the time you have to get a library. 

thats what the 
```C#
#include <stdio.h>
```
at the top of the code

the whole code:
```C#
#include <cs50.h>
#include <stdio.h>

int main(void)

{
    string answer = get_string("What's your name? ");
    printf("hello, %s\n", answer);
}
```

The
```C#
#include <cs50h>
#include <stdio.h>
```
are the libraries that add extra functionality to the programs.

## Displaying text
This block of code:
![[Pasted image 20230723150124.png]]

becomes:
```C#
printf("Hello, %s", answer);
```

## The equivalent of a start block
This block:
![[Pasted image 20230723150325.png]]

Becomes this in C:
```C#
int main(void)
{

}
```

## How to make the "hello, world" Program in a Programming Language
This code:
![[Pasted image 20230723150437.png]]

Becomes:
```C#
#include <stdio.h>

int main(void)
{
	printf("Hello, world\n");
}
```

This is the library
```C#
#include <stdio.h>
```

This is a header file
```C#
stdio.h
```

In C, there was no string, though it was common in programming, but it was implemented as a library by cs50

A library is used so that the code doesn't crash horrifically due to C being and older, lower level programming language. Due to this user input could be done in such a way that a crash will be likely to occur. But libraries circumvent this problem.

# Using the terminal
Using the terminal is usually faster then clicking, because you have to fiddle stuff in the GUI and such, this can make your workflow slow, that is why you should almost always use the terminal when testing programs, and making new files for programs.

### Terminal commands:
cd - change directory
cp - copy
mkdir - make directory
mv - move or rename
ls - list
rm - others
rmrdir - remove directory
.. - parent directory/previous folder

# C++ Syntax
## Data types of C:
string - words
int - integer
long - bigger integer
char - 1 character
bool - true or false
float - decimal no.
double - bigger float 

## CS50 fuctions:
get_char
get_double
get_float
get_int
get_long
get_string

## To print diff data:
%c - char
%f - float/double
%s - string
%i - integer
%li - long

## Operators:
```C#
+ addition
- subraction
* multiplication
/ division
% remainder
```

## Variables and syntactic sugar:
Syntactic sugar is a way to make your code look cleaner and easier to look at.

This:
![[Pasted image 20230723152812.png]]

this becomes:
```C#
int counter = 0;
```

this:
![[Pasted image 20230723152929.png]]

becomes:
```C#
int counter = counter + 1;
```

or 
```C#
int counter += 1;
```

or
```C#
int counter++;
```

These all does the same thing but is easier to understand and is easier in the eyes.



Side note: All Data types have a certain amount of bits that it could handle, some have 32 bit, some has 64 bit. You have to take this into account while writing code.

In a conditional statement, try to minimize the amount of questions being asked, this is for optimization reasons. 

If you know that number should not change, then make it into a constant.

You can use the comments to put in pseudo code to think of a way to solve the problem you want to solve.

# Concept of Loops
## While loops
While a condition is not achieved, do the program. When the condition is achieved, then stop the program inside the loop.

This makes it so that you can loop up to three times.
```C#
int i = 0
while (i < 3)
{
	printf("Meow\n");
	i++;
}
```

# For loops
This is a type of loop that you can usually use to repeat a 'code' a certain amount of times. This is usually used for counting.

```C#
for (int = 0; in < 3; i++)
{
	printf("Meow\n");
}
```
the variable inside the "()" will stay inside the () in a for loop.


## Do while loop:
Does the thing first then the condition is at the end of the code.

### ASCII print
Example code:
```C#
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int n;
	do //This asks how many '?' to make
	{
		n =  get_int ("Width: ");
	}
	while (n < 1);

	for (int i  = 0; i < n; i ++) //This for loop makes the '?'
	{
	printf("?");
	}
	printf("\n");
}
```


Another Example code:

```C#
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int n;
	do //This asks how many '?' to make
	{
		n =  get_int ("Width: ");
	}
	while (n < 1);

	for (int i  = 0; i < n; i ++) //This for loop prints the columns
	{
		for (int j = 0; j < n; j++) //This for loop prints the rows
			{
			printf("#");
			}
			printf("\n"); // Moves to the next row
	}
}
```



# Calculator problems

When calculating you can have times where you can't get the exact answer you want the computer to give you, this is because there will be times that the program will run out of bits for that one task. Just like how exceeding a specific number in whole numbers will make the answer suddenly negative, or that numbers that have long decimals will not have a proper decimal, due to integer overflow. Or sometimes, it just approximates to give you the answer somewhat near.

Truncation can happen sometimes, this is the act of the computer cutting away a value due to it not being the correct data type or a data type that doesn't support that kind of number. For example you have a variable that is an integer, but your output is a float, your answer would only show whole numbers due to the integer data type simply not supporting decimals. However you can convert one data type to another.

## Data type conversion

The first iteration of the calculator:
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int x = get_int("x: ");
	int y = get_int("y: ");
	float x = x / y;
	
	printf("%.50f\n, z");
}
```

Where you convert the data type from one to another:
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int x = get_int("x: ");
	int y = get_int("y: ");
	float x = (float) x / (float) y;
	
	printf("%.50f\n, z");
}
```

The only thing you need to do is specifically say that no a later part of the code what you want the variable's data type to be. 

## Integer Overflow
This happens when a bit has too much information than it can display for example 

![[3 bits]]
This is the limit of 3 bits, it shows no. 7 if you all them all up, but if we add more to show 8...

![[Overflow]]
it would make an invisible 1 and make all the 3 bits zero, which would just turn the bit back to 0.