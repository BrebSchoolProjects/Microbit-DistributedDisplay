# Distributed Display with BBC Micro:Bit

Work based on https://github.com/DavidMS51/Microbit-Scroll-Display

## Introduction

Several microbit boards are connected over the radio interface to display text.
Text can be shown static or scrolled over the microbits.

## Technical Background

The project consists of 2 files:
* Node-Display.py: For microbits used as display
* Node-Gateway.py: For managing node

The managing node sends the text to the display node. The text is currently hardcoded but can be also changed over the uart interface
(currently disabled). Settings for the uart are: 115200 8N1 . Do not send a CR or LF with the data.

The display node receives characters from the managing node and show them on the LED display.

## Configuration

On first startup all of the nodes have to be configured. For the managing node the number of display nodes has to be configured.
The display nodes have to be assigned to an address.

The number/address is altered by pressing the A button. Pressing the B button will save the current value. (Configuration is stored in internal flash)
