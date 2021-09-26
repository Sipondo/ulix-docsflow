---
title: Move
keywords: UPL Ulix Parsed Language Move
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_move.html
folder: upl_docs
summary: "Move to the specified location"
---

## Move

Move to the specified location. The entity will automatically pathfind towards the location and stop early if anything actively blocks the entity. `Move()` will throw an error when there is no path available, including when the entity is already on the specified location.
In most situations `Move()` should be excused to prevent unwanted errors.

### Inputs:
- Numeric: x position
- Numeric: y position
- [DEPRECATED] Bool: whether to move to the position or next to the position (Use `MoveTo()` instead!)

{% include links.html %}