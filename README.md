# Lander Game v0.1

A 2D physics-based arcade game built with PixiJS 8 and Rapier.js physics engine.

## Quick Start

1. **Open the game**: Simply open `index.html` in a web browser
2. **No build required**: The game runs directly from the HTML file using CDN resources

## Current Demo

This initial version shows a physics demo with:
- **Falling boxes** with realistic gravity (9.8 m/s²)
- **Physics simulation** using Rapier.js WASM
- **Interactive controls**:
  - Press `F` to toggle FPS counter
  - Press `SPACE` to add more falling boxes
- **Ground collision** - boxes will bounce and settle on the ground

## Tech Stack

- **Renderer**: PixiJS v8.10.2 (from CDN)
- **Physics**: Rapier.js v0.17.2 (from CDN)
- **No bundler required**: Standalone HTML file

## Configuration

Edit `settings.json` to adjust physics parameters:
- `gravity`: Gravitational acceleration
- `thrustForce`: Ship thrust force (for future ship implementation)
- `shipMass`: Ship mass (for future ship implementation)
- Graphics and control settings

## Controls (Planned)

Future ship controls will include:
- `←/→` or `A/D`: Rotate ship
- `↑` or `W`: Thrust
- Mouse wheel: Zoom (desktop)
- Touch controls (mobile)

## Browser Requirements

- Modern browser with WebGL support
- WebAssembly (WASM) support for physics engine
- Internet connection for CDN resources on first load

## File Structure

```
lander-game/
├── index.html      # Main game file
├── settings.json   # Physics and game configuration
├── README.md       # This file
└── PRD.md         # Project requirements document
```

## Development Status

- ✅ Basic physics simulation
- ✅ PixiJS rendering
- ✅ Rapier.js physics integration
- ⏳ Ship implementation (next)
- ⏳ Player controls
- ⏳ Game mechanics 