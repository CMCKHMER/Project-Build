# 🧱 BrickForge Pro — Build & Conquer

A Minecraft-style 3D voxel building game for schools, with **four game modes**:
a 20-level campaign, free building, teacher-assigned class projects, and live
team multiplayer. Students build trees, houses, bridges and castles
block-by-block, earn stars, and can build together in shared rooms.

**Live site:** https://cmckhmer.github.io/Project-Build/

## 🚪 Start Screen — Pick Your Mode

| Mode | What it is |
|---|---|
| 🏁 **Campaign** | 20 missions across 4 chapters — earn up to 60 stars |
| 🎨 **Free Build** | The whole workshop, every block, no budgets or timers |
| 📋 **Class Projects** | Builds assigned by a teacher: a brief, block budget & deadline |
| 👥 **Team Build** | Live shared world via room code — build together in 4 teams |

A 🏠 button in-game returns to the menu at any time (your build stays loaded).

## 🎮 Quick Start — Play Now (No Install)

1. Open the live site (or open `index.html` directly in any modern browser).
2. Pick a mode on the start screen — **Campaign → Level 1. First Tree** is the classic start.
3. Left-click the ground to place blocks. That's it — the first level teaches the rest.

Progress (stars, completed levels) is saved automatically in your browser.

## 🏆 Campaign

- **20 levels across 4 chapters** — Forest, City, Desert, Fantasy
- **3-star scoring**: finish fast, use your full block budget, keep a combo going
- **Boss build levels** at the end of each chapter
- **Sandbox mode** also unlocks after completing level 5 (or use Free Build from the menu anytime)
- Levels have a **time limit and block budget**; the timer starts only after you
  dismiss the mission brief, so reading the hint costs you nothing

## 📋 Class Projects (Teacher-Assigned)

- 6 built-in sample briefs: River Bridge, Khmer Temple (Wat), Stilt House,
  Dream Classroom, Floating Village (Tonlé Sap) and School Garden
- Each project runs on the campaign engine: brief card → budget & timer →
  star-scored results
- **Teachers post their own projects** from any Team Build room:
  *Classroom Control → Create Assignment → **Post to Class Projects***
  — title, description, requirements, due date, block budget and time limit
- Posted projects appear **live** for every student on the Class Projects screen
  (Firebase path `brickforge-projects`); samples work fully offline

## 👥 Team Build (Live Multiplayer)

1. Pick **Team Build** on the start screen, enter your name and pick a team
   (Mint, Amber, Sky or Coral).
2. **Create a room** (generates a 4-letter code) or **Join** with a shared code.
3. Everyone in the room builds in the same world — block places **and erases**
   sync live to all players.
4. The room pill (top-left) shows the code, your team and online count; click it
   for the **team roster** with per-team block totals.
5. Teachers tick *"I'm the teacher"* to get classroom controls: lock the room,
   clear all blocks, post room assignments / class projects, export progress.

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

## 🌐 Multiplayer Backend

Team Build and Class Projects sync through **Firebase Realtime Database**
(project `creative-minds-cambodia`, region `asia-southeast1`) — rooms live only
in the database, nothing to install on student devices. The game itself is
static and works on GitHub Pages; Campaign and Free Build run fully offline.

> Note: for room writes to succeed, publish `database.rules.json` in the
> Firebase Console → Realtime Database → Rules.

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
