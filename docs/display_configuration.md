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

The display can show information as individually configured items. The configuration options are described below.

## Value
The `Value` field has to be provided through an MQTT topic. It is aligned left in the display item.

## Label
The `Label` field can be configured statically in the web interface or dynamically through MQTT. Label is optional.

## Unit
The `Unit` field can be configured statically in the web interface or dynamically through MQTT. Unit is optional. It is aligned right in the the display item.

## Alignment
The anchor point of the display item on the display can be selected. Default is top left corner of the display with the top left corner of the display item. Choosing Center places the center of the display item at the center of the display.

## x and y offset
Position of the display item' anchor point relative to the chosen Alignment anchor point. Scale is always 100 by 100. Choosing for instance a center alignment and an x offset of 50 will place the display item 50% outside the display, on the right side. Values of -100 through 100 are accepted.

## Section 1 level 1
`## Section 1 level 1`

content

## Section 2 level 1
`## Section 2 level 1`

content

### Section 2 level 2
`### Section 2 level 2`

content

