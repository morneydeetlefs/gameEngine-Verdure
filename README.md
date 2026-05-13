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

Open the project folder in VS Code.
Right‑click editor/index.html → Open with Live Server.
The editor will ask you to select a project folder – choose the same gameEngine-Verdure folder (this gives read/write permission).

Start building your game
Upload assets (sprites, backgrounds, audio) in the Assets tab.

Configure game metadata, player stats, and HUD in the Game tab.

Create entity templates (plants, NPCs, tools, portals) in the Entities tab.

Write dialog trees in the Dialogs tab (visual node graph).

Build scenes with backgrounds, placed instances, masks, and hotspots in the Scenes tab.

Press Ctrl+S to save – the game tab (if open) reloads automatically.

Click Export Zip to get a deployable package.

📁 Project Structure (highlights)

gameEngine-Verdure/
├── editor/                # The editor itself (index.html + js/css)
├── game/                  # The game engine (what players run)
├── shared/                # renderer.js + animations.js (used by editor preview & game)
├── data/                  # All game JSON (game.json, entities.json, scenes/, dialogs/)
├── assets/                # User‑uploaded images and audio (sprites/, backgrounds/, audio/)
├── minigames/             # Optional custom mini‑game HTML files
├── manifest.json          # PWA manifest (filled during export)
├── sw.js                  # Service worker (filled during export)
└── EDITOR_HELP.html       # Complete built‑in documentation

🧠 Architecture (what this project demonstrates)
File System Access API – the editor reads/writes real files on disk, no “download JSON” workflow.

Separation of concerns – editor UI, game engine, and shared renderer are independent.

State persistence – game saves use localStorage; entity timers survive browser restarts.

Event‑driven effects system – all interactions, dialogs, and timers trigger composable effects (set_state, give_item, play_sfx, transition_scene, etc.).

Condition system – interactions and dialog choices can be gated by flags, inventory, stats, or online status.

Visual tooling – canvas‑based scene editor + node‑based dialog editor, both with live preview.

Progressive Web App – the exported game is installable and works offline after first load.

📦 Export & Deployment
When you click Export Zip, the editor packages:

All data/*.json (game config, entities, scenes, dialogs)

All assets/ files (sprites, backgrounds, audio)

The full game/ folder (engine, css, js)

The shared/ folder

manifest.json and sw.js (configured for your game ID)

A minigames/ folder if present

You can then extract the zip and upload the contents to any static web host:

GitHub Pages – push to a repo, enable Pages

Netlify – drag & drop the folder

Vercel – vercel --prod

HTTPS is required for service worker and ads.
The game is fully functional offline after the first load.

🔗 Links
Live Demo (GitHub Pages) – morneydeetlefs.github.io/gameEngine-Verdure

Repository – github.com/morneydeetlefs/gameEngine-Verdure

Documentation – see EDITOR_HELP.html in the repo

👤 About this project (for prospective employers)
This is a pet project I built to explore:

Building a complex, stateful web application without a framework (vanilla JS)

Integrating third‑party canvas libraries (Konva, Drawflow) into a cohesive UI

Designing a data‑driven game engine that reads plain JSON

Implementing a full authoring workflow (asset management, visual editing, real‑time save)

Creating a production‑ready export that includes PWA features

The code is modular, self‑documenting, and follows consistent naming conventions.
I focused on developer experience (Live Server integration, instant save‑reload) and user experience (offline support, installability, responsive HUD).

📄 License
MIT – feel free to use, modify, and learn from it.

🙌 Acknowledgments
Konva.js – canvas scene editing

Drawflow – node‑based dialog editor

JSZip – client‑side zip export

Built with ☕ and a love for adventure games.


---




git clone https://github.com/morneydeetlefs/gameEngine-Verdure.git
cd gameEngine-Verdure
