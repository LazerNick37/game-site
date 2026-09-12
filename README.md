# Game Shelf

A tiny, dependency-free static site for testing a game-hosting pipeline (GitHub → Cloudflare Pages).

## Structure

```
index.html              # The hub page — a tileable grid listing all games
style.css                # Styles for the hub page
games/
  number-guess/
    index.html           # A self-contained "Number Guess" game (no dependencies)
```

## Adding a new game

1. Create a new folder under `games/`, e.g. `games/tic-tac-toe/`.
2. Put that game's `index.html` (and any of its own CSS/JS) inside it.
3. Open the root `index.html`, copy one `<li class="tile">` block, and update:
   - the `href` to point at the new game's folder
   - the title and blurb text
   - the `--stripe` color if you want a different accent color for that tile
4. Commit and push — Cloudflare Pages will redeploy automatically.

No build step, no dependencies, no server required — it's plain HTML/CSS/JS, so it will always load.
