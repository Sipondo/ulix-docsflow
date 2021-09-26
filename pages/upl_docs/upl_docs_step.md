---
title: Step
keywords: UPL Ulix Parsed Language Step
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_step.html
folder: upl_docs
summary: "Take a step in the specified direction."
---

## Step

Take a step in the specified direction. Directions are given by single-letter capital-only strings `N` `W` `S` `E`.
`Step()` will throw an error if the step is blocked. Fou should excuse `Step()` if this is a possibility.

### Inputs:
- String: direction

{% include links.html %}