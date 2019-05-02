# Electrical-Hardware Documentation
Electrical hardware development consists of choosing the sensors, computing device(s), battery, and other electronics.  It involves researching how the components operate and getting them to work together.  The electrical hardware is what links the mechanics and the software of the robot.  

<img src="Diagrams/block%20diagram%20v4.PNG" width="600px"/>

**Figure 1:** Electrical Block Diagram

We selected 3 different sensors to help the robot be aware of its surroundings in the arena: a visual camera, a 2D LIDAR, and rotary encoders. The camera used is the Raspberry Pi Camera Module.  The raw images are processed on entirely on a Raspberry Pi to find the debris objects on the field.  The LIDAR is a relatively low-cost 2D LIDAR system. The YDLIDAR uses a spinning laser rangefinder to return a 2D point cloud at about 8 Hz.  The rotary encoders monitor the rotation of each drive motor.  The LIDAR and encoders are used for localizing the robot in the field.  We originally were going to utilize an inertial measurement unit (IMU) to help receive information on orientation and acceleration but we did not use it in the final design.

The robot is controlled using two coprocessing Raspberry Pi 3B+ connected via an ethernet cable.  A Teensy microcontroller polls the encoders and sends the velocity information to the main Pi. Once the Pi’s determine the desired path, an Arduino microcontroller instructs the motor controllers of the corresponding commands.  Two different batteries are used to prevent the motors from causing a brownout situation for the Raspberry Pi’s.  In Figure 1, the latest version of the electrical block diagram shows all of the components on the robot.

To facilitate rapid prototyping, protoboards were used to keep most of the main components centralized to one area and clean up some of the wiring. Two primary peripherals were used to supplement the Raspberry Pi’s as I/O: an Arduino Nano on the main protoboard and a Teensy on its own protoboard.  Figure 5 shows a wiring diagram of how the protoboards were utilized.

The Arduino Nano served to wire most of the components together. This includes the servos, buttons, LCD, selector switch, and main motor controller. The decision behind this would be to relieve the processing load from the already over-taxed Raspberry Pi. 

The Teensy was required later on in the design process due to the Arduino’s lack of available pins and hardware interrupts to properly implement the encoders. It counts the number of ticks the encoders have counted and sends the values via serial bus to the Raspberry Pi. The Pi can then compute this easily into motor distance traveled.

<img src="Diagrams/Circuit%20Diagram.png" width="600px"/>

**Figure 2:** Wiring Diagram