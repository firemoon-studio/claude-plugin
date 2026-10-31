# Speed Studio

Claude plugin from [Firemoon Studio](https://firemoon.studio). Play a short video at 0.5×, 0.75×, 1.25×, 1.5× or 2× speed. The audio tempo is adjusted to match.

This tool does not use AI to generate or redraw media. It is a fixed ffmpeg operation, so the output contains only what was in your own video.

## Install

```
/plugin install firemoon-speed-studio@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `change_video_speed` | Speeds a video up or slows it down; audio tempo follows | `rate`: 0.5, 0.75, 1.25, 1.5 or 2 |

Limits: each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller.

## Examples

- "Slow https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522617447.mp4 down to half speed."
- "Speed up https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522621250.mp4 to 2x."
- "Play https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522627252.mp4 at 1.5x speed."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/speed-studio/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the video URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source video from its URL to edit it.
- **Stored:** the edited video is saved to private storage on your Firemoon account. Claude gets a result link and a download link that work for anyone holding them and expire after 24 hours. Source videos are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
