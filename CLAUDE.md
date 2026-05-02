# Jason's 40th Birthday Invite — Project Context

## What this is
A self-contained HTML invite (`index.html`) sent to guests as a file they open on their phone. No server, no backend — pure HTML/CSS/JS.

## Party details
- **Who:** Jason Gendron (Jason_G), turning 40
- **When:** Saturday 27 June 2026, from 6pm
- **Where:** Carlton (exact address encrypted — revealed on RSVP confirmation)
- **Food (HP):** Sweet & savoury, host-stocked
- **Drinks (MP):** Red, white & sparkling, host-stocked
- **Dress (SKIN):** Casual. Optional: wear a nod to a favourite old game (pin, cap, tee, etc.)
- **RSVP:** By SMS reply. Address sent on confirmation.

## Design system
Jason's arcade style guide is at `jasonsstyleguide_arcade.html` in this folder.

**Palette:**
- `--deep-canopy: #1A2E22` — primary/structure
- `--forest: #3D6E50` — brand green, borders
- `--harvest-gold: #C8A84B` — accent, highlights, selected state
- `--parchment: #F5F7F2` — text on light
- `--meadow: #7CB542` — positive/interactive
- `--lichen: #9EA89A` — neutral/inactive
- `--smoke-green: #7A9080` — secondary text
- `--screen-bg: #060E08` — CRT screen background

**Fonts:** `Press Start 2P` (pixel headings/labels), `Courier New` (body text)

## Current HTML structure (`index.html`)
1. **Boot overlay** — LEVEL 40 logo flickers in, loading bar fills, fades out at ~3.2s
2. **Cover** — HI-SCORE / PLAYER stats, "▶ LEVEL 40 UNLOCKED", "YOU'RE INVITED" hero with blinking cursor
3. **Tile grid** — 3×2 grid (2×3 on mobile) of clickable Final Fantasy-style menu tiles:
   - ◆ WHEN · ▲ SECTOR · ♥ HP · ◇ MP · ★ SKIN · ▶ SYNC
   - Hover/tap: border switches green → gold, FF cursor `▶` appears top-left
4. **Modal dialog** — clicking a tile opens a gold-bordered FF-style dialog with full detail text; tap anywhere or ESC to close
5. **RSVP Terminal** — styled terminal box with encrypted coords status

## Key style details
- CRT scanline overlay via `body::after` fixed pseudo-element
- Screen wrapper has multi-layer gold/green box-shadow for the arcade bezel look
- Tile hover state mirrors Final Fantasy menu cursor selection
- Modal uses `inset` box-shadow for double-border FF dialog effect
- Responsive: tiles go 3-col → 2-col at 640px, padding tightens throughout
