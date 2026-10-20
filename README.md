# 🧱 BrickForge Pro — Build & Conquer

A Minecraft-style 3D voxel building game with a **20-level campaign** for schools.
Students build trees, houses, bridges and castles block-by-block, earn stars,
unlock Sandbox mode, and can optionally build together in shared multiplayer rooms.

**Live site:** https://cmckhmer.github.io/Project-Build/

## 🎮 Quick Start — Play Now (No Install)

1. Open the live site (or open `index.html` directly in any modern browser).
2. Pick **Level 1. First Tree** from the Forest chapter and press **▶ Start Building**.
3. Left-click the ground to place blocks. That's it — the first level teaches the rest.

Progress (stars, completed levels) is saved automatically in your browser.

## 🏆 Campaign

- **20 levels across 4 chapters** — Forest, City, Desert, Fantasy
- **3-star scoring**: finish fast, use your full block budget, keep a combo going
- **Boss build levels** at the end of each chapter
- **Sandbox mode** unlocks after completing level 5 — free building with all blocks
- Levels have a **time limit and block budget**; the timer starts only after you
  dismiss the mission brief, so reading the hint costs you nothing

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `B` | Build tool (default) |
| `E` | Erase tool |
| `R` | Rotate block |
| `Ctrl+Z` | Undo |
| `Ctrl+Y` | Redo |
| `Ctrl+S` | Save scene (opens save modal) |
| `T` | Toggle toolbar |
| `G` | Toggle grid snap |
| `P` | Screenshot (PNG) |
| `M` | Mute sounds |
| `N` | Day/night cycle |
| `F` | Toggle fog |
| `?` | Help modal |
| `Esc` | Confirm-abandon a level / close dialogs |
| Left-drag | Place / erase (tool-dependent) |
| Right-drag | Rotate camera |
| Middle-drag | Pan camera |
| Wheel | Zoom camera |

On phones/tablets: one finger rotates the camera, the toolbar places blocks,
and all menus scroll normally.

## 👥 Multiplayer Classroom (Optional)

The core campaign is fully offline. For shared building rooms:

1. **Start the WebSocket server** (any machine on the school network or a small VPS):
   ```bash
   npm install
   npm start        # serves on PORT 3000 by default
   ```
2. Open the site, click **Join Room** in the multiplayer dialog.
3. Teachers enter a name, pick **Teacher**, create a room and share the 6-char code.
4. Students pick **Student**, enter the code, and build together in real time.
5. Teachers can post assignments, lock/unlock the room, and monitor progress.

Multiplayer sync runs on **Firebase Realtime Database** (project
`creative-minds-cambodia`, region `asia-southeast1`). Rooms live only in the
database — nothing to install on student devices.

> Note: the game itself is static and works on GitHub Pages; only the
> multiplayer room sync needs the Firebase project (already configured).

## 🖥️ System Requirements

- A modern browser with WebGL (Chrome/Edge/Firefox/Safari)
- No build step, no dependencies to install for single-player

## 🗂️ Project Structure

```
Project-Build/
├── index.html      # The entire game (single file, self-contained)
├── server.js       # Optional WebSocket relay for local multiplayer
├── public/         # Static assets
├── src/            # Legacy Next.js prototype (not used by the deployed game)
└── README.md
```

## 🔒 Privacy & Safety

- No accounts, no personal data collection — progress stays in the browser's
  `localStorage`; multiplayer rooms only store display names and block data
- Teacher controls: room locking, clearing blocks, assignment posts

## 📜 License

MIT — free for educational use.

---

**Built for classrooms. Place your first block in 10 seconds.** 🎓
