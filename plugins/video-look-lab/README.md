# Video Look Lab

Claude plugin from [Firemoon Studio](https://firemoon.studio). Apply a natural, warm, cool or monochrome colour preset to a short video, with an optional exposure adjustment. Geometry, timing and audio are unchanged.

This tool does not use AI to generate or redraw media. It is a fixed ffmpeg operation, so the output contains only what was in your own video.

## Install

```
/plugin install firemoon-video-look-lab@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `grade_video` | Applies a colour preset | `look`: natural, warm, cool or monochrome; `exposure`: -50 to 50 |

Limits: each source video must be an MP4 or MOV at a public `https://` URL, 10 seconds or shorter, and 50 MB or smaller.

## Examples

- "Give https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522617447.mp4 a warm look."
- "Make https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522621250.mp4 black and white."
- "Apply a cool grade to https://jxzwlpbdjhikca2p.public.blob.vercel-storage.com/generated-video-1789522627252.mp4 and brighten it a little."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/video-look-lab/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the video URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source video from its URL to edit it.
- **Stored:** the edited video is saved to private storage on your Firemoon account. Claude gets a result link and a download link that work for anyone holding them and expire after 24 hours. Source videos are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
