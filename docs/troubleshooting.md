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
Your Button Plus is restarting all the time.

### Cause: Power supply
* Using a USB adapter: 
  > Try some different power supply's with at least 1A at 5V.

  > Try a different USB-C cable.

  > Try to connect the 3.3v wires to a 3.3v power supply.
* Using the 3.3v power cord:
  > Make sure that the power supply can supply at least 1A

  > Try another power supply.

  > In case of long or thin wiring please check the [section below](#cause-long-or-thin-cabling) 

### Cause: Long or thin cabling.

* Long and/or thin wiring will cause a voltage drop over the wire
  > Put the power supply in the box behind the button plus. If the wiring does not meet the requirements for 230V,
  > consider adding a 12v (or bigger) power supply and add a module with for example an LM2596 DC-DC drop down converter behind your button plus.
  
  > Increase the voltage a bit but do not go over 3.6v! (see chapter 4.2 of the [ESP32-S3 datasheet](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf))
  
  > Add a capacitor behind your button plus. I suggest a capacitor of at least 1000µF and parallel 100nF. This will act as a little buffer 
  > for the initial current and decouple some noise.
  >

## Loading the "factory default" settings
If your Button+ experiences problems, you can reset it to "factory default". **This will not reset the WIFI credentials, these are stored in a different part of the flash memory.**

![reset-small](https://github.com/balk77/balk77.github.io/assets/10166350/d6b4d574-9c1e-4796-a998-eda07cce40e6)
*Position of CONFIG and RESET buttons*

To (re)set to Factory Default:
* keep CONFIG pressed
* press and release RESET button
* for firmware version 1.081 and lower: wait little moment (one or two seconds is enough) and release CONFIG button
* for firmare version 1.1 and higher: after the RESET button is released, firmware is restarted and factory default settings will be confirmed by one red flash of LED's.

Your Button+ should now be back to factory default settings. If WIFI credentials were set, you should see time at Amsterdam time zone. If no WIFI crendentials were set, the Button+ is in AP (Access Point) mode, waiting for a connection.
This procedure will remove all configurations from the Button+. It will not affect the firmware it self. So if you are on version 1.11. you will still be on 1.11 after this procedure. To switch to an other firmware, please use the USB port for flashing firmware of you choice.
