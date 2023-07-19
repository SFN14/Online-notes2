Date: 07-17-2023 
Time: 22:03
status: #📝 
Tags: [[CS50]] #personalnotes 

# Summary 


# Algorithm
It is a step by step instruction on how to solve a problem or set of instructions on solving a problem. This is usually done by using your logic or intuition to make a step by step plan to solve a big problem, so that it takes less time to solve it the natural or longer way. 

## An example of this is:
Problem: Finding a name in a phone book
Solution 1: Flipping the book pages 1 by 1 to find the name you are looking for. (The longway)
Solution 2: Flipping the book every 2 pages to find the name you are looking for. (Problematic, you could skip the person you're finding)
Solution 3: Open the book in the center. Use one side, then keep halving the pages you have until you find the person you are looking for. If you can't find them, use the other half, then use the previous instructions. (The Faster way)

## Pseudo Code
This is a way of showing the logic of an algorithm without using any code or coding language, but you do write it out in such a way that it looks like code. But all you need is logic to understand it.

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
Are what you call actions that you do when something unforeseen, unlikely or unaccounted happen. You usually have to think of this ahead of time, so that it doesn't become an issue in the long run.

## Functions
These are actions or series of actions that solves smaller problems and contribute to solving of the bigger problem.

Ex:
The Phonebook problem using 
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