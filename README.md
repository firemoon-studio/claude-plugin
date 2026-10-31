# Firemoon Tools

Claude plugin for quick, fixed edits to short videos. Crop a clip to portrait, square or landscape, change its speed, remove its audio, turn part of it into a GIF, or trim and join two to four clips. Every edit runs through [Firemoon Studio](https://firemoon.studio)'s remote [Model Context Protocol](https://modelcontextprotocol.io/) server.

These tools do not use AI models. Each one is a fixed ffmpeg operation, so the output contains only frames and sound from your own clips.

## Install

```
/plugin install firemoon-tools@claude-plugins-official
```

The first time Claude calls a tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tools

| Tool | What it does | Settings |
| --- | --- | --- |
| `crop_video` | Center-crops a video, keeping timing and audio | `format`: landscape (1280×720), portrait (720×1280) or square (720×720) |
| `change_video_speed` | Speeds a video up or slows it down; audio tempo follows | `rate`: 0.5, 0.75, 1.25, 1.5 or 2 |
| `remove_audio` | Removes every audio track | none |
| `make_gif` | Exports up to 5 seconds as a looping GIF, with no audio | `start`, `end`, `width` (320, 480 or 640), `fps` (8, 12 or 15) |
| `join_clips` | Trims two to four clips and joins them in order, padded to one frame size | each clip's `start` and `end`, `format` |

Limits: each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller.

## Examples

- "Crop https://example.com/launch.mp4 to portrait for Reels."
- "Make a 3-second GIF of https://example.com/demo.mp4 starting at 2 seconds, 480 pixels wide."
- "Take the first 4 seconds of https://example.com/a.mp4 and seconds 1 to 5 of https://example.com/b.mp4 and join them as a square video."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/tools/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the video URLs you give Claude and the edit settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source video from its URL to edit it.
- **Stored:** the edited video is saved to private storage on your Firemoon account. Claude gets a result link and a download link that work for anyone holding them and expire after 24 hours. Source videos are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to a tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
