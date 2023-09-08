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
- Truth table
	- a table with inputs and outpouts
	- The inputs must be in order or **I lose Points**
- Logic diagram
	- see picture
- IEEE std 91 
	- see picture

- buffer gate
	- logic equation Y(A) = A
	- ![[Pasted image 20230908082218.png | 100]] 
	- Potential energy at any point along cable weakens the voltage
	- buffers regenerate the signal (think Minecraft repeater)
		- this is critical

- AND gate
	- Y(A) = A⋅B
	- Only true if A and B are true