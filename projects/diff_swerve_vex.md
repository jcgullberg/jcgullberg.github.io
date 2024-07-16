---
layout: page
title: VEX Differential Swerve Modules
---
<img src="{{ site.github.url }}/assets/img/diff_swerve_v2v3_.jpg" alt="bing" width="100%"/>

## About
This project began two thirds the way through the 2023 ~ 2024 Vex season, when I got recruited onto the team specifically for this project. But fresh off designing my first swerve module, I knew exactally all the changes and improvements I needed to make, which allowed me to go from joining the team to a finished and working prototype in lass than a week.

The modules we supposed to be completly printed on Markforged printers in Onyx CF Nylon, unfortunatly we ran out of time beforethe compitition so only a couple parts in each module was nylon and the rest were printed in PLA.

During our matches at the Vex World Chanmpionship in Dallas, My biggest fear was the reliability of the modules would be poor. Luckily the modules actually held up quite well, the only fault we had in all our matches was the teeth sheard off one of the bevel gears due to under extrusion in the print.

Although we didn't place that well overall, after the compitition we discussed all the changes that needed to be made and got to work making an increadibly compact and reliable swerve module that the team can use for years to come.

## The Design
### 2023 ~ 2024 Module
<img src="{{ site.github.url }}/assets/img/diff_swerve_v3_thumbnail.jpg" alt="bing" width="100%"/>
I went with a completly diffferent design from my first swerve module, where it doesn't use any bevel gears in the top differential section. The main turret and ring gears are still supported with built in ball bearings, where I design in the bearing tracks into the 3D printed parts and insert 4.5mm BBs with a bearing cage, this works supprisingly well and is increadably cheap and saves space compared to buying several 100mm ball bearings. There are now two shafts with bevel gears to spread the load when tranfering the power to the wheel. 


If you want to take a closer look you can find an Onshape file to view it here:
<p><a href="https://cad.onshape.com/documents/2555a01d96c802705afa0753/w/fc88a9f7caf54323172ac45a/e/96277ac527fc346c79a3a30f">Onshape.com</a></p>


### 2024 ~ 2025 Module
<img src="{{ site.github.url }}/assets/img/diff_swerve_thumbnail_2.jpg" alt="bing" width="100%"/>
This module is pretty much the same as the last one, except it is a whole lot smaller. It uses a 2.75" wheel instead of the 3.25" wheel on the last one, and takes up 45% less volume in the robot. A couple small changes had to be made, like flipping the motors around. There was no room between the motors and wheel for the wires to come out with the previous setup, so they were turned 180 degrees and ideler gears were added. All the screws also had to be changed from M4 to M3 due to space constraints and a cover was added on top.

Overall, I believe this design is approching a limit for how small a Vex swerve module could be, simply because even if I shrink the main turret smaller, the width of the whole module will have to stay the same thanks to the bulky Vex motors that have to be used. This design is ready to be sent off to the Markforged printers to finally be made from nylon, and these will likely be the modules our team uses for many years to come.

Here are a few more pics to show how much smaller the new design is:


## The Reason for Omni Wheels - Nick's Master Plan
One of our team members Nick, who is also a very well known individual in the Vex robotics community, came up with a master plane to use omni wheels on the swerve modules, which can be angled to act as a CVT.

The way it works is similar to X-drive, where in X-drive when the drivebase moves forward it goes at √2 times faster than the linear speed of the wheels, because the omni wheels are angles at 45° reletive to the direction of travel.

With our modules, we can change the angle of attack of the wheels reletive to the direction of travel (theta), causing the speed of the robot to be sec(Θ) multiplied by the linear speed of the wheels. Letting us in theary, reach infinite speed.

This lets our robots simaltainously be capable of more torque or more speed than any other robot, with the added degree of freedom thanks to it being swerve drive, this is the most optimal drivetrain in Vex EVER, giving us an unparalled advantage.

## Power Take-Off
A power take-off is basically a clutch system that lets us route the power from the motors to something else on the robot. This come in super handy with one of the components of this game which is "the climb", where our robots need to climb a lader to get additional points. By connecting all 8 motors from the swerve modules together with bevel gears and driveshafts running along the bottom of the robot and connecting them to a winch for the climb, we save a ton of weight by not having to add extra motors that are just dead weight on the robot most of the time.

This mechanism is still under development, but so far is showing huge potential for our robots this season.

Here are some picture of the current CAD designs:
<img src="{{ site.github.url }}/assets/img/diff_swerve_v3_pto.jpg" alt="bing" width="100%"/>