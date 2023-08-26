Date: 07-23-2023 
Time: 10:06
status: #✏️ 
Tags: [[C++]]

Errors and warnings:
1. Compile Time Error 
2. Runtime Errors
3. Warnings

The goal of a programmer is to generate a binary executable file, to do this you have to run your program through a complier then to turns that into binary code for the computer. 

![[Pasted image 20230724105521.png]]


Compile Time Error:
![[Pasted image 20230724105547.png]]
This error happens when the format of the program is not correct, meaning there is something missing. In the context of human language, there is a major grammatical error, which makes it so that the compiler cannot translate the program properly.

Runtime Error:
![[Pasted image 20230724105724.png]]

This error is a logical error that happens in the program. The program executes and runs in but things aren't working as it should. This could range from text not looking correctly all the way to the program outright crashing at start up. With this problem you usually have to fix your logic in the code.

Warning:
![[Pasted image 20230724111015.png]]
It is a problem that the compiler doesn't see as a major problem that it still compiles the program. But it is an indication that you do have to fix something or else it could become worse.

Statement and Functions
Statement - The smallest thing that you computer can run. These are the lines of codes that you put in the IDE. They end with an (;).

Ex;
```C++
int firstNumber = 12;
int secondNumber = 9;
```
This has two sentences.

Sentences are read from top to bottom. Execution keeps going until the end of the program which is the 'return 0'. There will be times that the program has to terminate because of a problem or it has been explicitly said that you have to close the program.

Function:
You give it inputs and it give you outputs.

![[Pasted image 20230724115305.png]]
In this case you have the 'first_number' and 'second_number' are the numbers that you input to the function, then the gear, the function, then does something to the inputs and spits out the output, which is the sum.

Syntax of a function:

Return type
![[Pasted image 20230724115520.png]]
The return type is the data type of the function, this is needed so the computer has context on what the information being given to it is.

Function name
![[Pasted image 20230724115657.png]]
This is what you name the function so that you can call it again in the future.

Parameters
![[Pasted image 20230724115728.png]]
This is what will be input to the function. Functions act basically like an isolated program, unless you give it specific information that it can use. When you give it the information you need, it spits it out as the, in this case, sum but it can be what ever you need the function to give you.

You have to define the function before the program can use it. so you have to declare the function on the top of the program before you can use it. Though what you can do for clarity is that you can declare the name of the function first then you declare what it has to do later.

Since a function is an isolated system, you have to give it information. ![[Pasted image 20230724120143.png]]
in this case, you can see that you are giving the numbers to the function 'addNumbers' so that it can use it. 

Input Output

std::cout - goes from the program to cout then cout displays the information on the terminal..

std::cin - the information from the terminal goes to cin then goes into the program.

std::cerr - prints the errors from the compiler to the console.

std::clog - prints log messages to the console.


