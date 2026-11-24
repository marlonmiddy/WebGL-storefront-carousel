# WebGL-storefront-carousel
# 🛍️ WebGL Curved Glass Storefront Carousel

A mobile-first, zero-cost (**R0**) e-commerce showcase featuring an interactive **WebGL Distortion Carousel** with barrel lens warping, velocity-based chromatic aberration (RGB split), category filtering, and a carousel-to-grid view switcher.

Built and deployed 100% on **iPhone 15** using **GitHub** and **GitHub Codespaces (VS Code)**.

---

## ✨ Key Visual & UX Features
* **Curved Glass Distortion:** Custom GLSL fragment shader that bends product textures outward during swipe momentum.
* **Chromatic Aberration:** Dynamic Red/Green/Blue edge separation scaled by touch velocity.
* **iPhone-Native Touch Physics:** Smooth `lerp` inertia scrolling, magnetic center-card snapping, and Safari gesture locking (`touch-action: none`).
* **HUD & Micro-Details:** Fixed center corner crosshairs (`+`), dynamic product caption updates (Title + Price in **ZAR**), category filter pills, and a Carousel/Grid layout toggle.

---

## 🛠️ R0 Tech Stack & Workflow
* **IDE:** GitHub Codespaces (Browser VS Code on iPhone 15 Safari)
* **VS Code Extensions:** 
  * `Live Server` (Local port forwarding for real-device Safari testing)
  * `Shader languages support` (GLSL syntax highlighting)
* **Core Engine:** Vanilla HTML5, CSS3, ES Modules, and **Three.js** (loaded via CDN Import Map—zero build tools or `npm` overhead)
* **Hosting:** GitHub Pages (Free HTTPS static hosting from `main` branch)

---

## 📂 Planned Project Structure
```text
├── index.html        # App shell, safe-area HUD, filter tabs, & import map
├── style.css         # Mobile-first styling, Dynamic Island safe areas, & grid view
├── app.js            # Three.js scene, GLSL shaders, touch physics, & product catalog
├── assets/           # Compressed product imagery (WebP/JPEG < 200KB)
└── README.md         # Project blueprint & roadmap
```

---

## 🗺️ 5-Stage Development Roadmap

- [ ] **Stage 1: Workspace & R0 Setup**
  - Create public GitHub repo and launch 2-core Codespace.
  - Set Codespaces idle timeout to 15 minutes to preserve free monthly hours.
  - Install `Live Server` and `Shader languages support` extensions.
- [ ] **Stage 2: Mobile-First UI Shell**
  - Configure iPhone 15 viewport safe areas (Dynamic Island & home bar).
  - Build ambient radial backdrop, center `+` focus crosshairs, top category bar, and bottom product HUD.
- [ ] **Stage 3: WebGL Engine & Distortion Shader**
  - Initialize Three.js camera tuned for portrait mobile aspect ratios.
  - Write vertex & fragment shaders for barrel distortion and RGB color split.
  - Implement infinite horizontal card wrapping.
- [ ] **Stage 4: Touch Physics & Storefront Logic**
  - Tune thumb-drag inertia, center snapping, and raycast tap-to-open detection.
  - Wire up category filtering and Carousel ↔ Grid view switching.
  - Optimize product images for fast loading on mobile data.
- [ ] **Stage 5: Device Testing & GitHub Pages Launch**
  - Test live touch responsiveness via Codespaces forwarded port in Safari.
  - Commit via VS Code Source Control and publish live via GitHub Pages.

---

## 📱 Mobile Development Notes
* **Codespaces Hours:** Always stop the active Codespace via the bottom-left VS Code status bar when ending a session.
* **Asset Budget:** Keep individual product images under `200KB` (`600x800px` portrait) to ensure instant GPU texture uploads and smooth 60fps performance on mobile networks.
