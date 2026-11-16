# AgneaX OS — Keyboard Shortcuts & Command Reference Guide

A complete, categorized reference of all global hotkeys, window management shortcuts, native application binaries (`agneax-*`), terminal productivity commands, and system administrative tools in **AgneaX OS (Ubuntu 24.04 LTS Noble Numbat)**.

---

## 📑 Table of Contents
1. [Global Desktop Shortcuts (System Hotkeys)](#1-global-desktop-shortcuts-system-hotkeys)
2. [Window Management & Navigation (KWin X11)](#2-window-management--navigation-kwin-x11)
3. [Screenshot & Screen Capture Controls](#3-screenshot--screen-capture-controls)
4. [AgneaX Native Applications & Binaries](#4-agneax-native-applications--binaries)
5. [AgneaX System Daemons & Background Services](#5-agneax-system-daemons--background-services)
6. [Terminal Shortcuts & Power Navigation](#6-terminal-shortcuts--power-navigation)
7. [System Administration, Hardware & Diagnostic Commands](#7-system-administration-hardware--diagnostic-commands)
8. [Dual-Boot & Bootloader Management Commands](#8-dual-boot--bootloader-management-commands)

---

## 1. Global Desktop Shortcuts (System Hotkeys)

Managed by `agneax-hotkeys` with NumLock (`Mod2Mask`) and CapsLock (`LockMask`) immunity:

| Shortcut | Action Description | Target Executable / Service |
| :--- | :--- | :--- |
| **`Super` (Windows Key)** | Toggle AgneaX Fullscreen App Launcher | `agneax-launcher` |
| **`Ctrl` + `Alt` + `T`** | Open AgneaX Terminal | `agneax-terminal` |
| **`Meta` + `L`** | Lock Screen immediately | `agneax-screenlocker` |
| **`Ctrl` + `Alt` + `L`** | Alternative Lock Screen shortcut | `agneax-screenlocker` |
| **`Ctrl` + `Alt` + `Del`** | Open AgneaX Power Dialog (Shutdown/Reboot/Logout) | `agneax-shutdown` |
| **`Alt` + `Space`** | Open Quick Window Operations Menu | KWin Window Action |
| **`Ctrl` + `Alt` + `Backspace`** | Restart X11 Display Server (if enabled) | Xorg Server |

---

## 2. Window Management & Navigation (KWin X11)

Native macOS-style and standard Linux window management keybindings:

| Shortcut | Action Description | Scope |
| :--- | :--- | :--- |
| **`Alt` + `F4`** | Close the currently focused window | Active Window |
| **`Ctrl` + `Q`** | Quit active application gracefully | Active Application |
| **`Meta` + `Up Arrow`** | Maximize current window to fullscreen | Active Window |
| **`Meta` + `Down Arrow`** | Restore / Unmaximize current window | Active Window |
| **`Meta` + `Left Arrow`** | Tile window to the left half of display | Window Snapping |
| **`Meta` + `Right Arrow`** | Tile window to the right half of display | Window Snapping |
| **`Alt` + `Tab`** | Switch forward between active application windows | Task Switcher |
| **`Alt` + `Shift` + `Tab`** | Switch backward between active windows | Task Switcher |
| **`Meta` + `Tab`** | Alternative task switcher (CoverSwitch / FlipSwitch) | Visual Switcher |
| **`Ctrl` + `F1` .. `F4`** | Switch directly to Virtual Desktop 1, 2, 3, or 4 | Workspace Switcher |
| **`Ctrl` + `Alt` + `Left/Right`** | Cycle through Virtual Desktops | Workspace Switcher |
| **`Alt` + `Left Mouse Drag`** | Move window from anywhere inside its canvas | Interactive Move |
| **`Alt` + `Right Mouse Drag`** | Resize window from anywhere inside its canvas | Interactive Resize |
| **`F11`** | Toggle borderless fullscreen mode | Browser / Player / Apps |

---

## 3. Screenshot & Screen Capture Controls

All screenshot hotkeys launch interactive capture with annotation controls:

| Shortcut | Mode | Output / Behavior |
| :--- | :--- | :--- |
| **`PrintScreen`** | Full / Interactive Selection | Opens `agneax-screenshot` GUI |
| **`SysRq`** | Full / Interactive Selection | Fallback for keyboards with shared SysRq |
| **`Meta` + `Shift` + `S`** | Area / Rectangular Snipping | Modern Windows/macOS familiar shortcut |
| **`Ctrl` + `PrintScreen`** | Capture & Copy to Clipboard | Direct clipboard buffer |
| **`Shift` + `PrintScreen`** | Instant Fullscreen Capture | Saves to `~/Pictures/Screenshots/` |
| **`Ctrl` + `Alt` + `A`** | Custom Selection Snipping | Native Cutefish/AgneaX area hotkey |

---

## 4. AgneaX Native Applications & Binaries

All native GUI applications installed in `/usr/bin/`:

| Binary Command | Application Name | Category | Description |
| :--- | :--- | :--- | :--- |
| `agneax-calculator` | AgneaX Calculator | Utilities | Clean Qt5/QML desktop calculator |
| `agneax-camera` | AgneaX Camera | Media | Webcam capture, photo snap & video recording |
| `agneax-filemanager` | AgneaX Files | System | Native file browser with macOS-style layout |
| `agneax-imageviewer` | AgneaX Image Viewer | Graphics | High-speed photo preview with zoom & rotate |
| `agneax-screenshot` | AgneaX Screenshot | Utilities | Interactive screen snipping & markup tool |
| `agneax-settings` | System Settings | System | Comprehensive control center for display, themes, battery, audio |
| `agneax-terminal` | AgneaX Terminal | System | GPU-accelerated tabbed terminal |
| `agneax-text-writer` | Text Writer | Productivity | Syntax-highlighting code & note editor |
| `agneax-videoplayer` | AgneaX Video Player | Media | Hardware-accelerated MP4/MKV video player |
| `agneax-debinstaller` | Package Installer | System | Standalone GUI installer for `.deb` packages |
| `calamares-launcher` | Install AgneaX OS | System | Live-to-disk system installer with dual-boot engine |

---

## 5. AgneaX System Daemons & Background Services

Low-level daemons running in the desktop session:

| Daemon Binary | Purpose / Responsibility |
| :--- | :--- |
| `agneax-session` | Desktop environment master session initializer |
| `agneax-dock` | Floating bottom desktop application dock |
| `agneax-statusbar` | Top panel bar displaying time, status widgets & control center |
| `agneax-launcher` | Fullscreen categorized application drawer |
| `agneax-screenlocker` | PAM-authenticated desktop lockscreen (`com.agneax.ScreenLocker`) |
| `agneax-hotkeys` | Global X11 shortcut grabber (`kglobalaccel` bridge) |
| `agneax-settings-daemon` | Handles real-time brightness, audio volume, display resolution & power |
| `agneax-notificationd` | Desktop desktop notification server (`org.freedesktop.Notifications`) |
| `agneax-polkit-agent` | Elevated privilege authentication dialog (`polkit-1`) |
| `agneax-powerman` | Battery monitoring, display sleep, & system suspend manager |
| `agneax-clipboard` | Clipboard history synchronization manager |
| `agneax-gmenuproxy` | Global menu DBus proxy for GTK/Qt applications |
| `agneax-xembedsniproxy` | System tray icon converter for legacy XEmbed tray icons |
| `agneax-cpufreq` | CPU power profiles (Performance / Balanced / Power Saver) |
| `agneax-shutdown` | Interactive modal shutdown, restart, and logout interface |

---

## 6. Terminal Shortcuts & Power Navigation

Common command-line editing and process management shortcuts:

| Shortcut | Action Description |
| :--- | :--- |
| **`Ctrl` + `Shift` + `C`** | Copy selected text in terminal |
| **`Ctrl` + `Shift` + `V`** | Paste clipboard content into terminal |
| **`Ctrl` + `Shift` + `T`** | Open a new terminal tab |
| **`Ctrl` + `Shift` + `W`** | Close current terminal tab |
| **`Ctrl` + `Shift` + `N`** | Open a new terminal window |
| **`Ctrl` + `C`** | Interrupt / Terminate active foreground process (`SIGINT`) |
| **`Ctrl` + `Z`** | Suspend active foreground process (`SIGTSTP`) |
| **`Ctrl` + `D`** | Send EOF (End of File) or exit terminal session |
| **`Ctrl` + `L`** | Clear terminal screen (equivalent to `clear`) |
| **`Ctrl` + `A`** | Move cursor to the beginning of command line |
| **`Ctrl` + `E`** | Move cursor to the end of command line |
| **`Ctrl` + `U`** | Cut / Delete from cursor position to beginning of line |
| **`Ctrl` + `K`** | Cut / Delete from cursor position to end of line |
| **`Ctrl` + `W`** | Delete the preceding word |
| **`Ctrl` + `R`** | Reverse-i-search bash command history |
| **`Tab`** | Autocomplete command, option, or file path |
| **`Tab` + `Tab`** | Display all available command or filename completions |

---

## 7. System Administration, Hardware & Diagnostic Commands

Essential terminal commands for troubleshooting and managing AgneaX OS:

### Hardware & Battery
```bash
# Check battery health, capacity, and charge state
upower -i /org/freedesktop/UPower/devices/battery_BAT0

# Query raw sysfs battery data
cat /sys/class/power_supply/BAT*/capacity
cat /sys/class/power_supply/BAT*/status

# Query and adjust display backlight
brightnessctl get
brightnessctl set 50%
```

### Audio & Sound Server
```bash
# Verify audio sinks and sources
pactl info
pactl list sinks short

# Restart PulseAudio sound server
pulseaudio -k && pulseaudio --start
```

### Themes & Desktop Cache
```bash
# Rebuild icon caches for AgneaX themes
sudo gtk-update-icon-cache -f /usr/share/icons/AgneaX
sudo gtk-update-icon-cache -f /usr/share/icons/hicolor

# Update desktop application database
sudo update-desktop-database /usr/share/applications
```

### User Management
```bash
# Instant removal of leftover live user account after physical install
sudo userdel -f -r agneax

# Verify active user accounts on the system
cut -d: -f1,3 /etc/passwd | grep -E ':[1-9][0-9]{3}$'
```

---

## 8. Dual-Boot & Bootloader Management Commands

Standard commands for EFI, NVRAM, and GRUB administration:

### Disk & Partition Layout
```bash
# List all block devices with filesystem types, labels, and UUIDs
lsblk -f

# Print exact partition boundaries in KiB (for dual-boot Dell SSDs)
sudo parted /dev/nvme0n1 unit KiB print free

# Inspect GPT partition table and partition type GUIDs
sudo sgdisk -p /dev/nvme0n1
```

### UEFI NVRAM & Secure Boot
```bash
# View active UEFI boot entries in firmware NVRAM
sudo efibootmgr -v

# Check Secure Boot enforcement status
mokutil --sb-state
```

### GRUB Reinstallation & Config Regeneration
```bash
# Regenerate boot menu entries (auto-detects Windows Boot Manager & AgneaX OS)
sudo update-grub

# Reinstall signed UEFI bootloader to ESP
sudo grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=AgneaX_OS --recheck
```

