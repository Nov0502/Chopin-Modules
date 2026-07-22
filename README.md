# ⚡ STouch Chopin
**STouch Chopin** is a high-performance module specifically designed and optimized for POCO X3 GT / Redmi Note 10 Pro 5G (`chopin`)

Created by: **@Nov0502**

---
## 🌟 Key Features
* 🎮 **Per-Game 120Hz Display Lock**: Automatically bypasses Xiaomi Powerkeeper & Joyose refresh rate throttling. Keeps your screen locked at 120Hz when playing games (PUBG, Mobile Legends, Genshin, etc.).
* ⚡ **Locked 240Hz Touch Sampling Rate**: Forces XiaomiTouch hardware drivers into 240Hz high-frequency report mode for instantaneous touch response and zero input delay.
* 🚀 **MediaTek Dimensity 1100 Engine Boost**: Dynamically switches CPU scaling governors and GED GPU boost parameters when a game is launched.
* 🔋 **Smart Battery Preservation**: Automatically restores default system refresh rates and power profiles when you exit your games.
* 📝 **Customizable Game List**: Add or remove game package names in 30 seconds directly from your phone.
* 📊 **Live Real-time Logging**: Writes active game detection logs directly to `/sdcard/stouch.log` for easy verification.
---
## 🛠️ Supported Environments
* **Device**: POCO X3 GT / Redmi Note 10 Pro 5G (`chopin`)
* **SoC**: MediaTek Dimensity 1100 (MT6891)
* **ROM**: MIUI 12.5 / 13 / 14 / HyperOS / AOSP (Android 11 - 14)
* **Root Managers**: ReSukiSU / SukiSU, KernelSU, Magisk (v20.4+), APatch
---
## 🚀 Installation Guide
1. Download **`STouch_Chopin.zip`**.
2. Open your Root Manager (**SukiSU**, **KernelSU**, **Magisk**, or **APatch**).
3. Select **Install from Storage / Modules** and select `STouch_Chopin.zip`.
4. Reboot your device.
---
## 🎮 How to Add / Edit Target Games
You can edit your target games directly on your phone using **MT Manager** or any text editor with root access:
1. Open **MT Manager** and navigate to:
   ```text
   /data/adb/modules/STouch_Chopin/service.
      ```
2. Near line 12, edit the `TARGET_GAMES` variable:
   ```sh
   TARGET_GAMES="com.tencent.ig com.mobile.legend com.mobile.legends com.pubg.krmobile com.vng.pubgmobile com.dts.freefireth com.dts.freefiremax com.miHoYo.GenshinImpact com.levelinfinite.sgameGlobal.default"
   ```
3. Add any game package name (separated by a space) and save the file.
### Finding a Game's Package Name
* **In MT Manager**: Open Menu -> **App Manager** -> Locate the game -> Copy package name.
* **Play Store**: Check the URL: `https://play.google.com/store/apps/details?id=com.mobile.legends` -> `com.mobile.legends`.
---
## 🔍 How to Verify It Is Working
Open **Termux** or any root file manager and view the live log file:
```sh
cat /sdcard/stouch.log
```
When launching **PUBG Mobile** or **Mobile Legends**, you will see:
```text
=== STouch Chopin Started ===
2026-07-22 06:35:00 - Module STouch Chopin initialized by Nov0502
2026-07-22 06:35:10 - Boot completed. Starting foreground game monitor...
2026-07-22 06:35:25 - [STouch] Game ACTIVE: com.tencent.ig -> Applied 120Hz + 240Hz Touch Mode!
2026-07-22 06:40:12 - [STouch] Game CLOSED: Restored normal mode.
```
---
**Author**: @Nov0502  
**License**: Open Source / Free to use for POCO X3 GT community.
