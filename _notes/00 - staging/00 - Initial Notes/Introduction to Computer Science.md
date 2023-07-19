---
Type: personalnotes
---
Date: 07-17-2023
Time: 11:11
Status: #💡 
Tags: [[CS50]] 

----
# What is Computer Science?
- In a basic sense it is problem solving. Where you have to process inputs into outputs.
![[Inputoutput]]
# What is Computer language? 
- Computer language represents the inputs that give to our computers.
- Computers use the Binary language, using ones and zeroes to count. using different patterns to count numbers. These numbers are called Bits 
- Computer language is basically a language that is written in 1s and 0s, and we have to agree (standards) what that pattern of 1s and 0s mean to know what a computer is outputting. 
## What is binary?
In Binary, 1 represents that it stores electricity, while zero means it doesn't, this is the most basic way a computer can communicate.
- We could use a switch to represent the one or zero, an open switch is 1 while a zero isn't.
- We use the decimal system to represent number like 123, 1 in in the 100ths 2 is in the 10ths and 3 is in the 1s. In binary the 000 is just in powers of zeroes from left to right 2<sup></sup><sup>2</sup>, 2<sup>1</sup>, 2<sup>0</sup>. This is why 010 is equals to 2, because we times 4 to 0, 2 to 1, then 1 to 0, then we all them all together to get 2. You can change the base base to count in a different way, or add more bits to count more.
- We could also use numbers in binary to represent letters in a language.
# How do we understand the language of computers?
## How Letters are Displayed with Numbers
- We interpret the patterns of  0s and 1s depending on the context, meaning it depends on the program, or file type.
- We give a computer a hint to tell the computer how to interpret the bits. The standardized way to do this is ASCII.
![[Pasted image 20230717113659.png]]
*ASCII Chart*

- Byte are 8 bits
- in 8 bit, you can count up until in 255.
- ASCII can only handle 255 characters due every character being only 8 bits.
- Unicode is ASCII but it uses 16 Bits to represent characters, and can represent ~65,000 characters and sometimes 32 Bits for ~4 Billion Characters. it is backwards compatible with ASCII. 
## How Can a computer display Colors?
- We can use RGB, or mixing Red Green and Blue to display colors.
- We can use representation again, just like in ASCII to represent the amount R, G, B we want to display.
- We use 24 bits total to represent 8 bits of R, 8 bits of G, and 8 bits of B to know how to mix them together and represent a pixel.
### How to represent a video using bytes.
 - Video is just the changing of colors over time
### How to represent audios into bytes.
 - Using MIDI, we could use musical notes, and again, represent them into bytes just like ASCII.

# Algorithm
- it is a step by step instruction on how to solve a problem or sets of instructions on solving a problem.
- Ex: looking for a name in a Phone Book page by Page (not the best way).
- Harnessing intuition.
- The goal is to lessen the time used to an problem, no matter how big it gets. 

## Pseudo Code
- The logic behind the solution to a problem, the code or an Algorithm 
Ex: 
```C++
1 Pick up phone book
2 Open to the middle of phone book
3 look at the page
4 If person is on page
5	Call Person
6 Else if person is earlier in book
7	Open middle of left half of book
8	Go back to Line 3
9 Else if person is later in book
10	Open to middle of right half of book
11	Go back to line 3
12 Else
11  Quit
```
## Edge cases
- In This case quit is an important action. Because, what will the computer due if doesn't find the person?
- 
## Functions
- Actions that solve smaller problems.
Ex:
```c++
1 **Pick** up phone book
2 **Open** to the middle of phone book
3 **look** at the page
4 **If** person is on page
5	**Call** Person
6 Else if person is earlier in book
7	**Open** middle of left half of book
8	Go back to Line 3
9 Else if person is later in book
10	**Open to** middle of right half of book
11	Go back to line 3
12 Else
11 **Quit**
```
Those quoted in "****" shows what would be functions if it were real code. 

```C++
1 Pick up phone book
2 Open to the middle of phone book
3 look at the page
4 **If** person is on page
5	Call Person
6 **Else if** person is earlier in book
7	Open middle of left half of book
8	Go back to Line 3
9 **Else if** person is later in book
10	Open to middle of right half of book
11	Go back to line 3
12 **Else**
11  Quit
```
Those quoted in "******" shows what would be conditionals if it were real code.

```C++
1 Pick up phone book
2 Open to the middle of phone book
3 look at the page
4 If **person is on page**
5	Call Person
6 Else if **person is earlier in book**
7	Open middle of left half of book
8	Go back to Line 3
9 Else if **person is later in book**
10	Open to middle of right half of book
11	Go back to line 3
12 Else
11  Quit
```
Those quoted in "******" shows what would be Boolean expressions if it were real code.
Boolean expressions answers in 'yes' or 'no's

```C++
1 Pick up phone book
2 Open to the middle of phone book
3 look at the page
4 If person is on page
5	Call Person
6 Else if person is earlier in book
7	Open middle of left half of book
8	**Go back to Line 3**
9 Else if person is later in book
10	Open to middle of right half of book
11	**Go back to line 3**
12 Else
11  Quit
```
Those quoted in "******" shows what would be loops if it were real code.
This is done to do the same problem by looping on its self over and over again with only a few lines of code.

# What actual code actually looks like

```
# include <stdio.h>
int main(void)
{
	printd("Hello, world\n");
}
```

```C++
# include <iostream>
int main()
{
	std::cout>> "Hello world" >> ln;
}
```