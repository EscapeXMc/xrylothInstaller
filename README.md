<div align="center">

# 🛠️ XRYLOTH INSTALLER

### The official installer & updater for the Xryloth Minecraft launcher.

**One click. Everything set up. Always up to date.**

[![Release](https://img.shields.io/github/v/release/EscapeXMc/xrylothInstaller?style=for-the-badge&color=22c55e&label=installer)](https://github.com/EscapeXMc/xrylothInstaller/releases/latest)
[![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20Linux-1e88e5?style=for-the-badge)](#-download)
[![License](https://img.shields.io/badge/license-Proprietary-ef4444?style=for-the-badge)](#-license)

[**Download**](#-download) · [**What it does**](#-what-it-does) · [**Launcher repo**](https://github.com/EscapeXMc/xryloth)

</div>

---

> **Note for the website:** the Xryloth website **Downloads** page reads the assets
> published in this repository's [releases](https://github.com/EscapeXMc/xrylothInstaller/releases).
> The launcher binaries themselves live in [`EscapeXMc/xryloth`](https://github.com/EscapeXMc/xryloth).

## 🚀 Download

| Platform | File | Notes |
| --- | --- | --- |
| 🪟 **Windows (universal)** | `xryloth_vX.Y.Z.W_windows_universal.exe` | Single portable installer — no setup required |
| 🪟 **Windows (32-bit)** | `xryloth_vX.Y.Z.W_windows32.exe` | For 32-bit Windows only |
| 🐧 **Linux (Debian/Ubuntu)** | `xryloth_vX.Y.Z.W_linux.deb` | `sudo apt install ./…deb` or `sudo dpkg -i` |

> **The asset filename is part of the interface — always keep the extension lowercase.**
> GNOME Software only recognises the lowercase `*.deb` suffix; a capital `.Deb` will not
> open on double-click (`no application was created for running file-to-app on
> plugin=packagekit`). GitHub also compares asset names case-insensitively, so `.deb` and
> `.Deb` cannot coexist on the same release.

---

## ✨ What it does

When you run the installer the first time:

1. **Choose a scope** — install for **everyone** on the computer, or **only for your account**.
2. **Requirements check** — it verifies everything Xryloth needs (for example **Java 21**, Java 17, curl, VC++ runtime, `libfuse2`).
   - Each item shows **Checking → Found** or **Not Found**.
   - Anything missing gets an **Install** button that fetches it live (winget / apt, or a direct download).
3. **Install** — it creates the hidden `.xryloth` folder, writes a `Status.txt` control file, drops a **desktop shortcut** for the installer, and downloads the launcher from [`EscapeXMc/xryloth`](https://github.com/EscapeXMc/xryloth) as `launcher.exe` / `launcher.appImage`.

After that, the same file becomes an **updater**:

- Open it again → it checks for a newer launcher and **launches it** (updating first if needed).
- It uses the `Status.txt` switch inside `.xryloth`:

  ```ini
  # Status file to change status. Change the line below to 'updater' or 'installer'
  Status = updater
  ```

Run it again from a **newer installer file** and you get three choices:

- **Repair** — rebuilds `Status.txt` and refreshes the desktop shortcut.
- **Reinstall** — removes the launcher and installs it again from scratch.
- **Uninstall** — removes every Xryloth file and folder, then opens <https://xrylothClient.vercel.app/uninstall>.

---

## 📄 License

**Proprietary — All Rights Reserved.** © Xryloth / EscapeXOG. This software may **not** be copied,
modified, or redistributed without written permission. See [`LICENSE`](LICENSE).

<div align="center">

**Made with ❤️ for the Minecraft community.**

</div>
