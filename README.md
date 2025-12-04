# QR On-Site

<a href="https://winter-of-open-source.vercel.app/"><img src="https://raw.githubusercontent.com/datavorous/tinytracer/main/media/banner.png"></a>

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

**QR On-Site** is a web-based QR Code Scanner and Generator built from scratch without external QR libraries.

This project is part of **[Winter of Open Source](https://winter-of-open-source.vercel.app/)**, where contributors learn to implement QR code encoding/decoding algorithms from the ground up, understand error correction, and build a fully functional QR code tool.

## Web Interface

<!-- Add your screenshots here -->
<p align="center">
  <img src="assets/screenshots/image.png" alt="QR Generator Demo" width="400">
  <!-- <img src="assets/screenshots/scanner-demo.png" alt="QR Scanner Demo" width="400"> -->
</p>


## Current Status

| Feature | Status | Details |
|---------|--------|---------|
| **QR Generator** | 🟡 Partial | Version 2, Medium error correction only (hardcoded) |
| **QR Scanner** | 🔴 Placeholder | UI exists, logic needs to be implemented |
<!-- | **Responsive UI** | 🟢 Complete | Works on desktop and mobile | -->

### What Needs To Be Done

**Generator Improvements:**
- [ ] Support for multiple QR versions (currently only Version 2)
- [ ] Configurable error correction levels (L, M, Q, H)
- [ ] Dynamic version selection based on data length
- [ ] Support for different encoding modes (numeric, alphanumeric, byte, kanji)

**Scanner Implementation:**
- [ ] Image processing to detect QR codes
- [ ] Finder pattern detection algorithm
- [ ] Perspective correction for tilted QR codes
- [ ] Data extraction and decoding logic
- [ ] Error correction decoding (Reed-Solomon)

## Features

- **QR Code Scanner** - Upload images to decode QR codes *(needs implementation)*
- **QR Code Generator** - Create QR codes from text input *(Version 2-M only)*
- **No External Libraries** - Built from scratch for learning
- **Responsive Design** - Works on desktop and mobile

## Demo

Visit the live demo: [QR On-Site](https://qr-on-site.vercel.app)

## Installation

```bash
git clone https://github.com/ConsoleCzar-2/qr-on-site.git
cd qr-on-site

# Open directly in browser
# Just open index.html in your browser

# Or use a local server (recommended)
python -m http.server 8000
# Then visit http://localhost:8000
```

## How to Contribute

We need contributors to help complete this project! Check out [CONTRIBUTING.md](CONTRIBUTING.md) for:
- Learning resources (10-part QR code tutorial series)
- Setup instructions
- Contribution guidelines and points system

Browse [Open Issues](https://github.com/ConsoleCzar-2/qr-on-site/issues) to find tasks labeled by difficulty and component.

> [!IMPORTANT]
> **Do NOT use external QR libraries.** The goal is to implement everything from scratch!

## Code of Conduct

Please follow [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) to ensure a welcoming and productive environment for all contributors.

---

<p align="center">
Made with ❤️ by <a href="https://github.com/ConsoleCzar-2">ConsoleCzar</a>
</p>
