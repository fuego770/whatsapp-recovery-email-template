# WhatsApp Account Recovery - Support Template Assistant

A minimalist, mobile-responsive web utility designed to assist users in recovering compromised WhatsApp accounts. This tool generates a pre-formatted, standardized incident report template that can be copied to the device clipboard with a single tap, satisfying strict mobile security sandboxes across Android, iOS, and desktop browsers.

## 🚀 Live Demo
The application is deployed using GitHub Pages. You can access the live tool here:
👉 **[fuego770.github.io/whatsapp-recovery-email-template](https://fuego770.github.io/whatsapp-recovery-email-template/)**

## 📱 Features
* **Cross-Platform Support:** Fully optimized to bypass Mobile Safari (iOS) and Chrome (Android) security restrictions regarding clipboard access.
* **Single-Tap Copy:** Replaces manual drag-and-select highlighting with a clean, programmatic clipboard injection interface.
* **Zero Overhead:** Built purely with semantic HTML5, CSS3, and Vanilla JavaScript—no external frameworks, dependencies, or tracking cookies.

## 🛠️ How It Works (The iOS Safari Workaround)
Modern mobile engines (specifically WebKit/Safari) block programmatic clipboard execution (`document.execCommand('copy')` or `navigator.clipboard.writeText`) if they suspect background scripting or if elements are hidden (`display: none` or `opacity: 0`). 

To guarantee compliance, this tool leverages a `contenteditable` container directly inside the visible viewport layout. Upon firing the touch gesture listener, the script temporarily manipulates element permissions to secure a legitimate user-space selection context, copying the text instantly without visual flickering.

## 📦 Deployment Instructions
If you want to host your own instance of this tool:
1. Clone or fork this repository.
2. Ensure `index.html` resides in your root working directory.
3. Head to repository **Settings -> Pages**.
4. Set the build source to deploy from the **main** branch root (`/`).
5. Link the generated deployment URL to a custom QR Code for quick physical distribution.
