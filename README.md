# mac-android-log-viewer

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Foakleychen0707%2Fmac-android-log-viewer&count_bg=%23473DC8&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

# How to Capture Android Logs on macOS (如何在 macOS 上抓取 Android Log)

This tutorial explains how to capture Android logs using ADB (Android Debug Bridge) on macOS. No need for Android Studio, just use the command line!

本文將介紹如何在 macOS 上使用 ADB (Android Debug Bridge) 抓取 Android 日誌。無需使用 Android Studio，只需使用 command 即可！

---

## Prerequisites (前置條件)

Before you start, make sure you have the following:

在開始之前，請確保你已具備以下條件：

- A macOS computer (一台 macOS 電腦)
- Android device with USB debugging enabled (啟用 USB 除錯的 Android 手機)
- A USB cable to connect your Android device to the Mac (一條 USB 線，用來將 Android 手機連接到 Mac)
- Confirmed that Developer Mode is enabled (確認已開啟開發者模式)
- Homebrew installed (已安裝 Homebrew) *(optional but recommended)*

---

## Step-by-Step Guide (步驟指南)

### 1. Install ADB (安裝 ADB)

First, install ADB (Android Debug Bridge) on your Mac. If you haven't installed Homebrew yet, you can install it first.

首先，安裝 ADB (Android Debug Bridge) 到你的 Mac。如果你尚未安裝 Homebrew，先安裝它。

### 2. Install Homebrew (安裝 Homebrew)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### 3. Install ADB using Homebrew
```
brew install android-platform-tools
```

### 4. Check Device Connection (檢查設備連接)
```
adb devices
```

### 5. Capture Android Logs (抓取 Android 日誌)
```
adb logcat
```

### 6. Save Logs to a File (將 Logs 儲存至檔案)

If you want to save the logs to a file instead of viewing them in real time, use:

如果你希望將日誌儲存至檔案，而不是即時查看，請使用：

```
adb logcat > /path/to/your/folder/log.txt
```

This will save the logs to the log.txt file in the specified folder. By default, if no path is provided, the file will be saved in the current directory where the command is executed.

這會將日誌儲存至指定資料夾中的 log.txt 檔案。如果未提供路徑，則會將檔案儲存在當前執行命令的目錄中。

---

## Conclusion

Hope this helps you! 😊
