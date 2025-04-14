---
title: Device Client Demo Docs
parent: MQTT
layout: default
nav_order: 2
---

# HID MQTT Device Client – Demo Documentation

## Overview

This document provides instructions for the [**HID MQTT Device Client**](https://rms.magensa.net/TEST/demo/mmsmqttdevice.html), a web-based tool designed to establish an MQTT connection with a locally connected MagTek Dyna Family device via USB HID. It facilitates communication between your device and an MQTT broker.

## Prerequisites

- A MagTek Dyna Family device via USB HID.
- A compatible desktop Chromium-based web browser (e.g., Google Chrome, Microsoft Edge, etc.).
- Ensure that no other applications are accessing the MagTek Dyna Family device.

## Establishing a Connection

1. **Access the Application**:  
   Navigate to [https://rms.magensa.net/TEST/demo/mmsmqttdevice.html](https://rms.magensa.net/TEST/demo/mmsmqttdevice.html).

2. **Connect Your Device**:  
   Ensure your MagTek Dyna Family device is securely connected to your computer via USB.

3. **Initiate Connection**:  
   Click the **"Open"** button on the webpage to establish a connection between the application and your MagTek Dyna Family device.

   - Once connected, the status indicator will display **"Connected"**.

4. **Maintain the Connection**:  
   - **Do not close** this browser tab or window; the connection will terminate if the page is closed.
   - **Avoid opening** this application in multiple tabs or windows simultaneously.
   - You may **minimize** the browser window; the connection will remain active as long as the page is open.

## Disconnecting the Device

- To terminate the connection, click the **"Close"** button on the webpage.

   - The status indicator will change to **"Disconnected"**, confirming the disconnection.

## Additional Features

- **Friendly Name**:  
  You can assign a custom name to your connected device for easier identification.

   1. Enter your desired name in the **"Friendly Name"** field.
   2. Click the **"Save"** button to apply the name.

---