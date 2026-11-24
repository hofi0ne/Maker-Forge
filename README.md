# Vase-Forge
Design a vase in your browser and export it for 3D printing or use in other 3D tools. Adjust the shape with sliders and watch the model update in real time.

Features

• Profile controls for height, base, belly, neck and lip radius, and belly position • Surface controls for ribs, rib depth and twist • Hollow walls with adjustable wall and floor thickness • Five presets: Amphora, Cylinder, Bulb, Twisted, Fluted • Orbit, zoom and pinch controls, with wireframe and auto-rotate • Export to binary STL (millimetres, Z-up, ready for slicing) or GLB Usage Open index.html in a browser. No install or build step is needed, but an internet connection is required to load three.js from a CDN.

How it works The vase is a lathe surface. A smooth radius profile is swept around the vertical axis and modulated by a rib and twist function. An inner surface, rim and floor close the mesh into a solid, so it prints without supports. Geometry is built with three.js, and the STL and GLB writers are hand-rolled with no export libraries.

Tech: HTML, JavaScript, three.js r128
