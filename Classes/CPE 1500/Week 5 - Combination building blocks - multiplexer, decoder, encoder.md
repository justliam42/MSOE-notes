-- 9/22/2023 -- 

##### Multiplexor data selector
Traditional (2 input selector):
	Y=D1 if S=1
	D0 id S=0
	 Basically Y(S,D1,D0) = !SD<sub>0</sub> + SD<sub>1</sub> 
  
4-bit input selector:
	Build bigger multiplexer from smaller ones:
	1. build however many 2-input selectors needed
	2. Put them through more 2-input selectors