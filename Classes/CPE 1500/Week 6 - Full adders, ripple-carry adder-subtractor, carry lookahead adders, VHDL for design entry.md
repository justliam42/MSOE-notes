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
