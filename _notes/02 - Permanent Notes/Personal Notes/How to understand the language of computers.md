Date: 07-17-2023 
Time: 20:08
status: #📝 
Tags: [[CS50]] #personalnotes 

# Summary
Binary numbers are just 1s and 0s, even putting them in a pattern will mean nothing if you don't give it meaning. So the meaning of 1s and 0s will change depending on the context we are using, like displaying images, video, making sounds and others. The software has to give context to the computer so that it knows what to do with the bytes you give it.

## How Letters are Displayed with Numbers
Since Binary numbers are just a pattern of 1s and 0s, we have to give it meaning, [[What is Computer Language|we have used binary to represent the patterns of 1s and 0s into numbers]], but we could also use them to represent letters. There is already a standard to show letters using Binary, and it is called ASCII or American Standard Code for Information Interchange. 
![[Pasted image 20230717113659.png]]
*ASCII Chart*

### ASCII
To use ASCII you would need to use 1 Byte or 8 [[Bits]], so that you would have 255 characters (Though initially ASCII used 7 bits, then used 8, which is called extended ASCII). However, there is more that just English as a language, so a new standard was made do accommodate that, and its Called Unicode.
### Unicode
Unicode is just the same as ASCII, Unicode is even backwards compatible with it, but it just adds more characters to be used. From the 8 Bit of ASCII, it became 16 Bit in Unicode, meaning that it can display ~65,000 characters and it can even go to 32 Bit, which is roughly ~4 Billion characters.
However, sometimes one character in one device, will not look the same in another, this is because what is on that assigned number of a character will stay the same but the interpretation of who implements the Unicode to the device will differ, that's why we can interpret the same character differently, this is especially prevalent in emojis.

## How Can a Computer Display Colors
We often use RGB to display colors in a screen, RGB referring to the colors of a pixel in a scree, Red Blue Green. Again, we can use the concept of using 8 [[Bits]] to control the output of the individual RGB in a Pixel. We would use the numbers 1 - 255 in 8 [[Bits]] that we have and assign those to the visibility of the color. 

![[RGB color]]

Look at no. 1, first is that we assign values in each of the colors, R is 224, G is 49 and B is 49. Think of this as how bright they're outputting the color. Then when the colors at outputted by the LED in the pixel, they get mixed together and you get the color that you wanted. Now if we combined multiple pixels together, we will be able to make an image using Bytes. 

The higher the [[Bits|bit]] the color is, the more control there is in outputting the color, therefore it is more accurate. The way that the colors are displayed will vary depending on the color space, because there are multiple standards that are used in different applications. 

## How Can a Computer Show a Video Using Bytes
Since we have established that images are just controlled by bytes, we could also use that concept in video we just have to take into account time. So what happens is that, we display an image or in this case, a frame, every few seconds. Because technically video is just moving images, so we just change the pixel's color in accordance to the frame that we want to show. It could be 24 frames, 30 frames, 60 frames, 120 frames and so on and so forth. The amount of images shown depends on the performance of the computer and the display itself. 

## How Can a Computer Turn Audio into Bytes
We would just use the concept that we have established earlier, that we can just assign the values we have from binary into, in this case, notes, or sound. So when we press a key on a MIDI keyboard, it turns notes into bytes. You can turn analog information like the duration of a note, the hardness pressed by a key into a digital bytes, that can be used and interpreted by computers. 

## Computers Have to have context to use Bytes properly
For a computer to use bytes, you have to say where it will be used. Because a 64 Bit computer will have a hard time to know what the Bytes you gave it mean if you don't give context on where it will use it. Will it use it on making colors? videos? images? text? and such. We cannot assign a pattern of byte to everything, because that would just make things too difficult, imagine using a 256 Bit computer, and designing a processor to process all the information in very tiny places, it would be very hard. That's why we use a smaller amount of Bits and just contextualize it. 