# wro-final
this is the inctruction for WRO 2022 final, team "tesla" from kazakhstan.
the program written for lego mindstorms ev3.
team participants:
* Usoltsev Maksim
* Orazbek Nurmukhamed. 

teacher: Akhmetov Serik.
## git
repository include files with program both for qualification and final rounds. 
## construction
robot consists of 2 motors and 3 sensors. they are: 2 middle lego motors, one for steering and other for driving. one of the sensors is a gyroscope,
 it helps to straighten the robot to correct course after turning. second one is a ultrasonic sensor to see whether robot must stop or should continue to drive. also, it see obstacles we should avoid.
main robot's processing center is lego ev3 brick. it is connected to sensors and motors through lego cabels. 
we intended to include raspberry pi and raspberry cameras in the future.

**Ultrasonic Sensor**

This is a digital sensor, which measures the distance to an object.

In addition to the ultrasound receiver, which is a kind of a special microphone, this sensor also has an ultrasound transmitter. The transmitter sends an ultrasonic wave that bounces off the obstacle and reflects back to the robot. This returning wave is picked up by the receiver, which is the actual sensor. The robot calculates the distance to an obstacle by measuring the time elapsed from the moment the ultrasonic wave was emitted until the echo of this wave, which has reflected back from an object, came back.
![ultra](https://petljamediastorage.blob.core.windows.net/root/Media/Default/Kursevi/international/BlockBasedProgMakeCodeEng/brick6.jpg)

**Gyroscope**

Gyroscope is a digital sensor, which detects movement and changes in the movement of the robot. When the robot moves, this sensor will present this as the change in the rotation speed in degrees per second (deg/s). The maximum rate is 440 deg/s.

![gyro](https://petljamediastorage.blob.core.windows.net/root/Media/Default/Kursevi/international/BlockBasedProgMakeCodeEng/brick10.png)

Based on this data, the user can determine whether the robot is turning, and also to program these turns (with the accuracy of +/- 3 degrees for a 90-degree turn).

