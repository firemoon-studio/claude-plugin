# GIF Studio

Claude plugin from [Firemoon Studio](https://firemoon.studio). Export up to five seconds of a short video as a looping GIF, at 320, 480 or 640 pixels wide and 8, 12 or 15 frames per second. GIFs have no audio.

This tool does not use AI to generate or redraw media. It is a fixed ffmpeg operation, so the output contains only what was in your own video.

## Install

```
/plugin install firemoon-gif-studio@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `make_gif` | Exports up to 5 seconds as a looping GIF | `start`, `end`, `width` (320, 480 or 640), `fps` (8, 12 or 15) |

Limits: each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller.

## Examples

- "Make a 3-second GIF of https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522621250.mp4 starting at 1 second, 480 pixels wide."
- "Turn the first 2 seconds of https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522617447.mp4 into a small 320-pixel GIF."
- "Make a 15 fps GIF of seconds 2 to 5 of https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522627252.mp4."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/gif-studio/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the video URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source video from its URL to edit it.
- **Stored:** the edited video is saved to private storage on your Firemoon account. Claude gets a result link and a download link that work for anyone holding them and expire after 24 hours. Source videos are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
