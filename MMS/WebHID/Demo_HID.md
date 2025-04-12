---
title: WebHID MMS Docs
layout: default
parent: Web HID
nav_order: 2
---

# MMS WebHID Demo

MagTek [**HID MMS Demo**](https://rms.magensa.net/TEST/demo/mmsdemo.html) User Guide

Interact with MagTek HID devices: send commands, test operations, and manage features.

### Getting Started

Open the HID MMS Demo in a **Chromium browser** with the device connected via USB.

### Device Connection

- **Open / Close / Clear** – Manage USB connection and logs  
- **USB Status** – Shows connection state

### Log and Status Display

- **Device Display / Image Data / Log Area** – Visual and text feedback

### Auto Start Options

Enable automatic startup for:
- EMV
- NFC
- MSR
- Touch (hidden by default)

### Sending Commands

- Enter command manually or use **Command List Dropdown**  
- Examples: `Start EMV`, `Reset Device`, `Display Commands`, `Request PIN`, etc.

### Firmware Update

- **Update Firmware RMS** – Initiates update from RMS

### File Upload

- Upload firmware or certificates using **File Input**

### Progress Bar

- Shows progress for operations

### Troubleshooting

- Confirm USB is connected  
- Validate commands  
- Review logs for errors

---

## MagTek MQTT MMS Demo User Guide

Use MQTT to remotely manage and test MagTek DynaFlex II PED devices.

### Getting Started

Open the MQTT MMS Demo page in a **JavaScript-enabled browser**.

### Device Connection

- **Open / Close / Clear Buttons**  
- **USB Status** – Displays connection state

### Log Data

- Monitor device communication via log area

### Auto Start Options

Configure for:
- EMV  
- NFC  
- MSR

### Sending Commands

- Enter custom command or choose from predefined options  
- Use **Send Command** to execute

### Predefined Commands

Examples include:
- `START EMV`, `CANCEL EMV`  
- `Get SN`, `Get Capabilities`  
- `START CONTACT`, `START MSR`  
- `Display Amount`, `Request PIN`, `PIN Entry Success/Fail`

### File Input

- Upload firmware or configuration files

### Troubleshooting

- Confirm USB and MQTT connectivity  
- Verify server settings  
- Use logs for diagnostics