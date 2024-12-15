## fighter_bot

This project involves controlling a HC-05 Bluetooth Module, 5 DC motor using an Arduino board, a motor driver module, a potentiometer for speed control, and LEDs for status indication. The motor runs for a specified duration, and the system provides visual feedback via the LEDs. The project is designed to be simple yet effective in controlling the

## Pin Configuration
- motorPin1 (Pin 5): Controls the direction of the motor (via motor driver).
    - motorPin2 (Pin 6): Controls the direction of the motor (via motor driver).
* motorPin3 (Pin 10): Controls the direction of the motor (via motor driver).
    * motorPin4 (Pin 11): Controls the direction of the motor (via motor driver).
* redLedPin (Pin A2,3): Indicates the motor is off (red LED).
    * WhiteLedPin (Pin A0,1): Indicates the motor is on (White LED).

## Key Logic Breakdown
### 1. Motor Control:
* The motor's direction and speed are controlled via the motor driver module.
Speed is determined by the bluetooth rc cantrola app 
* runTime 10 hour 
  ### 1. LED Control:
    * Also, it is quite nice to be able to switch on and off an LED using a mobile app.

    * To do this, you do not really need much of prior knowledge at all, and is very easy to do. 
## Circuit Diagram
### 1.Motor Driver Connections (L298N or L293D):
![ Diagram](d3.jpg)
