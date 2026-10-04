Astra CPU Silencer v2.9.0
README / English

===========================================================

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
Astra CPU Silencer v2.9.0
Support: masatech.dev.apps@gmail.com
============================================================


============================================================
Astra CPU Silencer v2.9.0
README日本語 / 配布用説明書
============================================================

■ はじめに

Astra CPU Silencer は、Windows 標準の CPU 電源管理機能を利用して、
CPU の最大周波数、最小性能状態、ブースト動作を調整するためのユーティリティです。

独自のカーネルドライバや CPU 電圧の直接制御は使用しません。
設定変更には Windows 標準の電源管理機能（powercfg 等）を使用します。


■ 対応環境

・Windows 11 64bit
・Intel CPU / AMD Ryzen CPU
・管理者権限が必要です

※ Windows 10 でも動作する可能性がありますが、正式サポート対象は Windows 11 です。
※ PC・CPU・BIOS・メーカー独自電源管理機能などの違いにより、動作結果は異なる場合があります。


■ 基本的な使い方

1. Astra CPU Silencer を起動します。
2. 必要に応じて Windows 電源プランを選択します。
3. AC（電源接続時）/ DC（バッテリー駆動時）の設定を入力します。
4. ［設定を適用］を押します。

主な設定項目：

・最大周波数
・最小周波数
・ブーストモード
・Windows 起動時の自動実行

0 MHz は「最大周波数の制限なし」です。
CPU をオーバークロックする設定ではありません。


■ Standard 版の安全仕様

Standard 版の最小周波数入力は 1400 MHz を安全下限としています。

最小周波数の MHz 入力は、Windows の「最小のプロセッサの状態（%）」へ換算して適用されます。
そのため、入力した MHz が実際の CPU クロックとして常時固定されるわけではありません。

最大周波数は、CPU 型番が CPU 仕様データベースと完全一致した場合のみ、
登録済みのメーカー仕様最大値を入力上限として使用します。

CPU がデータベースで確認できない場合、最大値を推測しません。
その場合は 0 MHz（制限なし）をご利用ください。

データベース確認済み上限を超える値を入力した場合は、
入力欄だけを確認済み最大値へ修正し、その時点では Windows へ書き込みません。
表示された値を確認して、もう一度［設定を適用］してください。


■ 2500 MHz について

本プロジェクトの実機検証で安全上避けるべき値と判断したため、
2500 MHz が入力された場合は 2400 MHz へ自動的に変更します。


■ ブーストモード

Windows の Processor Performance Boost Mode に対応した 0～6 の値を使用します。
標準値は 1（Enabled）です。

Windows や CPU により、各モードの実際の挙動は異なる場合があります。


■ 「変更前へ復元」と「完全初期化」

メニューまたはタスクトレイから
［変更前へ復元 / 完全初期化］を選択できます。

【変更前へ復元】
Astra CPU Silencer が変更する前に保存した CPU 電源設定と
Processor メニューの表示状態へ戻します。

【完全初期化】
CPU 設定を Astra の基準初期値へ戻し、
Processor メニューを Clean Baseline へ整理して、
アプリ設定も初期化します。

通常、元の環境へ戻したい場合は「変更前へ復元」を使用してください。


■ 60分無料体験

ライセンス未登録時は 60 分間の無料体験が可能です。

体験時間は累積で管理されます。
手動でテストを終了した場合、残り時間は次回起動時へ引き継がれます。

体験時間が終了した場合は、
保存済みの変更前設定への復元を試みた後、
製品版ライセンス登録画面を表示します。


■ ライセンス登録

メニューの
［ライセンスキーの登録］
から登録できます。

画面に表示されるマシン ID を開発者へお知らせください。

サポート / ライセンス申請：
masatech.dev.apps@gmail.com

BOOTH：
https://masatech.booth.pm/


■ CPU 仕様データベース

CPU の基本周波数・最大周波数は、GitHub 上の CPU 仕様データベースを利用します。

CPU 型番の完全一致のみを採用し、
不明な CPU の最大周波数を推測して使用することはありません。

一度取得した有効なデータベースはローカルへキャッシュされます。


■ 診断ログ
サポートや不具合調査のため、診断ログを保存します。フォルダの隠しファイルを表示してから、フォルダのパスを追って下さい。  
保存先：C:\Users\<Windowsユーザー名>\AppData\Roaming\Astra_CPU_Silencer\Astra_Diagnostic_Log.txt  

※ <Windowsユーザー名> の部分は、お使いのWindowsアカウント名に置き換わります。  
配布フォルダやAstra CPU Silencer.exeと同じ場所には、診断ログを作成しません。  
診断ログには、CPU情報、Windows電源プラン、設定処理の結果など、不具合調査に必要な情報が記録されます。  

■ アップデート

アプリ内の
［ヘルプ］→［最新版の確認］
から GitHub Releases の最新版を確認できます。

GitHub：
https://github.com/Masa-Tech-777/Astra-CPU-Silencer


■ アンインストールについて

専用アンインストーラーはありません。

削除する前に、必要に応じて
［変更前へ復元］または［完全初期化］を実行してください。

その後 Astra CPU Silencer を終了し、
実行ファイルを削除してください。

スタートアップ登録を使用している場合は、
復元 / 完全初期化処理によって解除されます。


■ ご注意

本ソフトは CPU の電圧や BIOS 設定を直接操作するものではありませんが、
Windows の CPU 電源設定を変更します。

PC の状態を確認しながら無理のない設定で使用してください。

CPU クロックの実際の動作は、
CPU、Windows、電源プラン、負荷、温度、BIOS、メーカー独自制御などの影響を受けます。
入力した MHz と実クロックが常に一致することを保証するものではありません。

==================================================
【免責事項・ご注意点】
・本ソフトウェアはWindows標準APIのみを使用する安全設計ですが、CPUの動作周波数を変更する特性上、お使いのPC環境や設定値によってはOSの動作低下や一時的なフリーズが発生する可能性がございます。
・本ソフトウェアの使用、または使用不能によって生じた直接的・間接的な損害（ハードウェアの故障、データの消失、事業の中断、機会損失等）について、開発者（Masa Tech!! / イタチ）は一切の責任を負いかねます。
・必ずお使いの環境にて「無料お試し版（Trial）」で動作確認を行った上で、ご自身の責任においてご利用・ご購入ください。
==================================================


============================================================
Astra CPU Silencer v2.9.0
Support: masatech.dev.apps@gmail.com
============================================================
