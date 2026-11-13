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

- **Push/pull modeling**: Lines that split edges, cut faces and close into faces; rectangles, circles, polygons, arcs and offsets; push/pull that carves windows and doors into walls; Follow Me sweeps for trim and cornices; auto-fold when a move bends a face.
- **Inference and exact input**: Snaps to endpoints, midpoints, edges, faces, guides and the red/green/blue axes, with From Point alignment and arrow-key axis locks. Type a number and press Enter for exact lengths, sizes, angles and arrays.
- **Organize and document**: Groups and components (edit one, every copy updates), tags, hide/unhide, dimensions and text labels, saved views, section cuts, X-ray, shadows and parallel projection.
- **Built-in library and interoperability**: Doors, windows, garage doors, trees, palms, cars, streetlights, benches and hydrants. glTF (.glb), OBJ and STL export, OBJ import, and headless PNG renders.
- **Automated & agentic control**: Every action is a JSON command, scriptable through the CLI, a JSON-over-stdio channel, or a Model Context Protocol (MCP) server. An AI agent and a person can edit the same live model at the same time.

## Documentation guides

- [Getting started](/apps/sketchcraft/getting-started/): The workspace, how push/pull modeling works, and your first building.
- [Install and update](/apps/sketchcraft/install-update/): Installing on macOS, Windows and Linux, the headless CLI, and building from source.
- [Workflows](/apps/sketchcraft/workflows/): Roofs, doors and windows, components, dimensions and elevations, scripting, and AI agents over MCP.
- [Troubleshooting](/apps/sketchcraft/troubleshooting/): Faces that won't form, push/pull surprises, snapping, and display issues.

## Project links

- [SketchCraft on GitHub](https://github.com/jasonsutter87/sketchcraft)
- [Releases](https://github.com/jasonsutter87/sketchcraft/releases)
- [Issue Tracker](https://github.com/jasonsutter87/sketchcraft/issues)
