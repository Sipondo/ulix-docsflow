---
title: Prompt
keywords: UPL Ulix Parsed Language Prompt
tags: [documentation, upl]
sidebar: guide_sidebar
permalink: upl_docs_prompt.html
folder: upl_docs
summary: "Retrieve text input from the player."
---

## Prompt

Ask a question and request text input from the player. Text inputs can be limited to a specified length and can be filtered on symbols.
The result is stored afterwards in `game.text_input`.

### Inputs:
- String: question to ask
- [Optional, 15] Numeric: max length of answer
- [Optional, "letters"] String: filter to use

{% include links.html %}