# Working with Analog Signals - Fading Effect with Arduino

This Arduino project gradually turns on and off five LEDs connected to different pins. The LEDs fade in and out using Pulse Width Modulation (PWM) to create a smooth brightness transition.

## Preparation
1. What you need:
    - Arduino UNO 
    - 5 LEDs
    - Wires
    - Breadboard

2. [Breadboard Diagram here.](./analog_signals_breadboard-diagram.png)

## Explanation
1. Setup
    - Defining the LED pins
    - Setting up LED pins as outputs
2. Loop
    - Gradually increases brightness of each LED to maximum using analogWrite().
    - Keeps all LEDs at full brightness for 1 second.
    - Gradually decreases brightness to turn them off.
    - Keeps all LEDs off for 1 second before repeating.