# Environment sensor board

Copyright (c) 2023 [Antmicro](https://www.antmicro.com)

![Visualization](img/environment-sensor-vis.png)

## Overview

This project contains open hardware design files for an environment sensor board with temperature, pressure and humidity sensors.
These sensors are placed on a separated island in the PCB corner, which can be easily broken out from the main board and connected to it via provided connectors with a cable.
The design files were prepared in KiCad 6.x.

## Key features

* 50.00 mm X 26.50 mm PCB size
* USB-C Connector for data and power
* STM32G474CET6 host MCU
* 128kB external FeRAM 
* FTDI FT4232H USB - JTAG/I2C/UART converter
* SHT45 temperature + humidity sensor:

	* Typ. relative humidity accuracy ±1% RH
	* Operating relative humidity range 0 - 100% RH
	* Typ. temperature accuracy ±0.1 °C
	* Operating temperature range (-40) - (+125) °C
	
* BME280 temperature + humidity + pressure sensor:
	* Typ. relative humidity accuracy ±3% RH
	* Operating relative humidity range 10 - 100% RH
	* Typ. temperature accuracy ±1 °C
	* Operating temperature range (-40) - (+85) °C
	* Typ. pressure accuracy ±1 hPa
	* Operating pressure range 300 - 1100 hPa
	
* I2C connectors
* RTC battery backup

## I2C Address map (7-bit)
* FeRAM: 0x50 + A16 (optional)
* SHT45: 0x44
* BME280: 0x76

## Project structure

The main directory contains KiCad PCB project files, a LICENSE, and a README.
The remaining files are stored in the following directories:

* `img` - contains graphics for this README
* `assets` - contains visual assets for showcasing this design on [Open Hardware Portal](https://openhardware.antmicro.com)

## Licensing

This project is published under the [Apache-2.0](LICENSE) license.
