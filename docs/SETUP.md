# Setup and validation

## Source and preservation

Imported from `Infinity_Empire_Neon_Dynasty_Rift_Rush.zip`, the latest saved Infinity Empire build found on 2026-10-30. Both runtime files are byte-for-byte copies of that archive. Its README was replaced with repository run instructions and these notes. No gameplay refactor, asset move, or save-key change was made.

SHA-256:

```text
index.html     22180ae5307f23b918a210c9543c22a1e227ecc92dc6e137e5ac122a52fdcdd2
renderer3d.js  fc2b3d683a4bb1f3877fd2bdf8c86e613a95595beac24b0db8a016a8181db151
```

## Requirements and assets

- A modern browser with JavaScript, Canvas 2D, and browser storage enabled.
- WebGL for the full 3D scene. The existing code includes a 2D reactor fallback when WebGL is unavailable.
- No package installation, build pipeline, API keys, external fonts, downloaded models, textures, or audio assets are required for standalone gameplay.
- `renderer3d.js` must stay beside `index.html`; the HTML uses that relative path.
- The HTML references `https://www.youtube.com/game_api/v1`. Outside the Playables environment it selects the standalone storage path. The external SDK is not bundled, so a fully offline browser may report a failed SDK request.
- Local progress uses `localStorage` key `infinityEmpire_v1`. File URLs, private browsing, blocked storage, or changing the server port can affect save availability. Platform saves use the existing `ytgame` calls when the game detects the Playables environment.

## Checks completed before import

- Inspected the archive and runtime resource references: both required runtime files are present; no missing local asset references were found.
- Node syntax checks passed for the inline game script and `renderer3d.js`.
- Confirmed runtime files match the archive byte-for-byte.
- Browser smoke testing was attempted, but the available Playwright package has no installed browser executable. Gameplay, visual layout, WebGL rendering, and save reload behavior are therefore not browser-verified in this import.

## Remaining launch checks

These are validation/setup tasks, not missing game assets:

1. Run locally and check reactor taps, selling, first building purchase, passive production, Rift rewards, contracts, and save/reload.
2. Check desktop and portrait touch layouts, orbit/zoom, sound, and graphics quality; test the WebGL fallback on a suitable device.
3. Validate the existing SDK calls, save/load, pause/resume, audio handling, and readiness callbacks in the actual YouTube Playables environment.
4. Confirm current platform packaging, acceptance, and performance requirements before submission. This import does not establish YouTube approval or production readiness.
