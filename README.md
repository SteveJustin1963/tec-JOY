# tec-JOY

![](https://github.com/SteveJustin1963/tec-JOY/blob/master/pics/S1145.jpg)

A typical jojstick has 2 10k pots for XY. 
by read and write 0 or 1 to a port we can charge an RC circuit. 
by timing the duration it takes to charge or discharge the cap we can estimate the value of R and estimate the postion.
the duration = r*c. so r=dur/c.

we wtite to the port a 0 that discharges the cap, then we write 1 the port foirst write 0 to it then write 1 to it and then time the charge up time constant for the cap which = R*C in seconds. this gives us the xy positon, 




The circuit is https://easyeda.com/editor#id=9c0ca07733b341c99b19ee6c88a706eb|cb8c65c8ba744130a871917f4e325e17




