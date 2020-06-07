# ElementLights
Community Development Work on Element Lights by PhotonLabs

## Components and Terminology

### Controller
Used to refer to the trapezoidal component that connects the power supply to the Element Light panels.

### Panel
The hexagonal panels containing 55 LED lights.

## Hardware Versions
As far as I am aware, there are 2 distinct revisions of the Element Light panels and controller boards.

### Generation 1
The first iteration of Element Lights shipped, these have an ESP32 microcontroller on each board, communicating using a WiFi mesh.

#### Controller
The controller boards for the Gen1 lights lacks a microphone, and doesn't have an antenna cutout for the ESP32.

#### Panels
The light panels for Gen1 each possess an ESP32, allowing them to be individually controlled.  They feature a presence sensor that can be used to turn the panels off.

### Generation 2
The second iteration of Element Lights shipped, which appear to have been simplified and made cheaper.  These have a single ESP32 microcontroller on the controller board, and use a wired bus for communicating between panels.

#### Controller
The Gen2 controller features a microphone, which can be used for sound-reactive animations and effects.

#### Panels
The Gen2 panels appear to rely on the wired bus for lighting information, as they lack an ESP32 (compared to the Gen1 panels), as well as lacking the presence sensor for interactivity.

##### Notes on the Gen2 Bus and Light Addressing
Each Gen2 panel appears to act as a 'hub' for all panels connected to it.  As a result, each panel is effectively addressed based on it's 'depth' from the controller.  Each panel at a given 'depth' will be identical

## Interoperability Between Generations
No testing has been done at this time regarding interoperability between panels of different generations.
