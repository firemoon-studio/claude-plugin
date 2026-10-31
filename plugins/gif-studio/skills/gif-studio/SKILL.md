---
name: gif-studio
description: Use when the user wants to turn part of a short video into a GIF.
---

# GIF Studio

Each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller. If the user only has a local file, ask them to upload it somewhere that gives a public HTTPS link first.

`end` must be after `start` and at most 5 seconds later. Larger widths and frame rates give bigger files.

This is a fixed edit. It does not generate, extend or restyle anything. If the user asks for that, say this tool can't do it.

## Results

Each call returns a result link and a download link. Both expire after 24 hours, so tell the user to download anything they want to keep.

If a call is interrupted or times out, call the same tool again with the `request_id` from the error message. That recovers the original job instead of starting a second one.

## Sign-in

The first call asks the user to sign in to Firemoon.
