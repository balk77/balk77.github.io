---
layout: default
title: Display Configuration
nav_order: 40
---

# Display Configuration
{: .no_toc }


## Table of contents
{: .no_toc .text-delta }
- TOC
{:toc}

The display can show information as individually configured items. The configuration options are described below. The examples below use `<uid>` which is a unique number, but can be for instance two digits. `<device>` is a unique name for your device, for instance `hall`, or `livingroom`. Buttonplus uses so called `eventtypes` internally; they point to a specific action of the Button plus. Eventtype 1 is for instance the click of a button.

## Value
The `Value` field has to be provided through an MQTT topic. It is aligned left in the display item. Leave the `MQTT Payload` field empty.
### Example
#### topic:
`buttonplus/<device>/display/<uid>/value`
#### payload issued by your home automation system
`19.21346`

## Label
The `Label` field can be configured statically in the web interface or dynamically through MQTT. Label is optional. Leave the `MQTT Payload` field empty.
### Example
#### topic:
`buttonplus/<device>/display/<uid>/label`
#### payload issued by your home automation system
`Room temperature`

## Unit
The `Unit` field can be configured statically in the web interface or dynamically through MQTT. Unit is optional. It is aligned right in the the display item. Leave the `MQTT Payload` field empty.
### Example
#### topic:
`buttonplus/<device>/display/<uid>/unit`
#### payload issued by your home automation system
`°C`

## Alignment
The anchor point of the display item on the display can be selected. Default is top left corner of the display with the top left corner of the display item. Choosing Center places the center of the display item at the center of the display. Static configuration in the Buttonplus WebUI.

`<inser picture>`

## x and y offset
Position of the display item' anchor point relative to the chosen Alignment anchor point. Scale is always 100 by 100. Choosing for instance a center alignment and an x offset of 50 will place the display item 50% outside the display, on the right side. Values of -100 through 100 are accepted. Static configuration in the Buttonplus WebUI, default is 0.

## Fontsize 
Fontsize; smallest size is 1, largest size is 5. Static configuration in the Buttonplus WebUI.

## Width
Width of the display item, 1 to 100, required field. Static configuration in the Buttonplus WebUI.

## Rounding
Number of digits to be shown for numeric values. Note that the Button Plus shows a dot as decimal separator. Static configuration in the Buttonplus WebUI.

## Section 1 level 1
`## Section 1 level 1`

content

## Section 2 level 1
`## Section 2 level 1`

content

### Section 2 level 2
`### Section 2 level 2`

content

