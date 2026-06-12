# 🚀 ADB & Fastboot Command Center

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows" alt="Platform"/>
  <img src="https://img.shields.io/badge/Framework-WPF%20%7C%20.NET%208.0-indigo?style=for-the-badge&logo=.net" alt="Framework"/>
  <img src="https://img.shields.io/badge/License-Apache%202.0-green?style=for-the-badge" alt="License"/>
</p>
Preview: <img width="959" height="502" alt="image" src="https://github.com/user-attachments/assets/13ede0ac-c09c-4b5a-a758-f1a45d20647a" />

<p align="center">
  <strong>A modern Windows desktop interface for Android Debug Bridge (ADB) and Fastboot.</strong>
  <br />
  Built with C#, WPF, and asynchronous process execution.
</p>

---

## 📖 Overview

**ADB & Fastboot Command Center** converts common ADB, Android shell, and Fastboot commands into an organized graphical interface.

It is designed for Android developers, technicians, and advanced users who need to manage devices, install applications, read system information, run shell commands, control A/B slots, or flash firmware without manually typing every command.

The application includes **80+ built-in operations** across multiple categories and supports selected-device targeting through ADB and Fastboot serial numbers.

> [!WARNING]
> Flashing, erasing, formatting, unlocking, relocking, and factory firmware installation can erase data or make a device unbootable. Always use files made for the exact device model and build.

---

## ✨ Core Features

* **Live Device Detection:** Detects ADB and Fastboot devices, displays serial numbers, connection states, model information, and the current A/B slot.
* **Asynchronous Execution:** Runs commands without freezing the WPF interface.
* **Selected Device Targeting:** Sends commands only to the selected ADB or Fastboot device.
* **Input Validation:** Validates files, package names, ports, coordinates, components, and partition names before execution.
* **Dangerous Command Warnings:** Displays confirmation dialogs for flashing, erasing, formatting, unlocking, relocking, wiping, and factory firmware operations.
* **Structured Logs:** Records command output, errors, duration, selected serial, and final status.
* **APK and File Management:** Installs APKs, handles split APKs, pushes files, pulls files, creates bugreports, and captures screenshots.
* **Device Controls:** Supports reboot, recovery, sideload, bootloader, screen input, screen recording, and shell commands.
* **Fastboot Tools:** Includes partition flashing, temporary image booting, erase, format, unlock status, slot switching, and OEM commands.

---

## 🏭 Factory Firmware Flashing

The **Flash Factory Firmware** feature allows the user to select an official:

```text
flash-all.bat
```

The application validates the file, opens a visible Windows Command Prompt, and runs the original factory flashing script.

It also:

* Uses the firmware folder as the working directory
* Adds the configured platform-tools folder to `PATH`
* Passes the selected Fastboot serial using `ANDROID_SERIAL`
* Displays live bootloader, radio, image update, sending, writing, and failure output
* Uses the real script exit code to determine success or failure
* Refreshes connected devices after completion

> [!CAUTION]
> The standard Google `flash-all.bat` normally wipes user data because it uses the `-w` option.

---

## 🗂️ Command Categories

| Category              | Available Operations                                                                       |
| :-------------------- | :----------------------------------------------------------------------------------------- |
| **Connection**        | ADB/Fastboot device listing, server controls, USB restart, wireless connection and pairing |
| **Device Info**       | Build properties, battery report, memory, storage, display and network information         |
| **Apps & Packages**   | APK installation, split APKs, uninstall, clear data, disable/enable and activity launch    |
| **Files & Backup**    | Push, pull, bugreport, backup and directory listing                                        |
| **Shell & Logs**      | Logcat, kernel logs, process lists, CPU snapshot and custom shell commands                 |
| **Screen & Input**    | Screenshot, screen recording, tap, swipe and text input                                    |
| **Reboot & Recovery** | Android reboot, bootloader, recovery, sideload and Fastboot reboot                         |
| **Fastboot Flash**    | Boot, recovery, vbmeta, custom partition, erase, format and factory firmware               |
| **Fastboot OEM**      | Unlock, lock, critical unlock, userdata wipe, boot mode and A/B slot controls              |
| **Root & Advanced**   | Root-based `devinfo` backup                                                                |

---

## 🔧 Platform Tools

The application requires both:

```text
adb.exe
fastboot.exe
```

Only a platform-tools folder containing both executables is accepted.

For real-device use, use official Android SDK Platform Tools. Do not use mock executables when a real phone is connected.

---

## 📥 Installation

### Windows Installer

Download the latest setup package:

[AdbCommandCenter-Setup-1.0.0-win64.exe](https://github.com/zainaamir384/Adb-Command-Center/releases/download/v2.0.0/AdbCommandCenter-Setup-2.0-win64.exe)

### Portable Build

Run from the project root:

```powershell
dotnet publish AdbCommandCenter\AdbCommandCenter.csproj `
  -c Release `
  -r win-x64 `
  --self-contained true `
  -p:PublishSingleFile=true `
  -p:IncludeNativeLibrariesForSelfContained=true `
  -o .\publish\
```

---

## ⚠️ Safety Notes

Before running destructive operations:

* Back up important data
* Confirm the exact device codename
* Use matching firmware files
* Use a reliable USB cable
* Charge the device sufficiently
* Connect only one Fastboot device
* Do not interrupt an active flash
* Do not relock the bootloader until stock firmware boots successfully

Mock testing can verify command construction and application behavior, but it cannot guarantee compatibility with real hardware.

---

## 🛠️ Technology Stack

* C#
* WPF
* .NET 8
* ADB
* Fastboot
* Asynchronous process execution

---

## 📄 License

Licensed under the **Apache License 2.0**.

---

## 👨‍💻 Developer

Developed by **Zain Aamir**.
