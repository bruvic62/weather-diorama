# 🌤️ 3D Live Weather Diorama & Ambient Wallpaper

A zero-dependency, single-file Progressive Web App (PWA) engineered to act as a continuous, living environment. This project is not a static webpage or a basic API widget; it is a real-time visual rendering engine built entirely from scratch using pure HTML, CSS, and Vanilla JavaScript.

Designed to be lightweight enough to run continuously as an ambient wallpaper on a secondary monitor or tablet, it translates live meteorological and astronomical telemetry into a dynamic, 3D-styled glassmorphism environment.

**📺 [Watch the Engine Showcase & Real-Time Sunset Transition on YouTube](https://youtu.be/95G5Tl7sW4c)**

---

## ⚙️ The Engineering Architecture

This application was built under a strict self-imposed constraint: **No heavy frameworks, no WebGL, no build steps, and zero external libraries.** ### 1. Chronological Rendering Engine
The environment does not simply toggle between "day" and "night" modes. The engine polls the [Open-Meteo API](https://open-meteo.com/) for localized telemetry (latitude, longitude, exact sunrise/sunset timestamps) and calculates the precise percentage of daylight remaining. This data is physically interpolated into the DOM, dynamically shifting the CSS hex codes of the sky gradient and ambient lighting millisecond by millisecond.

### 2. Astronomical Mathematics & Asset Layering
Instead of relying on heavy 3D models or dozens of static image files, the celestial bodies are driven by math and CSS manipulation:
* **The Sun:** Physically tracks across the viewport, accelerating naturally as it hits the horizon based on real-time sunset data.
* **The Moon:** The moon utilizes a single, static cropped image asset. The engine calculates the current astronomical lunar phase and applies dynamic CSS shading and layering directly over the image to accurately simulate the moon's phase and real-time movement across the night sky.

### 3. High-Performance Glassmorphism UI
The data dashboard floating above the 3D space was built using pure CSS backdrop-filters and calculated drop-shadows to achieve a frosted glass (glassmorphism) depth effect. By offloading the visual heavy lifting to native CSS rendering, the application maintains high performance without eating up system resources, preventing screen burn-in and battery drain.

---

## 📡 Tech Stack
* **Core:** Pure HTML5, CSS3, Vanilla JavaScript.
* **Architecture:** Standalone Progressive Web App (PWA).
* **Telemetry:** [Open-Meteo API](https://open-meteo.com/).

---

## 🚀 Installation & Usage
Because this is a pure, zero-dependency environment, installation is instant.

1. Clone this repository or download the source code.
2. Open `index.html` in any modern web browser.
3. The engine will initialize immediately.

---

## ☕ Support the Project
Thanks for downloading it. There is definitely no pressure for buying a coffee.

[![Buy Me A Coffee](https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png)](https://www.buymeacoffee.com/bruvic62)

---

## 📄 License
**PolyForm Noncommercial License 1.0.0**
<https://polyformproject.org/licenses/noncommercial/1.0.0>

### Acceptance
In order to get any license under these terms, you must agree to them as both strictly necessary and sufficient for your use of the work.

### Copyright License
The licensor grants you a copyright license for the duration of the copyright to do everything with the work that would otherwise infringe the licensor's copyright in it, with the following exceptions:

* You may not make the work available to others for commercial purposes, except as permitted under the "Limited Commercial Use" section below.

### Limited Commercial Use
You may make the work available to others for commercial purposes only if you have obtained a separate commercial license from the licensor.

### Notices
You must ensure that everyone who gets a copy of any part of the work from you also gets a copy of these terms or the URL for them above.

### No Other Rights
These terms do not allow you to sublicense or transfer any of your licenses to anyone else. These terms do not imply any other licenses, including any implied license to patents.

### Termination
If you violate any of these terms, your license ends immediately.

### No Liability
As far as the law allows, the work comes as is, without any warranty, and the licensor will not be liable to you for any damages arising out of these terms or the use or nature of the work, under any kind of legal claim.
