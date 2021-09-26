---
title: Teleport
keywords: UPL Ulix Parsed Language Teleport
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_teleport.html
folder: upl_docs
summary: "Teleports the user to the specified location in a different map."
---

## Teleport

Teleports the user to the specified location in a different map. This function should be used in all custom actions that require map travel.

### Inputs:
- String: level to teleport to
- Tuple of numeric of length 2: position to teleport to
- [Optional, False] Bool: whether to fade to the target map

{% include links.html %}