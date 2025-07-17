# GitHub Image Test

Tests to see which image formats are supported by GitHub Markdown for README.

> [!NOTE]
> This test doesn't apply for GitHub Rich Text Editor.

## Animated Image

| **Constraint**    | **Value**  |
| :---------------- | :--------- |
| Width     | [830 px](./misc/width.md) |
| FPS       | [20 FPS](https://github.com/ImageOptim/gifski/issues/351) |
| File Size | [< 10 MB](https://github.com/github/docs/blob/2675b8e99f78b83d43907caca3ddb69deee0ce68/content/get-started/writing-on-github/working-with-advanced-formatting/attaching-files.md?plain=1#L47-L49) |

| Format | Command | Size |
| :----- | :------ | ---: |
| GIF    | `ffmpeg -i test.mp4 -f yuv4mpegpipe - \| gifski --width=830 --fps 20 --quality 59 -o test.gif -` | 9.8MB |
| WebP   | `ffmpeg -i test.mp4 -an -loop 0 -vf scale=830:-2,fps=fps=20 -c:v libwebp_anim -quality 84 test.webp` | 8.8MB |
| AVIF   | `ffmpeg -i test.mp4 -an -loop 0 -vf scale=830:-2,fps=fps=20 -c:v libsvtav1 -preset 6 -crf 23 test.avif` | 3.3MB |

### GIF

![GIF format](./animated/test.gif)

### WebP

![WebP format](./animated/test.webp)

### AVIF

![AVIF format](./animated/test.avif)
