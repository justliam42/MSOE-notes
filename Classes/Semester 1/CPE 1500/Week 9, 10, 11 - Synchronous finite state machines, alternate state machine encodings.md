--10.25.2023--

Finite State Machines (FSM)
- Sequence through numbers in time
- numbers stored in memory
- stored numbers represent the ***state*** of the machine

**State**: a stored number representing a place in time.

Moore Machine
- At the heart of the Moore machine there is a n-bit storage register.
- In front of the ***State Register*** is a ***Next State Logic*** block which may have inputs
- The output stored state also feeds back into the next state logic block
- What is held in memory is called the ***Current State*** Q
- What is held as the data input is called the ***next state***
- Finally, the output is the output logic and output k
![[20231025_081546.jpg]]


Mealy Machine
- Will look almost identical to the Moore Machine but:
- The inputs also feed into the output logic (think line from input to output logic block)
- Basically output is dependent on everything available, as opposed to just the register



**State Bubble Diagram**
- The name of the state name on top (T0, T1, etc)
- at the bottom is da outputs
- A departure from this state is represented by a graph arc (representing the clock)
- Like a flow chart or something
**State Table**
-  Outputs get both the next-state D and the output
- Inputs are state
![[20231025_083714.jpg | 300]]
**Truth Table**
- Based on number of input states, calculate how many bits needed
- Truth table looks like State table but translate to bits or something
![[20231025_084023.jpg | 300]]
- 


--10.27.2023--
	some vhdl for a garage opener

```vhdl
library ieee;
use ieee.std.logic.1164.all;

enitity GDOOR is
port(
	O,C,RST,CLK: in std.logic;
	M,D: out std.logic)
end entity GDOOR;

architecture MOORE of GDOOR is
	type states is (wai,o1,o2,o3,o4,d1,d2,d3,c1,c2,c3,c4);
	signal D,Q: STATES;
	 -- vhdl makes the appropriate amt of bits here
	begin 
		--next state logic
		D <= o1 when 0=wai and o='1' else 
			o2 when Q=o1 else
			o3 when q=o2 else
			o4 when q=o3 else 
			-- ... teehee agag
	
```

--11.10.2023--
### Counters
- Standard n-bit binary
	- 0, 1, 2, ... (2<sup>n</sup>-1) and repeats. 
	 - 2,<sup>n</sup> clock periods
- Binary coded decimal
	- 0, 1, ... 9 and repeats
	- 10 clock periods
- modulo-n
	- gets modulo n from a counter
	- from 0 to n-1 and repeat
- n-bit gray code
	- one bit changes at a time
	- start with columns
	- first column is 01 then mirrored down
	- second column is 0011 then mirrored down etc.
	- so each is n 0s and n 1s
- n-bit one hot
	- one hot is only one is active at a time
	- 001 010 100 001 010 100 for 3-bit
	- so 1,2,4, ... 2<sup>n</sup>-1
	- can be one-cold

--1.13.2023--

- Standard counters roll over and start again
- Directionality can be added. Up and down counters exist.
	- Up Counters
	- Down Counters
	- Controllable Up/Down counters are common
		- Exe:  74191
- Saturation can be added (so opposite of standard mentioned earlier)
	- The counter locks in its final directional state - holds its final directional value

State the name of a counter this way:

n-bit {standard, saturated} {direction} {type} counter

0 -> 12 12 12 ...

--11.15.2023--

EMI can cause bits to flip so we determine wat to do or somthn

for ERROR states, you can either self correct or lock in the error (and effectively shut down the system)


--11.17.2023--
complex programmable logic device (CLPD)

--11.20.2023--

Instruction Processor 

A processor is a machine that interprets and executes an instruction
- finite state machine interprets a  binary number as a command request and executing that command
- Von Neumann did things
	- Extended moore machine with an added program memory
	- A moore machine is in front of it as an instruction counter
	- the program counter pulls specific time in memory that ends up outputting
	- With a program counter, we can fetch commands and stuff
	- ARM is pretty widely used

--11.21.2023--

### Acceptor machine
- an acceptor monitors for an input pattern through time
- if the pattern is seen, it accepts it, and reports true
- If pattern is 0110:
	- Acceptor identifies pattern as F(ound)0, F01, F011, F0110 etc
	- Once the F0110 exists, Y is put to true, and pc starts accepting the packet (:
- If pattern is not found, the acceptor enters a ERR/REJECT state.
- In the acceptor state the state diagram gets a double circle
- 