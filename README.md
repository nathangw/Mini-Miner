# MiniMiner Project — Compact 16-Core Crypto CPU Miner

Full Build Playlist:   https://youtube.com/playlist?list=PLz4TjqIRHbyDjz2bluU7x6abvywT1p9yq&si=cQBJ917Fk-47ptS9

Welcome to the **MiniMiner Project**, an open hardware + software platform for building a compact, efficient, fully-autonomous 16-core CPU cryptocurrency miner.  
This repository contains everything you need to build the physical frame, assemble the system, and install the complete MiniMiner software stack, including auto-updates, watchdog recovery, real-time telemetry, and hands-free operation.

---

## ⭐ Features

- Small-form-factor aluminum frame designed for airflow, serviceability, and durability  
- Supports 16-core Ryzen and similar CPUs optimized for RandomX mining  
- Full hardware assembly instructions with printable templates  
- Integrated cooling + PSU mount  
- Clean internal wiring layout using nylon ties  
- Fit-StatUSB LED support for real-time health indication  
- Plug-and-play Debian-based mining OS  

### Automatic:
- XMRig updating  
- System OS updating  
- Miner performance telemetry  
- Email notifications  
- Safe watchdog rebooting  

---

## 📦 What’s Included in This Repository

- Printable templates for the aluminum frame  
- Full build instructions for cutting, drilling, bending, and assembling the chassis  
- Photos of each step (if included)  
- The complete MiniMiner software suite, including:  
  - Miner Status JSON server  
  - Auto Update Script  
  - Watchdog Script  
  - LED Controller  
  - Rasdaemon integration  
  - Power + temperature sensors  
- Example `miner.env` configuration  

---

## 🔧 Hardware Overview

MiniMiner uses a compact aluminum flat-bar frame designed to mount:

- Standard ATX/SFX power supply  
- Mini-ITX motherboard with 16-core CPU  
- 120mm cooling fan  
- Fit-StatUSB RGB indicator  
- Optional USB-C lapdock for setup  
- Nylon-tie wiring system for a clean, vibration-free internal layout  

The entire chassis is built from **1" × 1/8" aluminum bar**, requiring only drilling, bending, and basic hand tools.

---

## 🛠️ Software Overview

The MiniMiner software stack turns the system into a **self-maintaining mining appliance**.

### **Miner Status Server**
A lightweight TCP JSON service providing:
- Hashrate  
- Temperature  
- Power usage  

Used by the watchdog and auto-update system.

### **Auto-Update System**
Automatically:
- Rebuilds XMRig from the latest GitHub release  
- Updates Debian packages  
- Collects before/after performance metrics  
- Sends detailed status emails  
- Performs safe system reboots  

### **Miner Watchdog**
Continuously monitors:
- CPU temperature thresholds  
- Short-term hashrate  
- Long-term hashrate  
- General system stability  

If the miner becomes unstable or unproductive, the watchdog will:
- Log the condition  
- Send an email report  
- Perform a safe reboot  
- Restore mining operation  

### **Fit-StatUSB LED Integration**
- **Green pulse** → Healthy operation  
- **Red pulse** → Warm but stable  
- **Off** → Error state or rebooting  

---
