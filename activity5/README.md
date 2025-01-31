# Midterm Laboratory

This Arduino project monitors ambient light intensity using a photoresistor and categorizes it into three levels:

1. Low (Green LED)
2. Medium (Yellow LED)
3. High (Red LED)

The system operates in two modes:

1. Automatic Mode – Adjusts thresholds dynamically based on environment.
2. Manual Mode – Allows the user to set custom light intensity thresholds via the Serial Monitor.

## Preparation
1. What you need:
    - Arduino UNO 
    - Photoresistor(A0)
    - LED (Green(pin 11), Yellow(pin 12), Red(pin 13))
    - Wires
    - Resistors
    - Breadboard

## Explanation
1. Setup
    - The photoresistor measures ambient light intensity.
    - The LEDs indicate different light intensity levels.
    - The Serial Monitor (9600 baud rate) displays real-time light intensity and allows user input.
2. Loop
    1. Reads the light intensity and converts it to a percentage (0% - 100%).
    2. If in Automatic Mode, the system categorizes the environment into:
        - Cloudy (< 40%)
        - Normal (41% - 70%)
        - Bright Sunlight (> 70%)
    3. Based on intensity, it activates the appropriate LED:
        - Green for low light
        - Yellow for moderate light
        - Red for high brightness
    4. The user can send Serial Commands to switch modes or manually adjust thresholds:
        - "MODE AUTO" – Enables automatic mode
        - "MODE MANUAL" – Enables manual mode
        - "SET LOW <value>" – Sets the low threshold (manual mode only)
        - "SET HIGH <value>" – Sets the high threshold (manual mode only)