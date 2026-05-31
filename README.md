# 🚀 ADB & Fastboot Command Center

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows" alt="Platform"/>
  <img src="https://img.shields.io/badge/Framework-WPF%20%20.NET%208.0-indigo?style=for-the-badge&logo=.net" alt="Framework"/>
  <img src="https://img.shields.io/badge/License-Apache%202.0-green?style=for-the-badge" alt="License"/>
</p>

<p align="center">
  <strong>A sleek, high-performance, and safe desktop Graphical User Interface (GUI) wrapper for Android Debug Bridge (ADB) and Fastboot toolkit.</strong> <br />
  Built with C# and WPF utilizing an asynchronous execution architecture to maximize flash safety and layout stability.
</p>

---

## 📖 Overview

**ADB & Fastboot Command Center** abstracts away the tedious command-line interface (CLI) into a striking, ultra-modern dark UI equipped with neon mint glows. Designed explicitly for power users, developers, and Android enthusiasts tweaking modern devices like the **Google Pixel 6** series, this utility ensures low-level partition flashing functions flawlessly without putting your real hardware at risk.

Featuring **58 built-in automated macro actions** spread across nested contextual grids, you can command, query, backup, format, and flash any system node instantly.

---

## ✨ Core Features

* **📱 Live Device Detection & Discovery:** Auto-updates active device states with bright green authorization badges. Queries internal properties (`ro.product.model`, manufacturer details) on the fly via background streams.
* **⚡ Asynchronous Execution Core:** Process runners read system output buffers concurrently (`ReadToEndAsync`), keeping the WPF interface thread fluid and responsive without freezing.
* **🛡️ Production Flash Safety Engine:** Advanced string parsers dynamically sanitize custom input names using strict whitelists (`^[a-zA-Z0-9_-]+$`) to prevent CLI character injection attacks.
* **⚠️ Intelligent Hardware Guardrails:** Intercepts critical execution pathways to display alert modals if low-level infrastructure layouts (like `persist`, `modem`, or `bootloader`) are targeted. Includes explicit architectural warnings regarding dynamic A/B slot formatting variables.
* **📋 Real-Time Output Mirroring:** Features an advanced Cascadia Mono terminal interface with timestamped logging arrays supporting instant selective text grouping or single-click clipboard copying.

---

## 🗂️ Staging Workspace Grid

The workflow separates custom toolsets across granular categorical panels:

| Category | Icon | Target Macro Utilities |
| :--- | :---: | :--- |
| **Connection** | 🌐 | List ADB Devices, Kill ADB Server, Start ADB Server, Wireless TCP/IP Pairing |
| **Device Info** | 📊 | Full Build Reports, Battery Health Status, Dumpsys Meminfo, Free Storage Usage |
| **Apps & Packages** | 📦 | APK/Split-APK Installer, Wipe App Cache, App Disabling, Activity Staging |
| **Files & Backup** | 📁 | Push Files, Pull Files, Android Bugreports, Directory Trees |
| **Shell & Logs** | 💻 | Logcat Snapshot, Buffer Purging, DMESG Ring Buffer, Custom Active Terminal |
| **Screen & Input** | 🖥️ | Frame Buffer Screen-capping, Video Record, Tap/Swipe Simulation Matrix |
| **Reboot & Recovery** | 🔄 | Normal Reboot, Bootloader, Sideload Staging, EDL, FastbootD Recovery Jump |
| **Fastboot Engine** | ⚡ | Getvar Dump, Device-Info Variables, Boot Image Staging, Flash/Erase/Format |

---

## 📥 Installation & Deployment

### Method A: All-In-One Automated Installer 🚀
1. Click here to download the official standalone setup package directly from the repository release tag: [AdbCommandCenter-Setup-1.0.0-win64.exe](https://github.com/zainaamir384/Adb-Command-Center/releases/download/v1.0.0/AdbCommandCenter-Setup-1.0.0-win64.exe)
2. Launch the setup file on your computer. Accept the standard open-source license agreements.
3. The wizard automatically initializes, pulls the official platform-tools archive payload directly from Google’s production servers, and provisions the directories inside Program Files dynamically!

### Method B: Self-Contained Portable Build 🧳
For offline environments or portable execution arrays, use standard framework compilation commands inside the project root folder:

```powershell
dotnet publish AdbCommandCenter\AdbCommandCenter.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfContained=true -o .\publish\
