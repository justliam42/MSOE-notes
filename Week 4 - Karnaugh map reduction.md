-- 9/18/2023 --
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
		 doesn't need smaller groups when in bigger ones
		 every rectangle is an and gate
		Standard way to get the same equation
			start with lowest essential ting in biggest gate or something
			2 to the size of the rectangle is how many complements term

G<sub>c</sub> / G<sub>m</sub> but then move G<sub>m</sub> to other side so say G<sub>c</sub> = 2.25 * G<sub>m</sub> 


-- 9/20-2023 --

review steps of j