---
layout: page
title: The Nalo Mix Pro
---

<img src="{{ site.github.url }}/assets/img/nalo_mix_thumbnail.jpg" alt="bing" width="100%"/>

## About
This project was a part of my first year design course APSC101, where we had to create a device that could dispense a set amount of water and naloxone (we used Kool-Aid) into 5 test tubes at the push of a button. Our design was successful in completing the task efficiently and effectively.

We had to use the components provided to us, including several gears, a servo motor, a small DC motor, a water pump, an Arduino UNO and an Arduino motor shield. 

## Hardware
Designed with Solidworks, implementing DFM/DFA principles like avoiding overhangs and imbedding m4 nuts. It was fabricated with 3d printing and laser cut acrylic sheets.

The most unique part of our design was that we used an auger-style screw to dispense the powder with a much higher accuracy compared to the "trap door" style dispenser that all other groups used. We were able to implement this by disassembling the servo motor and ripping out the potentiometer to let it spin continuously. 

Instead of using the provided plastic gears to make a large and bulky gearbox with lots of slop, we decided to 3D print a worm gear and a large spur gear that fits around the entire turntable, giving us our desired ratio with only 2 gears.

The entire enclosure was also 3D printed to hide all the electronics and allowed the powder to be filled from the top by removing a lid, and the water to be refilled with a fold-out funnel on the back.

Below are some screenshots from the Solidworks cad:
<img src="{{ site.github.url }}/assets/img/nalo_mix_cad_exploded.jpg" alt="bing" width="100%"/>

<img src="{{ site.github.url }}/assets/img/nalo_mix_cad.jpg" alt="bing" width="100%"/>

## Software
The code was written in C in the Arduino IDE and is pretty simple. 

The main operations start with calling the `buttonPressDetection()` function every loop to determin the mode to enter. This function will return a `buttonStatus` value based on wether the button press was a single press, double press, or long press.

We then have a switch case to decide based on the button press to either enter "Purge mode" when adding new powder or water, "Rotate turnable mode" to make removeing the test tubes easier, or the standard "Dispensing mode".

When in dispensing mode, it would take in the amouts of water and powder from an array and convert it to time values in milliseconds, based off of previous testing. Dispense both at the same time and rotate to each test tube with a limit switch that could sense the position of the turn table.

And it is also constantly calling the `eStopCheck()` function every loop so it can be shut off at anytime for safety.

<!--## Downloads
The CAD
The Code
-->