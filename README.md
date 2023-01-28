# EurorackChordSequencer
This project gives some information about my built of a modular synthesizer 8-step CV sequencer module in the Eurorack format.
The module is an extension of the sequencer module from TimMJN , making use of an Arduino Nano as the central control unit.

Please check the [GitHub project from TimMJN](http://github.com/TimMJN/Arduino-Sequencer).

There are a few changes to the original design:
- Extension to 3 individual CV outputs for controlling chords
- Switches for each of the 8 steps to control a gate signal output for each step
- In planning: quantization of CV outputs (see details below)

A [demonstration video](https://youtu.be/u9PBp1COE9A) can be checked on YouTube.

## Arduino Firmware
The code for the Arduino Nano is taken from the sequencer project from TimMJN.
I did not yet change anything, and the current version of the module contains the same functions, as the one from Tim MJN.

## PCB Design
I built this module, like most of my other DIY modules, using two PCB levels. The control PCB is used for all control components at the front of the module. The other main PCB contains the main circuit components, like the Arduino Nano.
Both PCBs are connected via standard header connectors.

## Module Build and PCBs
If you want to want to have PCBs for the module, I uploaded a set of Gerber files.

The module is built up by two PCBs, the control board with the control components going to the front panel and the main board behind it.
Those boards are connected via standard male and female headers with a pin distance of 2.54mm (0.1 inch).

There are two different versions for the control board, an "original" and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop, as well as small pushbottons, which I did not find at online providers, like Mouser.

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created a version with footprints for those components. Thas version also utilizes pushbuttons and switches, which you can find at Mouser.
Choose the one you need.

I created the Gerber files with the online tool EasyEDA and ordered it at JLCPCB.
I cannot guarantee, if this set of zipped Gerber files works also for other providers, like e.g. PCBWay. I have not tried that. But I saw online, that others did it.

If you want to know about my DIY building process, take a look at those two YouTube videos:
- [How I design PCBs for my Eurorack Synth Modules](https://youtu.be/pXtuV9Pv-m4)
- [Eurorack Module Synth - Building an Electric Druid Wavetable Oscillator Module](https://youtu.be/ECpdo4HfqLg)

## Panel Layout
I added the information about hole coordinates for the front panel in the folders PanelLayout_..., referring to the component layout in the Gerber files.

PLEASE NOTE! Since there is a slight difference in the location of hole no. 29 between the PCB for the "original" and the "Thonk" version, there are two different sets of coordinates. 

## Additional Information about specific Components
If you want to use the Gerber files for having PCBs manufactured, please note the following information about components used.

- There is a number of SMD 0.1uF capacitors with the package size 1608.
- For the tranistors 2N3904 the SMD version MMBT3904 is used on the PCBs.
- In order to save space, I am always using small size resistors, about 3mm length, which are about half the size of usually used resistors.
- The switches used are a standard SPDT toggle switches. Some of them are of type ON-ON, others of type ON-OFF-ON. Please check the BOMs, which differ depending on the version (original or Thonk).
- For the momentary pushbuttons in the "Thonk" version PCB (Mouser no. 8MS8P1B05VS2QES), two connection points are marked as connected. You need to orientate the pushbutton on the PCB in a way, that the connection is closed for those two points, when the button is pushed.

Many thanks to TimMJN!


![Front](https://user-images.githubusercontent.com/97026614/150731201-aff2b512-5bf7-41cf-ba18-e26e32674c4d.JPG)
![FrontSide](https://user-images.githubusercontent.com/97026614/150775298-86a71474-52ac-46d7-bc23-a0976e2a9e81.JPG)
![Back](https://user-images.githubusercontent.com/97026614/150775348-6887f31b-559f-4db2-9151-5f1113250aee.JPG)
![MainBoard](https://user-images.githubusercontent.com/97026614/150775392-d1e1c4a5-80a8-443a-8e66-608f4eda3d76.JPG)
![ArduSeqCtrl2](https://user-images.githubusercontent.com/97026614/178224754-758cf3b9-897a-4212-a1f1-b3877e479c85.JPG)
![ArduSeqCtrl1](https://user-images.githubusercontent.com/97026614/178224784-4968c778-2444-47d8-9ae6-7327c37938c8.JPG)
![ArduSeqMain1](https://user-images.githubusercontent.com/97026614/178224797-28ccbf26-be66-4726-aadb-beb963a8e684.JPG)
![ArduSeqMain2](https://user-images.githubusercontent.com/97026614/178224915-1d7b2cf2-32e2-4549-b905-9c10ba274bb0.JPG)
