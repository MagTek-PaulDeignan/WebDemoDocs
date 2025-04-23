---
title: MQTT Magensa Local Start Demo
layout: default
parent: Magensa
nav_order: 3
---

# MagTek MQTT Magensa Local Start Demo – User Instructions

## Overview

This [MQTT Magensa Local Start Demo](https://rms.magensa.net/TEST/demo/mmsUnigateLocalStart.html) enables users to initiate and process MPPG transactions using the **Local Start** mode on a MagTek **DynaFlex II PED**. The device must be configured to use native MQTT messaging or connected via the Web HID MQTT Client. The interface displays real-time communication logs, shows device connection status, and provides controls for configuring the PED's transaction behavior.

> **Note:** The DynaFlex II PED must be configured for **Mode 1B (Local Start)**, where transactions begin from the PED’s screen instead of a POS application.

---

## Prerequisites

Before starting, ensure the following:

- A compatible MagTek device (DynaFlex II PED) configured for MQTT or connected via Web HID.
- USB-C cable for device power and communication (if using Web HID).
- Chromium-based browser (e.g., Chrome or Edge) for Web HID functionality.
- Internet connectivity to load demo assets.
- Web HID permissions granted to access USB-connected devices (browser will prompt).

---

## Interface Elements

### 1. **Device Display Area**
- **Location:** Beneath the page heading.
- **Purpose:** Displays the current UI status or messaging from the PED.

### 2. **Log Data Output**
- **Element ID:** `LogData`
- **Purpose:** Shows real-time logs of communication and transaction feedback.
- **Use:** Monitor device activity, configuration commands, and processor responses.

### 3. **Connection Status**
- **Icon Indicator:** Displays either connected or disconnected status.
- **Label Text:** Updates dynamically to “Connected” or “Disconnected” based on the current state.

---

## Configure Transaction Modes

Use the buttons to configure how the PED starts a transaction:

### 🟦 `Configure Local Start`
- Sets the device to initiate transactions from its touchscreen UI.
- No POS interaction is needed to start a sale.
- Required for this demo to function properly.

### 🟦 `Configure Standard Start`
- Returns the device to host-initiated (POS-driven) transaction mode.
- **Note:** This demo does not support Standard Start for live transactions.

---

## Navigation Links

### 🔗 `Configure Unigate`
- Opens the `configure_mppg.html` page.
- Used to configure Unigate processor settings such as endpoints, tokens, and credentials.

---

## Usage Instructions

1. **Connect Your Device**
   - Plug in the DynaFlex II PED using a USB-C cable if using Web HID.
   - If using MQTT directly, ensure the device is powered (USB or battery).
   - If prompted, allow your browser to access the device via USB.

2. **Open Connection**
   - If using Web HID, click **Open** to establish the device connection.
   - Confirm the status icon changes to **Connected**.

3. **Configure Device Mode**
   - Click `Configure Local Start` to prepare the device for PED-initiated transactions.
   - Optionally click `Configure Standard Start` to return to POS-initiated mode after testing.

4. **Initiate a Transaction from the PED**
   - On the DynaFlex II PED touchscreen:
     - Tap **Start Sale**.
     - Enter the **Sale Amount**.
     - Enter a **Tip Amount or Percentage** (configured for percentage by default).
     - Optionally enter a **Tax Percentage**.
     - Press **Submit** to begin the payment process.
     - Present a payment card or mobile wallet when prompted.

5. **View Results**
   - Use the **LogData** output area to view real-time feedback from the transaction process, including processor response and ARQC.

6. **Clear or Close**
   - Click **Clear** to reset the log area.
   - Click **Close** to disconnect the device when finished.

---

## Notes & Tips

- Tip and tax configurations are defaulted to percentages but can be modified in your device’s configuration profile.  Please contact PGD for support.
- Make sure your Unigate configuration is set correctly prior to attempting transactions.
- The demo uses the active processor profile stored in the web page.

---

## Support

If you encounter issues or need additional help, contact **MagTek Support**:

📞 [https://www.magtek.com/support](https://www.magtek.com/support)