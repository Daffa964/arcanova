# ARCANOVA UI Foundation

First deliverable: style guide and component sheet only. The foundation is built for a 1920×1080 stage that scales down responsively while preserving a 16:9 composition.

## Files
- `tokens.css`: palette, typography, spacing, radii, shadows, easing, z-index map.
- `components.css`: stage, panels, relic buttons, state switcher, cards, stat tokens, life bar.
- `screens/style-guide.html`: executable visual reference with state switcher.

## Design tokens
Colors: ink `#080a10`, panel `#101522`, gold `#e5a93b`, bronze `#b8793a`, ember `#ff6a2a`, ice `#4fd0ff`, trap `#9b6bd6`, paper `#f2ebdd`, muted `#9aa0b4`, life `#2ecc71`, danger `#d9473f`.
Typography: Cinzel for display/card names; Rajdhani for body, controls, and stats. Spacing uses 8px increments. Motion uses `cubic-bezier(.2,.75,.2,1)` with 160–220ms transitions; reduced motion disables animation.

## Component inventory and states
- Relic button: default, hover (provided hover plate), pressed (provided pressed plate), focus, disabled, loading.
- Panel: bronze inlay border, corner-safe padding, inner shadow, compact HUD density.
- Card: real card art asset, hover lift, selected gold focus ring, dim/unavailable treatment.
- Stat token: attribute/stat asset icon, label, value; never color-only.
- Life bar: provided `lifebar_frame.webp`, numeric LP is always visible.
- State switcher: keyboard-focusable buttons for default, selected, dim, and loading previews.

## Asset map
- Buttons: `assets/ui/button_normal.webp`, `button_hover.webp`, `button_pressed.webp`
- Life points: `assets/ui/lifebar_frame.webp`
- Card frames and backs reserved for card/duel screens: `assets/frames/frame_monster.webp`, `frame_spell.webp`, `frame_trap.webp`, `card_back.webp`
- Icons: `assets/ui/icons/*`
- Style guide sample art: Magma Drake, Frostfang, Dragon's Breath under `assets/cards/`
- Arena art: `assets/arenas/arena_default.webp`

## Z-index map
`0` base, `1` arena art, `10` panels, `20` HUD, `40` modal, `60` toast/state controls.

## Interaction and accessibility notes
All controls are native buttons with visible `:focus-visible` rings and at least 44px touch height. Hover is never the only state cue: selection uses a gold outline and dim uses reduced opacity plus grayscale. Use `aria-pressed` for state switchers and descriptive alt text for non-decorative images. Keep body copy at 16px or larger at base resolution. Future screens should retain compact edge HUDs so the arena remains the visual focus.
