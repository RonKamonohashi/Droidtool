# DROIDTOOL - Android Toolkit for Linux

DROIDTOOL is a user-friendly, menu-driven Bash script designed for Linux users to manage Android devices via ADB. It simplifies common tasks like device information retrieval, app management, file transfers, custom tweaks, and developer operations. Ideal for developers, enthusiasts, and power users who need a CLI-based toolkit without complex setups.

**Note:** This tool requires ADB debugging enabled on your Android device. Some features (e.g., global uninstalls or full device searches) require root access.

## Features

### Device Information
- Generate a comprehensive system report including:
  - Brand, model, Android version, SDK, serial, build, security patch,arch,supported archs.
  - Uptime, battery status (level, health, temperature).
  - Storage usage, memory info, screen resolution.
  - Network details (Wi-Fi name, IP address).
  - Hardware specs (CPU, GPU).

### App Management
- Install APKs (single files or from folder).
- Uninstall apps (with root support for global removal).
- Enable/disable apps (user or system-wide with root).
- Clear app data and cache (per app or just cache for all apps).

### File Management
- Pull/push files and folders between device and PC.
- Delete files/folders on the device.
- Search for files or folders

### Custom Settings
- TV Tweaks: Optimize animations, caches, and UI for better performance on Android TV devices (Android 9+).
- DNS Settings: Set private DNS providers (Cloudflare, Mullvad, AdGuard, etc.) or custom hostnames.
- Check for system updates.

### Developer Tools
- View, save, or clear logcat logs.
- Open an interactive ADB shell.
- Execute custom ADB commands.
- Capture screenshots.

## Requirements
- **Operating System:** Linux (tested on Arch-based and Debian-based distributions like Ubuntu).
- **Dependencies:** 
  - `android-tools` package The script automatically installs it if missing (requires `sudo`).

- **Device Setup:**

-Enable Developer Options
 * Go to Settings.
 * Tap About phone.
 * Tap Build number (usually under "Software information") seven times rapidly.
 * You will see the message "You are now a developer!"
 * Developer options is now available in the main Settings menu.

  - Android device with USB debugging enabled (Settings > Developer Options > USB DEBUGGING).
  - USB cable,IP Adress of the device (Wireless pairing supported for Android 11+).
- **Optional:** Root access on the device for advanced features.

## Installation
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/droidtool.git
   cd droidtool
   ```
2. Make the script executable:
   ```
   chmod +x droidtool
   ```
3. Run the script:
   ```
   ./droidtool
   ```

The script will check for `android-tools` and install it if needed (supports `pacman` and `apt` package managers).

## Usage
1. Launch the script: `./droidtool`.
2. Select a connection method (USB, IP, or Wireless Pairing for Android 11+).
3. Navigate through the interactive menus using numbers.
4. Follow on-screen prompts for each feature.

**Tips:**
- For root features, ensure your device is rooted (e.g., via Magisk).
- Use cautiously: Some operations (e.g., uninstalls, tweaks) are irreversible without backups.
- If ADB fails, ensure no port conflicts and accept the debugging prompt on your device.

## Acknowledgments
-Thanks to the ADB and Fastboot Devs.
- Inspired by the FOSS community .