<div align="center">

  <h1>☕ KofiType Signed Export Generator</h1>
  
  <p>
    <b>The ultimate payload forger and security bypass tool for KofiType — now targeting V5.</b>
  </p>

  <p>
    <a href="https://iamjaved.site"><img src="https://img.shields.io/badge/Made_with_❤️_by-Javed-d9a066?style=for-the-badge&logo=heart" alt="Made by Javed" /></a>
    <img src="https://img.shields.io/badge/Version-5.0-3b82f6?style=for-the-badge" alt="Version 5.0" />
    <img src="https://img.shields.io/badge/Status-Bypassed-10b981?style=for-the-badge" alt="Status" />
    <img src="https://img.shields.io/badge/Encryption-AES--256--GCM-ff6b6b?style=for-the-badge" alt="Encryption" />
  </p>

</div>

---

## 🚀 Overview

The **KofiType Result Forger** is a custom security tool designed to analyze, test, and bypass the "Guardian v5 Secure" Bootloader integrity checks found in KofiType V5.

This tool allows you to generate mathematically perfect `.kofi` export files with custom statistics (WPM, XP, Level, Accuracy) that will pass seamlessly through the live site's newest security validations — including SHA-256 signature verification, AES-GCM encryption, XOR checksum integrity, and zero-width steganographic encoding. It also features a built-in visual Profile Card generator exactly replicating the live site.

## ✨ Features

- **Profile Card Generator [NEW in V5]:** Visually preview your stats in a modal with an exact replica of the official V5 Profile Card. Capture and save it as a high-res PNG image natively via `html2canvas`.
- **AES-256-GCM Encryption:** Fully replicates the live site's AES-GCM encryption logic. Derives the 32-byte master key dynamically from the `SECURITY_TOKEN` (`4004198119` for V5).
- **Zero-Width Steganography:** Automatically encodes the encrypted payload into invisible zero-width characters (`\u200B` and `\u200C`). Exported `.kofi` files appear completely blank in Notepad — perfectly mimicking authentic KofiType exports.
- **XOR Checksum Forging:** Dynamically computes `_c = (XP * Level * Tests) ^ SECURITY_TOKEN` to match the Guardian's integrity verification.
- **Heuristic Bypass Engine:** Auto-adjusts typing time, history array lengths, tests completed, and XP relationships to satisfy all server-side heuristic checks:
  - `totalXP ≤ timeTyped × 45`
  - `timeTyped ≥ testsCompleted × 1`
  - `history.length === 20` when `tests ≥ 20` (else `=== tests`)
  - `bestWpm ≤ 350`
- **Realistic History Generation:** Creates plausible historical test entries with varied dates, randomized WPM/accuracy offsets, and pinned best-result entries.
- **One-Click Forge & Download:** Single button encrypts, encodes, and triggers an automatic `.kofi` file download.
- **Interactive Loading Modal:** Randomized "hacking" phase messages with animated progress bar during payload generation.
- **Premium Glassmorphism UI:** Dark-themed interface with tech-chip indicators, pulse animations, gradient accents, and full mobile responsiveness.

## 📂 Version History

| Version | File | Target | Token | Status |
|---------|------|--------|-------|--------|
| **v1.0** | `result genrator.html` | KofiType V1 | — | ✅ Legacy |
| **v2.0** | `result_generator_v2.html` | KofiType V2 | — | ✅ Working |
| **v3.0** | `result_generator_v3.html` | KofiType V3 | `4100198909` | ✅ Working |
| **v4.0** | `result_generator_v4.html` | KofiType V4 | `2589710461` | ✅ Working |
| **v5.0** | `result_generator_v5.html` | KofiType V5 | `4004198119` | ✅ Active |

## 🛠️ Usage

1. Open `result_generator_v5.html` in any modern web browser.
2. Enter your desired custom statistics (Username, WPM, XP, Level, etc.).
3. Click **⚡ Encrypt .kofi** to download the bypass file, OR click **📷 Profile Card** to open the visual card generator and save a PNG image.
4. Watch the interactive loading screen while the payload is mathematically sealed and encrypted.
5. The `.kofi` file downloads automatically — upload it to the live KofiType website!

> **Token Updates:** The generator ships with the V5 security token (`4004198119`) derived from hash `eeab36e7`. If the target site updates its source code, extract the new token by running:
> ```bash
> node get_v5_hash.js
> ```
> Then update the hidden `<input id="securityToken">` value in the HTML file.

## 🔐 Security Architecture Bypassed

```
┌─────────────────────────────────────────────┐
│           Guardian v5 Secure                │
├─────────────────────────────────────────────┤
│  SHA-256 Bootloader Signature    → Bypassed │
│  AES-256-GCM Payload Encryption  → Forged  │
│  XOR Checksum Integrity          → Computed │
│  Zero-Width Steganography        → Encoded  │
│  History Array Length Validation  → Matched  │
│  XP/Time Heuristic Bounds        → Evaded   │
│  WPM Ceiling Check (≤350)        → Clamped  │
└─────────────────────────────────────────────┘
```

## 👨‍💻 Author

Created with love and curiosity by **Javed**.

- 🌐 Website: [iamjaved.site](https://iamjaved.site)
- 🐙 GitHub: [@iamjaved026](https://github.com/iamjaved026)

If you find this project fun or useful, please consider giving it a ⭐️ on GitHub!

---
*Disclaimer: This project was built for educational purposes and security auditing. Please use responsibly.*
