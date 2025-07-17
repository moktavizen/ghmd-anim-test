# GitHub Image Test

Tests to see which image formats are supported by GitHub Markdown.

## Animated Image

| **Constraint**    | **Value**  |
| :---------------- | :--------- |
| Maximum File Size | [10 MB](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/attaching-files#supported-file-types) |
| Minimum FPS       | [20 FPS](https://github.com/ImageOptim/gifski/issues/351) |
| Minimum Width     | [830 px](./misc/min-width.png) |

### GIF

![GIF format](./animated/test.gif)

### WebP

![WebP format](./animated/test.webp)

### AVIF

![AVIF format](./animated/test.avif)
