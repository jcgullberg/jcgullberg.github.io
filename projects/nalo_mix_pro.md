---
layout: page
title: The Nalo Mix Pro
---

<img src="{{ site.github.url }}/assets/img/nalo_mix_thumbnail.jpg" alt="bing" width="100%"/>

This project was a part of my first year design course APSC101, where we had to create a device that could dispense a set amount of water and naloxone (we used Kool-Aid) into 5 test tubes at the push of a button. Our design was successful in completing the task efficiently and effectively.

We had to use the components provided to us, including several gears, a servo motor, a small DC motor, a water pump, an Arduino UNO and an Arduino motor shield. 

## Hardware
The most unique part of our design was that we used an auger-style screw to dispense the powder with a much higher accuracy compared to the "trap door" style dispenser that all other groups used. We were able to implement this by disassembling the servo motor and ripping out the potentiometer to let it spin continuously. 

Instead of using the provided plastic gears to make a large and bulky gearbox with lots of slop, we decided to 3D print a worm gear and a large spur gear that fits around the entire turntable, giving us our desired ratio with only 2 gears.

The entire enclosure was also 3D printed to hide all the electronics and allowed the powder to be filled from the top by removing a lid, and the water to be refilled with a fold-out funnel on the back.

Below are some screenshots from the Solidworks cad:
<img src="{{ site.github.url }}/assets/img/nalo_mix_cad_exploded.jpg" alt="bing" width="100%"/>

<img src="{{ site.github.url }}/assets/img/nalo_mix_cad.jpg" alt="bing" width="100%"/>

## Software
The code was written in C in the Arduino IDE and is pretty simple. 

The main operations start with 

`void loop() {                   // Main loop
  
  buttonStatus = 1;             // 1 is standard state (looping), 2 is one press, 3 is a double press, 4 is a press and hold
  
  eStopCheck();

  pulseLED();

  
  if(digitalRead(StartPin) == LOW){
    buttonStatus = buttonPressDetection();
  }
  
  
  if(buttonStatus == 2){
    Serial.println("Dispensing...");
    dispenseFunction();
    buttonStatus = 1;
  }else if(buttonStatus == 3){
    Serial.println("Entered Purge Mode.");
    purgeMode();
    buttonStatus= 1;
  }else if(buttonStatus == 4){
    Serial.println("Rotating turn table.");
    rotateTurnTable();
    buttonStatus = 1;
  }

  delay(10);
}`