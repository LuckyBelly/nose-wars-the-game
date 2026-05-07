# Nose Wars

**A browser game where kids practice their times tables by blasting boogers.** One HTML file. No build, no install, no dependencies.

[**Play it →**](https://luckybelly.github.io/nose-wars-the-game/)

---

## For parents and teachers

Nose Wars now has a **Times Tables Mode** designed to make multiplication practice feel less like homework and more like a reason to keep playing.

The pitch in one sentence: kids choose which times tables they want to work on, then play a normal action game where running out of ammo means they have to answer a multiplication question to keep going.

### Why it works

- **The math is the reward, not the punishment.** When ammo runs out, the game pauses and a multiplication question appears. Answering correctly reloads ammo, regenerates a heart, and unlocks an optional bonus round. Kids associate getting questions right with progress, not with a worksheet.
- **They pick their own tables.** On the start screen they tap which tables they want to practice (any combination of 2× through 12×, or "Mixed" for all of them). A child working on 7s can drill 7s. A class working through the term's targets can switch as they go.
- **Stakes that scale with confidence.** A correct answer earns a heart, then offers a *Try It* / *Skip* choice for a harder question. Get the hard one right, all hearts come back. Get it wrong, game over. Skipping is always free. The risk-reward decision is a real one and kids think hard about it.
- **A safety net for struggling moments.** If they lose all their hearts, they get up to **three revive attempts** per run — each one a hard question. This rewards persistence and turns "I died" into another practice rep instead of a frustrated exit.
- **Wrong answers cost something but don't end the run.** A wrong answer on a regular question costs one heart and reloads anyway. The correct answer is shown so they learn from the mistake. There's no shame loop.

### What the math looks like

- **Regular questions:** one factor from a chosen table, one factor between 1 and 12. Four multiple-choice answers, including plausible distractors (off-by-one-row mistakes, common errors). This is recognition-level practice.
- **Bonus and revive questions:** larger factors (typically 11–19 × 11–19, or a chosen table × 12–19). These are genuinely harder and meant to stretch kids who already feel solid on basics.

### Practical notes

- Works on phones, tablets, Chromebooks, and any modern browser. Mobile users get touch controls; desktop uses keyboard.
- No accounts, no sign-in, no data collection. Nothing leaves the device.
- A single round of Times Tables mode covers roughly 5–15 multiplication questions depending on how the kid plays. Easy to fit into a 10-minute session.
- The classic (non-math) game is still there for siblings who just want to play, or for warming up before practice.

---

## What is this

You pick a nose. You shoot boogers. You fight a Nosebleed Overlord. If you survive, you can plunge into a vertical Nose Dive scroller, run Endless mode, or play Flappy Nose through a forest of nose hairs.

Twelve characters, each with a different shot pattern that scales over five levels, and a different ult.

## Modes

| Mode | What it is |
|---|---|
| **Times Tables** | Pick your tables, pick a character, play with limited ammo. Math questions on empty. New. |
| **Classic** | Fight progressively harder waves through the Nosebleed Overlord boss. The original game. |
| **Endless** | Boss fights forever, scaling difficulty. Unlocked after beating the boss. |
| **Nose Dive** | Vertical scroller through the inside of a nostril. Unlocked after beating the boss. |
| **Flappy Nose** | Flappy Bird but with nose hairs. Unlocked after beating the boss. |

Times Tables Mode also has its own endless variant: clear the Nosebleed boss in math mode and you unlock an endless run with the math-reload system still active.

## Characters

| Nose | Style | Shot | Ultimate |
|---|---|---|---|
| **Nate** | Dad energy | Throws socks, slippers, sandwiches | DAD JOKE STORM |
| **Retts** | Verbal warfare | Letters → words → sentences | (try it) |
| **Calvin** | Iron lungs | Bouncing snot drops | Invuln rush |
| **Linus** | Stealth ninja | Silent shadow darts (homing at high levels) | VANISH (8s ghost mode) |
| **Beans** | Sleepy hound | Drool dart | PARK ZOOMIES |
| **Jane** | Quick hunter | Sleek tracking shots | (try it) |
| **Rodrigo** | Three eyes | Multi-angle stuff | Three-eyed form |
| **Max** | Lickin' & stickin' | Tongue lick → giant lick at Lv5 | MINI MAX ARMY |
| **Axel** | Apple thrower | Apples that stun → Lv5 adds APPLE PIE STUN | GINGER BOOMBOX |
| **Kirril** | Paranoid | Sneezes a spinning gun → Lv5 fires SCAM words | SCAM WAVE (timed booger explosions) |
| **Raheel** | Tank (extra heart!) | Big booger that grows every level | GOOFY BEAM (5s laser) |
| **Huntsman** | Patient hunter | Lingering spear (refreshes on hit) | SNIPER SHOT (aim, then charge) |

Plus a **Tutorial** card on the character select if you've never played before.

## Controls

**Desktop:**
- Arrow keys / WASD to fly
- SPACE to shoot (tap, no holding)
- E for ultimate
- P to pause

**Mobile:**
- Joystick (bottom-left) for thrust
- ◀ ▶ buttons (bottom-right) to turn
- FIRE button to shoot (one tap = one shot)
- ULT button for ultimate
- ⏸ in the top-right to pause

In Times Tables Mode, the math overlay covers the whole screen when ammo runs out, so accidental fire-button taps won't leak through.

## Running it locally

It's a single self-contained HTML file. You can just open it in a browser:

```bash
open index.html
```

Or if you want to serve it (which avoids some browser `file://` quirks):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/
```

No build step. No npm install. No dependencies.

## Deploying to GitHub Pages

The repo is already set up: the game lives in `index.html` at the root, and GitHub Pages serves it automatically at the repo URL.

To deploy your own fork or copy:

1. Push the repo to GitHub with `index.html` at the root
2. Settings → Pages → Source: Deploy from a branch → `main` → `/` (root)
3. Wait ~1 minute, your URL will be `https://<your-username>.github.io/<repo-name>/`

## Save data

The game uses `localStorage` to remember:

- `nw_flappy_best` — your best Flappy Nose score

That's the only thing it persists. Clearing site data resets it. Times Tables Mode does not store progress between sessions; each run is fresh.

## Tech

- Vanilla JavaScript, single HTML file
- Canvas 2D for everything (no WebGL)
- Mobile-friendly: responsive canvas, touch controls, meta viewport tag
- ~8,000 lines of code, ~325 KB on disk

## Known limits / things to try

- Tuning is rough — ammo size, durations, damage values, and ult costs are first-pass guesses. Play around with them.
- Tutorial uses Nate as the default. If you want to learn with a specific nose, that's a future addition.
- The Nosebleed Overlord is the only boss in classic mode (Endless rotates through more variants).
- Times Tables ammo is currently 8 shots between questions. Easy to bump up or down — search for `TT_AMMO_MAX` in `index.html`.
- Bonus and revive questions currently draw from a fixed hard range (11–19 × 11–19). If you want a softer curve, that's a one-line change.

## Credits

Built collaboratively with Claude. Every nose drawn from scratch in canvas, every ult tuned over a lot of back-and-forth, every multiplication distractor written to mimic an actual mistake a kid would make.
