-- 9/22/2023 -- 

##### Multiplexor (data selector)
Traditional (2 input selector):
	Y=D1 if S=1
	D0 id S=0
	 Basically Y(S,D1,D0) = !SD<sub>0</sub> + SD<sub>1</sub> 
  
4-bit input selector:
	Build bigger multiplexer from smaller ones:
	1. build however many 2-input selectors needed
	2. Put them through more 2-input selectors waka waka

7-151 chips have a GO ting... the thing is active when 0
#### New Symbols
Digital power is an upward pointing triangle
Digital ground is 3 progressively smaller lines (downward triangle divided into three)


#### Electronics suppliers
1. JameCo
2. Digikey
 - TI is best supplier
 - Then National Semi-Conductor

9/29/2023
7400 series is commercial
5400 series is military grade (crazy temps, atmosphere, radiation, etc)

#### Decoders 
Decoders takes a small set of inputs and decodes that number into a larger set of outputs
	The corresponding output becomes true goof ah
This means that the decoder is just a canonical complete circuit
also takes an active-low-control signal

#### 7-segment display
Each number is representing one side of the 7-segment display
it could have active-high segments, or it could have active-low segments.
	74XX47 and 74XX48
 - 7-segment decoder
	 - Multiple outputs on for every input row
- outputs connected to 7-segment display
- then would have a set of inputs (traditionally 4-inputs to do hexadecimal)
- ![[20231002_084541.jpg | 300]] 
- a-g clockwise from the top
- the numbers are right-adjusted in their field
- hex: ![[20231002_085030.jpg | 200]]


#### Adders (full, ripple, fast)
- addition is the fundamental arithmetic operation
	- we can create subtraction (adding the negative)
	- we can create multiplication (repetitive addition)
	- we can create division (repetitive subtraction)
 