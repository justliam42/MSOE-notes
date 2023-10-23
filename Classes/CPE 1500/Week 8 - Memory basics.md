##### We have been working with combinational circuits.
- Current inputs generate an output. They have no memory of past inputs
- *in discrete math there is combinatorics. or the study of countable things*
- multiplexors
- adders
- g4
- prime
- robot
- etc

#### Sequential circuits:
- consider the current inputs and the history of past events. Thus, this type of circuit has memory

1-bit memory is called a flip-flop 
- flip it on logic 1 and it remembers until you change it
- flop it off to logic-0 and it remembers it
first built them with vacuum tubes then mercury tubes
Then we use transisters haha

n-bit memory is just side-by-side flip-flops
an n-bit wide memory is a "register"

period of oscillation is tao
with a single self-attached not gate, the oscilation is 2 delta

even number of not gates where output attaches to input, it holds memory

we can represent this with nor gates.
- becomes and sr latch
**output is Q
- stands for quiescent (stable, not changing)
S is set R is reset

reset = clear in memory

--10/18/2023--

##### D flip flop (DFF)
-  Q is still output
- D is data input (D flip flop)
- active low load control signal 
- sample clock
- ![[Pasted image 20231018081438.png | 200]]
- when both inputs 1, it is n/a
##### Register
- one n-bit number
- active low load and reset signals
- n amount of data and outputs
- sample time clock
- ![[Pasted image 20231018081609.png | 200]]


#### Controlled 1-bit
![[Pasted image 20231018084334.png | 350]]
- this is dumb tho because it no longer stores memory so ->
![[Pasted image 20231018084651.png | 350]]
- so the enable bit is just switching between the feedback loop and the data pin
- In this the controlled thing from above is used because with the not it makes the NORS jus act like nots because the inputs will be the same or someting
- this is a **d latch

![[Pasted image 20231020082356.png]]
basically when the clock goes high, it outputs the last thing that was on the wire when the clock was low until it goes from low to high again
- now it is a d flip flop
pretty sure the load is necessary(helpful)


--10.23.2023--

in the 74194 4-bit register:
- provid