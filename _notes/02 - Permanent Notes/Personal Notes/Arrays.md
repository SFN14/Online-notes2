---
Type: personalnotes
---
Date: 07-27-2023
Time: 15:02
Status: #✏️
Tags: [[CS50]]

----

Compiler
this is a software that turns programming languages into machine code or binary that you computer can read.

compiling process
1. preprocessing - find and replace.
```C
 #include <cs50.h>
 #include <stdio.h>
```
This is where you process the libraries for the prototypes of the functions you are going to use in the program you made. The program trust that you have the files somewhere in your storage device and gets the functions from those libraries.
   
2. compiling
Turns your programming language into assembly language, it is the lowest level of programming language before its binary.
![[Pasted image 20230727154235.png]]
This are assembly instructions, these are the instructions that are give from the memory to the processor. 

3. assembling
   Assemble the assembly instructions into binary.
   
4. linking
   Links all the binary codes of the 2 libraries, and your code, to make 1 sequence of machine language. 


Debugging

bug - a mistake in your code. 

Print method
Goal: make a 1x3 vertical block tower using hashes
code
```C
#include <stdio.h>
int main(void)
{
	for (int i = 0; i <= 3; i++)
	{
	printf("#\n");
	}
}
```

Running this would yield:
```
#
#
#
#
```

The simplest way to solve this is using printf. 

This code
```C
#include <stdio.h>
int main(void)
{
	for (int i = 0; i <= 3; i++)
	{
	printf("i is %i\n", i);
	printf("#\n");
	}
}
```

would print out:
```
i is 0
#
i is 1
#
i is 2
#
i is 3
#
```

Now you can see the problem that the computer is counting more than it should, so now you know that you have to adjust the i <= 3 to solve the problem.

Debugger method
Runs the execution of the code one step at a time. This lets you do automatically the previous debugging process. 

Rubber Duck Method
Talking to someone or something about running the code that you are trying to debug. By doing this, you will eventually realize illogical logic that you first thought was logical. 


Type

| Data type | Bytes taken |
| --- | ---|
| bool | 1 byte |
| char | 1 byte |
| double | 8 bytes |
| float | 4 bytes |
| int | 4 bytes|
|long | 8 bytes |
| string | ? bytes |

Data types takes up space in memory. 

Visualization:
![[Pasted image 20230728154210.png]]
This is how data types in a program would take up space in memory. One box is a byte.

Lets test this out in a program:
```C
#include <stdio.h>

int main(void)
{
	int score1 = 72;
	int score2 = 73;
	int score3 = 33;

	printf("Average: %f\n", (score1 + score2 + score3) / 3);
}
```

However this will not work, because all number participating are not floating point values, you could solve this by converting the 'int' into 'float', but you could also just turn the 3 into 3.0 to make it so that it is a floating point value.

```C
#include <stdio.h>

int main(void)
{
	int score1 = 72;
	int score2 = 73;
	int score3 = 33;

	printf("Average: %f\n", (score1 + score2 + score3) / 3.0);
}
```

Output:
```
Average: 59.333333
```


The problems with this code, is that you cannot change the scores, you cannot add more scores and that you cannot modify the denominator to get the average. 

Representation of how the data is stored in the RAM:
![[Pasted image 20230728155752.png]]

or 

![[Pasted image 20230728155851.png]]


Now to fix the ugly code from earlier, we can use arrays to store and recall the data.

Arrays is a type of data that makes it so that you can store the same data type with different values but one name. 

This is an array
```
int scores[3];
```

An array's purpose is to remove having different multiple variable names for the same thing. 

This can store 3 integers, as said by the number inside the bracket. 

So to assign values  you need to:
```
int scores[3];
	scores[0];
	scores[1];
	scores[2];
```


To use this in the code:
```C
#include <stdio.h>

int main(void)
{
	int scores[3];

	scores[0] = 72;
	scores[1] = 73;
	scores[2] = 33;

	printf("Average: %f\n", (scores[0] + scores[1] + scores[2]) / 3.0);
}
```

This doesn't solve all the problems, but this is good way to show how arrays work. Now we can use get_int to get the values for the arrays.
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int scores[3];

	scores[0] = get_int("Score: ");
	scores[1] = get_int("Score: ");
	scores[2] = get_int("Score: ");

	printf("Average: %f\n", (scores[0] + scores[1] + scores[2]) / 3.0);
}
```

Now this will allow you to place now value. But this could still be better, but you can use a for loop to do this better
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int numb;
	int scores[3];
	for (int i = 0; i < 3; i++)
	{
	scores[i] = get_int("Score: ");
	}

	printf("Average: %f\n", (scores[0] + scores[1] + scores[2]) / 3.0);
}
```

