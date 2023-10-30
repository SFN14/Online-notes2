---
Type: College Notes
Subject: CC103
---
Date: 10-25-2023
Time: 16:34
Status: #✏️
Tags:

----
# If Statements

The logic
```Java
if(condition) 
	true statement; //this will be read and will be executed

false statement; //this will execute if the condition is not met
```

or

```Java
if(condition)
{
	true statement; //However is best practice to put everything in curly braces
	true statement;
	true statement;
}
else //this is when the condition fails;
{
false statement; 
}
```

Example:
```java
import java.util.Scanner;
public class calculator
{
	public static void main(String[] args)
	{
		Scanner inp = new Scanner(System.in);
		int n1, n2, operation;
		String choice;
		
		System.out.print("Input First Number: ");
		n1 = inp.nextInt();
		System.out.print("Input Second Number: ");
		n2 = inp.nextInt();
		inp.nextLine();
		
		System.out.print("input operation (m, d, a, s): ");
		choice = inp.nextLine();
		

		if(choice.equals("m")||choice.equals("M")) // .equals is used rather than == or = this is because what you are testing is a string rather than an integer.
		{
				operation = n1 * n2;
				System.out.print("Product: "+operation);
		}//block for multiplication
		else if(choice.equals("d")||choice.equals("D")) //use 'else if' for the second question and onwards, do not use another if, it will break the program, promise.
		{
				operation = n1 / n2;
				System.out.print("Quotient: "+operation);
		}//block for the division
		else if(choice.equals("a")||choice.equals("A")) //you can use || here so that you can test for two strings, of one of them becomes true, then it will do the block of code.
		{
				operation = n1 + n2;
				System.out.print("Sum: "+operation);
		}//block for the addition
		else if(choice.equals("s")||choice.equals("S")) 
		{
				operation = n1 - n2;
				System.out.print("Difference: "+operation);
		}//block for the subtraction
		else //this block will be ran when all preceeding else-if statements do not meet the conditions of the past 
		{
				System.out.print("You have input an invalid operator, please use m, d, a, s,");
		}//block for when the condition isn't met
		System.out.println("\nProgram closed...");
		
		
		
	}
}
```

# Escape Sequence
```java
System.out.print("CICT"\n"\BSIT\"") //the \n\ denotes that its an escape sequence and that anything inside the quote and backslash after will be on a new line.
```


Note: you can make a variable when you need it.

Note(2): for the exam you can use a pencil to know what is the problem with the programs.

# Other syntaxes
## Assignment Operator
instead of using
```Java
operator = operator + 1;
```

you can use
```java
operator += 1;
```

you can also use this with other operators
```java
operator -= 1;
operator *= 10;
operator /= 2;
operator %= 75;
```

## Increment
to add one to a variable
```java
++value; //this adds one to a number in memomry and is also the output. (pre increment)

value++; //this number adds one to the number in memory first then outputs the previous number if you immediately display it. (post increment)
```

## Decrement
to minus one to a variable
```java
--value; //this minus one to a number in memomry and is also the output. (pre decrement)

value--; //this number minus one to the number in memory first then outputs the previous number if you immediately display it. (post drcrement)

```

# Switch Statement
Dispatches the control to the different parts of the code based on the value of a single variable or expression.
Values is compared to the literal values in the case statements.
This is like an if statement, this is used to validations, if the statement isn't true then the program won't go through.
Most of what you can do with an if-else statements can also be done with switches.

## Difference vs  If-else if
Only uses one variable for comparison.
You cannot use conditions like > or < etc. in switch.


how to use switch
```Java
switch(num) //num = variable name
	case 1: //you don'thhave to order the cases, but you can order it for readability
	{//if true do this
	statements;//add
	break; // tells the program to stop after the condition is met;
	}//if not true, then skip the block then do the next case
	case 2:
	{
	statements;//multiply
	break; //if you don't place a break, it will do the case 2, 3 and onwards.
	}
	default: //this can be placed anywhere
	{//if all other cases are not met, then this is what is run in that case. This is basically the equvalent of else.
	statement;
	break;
	} //you can, not include a default but not recommended. 
	
```

you can use also "charAt(0)" to say that you want to read the first character of a string so that you can input it and read it (choice.charAt(0)), you can also use this with char. this is looking at the string at index 0, so that you can use it as a char.

```Java
switch(choice)
case "A";
case "a";
{
statement();
}
else
{
statement();
}
```

Converting a string to char
```Java
String choice;
switch(choice.charAt(0))
{
	case '1':
}
```

getting a char from scanner
```Java
Scanner x = new Scanner(System.in);
char choice;

choice = x.next().charAt(0);

switch(choice)
{
	case '1':
}
```

Lab:
simulate phone 
if program is run (Program LAB)
there should be a load
and charge
Press 1 - 8
if you in put:
1: send sms (requires a number) after being sent, then minus load and charge to all
2: check missed called minus 1 load and 2 charge
3: call a number (minus load 5 and 3 charge)
4: reload (adds a cellphone load, only adds 5 load) (max load is 15 and charge is 10)
5: recharge (adds 5 to load)
6: back to menu (redisplay menu)
7: balance inquiry (shows current load and charge)
8: exit the program

make your own interface

include classname: PerezRaf

send both the class and java

# Difference of [[Chapter 3 Conditional#If Statements||If]] and [[Chapter 3 Conditional#Switch Statement||Switch]]

## if statement 
Uses condition and a statement.
```Java
if(num==1)//if false skip this 
{
	statement;
}
else if(num=2)
{
	statement;
}
else if(num=3)
{
	statement;
}
else //if all else is false, then do this
{
	statement;
}
```
Finds a condition in the program before the if statement, then does something after the program gets the condition it wants.

## Switch statement
Uses a switch and an object name inside, and uses cases to know which outcome you want
```Java
switch(num)//which variable/object to look for
{
	case 1://first condition
	{
		statement;
		break;
	}
	case 2:
	{
		statement;
		break;
	}
	case 3:
	{
		statement:
		break;
	}
	default://if nothing applies, do this
	{
		statement:
		break;
	}
}
```
In switch, the program is looking at one variable/object and finding a certain outcome it wants, and do something after it.