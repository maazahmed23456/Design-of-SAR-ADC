

# SAR Analog to Digital Converter
This project is my final year major project and is still in development. This projects aims to perfrom layout of a SAR ADC and analyse and improve upon the performance prameters. Currently the prelayout design and simulation of Sample and Hold Circuit and Comparator are completed 

*Note: Circuit requires further designing . Design yet to be modified.*


## A Glance at the SAR ADC IP

A Successive Approximation Register (SAR) ADC is an efficient ADC architecture known for its balance of speed, power, and resolution, widely used in data acquisition, medical devices, audio, and low-power IoT systems. It operates by performing a binary search to approximate the input voltage level in successive steps, starting from the most significant bit.

A SAR ADC includes a sample-and-hold circuit, DAC, comparator, and SAR logic. Each bit is determined sequentially, creating a digital output that closely matches the analog input. Key design goals are low power, high SNR, low THD, and maintaining linearity. Challenges include minimizing power and noise while improving resolution and tolerance to process and temperature variations.

**Upload your paper on Github and give a link to it**

## Block Diagram of the SAR ADC IP

 <p align="center">
  <img width="800" height="500" src="/Images/block diagram.png">
</p>




## Circuit Diagram of the Sample and Hold IP

 <p align="center">
  <img width="800" height="500" src="/Images/Screenshot.png">
</p>

## Circuit Diagram of the Comparator IP

 <p align="center">
  <img width="800" height="500" src="/Images/2.png">
</p>
 <p align="center">
   <img width="800" height="500" src="/Images/1.png">
</p>


## Pre-Layout Simulation

###  Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_temp.png">
</p>


###  Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_supply.png">
</p>

###  Temperature Coefficient of Vbgp v/s Temperature [ -40C - 140C] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_tc.png">
</p>

###  Voltage Coefficient of Vbgp v/s VDD [ 2V - 4V] @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_vc.png">
</p>

###  Start-Up Time of Vbgp @ RL = 100M ohms plot


 <p align="center">
  <img width="800" height="500" src="/Images/N/PRE/pre_startup.png">
</p>


###  On-Off-Current of Vbgp wrt Enable @ RL = 100M ohms plot

 <p align="center">
  <img width="1000" height="500" src="/Images/N/PRE/pre_c.png">
</p>

**Note: Current without Inverter for Enable Logic**



***************



## Future Work

1. Improved matching techniques such as Common Centroid / Interdigitisation need to be implemented while laying out the current mirror.
2. PNR for the designed circuit is yet to performed using the Open Source Tool provided by the OpenROAD project.
3. Corner Analysis Testing of the bandgap reference circuit is yet to be performed.
4. The load driving capability needs to be improved by addition of a buffer block such as an OTA or a common drain amplifier.
5. To adjust the reference voltage resistors must be trimmed using fuses, hence, resistor trimming must be employed in the circuit.
6. The design must be improved to provide a higher PSRR.
7. In the future an OTA based bandgap reference circuit will be developed with improved performance characteristics. Also, a second order bandgap reference will be studied and developed, to improve the temperature coefficient.
8. To solve the problem of unwanted parasitic BJTs being extracted due to the modification made in the Technology File.

## Contributors 

- **Sheryl Serrao** 
- **Kunal Ghosh** 
- **Philipp Gühring** 



## Acknowledgments


- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd.
- Philipp Gühring, Software Architect, LibreSilicon Assocation
- Saroj Rout, Associate Professor & Chief Mentor of VLSI Center of Excellence SIT, Bhubaneswar, India
- Santunu Sarangi, Asst. Professor, SIT, Bhubaneswar, India
- Tim Edwards, Senior Vice President of Analog and Design at efabless corporation
- Ankur Sah, M.Tech Embedded Systems, NIT Jamshedpur

## Contact Information

- Sheryl Serrao, Undergraduate Student, Mumbai University sherylcorina@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at
- Dr. Gaurav Trivedi Co-Principal Investigator, EICT Academy, IIT Guwahati trivedi@iitg.ac.in
