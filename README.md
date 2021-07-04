# tec-JOY

![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/1.png) ![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/2.png)

A typical jojstick has 2 of 10k pots for XY. 
by read and write 0 or 1 to a port we can charge an RC circuit. 
by timing the duration it takes to charge or discharge a fixed value cap we can estimate the value of R which estimate the postion.
the duration = r*c. so r=dur/c.

we write 0 to the LHS of cct to discharge the cap, then wait 5rc times.
then we write 1 again and as the current flows thru R of the pot value it charges the cap.
we read the RHS of cct with another port and repeat and count until we see a 1.
the total reads count approx = R*C in seconds. this gives us the xy positon. 

pressing down on the knob is a switch, it calls /INT and latches 0.

The circuit is https://easyeda.com/editor#id=9c0ca07733b341c99b19ee6c88a706eb|cb8c65c8ba744130a871917f4e325e17




