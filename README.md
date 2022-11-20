# JAWS
A recreation of Joseph A. Weisbecker's FRED hobby computer from 1971.  Why Jaws?  Joseph A. Weisbecker - SuperHero.



In 1970/71 Joseph A. Weisbecker built a hobby computer from standard TTL and nicknamed it FRED (Flexible Recreational & Educational Device). It had a video display, a cassette interface and a punched card reader. He demonstrated it to his bosses at RCA and eventually in 1975 it was integrated into a 40 pin CMOS chip, that is better known as the RCA CDP1802.

Fortunately, Weisbecker documented his project well, and full hand drawn schematics are available as a lasting historical document, now 50+ years old. Very few microprocessors from the 1970s began life as TTL prototypes and very few of the architectures are in the public domain.

http://www.cosmacelf.com/publications/books/system-00-manual-orig.pdf

I have taken these schematics and created a reproduction of the FRED CPU, that will run in the "Digital" simulator by H. Neemann - available here on GitHub.

It's a work in progress, and I expect to have to correct numerous mistakes. If you are an 1802 enthusiast or even a complete newcomer to CPU architectures, I hope that these simulation files will be of use to you.

The original FRED from 1971 used 74151 multiplexers to allow data from several different sources to be put onto the databus.

A revised version of FRED from 1972 used multiple open collector NAND gates (7401) to perform the same function. My simulation used this latter approach.

Some of the original chips used in FRED are obsolete and difficult to find. This includes the 74181 ALU and the 7489 16 x 16-bit memory. The simulation uses these original devices, but future versions will use modern, available components.

Where the 7404 hex inverter was used I have substituted the 74540 octal inverter.

The 74154 1 of 16 decoder is also obsolete, so I have substituted a pair of 74138, 1 of 8 decoders.

The original FRED used 7475 and 74175 quad flipflops. In some cases I have substituted these for the more modern 74173.

About 25% of the chips used in FRED are basic gates, NAND, NOR, AND, OR. and inverters, 7400, 7401, 7402, 7404, 7408, 7410, 7420, 7427, 7430. They are used for basic control logic and interfacing with the data bus. Modern Tristae devices could reduce a lot of this random logic.

The 74181 4-bit ALU is virtually obsolete, but included here for historical accuracy. A future version will use the ALU based on multiplexers, as used on the Gigatron TTL Computer. Credit to Dieter Muller for this economical ALU design.

#Circuit Description

There are 4 main parts to Joseph Weisbecker's design.  

1.  The register file, consisting of sixteen, 16-bit registers that can be incremented or decremented with an up/down counter.
2.  The 4-bit system registers I (instruction), N, P and X.
3.  The ALU. A pair of 74181s followed by a pair of 7495 shift registers. Much of this is obsolete, and can be replaced with an ALU based on multiplexers - as designed by Dieter Muller and used in the Gigatron.
4.  The control logic.  This is about 25 or 30 basic gate packages often caled "random" logic.  7400, 7402, 7404, 7408, 7410, 7420, 7427, 7430.

The current design stands at about 90 packages. 

I have added the following TTL devices to the "Digital" library. Please download these and add them to your library files.

7475  Quad flipflop

7495  4 bit shift register

74175 Quad D-type flipflops with clear.


