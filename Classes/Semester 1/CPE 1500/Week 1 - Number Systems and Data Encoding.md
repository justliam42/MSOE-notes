-- 8/28/23 --
computer engineering is the moving of energy around to compute

Voltage - named after Volta

- Voltage
    - electrical potential energy
    - unit is volts (V)
    - if we close a switch the voltage increases as it is potential energy
- current
    - dynamic kinetic electrical energy
    - unit: amperes (A)
- switching polarity of voltage changes direction of current

see picture*

- these plots are real valued functions
- infinite number of measurable values
- analog electrical signal
- one way to do numbers is by using voltages representing different numbers (analog)
    - problem with this approach is precision and speed
    - this is analog
    - have to generate between 0-9 volts cleanly without noise and identify the volts (in base ten)
        - or do this with amps which slows down behavior
- so we use 0 or 1 (digital abstraction)
    - binary time woot woot
    - battery with a switch instead of generator with infinite possibilities
    - asking if it is on or off is a very fast ting
    - this is **digital signal**
    - negative volts is off (maybe)
    - off-on, low V-high V, 0-1, false-true
    - This is the **digital abstraction**

we built analog computers for years

binary computers became standard a 1960s

(day one)
![[cpe graphs day 1.jpg]]

-- 8/29/23 --
some ways of stuff makes a sine graph

when electrical potential energy changes, the flow changes directions (vibrating)\
170 volts out of the wall
in real-valued (analog) signals, it boosts or interferes with the wave

ionized chemicals kept separate in a battery creates a positive and negative side. As long as the sides aren't connected, there is no kinetic energy. The when a switch closes the voltage becomes constant. Then we get the square wave. On-off behavior. (discrete behavior)
	- this is countable
	- countable = digital (fingers)
	- digital abstraction
	- 0V - Battery voltage (Vbat)

Battery voltage has historically been 5 volts, could also be 3.3v
 - miniaturization has made battery voltage requirements less (doesn't have to carry the energy as far) 
	  - increases battery lifetime
	  - 
   - instead of recording the voltage, it was decided that it will be 0 or 1

#### Binary things
- Our counting system (base 10)
	- 1000s 100s 10s 1s ...
	- Positional number system
	- any number is a coefficient in that column
	- left is the most significant column

romans be like
I II III IV V


in binary the precision or range is much less for the same number of columns but the advantage of speed and noise tolerance far outweighs that disadvantage

A positional system uses a discrete base set of symbols. 10 symbols is base 10, 2 symbols is base 2
much of binary stuff was made by george bool (boolean)

binary digit = bit
- is either 0 or 1

- unsigned n-bit number line

precision of binary becomes [0,(2^n)-1]
unsigned precision table
| bit length | range               |
| ---------- | ------------------- |
| 4 bit      | [0,15] (nibble)     |
| 5 bit      | [0,31]              | 
| 6 bit      | [0,63]              |
| 7 bit      | [0,127]             |
| 8 bit      | [0,255] (byte)      |
| 9 bit      | [0,511]             |
| 10 bit     | [0,1027]            |
| 11 bit     | [0,2047]            |
| 12 bit     | [0,4095]            |
| 13 bit     | [0,8191]            |
| 14 bit     | [0,16383]           |
| 15 bit     | [0,32767]           |
| 16 bit     | [0,65535]           |
| 32 bit     | [0, 4+billion]      |
| 64 bit     | [0, 18+quintillion] |
first commercial processor 1971 intel 4001 or something. 4 bit processor
a year later they used 8 bit processor

in ISO 80000, the 8-bit value has the unit byte. This is the only standardized unit of bits
01001100 -> 76 01011001

DIV-BY-BASE
- ex: div-by-2
	- write long-division upside-down idk
	- keep dividing by two and remainders become the backwards moment

128 + 32 +16 + 8 +4 +2 +0
10111110<sub>2</sub>


nibble (not standard) 4-bit (potentially nybble)


-- 8/30/2023 --
minimum number of bits to represent decimal number X is 
	n = ceil(log<sub>2</sub>x)
	aka 2<sup>?</sup> = x
	![[20230830_082840.jpg|500]]

Writing in binary is annoying, therefore we write in octal, which is now deprecated, so we write in hexadecimal

In programming, hex is written is 0x FFFF...
- means the 0 is written in x (hex)
each nibble can be represented as one hex character

-- 9/1/23 --

##### Addition
- 1st grade rules appy:
	- 0+0 = 0
	- 0+1 = 1 ...
	- Carry when result is greater than or equal to 10 (base)
	- Binary carries when result is greater than one

| equation  | c   | s   |
| --------- | --- | --- |
| 0 + 0     | 0   | 0   |
| 0 + 1     | 0   | 1   |
| 1 + 1     | 1   | 0   |
| 1 + 1 + 1 | 1   | 1   |

suitable to show:
![[20230901_082556.jpg|400]]
carry out is a **status flag** that tells us not enough space is there

#### signed numbers

a human might write +1, -1 etc. which takes extra symbols so one might imagine that we would add a sign bit to determine sign

this has 2 zeros and this is a major flaw. it adds much more complexity. It would hace yto monitor for -0 and correct it. *regular implies simple, small, and fast*

##### thus we have the uh uh uh two's compliment![[20230901_084253.jpg| 500]]
most significant bit is -(that bit), then other bits are normal

4-bit unsigned: 0 -> 2^(n-1)
4-bit signed:  -2^(n-1) <- 0 -> 2^(n-1) - 1

converting to negative -> invert all bits + 1