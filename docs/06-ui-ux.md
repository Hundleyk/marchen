# 06 · UI and UX

## Principles

1. **The body is the HUD.** Breath, stance and danger are shown on Nix, not on screen.
2. **Storybook frame.** Menus look like pages of a fairy-tale book: cream paper, soft watercolour washes, handwritten script beside clean sans type (matches the extraordinary. games brand).
3. **Nothing urgent unless it's urgent.** No timers on screen; no flashing alerts outside encounters.

## In-game HUD

| Element | Where | Behaviour |
|---|---|---|
| Breath | On Nix (bubble clusters) | Below 25%: a faint ring of bubbles appears around the screen edge and Nix's expression goes Concerned |
| Stance | On Nix (fin and skin tint) + a small shell icon bottom-left | Icon flips lilac/coral on Q; fades after 2 s |
| Tide level | Small wave glyph bottom-left beside stance | Shows Ebb / Slack / Flood; animates during transitions |
| Interaction prompt | Above the object | Key glyph + verb ("E · Soothe") |
| Thread marker | In world | Glows only in Listen mode; a faint shimmer outside it once discovered |
| Pearl pickup | Top-right toast | "Pearl 4/10", 2 s |

Toggle: **HUD minimal** hides stance and tide icons entirely (body reads only).

## Screens

### Title
* Cream page; the coast painted in watercolour; the title in handwritten script.
* *Continue · New Tale · Settings · Quit*
* A gentle wave animates across the bottom; music is the hub theme on harp.

### Pause / Journal (Tab)
A book with tabs:
* **Tales:** each district as a page; stuck beats listed with a small illustration that fills in as restored.
* **Map:** a hand-drawn coast; districts unlock as discovered; tide state shown per district.
* **Keepsakes:** items and tale memories (Soft/Strong rewards).
* **Necklace:** the shells collected, with ability descriptions.
* **Settings.**

### Dialogue
* Portrait panel bottom-left showing one of the six expressions.
* Name in script, text in sans, typewriter reveal (skippable).
* Choices appear as two shells: **lilac (Soft)** on the left, **coral (Strong)** on the right. Neutral options sit in the middle.
* The in-world model's face swaps to match the portrait.

### Tale ending
* The screen folds into storybook panels (3–5 illustrated stills) with narrated text.
* Ends on the new shell joining the necklace, with the ability unlock card.

## Controls

| Action | KB/M | Gamepad |
|---|---|---|
| Move | WASD | Left stick |
| Camera | Mouse | Right stick |
| Jump / float (hold) | Space | A |
| Glide (Soft) / Surge (Strong) | Shift | B |
| Switch nature | Q | Y |
| Interact / tide stone / soothe (hold) | E | X |
| Listen (hold) | F | LB |
| Wave push | LMB | RT |
| Journal | Tab | Select |
| Pause | Esc | Start |

All bindings remappable.

## Accessibility

* **Breath bar option:** a conventional bar for players who can't read the bubble meter.
* **Colour-safe stance:** stance also shown by shape (round shell = Soft, spiked shell = Strong), never colour alone.
* **Hold-to-toggle** for Listen, Soothe and Glide.
* **Subtitles** on by default, with speaker names and size options.
* **Camera:** sensitivity, invert, reduce camera drift (turns off the underwater sway).
* **Motion:** reduce screen-edge bubble effect and wave transitions.
* **Encounter assist:** the Stopped's patterns slow by 30%; Unfinished push without Breath loss.

## Feedback language

| Event | Visual | Audio |
|---|---|---|
| Breath spent | Bubble pops off | Pitched pop in the district's key |
| Breath refilled | Bubbles re-form with a shimmer | Rising glassy chime |
| Stance switch | Tint wave across Nix | Soft: harp gliss; Strong: low cello stab |
| Tide change | Wave front sweeps the district | Long surf swell |
| Thread found | Glow + fins flare | Single celesta note |
| Beat restored | Freeze-frame releases | District theme gains a layer |
