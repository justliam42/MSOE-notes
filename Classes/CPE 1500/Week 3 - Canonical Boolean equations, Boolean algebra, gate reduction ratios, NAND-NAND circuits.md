-- 9/13/2023 --
Standard form canonical : F(abc) = !abc + a!bc ...
Short form canonical: F(abc) = Sigma<sub>m</sub>(3,6,...) 

-- 9/15/2023 -- 

process (with four outputs)
1. make the black box diagram w/ multiple outputs
	- the outputs are labled y<sub>0</sub>, y<sub>1</sub>, etc going up from the bottom...
2. function be like Y(ABC) = ABC+4
	- we finally doing adding?? owo
3. Make truth table
4. make canonical form (maybe short)
	- with multiple oiutputs there are multiple forms
		- Y<sub>3</sub>(ABC) = Sum(4,5,6,7), Y<sub>2</sub>(ABC) = Sum(0,1,2,3), ...
	- n-bit input producing an m-bit output
	- we then made the standard form
5. find all required minterms
6. cook (make diagram)
	1. make diagram match entity
	2. name association (don't forget to name wires)![[20230915_082607.jpg]]

- Canonical equations
	- not optimized
	- not algebraically reduced
	- biggest
	- costliest
	- most power consuming
	- slowest
 
![[boolean-algebra-quick-reference.pdf]]

assume Y<sub>3</sub> = A!B!C + A!BC + AB!C + ABC
	create tree diagram
		each gets compared to all of them
		always looking for a single term das complements term
		if term doesnt participate in reduction, then they get ord with the reduced tings![[20230915_084721.jpg]]

gate and wire reduction ratios:
	Bigger number always goes on top
	![[20230918_081738.jpg | 300]]
 