## Project Description
This project is an attempt to create a variation of "reaction game." The game has a buzzer, a multicolor LED, and two buttons, one on either side of the breadboard.  
When the game's script is run:
- Each player selects a color from a list
- The game is started by pressing ENTER
- After a random time (a few seconds) the buzzer will sound indicating the start
- Each player presses their button as quickly as they can
- The LED lights up with the color of the player who won
## Resources Used
- Raspberry Pi
- Breadboard
- 10 male-to-female jumper cables
- 2 push-button switches
- 3 220 Ohm resistors
- 1 RGB LED
- 1 Buzzer


## Building the Project
#### Step 1: Connect the LED
Here we have connected the cathode of the LED to the ground and 220 Ohm resistors bridging each other leg of the LED to where we will connect power from GPIO pins. 

![[image15.jpeg]]
![[image12.jpeg]]

#### Step 2: Connect the Buttons
Next we connect GPIOs 9, 10, 11 to the LED's legs on the other side of the resistors, attach the buttons, and wire them to GPIOs 4 and 13 and the opposite side to ground.
![[image14.jpeg]]

#### Step 3: Test the Components so far
Next, I wrote a simple script using the GPIO library to test that all of the components are working properly, and they were.

#### Step 4: Attach the Buzzer
This is where my project failed.  I couldn't find any documentation for the buzzer pictured below, so tried every possible configuration I could think of and they all failed.
I attached the buzzer to a ground and GPIO to VCC: the buzzer wouldn't do anything
I attached the ground to ground, the I/O to GPIO, and the VCC to 5v power: As soon as the Pi was powered on the buzzer sounded until the power was removed.
I replaced the 5v power with 3.3v: the buzzer didn't work at all

![[image11.jpeg]]![[image9.jpeg]]