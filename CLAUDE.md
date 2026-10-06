# Notes for Claude Code

This repo is a static, single-page brand guide site. No framework, no build step, no package manager. Keep it that way unless asked.

## Layout

- `index.html` holds the page markup and all site CSS (in one `<style>` block).
- `assets/js/maker.js` holds the logo and GIF maker. It is one IIFE.
- Maker styles are scoped under `#maker` inside the same `<style>` block.
- Images are in `assets/img/` and referenced with relative paths.

## Conventions

- One font: Montserrat. Headings are bold and uppercase.
- Colors are CSS custom properties on `:root`. Dark mode overrides them under `prefers-color-scheme` and `[data-theme]`. Logo tiles stay white in both themes.
- Copy is short and plain. No em dashes.
- Do not redraw, recolor, or retype the logo artwork. Treat `logos/` and `source/` as read-only originals.

## How the maker works

- `MARKS` (top of `maker.js`) is a table of logos. Each has a `w` and `h` (viewBox), a list of `layers` (SVG path data plus a color role), and motion settings.
- Color roles: `main` (wing), `accent` (belly), `outline`, `ring`, `fill`, `text`, plus `bg`.
- `scheme(preset, bg, mark)` picks ring, fill, and lettering colors for a circle preset and background.
- `draw(ctx, size, pose, colors, opts)` renders one frame to a canvas. PNG, the live preview, the preset thumbnails, and every GIF frame all go through it.
- `pose(t, hold, mode, anim)` gives the motion at time `t` for one of the animations in `ANIMS` (swim, swing, slide, zoom). `timing(anim)` gives each one's in and out lengths.
- `draw` paints the circle and lettering first and the stingray last, so the stingray covers the lettering as it moves. At rest this matches the artwork's stacking exactly.
- The preview plays on load unless the viewer prefers reduced motion. "Random GIF" picks an animation, circle, background, and exit for the current logo.
- `svgText()` builds the SVG export from the same layers.
- `makeGif(size, onProgress)` is a small built-in GIF encoder (palette, LZW, frame diffing). No library.
- Saving: on claude.ai it uses the `downloads` capability. Anywhere else it falls back to a normal browser download. Leave both paths in place.
- The path data in `MARKS` was extracted from `source/SSCS_logo.ai` (artboards 1, 2, 3, 6, 7, 9, 17, 18). If the artwork changes, that table has to be regenerated.

## Good next steps, if asked

- Split the site CSS into `assets/css/site.css`.
- Add a favicon and social preview image made from the seal.
- Add a LICENSE and a short usage policy for the logos.
