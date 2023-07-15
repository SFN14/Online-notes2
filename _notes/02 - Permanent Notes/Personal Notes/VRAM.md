07-14-2023 21:59
status: #📝
Tags: [[Graphics Processing Unit]] [[RAM]] #personalnotes 

# Summary 
VRAM is a special type of [[RAM]] where textures are temporarily stored so that the [[Graphics Processing Unit|GPU]] can immediately access it. 

# What is VRAM?
Video Random Access Memory or VRAM is a special type of [[RAM]] that [[Graphics Card]]s use to temporarily store information like how a normal [[RAM]] functions. But the type of information stored is what is different, the information stored in VRAM is mostly textures of games or software. These textures may refer to images used for texturing like in old 2D games or polygonal 3D models used in 3D software or games. The textures mostly come from the storage of the computer, where the software or game is stored.

# Why don't the Graphics Card and Processor just share the computer's RAM?
VRAM is part of the [[Graphics Card]], therefore closer to the [[Graphics Processing Unit|GPU]], which means that data will be able to go to the VRAM and to the [[Graphics Processing Unit|GPU]] much faster. If the [[Graphics Card]] where to share memory with the [[Processor]], the system memory could run out quickly and make the whole computer run much slower. Long with that, the [[Graphics Card]] is physically further away from the [[RAM]], which would cause a lot of delay, making the computer much slower. The only reason on why [[Accelerated Processing Unit|APU]]s work is because the [[Processor]] and [[Graphics Processing Unit|GPU]] are in the same place, which would mean that the distance from the ram would not affect the [[Graphics Processing Unit|GPU]] too much, however running out of [[RAM]] is very much a possibility, specially with systems with low [[RAM]].

# What happens if you don't have enough VRAM?
If you don't have enough VRAM, you will suffer the same issues as not having enough [[RAM]]. You will feel a lot of lag when playing a game or using a software, and especially stutters. This is because the VRAM is constantly replacing its contents to get the data of new incoming data, and the [[Graphics Processing Unit|GPU]] cannot get the information immediately, because the texture it needs would be going in and out of VRAM. To combat this, you should lower the settings of the game or software, such as render resolution or texture quality, to lower the usage or VRAM.

# References
https://www.howtogeek.com/781787/what-is-vram/