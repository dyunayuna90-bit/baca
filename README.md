# Baca. Reader 📖

**Baca.** is a highly optimized, privacy-first Progressive Web App (PWA) engineered for a pure, distraction-free reading experience[span_1](start_span)[span_1](end_span). Built entirely on client-side technologies, it transforms your web browser into a powerful, offline-capable e-reader for PDF and EPUB documents[span_2](start_span)[span_2](end_span). 

No servers. No accounts. No data telemetry. Your books and reading data never leave your device[span_3](start_span)[span_3](end_span).

## 🧠 The Philosophy & Architecture
Unlike traditional cloud-based readers, **Baca.** relies entirely on your device's memory and local storage via IndexedDB (wrapper by localForage)[span_4](start_span)[span_4](end_span). 
* **For EPUBs:** It parses the OPF manifest and reconstructs the chapters and inline Base64 images directly in the DOM[span_5](start_span)[span_5](end_span).
* **For PDFs:** It uses a custom text-extraction algorithm via PDF.js. Instead of rendering heavy canvas images, it dynamically calculates line heights to reconstruct paragraphs and headings (H1/H2), discarding embedded images to give you a clean, unified text layout[span_6](start_span)[span_6](end_span).

## ✨ Comprehensive Feature Set

### 📚 Smart Library Management
* **Zero-Upload Processing:** Files are processed entirely in-browser. 
* **Persistent Storage:** Books, covers, reading progress (percentage and exact scroll position), and annotations are saved locally[span_7](start_span)[span_7](end_span).
* **Customizable UI:** Personalize your library grid with 4 different book card shapes (Dynamic, Rounded, Square, Leaf)[span_8](start_span)[span_8](end_span).
* **Metadata Editing:** Manually edit book titles and upload custom gallery images as book covers[span_9](start_span)[span_9](end_span).

### 📖 Advanced Reader Engine
* **Immersive Mode:** Full-screen reading capability with a hideable top UI bar[span_10](start_span)[span_10](end_span).
* **Auto-Generated TOC:** Automatically generates a Table of Contents by scanning for H1 and H2 nodes within the parsed document[span_11](start_span)[span_11](end_span).
* **In-Book Search:** Lightning-fast specific text search that highlights results contextually and offers smooth scrolling to the exact paragraph[span_12](start_span)[span_12](end_span).

### 🎨 Ultimate Customization (Material 3)
* **15 Dynamic Color Palettes:** Choose from Purple, Green, Rose, Blue, Orange, Teal, Yellow, Pink, Cyan, Slate, Red, Indigo, Lime, Sepia, or Monochrome[span_13](start_span)[span_13](end_span).
* **Adaptive Viewing Modes:** Switch seamlessly between Light, Dark, and true AMOLED (Pitch Black) modes[span_14](start_span)[span_14](end_span).
* **Typography Control:** Fine-tune font sizes, text alignment (left, center, justify), and choose from curated font families (Lora, Merriweather, Playfair, Inter, Space Mono)[span_15](start_span)[span_15](end_span).

### 🛠️ Interactive Reading Tools
* **Multi-Color Highlighting:** Select text and apply Yellow, Green, Pink, or Blue highlights[span_16](start_span)[span_16](end_span).
* **Personalized Notes:** Attach personal, editable text notes to specific highlights[span_17](start_span)[span_17](end_span).
* **Tanya AI / Wikipedia Lookup:** Highlight any word or phrase to fetch instant summaries using the free Wikipedia API[span_18](start_span)[span_18](end_span). Supports English and Indonesian languages, with a fallback search mechanism if an exact match isn't found[span_19](start_span)[span_19](end_span).

---

## 📸 Screenshots

<img width="1443" height="1522" alt="ResizedImage_2026-05-28_05-01-55_8292" src="https://github.com/user-attachments/assets/d1314cf0-0033-4a55-93f6-ac6f5ed93c4f" />

---

## 🚀 Quick Start

Since Baca. is a 100% client-side application, setup is instant.

1.  **Clone the repository:**
```bash
    git clone [https://github.com/yourusername/baca-reader.git](https://github.com/yourusername/baca-reader.git)
    ```
2.  **Run it locally:**
    Simply open the `index.html` file in any modern web browser.
3.  **Host it online:**
    Host this app for free using GitHub Pages, Vercel, or Netlify. Just deploy the root directory!

## 💻 Tech Stack

* **Frontend:** Vanilla HTML, JavaScript, [Tailwind CSS](https://tailwindcss.com/) (via CDN)
* **Icons:** [Lucide](https://lucide.dev/)
* **Document Parsing:** [PDF.js](https://mozilla.github.io/pdf.js/) (PDF) & [JSZip](https://stuk.github.io/jszip/) (EPUB)
* **Local Storage:** [localForage](https://localforage.github.io/localForage/) (IndexedDB wrapper)
* **APIs:** Public Wikipedia REST API

## 🤝 Contributing

Contributions are heavily encouraged and always welcome! 

Since this is currently a web-based PWA, **I am especially open to pull requests or forks from anyone willing to compile this into a native Android APK** (using tools like Capacitor, Cordova, or a custom Android WebView implementation). 

**How to contribute:**
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
