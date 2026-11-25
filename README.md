# Vase-Forge

Vase-Forge is a browser-based 3D vase designer. Adjust the shape with sliders or exact values, preview the result in real time, and export it for 3D printing or use in another 3D application.

The project runs entirely in a single `index.html` file and has no build step. It is available online through GitHub Pages:

**https://hofi0ne.github.io/Vase-Forge/**

## Features

- Shape the vase using height, radii, belly position, and lip controls
- Adjust ribs, rib depth, twist, wall thickness, floor thickness, and mesh resolution
- Start with Amphora, Cylinder, Bulb, Twisted, or Fluted presets
- Randomize designs and move backward or forward through changes
- Orbit and zoom the live 3D preview
- Switch between wireframe, cross-section, and auto-rotation modes
- Highlight overhanging surfaces that may need print support
- Preview custom glaze colors
- View estimated volume, solid-PLA mass, dimensions, and overhang percentage
- Copy shareable design links
- Save and load designs as JSON
- Export PNG snapshots
- Export STL, GLB, or OBJ models
- Switch between English and Czech
- Use light or dark interface themes

## Getting Started

### Use the hosted version

Open [Vase-Forge on GitHub Pages](https://hofi0ne.github.io/Vase-Forge/) in a modern browser.

### Run locally

No installation or build process is required.

```bash
git clone https://github.com/hofi0ne/Vase-Forge.git
cd Vase-Forge
```

Open `index.html` directly in a browser, or serve the directory locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/`.

## Controls

- Drag the 3D view to orbit.
- Scroll with a mouse or pinch on a touch screen to zoom.
- Adjust a slider or enter an exact value in the control panel.
- Select a preset to apply a ready-made shape.
- Use **Random** to generate a new design.
- Use **Undo** and **Redo** to navigate design changes.
- Set the export height before generating a downloadable model.

## Export Formats

| Format | Purpose |
|---|---|
| STL | Binary STL in millimetres, Z-up, suitable for slicing software |
| GLB | Binary glTF 3D model with color and material data |
| OBJ | Text-based 3D mesh for compatible modeling tools |
| PNG | Screenshot of the current 3D preview |
| JSON | Vase parameters and glaze color for later editing |

## How It Works

Vase-Forge creates a hollow rotational mesh from a radius profile:

1. The height profile combines the base, belly, neck, and lip radii.
2. An optional rib pattern and twist modify the outer surface.
3. A smaller inner profile creates the wall thickness.
4. The rim and floor close the mesh.
5. Three.js renders and allows interaction with the generated model.

The STL, GLB, and OBJ exports scale the geometry to the selected export height.

## Technology

- HTML
- CSS
- JavaScript
- [Three.js r128](https://threejs.org/) loaded from cdnjs
- Browser APIs for canvas rendering, clipboard sharing, local storage, and file downloads

## Project Structure

```text
.
├── index.html  # Application markup, styles, geometry, UI, and exports
└── README.md   # Project documentation
```

## Browser Requirements

A modern desktop or mobile browser with WebGL support is required.

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository.
2. Create a branch for your change.
3. Make and test the update in a local browser.
4. Open a pull request describing the improvement.

## License

No license is currently specified. If you plan to allow reuse or contributions, consider adding a license file and a corresponding `License` section.

## Author

Created by [hofi0ne](https://github.com/hofi0ne).
