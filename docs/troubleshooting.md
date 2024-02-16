---
layout: default
title: Troubleshooting
nav_order: 60
---

# Troubleshooting
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }
- TOC
{:toc}

## Issue: Boot loop
Your Button plus is restarting all the time.

### Cause: Powersupply
* Using a USB adapter: 
  > Try a different power supply's with at least 1A at 5V.

  > Try a different USB-C cable.

  > Try to connect the 3.3v wires to a 3.3v power supply.
* Using the 3.3v power cord:
  > Make sure that the power supply can supply at least 1A

  > Try another power supply.

  > In case of long or thin wiring pleas check the [section below](#cause-long-or-thin-cabling) 

### Cause: Long or thin cabling.

* Long and/or thin wiring, will cause a voltage drop over the wire
  > Put the power supply in the box behind the button plus. If the wiring do not meet the requirements for 230v,
  > consider adding a 12v (or bigger) power supply and add a LM2596 DC-DC drop down converter behind your button plus.
  
  > Increase the voltage a bit but do not go over 3.6v! (see chapter 4.2 of the [ESP32-S3 datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf))
  
  > Add a capacitor behind your button plus. I suggest a capacitor of at least 470µF. This will act as a little buffer 
  > for the initial current.