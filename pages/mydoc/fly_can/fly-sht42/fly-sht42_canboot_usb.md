---

title: Configuring the Mellow SHT-42 CAN bus tool boards for Klipper on USB
tags: [content_types]
keywords: 
last_updated: 20/10/2022
summary: "CanBoot Configuration for the Fly SHT-42 on USB"
sidebar: mydoc_sidebar
permalink: fly-sht42_canboot_usb.html
folder: mydoc
comments: false
toc: true
datatable: true
boardname: sht42
firmware: usb
version: v1

mcu: "SHT-42"

mcufile: "SHT-42"
com: "USB on PA11/PA12"

cancom_img1: "fly-sht36-42/sht_36_42_canbus_fw_usb_config.png"
cancom_cap1: "CanBoot Menu Config USB - update this image"

canburn_img1:  "fly-sht36-42/sht_42_dfu_jumper.png"
canburn_cap1:  "DFU jumper location" 

canburn_img2:  "fly-sht36-42/sht_42_dfu_jumper_image.png"
canburn_cap2:  "DFU jumper location"

canburn_img3: "fly-sht36-42/sht-36_42_lsusb_screenshot.png"
canburn_cap3: "lsusb Results"

canburn_img4: "fly-sht36-42/sht_36_42_canbus_usb_flash.png"
canburn_cap4: "CanBoot burn complete"

klipcom_img1: "fly-sht36-42/sht_36_42_klipper_fw_usb_config.png"
klipcom_cap1: "Klipper Menu Config USB - update this image"

klipcom_img2: "fly-sht36-42/sht_36_42_klipper_usb_flash.png"
klipcom_cap2: "Klipper USB burn complete"

klipcom_img3: "fly-sht36-42/sht_36_42_klipper_can_flash.png"
klipcom_cap3: "Klipper verify CAN bus UUID"

klipcom_img4: "fly-sht36-42/sht_36_42_klipper_can_flash.png"
klipcom_cap4: "Klipper CAN bus burn complete"


---

{% include important.html content="This guide assumes you have a working Klipper host installation on a Raspberry Pi or compatible device" %}



## Setup steps

### Toolboard firmware

{% include custom/can/sht_canboot_compile.html %}

{% include custom/can/sht_canboot_burn.html %}

{% include custom/can/sht_links.html %}

