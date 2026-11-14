---
title: SketchCraft
description: Independent push/pull 3D modeler for buildings and streets in the Craft ecosystem.
sidebar:
  order: 0
---

:::note[Third-Party Application]
SketchCraft is an independent, community-developed application created and maintained by Jason Sutter and the SketchCraft contributors. It is not developed or officially maintained by ArtCraft, but is part of the broader Craft ecosystem.
:::

SketchCraft is an open-source push/pull 3D modeler written in Rust. Draw an outline on the ground or on any face, pull it up into a solid, and keep shaping: cut a door into a wall, raise a ridge line into a gable roof, sweep trim around the eaves, and dimension the result as an elevation.

![SketchCraft workspace showing a dimensioned two-story house with the outliner, floating toolbar, and shadows](/assets/uploads/sketchcraft/hero.webp)

## Features

- **Push/pull modeling**: Lines that split edges, cut faces and close into faces; rectangles (also rotated), circles, polygons, arcs (2-point, center, 3-point and pie), freehand, offsets; push/pull that carves windows and doors into walls; Follow Me sweeps; Solid Tools (union, subtract, intersect, trim, split) and Intersect Faces.
- **Inference and exact input**: Snaps to endpoints, midpoints, edges, faces, guides and the red/green/blue axes (which the Axes tool can turn), with From Point alignment and arrow-key axis locks. Type a number and press Enter for exact lengths, sizes, angles and arrays. Shift+S searches every command.
- **Organize and document**: Groups and components (edit one, every copy updates; doors and windows cut their opening in the wall), Dynamic Components with Component Options, tags, scenes that remember their style, named section planes, dimensions, labels, drawing sheets and blueprints as PDF.
- **Buildings and sites**: Walls, stairs and roofs; **Raise walls** turns an imported floor plan into 3D walls with window openings; terrain (Sandbox) and Add Location for real terrain and map imagery; point clouds (PLY, LAS, XYZ) to model over a scan.
- **Presenting**: Styles (sketchy, hidden line, blueprint and more), Match Photo, physically based finishes, a photoreal path-traced renderer, and a timeline for turntables, walkthroughs and sun studies exported as MP4.
- **Files**: Opens SketchUp (.skp), AutoCAD DWG and DXF, IFC (Revit and ArchiCAD exports), FBX and OBJ. Exports glTF, OBJ, Collada, STL, DXF, DWG, PDF and IFC.
- **Automated and agentic control**: Every action is a JSON command, scriptable through the CLI or a Model Context Protocol (MCP) server. An AI agent and a person can edit the same live model at the same time.

## Documentation guides

- [Getting started](/apps/sketchcraft/getting-started/): The workspace, how push/pull modeling works, and your first building.
- [Install and update](/apps/sketchcraft/install-update/): Installing on macOS, Windows and Linux, the headless CLI, and building from source.
- [Workflows](/apps/sketchcraft/workflows/): Roofs, doors and windows, components, dimensions and elevations, scripting, and AI agents over MCP.
- [Troubleshooting](/apps/sketchcraft/troubleshooting/): Faces that won't form, push/pull surprises, snapping, and display issues.

## Project links

- [SketchCraft on GitHub](https://github.com/jasonsutter87/sketchcraft)
- [Releases](https://github.com/jasonsutter87/sketchcraft/releases)
- [Issue Tracker](https://github.com/jasonsutter87/sketchcraft/issues)
