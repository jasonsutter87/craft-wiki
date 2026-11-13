---
title: Getting started
description: The SketchCraft workspace, push/pull basics, and your first building.
sidebar:
  order: 1
---

:::note[Third-Party Application]
SketchCraft is an independent open-source modeler maintained by Jason Sutter and the SketchCraft contributors.
:::

## The workspace

- **Left panel**: **Outliner** lists groups and components with show/hide toggles and tags. **Library** holds the built-in assets and templates. **Views** saves camera angles you can fly back to.
- **Right panel**: **Entity Info** for the selection (area, length, tag), paint swatches, and Arrange actions such as Make group and Make component.
- **Toolbar**: The floating bar at the bottom holds every tool, grouped as Select; Line, Arc, Rectangle, Circle, Polygon; Push/Pull, Offset, Follow Me; Move, Rotate, Scale; Tape Measure, Dimension, Text, Paint, Erase; Orbit and Section.
- **Measurements box**: Bottom right. While a tool is running, type a number and press **Enter** to make it exact.
- **Style bar**: Top right. Standard views (Iso, Top, Front, Right), Fit, and toggles for X-ray, Shadows, Edges and Parallel projection.

Units are meters. Z points up, and the red, green and blue lines through the origin are the X, Y and Z axes.

## Moving around

- **Orbit**: middle-drag, or hold **Space** and drag. Tap **Space** to return to Select.
- **Pan**: right-drag.
- **Zoom**: scroll; it zooms toward the cursor.
- **Zoom extents**: **Shift+Z**, or **Fit** in the style bar.

## Your first building

1. Press **R** and click on the ground, then type `8,12` and press **Enter**. You now have an 8 × 12 m rectangle.
2. Press **P**, click the rectangle, type `6` and press **Enter** to pull it up 6 m.
3. Press **L** and draw a line across the roof from the midpoint of one short edge to the midpoint of the other. The cursor shows **Midpoint** when it snaps. The roof splits in two.
4. Press **M**, click the new ridge line, press the **Up** arrow to lock the blue axis, type `3` and press **Enter**. The ridge rises and the gable ends form.
5. Open **Library**, click **Door** and click the front wall. The door faces out of the wall and stands on its bottom edge.
6. Press **D**, click two corners of the front wall, move the cursor away to place the dimension, and click.

Press **Cmd+Z** (Ctrl+Z on Windows and Linux) to undo any step.

## How push/pull works

- Faces form automatically when edges close a flat loop.
- A shape drawn **inside** a face cuts a hole in it. Push it in for a window, or pull it out for a bay.
- A shape that **touches** a face's edge splits the face, so a door can sit at ground level.
- Pulling a face that already has walls around it just raises it, so the box gets taller rather than gaining a second box.
- Groups keep geometry apart: two houses in separate groups never stick together. Double-click a group to open it, and press **Esc** to close it.
