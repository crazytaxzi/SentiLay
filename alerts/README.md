# Cinder HellGlass Holo AlertBox Theme

This theme is designed for the native StreamElements **AlertBox**, not a separate Custom Widget. That means the existing alert queue, sounds, media, event filters, and emulation controls remain intact.

## Files

- `HTML.txt`
- `CSS.txt`
- `JS.txt`

Use the same three files for each alert type you want themed:

- Followers
- Subscribers
- Tips
- Cheers / Bits
- Raids
- Hosts, if still used on the connected platform

## Installation

1. Open the StreamElements overlay containing the stock AlertBox.
2. Select the AlertBox.
3. Open the first alert type, such as **Followers**.
4. Enable **Custom CSS / Custom Code** for that alert type.
5. Open the code editor.
6. Paste `HTML.txt`, `CSS.txt`, and `JS.txt` into their matching tabs.
7. Save the alert type.
8. Repeat for Subscribers, Cheers, Raids, Tips, and any other alert types you use.
9. Use StreamElements **Emulate** to test each alert type.

## What stays controlled by StreamElements

- alert duration
- sound selection and volume
- video/media selection
- event thresholds
- text announcement configured for that alert type
- alert queue and skip controls

## Recommended settings

- Widget canvas: at least `900 × 500`
- Alert duration: `7–10 seconds`
- Keep large stock animations disabled or choose a transparent WebM so the HellGlass plate remains the focus.
- Use short announcement text, because the viewer name already appears as the large center line.

## Template variables used

- `{{name}}`
- `{{announcement}}`
- `{{amount}}`
- `{{message}}`
- `{{video}}`
- `{{audio}}`
- `{{widgetDuration}}`
