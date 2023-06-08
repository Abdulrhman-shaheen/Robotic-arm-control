# The workspace is used to control 6 Servo-robotic arm using Arduino and ROS system.


Using talker.py node in beginner_tutorials package the python script translates the inputs from the keyboard and send orders to the servos according to it. Where each servo has its own topic to be sent on.

- Servo1 is controled by "q" and "a" q to increase the angle and "a" to decrease.
- Servo2 is controled by "w" and "s" w to increase the angle and "s" to decrease.
- Servo3 is controled by "e" and "d" e to increase the angle and "d" to decrease.
- Servo4 is controled by "r" and "f" r to increase the angle and "f" to decrease.
- Servo5 is controled by "t" and "g" t to increase the angle and "g" to decrease.
- Servo6 is controled by "y" and "h" y to increase the angle and "h" to decrease.
<br>
Listener.py is another node in the same package that recieve the data independently just to view the servo you are controlling right now and its angle.

rosserial is another package that recieves the published data from talker.py then do the arduino part where it matches each Servo with the data sent on its topic.s

Dont forget to clone the 'Rosserial' package by:
<br>`cd cd catkin_ws/src/rosserial/` <br> 
`git clone https://github.com/ros-drivers/rosserial.git`

 
# To run the controller
 1. *Roscore* (in a separte terminal)
 2.  Upload the **code Servos_control** in the folder Arduino on the arduino. (Attatch the servos to the mentioned pins)
 3. *rosrun rosserial_python serial_node.py /dev/ttyUSB0* (USB0 may change according to the port) in a separate terminal
 4. *rosrun beginner_tutorials talker.py * This is the publlisher that neeed some preprerequisites mentioned in the **prerequisites** file.
 5. *rosrun beginner_tutorials listener.py* This is oprtional best better for monitoring the changes.  

<sub>
Sorry for in the inconvenience in the name of the workspace and the packages, might fix them later but not now.
</sub>
