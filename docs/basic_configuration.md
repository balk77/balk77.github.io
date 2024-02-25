---
title: Basic Configuration
layout: default
nav_order: 30
---

# Basic Configuration
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }
- TOC
{:toc}

## Initial WiFi connection
Connecting your Button+ to a Wifi network is very easy. It takes only 5 logical steps: 
1. Make sure that the Button+ is in Access Point (AP) mode
2. Connect your phone to this Access Point
3. Configure the WiFi network

### Access Point mode
Your new Button+ will show that it is not connected:

![](pictures/PXL_20240216_094727167~2-small.jpg)

### Connect your phone
Open the wifi access point selection screen on your phone, similar to how you would connect to a public hotspot. On an android phone, you can swipe from the top of your screen down. If you use IoS on an Apple iPhone or a different flavour of Androud, it looks different.

The screenshots in these steps are for a version of Android, but are similar to the screens on other operating systems.

<img width="327" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/35956063-e024-4fc1-b4d4-ee89fa13c8a9">

In the list of available access points (Wifi networks) you will see the ‘Button+ AP’. If not, make sure your Button+ is still powered on and the initial message is visible. Select the Wi-Fi network ‘Button+ AP’. Depending on your brand/type of mobile phone, either a pop-up message will be displayed or a web browser will open. When you are sure you are connected but you don't see the WiFi selection screen, go to (http://172.217.28.1/_ac/config).

### Configure the Button+
A web page that will be opened, displays some technical information. In the upper right corner, you will see a hamburger menu-button. (See below.) Click on it.

<img width="206" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/f906fa05-bf07-43df-8718-a35249e970b7">

Select the option ‘Configure new AP’:

<img width="335" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/9d0152fc-5e09-477b-a6b1-595fb8821384">

A list of all available wifi- networks will be displayed. Select your network.

<img width="196" alt="image" src="https://github.com/balk77/balk77.github.io/assets/10166350/5860d944-e287-4b1b-b60f-01d6c7301a80">

The field ‘SSID’ will be filled with the name of the selected network. Enther the Wi-Fi passphrase in the field below it. If you want to assign a fixed IP-address or configure other network parameters, uncheck the ‘Enable DHCP’ box. More fields will be listed. Configuring those parameters is beyond the scope of this document. Click on ‘Apply’. The Button+ will restart and show its IP on the display. You can now start with the fun part: configure the Button+!

In case your phone does not reconnect to your home network, you will have to do that manually. The Button+ will give a warning when something went wrong; you can restart the WiFi procedure.

