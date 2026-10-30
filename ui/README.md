# Arcanova UI foundation

Open `screens/style-guide.html` in a browser. The sheet is self-contained and uses the supplied rune plate, frame, icon, arena, card, and card-back assets.

- `tokens.css`: color, type, spacing, radius, elevation, motion, and z-index tokens.
- `components.css`: panels, controls, HUD, card states, responsive rules, and accessibility focus ring.
- `screens/style-guide.html`: the single visual component sheet with a state switcher.

Card art and frame overlays follow the normalized placement values in `assets/frames/frame_layout.json`; frame-specific art windows are encoded as CSS custom properties on `.card`, `.card.spell`, and `.card.trap`.
