---
title: Fly TMC5160 Stepstick
tags: []
keywords: 
last_updated: 20/10/2022
summary: "General information regarding the Fly TMC5160"
sidebar: mydoc_sidebar
permalink: fly_tmc5160_general.html
folder: mydoc
comments: false
toc: true
datatable: true

driver_img1: "fly-5160/fly-5160_general.webp"
driver_cap1: "Fly-TMC5160 Overview"

driver_img2: "fly-5160/fly-5160_dimensions.webp"
driver_cap2: "Fly-TMC5160 Dimensions"

driver_img3: "fly-5160/fly-5160_pins.webp"
driver_cap3: "Fly-TMC5160 pin map"

driver_img4: "fly-5160/fly-5160_bom.webp"
driver_cap4: "Fly-TMC5160 BOM"



---

    {% capture driver_img1 %}{{page.driver_img1 }}{% endcapture %}
    {% capture driver_cap1 %}{{page.driver_cap1 }}{% endcapture %}
    {% capture driver_url1 %} .\images\{{ page.driver_img1 }} {% endcapture %}

    {% capture driver_img2 %}{{page.driver_img2 }}{% endcapture %}
    {% capture driver_cap2 %}{{page.driver_cap2 }}{% endcapture %}
    {% capture driver_url2 %} .\images\{{ page.driver_img2 }} {% endcapture %}

    {% capture driver_img3 %}{{page.driver_img3 }}{% endcapture %}
    {% capture driver_cap3 %}{{page.driver_cap3 }}{% endcapture %}
    {% capture driver_url3 %} .\images\{{ page.driver_img3 }} {% endcapture %}

    {% capture driver_img4 %}{{page.driver_img4 }}{% endcapture %}
    {% capture driver_cap4 %}{{page.driver_cap4 }}{% endcapture %}
    {% capture driver_url4 %} .\images\{{ page.driver_img4 }} {% endcapture %}

    {% capture driver_img5 %}{{page.driver_img5 }}{% endcapture %}
    {% capture driver_cap5 %}{{page.driver_cap5 }}{% endcapture %}
    {% capture driver_url5 %} .\images\{{ page.driver_img5 }} {% endcapture %}

## Overview 

  {% 
  include image.html 
  file=driver_img1
  url=driver_url1
  alt=driver_cap1
  caption=driver_cap1
  %}

### Fly TMC5160 Driver

This is the 12-24v operating voltage version TMC5160. Because of the lack of components, the high-voltage version cannot be made at this time, but this version is sufficient for normal use. If you need 5160, this is a good choice.

 - 12-24v Operating Voltage
 - 4.4A max Current
 - Step/direction interface with microstep interpolation microPlyer
 - The highest resolution is 256 microsteps
 - StealthChop2 silent work and smooth motion
 - Resonance suppression for mid-range resonance
 - SpreadCycle high dynamic motor control chopper
 - DcStep load related speed control
 - StallGuard2 high-precision sensorless motor load detection
 - CoolStep current control, which can achieve up to 75% energy savings

### Dimensions

  {% 
  include image.html 
  file=driver_img2
  url=driver_url2
  alt=driver_cap2
  caption=driver_cap2
  %}

### Circuit Diagram
  {% 
  include image.html 
  file=driver_img3
  url=driver_url3
  alt=driver_cap3
  caption=driver_cap3
  %}

### BOM
  {% 
  include image.html 
  file=driver_img4
  url=driver_url4
  alt=driver_cap4
  caption=driver_cap4
  %}
