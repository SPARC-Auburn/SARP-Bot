# Mechanical Documentation

<img src="../Images/Mechanical%20Development/final-bot.jpg"  width="400px"/>

**Figure 1:** Final robot design

Mechanical development involves designing and manufacturing the mechanical system of the robot.  This includes everything from the mobility system and framework to the mechanism that collects the cubes.  We have many tools to our disposal from physical tools and 3D printers in our lab, to the free student edition of the professional design tool, SolidWorks.  We utilized Solidworks 2018-2019 for this project.  We printed all of our parts on a Creality CR-10S with ESun PLA+.

<img src="../Images/Mechanical%20Development/mechanical-progression.PNG"  width="400px"/>

**Figure 2:** Mechanical Progression
We constructed a 4 wheel differential drive robot.  Each side has a motor powering the wheels with a chain and sprocket system.  There is an opening with a movable flap in the center section on the bottom for the debris to be collected.  The robot fits within the 9” x 9” x 11” size requirement.  It was constructed with an 8020 aluminum frame and custom PLA+ 3D printed brackets.

<img src="../Images/CAD%20Images/finalFramework.PNG"  width="400px"/>

**Figure 3:**  8020 Frame

We initially intended on using a spinning rod to actuate vertically to collect and dispose of the debris.  We called this mechanism the gate.  It utilized three stepper motors.  During the testing of the robot, the stepper motors were run using a basic program to make them turn.  During this test it was discovered that the rubber tubing connecting the stepper motors to the threaded poles was not tight enough, allowing the motors to slip through the tubing.  This, alongside the front gate making the robot front heavy lead to the decision to remove the stepper motors and front gate completely. The front gate can be seen in Figure 2 with the pink 3D printed material and the two servo motors on top.   In its place, a servo motor was mounted onto the side of the robot and attached to a paddle that will lift it up to allow objects underneath the robot as shown in Figure 1.  

The servo motor not only solves the connection problem of the stepper motors but is considerably easier to program.  Removing the added weight from the stepper motors at the top of the gate also lowered the center of gravity.  This allows the robot to make more sudden stops and maneuver easier around the obstacles on the field.  The simpler mechanical approach helped free up more space for additional electronics.

Another issue that was encountered, was the LIDAR needed to be lowered in order to account for the field being constructed in lumber sizes instead of the state height.  At the original position, testing proved that the LIDAR would measure some distances beyond the dimensions of the field.  A few different parts of the frame and electronics had to be adjusted to account for this.  Once this change was made, the LIDAR could not detect anything above the arena walls.