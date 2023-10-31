# MicroController_C
# IMP Lab Assignment 2 - GPIO Button Handling with Interrupts

This is the solution for Laboratory Assignment 2 from the IMP (Embedded Systems) course. It demonstrates the use of GPIO for handling button presses using interrupts on an MKL05Z4 microcontroller.


## Overview

This code demonstrates the use of GPIO to handle button presses using interrupts on the MKL05Z4 microcontroller. It includes functions for creating a short beep sound and flashing an RGB LED.

## Pin Definitions

- BUTTON_UP_MASK: 0x08
- BUTTON_CENT_MASK: 0x10
- BUTTON_LEFT_MASK: 0x20
- BUTTON_DOWN_MASK: 0x40
- BUTTON_RIGHT_MASK: 0x80
- PIEZZO_MASK: 0x2000
- LED_R_MASK: 0x200
- LED_G_MASK: 0x300
- LED_B_MASK: 0x400

## Functions

### `delay(uint64_t bound)`

This function provides an active delay for a specified number of cycles.

### `beep(int zpoz)`

This function generates a short beep sound using the piezo buzzer. It takes the duration of the beep as a parameter.

### `flash()`

This function causes a short flash on the red LED.

### `flash1()`

This function causes a short flash on the green LED.

### `PORTB_IRQHandler(void)`

This is the interrupt service routine (ISR) for handling button presses. It checks which button was pressed, filters out button bounce, and triggers the appropriate response, such as flashing an LED or generating a beep.

### `init_hardware(void)`

This function initializes the microcontroller hardware, including configuring pins for buttons, LEDs, and the piezo buzzer.

### `main(void)`

The main function initializes the hardware and enters an infinite loop, waiting for button press interrupts to trigger responses.

## Usage

1. Set up your development environment for the MKL05Z4 microcontroller.
2. Build and flash this code onto the microcontroller.
3. Connect the required hardware components, including buttons, LEDs, and the piezo buzzer.
4. Press the buttons, and the code will respond with flashes and beeps according to the button pressed.

Please note that the code assumes a specific hardware setup. Make sure to consult the microcontroller's documentation and your hardware configuration to adapt the code as needed.

Have fun experimenting with button presses and the microcontroller's GPIO!


