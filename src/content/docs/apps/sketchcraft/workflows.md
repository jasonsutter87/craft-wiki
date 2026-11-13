---
title: Workflows
description: Roofs, openings, components, dimensions, scripting, and AI agents in SketchCraft.
sidebar:
  order: 3
---

:::note[Third-Party Application]
SketchCraft is an independent open-source modeler maintained by Jason Sutter and the SketchCraft contributors.
:::

## Keyboard shortcuts

| Key | Tool | Key | Tool |
|---|---|---|---|
| Space | Select (hold to orbit) | M | Move (Option copies) |
| L | Line | Q | Rotate |
| A | Arc | S | Scale |
| R | Rectangle | T | Tape Measure |
| C | Circle | D | Dimension |
| N | Polygon | W | Text |
| P | Push/Pull | B | Paint (Option samples a color) |
| F | Offset | E | Erase (Shift hides) |
| J | Follow Me | O | Orbit |
| X | Section cut | G / H | Group / Hide |

While drawing, the arrow keys lock a direction: **Right** for red (X), **Left** for green (Y), **Up** for blue (Z). Press the same arrow again to unlock it.

## Exact sizes

Every tool reads the measurements box. Start the tool, then type and press **Enter**:

- Rectangle: `4,6` (width, depth)
- Line, Tape Measure, Move: a length along the direction you're pointing
- Push/Pull and Offset: a distance. Negative pushes in.
- Rotate: degrees. Scale: a factor, or `x,y,z` for each axis.
- Circle and Polygon: a radius, or `24s` to set the number of sides first.

Typing right after an action changes that action. Pull a face up, type `3.2`, and the pull becomes exactly 3.2 m.

## Roofs

- **Gable**: Draw a line across the top face between the midpoints of two opposite edges, then move that line straight up (Move, **Up** arrow, type the rise).
- **Overhanging roof slab**: Draw the roof's end profile, a V with thickness, on a vertical plane in front of the house, then push/pull it the length of the house plus both overhangs.
- **Eave trim and cornices**: Select the top face as the path, draw a small profile at one corner, then use **Follow Me** and click the profile.

## Doors, windows and openings

- Draw a rectangle on a wall. Inside the wall it becomes a hole; touching the bottom edge it splits the wall, which is right for doors.
- Push the new face in (for example `-0.3`) to make a recess, or pull it out to make a bay.
- Or drop a **Door**, **Window** or **Garage door** from the Library onto the wall. It faces out of the wall, and doors land on the wall's bottom edge.

## Components

- Select faces or a group, right-click and choose **Make component**.
- **Move** with **Option** held copies a component. Then type `x5` for five copies at the same spacing, or `/5` to fill the distance with five.
- Double-click any copy to edit it. Every copy changes together. Press **Esc** when done.
- **Explode** turns a copy back into plain geometry you can edit on its own.

## Dimensions and elevations

1. Press **D**, click two points, move the cursor away and click to place the dimension. Hover a dimension and click **×** to delete it.
2. Press **W**, click the point to label, then click where the label goes, and type the text.
3. Choose **Front** and turn on **Parallel** for a true elevation. Save it in **Views** to come back to it.
4. **Render** saves a PNG of the current view, dimensions included.

## Scripting

Everything in the app is a JSON command, one per line. Add `"as":"name"` to remember a result and use `"@name"` later:

```json
{"cmd":"rect","from":[0,0,0],"to":[8,12,0],"as":"lot"}
{"cmd":"pushpull","face":"@lot","distance":6}
{"cmd":"insert","asset":"door","at":[3.5,0,0]}
{"cmd":"render","out":"house.png","view":"iso"}
```

Run it with `sketchcraft run house.jsonl`. The repository's `examples/` folder has a full two-story house.

## AI agents over MCP

`sketchcraft mcp --doc ~/Documents/SketchCraft/live.sketchcraft` starts a Model Context Protocol server with three tools: `sketchcraft_run` (run commands), `sketchcraft_render` (returns an image the agent can look at) and `sketchcraft_info`. The desktop app uses the same live file, so changes an agent makes appear in the app within a second, and yours appear to the agent.
