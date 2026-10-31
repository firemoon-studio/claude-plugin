# Retro Camera

Claude plugin from [Firemoon Studio](https://firemoon.studio). Apply a fixed warm-film, monochrome or cool-chrome treatment to a photo. Only the colour changes; faces and scene contents are untouched. Returns a PNG.

This tool does not use AI to generate or redraw media. It is a fixed image filter, so the output contains only what was in your own image.

## Install

```
/plugin install firemoon-retro-camera@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `apply_photo_look` | Applies a fixed photo treatment | `look`: warm film, monochrome or cool chrome |

Limits: each source image must be a JPEG, PNG or WebP at a public `https://` URL, 20 MB or smaller.

## Examples

- "Give this photo a warm film look: (image link)"
- "Make this photo monochrome: (image link)"
- "Apply the cool chrome look to (image link)."

## Cost

Free. These edits do not use Firemoon credits. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/retro-camera/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the image URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source image from its URL to edit it.
- **Stored:** the result is saved as a PNG at a public link that anyone holding it can open. The source photo is downloaded to process it and is not kept.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
