---
layout: page
title: The Nalo Mix Pro
---

<img src="{{ site.github.url }}/assets/img/nalo_mix_thumbnail.jpg" alt="bing" width="100%"/>

This project was a part of my first year design course APSC101, where we had to create a device that can dispense a set amount of water and naloxone (we used kool aid) into 5 test tubes at the push of a button.

We had to use the components provided to us, including a bunch of gears, a servo motor, a small DC motor, a water pump, an Arduino UNO and Arduino motor shield. 

## Hardware
The most uniqe part of our design was that we used a auger style screw to dispense the poweder with a much higher accuracy compared to the "trap door" style dispenser that all other groups used. We were able to impliment this by disasembling the servo motor and ripping out the potentiometer to let it spin continously. 

Instead of using the provided plastic gears to make a large and bulky gearbox with lots of slop, we decided to 3D print a worm gear and a large spur gear that fits around the entire turntable, giving us our desired ratio with only 2 gears.

The entire enclosure was also 3D printed to hide all the electronics and allowed the powder to be filled from the top by removing a lid, and the water to be refilled with a fold out funnel on the back.

<img src="{{ site.github.url }}/assets/img/nalo_mix_cad_exploded.jpg" alt="bing" width="40%"/>

<img src="{{ site.github.url }}/assets/img/nalo_mix_cad.jpg" alt="bing" width="40%"/>

## Software
