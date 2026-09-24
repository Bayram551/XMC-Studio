# XMC Studio

A professional Digital Audio Workstation (DAW) for Android — built with Kotlin + C++ + Oboe.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Platform](https://img.shields.io/badge/platform-Android-green.svg)
![Min SDK](https://img.shields.io/badge/minSdk-24-orange.svg)

---

## Features

### 🎹 Audio Engine
- Native C++ engine with **Oboe** (low-latency AAudio/OpenSL ES)
- 48 kHz / 32-bit float processing
- 16 channels, 12 voices per channel
- Multi-waveform oscillator (Sine / Square / Saw / Triangle / Noise)
- ADSR envelope per voice

### 🎛️ Mixer
- 16 channel strips
- Per-channel gain, pan, mute, solo
- Master bus with stereo meter
- Real-time peak metering

### 🎵 Timeline
- Multi-track arrangement
- 128 bars
- Clip-based editing
- Drag / resize / delete clips
- Snap-to-grid quantization

### 🎼 Piano Roll
- Full MIDI note editor
- Pitch zoom (24–120)
- Note drag, resize, delete
- Quantization grid (1/1 to 1/32)

### 🔌 ASv1 Plugin Format
- External plugins as separate APKs
- Native `.so` loading via `dlopen`
- Manifest-driven UI
- In-process DSP (AUv3-style)
- See [docs/ASV1_PLUGIN_FORMAT.md](docs/ASV1_PLUGIN_FORMAT.md)

### 🎚️ Effects
- **Reverb** — Schroeder algorithm
- **Delay** — stereo, tempo-sync
- **EQ** — 3-band
- **Compressor** — envelope follower
- **Bitcrush** — bit depth + downsampling

### 💾 Project System
- Save / load projects (JSON)
- Auto-restore last project
- Undo / Redo (50 steps)
- Dirty state tracking

### 📤 Export
- WAV export — 32-bit float, stereo
- Custom duration
- Native offline rendering

### 🎹 MIDI
- MIDI note input
- Velocity support
- Panic / all-notes-off

---

## Screenshots

> *(add screenshots here)*

---

## Requirements

| | |
|---|---|
| **OS** | Android 8.0 (API 26) or newer |
| **ABI** | ARM64 (arm64-v8a) |
| **Storage** | ~50 MB |
| **RAM** | ~100 MB |

---

## Installation

### From GitHub Releases

Download the latest APK:

👉 [**Download Latest Release**](https://github.com/Bayram551/xmc-studio/releases/latest)

Enable **"Install from unknown sources"** in your device settings.

### From Source

```bash
git clone https://github.com/Bayram551/xmc-studio.git
cd xmc-studio
./gradlew assembleDebug