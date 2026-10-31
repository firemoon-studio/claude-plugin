# Firemoon for Claude

Eleven Claude plugins from [Firemoon Studio](https://firemoon.studio), one per tool. Each one makes a fixed edit to a video or photo you link to. None of them use AI to generate or redraw media.

| Plugin | What it does | Remote MCP server |
| --- | --- | --- |
| [Video Crop](plugins/video-crop) | Center-crop short videos to portrait, square or landscape for Reels, Shorts and feeds. | `https://mcp.firemoon.studio/claude/video-crop/mcp` |
| [GIF Studio](plugins/gif-studio) | Turn up to five seconds of a short video into a looping GIF. | `https://mcp.firemoon.studio/claude/gif-studio/mcp` |
| [Speed Studio](plugins/speed-studio) | Speed up or slow down short videos, with audio tempo matched. | `https://mcp.firemoon.studio/claude/speed-studio/mcp` |
| [Silent Cut](plugins/silent-cut) | Remove the audio from short videos. | `https://mcp.firemoon.studio/claude/silent-cut/mcp` |
| [Clip Composer](plugins/clip-composer) | Trim two to four short videos and join them in order. | `https://mcp.firemoon.studio/claude/clip-composer/mcp` |
| [Privacy Blur](plugins/privacy-blur) | Blur a fixed area of a short video, such as a licence plate or a screen. | `https://mcp.firemoon.studio/claude/privacy-blur/mcp` |
| [Video Look Lab](plugins/video-look-lab) | Apply fixed colour presets to short videos. | `https://mcp.firemoon.studio/claude/video-look-lab/mcp` |
| [Vertical Remix](plugins/vertical-remix) | Reframe short videos to 9:16, 1:1 or 4:5 by cropping or padding. | `https://mcp.firemoon.studio/claude/vertical-remix/mcp` |
| [Collage Studio](plugins/collage-studio) | Arrange two to six photos into a grid, story or strip. | `https://mcp.firemoon.studio/claude/collage-studio/mcp` |
| [Retro Camera](plugins/retro-camera) | Give photos a warm-film, monochrome or cool-chrome look. | `https://mcp.firemoon.studio/claude/retro-camera/mcp` |
| [Color Match](plugins/color-match) | Correct the colour of photos: temperature, brightness, contrast, saturation and gamma. | `https://mcp.firemoon.studio/claude/color-match/mcp` |

## Install

Add this marketplace, then install the plugins you want:

```
/plugin marketplace add firemoon-studio/claude-plugin
/plugin install firemoon-video-crop@firemoon
```

The first tool call asks you to sign in to Firemoon. There is no API key to configure. You can revoke access at any time from https://firemoon.studio/keys.

Each plugin's README covers its tool, limits, cost and data handling. Privacy policy: https://firemoon.studio/privacy. Support: https://firemoon.studio/support or support@firemoon.studio.

## License

MIT. See `LICENSE`.
