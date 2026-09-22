# Starfall Farm

*A cozy, farming-sim inspired live wallpaper for [Wallpaper Engine](https://www.wallpaperengine.io/), built entirely with HTML, CSS, JavaScript, and the Web Audio API.*

![Preview](preview.gif)

*Dawn → morning → noon → golden hour → dusk → night, all rendered live in the wallpaper itself.*

> Renamed it already? This README uses **Starfall Farm** as a placeholder — swap it (and the title in `project.json`) for whatever you settled on.

## Overview

A pond-side farm scene with a real day/night cycle, four seasons, seven weather types, a small original cast of villagers and animals, a steam train that passes and stops at a lakeside station, and a fully generative music and ambience system — no external audio or video files, no copyrighted game assets. Everything you see and hear is drawn and synthesized live in the browser.

## Features

- **Real-time day/night cycle** — the sun and moon move across the sky based on your system clock (or a manual hour, for testing). Moon phases follow the real date.
- **Sunrise/sunset sync** — optionally enter your latitude/longitude for a real-world sunrise and sunset time. Calculated entirely on-device; nothing is sent anywhere.
- **Four seasons** — Spring, Summer, Fall, and Winter, either automatic (rotating every 28 in-wallpaper days) or fixed. Each season shifts the palette, foliage, and particle effects (petals, fireflies, falling leaves, snow).
- **Seven weather types** — Clear, Cloudy, Rain, Thunderstorm, Fog, Windy, and Random, with smooth transitions, lightning flashes, and a rainbow that appears once the rain clears.
- **Sky detail** — twinkling stars, shooting stars (adjustable frequency), and drifting clouds, all dimmed appropriately in daylight.
- **Original cast** — a wandering couple, five villagers with their own routines, and farm animals (chickens, cows, sheep, a cat, a dog, rabbits, ducks), all original pixel-art designs with day/night and weather-aware behavior.
- **Character editor** — customize the couple's skin tone, hairstyle, hair color, shirt, and pants directly from Wallpaper Engine's properties panel.
- **Steam train** — an 8-car passenger train that stops at a small lakeside station (with waiting passengers who board), alternating with an 8-car freight train that passes through without stopping.
- **Pond life** — a moored fishing boat, a passing fishing ship, swimming ducks, and (in summer) dragonflies skimming the water.
- **Evening picnic** — a couple settles by the lake at dusk for a small recurring scene.
- **Original audio** — background music with four seasonal themes (synthesized, not sampled) and ambient sound (rain, thunder, wind, crickets, campfire, train, boat), all generated with the Web Audio API. No copyrighted or third-party audio is included.
- **Customizable clock** — 12/24-hour format, seconds, date, language (English/Indonesian), position (freely nudge it anywhere on screen), and size.
- **50+ properties** in total, grouped by category in the Wallpaper Engine panel: Time & Sky, Season & Weather, Residents & Wildlife, Character Editor, Music & Ambient Sound, Clock Display, and Performance.

## Files

```
.
├── index.html          # the entire wallpaper — scene, animation, audio engine
├── project.json         # Wallpaper Engine project definition & properties
├── preview.png           # Workshop/library thumbnail
├── pressstart2p.woff2    # bundled clock font
└── OFL.txt              # SIL Open Font License for the bundled font
```

Everything is self-contained in a single HTML file — no build step, no external dependencies, no network requests.

## Installation

**Option A — Steam Workshop**
Subscribe from the Workshop page (link once published) and Wallpaper Engine handles the rest.

**Option B — Manual / local build**
1. Copy this whole folder into your Wallpaper Engine projects directory, e.g.
   `Steam\steamapps\common\wallpaper_engine\projects\myprojects\starfall-farm\`
2. Open Wallpaper Engine → **Installed** tab (or **Open Wallpaper → Open from File** and pick `project.json`).
3. Select it and set it as your active wallpaper.

## Customization

All settings are available from Wallpaper Engine's **Properties** panel once the wallpaper is applied — no code editing required. A few worth knowing about:

- **Performance** → lower the FPS cap if the wallpaper competes with games or other GPU-heavy apps.
- **Season & Weather → Sync sunrise/sunset to coordinates** → enter your latitude/longitude for locally accurate sun timing.
- **Music & Ambient Sound** → separate on/off switches and volume sliders for music and ambience, plus a fixed or automatic music theme.

If you *do* want to edit it directly, everything lives in `index.html`: the scene is drawn procedurally on an HTML `<canvas>`, animals/villagers/objects are depth-sorted each frame, and the audio engine (search for `MU` and `AM` in the script) synthesizes every note and sound effect at runtime.

## Credits

- All artwork, animation, music, and sound effects were created specifically for this project — no assets from Stardew Valley or any other game are used, and this project isn't affiliated with or endorsed by ConcernedApe.
- Clock font: [Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) by CodeMan38, licensed under the [SIL Open Font License 1.1](OFL.txt).

## License

Choose a license for your own code/art before publishing (e.g. MIT for the code) and note it here. The bundled font keeps its own OFL license regardless of what you choose for the rest of the project.

## Feedback & Bug Reports

Found an issue or have a feature request? Open an issue on this repository, or reach out via [your Discord/Steam link here].

If you'd like to support development, you can do so here: [your Ko-fi link here].
