# 🔬 LSPosed Detector

**Root Module — LSPosed Injection Trace Scanner**

LSPosed Detector is a Root module that detects all **LSPosed** and **RElsposed** injection traces on your Android device using 5 comprehensive scan sections with a live WebUI dashboard built right into KSU Manager.

<div align="center">
  <img src="assets/demo.gif" alt="LSPosed Detector Demo" width="300"/>
  <p><i>Live scan in action</i></p>
</div>

---

## ✨ Features

- 🧬 System props detection (`ro.relsposed.*`, `ro.lspd.*`, `ro.zygisk.enabled`)
- 📁 Filesystem path scan (`/data/adb/lspd`, `/data/adb/relsposed`, `/data/adb/modules`)
- 🗺️ Zygote maps analysis (injected `.so` libs in zygote & zygote64)
- 📦 Installed packages scan (LSPosed / RElsposed / Xposed / Zygisk)
- 🔍 Per-app deep scan — maps, file descriptors, thread names
- 📱 Searchable dropdown of all third-party apps — scan runs instantly on selection
- ⚡ Live WebUI inside KSU Manager — no ADB, no terminal

**UI**: Dark terminal-style design with live animated scan progress.

---

## 📥 Download

**Version 1.0.0** — [Download ZIP](https://github.com/arvinjangid/LSPosed-Detector/releases/download/LSPosed-Detector-v1.0.0/lspd-detector-v1.0.0.zip)

### Requirements
- KernelSU
- LSPosed or RElsposed installed
- Android 10+

---

## 🚀 Quick Start

1. **Download** `lspd-detector-v1.0.0.zip`
2. Open **Root Manager** → Modules → tap **+**
3. Select the zip → **Reboot**
4. KSU Manager → Modules → **LSPosed Detector** → tap **Open WebUI**
5. Tap **▶ RUN FULL SCAN**

```
✅ Green  = Clean — no trace detected
⚠️ Yellow = Warning — suspicious but not definitive
❌ Red    = FOUND — injection trace detected
```

---

## 🧪 Scan Sections

| # | Section | What It Checks |
|---|---------|----------------|
| 1 | **System Props** | `ro.relsposed.*`, `ro.lspd.*`, `ro.zygisk.enabled`, `ro.dalvik.vm.native.bridge`, build tags, debuggable, SELinux state |
| 2 | **Filesystem Paths** | `/data/adb/lspd`, `/data/adb/relsposed`, `/data/misc/lspd`, `/data/adb/modules`, `/data/adb/ksu` |
| 3 | **Zygote Maps** | Injected `.so` libraries in `/proc/<zygote>/maps` and `zygote64` — shows exact filenames |
| 4 | **Installed Packages** | All packages matching LSPosed / RElsposed / Xposed / Zygisk names visible to `pm list` |
| 5 | **App Deep Scan** | Select any third-party app → scans `/proc/<pid>/maps`, file descriptors, and thread names for injection traces |

---

## 📱 App Deep Scan — How to Use

1. **Open the app** you want to scan (e.g. a banking app) so it's running in the background
2. In the WebUI, scroll to **Section 5**
3. Tap the search box and type the app name
4. **Tap the app** in the dropdown — scan runs instantly
5. Detected lines from `/proc/maps`, suspicious fds, and thread names are shown inline

> If the app shows **NOT RUNNING** — open it first, then re-select it from the dropdown.

---

## 📞 Contact

- 🐛 **Issues**: [GitHub Issues](https://github.com/arvinjangid/lspd-detector/issues)
- 📧 **Email**: arvinj581@gmail.com
- 💼 **Developer**: Arvin Jangid

---

**Version**: 1.0.0 | **Developed by**: Arvin Jangid | **Made with ❤️**
