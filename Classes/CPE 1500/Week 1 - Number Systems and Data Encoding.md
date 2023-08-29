-- 8/28/23 --
computer engineering is the moving of energy around to compute

Voltage - named after Volta

- Voltage
    - electrical potential energy
    - unit is volts (V)
    - if we close a switch the voltage increases as it is potential energy
- current
    - dynamic kinetic electrical energy
    - unit: amperes (A)
- switching polarity of voltage changes direction of current

see picture*

- these plots are real valued functions
- infinite number of measurable values
- analog electrical signal
- one way to do numbers is by using voltages representing different numbers (analog)
    - problem with this approach is precision and speed
    - this is analog
    - have to generate between 0-9 volts cleanly without noise and identify the volts (in base ten)
        - or do this with amps which slows down behavior
- so we use 0 or 1 (digital abstraction)
    - binary time woot woot
    - battery with a switch instead of generator with infinite possibilities
    - asking if it is on or off is a very fast ting
    - this is **digital signal**
    - negative volts is off (maybe)
    - off-on, low V-high V, 0-1, false-true
    - This is the **digital abstraction**

we built analog computers for years

binary computers became standard a 1960s

(day one)
![[cpe graphs day 1.jpg]]

-- 8/29/23 --
some ways of stuff makes a sine graph

when electrical potential energy changes, the flow changes directions (vibrating)\
170 volts out of the wall
in real-valued (analog) signals, it boosts or interferes with the wave

ionized chemicals kept separate in a battery creates a positive and negative side. As long as the sides aren't connected, there is no kinetic energy. The when a switch closes the voltage becomes constant. Then we get the square wave. On-off behavior. (discrete behavior)
	- this is countable
	- countable = digital (fingers)
	- digital abstraction
	- 0V - Battery voltage (Vbat)

Battery voltage has historically been 5 volts, could also be 3.3v
 - miniaturization has made battery voltage requirements less (doesn't have to carry the energy as far) 
	  - increases battery lifetime
	  - 
   - instead of recording the voltage, it was decided that it will be 0 or 1

#### Binary things
- Our counting system (base 10)
	- 1000s 100s 10s 1s ...
	- Positional number system
	- any number is a coefficient in that column
	- left is the most significant column

romans be like
I II III IV V


in binary the precision or range is much less for the same number of columns but the advantage of speed and noise tolerance far outweighs that disadvantage

A positional system uses a discrete base set of symbols. 10 symbols is base 10, 2 symbols is base 2
much of binary stuff was made by george bool (boolean)