# ECE-484-Individual-Project-3

## Introduction
This project had the goal to create a component to a Pinball machine. This particular part is the player controlled mechanism that hits the ball upwards into the obstacles, known as the flippers. In the process of making these I ran into a few issues that resulted the following system not working. I will still outline how to create the system and then explain what I did and why I think it didn't work.

---

## Components
* Arduino IDE and code
* Circuit
* Flipper

---

## Arduino
You'll need to install an Arduino IDE in order to put the code onto your Arduino to operate the circuit.

Follow this link and install the IDE that fits your device, https://www.arduino.cc/en/software.

### Code
You'll now need the code to run with the Arduino, this can be downloaded from the respository which I will outline how to do below.

(OUTLINING HOW TO DO IT)

## Circuit
For the circuit you'll need the following compoents:
* 1 Arduino Uno
* 2 12V Solenoids
* 2 Buttons
* 2 IRF520 Mosfet Transistors
* 2 1N4007 Diodes
* 2 10k Ohm Resistors
* 2 1k Ohm Resistors
* Wires

Once you have all of the above components, create the circuit shown below. One note, you'll need a 12V source and a 5V source. This can be accomplished many ways, I used an 8 1.5V battery holder for my 12V source and my laptop as a 5V source when connected to the Arduino. A sign of causion, if the Arduino consumes 12V you are at risk of damages or completely burning out your Arduino or another component!

## Flipper
My flippers are completely made from cardboard and tape, and they are addmitedly very simple. They can however be 3D printed for a more sturdy output or simply adjust your flipper to your needs or size needed.

There are three key parts to the flippers to note: the flipper (1), the rotation point (2), and the solenoid connnection (3). These will be outlined below.

![20240517_104243](https://github.com/LoganRauh/ECE-484-Individual-Project-3/assets/94214499/c01d4992-c4e7-4389-880a-7d88428c6420)

## Using The Program
After installing the repository files, installing the IDE, creating the circuit, and creating the flipper(s). Simply connect your device to the Arduino, upload the code (make sure to click on the "Tools" tab and have your Arduino as the selected port). After uploading, connect your voltage sources and click the buttons to fire off the solenoids!


