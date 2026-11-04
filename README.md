# Lily: ASCII Lily Bouquet

An animated bouquet of lilies drawn as coloured text characters, built with plain HTML, CSS and JavaScript. No libraries.

**Live demo:** https://vibhaedward17.github.io/Lily/

## What it does

- Draws 11 vector lilies (red, pink, cream, yellow, peach) with stems and leaves
- Makes them sway in the wind
- Turns every frame into coloured ASCII characters
- Lets you push the stems by moving your pointer over the bouquet
- Has 3 character sets (Symbols, Blocks, Code) and a "Show vectors" button to see the drawing under the text

## How it works

1. The lilies are drawn on a hidden canvas using bezier curves and gradients.
2. Each frame, that canvas is shrunk to a small grid, so one pixel becomes one future character.
3. For every pixel, the code reads its colour and brightness with `getImageData`.
4. Brighter pixels get denser characters (for example `.` for dim, `@` for bright).
5. Each character is drawn on the visible canvas in the pixel's own colour.
6. `requestAnimationFrame` repeats this every frame.

## Run it on your computer

1. Download or clone this repo.
2. Open `index.html` in your browser. You can also use the VS Code Live Server extension.

The fonts load from Google Fonts, so you need internet the first time. Without it, a fallback font is used.

## Built with

- HTML5 Canvas
- Vanilla JavaScript
- CSS

## Idea

Inspired by an ASCII lily bouquet reel on Instagram by @arimecoa.
