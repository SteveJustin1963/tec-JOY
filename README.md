# tec-JOY

![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/1.png) ![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/2.png)

draft do not use

A typical jojstick has 2 of 10k pots for XY. 
by read and write 0 or 1 to a port we can charge / discharge the C of an RC circuit. 
by timing the duration it takes to charge or discharge a fixed value C we can estimate the value of R which estimates the postion.
the duration = R*C, with C a constant, dur=C. 

we will measure with charging only. 
we write 0 to the LHS of cct to discharge the cap, and wait 5rc times so its reaches zero.
then we write pulse 1 again and as the current flows thru R of the pot value it charges the cap.
we read pulse the RHS of cct with another port and repeat count until we see a 1. the read R stops discharging.
the total reads count = approx R*C * f* seconds. f is some factor. this gives us the xy positon. 

also pressing down on the knob switch calls /INT and latches 0. the cap hold the line to 0 so the latch can be read.

The circuit is https://easyeda.com/editor#id=9c0ca07733b341c99b19ee6c88a706eb|cb8c65c8ba744130a871917f4e325e17




