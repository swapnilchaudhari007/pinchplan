# PinchPlan – Hands-First Spatial Focus Desk

![WebXR](https://img.shields.io/badge/WebXR-Meta%20Quest-0467DF?logo=meta&logoColor=white) ![Three.js](https://img.shields.io/badge/Three.js-r169-black?logo=threedotjs&logoColor=white) ![hackathon](https://img.shields.io/badge/hackathon-Meta%20VR%20Start%202026-purple) [![demo](https://img.shields.io/badge/demo-live-success)](https://swapnilchaudhari007.github.io/pinchplan/) [![license](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

A seated, hands-first mixed-reality task board and focus timer for Meta Quest, built with WebXR + Three.js.
Entry for the Meta VR Start Developer Competition 2026 (Productivity track).

**Live demo:** https://swapnilchaudhari007.github.io/pinchplan/ — open it in the Meta Quest Browser and tap **Enter Mixed Reality**.

## Hand controls (no controllers needed)
- **Pinch** a card quickly → moves it to the next lane (Next up → Now → Done)
- **Pinch & drag** a card → move it between lanes / reorder
- Drag a card **below the board** → delete
- **Pinch the orb** → start / pause a focus session (5, 15 or 25 min)
- Turn your **left palm up** → wrist menu (add task, focus, clear done, recenter)

Controllers and mouse also work as fallbacks. Data is stored locally on the device.

## Tech
- WebXR `immersive-ar` (passthrough) with `hand-tracking`, falls back to `immersive-vr`
- Three.js r169, custom pinch / palm-up gesture detection from WebXR joint poses
- Single static `index.html`, hosted on GitHub Pages

## Run locally
```bash
python3 -m http.server 8000   # then open http://localhost:8000
```
WebXR needs HTTPS on a headset — use the GitHub Pages link above, or a tunnel such as `npx localtunnel --port 8000`.

## License
See [LICENSE](LICENSE).
