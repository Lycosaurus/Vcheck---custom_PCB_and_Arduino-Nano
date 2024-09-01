Arduino based Dynamic Propeller Balancer

![image](https://github.com/user-attachments/assets/1f9cf407-a442-4f9d-9c8b-3a701874bc64)

This is a full blown features implementation of a propeller balancer on an Arduino Uno. The software was originally developed by Peter Ashwood-Smith  -  https://github.com/peterashwoodsmith

  September 1, 2024  Please Note: This project is NOT COMPLETE YET. DO NOT USE. 

  It is a work in progress, and documents are being uploaded and corrected. A PCB respin is planned to cleanup footprint and other errors. Please stay tuned.

Features

- Operating voltage from 4V to 15V. 4xAA, 1x9V, 2x9V, 5V USB, 14V automotive/external
- There is a boost supply for voltages lower than 10.5V to provide adequate voltage to the LED strobe sensor.
- Dynamic Propeller Balancing. The unit will determine the angle where the heavy weight is detected, and provide an inch per second value to quantify the vibration. The user will use this information to corrent this imbalance by attaching a correction weight 180 degrees away from this number.
- The main Signal Process Unit (SPU) PCB is housed in a thermoplastic enclosure that houses the connectors/switches, batteries (4AA, 1x9V, or 2x9V), as well as a window for the 16x2 LCD display.
- The processor is a Arduino Nano, which can be upgraded to an Arduion Nano Every, as the SPU is socketed to accept either of these two devices.
- Calibration amplitude and angle calibration can be performed by the user
- This is a DIY project, where you build and maintain/calibrate your unit. You will have access to the full schematics, component BOM and software.



![image](https://github.com/user-attachments/assets/15c27c24-ae22-4929-9cd0-cd7ce358f57c)

Acceleration Sensing Unit (ASU)
  
- An Acceleration Sensing Unit (ASU) is also provided as a PCB for ease of assembly/housing into a small aluminum flahslight case.
- The ASU contains an ADXL335 analog acceleration sensor, where all 3 axes are sent to the SPU. The SPU is able to accept to ASU units, and based on solder jumpers (0 Ohm resistors) can be configured to accept any 2 of the 6 axes presented. The two axes are processed individually by the Arduino in a ping pong fashion (e.g. 1 second axis Y, 1 second asis X).
- Full testing is not complete, however preliminary results lead us to believe that 4xAA batteries will last up to 19 hours in continuous operation (including using the boost converter).




![Vcheck Mosaic](https://github.com/user-attachments/assets/816c710b-a543-4b29-b071-321f13cf6c08)

LED trigger sensor

The LED sensor determines the reference 0 degree angle of the motor/propeller. The unit is pointed to the back of the propeller using a retroflective tape as a target. This sensor produces a digital active low signal when the 0 degree mark is encountered. Presently this off-the-shelf sensor is fairly expensive at a cost of $200US (with 10m cable). An alternative and lower cost sensor design is being tested. More to come.