Now this can still be better, by now asking the user how many scores do you want to input.
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	int n = get_int("How many scores?" );
	int scores[n];
	
	for (int i = 0; i < n; i++)
	{
	scores[i] = get_int("Score: ");
	}

	printf("Average: %f\n", (scores[0] + scores[1] + scores[2]) / n);
}
```

Though this still won't become larger with each addition of your score.



A string is just an array of characters . Where in you can individual can get the characters from a string by calling each character like how you would an array.

Example
Program:
```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	string s = "HI!";
	printf("%i %i %i\n", s[0], s[1], s[2]);
}
```

Output:
```C
72 73 33
```

Now when you place a string in memory it should look like this:
![[Pasted image 20230728165243.png]]

To add more characters next to it, but without it interfering with the next you will have to use a null character or a special character/ sentinel character, or '\n' in the C programming language, or a bit with only 0s in RAM. In a deeper programming language it is '\0' not '\n'.

Which would look like this:
![[Pasted image 20230729160750.png]]

A null value does waste a bit, but it does denote the end of a string, and since RAM is plentiful these days this isn't a problem. 

```C
#include <cs50.h>
#include <stdio.h>

int main(void)
{
	string name = get_stirng("Name: ");

	int i = 0;
	while (name[i] != '\0')
	{
		i++;
	}
	printf("%i\n", i);
}
```

This program shows how many character a string has.

Output:
```
Namme: HI!
3

Name: BYE!
4

Name: David
5
```


```C
#include <cs50.h>
#include <stdio.h>

int string_length(string s);

int main(void)
{
	string name = get_string("Name: ");
	int length = string_length(name);
	printf("%\n", length);
}


int string_length(string s);
{
	int i = 0;
	while (s[i] != '\0')
	{
		i++;
	}
	return s;
}
```
This does the same but much cleaner


This code is a code that prints out Strings.
```C
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Input: ");
	printf("Output: ");
	for (int i = 0; i < strleng(s); i++)
	{
	printf("%c",s[i]);
	}
	printf("\n");s
}
```
However, this code is not its most efficient, due to string length being constantly called.

This can be fixed by using an int variable to make it so that you only call it once.
```C
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Input: ");
	printf("Output: ");
	int length = strlen(s);
	for (int i = 0; i < length; i++)
	{
	printf("%c",s[i]);
	}
	printf("\n");s
}
```


But you can declare multiple variables inside for loops, so you can add the declaration of the length variable in the for loop.
```C
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Input: ");
	printf("Output: ");
	for (int i = 0, n = strlent(s); i < n; i++)
	{
	printf("%c",s[i]);
	}
	printf("\n");s
}
```

This is now more efficient and looks better.


This program turn strings into capitals:
```C
#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Before: ");
	pritnf("After: ");
	for (int i = 0, n = strleng(s); i < n; i++)
	{
		if (s[i] >= 'a' && s[i] <= 'z')
		{
			printf("%c", s[i] - 32);
		}
		else
		{
		printf("%c", s[i]);
		}
	}
}
```


Though to make it simpler, you can use another library and function:
```C
#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Before: ");
	pritnf("After: ");
	for (int i = 0, n = strleng(s); i < n; i++)
	{
		if (islower(s[i]) !=0)
		{
			printf("%c", s[i] - 32);
		}
		else
		{
		printf("%c", s[i]);
		}
	}
}
```

You can also use another function to make this significantly shorter:
```C
#include <cs50.h>
#include <ctype.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
	string s = get_string("Before: ");
	pritnf("After: ");
	for (int i = 0, n = strleng(s); i < n; i++)
	{
		printf("%c", toupper(s[i]));
	}
}
```



Command-line arguments

```C
#include <stdio.h>

int main(void) //(void) does not take command-line arguments
{

}
```

command-line arguments 
-> Words after the command you type in the terminal. 


```C
#include <stdio.h>

int main(int argc, string argv[])
{

}
```

int argc - how many words the user has typed in the terminal which will be taken from argv.

string argv - the array of all the characters the user has typed din the terminal.


Example code:
```C
#include <cs50.h>
#include <stdio.h>

int main(int argc, string argv[])
{
	printf("Hello, %s \n", argv[1]);
}
```

How you open it:
```
./argv Rafael
```


This outputs:
```
Hello, Rafael
```

Doing command-line arguments makes it so that you can input things so much faster compared to taking input from the terminal. 



Exit status
This is a way for the program to stop when something unintentional or something went wrong.

Example of a program with an exit status.
```C
#include <cs50.h>
#include <stdio.h>

int main(int argc, string argv[])
{
	if (argc !=2)
	{
		printf("Missing command-line argument\n");
		return 1;
	}
	else
	{
		printf("Hello, %s\n", argv[1]);
		return 0;
	}
}
```

Return 0 will always say that there is nothing wrong with the execution of code, and if you don't place the return 0; the program will always return 0;



Cryptography

Where you send a text or information where you have scrambled it in such a way that when someone tries to read it, they won't be able to understand it. Only the person who knows the method the the scrambling would understand. 

![[Pasted image 20230731130726.png]]
You can also use the same logic in programming in cryptography.

But in most cases you use two inputs.
![[Pasted image 20230731130841.png]]

They key is what you and the recipient/sender agree upon the meaning of the cipher.


