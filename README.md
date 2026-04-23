# ⚡ Hogwarts — An Interactive 3D Experience

A fully interactive Harry Potter world built with Three.js. Explore 4 iconic Hogwarts rooms in your browser — no game engine, no install, just open `index.html`.

live demo : https://hogwartexplorer.netlify.app

## 🏰 Rooms

| Room | File | Size |
|------|------|------|
| Transfiguration Classroom | `transfiguration_class.glb` | 0.9 MB |
| The Great Hall | `hogwarts_grand_hall.glb` | 1.5 MB |
| Gryffindor Common Room | `gryffindor_common_room.glb` | 10.8 MB |
| Dumbledore's Office | `dumbledores_office.glb` | 15.1 MB |



## 📁 File Structure

```
hogwarts-world/
├── index.html                    ← entire app (66KB)
├── transfiguration_class.glb     ← 0.9MB
├── hogwarts_grand_hall.glb       ← 1.5MB
├── gryffindor_common_room.glb    ← 10.8MB
├── dumbledores_office.glb        ← 15.1MB
└── README.md
```

All GLBs must be in the **same folder** as `index.html`.

---

## 🎮 Controls

### Desktop
| Action | Control |
|--------|---------|
| Look around | Click + drag |
| Walk forward/back | W / S or ↑ ↓ |
| Strafe left/right | A / D or ← → |
| Zoom | Scroll wheel |
| Interact / cast spell | Click on object |

### Mobile
| Action | Control |
|--------|---------|
| Look around | Single finger drag |
| Zoom | Pinch |
| Interact | Tap |
| Cast spell | Tap object |

---

## ✨ Features

- **4 fully explorable 3D rooms** — navigate between rooms via the Marauder's Map
- **Sorting Hat quiz** — get sorted into your Hogwarts house on first visit
- **Hedwig's Theme** — synthesised entirely via Web Audio API (no audio files)
- **Per-room ambient music** — each room has its own atmospheric drone
- **Spell interactions** — click objects to cast spells with particle effects and sounds
  - 🔥 Incendio — fireplace roars, lights pulse
  - ✨ Lumos — C major chord, blinding light flash
  - 💚 Floo Network — green particle explosion, emerald lights
  - 🎙️ Portraits — Web Speech API reads quotes in a British accent
  - 🪄 Levitate, Reveal, Transform — object animations
- **First-person camera** — drag to look, position never clips through walls
- **Room boundary system** — invisible walls keep you inside every room
- **Mobile responsive** — works on phones from 320px wide, safe-area aware for notched phones

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| Three.js r128 | 3D engine |
| GLTFLoader + DRACOLoader | Load & decompress GLB files |
| GSAP 3 | Animations & transitions |
| Web Audio API | All music & sound (no audio files) |
| Web Speech API | Portrait voices |
| Google Fonts (Cinzel + Crimson Text) | Typography |

Zero paid APIs. Zero build tools. Zero audio files. Single HTML file.

---

## 📦 GLB Compression

The GLB files in this repo are Draco-compressed (60–80% smaller than originals). If you want to compress your own:

```bash
npm install -g gltf-pipeline
gltf-pipeline -i your_room.glb -o your_room_compressed.glb --draco.compressionLevel 7
```

---

## 🏗️ Built With

Phases:
1. **Foundation** — Draco compression, Three.js skeleton, loading screen, Sorting Hat
2. **Interactions** — Hedwig's Theme, spell system, per-room music, mobile gestures, first-person camera

---
all credits to the owners of glb
*Made with ⚡ and a lot of Polyjuice Potion*
