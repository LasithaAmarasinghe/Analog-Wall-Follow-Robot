# Analog Wall Following Robot
This is a group project done under the module EN2091 - Laboratory Practice and Projects, Semester 3, Department of Electronic and Telecommunication Engineering, University of Moratuwa. 

## Introduction

*  Wall following robot is a robot that follows a wall and travels keeping a constant distance from the wall. 
*  Wall following is a common task in many robotics competitions.
*  But the interesting point is our project was to build a robot that travels on the centerline between two walls using only analog electronics.
*  That means we couldn’t use microcontrollers according to the [guidelines](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Project_Guidelines.pdf).

![IMG-20231206-WA0097](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/241e426e-1c0c-4cf3-a58a-3e9705a20f41)

## Working Concept

*  Two sharp IR sensors measure the distance from the robot to the side walls.
*  The difference between the sharp IR sensor values is taken as the error signal and fed into a PID control circuit.
*  The PID output signal is fed to the adder and subtractor circuits.
*  The PID output and a comparator circuit generate two PWM signals with varying duty cycles.
*  Then using the motor driver, PWM signals are fed to the left and right wheels.
*  The robot tracks the walls and travels on the centerline between walls.
*  Additionally we added another sharp IR sensor to the front of the robot to control the speed of the robot.
*  The measured distance is compared with a predefined distance and the difference is taken as the error signal.
*  The error signal is fed to a PID control circuit.
*  A PWM signal is generated using the PID output and a comparator circuit.
*  This PWM signal acts as the Base speed of the robot.
*  Consequently the additional sharp IR sensor will vary the car's speed accordingly.

![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/49f70bd2-af03-46a3-9955-452a3b607f5d)

## Sub Circuits and Tasks

* [Instrumentation Amplifier](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Instrumentation%20Amplifier.jpg)- Reduce noise in Sharp IR sensor outputs and amplify signals
* [PID circuit](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/PID.jpg)- Control the error signal smoothly using feedback
* [Adder & Subtractor](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Adder%20%26%20Substractor.jpg)- Generate two PWM signals with varying duty cycles according to PID output
	* Motor 1= base speed + PID output
	* Motor 2= base speed - PID output
* [PWM circuit](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/PWM.jpg)- Generate two different comparator voltages for the two motors
	* Motor 1 duty cycle ∝ base speed + PID output
	* Motor 2 duty cycle ∝ base speed - PID output
* [Voltage Regulator](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Voltage%20Regulator.png)- To get 3.3V and 5V for required parts accordingly
* [Speed Selector](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Circuits/Speed%20Selector.png)- Manually control the base speed

## Hardware Specifications

* [TL084CN ICs](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/TL084CN_GeneralPurposeAmplifier.pdf)
* Two [Sharp IR Sensors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/Sharp%20IR%20Sensor.pdf) 
* Two [N20 Motors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/GA12-N20%20Motor.pdf)
* [L298N Motor Driver](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/data%20sheets/L298%20Motor%20Driver.PDF)
* Wheels
* [Surface Mount Resistors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/resistors.png)
* [Surface Mount Capacitors](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/capacitors.png)
* [Other Components](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Components/other%20components.png)

## Software Specifications

* Solid Works
* Altium Designer
* Multisim

![Solidworks](https://img.shields.io/badge/Solid_Works_-red)
![Altium](https://img.shields.io/badge/Altium_Designer_-%23A5915F?logo=altiumdesigner&logoColor=white)
![Multisim](https://img.shields.io/badge/Multisim_-%2357B685?logo=multisim&logoColor=white)


## Enclosure Design

![297237961-194de710-68c9-488a-863e-5720f45de2e3](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/2d6a547f-fbf7-422a-8413-5abb84247a53)

## PCB Design

![IMG-20231206-WA0012](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/a627905f-60ce-4cc6-8d41-3c2be5a326dd)

## PCB

![20231201_162731](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/6fb28673-3319-4657-9a23-ef2d5f0c3bc5)

## Team Members

![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/5d1eefcf-3d5b-4ee2-8885-1eb820ad0053)
![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/5746e874-041f-421d-990f-f92470da315d)



## License
 
 * This project is licensed under the MIT License. See the [LICENSE](MIT-LICENSE.txt) file for details.
   
## For More Information - [Project Report](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/blob/main/Project_Report.pdf)
