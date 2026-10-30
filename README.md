# Infinity Empire — Neon Dynasty: Rift Rush

A standalone HTML/JavaScript incremental empire game with a procedural 3D WebGL scene. This repository preserves the latest saved **Rift Rush** prototype without changing its game code.

## Run locally

1. Download or clone this repository.
2. Keep `index.html` and `renderer3d.js` together.
3. From the repository folder, run:
   ```sh
   python3 -m http.server 8000
   ```
   On Windows, use `py -m http.server 8000` if needed.
4. Open <http://localhost:8000> in a modern browser. No npm install or build step is required.

You can also open `index.html` directly; a local server gives browser saves a consistent origin. Progress is saved in browser storage under `infinityEmpire_v1` outside YouTube Playables. Use the same browser and address to resume.

## Controls and gameplay

- Tap/click the reactor to gather energy, then **SELL** for credits.
- Use **Build**, **Upgrades**, and **Empire** to buy production, increase storage, expand, and eventually ascend.
- Drag the scene to orbit; scroll or pinch to zoom. Settings include camera reset, sound, effects, and graphics quality.
- Intercept moving Rift shards in timed challenges; six hits grant a temporary 2× production surge.
- Complete rotating field contracts, missions, achievements, and construction milestones.
- Unlock Overdrive, auto sell, additional buildings, and offline earnings.

## Files

```text
index.html          Game UI, styles, economy, input, saves, and Rift challenges
renderer3d.js       Procedural WebGL scene and camera controls
docs/SETUP.md       Dependencies, validation, and launch limitations
```

## Assets and launch status

No local image, model, font, or audio files are missing: visuals and sounds are generated in code. The HTML retains its external YouTube Game SDK script reference. Standalone play uses browser storage; YouTube integration still needs testing in the actual platform environment. See [setup and validation notes](docs/SETUP.md) before preparing a YouTube Playables submission.
