---
layout: page
title: Beam Profile Monitor Actuator
---

James Gullberg, 2024/5/16
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
The design below was made with a pneumatic air cylinder in mind, as it was determined to be the most suitable solution. Below are figures of the entire assembly.

