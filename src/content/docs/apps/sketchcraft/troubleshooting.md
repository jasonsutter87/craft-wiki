---
title: Troubleshooting
description: Fixing faces that won't form, push/pull surprises, snapping, and display issues in SketchCraft.
---

:::note[Third-Party Application]
SketchCraft is an independent open-source modeler maintained by Jason Sutter and the SketchCraft contributors. Report problems on the [issue tracker](https://github.com/jasonsutter87/sketchcraft/issues).
:::

## A face won't form

- The loop must be flat. If one corner is a little off the plane, the face won't close. Turn on **X-ray** to see the lines, then redraw the loop with snapping, watching for **Endpoint** at each corner.
- Every edge must meet the next one exactly. Draw from **Endpoint** to **Endpoint** rather than eyeballing it.

## Push/pull made a second box instead of raising the first

Push/pull raises a face only when walls already stand on all of its edges. If a face was drawn on top of a box rather than being the box's top, it extrudes on its own. Erase the extra face, then push/pull the box's own top.

## Faces look blue

You're seeing the back of a face. Painted faces show their color on both sides, but bare faces stay blue on the back so you can tell which way they point. Select the faces, right-click and choose **Reverse faces**.

## Lines won't connect to a group

Groups keep their geometry separate on purpose. Double-click the group to open it, draw inside, and press **Esc** to close it.

## The cursor snaps somewhere unexpected

- An arrow-key axis lock may still be on. Press **Down** to release it, or **Esc** to cancel the tool.
- A **From Point** dotted line means the cursor is lining up with a point you hovered earlier. Move away from the dotted line, or hover a different point.

## The view is empty or lost

Press **Shift+Z** to zoom to everything. If the model is still hidden, open the **Outliner** and check the eye toggles and tags, or right-click empty space and choose **Unhide all**. A section cut hides everything on one side of it; remove it with **Section ✕** in the style bar.

## The app won't open

- **macOS**: see the notarization note in [Install and update](/apps/sketchcraft/install-update/).
- **Linux**: the AppImage needs FUSE. Install `libfuse2`, or run it with `--appimage-extract-and-run`.
