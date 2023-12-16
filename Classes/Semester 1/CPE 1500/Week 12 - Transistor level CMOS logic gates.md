[Lilienfeld](https://en.wikipedia.org/wiki/Julius_Edgar_Lilienfeld) proposes field effect transistor in the 1920s

Bell laborotories creates the first transistor in 1947 (point contact)
Called the most important invention of the 20th century
Transistor can amplifies and switches signals


point contact transistor
bipolar junction transistor
field effect

takes about 30 years to fabricate the field effect transistor

silicon is a semi-conductive element so it conducts with some modification.

sand is purified and boild and strain is pulled up becoming a cylinder
then a millimeter tall wafer of silicon is cut 

The air purification is essential

the rest of the process takes about 60 steps called:
**photo-lithography**

taking 2 regions of the silicon and chemically change them
one region becomes electro negative
the other area is n-type material or something

then glass is pored on top (silicon dioxide originally) which is insulative

on top of the insulated region we drop metal (originally) (now polysilicon)

so a conductor seperated from another conductor becomes a capacitor (semi)

then glass is once again pored on top of all it.

then a hole is drilled with a semiconductor pored in
![[20231127_082731.jpg | 300]]

basically if the metal is charged, the silicon becomes ionized (all them electrons go to the top)



it takes years for us to get good at it.

We start with Small Scale Integration (SSI) - 10s of transistors on a chip

then Medium Scale Integration (MSI) - 100s-1000s of transistors on a chip

then Large Scale Integration (LSI) - 1000s-10000s

Very Large Scale Integration (VLSI) (1980s) - 1000000s+

This is Moores law... number of transistors on a chip doubles every 2 years
Moore founded National Semiconductor and Intel

Metal - Oxide - Silicon - Feld effect transistor = MOSFET

when on = 1 then it is NMOS

when on = 0 then it is PMOS (formed from column 3 so the n region is positive)

these are complement to their things so
not gate showed was a complementary metal oxide semiconductor design (CMOS)

--11.29.2023--
terminals are called source, gate, and drain 
the distance between n-regions historically called the channel length

today the channel is the size of the things we fabricate
channels are also no longer straight (finFETs)
![[20231129_082354.jpg | 500]]

TTL is the design scheme before CMOS

AC or HC chips instead of LS is CMOS instead of TTL

CMOS design:
	N-type transistors always connect the output to ground
	P-type transistors always connect the output to power
	Everything sits between the power rails
	The Inputs connect to the gate terminals
	CMOS naturally creates the inverted function

NAND gate:
	transistors in series (series forms and behavioro)


3 input nor:
	inputs connected to GND in parallel nmos
	so the pmos transistors go in series

the or function is just nor but it feeds into an inverter thing

--12.1.2023--
#### Power consumption: 
- The amount of battery energy used per unit time
- P<sub>dynamic</sub>: energy used to charge signal wire from logic 0 to logic 1
	- (1/2) CV<sub>dd</sub><sup>2</sup>f
	- Capacitance C is property of the metal wire, and measured in the unit Farad
- P<sub>static</sub>: energy used when signal is constant logic 0 or logic 1 
	- this equals I<sub>dd</sub> 
	- In CMOSS the P<sub>static</sub> is always 0
