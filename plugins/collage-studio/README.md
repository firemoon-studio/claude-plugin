# Collage Studio

Claude plugin from [Firemoon Studio](https://firemoon.studio). Arrange two to six photos into a square grid, a 9:16 story or a single-column strip, with your choice of gap and background colour. Returns a PNG.

This tool does not use AI to generate or redraw media. It is a fixed image filter, so the output contains only what was in your own image.

## Install

```
/plugin install firemoon-collage-studio@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `make_collage` | Arranges photos into a collage | `photos`, `layout` (grid, story or strip), `fit`, `gap`, `background` |

Limits: each source image must be a JPEG, PNG or WebP at a public `https://` URL, 20 MB or smaller.

## Examples

- "Make a grid collage of these photos: (2 to 6 image links)"
- "Put these three photos in a vertical story layout with no gaps: (image links)"
- "Make a strip of these photos on a black background: (image links)"

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/collage-studio/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the image URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source image from its URL to edit it.
- **Stored:** the collage is saved as a PNG at a public link that anyone holding it can open. Source photos are downloaded to build it and are not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
