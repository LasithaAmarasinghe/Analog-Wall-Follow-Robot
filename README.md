# Analog Wall Following Robot
This is a group project done under the module EN2091 - Laboratory Practice and Projects, Semester 3, Department of Electronic and Telecommunication Engineering, University of Moratuwa. 

## Introduction

*  Wall following robot is a robot that follows a wall and travels keeping a constant distance from the wall. 
*  Wall following is a common task in many robotics competitions.
*  But the interesting thing is our project was to build a robot that travels on the centerline between two walls, using only analog electronics. That means we couldn’t use microcontrollers.

![IMG-20231206-WA0097](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/241e426e-1c0c-4cf3-a58a-3e9705a20f41)

## Working Concept

*  We measured the distance from the robot to the side walls using two sharp IR sensors. 
*  Then using a PID control circuit, an error signal is generated.
*  That error signal is fed to the adder and subtractor circuits.
*  Two PWM signals with varying duty cycles are generated.
*  Then using the motor driver, PWM signals are fed to the left and right wheels. 
*  The robot tracks the walls and travels on the centerline between walls.

![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/68c7d26a-6e3c-42f4-9463-8e1196b14ca5)

## Sub Circuits and Tasks

* Instrumentation Amplifier- Reduce noise in Sharp IR sensor outputs and amplify signals
* PID circuit- Control the error signal smoothly using feedback
* Adder & Subtractor- Generate two PWM signals with varying duty cycles according to PID output
	* Motor 1= base speed + PID output
	* Motor 2= base speed - PID output
* PWM circuit- Generate two different comparator voltages for the two motors
	* Motor 1 duty cycle ∝ base speed + PID output
	* Motor 2 duty cycle ∝ base speed - PID output
* Voltage Regulator- To get 3.3V and 5V for required parts accordingly
* Speed Selector- Manually control the base speed

## Hardware Specifications

* TL084CN ICs
* Two Sharp IR Sensors
* Two N20 Motors
* L298N Motor Driver
* Wheels
* SMD resistors
* SMD capacitors

## Software Specifications

* Solid Works
* Altium Designer
* Multisim

## Enclosure Design

![Screenshot 2024-01-17 061048](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/194de710-68c9-488a-863e-5720f45de2e3)

## PCB Design

![Screenshot 2024-01-17 061105](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/3d634f6e-09d5-489e-bc33-8ddfe3addcb4)

![Screenshot 2024-01-17 061120](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/9f6abf7a-bebd-4099-b00e-d726d3bc01c8)

## Team Members

![image](https://github.com/LasithaAmarasinghe/Analog-Wall-Follow-Robot/assets/106037441/2d9a9b91-cac6-405b-b309-e2aa63132ca0)
