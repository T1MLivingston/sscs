# SSCS Brand Guide

A proposed brand guide for Seminole Science Charter School, Home of the Stingrays.
Logo artwork by Tim Livingston. Nothing here is approved school branding yet.

## What's in here

| Path | What it is |
|---|---|
| `index.html` | The brand guide website. One page. Logos, long logos, color layouts, palette, font, current logos, and the logo and GIF maker at the bottom. |
| `assets/img/` | Web-sized images the page uses (WebP). |
| `assets/js/maker.js` | The logo and GIF maker. Draws the real vector artwork and saves PNG, SVG, and GIF. |
| `logos/png/` | The original logo PNGs, full size, with their original file names. |
| `logos/svg/` | One SVG per Illustrator artboard, converted straight from the source file. |
| `source/SSCS_logo.ai` | The Illustrator source file (24 artboards). |
| `docs/SSCS_Proposed_Brand_Guide.pptx` | The slide deck version. Imports into Google Slides. |

## Run it

Open `index.html` in a browser. No build step. No dependencies.

The only outside request is the Montserrat font from Google Fonts.

## Put it online with GitHub Pages

1. Push this folder to a GitHub repo.
2. In the repo, go to Settings, then Pages.
3. Under "Build and deployment," choose "Deploy from a branch."
4. Pick the `main` branch and the `/ (root)` folder. Save.
5. The site appears at `https://<your-username>.github.io/<repo-name>/` after a minute or two.

The empty `.nojekyll` file tells GitHub to serve the files as they are.

## Brand basics

**Colors**

| Name | HEX | RGB | From |
|---|---|---|---|
| Stingray Navy | `#012F63` | 1, 47, 99 | Logo artwork |
| Stingray Red | `#DA152C` | 218, 21, 44 | Logo artwork |
| Stingray Grey | `#BEBEBE` | 190, 190, 190 | Logo artwork |
| Deep Navy | `#0D132E` | 13, 19, 46 | Orlando Science Schools logo |
| System Blue | `#315BA9` | 49, 91, 169 | Orlando Science Schools logo |
| White | `#FFFFFF` | 255, 255, 255 | |

These are screen values sampled from the exported files. Print values are not confirmed.

**Font:** Montserrat. Bold in all caps for headings, Regular for body. Free under the SIL Open Font License. It is in Google Slides and Docs under Font, then More fonts.

**Primary logo:** the circular seal.

## Known loose ends

- **Seal wording.** Two versions exist: "STEM Charter School" and "Charter School." Leadership has not picked one.
- **Two navies in the seal art.** The seal PNGs sample at `#003466` and `#042B56` with red `#D2122A`. Every other logo uses `#012F63` and `#DA152C`. The maker uses `#012F63` everywhere.
- **SVG colors.** The files in `logos/svg/` carry the color values stored in the Illustrator file, which read slightly different from the PNG exports (navy near `#013370`, red near `#E0182F`, grey near `#C6C6C6`). SVGs saved from the maker use the brand HEX values above.
- **SVG lettering.** Text in `logos/svg/` is converted to shapes, not live text.
- **Side stingray has no circle version.** None was drawn.
- **System colors are estimates.** Deep Navy and System Blue were sampled from a small web image. Ask Orlando Science Schools for official values.
- **No license file.** Add one before making the repo public, and decide who may use the logos.

## Where things came from

- Current-logo images in `assets/img/` (`oss`, `web`, `oldSeal`) were saved from orlandoscience.org and seminolescience.org in October 2026.
- The logo PNG folder on Google Drive: https://drive.google.com/drive/folders/12I6X4qPKyHAG0oh1OoSHPk0NDSjnXlD_?usp=sharing
