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


-- 9/18/2023 --
gate and wire reduction ratios:
	Bigger number always goes on top
	![[20230918_081738.jpg | 300]]

 Karnaugh map: (how to avoid algebra...) (k-map)
	 Y(XYZ) are coordinates ? 
	 fold the third dimension
	 take x and put it on the vertical
	 put y and z on the horizontal
	 Karnaugh's adjacency theorem
		 0 1 3 2
		 as you move along the axis, every jump is a compliments theorem
		 minterms in the lower right corner
		 then plot the energy points
		 power of 2 sized minterm squares that have energy
		 squares and rectangles wrap the edge
			do it systematically even though brain says no...
		 now identify energy points in only one rectangles (essential points)
		 everything in a rectangle is in a gate
		 ask which variables stay the same on a given axis
		 ![[20230918_083017.jpg | 300]]
		 always begin with the smallest minterm that's energized
		 doesnt need smaller groups when in bigger ones
		 every rectangle is an and gate
		Standard way to get the same equation
			start with lowest essential ting in biggest gate or something
			2 to the size of the rectangle is how many complements term

G<sub>c</sub> / G<sub>m</sub> but then move G<sub>m</sub> to other side so say G<sub>c</sub> = 2.25 * G<sub>m</sub> 