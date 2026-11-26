# Maker Forge

A browser-based 3D object designer for creating and exporting functional printable models. Maker Forge combines an interactive Three.js preview with parameter controls, presets, and direct STL, GLB, OBJ, PNG, and JSON workflows—all in a single `index.html` file.

**[Open Maker Forge](https://hofi0ne.github.io/Maker-Forge/)**

![Maker Forge](https://img.shields.io/badge/3D%20Designer-Browser%20Based-ff7ab0)
![Three.js](https://img.shields.io/badge/Three.js-r128-2b6cb0)
![Language](https://img.shields.io/badge/Languages-English%20%7C%20Czech-c8336f)

## Generators

Choose a generator from the model menu:

- **Vase** — Hollow rotational forms with ribs, twist, wall thickness, and presets.
- **Storage Bin** — Grid-based bins with configurable cells, dividers, stacking lips, and dimensions.
- **Planter** — Round, square, hexagonal, twisted, or tall hollow planters with drainage holes.
- **Organizer** — Custom rows and columns of slots for desk and cable organization.
- **Phone Stand** — Adjustable-width stands for phones or tablets.

## Features

- Live WebGL 3D preview with orbit, zoom, and optional auto-rotation
- Slider and exact-value editing
- Ready-made presets for every generator
- Random model generation
- Undo and redo history
- Wireframe and cross-section preview modes
- Optional overhang highlighting
- Custom glaze or material color
- Estimated volume, PLA mass, dimensions, triangle count, and overhang percentage
- Shareable design links
- Save and load JSON designs
- PNG screenshots
- STL, GLB, and OBJ exports
- English and Czech interface options
- Light and dark themes
- Desktop and mobile pointer support
- No installation or build step

## Getting Started

### Use the hosted app

Visit [Maker Forge on GitHub Pages](https://hofi0ne.github.io/Maker-Forge/) in a modern browser with WebGL support.

### Run locally

```bash
git clone https://github.com/hofi0ne/Maker-Forge.git
cd Maker-Forge
```

Open `index.html` directly, or serve the repository locally:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Controls

- Drag the preview to orbit.
- Scroll or pinch to zoom.
- Adjust sliders or enter exact values in the control panel.
- Select a preset to load a ready-made configuration.
- Use **Random** to generate a new variation.
- Use **Undo** and **Redo** to move through design changes.
- Set the export height before downloading a 3D model.
- Use **Share** to copy the current design URL.

## Export Formats

| Format | Description |
|---|---|
| **STL** | Binary millimetre-scale, Z-up mesh for slicers and 3D printing |
| **GLB** | Binary glTF model with material color |
| **OBJ** | Text-based 3D mesh for modeling applications |
| **PNG** | Screenshot of the current preview |
| **JSON** | Generator, parameters, and glaze color for later editing |

Exported STL, GLB, and OBJ geometry is scaled to the selected export height.

## How It Works

Maker Forge generates and previews meshes entirely in the browser:

- The vase generator constructs a hollow rotational profile with an inner wall and floor.
- The storage bin and organizer generators build printable wall and divider geometry.
- The planter generator supports radial, polygonal, and twisted meshes.
- The stand generator creates a tapered device holder from configurable dimensions.
- Three.js renders, lights, and orbits each generated mesh.
- Export functions convert the current geometry and selected scale into downloadable formats.

## Technology

- HTML5
- CSS
- Vanilla JavaScript
- [Three.js r128](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js)
- WebGL, Canvas, Clipboard, Local Storage, and File APIs

## Project Structure

```text
.
├── index.html  # Interface, styles, generators, geometry, viewer, and exports
└── README.md   # Project documentation
```

## Browser Requirements

Use a current desktop or mobile browser with WebGL and JavaScript enabled.

## Contributing

1. Fork the repository.
2. Create a branch for your change.
3. Test it locally in a browser.
4. Open a pull request describing the improvement.

## Author

Created by [hofi0ne](https://github.com/hofi0ne).
