transistor level is lower than the gate level.

circuit stack (hierarchy of hardware and shiz):
Software stack
______
System
Functions
Gate Level
Transistor Level

we start with black box diagram (we don't know what the transistors be doing) so like we input A to not gate and it makes not A

- not gate
	- Becomes not the input... (wow)
	- ![[Pasted image 20230908082309.png | 100]]
	- Logic equation Y(A) = Ā (!A)
	- Not gate could be called inverter, complementer etc...
	- Inverting byte becomes ones compliment 
	- ![[20230908_081536.jpg | 300]]
- Truth table
	- a table with inputs and outputs
	- The inputs must be in order or **I lose Points**
- Logic diagram
	- see picture
	- Typically the most significant bit is on top going down...
- IEEE std 91 
	- the standard for drawing gates
	- see picture

- buffer gate
	- logic equation Y(A) = A
	- ![[Pasted image 20230908082218.png | 100]] 
	- Potential energy at any point along cable weakens the voltage
	- buffers regenerate the signal (think Minecraft repeater)
		- this is critical
	- ![[20230908_082958.jpg | 300]]

- AND gate
	- Y(A) = A⋅B
	- Only true if A and B are true
	- ![[Pasted image 20230908082922.png | 100]]
	- ![[20230908_083116.jpg | 300]]
- OR Gate
	- Logic Equation Y(A) = A+B
	- Return true if either input is on
	- can be called the inclusive or
	- ![[Pasted image 20230908083431.jpg | 60]] Like an "elongated half moon"
	- ![[20230908_083746.jpg | 300]]
- 