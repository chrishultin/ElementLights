# Generation 2

## ESP32 GPIO Pins
| ESP32 Pin | Connected To |
| --------- | ------------ |
| GPIO32    | Microphone   |
| GPIO33    | LED Control  |

## Flashing Custom Firmware
In order to flash custom firmware onto the ESP32, connect your adapter to the
6-pin header on the controller board (as per the pinout documented below), then
connect the GPIO0 pin and Enable pin to `Ground`, then disconnect it.  This should
put the ESP32 into the correct mode to receive new firmware.

## Connectivity

### Controller Debug Header
The 6-pin header on the Controller board has the following pinout (starting with
the pin labelled '+'):
- 3.3v Power (for ESP32)
- Enable (for ESP32)
- GPIO0 (for ESP32)
- TX (on FTDI Adapter)
- RX (on FTDI Adapter)
- Ground

### Panel Connector
#### Male (From Left to Right)
- DIN (Control signal)
- 5v (from power adapter)
- Unknown/Not Connected
- Ground

### Panel Debug Header
- DIN (Control signal)
- 5v (from power adapter)
- Unknown/Not Connected
- Ground
