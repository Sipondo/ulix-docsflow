---
title: Ask
keywords: UPL Ulix Parsed Language Ask
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_ask.html
folder: upl_docs
summary: "Ask a multiple choice question."
---

## Ask

Ask the player a multiple choice question. Game must be in cinematic mode for the question to load properly.
Selected answer is stored afterwards in `game.selection` (id) and `game.selection_text` (option name).

### Inputs:
- String: question
- List of strings: options

{% include links.html %}