# CAN1602LONG

This is a description of the demonstration implementation of the RPC0005 CBUS protocol.

Please send any comments or requests for information to John Fletcher (M6777) john@bunbury28.plus.com 

## Long message example with pins and a display

This code supports a shield with buttons and a display with 2 rows of 16 characters.

It has been programmed so that the buttons send a long string message.

The display shows a received long string message.

The code sends on one stream ID and listens on several others.

The choice of stream IDs is made within the program.

It is necessary to have at least two units in order to send and receive messages.

## Hardware

The needed hardware is as follows

1. An Arduino UNO (or suitable clone)

2. DFRobot shield (DFR0009) https://wiki.dfrobot.com/LCD_KeyPad_Shield_For_Arduino_SKU__DFR0009

   This plugs into the UNO and provides both a 2x16 LCD display and buttons, so that messages can be sent and received.

3. A 5V CAN connection board such as this MCP2515 model:

https://www.electronicshub.org/arduino-mcp2515-can-bus-tutorial/

## Software

The Long Message protocol is in the Arduino CBUS libraries from Duncan Greenwood which are on MERG-DEV. https://github.com/MERG-DEV

The following library components are needed for AVR boards (NANO, UNO, MEGA etc):

CBUS2515 CBUS CBUSLED CBUSswitch CBUSconfig and also ACAN2515

All are available from the Arduino IDE.

There is also a version CBUSSAM3X8E which supports an Arduino DUE.

The following libraries are also used:

1.  IoAbstraction https://github.com/davetcc/IoAbstraction available from the Arduino IDE

    This is used for the control of the buttons.
	
2.  TaskManagerIO https://github.com/davetcc/TaskManagerIO available from the Arduino IDE

    This is used for task management in the example.

3.  SimpleCollections https://github.com/davetcc/SimpleCollections available from the Arduino IDE

    This is a dependency of IoAbstraction.

4.  Streaming for Arduino Streaming input/output available from the Arduino IDE

5.  Bounce2, LiquidCrystal, SPI, Wire, EEPROM also available from the Arduino IDE

## Setting Up

This module is a CBUS FLiM only module and does not have the push button and yellow and green LEDs on other modules.

The module has to be configured for use with CBUS using the method described for CANmINnOUT here: https://github.com/MartinDaCosta53/CANmINnOUT

See the section Setup and Serial Monitor at the end of the README.

