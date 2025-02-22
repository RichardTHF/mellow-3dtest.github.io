---
title: Fly-Super5 Pro Klipper firmware in USB to CAN Bridge
tags: []
keywords: 
last_updated: 05/04/2023
summary: "Fly-Super 5 Pro Klipper USB to CAN bridge mode"
sidebar: mydoc_sidebar
permalink: fly-super5_pro_klipper_usbtocan.html
folder: mydoc
comments: false
toc: true
datatable: true
boardname: "Fly-Super 5 Pro"
firmware: usbtocan
version: "V1.3"
micro: "STMicroelectronics STM32"
processor: "STM32H723"
offset: "128 KiB bootloader"
clock: "25 MHz crystal"
com: "USB to CAN Bridge on PA11/PA12"
appoffset: "128 KiB offset"
canspeed: "500000"
klipcom_img1: "fly-super5_pro/fly-super5_pro_klipper_menuconfig_usb_can_bridge.png"
klipcom_cap1: "Klipper Menu Config USB to CAN"
klipcom_img2: "fly-super8/fly-super8_klipper_makeflash_burn.png"
klipcom_cap2: "Burn Klipper firmware over USB"
klipcom_img3: "fly-super8/flash-can_query.png"
klipcom_cap3: "Flash Can Query"

---

## Configuring and installing Klipper for USB to CAN bridge mode

{% include custom/mcu/stm32/stm32_klipper_menuconfig.html %}

{% include custom/mcu/stm32/stm32_klipper_flash_canboot.html %}

{% include custom/can/sht_links.html %}