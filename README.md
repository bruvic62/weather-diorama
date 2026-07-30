# 🌤️ LiveCast Weather 3D

A single-file Progressive Web App (PWA) engineered to act as a continuous, living environment. This project is a real-time visual rendering engine built using pure HTML, CSS, and Vanilla JavaScript, paired with lightweight 3D and UI utilities.

Designed to be lightweight enough to run continuously as an ambient wallpaper on a secondary monitor or tablet, it translates live meteorological and astronomical telemetry into a dynamic, 3D-styled glassmorphism environment.

📺 [Watch the Engine Showcase & Real-Time Sunset Transition on YouTube](https://youtu.be/ftTTgyRl8m8)

---

## ⚙️ The Engineering Architecture

This application was built under a strict self-imposed constraint: **No heavy application frameworks (React/Vue/Angular), no build steps, and zero bloated package managers.**

### 1. Chronological Rendering Engine

The environment does not simply toggle between "day" and "night" modes. The custom Vanilla JS engine polls the [Open-Meteo API](https://open-meteo.com) for localized telemetry (latitude, longitude, exact sunrise/sunset timestamps) and calculates the precise percentage of daylight remaining. This data is physically interpolated into the DOM, dynamically shifting the ambient lighting millisecond by millisecond.

### 2. Astronomical Mathematics & 3D Environment

Instead of relying on static image files, celestial bodies and atmospheric weather effects are driven by real-time telemetry and Three.js rendering:

* **The Sun:** Physically tracks across the viewport, accelerating naturally as it hits the horizon based on real-time sunset data.
* **The Moon & Sky:** The engine calculates the current astronomical lunar phase and utilizes Three.js to accurately simulate the moon's movement, real-time cloud movement, and dynamic precipitation directly over the viewport.

### 3. High-Performance Glassmorphism UI

The data dashboard floating above the 3D space is styled using Tailwind CSS utility classes. By utilizing native CSS backdrop-filters and calculated drop-shadows to achieve a frosted glass (glassmorphism) depth effect, the application maintains high performance without eating up system resources, preventing screen burn-in and battery drain.

---

## 🛰️ Tech Stack

* **Core Logic:** Pure HTML5, CSS3, Vanilla JavaScript (ES6+).
* **Architecture:** Standalone Progressive Web App (PWA).
* **3D Environment:** Three.js (via CDN).
* **UI Styling:** Tailwind CSS (via CDN).
* **Telemetry:** [Open-Meteo API](https://open-meteo.com).
