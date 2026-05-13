# 🍃 Verdure World Editor

**A browser‑based, game‑agnostic authoring tool for point‑and‑click adventure games.**  
Design scenes, entities, dialog trees, and HUDs – then export a complete, deployable HTML5 game (PWA + offline support).

[![Live Demo](https://img.shields.io/badge/Live%20Demo-View%20Project-2ea44f?style=for-the-badge&logo=github)](https://morneydeetlefs.github.io/gameEngine-Verdure/)
[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

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

## 🚀 Getting Started

### Prerequisites
- **VS Code** with **Live Server** extension (or any local static server)
- **Chrome** or **Edge** (required for File System Access API – Firefox can only preview)

### Clone & run

```bash
git clone https://github.com/morneydeetlefs/gameEngine-Verdure.git
cd gameEngine-Verdure
