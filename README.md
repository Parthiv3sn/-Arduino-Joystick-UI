# Arduino Joystick Direction Controller

An Arduino interface that reads an analog joystick, displays its direction on a 16×2 I²C LCD, and lights a matching direction LED.

## Features

- Detects top, bottom, left, right, and center joystick positions
- Shows the detected direction on an I²C LCD
- Drives one LED for the active direction
- Outputs joystick readings over serial at 9600 baud

## Hardware

- Arduino Uno or compatible board
- Analog joystick module
- 16×2 I²C LCD (address `0x27`)
- 4 LEDs with current-limiting resistors

## Wiring

| Function | Arduino pin |
| --- | --- |
| Joystick X / Y | A0 / A1 |
| Joystick switch | 7 |
| Bottom / Right / Left / Top LEDs | 8 / 9 / 10 / 11 |
| LCD | I²C SDA / SCL |

The joystick switch uses `INPUT_PULLUP`; connect it to GND when pressed.

## Setup

1. Install the **LiquidCrystal_I2C** library.
2. Open `Source Code` (rename it to `JoystickUI.ino` if needed).
3. Confirm your LCD’s I²C address; update `0x27` if your module differs.
4. Upload and open Serial Monitor at **9600 baud**.

## Project files

- `Source Code` — Arduino sketch
- `Circuit_Image .png` — wiring reference

## Improvement ideas

- Use calibrated joystick thresholds or a configurable dead zone.
- Use the joystick switch to select a menu action.
- Add non-blocking timing to make display updates more responsive.

## License

No license has been specified. Add one before reusing or distributing this work.