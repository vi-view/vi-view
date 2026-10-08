## Note: vi-view is a fan-made, non-commercial project that is not affiliated with Rockstar Games or Take-Two Interactive, ships with no game files, and is provided as-is with no support (use at your own risk)!

# Overview:

vi-view is a Google Earth-like map viewer for the Grand Theft Auto games. It imports a game's map from a local install and renders it in 2D, 3D, and Free Camera views, with tools for measuring, annotation, and comparison.

[![Youtube Redirect](https://img.youtube.com/vi/cTz3gypNG8w/0.jpg)](https://www.youtube.com/watch?v=cTz3gypNG8w)

Video Demo: https://www.youtube.com/watch?v=cTz3gypNG8w

Features:

- **Views:** 2D (top-down), 3D (orbit and tilt), and Free Camera (fly), with adjustable time of day, sun position, and atmosphere
- **Measuring:** paths that report their length and areas that report their size and perimeter
- **Annotation:** waypoints, saved cameras, and folders to organize them; annotations export to and import from JSON
- **Comparison:** multiple maps loaded at once, each with its own position and rotation, all drawn at true scale
- **Custom Models:** .obj, .fbx, and .gltf/.glb files placed in any map, or imported as a map of their own
- **Import:** maps are converted directly from a local install of the game (no game data ships with the tool)
- **Export:** the 2D map can be saved as an image

### Local Installs

Importing a map requires a legitimately owned copy of the game installed on the same machine (e.g. through Steam or the Rockstar Games Launcher) as vi-view includes no game data.

The install directory and contents is never modified, and the game does not need to be running.

### Included Map

vi-view comes with one map so that it can be used without any game installed: **GTA VI (Yanis)**, a community-made map by YANIS (see [Credits](#credits)) and the GTA 6 Mapping Project community.

# Setup:

### 1. Download

Download the latest zip from the [Releases](../../releases/latest) page and unpack it into any folder. There is no installer.

Requirements: 64-bit Windows and a GPU that supports Direct3D 11.

### 2. Run

Run `vi-view.exe`. The included map is shown on first start.

Note: vi-view.exe is not code-signed, so Windows SmartScreen may show a warning the first time it is run

### 3. Import a Map (Optional)

Open **Maps & Widgets** -> **Maps** tab -> **Import**, select the game, and select its install directory

Supported Games:
- **Grand Theft Auto III:** original PC release and Definitive Edition
- **Grand Theft Auto: Vice City:** original PC release and Definitive Edition
- **Grand Theft Auto: San Andreas:** original PC release and Definitive Edition
- **Grand Theft Auto IV:** including The Complete Edition
- **Grand Theft Auto V:** Legacy and Enhanced

An import takes from a few seconds to a few minutes depending on the game, and the viewer stays usable while it runs. A map only needs to be imported once.

All data is stored next to the executable.

# Custom 3D Models:

Model files can be loaded in two ways:

1. As a model widget
	- Placed in any map and positioned with translate, rotate, and scale handles
	- Up to 4096 different model files can be loaded at once
2. As a map of its own
	- Imported with a name, an up axis, and a scale
	- Behaves like any other map (it can be shown, hidden, moved, rotated, and compared against a game map)

Supported formats:

- GLB and glTF 2.0
- FBX (binary, version 7.0 or later)
- OBJ, with its MTL file beside it
- Textures in PNG, JPEG, TGA, or BMP (embedded or beside the file)

Not supported: ASCII FBX, glTF compressed with Draco or meshopt, textures in other formats (DDS, WebP, KTX2, etc.), and animation, lights, and cameras (which are skipped)

# Controls:

The most common controls are listed below. Press `F1` in vi-view for the full list.

- **Drag / right drag / mouse wheel:** pan / rotate and tilt / zoom (2D and 3D views)
- **F:** toggle Free Camera
- **W A S D, Q / E, Shift / Ctrl:** fly, down / up, faster / slower
- **H / N:** home view / north up
- **1 to 9, 0:** show or hide a map
- **Right click:** context menu for the map, a widget, or a list row
- **G / R / C:** translate, rotate, and scale handles for the selected widget
- **Ctrl + C / X / V:** copy, cut, and paste a widget
- **Esc or mouse back button:** close a panel (Esc twice exits)
- **~:** console (`help` lists the commands, `tp` goes to a position, `where` prints the current view, `bake_2d` saves the 2D map as an image)

# Limitations:

A map is a static, daytime snapshot of the game world. The following are not imported:

- Building interiors
- Map additions from GTA V's online content packs and from GTA IV's episodes
- Objects that GTA IV and GTA V only draw at night

Terrain and surface materials are also simplified compared to the in-engine games.

# Credits

The viewer ships with a 3D model of the YANIS GTA 6 community map (V16). Huge credits to YANIS and the many others who contributed to the GTA 6 Mapping project!

View a more detailed version of the map here: https://map.stateofleonida.net/

# Legal / Disclaimer:

vi-view is an unofficial, fan-made map viewer. It is not affiliated with, endorsed by, or sponsored by Rockstar Games or Take-Two Interactive. Grand Theft Auto and all related names, marks, and content belong to their respective owners.

- **No game data included:** vi-view ships without any game files. Importing a map for viewing requires a legitimately obtained copy of the game installed on your own computer
- **Do not redistribute Rockstar's property:** do not share, upload, or otherwise distribute imported maps or anything else taken from the games. That data remains the property of its owners
- **Your own models only:** import only models you have the right to use, and do not share an imported map unless everything in it is yours to share
- **Non-commercial use only:** vi-view and everything made with it (including images) are for personal, non-commercial use. Do not sell them, charge for access to them, or use them in a paid product or service
- **Included map:** the "GTA VI (Yanis)" map is a community-made work that belongs to its author (YANIS). Do not redistribute it separately
- **No support, no warranty:** vi-view is a non-commercial fan project provided as-is, without support or warranty of any kind. Issues and requests are not monitored. Use it at your own risk

See `LICENSE.md` for the full terms.
