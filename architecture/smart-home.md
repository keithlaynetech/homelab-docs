# Smart Home Architecture

## Overview

The smart-home environment combines Apple HomeKit with Home Assistant and supporting integration services.

Apple Home provides the primary user-facing experience.

Home Assistant provides deeper automation logic and integration flexibility.

## Core Components

- Apple Home / HomeKit
- Home Assistant
- Homebridge
- Scrypted
- Zigbee2MQTT
- Mosquitto

## Connected Devices

- Lutron Caseta smart switches
- Aqara night lights
- Aqara and August door locks
- Ecobee thermostats
- Ubiquiti cameras
- Aqara lamps
- Garage doors
- Alarm/security system
- Water leak sensors
- Automated water shutoff valve
- Door/contact sensors
- Motorized window shades
- Air purifiers
- Apple TV and Apple devices

## Example Automations

- Good Night routine locks doors, closes garage doors, arms the alarm, turns off most lights, and turns on hallway night lights.
- Water leak detection generates alerts and closes the automated water shutoff valve.
- Freezer left open more than five minutes causes house lights to cycle as a visible alert.
- Bedroom door activity after 11 PM triggers green lamp alerts in the parents' bedroom.
- Package activity at the front door can generate an audible in-house notification.
- Camera motion can generate notifications and video clips on phones and Apple TV.
- Shades and air purifiers are scheduled.
