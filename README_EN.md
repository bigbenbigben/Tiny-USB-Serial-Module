# Tiny-USB-Serial-Module : Compact CP2102N USB-to-Serial Converter Module Compatible with UIAPduino

[日本語](README.md) | [English](README_EN.md)

## Overview

<div class="image-row">
    <img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_top.jpeg" width="240px">
    &nbsp;&nbsp;&nbsp;&nbsp;
    <img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_bottom.jpeg" width="210px">
</div>

This is a compact USB-to-serial converter board based on the Silicon Labs CP2102N, measuring only 20 mm × 12 mm.

It features a USB Type-C connector and operates via USB bus power. The TxD and RxD signals are available through through-hole terminals.

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_with_UIAPduino.jpeg" width="240px">

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_with_UIAPduino_description.jpeg" width="640px">

Do not connect Pin 1 (+5 V) of this product to the TX or RX pin of the UIAPduino.
Pin 1 can be connected to the 5 V pin of the UIAPduino using a jumper wire or similar connection to supply power to the UIAPduino.

The pin layout is compatible with the [UIAPduino Pro Micro CH32V003 V1.4](https://www.uiap.jp/uiapduino/pro-micro/ch32v003/v1dot4), allowing RXD, TXD, and GND to be connected directly using spring-loaded pin headers or a breadboard.

## Dimensions

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_size.jpeg" width="240px">

Board size: W20×D12
Height: 5 mm (measured)
Weight: 1.3g


## Features

* Compact design with a board size of 20 mm × 12 mm
* Uses the Silicon Labs CP2102N
* Built-in overcurrent protection
* Built-in ESD protection
* USB Type-C connector
* USB bus-powered operation
* 5 V-tolerant input
* Pin layout designed for direct connection to UIAPduino boards
* RoHS compliant

## Specifications

* Maximum supply voltage: 5 V
* Maximum I/O voltage: 3.3 V, with 5 V-tolerant input
* Minimum baud rate: 300 bps
* Maximum baud rate: 3 Mbps
* Receive buffer: 512 bytes
* Transmit buffer: 512 bytes
* Two LEDs:

  * Power: Blue
  * TxD: Orange

## Pinout

<img src="https://github.com/bigbenbigben/Tiny-USB-Serial-Module/blob/main/Tiny-USB-Serial-Module_pin.jpeg" width="240px">

* P1: +5 V (VBUS)
* P2: RXD
* P3: TXD
* P4: GND

## Supported Operating Systems

Drivers for the CP2102N used on this product are available for the following operating systems:

Windows, macOS, Linux, and Android

Driver download page: [Silicon Labs CP210x USB-to-UART Bridge VCP Drivers](https://www.silabs.com/software-and-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads)

Operation has been verified by the author on Windows 11 Pro 25H2.

## Notes

* RXD supports 5 V input, while TXD outputs 3.3 V logic levels. It can generally be used with standard 5 V microcontrollers, but it may not work with devices that strictly require a 5 V logic-high input.
* Pay attention to the TXD and RXD connections. For a typical UART connection, TXD and RXD must be cross-connected. Connect this module’s TXD to the RXD of the target device, and connect this module’s RXD to the TXD of the target device.
* As of July 12, 2026, `Serial.available()` does not appear to work on the UIAPduino. The author confirmed operation using the [UIAPSerial](https://github.com/tarosay/sdlog_uiapduino/tree/main/SDLog) library.


## Author

Positive Feedback
bigben ([@bigbenbigben](https://github.com/bigbenbigben))
