# Lander-Game (v0.1) — PRD

## 1. Purpose
A single-file 2-D arcade demo (top-down) where a player rotates and propels a ship through a gravity field. Built as a teaching showcase for PixiJS 8 + Rapier 2-D.

## 2. Core Gameplay
| Feature            | Notes |
|--------------------|-------|
| Rotate CW / CCW    | Keyboard `→` and `←` (or `D/A` on desktop; touch buttons on mobile). |
| Thrust             | `↑` / `W` / on-screen button — applies forward impulse from ship’s nose. |
| Gravity            | Constant downward `g` (configurable in `settings.json`). |
| Win/Lose           | **MVP:** none. Player free-flies; crash = reset. |

## 3. Tech Stack
| Layer       | Choice | Rationale |
|-------------|--------|-----------|
| **Renderer**| PixiJS v8.10.2  [oai_citation:0‡github.com](https://github.com/pixijs/pixijs/releases) | Small bundle, WebGL2/WebGPU auto-fallback, mature docs. |
| **Physics** | Rapier.js (WASM build) master (≈ 450 commits)  [oai_citation:1‡github.com](https://github.com/dimforge/rapier.js) | Fast, deterministic, first-class TypeScript. |
| **Bundler** | Vite “library mode” | Generates a single `index.html` + hashed WASM. |

## 4. Assets
| Item      | Source | License |
|-----------|--------|---------|
| Spaceship sprite (32×32 & 64×64) | Kenney “Pixel Shmup” pack  [oai_citation:2‡kenney-assets.itch.io](https://kenney-assets.itch.io/pixel-shmup) | CC0 (embed or base64-inline). |
| UI icons (arrows, flame) | Same pack | CC0 |

> _Stretch:_ swap sprite atlas via drag-and-drop for quick skinning.

## 5. Input & UX
* Desktop: keyboard as above; mouse wheel zoom.
* Mobile: responsive on-screen buttons + inertial pan.
* FPS counter toggle with `F` for perf testing.

## 6. Physics Tuning
* Mass = 1 kg, moment auto-calc from sprite bounds.
* Thrust force default `200 N`.
* Gravity `9.8 m/s²`.  
* Collision groups: ship vs. static world (ground/obstacles).

## 7. Non-Functional
| Requirement            | Target |
|-------------------------|--------|
| First load (< 3 G)      | ≤ 5 s on 4-year-old Android mid-tier. |
| Bundle size            | ≤ 250 KB gz (JS) + 200 KB sprite/wasm. |
| Offline‐first          | Service Worker runtime-cached. |
| Code style             | ESLint + Prettier, strict TS. |

## 8. Deliverables
1. `/index.html` — standalone game (imports CDN Pixi & local Rapier WASM).
2. `/README.md` — build/run instructions.
3. `/settings.json` — tweak physics without rebuilding.

## 9. Open Questions
* Desired art style (pixel vs. vector) — Kenney pack is pixel-art.
* Need for sound FX? (simple thrust loop & crash boom).
* Level design: flat ground only, or add obstacles?