---
title: MQTT MMS Docs
parent: MMS
layout: default
nav_order:
---

# MagTek MQTT MMS Demo Documentation

This document provides instructions for using the MagTek [**MQTT MMS Demo**](https://rms.magensa.net/TEST/demo/mmsMQTTDemo.html) page to interact with your MagTek device using **MQTT** for remote messaging and management.

The page serves as the MQTT MMS Demo interface for MagTek devices. It allows users to interact with any properly configured **MQTT-enabled DynaFlex II PED** device through features like opening and closing connections, clearing logs, sending specific commands, and configuring auto-start options for **EMV**, **NFC**, **MSR**, and **Touch**. A dropdown menu provides a list of predefined commands for testing and operations.

---

## Getting Started

Access the MQTT MMS Demo page using a compatible web browser with **JavaScript enabled**.

---

## Device Connection

- **Open Button**: Initiates connection to your MagTek device.
- **Close Button**: Disconnects your MagTek device.
- **Clear Button**: Clears displayed log data.
- **USB Status**: Shows current USB connection status (Connected/Disconnected).

---

## Log Data

- **Log Text Area**: Provides real-time log information about device interactions and command results.

---

## Auto Start Options

Enable automated transaction types:

- **Auto Start**: Automatically initiates configured operations.
- **EMV**: Enables EMV (chip card) transactions.
- **NFC**: Enables contactless (NFC) transactions.
- **MSR**: Enables Magnetic Stripe Reader transactions.

---

## Sending Commands

- **Command Data Field**: Input custom command data directly.
- **Send Command Button**: Sends the entered command to the connected device.

---

## Predefined Commands

Select and execute commands quickly using the dropdown list:

- `START EMV`, `CANCEL EMV`: Manage EMV transactions.
- `Reset Device`: Resets the device settings.
- `Get User Notify`, `Set User Notify`: Configures event notifications.
- `START CONTACT`, `START CONTACTLESS`, `START MSR`: Initiates specific transaction modes.
- `Get SN`, `Get Capabilities`: Retrieves device details.
- `NFC`, `NFC Mifare`: Manages NFC transactions.
- `Display Amount`, `Approved`, `Welcome`: Controls device display messages.
- `Request PIN`: Initiates PIN entry.
- `PIN Entry Success/Fail`: Confirms or denies PIN validation.

---

## File Input

- **File Input Button**: Use this button to upload files (e.g., firmware updates) to the device.

---

## Troubleshooting

- Confirm USB connection if experiencing issues.
- Validate that the MQTT server settings are correctly configured.
- Use **Log Data** for error diagnostics.
