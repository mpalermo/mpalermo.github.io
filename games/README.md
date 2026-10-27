# games-site

User site (mpalermo.github.io) served at https://mattpalermo.com. The games live under `games/` (https://mattpalermo.com/games).

## Layout

```
index.html        redirects / to /games/
games/index.html  games landing page
games/simball/          Godot web export of SimBall (index.html + .js/.wasm/.pck)
games/simkings/         Godot web export of SimKings
.nojekyll         disable Jekyll processing
```

## Adding / updating a game

1. In Godot: Project > Export > Add "Web" preset. **Disable "Thread Support"** (GitHub Pages can't send the
   COOP/COEP headers threaded builds need). Godot 4.3+ defaults to this.
2. Export to `games/simball/index.html` (the file must be named `index.html`).
3. `git add . && git commit -m "Update SimBall" && git push`

GitHub limits: 100 MB per file, ~1 GB per site. Compress large assets if needed.

## Baseball RPG

When ready, create `games/baseball-rpg/`, drop in the export, and change the "Coming soon" card in `index.html` into
an `<a class="card" href="baseball-rpg/">` link.
