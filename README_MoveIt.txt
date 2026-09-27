MOTION GAME CONTROLLER – MOVEIT 


MoveIt is a portable game controller that responds to the player’s movements.
During gameplay, the OLED screen randomly displays one of five commands: Up, Down, Left, Right, or Button. It also displays the current score and the high score.

The player must point the controller in the requested direction or press the button when the “Button” command appears. The controller’s movements are detected by the MPU-6050 sensor, which includes an accelerometer and a gyroscope.

An audio system is also built into the controller. A timer sound accompanies the game to indicate the time available to perform the actions. If the player fails to correctly follow a command within the allotted time, the game ends and a defeat sound is played.

To make the game fully portable, the board is powered by three AAA batteries located on the back of the PCB. The PCB was also designed to resemble a retro video game controller.




- How the Game Works -

1. The player presses the START button to begin a new game.
2. The OLED screen displays an initial instruction: Up, Down, Left, Right, or Button.
3. The player must perform the requested action within the allotted time:
   - movements are detected by the MPU-6050;
   - the “Button” action is detected by the dedicated button.
4. If the action is performed correctly and on time, the player earns 1 point and a new instruction appears.
5. The current score and the high score are displayed on the OLED screen during the game.
6. A timer sound plays during the game. If the player fails or runs out of time, the game ends and a failure sound plays.



- Electronic Architecture / Components -

- XIAO ESP32-S3: main microcontroller responsible for managing the game and various peripherals.
- MPU-6050: accelerometer and gyroscope used to detect the controller’s orientation and movements.
- I²C OLED display: shows instructions, the current score, and the high score.
- MAX98357A + Speaker: audio system that plays the timer sound and the defeat sound.
- RGB LED: Provides visual feedback to the player.
- 3 × AAA batteries + AP2112K-3.3: Portable power supply regulated to 3.3 V.
- 3 thermistors: Monitor the temperature of the three batteries.
- START button: Starts a new game.
- Action button: Used when the “Button” instruction appears.



- Circuit Diagram -

The MoveIt circuit diagram includes the various subsystems required for the controller to function: power supply, microcontroller, motion detection, display, user interface, and audio system. The XIAO ESP32-S3 serves as the heart of the system and handles communication with the various components. In particular, the MPU-6050 and the OLED display communicate with the microcontroller via the I²C bus.

The schematic has been organized into different functional blocks to make it easier to read.



- PCB Design -

The PCB was designed entirely in KiCad 10.0. Its shape was inspired by a retro video game controller so that the printed circuit board would be an integral part of the product’s design.
The components were placed with their function and intended use in mind. In particular, the display, buttons, and RGB LED are positioned to be accessible or visible to the player.
The battery holder containing the three AAA batteries is located on the back of the PCB to leave enough space on the front for the electronic components and the user interface.

The routing uses both copper layers of the PCB (F.Cu and B.Cu) to connect the various components.



- Project Files -

    MoveIt_PCB/
    │
    ├── MoveIt_PCB_BELLAICHE Chloé.kicad_pro
    ├── MoveIt_PCB_BELLAICHE Chloé.kicad_sch
    ├── MoveIt_PCB_BELLAICHE Chloé.kicad_pcb
    ├── README_MoveIt.md
    │
    └── images/
        ├── schematic.png
        ├── pcb.png
        ├── pcb_3D_front.png
        └── pcb_3D_back.png











