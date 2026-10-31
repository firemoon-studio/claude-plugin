# Vertical Remix

Claude plugin from [Firemoon Studio](https://firemoon.studio). Reframe a short video to 9:16, 1:1 or 4:5. Crop fills the new frame by trimming the edges; pad keeps the whole frame and adds bars.

This tool does not use AI to generate or redraw media. It is a fixed ffmpeg operation, so the output contains only what was in your own video.

## Install

```
/plugin install firemoon-vertical-remix@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `reframe_video` | Reframes to a new aspect ratio | `aspect_ratio`: 9:16, 1:1 or 4:5; `mode`: crop or pad |

Limits: each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller.

## Examples

- "Reframe https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522627252.mp4 to 9:16 with padding so nothing is cut off."
- "Make https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522617447.mp4 4:5 for an Instagram feed post."
- "Crop https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522621250.mp4 to 1:1."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/vertical-remix/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the video URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source video from its URL to edit it.
- **Stored:** the edited video is saved to private storage on your Firemoon account. Claude gets a result link and a download link that work for anyone holding them and expire after 24 hours. Source videos are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
