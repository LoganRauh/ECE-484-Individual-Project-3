# ECE-484-Individual-Project-3

## Introduction
This project had the goal to create a component to a Pinball machine. This particular part is the player controlled mechanism that hits the ball upwards into the obstacles, known as the flippers. In the process of making these I ran into a few issues that resulted the following system not working. I will still outline how to create the system and then explain what I did and why I think it didn't work.

---

## Components
* Git
* Arduino IDE and code
* Circuit
* Flipper
* Outputs
* Adjustments
* Conclusion
* Using the Project

---

## Git
Git can be installed in the following link: https://git-scm.com/downloads

## Arduino
You'll need to install an Arduino IDE in order to put the code onto your Arduino to operate the circuit.

Follow this link and install the IDE that fits your device, https://www.arduino.cc/en/software.

### Code
My code has two parts. First is a commented out simple two button and two solenoid code that if very simple. There is a the not commented code that I made for this project, which has an inversion element, after the buttons are pressed a total of 25 times the controls inverse (left button -> right solenoid, right button -> left solenoid)!

You'll now need the code to run with the Arduino, this can be downloaded from the respository which I will outline how to do below in the "Using the Project" section!

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

There are three key parts to the flippers to note: the paddle (1), the rotation point (2), and the solenoid connnection (3). These will be outlined below.

![20240517_104243](https://github.com/LoganRauh/ECE-484-Individual-Project-3/assets/94214499/c01d4992-c4e7-4389-880a-7d88428c6420)

---

## Outputs
The circuit above worked originally. The button was able to be pressed which activated the solenoids. This was for a period of time however, eventually the solenoids stopped working even after replacing all of the other components (including the Arduino). This was potentially due to an unsafe tests I made originally (explained later). As such I didn't get a demo video until this burnout happened. Still I do believe this circuit is a correct system to use for the purposes of making a button/solenoid circuit.

However, as a flipper the solenoids used were simply not powerful enough to push the ball enough for the pusposes of pinball, reaching roughly halfway up the board. I don't believe these solenoids with the given parameteres (ball and board size) would work for this project. So this circuit succeeded as a solenoid system but failed as pinball flippers.

### Adjustments
This was my first project that used operating voltages above 5V. As such I spent a period of time learning how to properly integrate with these higher voltage components (and was quite nervous to do so). For the solenoids I initially started with 5V solenoids, since I wanted to be in a familiar place with unfamiliar solenoids. After some testing I was able to get the proper output. However, these were far too weak in order to function as a flipper. So I moved onto using 12V.

There are two common methods to reduce voltage for the uses of Arduino, this is a relay or a transistor. After research I found transistors to be the more common option. Integration was fairly straight forward, eventually landing on the transistors shown above. I made an admittely dumb mistake by assuming that the bread board I was using had each side rail split into two sections and plugged both my different power supplies (12V and 5V) into the same rail, zap frying my Arduino.

I also had a running theory that potentially the buttons that I was using were accepting more amps than they are graded to handle, which may be true but since there are two different accepted voltage sources and there was no entropy taking place (the button heating up) I'm not convinced my circuit was damaging the buttons. The solenoids however heated up greatly when being used even it was only just a few clicks of the button.

For the flippers I tried a few models to try and maximize the amount of force on the ball. I tried changing the solenoid connection point height and also tried using rubber bands to see if that would increase the power. These attempts resulted in mostly nothing noticeable. I had very limited experience in 3D printing before this project and admittely didn't want to spend more money on the project than I already had so I decided to skip on using that method but recognize its a good alternative to cardboard if not better.

## Demo
Below is a link to the demo of the circuit. Notable the solenoids don't move in the demo and this is due to them being burnt out from previous testing and as such weren't available.

(Link)

## Conclusion
I believe that this project was a success as an experiment and learning oppotunity. As previously stated the circuit was successful but the flippers were a failure. I spent roughly $40-50 and 20-24 hours in my efforts for this individual project. If someone wanted to recreate something like this with similar experience to mine this would be a good resource to build off of but not emulate completely.

---

## Using the Project
If you would like to use either my circuit/flipper design, or code. Follow this proceedure: after installing the IDE, creating the circuit, and creating the flipper(s). Now you need to clone the repository, please follow these steps:

1. Open your command prompt by typing "cmd" in your devices search bar
2. Next you need to navigate the command prompt to find the file location you'd like to clone the repository file to. You can do this by typing "cd" then file_path_to_direcctory
3. Now click the large green "<> Code" button in this github project
4. A small window will appear, copy the link by clicking the double square button. A visual is shown below
   
   ![Screenshot 2024-05-17 132930](https://github.com/LoganRauh/ECE-484-Individual-Project-3/assets/94214499/98964bc0-4bb4-47df-9514-1eade4788674)

5. Finally, in the command prompt type "git clone" followed by the copied link which you can copy into the command prompt line by right clicking


Simply connect your device to the Arduino, upload the code (make sure to click on the "Tools" tab and have your Arduino as the selected port). After uploading, connect your voltage sources and click the buttons to fire off the solenoids!


