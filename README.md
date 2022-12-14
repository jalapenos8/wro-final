# wro-final
this is the inctruction for WRO 2022 final, team "tesla" from kazakhstan.
the program written for lego mindstorms ev3.
team name: tesla

country: kazakhstan

team participants:
* Ussoltsev Maxim
* Orazbek Nurmukhamed. 

coach: Akhmetov Serik.
## git
repository include files with program both for qualification and final rounds.
### content
* photos/team - photos of team
* photos/robot - photos of robot
* video.txt - link to youtube video
* some files are just codes
## construction
robot consists of 2 motors and 4 sensors, including 1 camera. they are: 2 middle lego motors, one for steering and other for driving. one of the sensors is a gyroscope,
 it helps to straighten the robot to correct course after turning. second one is a ultrasonic sensor to see whether robot must stop or should continue to drive. also, it see obstacles we should avoid.
main robot's processing center is lego ev3 brick. it is connected to sensors and motors through lego cabels. 
we intended to include raspberry pi and raspberry cameras in the future.

**Ultrasonic Sensor**

This is a digital sensor, which measures the distance to an object.

In addition to the ultrasound receiver, which is a kind of a special microphone, this sensor also has an ultrasound transmitter. The transmitter sends an ultrasonic wave that bounces off the obstacle and reflects back to the robot. This returning wave is picked up by the receiver, which is the actual sensor. The robot calculates the distance to an obstacle by measuring the time elapsed from the moment the ultrasonic wave was emitted until the echo of this wave, which has reflected back from an object, came back.
![ultra](https://petljamediastorage.blob.core.windows.net/root/Media/Default/Kursevi/international/BlockBasedProgMakeCodeEng/brick6.jpg)

The ultrasonic sensor enables three different modes. It enables making distance measurement up to 
250 cm (100 Inches) with an accuracy of 1 cm (0.393 Inches) in either centimeters or inches. It also 
enables a listen mode where the ultrasonic sensor is measuring whether other ultrasonic sensor are 
active within its surroundings. 
This sensor is implemented as a digital sensor, meaning the sensor includes a small 8-bit microcontroller which communicates with the EV3 P-brick using UART communication on pin 5 and 6. 
The microcontroller handles all sensor measurements and data analysis which is then communicated 
back to the EV3 P-brick. The ultrasonic sensor sends back new distance measurement whenever a new 
distance is detected. If the distance is 250 cm (100 Inches) the duration between new sensor values will 
approximately be every 15 mS. With a smaller distance the ultrasonic sensor will be able to return 
measurement faster. 
The ultrasonic sensor measure the distance to an object by sending out an ultrasonic sound signal, 12 
sound burst at 40 KHz. The receive transducer is most sensitive at 40 KHz and has a beam angle of 
approximately 90 degree.

**Gyroscope**

Gyroscope is a digital sensor, which detects movement and changes in the movement of the robot. When the robot moves, this sensor will present this as the change in the rotation speed in degrees per second (deg/s). The maximum rate is 440 deg/s.

![gyro](https://petljamediastorage.blob.core.windows.net/root/Media/Default/Kursevi/international/BlockBasedProgMakeCodeEng/brick10.png)

The microcontroller handles all sensor measurements and data analysis which is then communicated 
back to the EV3 P-brick. The gyro sensor is able to return new sensor values 1000 times a second if the 
sensor reading changes fast enough. The sensor is programmed to automatically return a new sensor 
value whenever the value changes or if the EV3 P-brick requests a latest sensor value.

Based on this data, the user can determine whether the robot is turning, and also to program these turns (with the accuracy of +/- 3 degrees for a 90-degree turn).
We used gyroscope to hold correct direction of movement and make proper turnings. Also, our PID regulator is based on data from the gyroscope. Although having great applications, the gyrocope needs time between 2-5 seconds at the beginning to get rid of drift; it means random unwanted errors.

** Color sensor **

![gyro](https://m.media-amazon.com/images/I/61ljvcb1SrL.jpg)

Color sensor is essential for our robot in determining direction of the movement. Because it defines reflected light intensity and, thus, color of the line before turnings. It can calculate RGB components of colors. After, native block in lego determines exact color of lines. it helps to recognize where turn is. if first seen line is orange, then robot turns right and vice verse.
The microcontroller handles all sensor measurements and data analysis which is then communicated 
back to the EV3 P-brick. The color sensor is able to return new sensor values 1000 times a second if 
read surface changes fast enough. The sensor is programmed to automatically return a new sensor 
value whenever the value changes or if the EV3 P-brick requests a latest sensor value. 
When the color sensor are connected to the EV3 P-brick it automatically starts by identifying itself to the 
EV3 P-brick as a color sensor and it communicates the modes and value ranges it supports before it 
switches to the default mode which is light sensor mode. 

** Camera Pixy2 **

** Medium motor **
The Medium Motor block controls the Medium Motor. You can turn the motor on or off, control its power level, or turn the motor on for a specified amount of time or rotations.
Select the motor (A, B, C, or D) that you want the Medium Motor block to control by using the Port Selector on the top of the block.
???
![gyro](https://cdn.kiobi.com/images/brickwatch/sets/45503.png)

Use the Mode Selector to select how you want to control the motor. After selecting the mode, you can choose values for the inputs. The inputs available will change depending on the mode. The modes and inputs are described below.
