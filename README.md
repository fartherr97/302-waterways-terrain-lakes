# 302 Waterways terrain tiles: lakes

Lake tiles for the 302 Waterways 3D view and Safe Route, served by GitHub Pages at
`https://fartherr97.github.io/302-waterways-terrain-lakes/`.

- The fourth terrain site: the lakes the first three (`302-waterways-terrain`, `-north`, `-south`)
  have no room for. Listed under `lakes` in the first site's `sets.json`
  (`https://fartherr97.github.io/302-waterways-terrain/sets.json`).
- Source: USGS 3DEP 1/3 arc-second elevation (NAVD88), public domain. Each lake sits under its own
  water; a lake with no published survey has a modeled bottom (deeper away from the shore, not
  measured), and the app says so.
- Tiles: XYZ (Web Mercator) at zoom 10, 12 and 14 in `lakes/`; `lakes/index.json` lists them.
- Format: 257 × 257 int16 heights in decimetres (NAVD88), rows north → south, each row
  delta-coded (first value absolute), little-endian, gzip.

Built by `scripts/engine3d/bake_lakes.py` and `publish_lakes.py` in the app repository.
