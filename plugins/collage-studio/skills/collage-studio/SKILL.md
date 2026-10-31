---
name: collage-studio
description: Use when the user wants to combine two to six photos into a collage, grid, story or strip.
---

# Collage Studio

Each source image must be a JPEG, PNG or WebP at a public `https://` URL, 20 MB or smaller. If the user only has a local file, ask them to upload it somewhere that gives a public HTTPS link first.

`contain` keeps each whole photo; `cover` crops to fill each cell.

This is a fixed edit. It does not generate, extend or restyle anything. If the user asks for that, say this tool can't do it.

## Results

Each call returns a result link and a download link.

## Sign-in

The first call asks the user to sign in to Firemoon.
