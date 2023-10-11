#### Adders (full, ripple, fast)
- addition is the fundamental arithmetic operation
	- we can create subtraction (adding the negative)
	- we can create multiplication (repetitive addition)
	- we can create division (repetitive subtraction)
 - numbers being added together become A and B and carry C
	 - bit slices of the total calculation ?
- when the carry is included in the input, the circuit is a **full adder**, otherwise it is a **half adder**
- C<sub>out</sub> is BC + AC + AB
- Sum is canonical, or 3 (2 2 input) XOR gate

#### Ripple Adder
The carries are called the carry chain or the carry cascade
rest is ez


VHDL is IEEE 1076

--10/6/2023--

groups of signals are: cable, bus, group, or vector



--10/9/2023--
Busses do be kinda nice (just remember to label them)
Quartus declares buses with A\[3..0] or so 
output bus be the same 


Idealized behavior (functional wit no delay)
Real gates exhibit delay

Each gate has some delay in time (delta t)
The delay time is the propagation delay

the longest path is the critical path because it is the slowest or something
therefore the whole circuit has a propagation delay

*for today lets assume all gates have T<sub>pd</sub> the same

so in a ripple carry adder it gets progressively slower the more full adders are added

so in a n-bit ripple carry adder, stability occurs at 2\*n\*delta where delta = t<sub>pd</sub>
	The delay time is linear with a slope of 2\*t<sub>pd</sub>

complexity is O<sub>rder</sub>(n) or it grows with n

--10/11/2023--
#### Carry-lookahead adder hahaha 

Normal COUT = AB + AC + BC
or A<sub>0</sub>B<sub>0</sub> + A<sub>0</sub>C<sub>0</sub> + B<sub>0</sub>C<sub>0</sub> 
and et cetera increasing the position
aka C<sub>i+1</sub> = A<sub>i</sub>B<sub>i</sub> + A<sub>i</sub>C<sub>i</sub> + B<sub>i</sub>C<sub>i</sub> 
or C<sub>i+1</sub> = A<sub>i</sub>B<sub>i</sub> + C<sub>i</sub>(A<sub>i</sub> + B<sub>i</sub>)

So we Let A<sub>i</sub>B<sub>i</sub> = G<sub>i</sub>
and (A<sub>i</sub> + B<sub>i</sub>) = P<sub>i</sub>

so C<sub>i+1</sub> = G<sub>i</sub> + P<sub>i</sub>C<sub>i</sub>

![[20231011_083908.jpg]]

So 
![[20231011_084232.jpg]]