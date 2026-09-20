# VoltTune 🛴⚡

**Scooter tuning app for Ninebot, Xiaomi and Navee scooters — built with Capacitor for native iOS.**

## Features
- Real BLE scan — no OS picker dialog
- NinebotCrypto encrypted pairing (all modern scooters)
- Speed limit tuning with per-model hardware maximums
- Sport Mode, Zero Start, Eco Mode, Cruise Control, Lock, Headlight
- Controller & firmware info (on supported models)
- Panic Button with configurable trigger
- Accent color themes + Rainbow mode
- 89 supported models

## Install via AltStore (no Mac needed)

1. **Install AltStore on your iPhone:**
   - On your PC: download AltServer from [altstore.io](https://altstore.io)
   - Connect iPhone via USB, open AltServer, install AltStore on iPhone
   - Open AltStore on iPhone, sign in with your Apple ID (free)

2. **Download VoltTune.ipa:**
   - Go to the [Releases page](../../releases/latest)
   - Download `VoltTune.ipa`

3. **Install VoltTune:**
   - Open AltStore on iPhone → tap **+** (bottom right)
   - Select the downloaded `VoltTune.ipa`
   - Wait for installation

4. **Trust the app:**
   - iPhone Settings → General → VPN & Device Management
   - Tap your Apple ID → Trust

5. **Open VoltTune** and connect your scooter!

> **Note:** AltStore re-signs apps every 7 days. Keep AltServer running on your PC with iPhone connected (or use AltStore+/Wireguard for wireless refresh).

## Build from source

```bash
git clone https://github.com/YOUR_USERNAME/volttune
cd volttune
npm install
npx cap add ios
npx cap sync
npx cap open ios
# In Xcode: select your team, build & run
```

## Supported models
- **Ninebot/Segway:** E-series, F-series, MAX G-series, GT-series, ZT3, P-series (44 models)
- **Xiaomi:** M365, Pro, 1S, 3, 4, 5, 6 series including Pro/Ultra variants (25 models)
- **Navee:** N/S/V/GT/ST series (20 models)

## Protocol
Implements the NinebotCrypto TEA-based encrypted BLE protocol (credit: [ScooterHacking.org](https://scooterhacking.org) / majsi), plus the legacy unencrypted Ninebot UART protocol for older models.
