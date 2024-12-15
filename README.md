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
### 1.Motor Driver Connections (L298N):
* ![ Diagram!](d3.jpg)
    * motorPin1 (Pin 5) → IN1 on the motor driver
    * motorPin1 (Pin 6) → IN2 on the motor driver
    * motorPin1 (Pin 10) → IN3 on the motor driver
    * motorPin1 (Pin 11) → IN4 on the motor driver
    * Connect the motor's terminals to the OUT1 and OUT2 pins on the motor driver.
    * Connect the motor's terminals to the OUT3 and OUT4 pins on the motor driver.
    * VCC → This is the pin which supplies power to the motor. It is imprinted with +12V on board but can be powered between 6-12V.
    * 5V → This pin supplies the power (5V) for the internal circuit (L298N IC). Will be used only if the 5V enable jumper is not intact. If jumper is intact, then it acts as an output pin.
    * Ground → This is the common ground pin.
### 2.LEDs:
* (WhiteLED) Front Right   pin A0 for Arduino Uno
* (WhiteLED) Front Right   pin A1 for Arduino Uno
* (red LED) Back Right    pin A3 for Arduino Uno
* (red LED) Back Right    pin A4 for Arduino Uno
## Code Overview
# setup():
*  pinMod esetup and Set the baud rate to your Bluetooth module.
# loop():
* Initialize with motors stoped.
## Operation Summary
# Motor Speed Control:
* You remove power and the motor stops. To control the speed we must periodically connect and remove power and do this very fast, so the motor "thinks" it is always powered, but with less power, according to the ON/OFF time ratio.
# LED Indicators:
* red led and WhiteLED on and off all led
## Troubleshooting
### 1.Motor Not Starting:
* DC motors to work while connected through Bluetooth in my Arduino UNO. My project is an RC car controlled by an Android app based on an Instructable. The problem with my project is that no motors are moving when I try to operate it with the Android app. This problem has been occurring for many weeks now, so I thought purchasing a new L293D motor driver would be a solution, but I still can't control the motors. I don't believe the Bluetooth transceiver (HC-06) is having any problems because it still connects to the Android device. The motors probably aren't broken because they still move flawlessly when given direct power. I would like some helpful solutions to this because I really want to finish my project soon. 
