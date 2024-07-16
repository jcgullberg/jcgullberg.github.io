---
layout: page
title: Differential Swerve Module V1
---
<img src="{{ site.github.url }}/assets/img/diff_swerve_v1_cad.jpg" alt="bing" width="100%"/>

## About
This project was originally started just as a fun side project for me to improve my design skills that was also partly inspired by my growing interest in robotics. I wanted to make 4 of them and mount them on a sofa or chair so I could drive around in any direction, but unfortunatly never got around to that due to cost constraints, however it did lead to me getting hired onto my schools VEXU robotics team directally as a technical lead to help them develop a Vex legal version.

## The Design
This module uses a ring bevel gear design, where the load is spread between 4 bevel gears instead of just one, these bevel gears are geared together with 3 more steel bevel gears that were bought off the shelf in the center. The power is then transferred down to the wheel through a set of herringbone gears, but the bottom gear isn't connected directally to the wheel, it is connected to the sun gear of a planetary gearbox that is inside the wheel. The planet gears are mounted to the wheel forks, and the rim itself is the ring gear.

To make everything turn smoothly, I would need a whole bunch of large bearings that would be extreamly expensive, so instead I implamented bearing tracks into all the 3D printing parts and inserted 4.5mm ball bearings with 3D printed bearing tracks, this ended up working suprisingly well for a fraction of the cost of regular bearings.

I planned on using brushless motors with Odrive motor controllers and as5600 magnetic encoders with an arduino to control all the modules, but the electronic costs ended up being too high for me to finish the project.

Below is a cross section image and a photo of the printed prototype:
<img src="{{ site.github.url }}/assets/img/diff_swerve_v1_cad_section.jpg" alt="bing" width="100%"/>
<img src="{{ site.github.url }}/assets/img/diff_swerve_v1_ass.jpg" alt="bing" width="100%"/>