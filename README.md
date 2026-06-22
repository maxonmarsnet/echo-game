# ECHO

A first-person **maze survival shooter** that runs entirely in the browser — one self-contained HTML file, no build step, no dependencies to install (Three.js loads from a CDN).

> Navigate a neon maze while a cast of goofy characters hunts you down. Listen for their footsteps closing in, turn the corner, and let 'em have it.

## Play

Open **`echo3d.html`** in a modern desktop browser (Chrome/Edge/Safari/Firefox). Click to lock the mouse and begin. **Sound on, headphones recommended** — enemy footsteps are directional.

`index.html` is the original 2D prototype of the same idea.

## Controls

| Input | Action |
|-------|--------|
| **WASD** | Move |
| **Mouse** | Look |
| **Hold Left-Click** | Fire (infinite ammo) |
| **Right-Click** | Scope zoom (after the bazooka is unlocked) |
| **Shift** | Dash |
| **Esc** | Pause (releases mouse) |
| **R** | Restart after Game Over |

## How it plays

- **Real-time survival.** Enemies hunt you continuously, navigating the maze via flow-field pathfinding.
- **Eat pellets** scattered through the corridors for points; **power pellets** make every enemy flee (slow + turn blue) for a few seconds.
- **The cast taunts you.** The moment a character comes into view, a comic speech bubble pops with its catchphrase; a name tag stays while it's on screen.
- **Enemy types:** fast chargers (red), ranged shooters (various colors), and a crowned boss every 3rd wave.
- **Progression:** shoot the central red brick (5 hits) to open a portal → Level 2 with two bosses → defeat them to unlock the **scoped bazooka** (splash-damage rockets).
- **High score** persists between runs (localStorage).

## Tech

- **Three.js** (ES module via CDN import map) with `EffectComposer` post-processing — bloom, chromatic aberration, vignette.
- **Cel-shaded (toon) art** with inverted-hull outlines.
- **Web Audio** — all sound effects synthesized in-code (gunshots, hits, footsteps with stereo panning by direction). No audio asset files.
- Single file: all HTML/CSS/JS in `echo3d.html`.

## Notes

The enemy characters are **original creations**. Rename or restyle the whole cast by editing the `CHARACTERS` array in `echo3d.html` (name, color, hat/accessory, catchphrase).

---

Built iteratively as a creative coding project.
