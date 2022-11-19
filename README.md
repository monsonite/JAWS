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

I have added the following TTL devices to the "Digital" library. Please download these and add them to your library files.

7475  Quad flipflop

7495  4 bit shift register

74175 Quad D-type flipflops with clear.


