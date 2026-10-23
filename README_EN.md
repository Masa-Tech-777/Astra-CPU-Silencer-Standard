Astra CPU Silencer Standard v2.9.6
README / English
============================================================
## 🌙 MasaTech Weekend Night Sale / 週末ナイトタイムセール

🎉 **October 23–25, 2026 | 2026年10月23日（金）～25日（日）**

**Every night 20:00–05:59 JST (UTC+9)**  
**毎晩20:00～翌朝5:59（日本時間）**

- ⚡ Astra CPU Silencer Standard Edition：**¥150**
- ⚡ Astra CPU Silencer Extreme Edition：**¥300**

Intel・AMD対応。CPU周波数の設定に加えて、ターボブーストの動作モードも調整できます。

Supports Intel and AMD processors, with configurable CPU frequency limits and Turbo Boost modes.

🛒 **BOOTH:** https://masatech.booth.pm/

*3夜限定の特別価格です。 / Special prices available during the three scheduled sale periods.*

============================================================

■ About Astra CPU Silencer Standard

Manage CPU frequency limits and turbo/boost behavior with straightforward settings.

Astra CPU Silencer Standard is a CPU power-management utility for Windows 11,
supporting Intel CPUs and AMD Ryzen CPUs.

It detects the CPU model and, when the model exactly matches an entry in its
embedded CPU specification database, refers to the registered base and maximum
frequencies. You can configure maximum CPU frequency, minimum processor
performance, and boost behavior separately for AC and DC power.

On boost-capable CPUs, you can choose to disable boost or set a maximum
frequency that includes the range above the CPU's base frequency. You can also
select how aggressively Windows requests boost performance or favors efficiency.

Silencer applies settings to Windows power management. Afterward, Windows and
the CPU automatically manage frequency changes and boosting in response to
operating conditions. Silencer does not directly modify CPU voltage or BIOS
settings.

It is intended for users who want accessible controls for tuning CPU frequency
limits and boost behavior when balancing performance and heat. Results depend
on the CPU and system configuration.


■ Introduction

Astra CPU Silencer Standard is a Windows utility that adjusts CPU power-management
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

1. Launch Astra CPU Silencer Standard.
2. Select the Windows power plan you want to configure.
3. Set the AC and DC values.
4. Click [Apply Settings].

Maximum Frequency:
0 MHz means Unlimited.

This does not overclock the CPU.
It removes the maximum-frequency limit applied by Astra CPU Silencer Standard.

Minimum Frequency:
The Standard edition normally uses a minimum input floor of 1400 MHz.
If a lower maximum frequency is selected, the minimum is limited so that it does not exceed the maximum.

The entered MHz value is converted to the Windows
"Minimum processor state (%)" setting.
It does not force the CPU to run at the entered MHz continuously.


■ CPU Specification Database

Astra CPU Silencer Standard identifies the CPU model and uses the CPU specification
database only when the model matches an entry exactly.

For a verified CPU:

・The registered base frequency is displayed.
・The registered maximum frequency is displayed.
・The registered maximum frequency is used as the allowed input ceiling.

If the CPU cannot be verified in the database, Astra CPU Silencer Standard does not
guess its maximum frequency.

In that case, use 0 MHz for Unlimited.

If a value above the verified maximum is entered, the input field is corrected
to the verified maximum, but Windows settings are not changed at that moment.
Review the corrected value and click [Apply Settings] again.

The CPU specification database is embedded in the application.
CPU lookup does not require Internet access or a downloaded cache.


■ 2500 MHz Safety Redirect

For this project, 2500 MHz is treated as a value that should be avoided based
on hardware testing.

If 2500 MHz is entered, Astra CPU Silencer Standard automatically redirects it to:

2400 MHz


■ Boost Mode

Standard supports Windows Processor Performance Boost Mode settings 0 through 6.
These select the policy for turbo/boost behavior. The default is 1 (Enabled).

0: Disabled
   Disables boosting above the processor's nominal performance level.

1: Enabled
   Allows boost under normal Windows and CPU power-management behavior.

2: Aggressive
   On supported control interfaces, Windows requests higher boost performance
   more aggressively.

3: Efficient Enabled
   Allows boosting while taking efficiency into account.

4: Efficient Aggressive
   Combines efficiency-aware behavior with more aggressive boost requests.

5: Aggressive At Guaranteed
   An aggressive boost-request policy referenced to the CPU's guaranteed
   performance level.

6: Efficient Aggressive At Guaranteed
   An efficiency-aware boost-request policy referenced to the CPU's guaranteed
   performance level.

