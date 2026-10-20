Astra CPU Silencer v2.9.6
README / English
============================================================

■ Introduction

Astra CPU Silencer is a Windows utility that adjusts CPU power-management
settings using standard Windows power controls.

It can manage maximum CPU frequency, minimum processor performance, boost
behavior, and per-power-plan settings without using a custom kernel driver
or directly changing CPU voltage.


■ Supported Environment

・Windows 11 64-bit
・Intel CPUs
・AMD Ryzen CPUs
・Administrator privileges are required

※ Windows 10 may work, but it is not officially supported.
※ Actual behavior may vary depending on the CPU, BIOS, Windows power plan,
   thermal conditions, and manufacturer-specific power-management features.


■ Main Features

・Maximum CPU frequency control
・Minimum processor performance control
・Processor Performance Boost Mode control
・Separate AC and DC settings
・Per-Windows-power-plan settings
・Startup support
・CPU specification database
・Restore Original
・Full Reset
・60-minute trial mode
・License activation
・Built-in update check


■ Basic Usage

1. Launch Astra CPU Silencer.
2. Select the Windows power plan you want to configure.
3. Set the AC and DC values.
4. Click [Apply Settings].

Maximum Frequency:
0 MHz means Unlimited.

This does not overclock the CPU.
It removes the maximum-frequency limit applied by Astra CPU Silencer.

Minimum Frequency:
The Standard edition uses a minimum input floor of 1400 MHz.

The entered MHz value is converted to the Windows
"Minimum processor state (%)" setting.
It does not force the CPU to run at the entered MHz continuously.


■ CPU Specification Database

Astra CPU Silencer identifies the CPU model and uses the CPU specification
database only when the model matches an entry exactly.

For a verified CPU:

・The registered base frequency is displayed.
・The registered maximum frequency is displayed.
・The registered maximum frequency is used as the allowed input ceiling.

If the CPU cannot be verified in the database, Astra CPU Silencer does not
guess its maximum frequency.

In that case, use 0 MHz for Unlimited.

If a value above the verified maximum is entered, the input field is corrected
to the verified maximum, but Windows settings are not changed at that moment.
Review the corrected value and click [Apply Settings] again.

A valid database copy may be cached locally for offline reuse.


■ 2500 MHz Safety Redirect

For this project, 2500 MHz is treated as a value that should be avoided based
on hardware testing.

If 2500 MHz is entered, Astra CPU Silencer automatically redirects it to:

2400 MHz


■ Boost Mode

Processor Performance Boost Mode uses the Windows values 0 through 6.

The default value is:

1 (Enabled)

The exact effect of each boost mode may vary depending on the CPU and
Windows implementation.


■ Restore Original and Full Reset

Open:

Menu -> Restore Original / Full Reset

[Restore Original]
Restores the saved CPU power settings and Processor-menu visibility from
before Astra CPU Silencer changed them.

Use this when you want to return the PC to its previous state.

[Full Reset]
Restores Astra baseline CPU settings, reorganizes the Processor menu to the
Astra Clean Baseline, and resets application settings.

Restore Original and Full Reset are intentionally different operations.


■ 60-Minute Trial

Without a registered license, Astra CPU Silencer can be used in a
60-minute trial mode.

Trial usage is accumulated.

Ending the test manually does not consume the remaining time.
The remaining trial time continues on the next launch.

When the trial expires, Astra CPU Silencer attempts to restore the saved
pre-change CPU power settings before displaying the license-registration screen.


■ License Activation

Open:

Menu -> Register License Key

The application displays a Machine ID used for license issuance.

Support / license requests:
masatech.dev.apps@gmail.com

BOOTH:
https://masatech.booth.pm/


■ Diagnostic Log

Astra CPU Silencer stores a diagnostic log for support and troubleshooting.

Location:

%AppData%\Astra_CPU_Silencer\Astra_Diagnostic_Log.txt

The diagnostic log is stored inside AppData.
It is not normally created beside the distributed EXE.

The log may contain information about the CPU, Windows power plans,
detected settings, and power-setting operations required for troubleshooting.


■ Updates

Use:

Help -> Check for Updates

Astra CPU Silencer checks the latest GitHub Release.

GitHub:
https://github.com/Masa-Tech-777/Astra-CPU-Silencer


■ Uninstalling

Astra CPU Silencer does not use a dedicated uninstaller.

Before deleting the application, use [Restore Original] or [Full Reset]
if needed.

Then exit Astra CPU Silencer and delete the executable.

If Startup registration is enabled, the restore/reset process removes the
related Startup entry.


■ Important Notes

Astra CPU Silencer does not directly modify CPU voltage or BIOS settings,
but it does change Windows CPU power-management settings.

Use settings appropriate for your system and verify system behavior after
applying changes.

Actual CPU frequency is affected by many factors, including:

・CPU architecture
・Windows power management
・Current workload
・Temperature
・BIOS settings
・Manufacturer-specific firmware and power controls

The entered MHz value does not guarantee that the CPU will operate at exactly
that frequency at all times.


============================================================
Astra CPU Silencer v2.9.5
Support: masatech.dev.apps@gmail.com
============================================================
