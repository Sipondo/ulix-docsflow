---
title: Push
keywords: UPL Ulix Parsed Language Push
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_push.html
folder: upl_docs
summary: "Pushes a pillar, making the pillar fall down if above a gap."
---

## Push

Pushes a pillar in the given direction. The pillar becomes uninteractable and walkable if pushed into a hole.
Directions are given by single-letter capital-only strings `N` `W` `S` `E`.

### Inputs:
- String: direction to push to
- [Optional, 1] Numeric: distance that the movement should cover

{% include links.html %}