# Fire Sensor Simulation in Arduino

This Arduino project detects potential fire hazards by monitoring both temperature and brightness levels. If the temperature and brightness exceed predefined thresholds, an LED blinks to indicate fire detection.

## Preparation
1. What you need:
    - Arduino UNO 
    - Temperature Sensor
    - Photoresistor
    - LED
    - Wires
    - Resistors
    - Breadboard

2. [Breadboard Diagram here.](./fire_sensor_simulation_breadboard-diagram.png)

## Explanation
1. Setup
    - Temperature Sensor (A0): Reads temperature in degrees Celsius. The threshold is set to 50°C.
    - Photoresistor (A2): Measures ambient brightness. The threshold is 220.
    - LED (12): Used as a fire warning indicator.
    - Serial Monitor (9600 baud): Displays real-time temperature and brightness values.
2. Loop
    - The temperature and brightness are read continuously.
    - If both values exceed their respective thresholds, the LED blinks rapidly (100ms ON/OFF) for 10 cycles.
    - If conditions return to normal, the LED remains OFF.
    - The system updates readings every second (delay(1000)).