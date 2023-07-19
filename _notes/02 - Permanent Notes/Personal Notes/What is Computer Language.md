Date: 07-17-2023 
Time: 18:13
status: #📝 
Tags: [[CS50]] #💡 

# Summary 
The language of computers is just 1s and 0s and it is called byte. We have to have a standard to know what the pattern of 1s and 0s mean and actually use it. We can represent Binary just like how we represent decimal numbers so that we can use the info that we get from computers. 

# Computer Language
It refers to the language that computers speak in, mainly Binary language. 
Where 'Bi' means two, in this case the computer only uses two things to speak and communicate, this is '1's and '0's.
Computer language is what we use to give the [[02 - Permanent Notes/Personal Notes/Introduction to Computer Science||inputs]] to our computers so that we can communicate to a level that they understand.
But a single '1' or '0' will not do the trick in if we do want to communicate with computers, or rather one single [[Bits|bit]]. We would have to use much more [[Bits|bits]], putting those together in a specific pattern is how we communicate with computers. But, these patterns of bits, in reality don't really mean anything, unless we give it meaning, and agree upon what they mean, to know what the computer is actually outputting. 

## How would we use Binary?
In real life we use binary in computers to denote that something has electricity or something doesn't have electricity. On or off, a 1 or a 0. What any programming language boils down to. 

We could use anything that only has 2 states to communicate in binary like switches or buttons. Though to actually use this concept and get something meaningful we would need a few bits, at least two, but to show more possibilities lets use three. 

## Representing the decimal system  using Binary.
To represent the number 123 (one hundred twenty three), in the decimal system we would
![[Decimalsys]]
from right to left, designate a number to the ones place, tens place, hundreds place, so on and so fourth. Then we times the value to their place then add everything.

We would also use this concept in Binary counting.
![[Binarysys]]
From right to left we would designate the first zero as 1, then the next 2 then the next 4. Now we would do the same, we would times the number we have in binary to the designated number to its place, then we would add them all together, in this case we get two.

Ex:
![[Examplebinary]]

Now we could also replace the base of 2 from earlier to base 10, so that we could use more numbers while using less bits, however, this is much harder to show in computers. So we continue to use Binary because it much to use two states rather than multiple states. 

## How to show more characters in Binary?
As you can see, with only three bits, we can only do until no. 7
because 111 in binary is, 4 + 2 + 1, which is 7. But, we can add more bits, so that we could do more, in which case, we would use 8 bits in total, for 1 Byte. 
with 8 Bits, in total we can have about 256 numbers to show, though we have to exclude 1 because we still have 0, realistically we only have 255, but that's still a lot compared to 7. With this, [[How to understand the language of computers|we could also add letters to display.]] 