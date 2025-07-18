# GitHub Image Test

Tests which image formats are supported in GitHub README Markdown.

> [!NOTE]
> Doesn't apply for GitHub Rich Text Editor.

## Animated Image

| Constraint | Value |
|:-----------|:------|
| Width      | [830 px](./misc/width.md) |
| FPS        | [20 FPS](https://github.com/ImageOptim/gifski/issues/351) |

| Format | Command | Size |
|:-------|:--------|-----:|
| GIF    | `ffmpeg -i test.mp4 -vf scale=830:-2,fps=fps=20 -loop 0 -c:v gif test.gif` | 14MB |
| WebP   | `ffmpeg -i test.mp4 -vf scale=830:-2,fps=fps=20 -loop 0 -c:v libwebp_anim test.webp` | 6MB |
| AVIF   | `ffmpeg -i test.mp4 -vf scale=830:-2,fps=fps=20 -loop 0 -c:v libsvtav1 test.avif` | 2MB |

### MP4 — Source

![MP4 format](./animated/test.mp4)

### GIF

![GIF format](./animated/test.gif)

### WebP

![WebP format](./animated/test.webp)

### AVIF

![AVIF format](./animated/test.avif)
