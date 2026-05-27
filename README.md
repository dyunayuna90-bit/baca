# Baca. | Offline Local Reader

**Baca.** is a lightweight, privacy-first Progressive Web App (PWA) designed for a distraction-free, personal reading experience. Built to run entirely offline, it turns your browser into a clean and customizable e-book library.

---

## 🚀 Key Features

* **100% Privacy & Offline**: All document processing happens locally within your browser. Your data never leaves your device.
* **Format Support**: Seamless reading for **PDF** and **EPUB** files.
* **PWA Capability**: Install it as a native app on your smartphone or desktop for a true full-screen reading environment.
* **Rich Customization**:
    * **Themes**: Multiple Material Design 3 palettes.
    * **Modes**: Light, Dark, and true pitch-black **AMOLED** mode.
    * **Typography**: Adjustable font sizes, text alignment, and a selection of curated serif, sans-serif, and mono fonts.
* **Smart Library**: Manage your collection with custom titles and cover image support.
* **Fluid Navigation**: Automatic Table of Contents (TOC) and in-book keyword search.

---

## 🛠 Tech Stack

* **Tailwind CSS**: For a modern, responsive UI.
* **PDF.js**: High-performance PDF rendering.
* **JSZip**: Efficient EPUB data extraction.
* **LocalForage**: Persistent local storage via IndexedDB.
* **Lucide Icons**: Clean, consistent iconography.

---

## 📥 Getting Started

1. Open the application in your browser.
2. Tap the **"+"** button in the bottom-right corner to upload a **PDF** or **EPUB** file.
3. Wait for the text extraction to complete.
4. Tap any book cover in your library to start reading.

> **Pro Tip:** For the best experience, open your browser menu (the three-dot icon in the top-right) and select **"Install App"** or **"Add to Home Screen"** to run it as a standalone application.

---

## ⚠️ Important Notes

* **PDF Handling**: This engine specializes in text extraction. Images within PDF files are ignored for performance and clarity.
* **EPUB Handling**: Fully supported, including illustrations and hierarchical structure.
* **Data Persistence**: Since data is stored in your browser's IndexedDB, please avoid clearing your browser cache if you wish to keep your library intact.

---

## 🛡 Privacy Policy

Privacy is our core value. **Baca.** has no backend, no analytics, and no external tracking. We do not collect, store, or transmit your files. Your reading collection stays yours.

---

*Built for those who value focus and simplicity.*
