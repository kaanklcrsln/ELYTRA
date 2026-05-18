# ELYTRA
<img width="2498" height="1360" alt="elytra_ss" src="https://github.com/user-attachments/assets/6e729c69-4eda-4aa1-8d81-ef1620d48478" />

Real-time satellite tracking dashboard covering every country with objects in
orbit. A single static `index.html`  no build step, no backend.

## Features

- Live TLE propagation (client-side, via satellite.js) for the full CelesTrak
  active catalog, cross-referenced with SATCAT for ownership.
- 2D world map (Leaflet) with CartoDB Dark/Light, Esri Satellite and
  OpenStreetMap base layers.
- 3D orbit view (Three.js) showing each selected satellite's orbit and position.
- Live comparison charts (Chart.js) for altitude and velocity.
- Full TLE-derived element readout for the focused satellite.
- Left sidebar: scrollable country flag column plus a per-country satellite
  selector with search.
- Glass UI design system from kaanklcrsln.space; offline localStorage cache so
  reloads survive CelesTrak rate limits.

## Usage

Open `index.html` in a modern browser. Pick a country flag, tick satellites,
and watch them on the map, 3D view and charts simultaneously. Click a row to
inspect its full element set in the bottom info bar.

## Tech

Leaflet, satellite.js, Three.js, Chart.js — all from CDN. Data from CelesTrak
(`gp.php` active TLE and `satcat.csv`).

Built by Jager — https://kaanklcrsln.space
