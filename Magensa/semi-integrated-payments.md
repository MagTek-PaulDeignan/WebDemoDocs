---
title: Semi-Integrated Payments
layout: default
parent: Magensa
nav_order: 2
---

# MQTT and Semi-Integrated Payment Model

**MQTT (Message Queuing Telemetry Transport)** is a lightweight messaging protocol optimized for devices with limited bandwidth, low power, and high latency environments. It operates on a **publish/subscribe** model, where a **MagTek payment device publishes data to a topic**, and other computing devices (e.g., mobile phones and tablets) subscribed to that topic receive the data. This ensures efficient data transfer with minimal overhead, making it ideal for IoT and real-time communication.

## Benefits of Using MQTT with Magensa and MPPG

Using MQTT, Magensa and MPPG can implement a **semi-integrated payment model**. Here’s how MQTT enhances this process:

### • Real-Time Communication
MQTT enables instant data exchange between the MagTek payment device and Magensa, ensuring:
- Secure transmission of sensitive card data and authorization responses
- Faster response times back to the POS system
- Improved transaction speed and user experience

### • Secure Data Transmission
- The MagTek device encrypts card data before transmission.
- MQTT supports **TLS/SSL**, securing data in transit.
- Communication between the MagTek device, Magensa, and the POS complies with **PCI-DSS** standards.

### • Lightweight and Efficient
- MQTT’s publish/subscribe model reduces the need for polling.
- Decreases network overhead, especially useful during peak transaction times.
- Handles large volumes of transactions without straining the system.

### • Integration Flexibility
- MQTT can seamlessly integrate with existing systems and protocols.
- Facilitates safe relay of non-sensitive data such as:
  - Authorization codes
  - Transaction tokens
  - Truncated card numbers

> This ensures that **no sensitive cardholder data** is exposed to the POS system.

---

## Demonstrating MQTT with the Magensa MMS Demo

You can test this semi-integrated model using the **MQTT MMS Demo**:

🔗 **Demo URL:** [MQTT MMS Demo](https://rms.magensa.net/TEST/HID/mmsMPPGDemo.html)  
🔧 **Configure Production Credentials:** [Configure MPPG](https://rms.magensa.net/TEST/HID/configure_mppg.html)

### **Instructions:**

#### **Demo Requirements**
- Use a PC, Mac, or Linux computer with a Chromium-based browser (e.g., Chrome or Edge).

---

### **Step 1: Configure MagTek Device for MQTT**
- Go to: [HID MQTT Device Client](https://rms.magensa.net/TEST/HID/mmsmqttdevice.html)
- Open a MagTek device attached to your desktop browser.
- You should see a message like:

```
Connected to: MagTek/Device/DynaFlexII/B54E05A
```

> ⚠️ **Important:** Do **not** close this browser window. It will disconnect the device.

---

### **Step 2: Access the MQTT Demo**
- On **any device** with internet access and a browser, visit the [MQTT MMS Demo](https://rms.magensa.net/TEST/HID/mmsMPPGDemo.html)

---

### **Step 3: Connect to a MagTek Reader**
- Scroll to the bottom of the page and click the hyperlink of the desired reader.
- A successful connection displays:

```
Configured Device: DynaProx/B544591  
Configured to use: TSYS - PILOT
```

---

### **Step 4: Enter Transaction Details**
- **Sale Amount** (Required)  
- **Tax** (Optional)  
- **Tip** (Optional)  
- **Receipt Email** (Optional)  
- **Receipt SMS** (Optional)

---

### **Step 5: Process the Sale**
- Tap, dip, swipe your card  
- Or manually click **Process Sale** if auto-transact isn’t configured

---

### **Step 6: View the Processor Response**
- A successful transaction displays:
  - Authorization data
  - Receipt info  
- If provided, a copy of the receipt is sent to the email/SMS fields

---

### **Step 7: View Transactions in Merchant Portal**
[Magensa Merchant Portal](https://merchantportal.magensa.net/qtlogin)  
- Log in to view transactions tied to the **production** (not pilot) TSYS Merchant Account.

---

## Architecture Summary

The **MQTT MMS Demo** illustrates a **card-present transaction** using MagTek devices where:

- Both the **MagTek Device** and the **application** (browser/mobile/PC) are MQTT clients.
- They communicate via a **shared MQTT broker** using the **publish/subscribe** model.
- This ensures:
  - Secure message exchange
  - Flexibility for semi-integrated payments

The **Merchant Portal** functions similarly to a POS but does **not** touch sensitive card data. Instead, it monitors and reports transaction data in real time.


---
