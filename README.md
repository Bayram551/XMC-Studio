# XMC Studio

<p align="center">
  <b>🎛️ A professional Digital Audio Workstation for Android</b><br/>
  <i>Kotlin · C++ · Oboe · ASv1 plugins</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Proprietary-red.svg"/>
  <img src="https://img.shields.io/badge/platform-Android-green.svg"/>
  <img src="https://img.shields.io/badge/minSdk-26-orange.svg"/>
  <img src="https://img.shields.io/badge/ABI-arm64--v8a-blue.svg"/>
  <img src="https://img.shields.io/badge/version-1.0.0-blue.svg"/>
</p>

---

## Download

👉 **[Download Latest APK](https://github.com/Bayram551/xmc-studio/releases/latest)**

Enable **"Install from unknown sources"** in your device settings.

---

## Screenshots

<table>
  <tr>
    <td align="center"><img src="screenshots/01-main.png" width="400"/></td>
    <td align="center"><img src="screenshots/02-mixer.png" width="400"/></td>
  </tr>
  <tr>
    <td align="center"><b>Timeline + Transport</b></td>
    <td align="center"><b>Mixer (16 Channels + Master)</b></td>
  </tr>
  <tr>
    <td align="center"><img src="screenshots/03-pianoroll.png" width="400"/></td>
    <td align="center"><img src="screenshots/04-plugin.png" width="400"/></td>
  </tr>
  <tr>
    <td align="center"><b>Piano Roll — MIDI Editor</b></td>
    <td align="center"><b>ASv1 Plugin Window</b></td>
  </tr>
</table>

---

## Features

### 🎹 Audio Engine
- Native C++ engine with **Oboe** (low-latency AAudio / OpenSL ES)
- 48 kHz / 32-bit float processing
- 16 channels × 12 voices per channel

### 🎛️ Mixer
- 16 channel strips
- Per-channel gain, pan, mute, solo
- Master bus with stereo peak meter

### 🎵 Timeline
- Multi-track arrangement (128 bars)
- Clip-based editing (drag, resize, delete)
- Snap-to-grid quantization

### 🎼 Piano Roll
- Full MIDI note editor
- Pitch range 24–120
- Quantization: 1/1 to 1/32

### 🔌 ASv1 Plugin Format
- External plugins as separate APKs
- Native `.so` loading via `dlopen`
- Manifest-driven UI
- See [docs/ASV1_PLUGIN_FORMAT.md](docs/ASV1_PLUGIN_FORMAT.md)

### 🎚️ Built-in Effects
- Reverb (Schroeder)
- Delay (stereo, tempo-sync)
- 3-band EQ
- Compressor
- Bitcrush

### 💾 Project System
- JSON-based save / load
- Auto-restore last project
- Undo / Redo (50 steps)

### 📤 Export
- 32-bit float WAV
- Native offline rendering

---

## System Requirements

| | |
|---|---|
| **OS** | Android 8.0 (API 26) or newer |
| **ABI** | ARM64 (arm64-v8a) |
| **Storage** | ~50 MB |
| **RAM** | ~100 MB |

---

## Plugin Development

XMC Studio supports the **ASv1** plugin format (Audio Session v1) — similar to AUv3 on iOS.

- Each plugin is a **separate APK**
- Plugin package is a **ZIP** (`.asv1`) with `manifest.json` + native `.so`
- Host discovers plugins via ContentProvider
- Native DSP loaded via `dlopen`

📖 **Full spec:** [docs/ASV1_PLUGIN_FORMAT.md](docs/ASV1_PLUGIN_FORMAT.md)
🧰 **Template:** [asv1-plugin-template](https://github.com/Bayram551/asv1-plugin-template)

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

---

## License

**Proprietary** — Copyright © 2026 Bayram. All rights reserved.
See [LICENSE](LICENSE) for details.

The APK is free to download and use on personal devices.
Source code is not distributed.

---

## Support

- 🐛 **Bug reports** → [Issues](https://github.com/Bayram551/xmc-studio/issues)
- 💡 **Feature requests** → [Discussions](https://github.com/Bayram551/xmc-studio/discussions)
- ⭐ **Star** if you like it