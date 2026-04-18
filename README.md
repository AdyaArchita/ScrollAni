# 🏎️ ItzFizz — Modern Car Experience

A premium, production-ready interactive hero section featuring a high-performance **GSAP-driven car scroll animation**. This project utilizes advanced front-end techniques to create a cinematic scrolling experience where a luxury sports car "paints" a neon headline onto the screen.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-accent)
![Tech](https://img.shields.io/badge/tech-GSAP%20%7C%20Tailwind%20%7C%20HTML5-green)

---

## ✨ Key Features

### 1. **Cinematic Scroll Journey**
The entire hero section remains pinned as you scroll, allowing the user to "drive" the car across the screen horizontally.

### 2. **Bidirectional "Neon Brush" Reveal**
As the McLaren 720S moves across the viewport, it acts as a light source that reveals the letters of the headline (**W E L C O M E   I T Z F I Z Z**). 
- **Forward Scroll**: Letters ignite with a neon glow as the car passes.
- **Reverse Scroll**: Letters dim back into darkness as the car moves backward, mimicking a live light projection.

### 3. **Fluid Typography & "Word-Lock" Layout**
Using `vw` (viewport width) units and atomic word-containers, the headline is guaranteed to never break or wrap incorrectly on any screen size, maintaining its premium impact from mobile to ultra-wide monitors.

### 4. **Modern Dashboard Metrics**
A glassmorphic footer containing impact statistics that:
- Count-up dynamically on page load.
- Staggered-reveal "one by one" as the user begins their scroll journey.
- Feature interactive hover states with neon highlighting.

### 5. **High-End Aesthetics**
- Deep dark theme (`#050505`) with a subtle interactive background mesh.
- Clean glassmorphism (`backdrop-filter`) for navigation and stat cards.
- Signature **Neon Lime** (`#def54f`) accents throughout.

---

## 🛠️ Technology Stack

- **Core**: HTML5, Vanilla JavaScript
- **Animations**: [GSAP 3.12.5](https://gsap.com/) (Core + ScrollTrigger)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) (CDN-based for single-file portability)
- **Typography**: [Outfit](https://fonts.google.com/specimen/Outfit) via Google Fonts
- **Assets**: High-resolution transparent car asset via GitHub Raw

---

## 🚀 Quick Start

Since this is a **single-file portable project**, there is no installation required.

1.  **Clone the repository** or download the `index.html`.
2.  **Open `index.html`** in any modern web browser (Chrome, Edge, or Safari recommended).
3.  **Scroll to drive** and experience the animation.

> [!TIP]
> For the best development experience, use the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code to see real-time changes.

---

## 📖 Under the Hood

The project relies on GSAP's `ScrollTrigger` to synchronize the `x` property of the car with the scroll progress. The "reveal" logic is calculated in the `onUpdate` callback:

```javascript
// Example Reveal Logic
if (carCenter > (letterRect.left + (letterRect.width * 0.15))) {
    letter.classList.add('reveal');
} else {
    letter.classList.remove('reveal');
}
```

---

## ⚖️ License

MIT License. Feel free to use this as a reference for your own high-end interactive projects.

---

**Developed with precision by the Antigravity AI team.**