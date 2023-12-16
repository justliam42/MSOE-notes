12.4.2023
CMOS design rules (again)
- Minterms energize NMOs devices to pull Y down to ground
- Thus, CMOS naturally creates the inverse of a function
- Build product terms as series NMOS transistors
- sum of products built as parallel product terms
- do opposite series-parallel rules with PMOS transistors

Electrict power is the use od electric energy through tume.
- P = E/t = VQ/t = VI
	- E/t is Joules per second or watts
	- Voltage * Culons idk
	- Voltage * I
- Dynamic and static power 
	- no dynamic power going backwards
	- no static pull in cmos
	- Dynamic power is $\frac{1}{2}CV^2_{DD}f$
	- even off transistors have diffusion (tiny amount of current)
		- reverse saturation current
		- we equate this satic current as 0
	- $P=I_{DD}V_{DD}$
	- in the absence of I<sub>dd</sub> we dont need to calculate static power



TTL (7400, 74Ls00)
| --- | VIL | VIH | Va | VOH | NMH |
| TTL | 0.8 | 2.4 | 0.4 | 2.4 (3.6?) | 0.4 |
| CMOS | 1.35| 3.15 | 0.33 | 3.84 | 1.02 | 0.69 |

standard interfacing technique for hc and ttl is to place a 2.2k ohm resistor.
	the output will be nd which pulls the thing up and tehn the thing
	so to interface ttl to cmos jus add aresistor of a thousand or more ohms
	called a pullup resistor

