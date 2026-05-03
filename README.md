Nose Wars
A browser game about noses, boogers, and questionable life choices. One HTML file. No build, no install, no dependencies.

Play it →

Replace YOUR-USERNAME above with your GitHub username once Pages is live.

What is this
You pick a nose. You shoot boogers. You fight a Nosebleed Overlord. If you survive, you can plunge into a vertical Nose Dive scroller, run Endless mode, or play Flappy Nose through a forest of nose hairs.

Eleven characters, each with a different shot pattern that scales over five levels, and a different ult.

Characters
Nose	Style	Shot	Ultimate
Nate	Dad energy	Throws socks, slippers, sandwiches	DAD JOKE STORM
Retts	Verbal warfare	Letters → words → sentences	(try it)
Calvin	Iron lungs	Bouncing snot drops	Invuln rush
Linus	Stealth ninja	Silent shadow darts (homing at high levels)	VANISH (8s ghost mode)
Beans	Sleepy hound	Drool dart	PARK ZOOMIES
Jane	Quick hunter	Sleek tracking shots	(try it)
Rodrigo	Three eyes	Multi-angle stuff	Three-eyed form
Max	Lickin' & stickin'	Tongue lick → giant lick at Lv5	MINI MAX ARMY
Axel	Apple thrower	Apples that stun → Lv5 adds APPLE PIE STUN	GINGER BOOMBOX
Kirril	Paranoid	Sneezes a spinning gun → Lv5 fires SCAM words	SCAM WAVE (timed booger explosions)
Raheel	Tank (extra heart!)	Big booger that grows every level	GOOFY BEAM (5s laser)
Huntsman	Patient hunter	Lingering spear (refreshes on hit)	SNIPER SHOT (aim, then charge)
Plus a Tutorial card on the character select if you've never played before.

Modes
Classic — fight progressively harder waves through the Nosebleed Overlord boss
Endless — boss fights forever, scaling difficulty
Nose Dive — vertical scroller through the inside of a nostril (unlocked after beating the boss)
Flappy Nose — flappy bird but with nose hairs (unlocked after beating the boss)
Controls
Desktop:

Arrow keys / WASD to fly
SPACE to shoot (tap, no holding)
E for ultimate
P to pause
Mobile:

Joystick (bottom-left) for thrust
◀ ▶ buttons (bottom-right) to turn
FIRE button to shoot (one tap = one shot)
ULT button for ultimate
⏸ in the top-right to pause
Running it locally
It's a single self-contained HTML file. You can just open it in a browser:

open nose_wars_12.html
Or if you want to serve it (which avoids some browser file:// quirks):

python3 -m http.server 8000
# then visit http://localhost:8000/nose_wars_12.html
No build step. No npm install. No dependencies.

Deploying to GitHub Pages
Rename nose_wars_12.html to index.html (or leave it and use the longer URL)
Push to GitHub
Settings → Pages → Source: Deploy from a branch → main → / (root)
Wait ~1 minute, your URL will be https://<your-username>.github.io/<repo-name>/
Save data
The game uses localStorage to remember:

nw_flappy_best — your best Flappy Nose score
That's the only thing it persists. Clearing site data resets it.

Tech
Vanilla JavaScript, single HTML file
Canvas 2D for everything (no WebGL)
Mobile-friendly: responsive canvas + touch controls + meta viewport tag
~7,000 lines of code, ~290 KB on disk
Known limits / things to try
Tuning is rough — durations, damage values, and ult costs are first-pass guesses. Play around with them.
Tutorial uses Nate as the default. If you want to learn with a specific nose, that's a future addition.
The Nosebleed Overlord is the only boss in classic mode (Endless rotates through more variants).
Credits
Built collaboratively with Claude. Every nose drawn from scratch in canvas, every ult tuned over a lot of back-and-forth.
