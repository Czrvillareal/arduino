# Remote LED Control using FastAPI
This project sets up a FastAPI server that communicates with an Arduino via a serial connection. The API allows users to turn an LED ON or OFF by sending HTTP requests.

## Preparation

1. What you need:
    1. Arduino UNO 
    2. LED
    3. Resistor
    4. USB cable
    5. Python environment with FastAPI installed
    6. Breadboard

2. [Breadboard Diagram here.](./light_fastapi_breadboard-diagram.png)

## Explanation
1. Arduino Setup
    1. Upload light_fastapi_arduino-code.ino to your Arduino.

2. Setup
    1. The FastAPI server initializes a serial connection to the Arduino on COM3 (9600 baud).
    2. If the connection is successful, the server is ready to receive requests.

3. Loop
    1. POST /led/on
        - When a "1" is received, "1" is sent to the Arduino to turn the LED ON.
        - Returns a success message if the command is sent successfully.
    2. POST /led/off
        - When a "0" is received, "0" is sent to the Arduino to turn the LED OFF.
        - Returns a success message if the command is sent successfully.