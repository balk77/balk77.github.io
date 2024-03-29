---
layout: default
title: Button Configuration
nav_order: 50
---

# Button Configuration
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }
- TOC
{:toc}

Your Button Plus has zero to 3 bars below the display. The buttons on the display do not have leds. The Bar buttons do have leds on the front and wall side.

##  Numbering of buttons
When 3 bars are installed, buttons are numbered from 0 (top left, on display) to 1 (top right, on display) further down to 7 (bottom right). When less bars are installed, numbering starts at 2 (with two bars), 4 (with 1 bar) and 6 (without bars). See tables below. This manual further refers to `<buttonid>`.

| 3 bar button numbering | Left | Right|
|---|---|---|
|Display| 0 | 1|
|Bar 1| 2| 3|
|Bar 2| 4 | 5|
|Bar 3| 6 | 7|

|  2 bar button numbering | Left | Right|
|---|---|---|
|Display| 2| 3|
|Bar 1| 4 | 5|
|Bar 2| 6 | 7|

| 1 bar button numbering| Left | Right|
|---|---|---|
|Display| 4 | 5|
|Bar 1| 6 | 7|

| no bar button numbering| Left | Right|
|---|---|---|
|Display| 6 | 7|


## Button label
Each button on a bar has a label. This is the main text on the minidisplay on a bar. The label can be configured statically in the web interface or dynamically through MQTT. 

<img width="193" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/41a24827-3c9d-486e-bd4e-43a9175167d0">

### Example
{: .no_toc }
#### topic:
{: .no_toc }
`buttonplus/<device>/button/<buttonid>/label`
#### payload issued by your home automation system
{: .no_toc }
`Porch`

## Button toplabel
Each button on a bar has a toplabel. This is the label above the main text on the minidisplay on a bar. The toplabel can be configured statically in the web interface or dynamically through MQTT. 

### Example
{: .no_toc }
#### topic:
{: .no_toc }
`buttonplus/<device>/button/<buttonid>/toplabel`
#### payload issued by your home automation system
{: .no_toc }
`Lighting`

## Clicks
A button click can generate different events. Main event is `Click`, which is issued when the button is pressed (does not need to be released). Another event is issued when the button is released or long pressed. You can for instance let all three events issue a message on the same topic, but with different messages (payloads). This example issues a payload `press` on topic `buttonplus/<device>/button/<buttonid>/state`. The other two payloads would be `release` and `longpress`. You could also configure a `toggle` this way.

<img width="716" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/9de085f3-043d-4782-ac1b-91705958a54c">

## Preconfigured Leds
Three pre-configured eventtypes have been setup for red, blue and green. In this example the led will turn blue when the payload sent to the configured topic is equal to the topic configured, "on". This is case-sensitive. Any other payload will switch off the led.

<img width="716" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/7850a67e-fd66-4248-ad52-c295b43088ff">

## Led (subscribe)
The `Led (subscribe)` option lets you switch on and off the wall and front led. The leds will take the configured color when the payload sent to the configured topic is equal to the topic configured; "on" in this example will make the front led red and wall led green.

<img width="716" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/8f6f631c-05c9-427c-82b1-6d9eeab6bcd2">

## RGB Led (subscribe)
More control over the led color can be obtained with `RGB Led` option. The front and wall led will both switch to the color that is received as payload. Payload 0 will switch off the leds. You have to send the color as a decimal value, `65535` will give a light blueish color for both leds. You can select your color on for instance this site: [https://www.mathsisfun.com/hexadecimal-decimal-colors.html
](https://www.mathsisfun.com/hexadecimal-decimal-colors.html
)
<img width="716" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/18ef5988-49fa-4fb2-8719-d91dc80fb343">



### Section 2 level 2
`### Section 2 level 2`

content

