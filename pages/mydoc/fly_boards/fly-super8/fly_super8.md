---
title: Fly-Super8 General Information
tags: []
keywords: 
last_updated: 16/07/2023
summary: "General information for the Fly-Super8 Versions 1, 1.1, 1.2 and 1.3"
sidebar: mydoc_sidebar
permalink: fly_super8.html
folder: mydoc
comments: false
toc: true
datatable: true

boardname: "Fly-Super8" 
ver: "V 1.2" 
processor: "STM32F407"

super8_img1: "fly-super8/fly-super8_front_back.png"
super8_cap1: "Super 8 Front and Back"
---


       {% capture boardname %}{{ page.boardname }}{% endcapture %}
        {% capture ver %}{{ page.ver }}{% endcapture %}
    {% capture super8_img1 %}{{page.super8_img1 }}{% endcapture %}
    {% capture super8_cap1 %}{{page.super8_cap1 }}{% endcapture %}
    {% capture super8_url1 %} .\images\{{ page.super8_img1 }} {% endcapture %}


## Overview

{% 
include image.html 
file=super8_img1
url=super8_url1
alt=super8_cap1
caption=super8_cap1
%}

This page covers any general information for the Fly-Super8 boards.  
It is currently available through [AliExpress](https://s.click.aliexpress.com/e/_DFg3ED3).

- 32-bit ARM Cortex-M4 series 168 MHz, STM32F407ZGT6 chip
- Supported Firmware: Marlin 2.0, Reprap, and Klipper
- Drivers supported: A4988, LV8729, DRV8225, TMC2208, 2209,5160, & 5160HV.
- Drive mode support: TMC: UART, & SPI
- Support for 8 independent motor drives, 5 extruders, and 10 PWM fans
- All drivers sockets support up to 48 volts (except the v1 which only had 3 x 48 volt ports). 
- Supported Displays: serial touch screen, 12864 LCD, 2004 LCD , FLY 4.3, & 7.0 V1
- Supports automatic bed leveling sensor: BLTouch
- Optional limit switch power supply: 5V, 12V, & 24V
- On-board WiFi supported with Reprap firmware.
- PWM Fan MOS boards can be directly replaced in case of damage.

### Board Fuses

The board is supplied without the fuses installed.  
It is supplied with different fuses than the listing on AliExpress. The fuses should be installed as shown below.  

{% include image.html file="fly-super8\fly_super8_fuses.png" alt="Fly-Super8 Fuses" caption="Fly-Super8 Fuses" %}

### Driver Jumpers

The jumpers should be installed as below. "Common Interpolation" should be used for standalone drivers. "SPI mode Interpolation" is supported for TMC5160 drivers. "UART mode Interpolation" should be used when using smart drivers (i.e. TMC2208, TMC2209, TMC2225 and TMC2226)

{% 
include image.html 
file="fly-super8\fly-super8_driver_jumpers.png" 
alt="Fly-Super 8 Driver Jumpers" 
caption="Fly-Super 8 Driver Jumper Locations" 
%}

### Driver Diag Pin

The driver diag pin is used for sensorless homing and stall detection.  
The {{boardname}} **does not** have a way of disabling the diag pin as it is designed to be used with [Fly-2209 drivers](https://s.click.aliexpress.com/e/_DEuELVP) which have a switch on the underside of them for disabling the diag pin.  Set the dip switch to 'ON' to enable the diag pin. 
If you plan on using endstops rather than sensorless homing and do not have the Fly-2209 drivers, you need to bend or remove the diag pin. 

### Fan Mosfets

The {{boardname}} features 5 replacable fan mosfet modules (VS3622e) that control 10 fan outputs.

If the MOSFET is damaged by an accidental short circuit it can easily be replaced. 
New Fly-MOS modules can be purchased from [AliExpress](https://s.click.aliexpress.com/e/_DeyVmCN)

The Fan-MOS design allows it to be inserted in either orientation. 

{% 
include image.html 
file="fly-super8\fly-super8_fan_mos.png" 
alt="Fly-Super 8 Fan Mosfet" 
caption="Fly-Super 8 Fan Mosfet" 
%}

### Fan Voltage

The fan voltage can be set using jumpers to either 5v, 12v and Vin.  
Set them as shown below.  

{% 
include image.html 
file="fly-super8\fly-super8_fan_voltage.png" 
alt="Fly-Super 8 Fan Voltage" 
caption="Fly-Super 8 Fan Voltage"
%}

### IO Output Voltage

The IO output voltage can be set to either 3.3v, 5v or 12v. The default is 5v. 
Set them as shown below.  

{% include image.html file="fly-super8\fly_super8_io_voltage.png" alt="Fly-Super8 IO Voltage" caption="Fly-Super8 IO Voltage" %}

### Maximum Input voltage

#### Board/Bed Power

The main board and heated bed power inputs can handle voltage up to 30v.

#### Driver Power

{{boardname}} versions 1.1, 1.2 and 1.3, both of the driver power inputs 0-2 and 3-7 can handle voltage up to 62v.

{{boardname}} version 1.0 allows for up to 62 volts on the power input for Drivers 0,1 and 2. Drivers 3-7 allow up to 24 volts. 

{% 
include image.html 
file="fly-super8\fly-super8_drive_power.png" 
alt="Fly-Super 8 Driver Voltage" 
caption="Fly-Super 8 Driver Voltage"
%}


{% include warning.html content="In industry, 30 volts is generally considered to be a conservative threshold value for dangerous voltage. The cautious person should regard any voltage above 30 volts as threatening, not relying on normal body resistance for protection against shock." %}

### Thermistor Connection  

Thermistors should use the ADC inputs. The thermistors should be connected between ground and the signal pin.  

{% include custom/mcu/super8/fly_super8_links.html %}