# Verdure World Editor

**A browser‑based, game‑agnostic authoring tool for point‑and‑click adventure games.**  
Design scenes, entities, dialogs, and HUDs – then export a complete, deployable HTML5 game (PWA + offline support).

![Editor screenshot](docs/screenshot.png)   <!-- add a real screenshot later -->

---

## ✨ Features

- **Visual scene editor** – place entities, draw masks/hotspots, set entry points (Konva.js)
- **Node‑based dialog editor** – branching trees with conditions & effects (Drawflow)
- **Entity state machine** – each entity has states, animations, timers, and interactions
- **Fully configurable HUD** – no hardcoded elements; define stats, bars, inventory, currency
- **Asset management** – upload sprites, backgrounds, audio; used by reference, not base64
- **Live save & play‑test loop** – writes JSON directly to disk (File System Access API)
- **One‑click export** – a zip containing the game engine, assets, and data
- **Progressive Web App** – the exported game includes a manifest + service worker for offline play

---

## 🧱 Tech Stack

| Area             | Technologies                                                                 |
|------------------|------------------------------------------------------------------------------|
| Editor frontend  | HTML5, CSS3, JavaScript (ES2020), Konva.js, Drawflow                        |
| Game engine      | Vanilla JS, no frameworks – runs in any modern browser                      |
| Storage          | File System Access API (edit mode) + localStorage (save games)              |
| Build / deploy   | No build step – plain static files, exported as zip                         |
| PWA              | Service Worker (cache‑first), Web App Manifest                              |
| Ads (optional)   | AdMob rewarded & interstitial (only when hosted on HTTPS)                   |

---

## 🚀 Getting Started (for developers / game designers)

### Prerequisites
- **VS Code** with **Live Server** extension (or any local static server)
- **Chrome** or **Edge** (required for File System Access API – Firefox can only preview)

### Clone & run
```bash
git clone https://github.com/your-username/verdure-world-editor.git
cd verdure-world-editor
