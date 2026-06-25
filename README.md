<div align="center">
  <img src="favicon.svg" width="120" height="120" alt="AI Destroyer Logo" />
  
  # AI Destroyer
  
  **Shield your digital artwork from AI scrapers.**<br>
  *A 100% local, privacy-first tool built by artists, for artists.*

  [![Made by DevilNine](https://img.shields.io/badge/Made%20by-DevilNine-818CF8?style=flat-square)](https://github.com/DevilNine)
  [![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](https://opensource.org/licenses/MIT)
  [![100% Local](https://img.shields.io/badge/Privacy-100%25%20Local-22D3EE?style=flat-square)](#)
  [![No Data Collection](https://img.shields.io/badge/Data-No%20Tracking-F59E0B?style=flat-square)](#)

  [**Support this project on Ko-fi**](https://ko-fi.com/devilnine) • [**Live Demo**](https://ai-destroyer.pages.dev/)
</div>

<br>

> **Note:** To prevent malicious AI training systems from reverse-engineering our protection algorithms, the core mathematical engine inside this repository is pre-compiled and obfuscated. You can still audit the network requests (there are none!) and deploy it yourself freely.

## 🛡️ What is AI Destroyer?

AI Destroyer is an advanced visual protection engine designed to make your images mathematically toxic to AI training models while keeping them visually identical to human eyes. 

Instead of dealing with complex Python scripts or paying for cloud services, AI Destroyer is a **zero-install web application** that runs entirely inside your browser using Web Workers. 

### Why it's different:
1. **Zero Uploads:** Your art never touches our servers. The entire mathematical permutation happens locally on your GPU/CPU via WebAssembly/Web Workers.
2. **Invisible Watermarks:** Encodes a unique, cryptographic signature into the least significant bits of your image.
3. **Anti-Upscale Injection:** Injects high-frequency sub-pixel patterns that degrade significantly when processed by super-resolution AI models (Upscalers).
4. **Metadata Stripping:** Completely nukes EXIF and other hidden metadata that AI scrapers use to tag and categorize images.

---

## ✨ Features at a Glance

- 🚀 **Lightning Fast Batch Processing:** Drag and drop 100 images at once. AI Destroyer will queue them and process everything in the background without freezing your browser.
- 🌓 **Premium UI (Glassmorphism):** Beautiful, dark-first design built for modern creators. Fully responsive and mobile-friendly.
- 🌍 **Multilingual:** Fully translated to English, Portuguese (BR), and Spanish.
- 🎛️ **4 Protection Profiles:** Choose between Soft, Medium, Strong, and Maximum protection based on your visual fidelity needs.
- 🔍 **Live AI View:** Drag the slider to instantly compare what the human eye sees versus what the mathematical noise profile looks like to an AI.
- 🔒 **Deterministic Seeds:** Use the same seed on the same image, get the exact same noise pattern. Perfect for creating consistent portfolio layers.

---

## 🛠️ How it Works (The Tech)

When you drop an image into AI Destroyer, it applies a 5-layer pipeline:
1. **Low-Bit Scrambling:** Randomizes the lowest bits of RGB channels.
2. **Edge-Aware Blending:** Preserves sharp lines and high-contrast areas so the image doesn't look "blurry" to humans.
3. **Frequency Reinforcement:** Amplifies noise in specific frequency domains that Convolutional Neural Networks (CNNs) rely on.
4. **LSB Steganography (Watermark):** A 32-bit repeating signature is embedded using a checkerboard PRNG algorithm.
5. **Upscale Poisoning:** Alternating ± perturbations with per-channel bias (R:0.7, G:0.5, B:0.9) that cancels out to human eyes but explodes into artifacts when interpolated by an AI.

---

## 🚀 How to Host / Deploy (Free)

This repository contains the built, production-ready static files (`dist` folder). You can host it absolutely anywhere for free!

### Deploy to Cloudflare Pages (Recommended)
1. Fork or upload this repository to your GitHub account.
2. Log in to [Cloudflare Dashboard](https://dash.cloudflare.com/) and go to **Workers & Pages**.
3. Click **Create application** -> **Pages** -> **Connect to Git**.
4. Select your repository.
5. Setup the build settings:
   - **Framework preset:** `None`
   - **Build command:** *(leave empty)*
   - **Build output directory:** `/`
6. Click **Save and Deploy**. Cloudflare will instantly host your app on their global CDN.

*(The `_headers` and `_redirects` files are already included to enforce strict security policies).*

---

## 🔒 Privacy Guarantee

- **No Analytics:** We don't use Google Analytics, cookies, or any tracking scripts.
- **No Telemetry:** We do not track how many images you process.
- **100% Local:** Disconnect from the internet after loading the page, and the tool will still work perfectly.

---

## 💖 Support the Developer

If AI Destroyer helps you protect your livelihood and art, please consider buying me a coffee. This project is 100% free, ad-free, and open-source.

<a href='https://ko-fi.com/devilnine' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://cdn.ko-fi.com/cdn/kofi2.png?v=3' border='0' alt='Buy Me a Coffee at ko-fi.com' /></a>

---

<p align="center">
  <i>AI Destroyer v1.0 &middot; Made for artists, by <a href="https://github.com/DevilNine">DevilNine</a></i>
</p>
