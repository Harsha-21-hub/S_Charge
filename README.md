# 🔋 S Charge

S Charge is a lightweight, root-powered smart charging manager for Android devices. Designed for rooted devices with compatible kernels, it helps extend battery longevity by automatically controlling charging at user-defined battery percentage thresholds. Built as part of the **S Suite** ecosystem, S Charge features a custom **Nothing OS-inspired** dot-matrix design with real-time battery telemetry and kernel-level charging control.

---

## ✨ Features

- **Smart Charge Protection:** Automatically stops charging at a configurable battery percentage and resumes charging at a lower user-defined threshold.
- **Kernel-Level Charging Control:** Uses Linux sysfs battery and charger nodes on supported rooted devices for hardware-level charging management.
- **Real-Time Battery Monitoring:** Displays live battery percentage, voltage, current, power consumption, temperature, and charging status.
- **Battery Analytics:** Interactive graphs for voltage, current, power, and temperature.
- **Nothing OS Inspired UI:** Minimal monochrome interface with custom dot-matrix styling.
- **Automatic Monitoring:** Starts monitoring when the charger is connected and stops automatically when the charger is unplugged.
- **Offline & Private:** Operates entirely on-device without collecting or transmitting any personal data.

---

## 🚀 How to Install

1. Go to the **Releases** section of this repository.
2. Download the latest **S_Charge.apk**.
3. Install the APK on your rooted Android device.
4. Grant **Superuser (Root)** permission when prompted.
5. Configure your preferred **Stop Charging** and **Resume Charging** percentages.

---

## 🔒 Permissions Guide

### 1. Root (Superuser)

**Why it's needed:**  
S Charge writes to supported Linux sysfs battery and charger nodes to control charging behavior. These files are only accessible with root privileges.

**How to grant:**  
When prompted by your root manager (Magisk, KernelSU, APatch, etc.), tap **Grant**.

---

### 2. Notifications

**Why it's needed:**  
To run the charging monitor as a foreground service and keep users informed about charging status.

---

### 3. Boot Completed

**Why it's needed:**  
Allows S Charge to automatically restore monitoring after the device boots when appropriate.

---

## ⚠️ Compatibility

- Requires **Root Access**.
- Compatible only with kernels exposing writable charging control sysfs nodes.
- Charging control depends on your device, kernel, and battery driver implementation.
- Monitoring features work on most rooted Android devices, while charging control is limited to supported kernels.

---

## 🛠️ Technical Specs

- **Minimum SDK:** Android 8.0 (API 26)
- **Target SDK:** Android 16 (API 36)
- **Architecture:** Universal APK
- **Package:** `com.hesi.scharge`
- **Language:** Kotlin
- **UI Framework:** Jetpack Compose
- **Root Framework:** libsu
- **Data Storage:** Android DataStore
- **Internet Required:** ❌ No

---

## 🔒 Privacy

S Charge is completely offline.

The application:

- Does **not** collect personal information.
- Does **not** upload any data.
- Does **not** require an internet connection.
- Does **not** include advertisements or analytics.

All settings and charging preferences remain stored locally on your device.

---

## ⚠️ Disclaimer

S Charge is intended for advanced users with rooted Android devices. Charging control is available only on supported kernels that expose writable charging control interfaces. Improper kernel modifications or unsupported devices may prevent charging control from functioning correctly.

The developer is not responsible for any damage resulting from unsupported kernels, custom ROMs, or improper device modifications.
