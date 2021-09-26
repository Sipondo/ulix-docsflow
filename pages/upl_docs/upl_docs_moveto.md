---
title: MoveTo
keywords: UPL Ulix Parsed Language MoveTo
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_moveto.html
folder: upl_docs
summary: "Move one tile next to the specified location"
---

## MoveTo

Move one tile next to the specified location. The entity will automatically pathfind towards the location and stop early if anything actively blocks the entity. `Move()` will throw an error when there is no path available, including when the entity is already on the specified location.
In most situations `Move()` should be excused to prevent unwanted errors.

### Inputs:
- Numeric: x position
- Numeric: y position

{% include links.html %}