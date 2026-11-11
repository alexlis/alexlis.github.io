# 弹珠乐境 · Marble Melody

Buildless static site. Serve `dist/` with any HTTP server. All Three.js code is vendored; no CDN dependency is needed for the experience. Google Fonts is optional with system fallbacks.

- Three.js 0.170.0, MeshPhysicalMaterial, procedural studio reflection environment, shadows, OrbitControls and ray casting.
- 56 playable objects across 8 instrument families. Oscillator partials and envelopes produce distinct live synthesized timbres with compressor and delay.
- Six public domain melody excerpts sequenced into an exact 60 second loop. Each excerpt occupies 10 seconds. This is a compact musical arrangement, not a full recording.
- Numeric notation supports degrees 1–7, #, octave apostrophes/commas, rest 0, sustain -, bar |. Up to 128 symbols. All animation and sound are browser local.
- Motion is a deterministic kinematic parabola interpolating collision points. It does not use a rigid body physics engine. Instrument deformation is a damped spring animation.
- A Canvas 2D projected compatibility renderer activates if WebGL context creation fails, preserving playback, notation and camera interactions. It does not offer PBR shading. Native WebGL rendering must be verified on a GPU-enabled browser; the QA cloud browser disables WebGL.
- Click Play to activate Web Audio. Keyboard 1–7 plays notes, Space toggles playback.

## Checks
`node --input-type=module --check < dist/app.js`

Browser checks completed in the Canvas fallback: playback and collision counter, song navigation, challenge hide/reveal, notation track generation, skin and camera selection.
