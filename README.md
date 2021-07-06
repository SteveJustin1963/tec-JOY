# tec-JOY

![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/1.png) ![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/2.png)

Copy Left. Draft, use at risk

A typical joystick has 2 of 10k pots for XY. I see so many chucked out in old consoles etc and cheap to buy. By reading and writing 0 or 1 to a port we can charge / discharge the C of an RC circuit. by timing the duration it takes to charge or discharge a fixed value C we can estimate the value of R which estimates the position. 

The duration = R*C, per second. C is fixed.

We will measure with charging only. We write 0 to the LHS of cct to discharge C and wait 5RC times so it reaches zero. Then we write pulsed 1’s again to the port and as the current flows thru R of the pot value it charges the C. We pulse read the RHS of cct with another port and repeat count until we see a 1. When we read the port, R of 470k stops discharging C. The total reads the are the count = approx = RC * f counts (per seconds). Using f as a scaling factor. This gives us the xy position.
Also pressing down on the knob switch calls /INT and latches 0. The cap holds the line at 0 long enough so the latch can be read.

https://easyeda.com/editor#id=|f38afcc535a449c0b98ccadf3163fde4|321ec5e4744a4cc79bfbc13cb8e15be6|dee47719661d4ba880eba90f8b386a9a

The variable time rc is also proportional to how far the stick is pushed and can also serve as velocity of moving the input or position in a matrix. Most cases only need to know if it was a push not how far it went. So next cct will simplify the pot into a switch using comparators.

https://easyeda.com/editor#id=cca9828b1c6e4638a1293eedd4f90bbe|d5d747e4fdc64215b9a840fcd2c6e1cf
