
The files permit to interract with a LSM303D pololu acceloremeter / magnetometer CI ;
For the moment, it is needed to use i2cdetect / i2cset (/usr/sbin/i2cdetect => i2c-tools package)
The script in bash :

* initializes the adress of the component (0x1d)
* initializes the component registers thanks to i2cset
* realise a while loop and inside : 
  - read the values 
  - convert the values thanks to the C code compiled (initLSM303D) to obtain :
    * polar coordinates of the force vector 
    * deduce to the vector
      --> PITCH
      --> ROLL
      --> HEADING

----------------------------------------------------------------------------------------------
