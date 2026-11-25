# Vase-Forge
A browser-based vase designer. Shape a vase with sliders, watch it update in 3D, and export it for printing or use in other 3D tools. It is a single HTML file with no build step.

## Features

**Design**
- Control height, base, belly, neck and lip radius, and belly position
- Add ribs, rib depth and twist, and choose the number of sides
- Set wall and floor thickness, so the vase is hollow and printable
- Start from five presets: Amphora, Cylinder, Bulb, Twisted and Fluted
- Drag a slider or type an exact value
- Randomize the design, with undo and redo

**Preview**
- Live 3D view: drag to orbit, scroll or pinch to zoom
- Wireframe, auto-rotate and cross-section views
- Overhang view that highlights faces needing support
- Glaze colour picker
- Estimates for volume, solid-PLA weight and overhang share

**Save and share**
- Copy a link that recreates the exact design
- Save and load designs as JSON
- Save a PNG snapshot

**Export**
- STL (binary, millimetres, Z-up, ready for slicing)
- GLB and OBJ
- Set the export height to scale the model

**Interface**
- English and Czech
- Light and dark mode
- Your language and theme choices are remembered

## How it works

The vase is a lathe surface. A smooth radius profile is swept around the vertical axis and modulated by a rib and twist function. An inner surface, a rim and a floor close the mesh into a solid. The STL, GLB and OBJ writers are written by hand, without export libraries.

## Tech

HTML, CSS, JavaScript and [three.js](https://threejs.org/) r128.
