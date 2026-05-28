# Baca. — Zero-Friction Local E-Book Reader

A brilliant, self-contained **single-file Progressive Web App (PWA)** engineered for deep reading, distraction-free literacy, and immediate contextual research. 

`Baca.` (Indonesian for *Read*) strips away the over-engineered bloat of modern e-readers. No logins, no cloud tracking, no paywalls, and absolutely no configuration friction. Just open your file, and start reading.

---

## 📸 Screenshots
<img width="2166" height="1524" alt="ResizedImage_2026-05-28_11-03-21_4025" src="https://github.com/user-attachments/assets/bd443545-b7f1-4fc4-8087-04b6c9980943" />

<!-- Placeholders for your assets -->
<!-- <p align="center">
  <img src="your-screenshot-library.png" width="45%" alt="Library View" />
  <img src="your-screenshot-reader.png" width="45%" alt="Reader View" />
</p> -->

---

## ⚡ What Makes It Unique? (The Philosophy)

* **Zero-Friction Access:** No complex directory mapping or painful file trees (unlike Moon+ Reader). It leverages native OS file pickers to import files directly into your local database.
* **True PDF Text-Reflow (Anti Pinch-to-Zoom):** Reading standard PDFs on mobile screens is usually a nightmare. `Baca.` forcefully extracts pure text spatial coordinates and rebuilds them into dynamic responsive HTML blocks (`<p>` and `<h1>`). Scroll vertically, adjust fonts, and read naturally.
* **Contextual AI & Dictionary Overlays:** Encounted a complex academic term or historical figure? Simply highlight the text. `Baca.` fetches real-time breakdowns from Wikipedia, Wiktionary, and the public Dictionary API instantly without breaking your reading momentum.
* **The "Frankenstein" Single-File Architecture:** UI layers, Material Design 3 theme engines, custom PDF/EPUB parsers, and local database management are all rolled into **one single `.html` file**. It runs entirely in-memory with zero compilation or build steps needed.

---

## 🛠️ Technical Deep Dive

* **PWA Self-Infection (Blob Trik):** Bypasses traditional server requirements by compiling standard PWA `manifest.json` and `service-worker.js` files *on-the-fly* via JavaScript **Blob Objects** directly inside the RAM.
* **Massive Local Database (IndexedDB):** Bypasses the strict 5MB `localStorage` limit by hijacking **IndexedDB** through `localForage`. You can safely store dozens of heavy books entirely offline.
* **Smart Rendering (Intersection Observer):** Even a 1,200-page book runs smoothly. The DOM doesn't render thousands of paragraphs at once; it dynamically mounts and updates page progression indexes based on exactly what is visible on your screen.

---

## ⚠️ Known Limits (By Design)
* **Pure Text Focus:** This engine is explicitly optimized for literature and text-heavy books. Images inside PDFs are skipped to optimize RAM overhead and maximize text-reflow responsiveness.
* **No Scanned Images / OCR:** PDFs containing raw image scans will trigger a graceful warning notification. `Baca.` is built for pure typography, not heavy machine learning OCR scanning.

---

## 🤝 Open for Contributions & APK Porting (Call to Action!)

This project is fully open-source and welcoming of all optimizations. 

### 🚀 The Big Goal: Native APK Packaging
We are looking for mobile developers to help wrap this single-file HTML app into a native **Android APK** (via **Capacitor**, **Trusted Web Activity (TWA)**, or **Cordova**).

**Crucial Issue to Solve:** Android OS aggressively wipes WebView caches and IndexedDB structures when a phone's storage runs low. We need contributors to help implement a native bridge plugin to duplicate the `localForage` binaries directly into the secure physical local Android directory instead of relying solely on the browser's volatile storage box.

If you love clean code, minimalist software architecture, or want to build a bulletproof Android wrapper for this, feel free to fork, optimize, and submit a Pull Request!

---

## 📄 License
MIT License. Completely free to use, modify, and redistribute. Built with absolute logic.
