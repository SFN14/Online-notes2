---
Type: personalnotes
---
Date: 07-23-2023
Time: 12:39
Status: #✏️
Tags: [[CS50]]

----

When programming focus on on:
Correctness - Solving the problem correctly.
Design - How well the program is structured, and how easy it is to read and understand.
Style - How pretty your code looks like.

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

some functions come with the program, but most of the time you have to get a library. 

thats what the 
```C
#include <stdio.h>
```
at the top of the code

the whole code:
```C
#include <cs50.h>
#include <stdio.h>

int main(void)

{
    string answer = get_string("What's your name? ");
    printf("hello, %s\n", answer);
}
```

The
```C
#include <cs50h>
#include <stdio.h>
```
are the libraries that add extra functionality to the programs.

This block of code:
![[Pasted image 20230723150124.png]]

becomes:
```C
printf("Hello, %s", answer);
```


This block:
![[Pasted image 20230723150325.png]]

Becomes this in C:
```C
int main(void)
{

}
```

This code:
![[Pasted image 20230723150437.png]]

Becomes:
```C
#include <stdio.h>

int main(void)
{
	printf("Hello, world\n");
}
```

This is the library
```C
#include <stdio.h>
```

This is a header file
```C
stdio.h
```

In C, there was no string, though it was common in programming, but it was implemented as a library by cs50

A library is used so that the code doesn't crash horrifically due to C being and older, lower level programming language. Due to this user input could be done in such a way that a crash will be likely to occur. But libraries circumvent this problem.


Terminal commands:
cd - change directory
cp - copy
mkdir - make directory
mv - move or rename
ls - list
rm - others
rmrdir - remove directory
.. - parent directory/previous folder

Data types of C:
string - words
int - integer
long - bigger integer
char - 1 character
bool - true or false
float - decimal no.
double - bigger float 

CS50 fuctions:
get_char
get_double
get_float
get_int
get_long
get_string

To print diff data

%c - char
%f - float/double
%s - string
%i - integer
%li - long

Operators:
```
+ addition
- subraction
* multiplication
/ division
% remainder
```

Variables and syntactic sugar:
![[Pasted image 20230723152812.png]]

this becomes:
```
int counter = 0;
```

this:
![[Pasted image 20230723152929.png]]

becomes:
```
int counter = counter + 1;
```

or 
```
int counter += 1;
```

or
```
int counter++;
```

All Data types have a certain amount of bits that it could handle, some have 32 bit, some has 64 bit. You have to take this into account while writing code.