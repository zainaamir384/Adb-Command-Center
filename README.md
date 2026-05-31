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

[cite_start]**ADB & Fastboot Command Center** abstracts away the tedious command-line interface (CLI) into a striking, ultra-modern dark UI equipped with neon mint glows[cite: 294, 295, 542]. [cite_start]Designed explicitly for power users, developers, and Android enthusiasts tweaking modern devices like the **Google Pixel 6** series, this utility ensures low-level partition flashing functions flawlessly without putting your real hardware at risk[cite: 191, 193].

[cite_start]Featuring **58 built-in automated macro actions** spread across nested contextual grids, you can command, query, backup, format, and flash any system node instantly[cite: 121, 127].

---

## ✨ Core Features

* [cite_start]**📱 Live Device Detection & Discovery:** Auto-updates active device states with bright green authorization badges[cite: 314, 426]. [cite_start]Queries internal properties (`ro.product.model`, manufacturer details) on the fly via background streams[cite: 77, 98].
* [cite_start]**⚡ Asynchronous Execution Core:** Process runners read system output buffers concurrently (`ReadToEndAsync`), keeping the WPF interface thread fluid and responsive without freezing[cite: 92, 210].
* [cite_start]**🛡️ Production Flash Safety Engine:** Advanced string parsers dynamically sanitize custom input names using strict whitelists (`^[a-zA-Z0-9_-]+$`) to prevent CLI character injection attacks[cite: 247, 252].
* [cite_start]**⚠️ Intelligent Hardware Guardrails:** Intercepts critical execution pathways to display alert modals if low-level infrastructure layouts (like `persist`, `modem`, or `bootloader`) are targeted[cite: 248, 406]. [cite_start]Includes explicit architectural warnings regarding dynamic A/B slot formatting variables[cite: 403, 404].
* [cite_start]**📋 Real-Time Output Mirroring:** Features an advanced Cascadia Mono terminal interface with timestamped logging arrays supporting instant selective text grouping or single-click clipboard copying[cite: 443, 542].

---

## 🗂️ Staging Workspace Grid

[cite_start]The workflow separates custom toolsets across granular categorical panels[cite: 119]:

| Category | Icon | Target Macro Utilities |
| :--- | :---: | :--- |
| **Connection** | 🌐 | [cite_start]List ADB Devices, Kill ADB Server, Start ADB Server, Wireless TCP/IP Pairing [cite: 128, 129, 130, 133] |
| **Device Info** | 📊 | [cite_start]Full Build Reports, Battery Health Status, Dumpsys Meminfo, Free Storage Usage [cite: 137, 139, 140, 141] |
| **Apps & Packages** | 📦 | [cite_start]APK/Split-APK Installer, Wipe App Cache, App Disabling, Activity Staging [cite: 145, 146, 151, 152, 154] |
| **Files & Backup** | 📁 | [cite_start]Push Files, Pull Files, Android Bugreports, Directory Trees [cite: 156, 158, 159, 160, 161] |
| **Shell & Logs** | 💻 | [cite_start]Logcat Snapshot, Buffer Purging, DMESG Ring Buffer, Custom Active Terminal [cite: 162, 163, 164, 168] |
| **Screen & Input** | 🖥️ | [cite_start]Frame Buffer Screen-capping, Video Record, Tap/Swipe Simulation Matrix [cite: 169, 170, 171, 172] |
| **Reboot & Recovery** | 🔄 | [cite_start]Normal Reboot, Bootloader, Sideload Staging, EDL, FastbootD Recovery Jump [cite: 174, 175, 176, 177, 178] |
| **Fastboot Engine** | ⚡ | [cite_start]Getvar Dump, Device-Info Variables, Boot Image Staging, Flash/Erase/Format [cite: 188, 191, 193, 197, 201] |

---

## 📥 Installation & Deployment

### Method A: All-In-One Automated Installer 🚀
1. Click here to download the official standalone setup package directly from the repository release tag: [AdbCommandCenter-Setup-1.0.0-win64.exe](https://github.com/zainaamir384/Adb-Command-Center/releases/download/v1.0.0/AdbCommandCenter-Setup-1.0.0-win64.exe)
2. Launch the setup file on your computer. Accept the standard open-source license agreements.
3. The wizard automatically initializes, pulls the official platform-tools archive payload directly from Google’s production servers, and provisions the directories inside Program Files dynamically!

### Method B: Self-Contained Portable Build 🧳
For offline environments or portable execution arrays, use standard framework compilation commands inside the project root folder:

```powershell
dotnet publish AdbCommandCenter\AdbCommandCenter.csproj -c Release -r win-x64 --self-contained true -p:PublishSingleFile=true -p:IncludeNativeLibrariesForSelfContained=true -o .\publish\# Adb-Command-Center
