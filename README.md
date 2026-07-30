☀️ LiveCast Weather 3D
A real-time, living 3D ambient weather environment and Progressive Web App (PWA) engineered to act as a continuous, living dashboard. Designed to run as an ambient wallpaper on a secondary monitor or tablet, it translates live meteorological and astronomical telemetry into a dynamic 3D environment.

▶️ Watch the Engine Showcase & Real-Time Sunset Transition on YouTube

⚙️ The Engineering Architecture
This application was built under a strict self-imposed constraint: No heavy application frameworks (React/Vue/Angular), no build steps (Webpack/Vite), and no Node.js overhead. The environment functions from a single, standalone HTML file.

The architecture utilizes targeted tools managed entirely by a custom Vanilla JavaScript brain:

1. Chronological Rendering Engine (Pure Vanilla JS)
The core logic is 100% custom JavaScript. The engine continuously polls the Open-Meteo API for localized telemetry (latitude, longitude, and exact sunrise/sunset timestamps). It calculates the precise percentage of daylight remaining and physically interpolates this data into the DOM, shifting the ambient lighting and sky gradients millisecond by millisecond.

2. Astronomical Mathematics & 3D Environment (Three.js)
Rather than relying on static image toggles for "day" and "night," the celestial bodies and weather particles are driven by math and 3D rendering via the Three.js library.

The Sun & Moon: Physically track across the 3D viewport, accelerating naturally as they hit the horizon based on real-time sunset/sunrise data.

Weather Systems: Dynamic cloud rendering, rain vectors, and atmospheric lighting adapt instantly to the current local conditions.

3. High-Performance Glassmorphism UI (Tailwind CSS)
The data dashboard floating above the 3D space is styled using Tailwind CSS utility classes. By utilizing pure CSS backdrop-filters (backdrop-blur) and calculated drop-shadows, it achieves a frosted glass depth effect. This offloads visual heavy lifting to native CSS rendering, maintaining high performance and preventing system resource drain.

📊 Live Telemetry & Features
The dashboard pulls comprehensive, real-time data to update the environment continuously:

Atmospheric Data: Real-time Humidity, Dew Point, UV Index, Pressure, and Visibility.

Wind Dynamics: Live Wind Speed, Gusts, and Direction (visualized via a custom SVG compass).

Astronomical Tracking: Live Sunrise/Sunset countdowns with a dynamic daylight progress bar, plus Lunar Phase and Illumination tracking.

Forecasting: Today's Precipitation Chance/Amount, an interactive 7-Day Forecast, and a detailed Hourly Panel with dynamic canvas loops.

Timezone Handling: Automatic detection and calculation of the localized time and timezone abbreviations.

🛠️ Tech Stack
Core Logic & Architecture: Pure HTML5, CSS3, and Vanilla JavaScript (ES6+).

3D Rendering Pipeline: Three.js (imported via CDN).

UI Styling: Tailwind CSS (imported via CDN).

Telemetry Provider: Open-Meteo API.

🚀 Installation & Usage
Because the application is entirely self-contained with zero dependencies or build steps, it can run on any modern browser right out of the box.

Live Demo:
Visit the live PWA hosted on GitHub Pages: https://bruvic62.github.io/weather-diorama/

Run Locally:
Simply clone the repository and open index.html in your preferred browser (like Vivaldi) straight from your Linux terminal. No npm install or local server required.
