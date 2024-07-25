---
layout: page
title: Beam Profile Monitor Actuator
---


### Introduction
The beam profile monitor is a device that is mounted near the end of a proton accelerator that can be slid into the beams path to give data of its’ shape and position. It currently needs to be operated by hand and the accelerator room; hence it cannot be actuated when the accelerator is on. The aim of this project is to design and construct a device that can actuate the monitor from the control room while the accelerator is on.
 
### Design Approach
The design approach taken has been to be as minimally invasive as possible, the aim was to create an actuator that does not require any permanent modifications to the current framework, where it can be removed so the handle would function just as it does now.
The handle is a 22 mm thick cylinder that is 40 mm in diameter, which slides linearly in and out 52mm. It requires approximately 30 newtons to pull out, determined through several tests. The two options for actuation are a pneumatic air cylinder or an electric linear actuator. 
A weighted evaluation matrix was constructed to compare some of the options found on McMaster-Carr that all meet the requirements.

Feature (Weight) | Air Cylinder 6453K125 | Electric Linear Actuator 6530K111 | Stepper Motor Actuator 4290N15
--- | --- | --- | --- 
Compactness (8) | 5 | 0 | 4
Simplicity of implementation (10) | 4 | 5 | 2
Reliability (5)	| 5 | 4	| 1
Cost (5) | 4 | 1 | 5
Total | 125	| 74 | 82



Since fine position control is not needed, a pneumatic solution would likely be simpler and more reliable, as it can be connected to the existing vacuum pump, and would not need any sort of large power supply or motor driver. 
Another thing to note is that both electric solutions are only available in 2 inch stroke lengths, which would be 1.5mm too short, or 4 inch stroke lengths, which would hurt its compactness even more. Whereas the air cylinder comes is 2.5 inch stroke lengths, which would fit nicely.
The selected cylinder is the second smallest option on McMaster-Carr, as it provides a decent factor of safety for the pulling force and is not much more expensive from the smallest.

 
### Detailed Design Description
#### The CAD
The design below was made with a pneumatic air cylinder in mind, as it was determined to be the most suitable solution. Below are figures of the entire assembly.

(images)

The design grips onto the handle with 2 rectangular frames cut from 1/8 inch aluminium that fit into the slot in the handle, and are screwed into an aluminum block which is attached to the piston.

(image)

The piston itself is screwed into a top mounting plate that is to be machined out of 1/4 aluminium. Hollow threaded steel rods connect the top plate and the clamps on the bottom. The clamps are made from a machined block and a 1/4 inch plate with a slot in it. The clamps were designed to fit in between the current clamps on the flange, in the area shown in red below, so the actuator can be installed and removed without having to depressurize the entire accelerator to move the existing clamps.

(image)

The clamps screw together with 2 1-1/4 inch screw that thread directally into the aluminum block.

(image)

The solenoid valve can be mounted on either side of the assembly and screws into a 1/2 inch aluminum block with tapped holes. This piece can alternitively be made from 3D printed plastic with threaded inserts to save cost. 


The tube and tube fittings selected are for 1/4 inch OD nylon tubing which may be connected directly to the air compresser, however if that is not possible, it can be connected through a T fitting to connect to an exsiting tube from another air cylinder.
The solenoid operates on 12V, 0.17A, and power can be delivered streight from the 2 green wires coming out of the wall in the accelerator room, that lead directly to the control room, where they can be wired up to a small power supply and a switch for control.



#### Actuator Position Sensors
The chosen air piston from McMaster-Carr supports the implementation of sensors that clip on to the side of the cylinder, however the OEM sensors from McMaster cost around $500 and seem to plug in to industrial PLCs, and would likely be difficult to integrate with an Arduino. After conducting some research, it seems that these “sensor ready” air cylinders have magnets in the piston, and the sensors are just reed switches or hall effect sensors with a proprietary connector. I believe that we can buy our own hall effect sensors and mount them on to the side of the air cylinder to achieve the same effect for around 1% of the cost.
I plan to use DRV5053CAQLPG hall effect sensors mounted on the side of the air cylinder with 3D printed clips, that can then be tightened with zip ties.
However, I am not 100% certain that these hall effect sensors will work with the magnets inside the piston, so as a backup plan we can attach two small 3D printed parts onto the device with the existing screws, where one will house a small magnet and the other will hold two hall effect sensors.


#### Electronics Enclosure 
An Arduino Nano mounted on the side of the device will communicate with a second Arduino Nano in the control room over I2C through the 2 unused wires running between the rooms. An RS-15-12 Meanwell power supply is used to supply 12V, up to 1.3A to the solenoid, an LM2596 buck converter board from Amazon is used to step down the voltage to 5V for the Arduino. An FQP30N06L mosfet is used to allow the Arduino to switch on and off power to the solenoid. All of these parts are mounted inside a 3D printed enclosure with M2 screws, which is then attached to the side of the device and has a cover that is secured with one screw and can slide off the top.

There will be a second enclosure for the Arduino in the control room that will also house a toggle switch and two LEDs to indicate the position of the beam profile monitor. This control box is made in a very similar way to the previous enclosure, with a sliding lid held in place with a single screw. The same power supply is chosen except it outputs only 5V directly to the Arduino.

#### Communications Software

#### Electronics Wiring

