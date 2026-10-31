# Color Match

Claude plugin from [Firemoon Studio](https://firemoon.studio). Apply global colour adjustments to a photo: temperature, brightness, contrast and saturation from -100 to 100, and gamma from 0.2 to 2.2.

This tool does not use AI to generate or redraw media. It is a fixed image filter, so the output contains only what was in your own image.

## Install

```
/plugin install firemoon-color-match@claude-plugins-official
```

The first time Claude calls the tool, it asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

## Tool

| Tool | What it does | Settings |
| --- | --- | --- |
| `color_grade_photo` | Applies global colour adjustments | `look`: `temperature`, `brightness`, `contrast`, `saturation`, `gamma` |

Limits: each source image must be a JPEG, PNG or WebP at a public `https://` URL, 20 MB or smaller.

## Examples

- "Warm up this photo a little and add some contrast: (image link)"
- "Make this photo brighter and less saturated: (image link)"
- "Cool down this photo: (image link)"

## Cost

4 Firemoon credits per photo. You need a Firemoon account to sign in.

## What the plugin sends and stores

The plugin adds one remote MCP server, `https://mcp.firemoon.studio/claude/color-match/mcp`. It contains no local code, hooks or scripts.

- **Sent to Firemoon:** the image URLs you give Claude and the settings for each call. Your Firemoon sign-in token is sent with every request.
- **Fetched:** Firemoon downloads each source image from its URL to edit it.
- **Stored:** the corrected image is saved to your Firemoon account. Claude gets a link to it.
- **Not collected:** your conversation, prompts, or files you did not pass to the tool.

Firemoon's privacy policy: https://firemoon.studio/privacy. Terms: https://firemoon.studio/terms.

## Support

https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