Notes:
・These modes do not lock the CPU to a fixed clock frequency.
・Their effects vary by CPU, firmware and Windows performance-control interface
  (such as P-state or CPPC). Some modes may behave identically on a given PC.
・A more aggressive setting does not guarantee a higher clock in every workload,
  and an efficient setting does not guarantee lower temperatures.
・On boost-capable CPUs, a configured maximum frequency may permit boosting
  within that limit, including above the base frequency.
・Entered MHz values are not a promise of exact operating frequencies.


■ Restore Original and Full Reset

Open:

Menu -> Restore Original / Full Reset

[Restore Original]
Restores the saved CPU power settings and Processor-menu visibility from
before Astra CPU Silencer Standard changed them.

Use this when you want to return the PC to its previous state.

[Full Reset]
Restores Astra baseline CPU settings, reorganizes the Processor menu to the
Astra Clean Baseline, and resets application settings.

Restore Original and Full Reset are intentionally different operations.


■ 60-Minute Trial

Without a registered license, Astra CPU Silencer Standard can be used in a
60-minute trial mode.

Trial usage is accumulated.

Time already used is counted; unused trial time is retained when you exit.
The remaining trial time continues on the next launch.

When the trial expires, Astra CPU Silencer Standard attempts to restore the saved
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

Use Help -> Save diagnostic log… to copy the log to a location you select.
You do not need to attach license keys or configuration files manually.
Review the log before sending it for support.

Astra CPU Silencer Standard stores a diagnostic log for support and troubleshooting.

Location:

%AppData%\Astra_CPU_Silencer\Astra_Diagnostic_Log.txt

The diagnostic log is stored inside AppData.
It is not normally created beside the distributed EXE.

The log may contain information about the CPU, Windows power plans,
detected settings, and power-setting operations required for troubleshooting.


■ Updates

Use:

Help -> Check for Updates

Astra CPU Silencer Standard checks the latest GitHub Release.

GitHub:
https://github.com/Masa-Tech-777/Astra-CPU-Silencer-Standard


■ Uninstalling

Astra CPU Silencer Standard does not use a dedicated uninstaller.

Before deleting the application, use [Restore Original] or [Full Reset]
if needed.

Then exit Astra CPU Silencer Standard and delete the executable.

If Startup registration is enabled, the restore/reset process removes the
related Startup entry.


■ Important Notes

Astra CPU Silencer Standard does not directly modify CPU voltage or BIOS settings,
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
Astra CPU Silencer Standard v2.9.6
Support: masatech.dev.apps@gmail.com
============================================================

■ Disclaimer and Compatibility

Although the software uses standard Windows APIs, changes to CPU power settings may reduce responsiveness or temporarily freeze the system, depending on the PC and selected values.
Masa Tech!! / イタチ disclaims responsibility for direct or indirect losses arising from use or inability to use the software, including hardware damage, data loss, business interruption and lost opportunities, to the extent permitted by applicable law.
Please test compatibility using the free trial before purchasing and use the software at your own responsibility.
Some manufacturer-specific motherboard or BIOS configurations may prevent control from working.
Applicable third-party license rights and their warranty terms are not restricted by this product notice; see THIRD-PARTY-RIGHTS.txt.

■ Distribution Files and Third-party Software

Extract the entire ZIP before launching the EXE.
README_JP.txt / README_EN.txt contain the Japanese and English instructions.
THIRD_PARTY_NOTICES.txt lists components and acknowledgements; THIRD-PARTY-RIGHTS.txt explains third-party rights.
licenses/ contains full license texts, component notices and the ScriptGuard author's permission record.
source/ contains the official AutoHotkey 2.0.29 and Ahk2Exe/BinMod source archives, runtime modification notes and build/apply instructions.
See source/BUILD-INFO.txt for this executable's build evidence and source/PROTECTED-RUNTIME-STATUS.txt for the supplied materials and verification limits.
Example.ahk is a harmless example of the third-party protection workflow. It is not required to run the product.
MasaTech's proprietary application source and license-issuing tools are not included.

Product terms do not restrict copying, modification or redistribution rights granted by applicable third-party licenses.
Third-party rights and warranty disclaimers are governed by their original license texts.

Help -> About -> Third-party software and licenses displays the basic embedded notices.
Those embedded documents can be viewed with the EXE alone. Consult the accompanying files for the newly supplied material and detailed build evidence.
Editing accompanying files does not automatically change the embedded display in this version.
When distributing this package, retain the complete set including licenses/ and source/ rather than distributing the EXE alone.

We sincerely thank the authors and developers of AutoHotkey and TAC109, the author of ScriptGuard.
