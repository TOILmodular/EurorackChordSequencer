# EurorackChordSequencer
This project gives some information about my built of a modular synthesizer 8-step CV sequencer module in the Eurorack format.
The module is an extension of the sequencer module from TimMJN , making use of an Arduino Nano as the central control unit.

Please check the [GitHub project from TimMJN](http://github.com/TimMJN/Arduino-Sequencer).

There are a few changes to the original design:
- Extension to 3 individual CV outputs for controlling chords
- Switches for each of the 8 steps to control a gate signal output for each step
- In planning: quantization of CV outputs (see details below)

A demonstration video is existing on YouTube.

## Arduino Firmware
The code for the Arduino Nano is taken from the sequencer project from TimMJN.
I did not yet change anything, and the current version of the module contains the same functions, as the one from Tim MJN.

## Quantization of CV Outputs
I created a new Arduino code version, which includes a simple chromatic quantization of all 3 CV outputs.
However, I could not yet build test that version of the module, because I would need a multi channel DAC, the MCP4728, a quad 12-bit DAC.
That IC is currently not available, I assume due to the global microchip shortage.
I will update this project with the new code and schematic, as soon as I could purchase a chip and test the changes.
The control component layout of the module will rermain unchanged. Only the PCB with the Arduino will be changed by adding the MCP4728.

## PCB Design
I built this module, like most of my other DIY modules, using two PCB levels. One PCB is used for all control components at the front of the module. The other PCB contains the larger circuit components.
Both PCBs are connected via standard header connectors.
You can check out more details about my way of designing modules that way via [this YouTube video](https://youtu.be/pXtuV9Pv-m4).

Many thanks to TimMJN!


![Front](https://user-images.githubusercontent.com/97026614/150731201-aff2b512-5bf7-41cf-ba18-e26e32674c4d.JPG)
![FrontSide](https://user-images.githubusercontent.com/97026614/150775298-86a71474-52ac-46d7-bc23-a0976e2a9e81.JPG)
![Back](https://user-images.githubusercontent.com/97026614/150775348-6887f31b-559f-4db2-9151-5f1113250aee.JPG)
![MainBoard](https://user-images.githubusercontent.com/97026614/150775392-d1e1c4a5-80a8-443a-8e66-608f4eda3d76.JPG)
