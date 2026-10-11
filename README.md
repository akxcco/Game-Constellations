# Game Constellations

A star map of my game library. Every game I own is a star, every genre is a constellation, and you can drag around the sky, zoom in, and click a star to read about the game.

It's one HTML file. No build step, no dependencies, no server. Open `index.html` and it works.

## What's in it

- 117 games sorted into 12 constellations (Shooters, Survival, Racing, Sandbox, Simulation, Horror, Platformers, Strategy, Puzzle & Party, Roguelikes, Idle, Sports)
- Click a star for a short description, tags, a "See more" blurb with developer and release details, and a link to its Steam search
- Search box, genre chips along the top, and a random star button if you can't decide what to play
- A small minimap in the corner, plus some background sky stuff (shooting stars, twinkling, slow drift)
- Optional ambient sound, which you can turn off with the speaker button

## Controls

| Action | Mouse / touch | Keyboard |
| --- | --- | --- |
| Look around | Drag | Arrow keys |
| Zoom | Scroll or pinch | `+` / `-` |
| Open a game | Click a star | |
| Search | Type in the box | `/` |
| Random game | Random star button | `R` |
| Close the card | × | `Esc` |

Clicking the minimap jumps you to that part of the sky.

## Running it

Just open `index.html` in a browser. To host it on GitHub Pages, push the file to a repo, then go to Settings → Pages and pick the branch you pushed to.

## Adding or editing games

The games live in a block of text near the top of the script, one per line:

```
Name|GROUP|tag one,tag two|Short description
```

The group code is one of `SH`, `SU`, `RC`, `SB`, `SM`, `HR`, `PF`, `ST`, `PZ`, `RL`, `CA`, `SP`. If you want a longer "See more" blurb, add an entry with the same game name in the `MORE` object just below it. Reload and the new star appears. If a group has no games left, its constellation just disappears.

## Notes

A few game names are shared by several unrelated games (FLOW, HELPLESS, MISERY, Midnight Driver). The entries point at the ones I could match to the library, and the blurbs say so where it matters. Release dates and details came from store pages and press coverage, so double-check anything important.

Everything is plain HTML, CSS and canvas. The sound is generated in the browser with the Web Audio API, so there are no audio files either.
