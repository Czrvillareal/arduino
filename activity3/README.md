# Photoresistor

This Arduino project uses a photoresistor to detect changes in brightness and triggers an LED blinking alert when brightness exceeds a defined threshold. The blinking can be stopped via a serial command.

## Preparation
1. What you need:
    - Arduino UNO 
    - Photoresistor
    - LED
    - Wires
    - Resistor
    - Breadboard

2. [Breadboard Diagram here.](./photoresistor_breadboard-diagram.png)

## Explanation
1. Setup
    - The photoresistor is connected to analog pin A2 to measure ambient light levels.
    - The LED is connected to digital pin 12 to signal fire detection.
    - The Serial Monitor (9600 baud rate) is used to display brightness values and accept commands.
2. Loop
    - The system continuously reads brightness levels.
    - If the brightness exceeds 220, the LED starts blinking.
    - The user can stop blinking by typing "stop" in the Serial Monitor.
    - If brightness remains low, the LED stays OFF.