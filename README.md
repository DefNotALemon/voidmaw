# VOIDMAW

A single-file arcade space shooter in the spirit of the 1982 mine-crystals-before-the-boss-wakes-up classics.

Something is being assembled out in the dark. Worker drones mine crystals from the planetoids and fly them back to build the Maw. Shoot the planetoids first, grab the crystals yourself, and stack them as homing bombs — you'll need thirteen when it wakes up and starts hunting you across the map.

**Play it:** open `index.html` in a browser. No build step, no dependencies.

## Controls

| Key | Action |
| --- | --- |
| ← → or A D | rotate |
| ↑ or W | thrust |
| ↓ or S | brake (retro jets) |
| Space | fire |
| X or Shift | launch bomb (homes on the Maw) |
| P / M | pause / mute |

An extra ship is awarded every 50,000 points.

Touch controls appear automatically on phones.

## How it works

- **Planetoids** hold crystals. Shooting one knocks a crystal loose.
- **Crystals** drift; fly near them and the ship's tractor field pulls them in. Each one is a bomb (max 20).
- **Workers** (green) mine the same crystals and carry them to the construction site. Kill a carrier and it drops its load.
- **Warriors** (amber) harass you and lead their shots.
- **The Maw** wakes when it has 13 parts. It's faster than you. Thirteen bomb hits break it and you move to the next sector, where the drones are faster and there are more of them.
- Bombs also work on the unfinished Maw — each hit knocks a part off.

## Tech

One HTML file: canvas rendering, procedural WebAudio sound, `speechSynthesis` for the Maw's voice, wrap-around 5200×5200 world with a scanner. High score is kept in `localStorage`.
