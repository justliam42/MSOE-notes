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

We doing bubbles or someting
- The name of the state name on top
- at the bottom is da outputs