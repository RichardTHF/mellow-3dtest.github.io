---
title: Updating Klipper Firmware on a Fly-E3-v2 in CANbus mode
tags: []
keywords: 
last_updated: 15/07/2023
summary: "How to update the klipper firmware running on a Fly-E3-v2 in CANbus mode"
sidebar: mydoc_sidebar
permalink: fly_e3_v2_klipper_can_updating.html
folder: mydoc
comments: false
toc: true
datatable: true

boardname: Fly-E3-v2
firmware: can
ver: v2
processor: "STM32F407"
offset: "32 KiB bootloader"
clock: "8 MHz crystal"
micro: "STMicroelectronics STM32"
com: "CAN bus (on PB8/PB9)"
canspeed: "500000"

klipcom_img1: "fly-super8/fly-super8_klipper_menuconfig_can.png"
klipcom_cap1: "Klipper Menu Config CAN"

klipcom_img2: "fly-super8/fly-super8_klipper_canboot_burn.png"
klipcom_cap2: "Burn Klipper firmware over CAN bus"

klipcom_img3: "fly-super8/flash-can_query.png"
klipcom_cap3: "Flash Can Query"

kconfig_name: "e3v2"
---

## Updating Klipper for CANbus

{% include tip.html content="To read more about the KCONFIG_CONFIG option, see [here](https://docs.vorondesign.com/community/howto/drachenkatze/automating_klipper_mcu_updates.html)" %}

{% include custom/mcu/stm32f4/klipper_menuconfig_can_updating.html %}

{% include custom/mcu/stm32f4/klipper_flash_canboot_can_updating.html %}

{% include custom/mcu/e3v2/fly_e3_v2_links.html %}
