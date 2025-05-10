# Arduino Automatic Gate Control System

This project implements an automatic gate control system using Arduino, featuring ultrasonic distance sensing, LED indicators, and servo motor control.

## Features

- Automatic gate opening when objects are detected within 10cm
- Visual status indicators using red and blue LEDs
- Audible feedback using a buzzer when the gate is open
- Automatic gate closing after 5 seconds of no detection
- Smooth servo motor control for gate movement

## Hardware Requirements

- Arduino board (Uno, Nano, or similar)
- HC-SR04 Ultrasonic Sensor
- SG90 Servo Motor
- 2 LEDs (Red and Blue)
- Buzzer
- Jumper wires
- Power supply

## Pin Connections

| Component          | Arduino Pin |
| ------------------ | ----------- |
| Ultrasonic Trigger | 2           |
| Ultrasonic Echo    | 3           |
| Red LED Anode      | 4           |
| Red LED Cathode    | 8           |
| Blue LED Cathode   | 7           |
| Blue LED           | 5           |
| Servo Motor        | 6           |
| Buzzer             | 12          |

## How It Works

1. The system continuously monitors the distance using the ultrasonic sensor
2. When an object is detected within 10cm:
   - The gate opens (servo rotates to 90 degrees)
   - Blue LED turns on
   - Red LED turns off
   - Buzzer starts beeping
3. After 5 seconds of no detection:
   - The gate closes (servo rotates to 6 degrees)
   - Red LED turns on
   - Blue LED turns off
   - Buzzer stops

## Installation

1. Connect the hardware components according to the pin connections table
2. Upload the `Gate.ino` sketch to your Arduino board
3. Power on the system

## Customization

You can modify the following constants in the code to adjust the system's behavior:

- `thresholdDistance`: Detection distance (default: 10.0 cm)
- `closedAngle`: Servo angle when gate is closed (default: 6 degrees)
- `openAngle`: Servo angle when gate is open (default: 90 degrees)
- `closeDelay`: Time before gate closes (default: 5000 ms)

## Credits

**Author:** MUNEZA Jean Dieudonne  
**Contact:** munezadieudonne2021@gmail.com

## License

This project is open source and available under the MIT License.
