07-14-2023 07:13
status: #📄 
Tags: [[Processor]]

# Summary 
To determine Processor Performance look at the CPU Clock Speed, IPC, Amount of Cores, Threads, and Cache it has. But only do this to [[processor]]s with similar [[microarchitecture]]s. To determine performance of a processor with different [[microarchitecture]] and [[processor architecture]], use [[Benchmarking software]] to see the difference.

# How do you determine Processor Performance?
To determine Processor Performance you could look at the specifications to determine its performance, specifications like:
1. CPU Clock Speed or Frequency - This refer to how many cycles (the tick of the internal clock of a processor) per second a processors does. It is usually measured in Giga Hertz or GHz.
2. IPC or Instructions Per Cycle - This determines how much instructions per tick of the internal clock a processor does.
3. Amount of [[Processor Core|Core]] - This refers how many [[Processor Core]]s or brains are present in a computer, more usually means better multitasking performance.
4. Amount of [[Threads]] - This usually refer how many virtual cores are detected per [[Processor Core|Core]] of a processor. 
5. Amount of [[Cache]] - This refers to how much cache a processor will have, measured in MB.
Usually the more that a processor has of these specifications, the faster it will be. But, you cannot compare these specifications against different [[microarchitecture]] and [[processor architecture]]. These specification is done to compare [[processor]]s with the same [[microarchitecture]], of the same generation, but other than that, it is not usually reliable.

## How to you properly determine Processor Performance?
To determine Processor Performance you would need [[Benchmarking software]]s to have a value to compare the performance of a processor to another with a difference [[microarchitecture]] and [[processor architecture]]. You could also use the Frames Per Second of a game with two different processors, however this is not as reliable. 

## Other Factors affecting Processor Performance
Other components could also affect the performance of the processor, components such as the [[GPU]], [[RAM]], and [[Storage]]. This is due to the rate at which component operate, if one component is slow, the whole computer will wait for that component to finish and send the required information the other component needs, this is called [[bottle necking]]. [[bottle necking|Bottle neck]]s don't usually happen in every software, due to the different needs of each software. A software that uses mostly the processor will not be affected by a slow [[GPU]] and vice versa. 

# References
https://www.intel.com/content/www/us/en/gaming/resources/cpu-clock-speed.html
https://www.tomshardware.com/news/clock-speed-definition,37657.html
https://superuser.com/questions/239178/cpu-speed-and-cycles