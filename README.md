# Lander Game v0.1

A 2D physics-based arcade game built with PixiJS 8 and Rapier.js physics engine.

## Quick Start

1. **Open the game**: Simply open `index.html` in a web browser
2. **No build required**: The game runs directly from the HTML file using CDN resources

## Current Game State

This version implements the core lander game mechanics:
- **Spaceship physics** - Green box representing the spaceship with realistic physics
- **Flat ground** - Full-width ground collision surface
- **Keyboard controls**:
  - `←/→` or `A/D`: Rotate spaceship clockwise/counterclockwise
  - `↑` or `W` or `SPACE`: Fire thrust in forward direction
  - `F`: Toggle FPS counter
- **Visual indicators**:
  - White line showing spaceship nose direction
  - Red line showing thrust effect when firing
  - Real-time position and frame tracking

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
- ✅ Spaceship implementation
- ✅ Player controls (rotation + thrust)
- ✅ Ground collision
- ⏳ Spaceship sprite/graphics
- ⏳ Landing mechanics
- ⏳ Win/lose conditions 