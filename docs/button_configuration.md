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
When 3 bars are installed, buttons are numbered from 0 (top left, on display) to 1 (top right, on display) further down to 7 (bottom right). When less bars are installed, numbering starts at 2 (with two bars), 4 (with 1 bar) and 6 (without bars). See tables below.

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
#### topic:
`buttonplus/<device>/display/<uid>/value`
#### payload issued by your home automation system
`19.21346`

### Section 2 level 2
`### Section 2 level 2`

content

