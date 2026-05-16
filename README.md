<div align="center">

  <h1>☕ KofiType Signed Export Generator</h1>
  
  <p>
    <b>The ultimate v3.0 payload forger and security bypass tool for KofiType.</b>
  </p>

  <p>
    <a href="https://iamjaved.site"><img src="https://img.shields.io/badge/Made_with_❤️_by-Javed-d9a066?style=for-the-badge&logo=heart" alt="Made by Javed" /></a>
    <img src="https://img.shields.io/badge/Version-3.0-3b82f6?style=for-the-badge" alt="Version 3.0" />
    <img src="https://img.shields.io/badge/Status-Bypassed-10b981?style=for-the-badge" alt="Status" />
  </p>

</div>

---

## 🚀 Overview

The **KofiType Result Forger** is a custom security tool designed to analyze, test, and bypass the "Guardian v4 Secure" Bootloader integrity checks found in KofiType v3.

This tool allows you to generate mathematically perfect `.kofi` export files with custom statistics (WPM, XP, Level, Accuracy) that will pass seamlessly through the live site's newest security validations.

## ✨ Features

- **AES-GCM Encryption:** Fully replicates the live site's AES-GCM encryption logic. Derives the 32-byte master key dynamically from the `SECURITY_TOKEN`.
- **Zero-Width Steganography:** Automatically encodes the generated encrypted binary payload into invisible space characters (`\u200B` and `\u200C`). Your exported file will look completely blank in Notepad to perfectly mimic the real KofiType exports!
- **Advanced Heuristics Evader:** Auto-adjusts typing time, exact history array lengths, tests completed, and XP relationships to fly under the radar of server-side heuristic checks.
- **Glassmorphism UI:** A sleek, beautiful, dark-themed UI restored from V1, fully optimized for both desktop and mobile devices.
- **Interactive Loading:** Enjoy a fun, simulated 4-second hacking loading screen while your payload is forged and encrypted.

## 🛠️ Usage

1. Open `result_generator_v3.html` in any modern web browser.
2. Enter your desired custom statistics (Username, WPM, XP, etc.).
3. Click **Encrypt & Download .kofi File**.
4. Enjoy the interactive hacking screen while the payload is mathematically sealed and encrypted.
5. The file will automatically download once generation completes. Upload it to the live KofiType website!

> **Note:** The generator uses the default security token (`4100198909`) configured for `kofitype.vercel.app`. If the target server changes its source code, you can extract the new token by looking at the `__EXPECTED_SIGNATURE__` hex string in the target browser's Developer Console and calculating its integer value, then updating the hidden HTML input.

## 👨‍💻 Author

Created with love and curiosity by **Javed**.

- 🌐 Website: [iamjaved.site](https://iamjaved.site)
- 🐙 GitHub: [@iamjaved026](https://github.com/iamjaved026)

If you find this project fun or useful, please consider giving it a ⭐️ on GitHub!

---
*Disclaimer: This project was built for educational purposes and security auditing. Please use responsibly.*
