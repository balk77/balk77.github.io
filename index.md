---
title: Button Plus Documentation
layout: home
nav_order: 1
---

# Introduction
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }
- TOC
{:toc}

The Button Plus is a device with a display and with buttons, all configurable.

## Prerequisites
The Button Plus communicates through MQTT. It needs an MQTT back-end and a hast most value when combined with a Home Automation system. The requirements are:
* An MQTT broker
* A Home Automation system
* Some technical know-how helps

## Home Automation
The Button Plus interacts with your Home Automation system through MQTT. It can show information present in your Home Automation system on the display and buttons, and it can send button clicks to your Home Automation system. There are various Home Automation solutions available; some are used in combination with others. Some examples are:

* [Home Assistant](https://www.home-assistant.io/), open source system that also records the historical state of your sensors and equipment
* [Domoticz](https://www.domoticz.com/), open source system that also records the historical state of your sensors and equipment
* [Homey](https://homey.app/), closed source hardware platform for home automation that also records the historical state of your sensors and equipment
* [IO Broker](https://www.iobroker.net/), open source system
* [Node Red](https://nodered.org/), open source low code visual flow based automation. Can be used in combination with the above solutions.

## about MQTT
MQTT is a kind of X (fka Twitter) for your IoT devices. Some devices publish their information to the platform and others subscribe to a channel (topic). The MQTT server (broker) can run on your home server or externally. For instance, a temperature sensor can regularly publish a measured value to `homesensors/livingroom/temperaturesensor1/temperature` and also listen to a topic  `homesensors/livingroom/temperaturesensor1/forceupdate` to force an update of the sensor. Your home automation system can subscribe to the measured value, and send commands. A popular MQTT broker is [Mosquitto](https://mosquitto.org/) but there are others as well.
Buttonplus also connects to the broker. When your home automation system publishes a new value, the Button Plus shows it. When you press a button, it gets published to the broker and your home automation system responds to it.

Throughout this documentation we assume a MQTT structure. You are free to choose yours.

level | topic level | Description | Example
 --- | --- | --- | ---
 1 | `<basetopic>` | Base topic for the Button Plus | `buttonplus/`
 2 |`<device>`| Device name| `hall/`
 3a |`display/`| Topics for the display| 
  3b |`button/`| Topics for the buttons | 
   4 |`<uid>`| Identifier for the item| `3/`

 

 

 
