# Audio Engine

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![Web Audio API](https://img.shields.io/badge/Web_Audio_API-000000?style=for-the-badge&logo=googlechrome&logoColor=white)

A high-performance, real-time generative audio visualizer built entirely in Vanilla JavaScript. It bridges the gap between digital math and physical sound, turning your system audio (Spotify, VLC, YouTube) into 30 distinct, customizable forms of reactive art rendered at 60FPS.

## ✨ Features

* **Real-Time Audio Capture:** Uses the Web Audio API and `getDisplayMedia` to capture live system audio or microphone input securely.
* **30 Generative Modes:** Features highly optimized mathematical rendering, including:
  * 🌌 *3D Hyperspace Drive & Rotating Galaxies*
  * 🧬 *DNA Helix & Sonic Phyllotaxis*
  * ⚡ *Plasma Lightning & Glitch City*
  * 🕶️ *Retro Synthwave & True Symmetrical Kaleidoscopes*
* **Dynamic Parameter Morphing:** A unified "Pro Customization" slider automatically adapts its function based on the active mode (e.g., controlling Star Size in Hyperspace mode, but Bar Width in Cyber Bars).
* **10+ Color Palettes:** Instantly switch between themes like *Cyberpunk*, *Vaporwave*, *Liquid Gold*, and *Blood Moon*.
* **Holographic Blending:** Drag and drop any custom background image. The engine uses advanced global composite operations (alpha-blending) to overlay the visuals like a hologram.
* **Graphite HUD:** A responsive, toggleable frosted-glass UI built with CSS backdrop-filters.

## 🚀 How to Run

This engine requires absolutely zero dependencies, build tools, or local servers.

1. Clone or download this repository.
2. Double-click the `visualizer.html` file to open it in any modern web browser (Chrome or Edge recommended for optimal system audio sharing).
3. Click **Capture System Audio**.
4. *Important:* When the browser prompts you to select a screen/tab, ensure you check the **"Share system audio"** or **"Share tab audio"** box at the bottom of the prompt.
5. Play your favorite track on Spotify, YouTube, or your desktop media player.

## 🧠 The Architecture

Instead of relying on heavy WebGL libraries like Three.js, this engine is optimized directly on the HTML5 `<canvas>` utilizing a 60Hz `requestAnimationFrame` loop.

* **Frequency Analysis:** It utilizes `AnalyserNode.getByteFrequencyData()` for equalizer-style rendering (bars, rings) and `getByteTimeDomainData()` for physical waveform representations (oscilloscopes).
* **Trail Buffering:** Cinematic glowing trails are achieved without heavy post-processing by drawing a highly transparent rectangle over the canvas every frame with the `destination-out` composite operation.

## 🎮 Controls & Customization

* **Sensitivity (Bounce):** Adjusts how violently the visuals react to amplitude spikes.
* **Smoothing (Lag):** Alters the `smoothingTimeConstant` of the Fast Fourier Transform, making the visuals either jittery and instantaneous or smooth and fluid.
* **Glow Blending:** Toggle between `Additive` (forces intersecting pixels toward pure white) or `Standard` blending.
* **Custom Background:** Use the file input to load a local image underneath the visualization layer.

## 🤝 Contributing

Feel free to fork this project and add your own mathematical rendering modes! To add a new mode, simply add a `<option>` to the HTML dropdown, define its dynamic slider label in the `modeCustomLabels` dictionary, and write the rendering logic inside the main `switch(mode)` statement within the `animate()` loop.

## 📜 License

Distributed under the GPL-3.0 License.
