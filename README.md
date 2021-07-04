# tec-JOY

![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/1.png) ![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/2.png)

draft do not use

A typical joystick has 2 of 10k pots for XY. I see so many chucked out in old consoles etc and cheap to buy. By reading and writing 0 or 1 to a port we can charge / discharge the C of an RC circuit. by timing the duration it takes to charge or discharge a fixed value C we can estimate the value of R which estimates the position. 

The duration = R*C, with C a constant, dur=C.

We will measure with charging only. We write 0 to the LHS of cct to discharge C and wait 5RC times so it reaches zero. Then we write pulsed 1’s again to the port and as the current flows thru R of the pot value it charges the C. We pulse read the RHS of cct with another port and repeat count until we see a 1. When we read the port, R of 470k stops discharging C. The total reads the are the count = approx = RC * f counts (per seconds). Using f as a scaling factor. This gives us the xy position.
Also pressing down on the knob switch calls /INT and latches 0. The cap holds the line at 0 long enough so the latch can be read.
The circuit is https://easyeda.com/editor#id=9c0ca07733b341c99b19ee6c88a706eb|cb8c65c8ba744130a871917f4e325e17




