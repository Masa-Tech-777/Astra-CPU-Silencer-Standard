# Astra CPU Silencer Standard

**A Windows CPU power-management utility designed for quieter operation, lower temperatures, and reduced power consumption.**

Astra CPU Silencer is a Windows utility that helps users manage CPU performance through the operating system's built-in power-management features.

It does not directly modify CPU voltage or BIOS settings.

Designed with simplicity and safety-conscious operation in mind, Astra CPU Silencer provides an accessible graphical interface for adjusting CPU power settings without requiring users to navigate complex Windows power-management menus.

## 💡 Why Use Astra CPU Silencer?

Astra CPU Silencer is designed for users who want to:

- Reduce laptop fan noise
- Help control CPU temperatures
- Reduce unnecessary power consumption
- Improve power efficiency during everyday tasks
- Limit CPU performance when maximum speed is unnecessary
- Manage Windows CPU power settings through a simple interface

It can be especially useful when working in quiet environments such as libraries, offices, and home workspaces.

Actual results depend on the processor, cooling system, firmware, Windows configuration, and workload.

## ⚙️ Main Features

Astra CPU Silencer provides graphical controls for:

- Maximum CPU frequency limits
- Minimum processor performance settings
- Processor Performance Boost Mode
- Windows power-plan selection and switching
- Separate AC and DC power settings
- Three convenient performance presets
- Restoration of previously saved CPU power settings
- Application and CPU power-setting reset functions

The application uses Windows' built-in power-management mechanisms rather than directly changing CPU voltage or BIOS configurations.

## 🛡️ Standard Edition Design

The Standard edition includes input restrictions and confirmation behavior intended to reduce accidental configuration mistakes.

### Frequency Input Rules

- Minimum frequency input: **1400 MHz**
- Frequency adjustment steps: **100 MHz**
- Maximum frequency input of **0 MHz** means Unlimited

Astra CPU Silencer does not perform CPU overclocking.

### Minimum Processor State

A minimum-frequency value entered in MHz is converted to Windows' Minimum processor state (%) setting.

This does not lock the CPU to the specified frequency.

Actual operating frequency remains controlled by Windows, processor hardware, firmware, thermal conditions, and workload.

## 🔍 Exact-Match CPU Specification Database

Astra CPU Silencer uses a CPU specification database to identify supported processor models.

Manufacturer-published base and maximum frequencies are displayed only when the detected CPU manufacturer and model match a verified database entry.

The application does not estimate the maximum frequency of an unverified processor.

### Unverified Processors

If your CPU is not found in the verified database, use:

**0 MHz = Unlimited**

### Automatic Input Correction

If an entered maximum-frequency value exceeds the verified maximum frequency for the detected processor, the input field is automatically corrected.

However, the corrected value is not immediately applied to Windows.

The process is:

1. The entered value is corrected to the verified maximum.
2. The user reviews the corrected value.
3. The user presses **Apply Settings** again to apply the configuration.

This two-step procedure helps prevent unintended settings from being applied without review.

## 🛡️ 2500 MHz Automatic Adjustment

Based on hardware testing conducted during the project, an entered frequency value of:

**2500 MHz**

is automatically adjusted to:

**2400 MHz**

This is a project-specific input adjustment. It does not mean that 2500 MHz is inherently unsafe for all processors.

## ⚡ Three Performance Presets

Astra CPU Silencer includes three presets for convenient switching between performance and power-saving configurations.

| Preset | AC Power | DC Power |
|---|---|---|
| 🔴 Normal Mode | Unlimited | Unlimited |
| 🟡 Medium Silent | 3.0 GHz | 2.6 GHz |
| 🟢 Low Power Eco | 1.8 GHz | 1.6 GHz |

Presets can be selected directly from the Windows system tray.

These settings are managed through Windows power-management controls and do not force the CPU to operate continuously at an exact frequency.

## 🔄 Windows Power-Plan Management

Astra CPU Silencer allows users to select and activate power plans registered in Windows directly from the application.

Power settings can be managed separately for:

- **AC:** External power connected
- **DC:** Battery operation

Users can adjust CPU-related settings for different Windows power plans without manually navigating the Windows power-settings interface.

## 🔧 Restore and Reset Functions

### Restore Original

Restores the previously saved CPU power settings and Processor-menu visibility state from before Astra CPU Silencer changed them.

### Full Reset

- Restores CPU power settings to the Astra-defined baseline
- Organizes the Processor menu according to the Astra Clean Baseline
- Resets application settings

Full Reset does not perform a factory reset of Windows, the BIOS, or the computer.

## 🎁 60-Minute Free Trial

Astra CPU Silencer provides a 60-minute trial before license registration.

Trial time is accumulated across sessions.

- Total trial duration: 60 minutes
- Manually ending the trial preserves the remaining time for the next launch
- When the trial expires, the application attempts to restore the saved pre-change CPU power settings
- The license-registration screen is then displayed

The trial allows users to check compatibility and evaluate the application's behavior on their own systems before purchasing.

## 🔑 License Activation

Commercial distribution through BOOTH is planned.

After purchasing Astra CPU Silencer, open:

**Menu → Register License Key**

Check the displayed Machine ID and enter the issued license key to activate the full version.

## 💻 System Requirements

| Item | Requirement |
|---|---|
| Officially supported OS | Windows 11, 64-bit |
| Processor | Intel processors / AMD Ryzen processors |
| Permissions | Administrator privileges required |
| Windows 10 | May work, but is not officially supported |

Some features may be unavailable or behave differently depending on the processor, system firmware, manufacturer-specific power management, and Windows configuration.

## 📂 Package Contents

Main application and documentation files:

- Astra CPU Silencer.exe
- Readme_JP.txt
- Readme_EN.txt

The final distribution package may also contain third-party license notices, corresponding source materials for applicable components, and additional compliance documentation.

The complete file list will be confirmed before release.

## 📄 Diagnostic Log

Diagnostic information for support and troubleshooting is stored at:

`%APPDATA%\Astra_CPU_Silencer\Astra_Diagnostic_Log.txt`

This log may help investigate application behavior and reported problems.

## ⚠️ Disclaimer and Important Notes

Astra CPU Silencer uses Windows' built-in power-management mechanisms and does not directly modify CPU voltage or BIOS settings.

However, this design does not guarantee trouble-free operation on every computer.

Depending on the hardware, firmware, Windows configuration, and selected settings, users may experience reduced performance, unexpected behavior, or temporary system freezes.

To the extent permitted by applicable law, the developer disclaims liability for direct or indirect damages arising from the use of, or inability to use, this software, including hardware damage, data loss, business interruption, or loss of opportunity.

Users are strongly encouraged to evaluate the software on their own systems using the free trial before purchasing.

Use this software with an understanding of the potential effects of changing system power-management settings.

## 💌 Support and Contact

For questions, support requests, or bug reports:

**masatech.dev.apps@gmail.com**

---

**Development and Production**

- Itachi (Kyokan / Masa Tech!!)
- Astra
- Mahiru

*Designed to make Windows CPU power management simpler and more accessible.*
