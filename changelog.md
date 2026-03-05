# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.1.0] - 2026-03-05

### Added

- **Extra Privacy: Sound Mute** - Optionally mute system audio when blur is active
  - Set `sound = 0` in `blur.conf` to enable auto-mute (default)
  - Set `sound = 1` to keep audio normal
  - Audio automatically unmutes when blur is disabled or app is closed
- Cross-platform volume control support:
  - Windows: PowerShell-based mute toggle
  - Linux: PulseAudio/ALSA support via `pactl` and `amixer`
  - macOS: AppleScript volume control

## [1.0.0] - 2026-03-05

### Initial Release

- Real-time screen blur overlay that covers the entire desktop.
- Capture screen using `mss` for high performance.
- Blur processing via OpenCV (if available) or PIL as fallback.
- Adjustable blur radius (via `*` and `/` keys).
- Grayscale mixing mode (toggle with F2, adjust intensity with F3/F4).
- Opacity control (via `+` and `-` keys).
- Colored mode (F1) resets grayscale mixing.
- Configuration saved to `blur.conf` (blur mode, blur radius, opacity, grayness).
- Hotkeys:
  - `Ctrl+Alt+B` – toggle overlay on/off.
  - `Ctrl+Alt+C` – quit application.
  - `F1` – colored mode.
  - `F2` – grayscale mode.
  - `F3` – decrease grayscale intensity.
  - `F4` – increase grayscale intensity.
  - `-` – decrease opacity.
  - `+` – increase opacity.
  - `/` – decrease blur radius.
  - `*` – increase blur radius.
- Window always on top, transparent for input (click-through).
- Platform‑specific topmost window hints for Windows and Linux.
- Minimal CPU usage with configurable frame rate.
