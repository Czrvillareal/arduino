# Arduino & FastAPI Remote LED Control using Button
This project connects an Arduino with a FastAPI server, allowing remote control of an LED using an API. The system listens for button presses on the Arduino and sends corresponding API requests to an external server.

This will only work if there are two users, One with the button and One with the LED light. In this particular scenario, the user is the one who has the button.
## Preparation

1. What you need:
    1. Arduino UNO 
    2. LED
    3. Button
    4. Resistor
    5. USB cable
    6. Wires
    7. Python environment with FastAPI installed
    8. Breadboard


## Explanation
1. Arduino Setup
    1. Upload arduino_control_button-arduino.ino to your Arduino.

2. Flow
    1. The Arduino detects a button press and sends "group2_on" or "group2_off" over serial.
    2. Using the Python script it reads the serial data and makes an HTTP request to the external API.
    3. The FastAPI server listens for API requests:
        - If "group2_on" is received, it sends a serial command to turn the LED ON.
        - If "group2_off" is received, it sends a serial command to turn the LED OFF.
    4. The Arduino connected to the FastAPI server receives the command and controls the LED accordingly.
