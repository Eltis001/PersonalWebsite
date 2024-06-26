# Introduction to Arduino
Arduino is an open-source hardware that manufactures single-board microcontrollers.

Below is the layout of Arduino UNO board.
![Example banner](.\Graph_Arduino\Arduino.png)

# Arduino Uno Board Pin Description

The Arduino Uno board is a popular microcontroller board based on the ATmega328P. It provides a variety of input/output pins for different functionalities. Below is a description of the functionality for each pin:

## Power Pins

- **Vin**: The input voltage to the Arduino board when it's using an external power source (as opposed to 5V from the USB connection or another regulated power source). You can supply voltage through this pin, or if supplying voltage via the power jack, access it through this pin.
- **5V**: This pin outputs a regulated 5V from the regulator on the board. The board can be powered via the USB connector (5V), the DC power jack (7-12V), or the Vin pin of the board (7-12V). Supplying voltage via the 5V or 3.3V pins bypasses the regulator, and can damage your board.

- **3.3V**: A 3.3V supply generated by the on-board regulator. Maximum current draw is 50 mA.
- **GND**: Ground pins.

## Reset Pin

- **RESET**: Reset the microcontroller. Typically used to add a reset button to shields that block the one on the board.

## Analog Pins

- **A0 to A5**: Analog inputs. These can also be used as digital I/O pins. Each pin provides 10 bits of resolution (i.e., 1024 different values). By default, they measure from ground to 5 volts, though it is possible to change the upper end of their range using the AREF pin and the analogReference() function.

## Digital Pins

- **D0 to D13**: Digital I/O pins. Each of these pins can be used as an input or output, using functions like `pinMode()`, `digitalWrite()`, and `digitalRead()`. They operate at 5 volts. Each pin can provide or receive a maximum of 40 mA and has an internal pull-up resistor (disconnected by default) of 20-50 kOhms.

## PWM Pins

- **D3, D5, D6, D9, D10, D11**: Provide 8-bit PWM output with the `analogWrite()` function.

## Serial Communication

- **D0 (RX)**: Used to receive (RX) TTL serial data.
- **D1 (TX)**: Used to transmit (TX) TTL serial data.

## SPI Pins

- **D10 (SS)**: Slave Select pin.
- **D11 (MOSI)**: Master Out Slave In pin.

- **D12 (MISO)**: Master In Slave Out pin.
- **D13 (SCK)**: Serial Clock pin.

## I2C Pins

- **A4 (SDA)**: Data line for I2C communication.
- **A5 (SCL)**: Clock line for I2C communication.

## Interrupt Pins

- **D2 (INT0)**: External Interrupt 0.
- **D3 (INT1)**: External Interrupt 1.

## AREF Pin

- **AREF**: Reference voltage for the analog inputs. Used with `analogReference()`.

## Special Functions

- **D13 (LED_BUILTIN)**: There is a built-in LED connected to digital pin 13. When the pin is HIGH value, the LED is on, when the pin is LOW, it's off.

Each of these pins can be used for specific functionalities as described, allowing the Arduino Uno to interface with a wide variety of sensors, actuators, and other electronic components.
You can copy and paste this markdown text into your markdown editor or viewer to get a nicely formatted