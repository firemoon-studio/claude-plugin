---
name: video-tools
description: Make quick fixed edits to a short video with Firemoon Tools. Use when the user wants to crop a video to portrait, landscape or square, speed it up or slow it down, remove its audio, turn part of it into a GIF, or trim and join two to four clips.
---

# Firemoon Tools

Every tool takes a public `https://` link to an MP4 or MOV file. Each source must be 10 seconds or shorter and 50 MB or smaller. If the user only has a local file, ask them to upload it somewhere that gives a public HTTPS link first.

Pick the tool from what the user asks for:

| The user wants to | Tool | Settings to confirm |
| --- | --- | --- |
| Reframe for Reels, Shorts, a feed or widescreen | `crop_video` | `format`: `portrait`, `square` or `landscape` |
| Speed up or slow down | `change_video_speed` | `rate`: 0.5, 0.75, 1.25, 1.5 or 2 |
| Strip the sound | `remove_audio` | none |
| Make a GIF | `make_gif` | `start` and `end` (at most 5 seconds apart), `width`, `fps` |
| Combine clips | `join_clips` | each clip's `start` and `end`, in order, and the `format` |

`crop_video` crops from the center. Tell the user to check that the subject is still in frame.

These are fixed edits. They do not generate, extend or restyle footage. If the user asks for that, say these tools can't do it.

## Results

Each call returns a result link and a download link. Both expire after 24 hours, so tell the user to download anything they want to keep.

If a call is interrupted or times out, call the same tool again with the `request_id` from the error message. That recovers the original job instead of starting a second one.

## Sign-in

The first call asks the user to sign in to Firemoon. These edits are free and do not use Firemoon credits.
