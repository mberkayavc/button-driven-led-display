# button-driven-led-display

1. The `main` function is the main part of the program and represents the operating point of the microcontroller.
2. The program runs continuously in an endless loop.
3. Inside the loop, the state (`buttonState`) of the button on pin 6 of the GPIOC port is read.
4. If the button is pressed (button status is 1), the following operations occur:
   - The `counter` variable is incremented by one.
   - A certain waiting period (provided by the 'delay' function) is passed.
   - Depending on the value of `counter`, the LEDs are controlled according to a certain pattern.
   - If `counter` reaches 3, `counter` is reset.
5. These processes repeat continuously and the LED pattern changes each time the button is pressed.

The pattern in the relevant code follows these steps:

If the counter is 1 -> only Pin 0 on the GPIOB port is on and the other pins are off.

If the counter is 2 -> Pin 0 and Pin 1 on the GPIOB port are on, Pin 2 is off.

If the counter is 0 or 3 -> Pin 0, Pin 1 and Pin 2 on the GPIOB port are lit.

In this way, each time the button is pressed, the lighting state of the LEDs changes depending on the value of the counter, representing a visual pattern. The pattern here is based on the lighting state of the LEDs and their combination, not on the flashing frequency. The flashing frequency is achieved by waiting for a certain period of time with the delay function.

