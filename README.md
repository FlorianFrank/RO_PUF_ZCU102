# Ring Oscillator PUF Optimized for Ultrascale+-Architectures

This repository is a fork of the implementation provided by Gabalo [https://github.com/Gabalo/RO_PUF](https://github.com/Gabalo/RO_PUF).

**It is currently under implementation do not clone!**

Operation: 
 - Executes a ring-oscillator PUF on a ZCU102+ board. 
 - Contains error correction using the BCH error correcting code provided by Russ Dill (https://github.com/russdill/bch_verilog)[https://github.com/russdill/bch_verilog].


The code was originaly implemented for Xilinx Artix-7 FPGAs but is currently modified to support Xlinx Ultrascale+ architectures. 

Configuration: 

The design uses the USB UART interface of the ZCU102 therefore can be accedded for example using putty over /tty/USBx. 

The output can be configured by the switches of SW8. 

| SW[0]    | SW[1]   | Result |
| -------- | ------- | ------ |
| 0        |    0    | Return PUF result directly |
| 1 | 0     | Return error corrected result |
| 0    | 1    | Corrected and hashed result |