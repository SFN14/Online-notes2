---
Type: College Notes
Subject: CC103
---
Date: 10-25-2023
Time: 17:53
Status: #✏️
Tags:

----
# The iterative constructs
This is where you repeat a given block of statements over and over again for a given number of times.
## There are three types of iterative constructs.
1. The While ... loop
2. The For loop
3. The do .. while loop

# Characteristics of Well-Behaved loops
1. Control Variable -> its value determines how many iterations the loop will have. It should have an initial value or the value will be input. (Also known as a counter).
2. Loop testing -> a loop should test the value of the variable to determine whether iteration is necessary. 
3. Loop control -> statement that changes the value of the control variable to ensure that the loop will not iterate infinitely. 

# While loop
Continually executes a block of statement while a particular condition is true. This will not run the program if the condition is not met already.

The condition is tested first then run.

```Java
while(condition)
{
	statement(s);
}
```
example:
```Java
import java.util.Scanner;
public class enter {
    public static void main(String[] args)
    {
        Scanner x = new Scanner(System.in);
        
        int value, temp=0;
        System.out.print("How many number would you like to add: ");
        int num = x.nextInt();

        System.out.println("Enter the " +num+ " numbers :");

        int i = 0; //control variable
        while(i < num) //loop testing
        {
            value = x.nextInt();
            temp += value;
            i++; //control loop
        }
        System.out.println("Total: "+temp);
    }//main
}//class
```

# Do-while loop
Do this, while this condition is true. the program will be executed at least once then if the condition is met, do it again, else stop.

The program is run, then condition is tested after

```Java
do
{
	statement();
}
while(condition);
```
