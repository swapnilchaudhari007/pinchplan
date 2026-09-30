# PinchPlan – Hands-First Spatial Focus Desk

A seated, hands-first mixed-reality task board and focus timer for Meta Quest, built with WebXR + Three.js.
Entry for the Meta VR Start Developer Competition 2026 (Productivity track).

**Live:** open the GitHub Pages URL of this repo in the Meta Quest Browser and tap **Enter Mixed Reality**.

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
