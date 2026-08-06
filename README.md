# Cinder Hellglass Chat for StreamElements

A transparent, message-by-message chat overlay with smoked glass, violet/cyan/pink edge lighting, compact bot messages, Twitch badges/emotes, automatic fading, message deletion support, and configurable fields.

## Install

1. Open your StreamElements overlay.
2. Add **Static / Custom > Custom widget**.
3. Open the widget's **Settings**, then choose **Open Editor**.
4. Replace each tab with the matching file:
   - HTML tab: `HTML.txt`
   - CSS tab: `CSS.txt`
   - JS tab: `JS.txt`
   - FIELDS tab: `FIELDS.json`
5. Save the editor, then save the overlay.
6. Set the widget to roughly **900 × 520** on a 2560 × 1440 canvas and place it near the lower-left edge.
7. Use **Emulate > Chat message** to test it.

## Recommended starting settings

- Maximum messages: 7
- Lifetime: 26 seconds
- Glass opacity: 38
- Blur: 12
- Font size: 26
- Glow: 62
- Compact bots: enabled

The bot list defaults to StreamElements, Nightbot, Streamlabs, and Blerp. Remove `blerp` if you want Blerp messages to use the full viewer styling, or add any other bot names you use.

## Notes

- The widget stores `msgId` and `userId`, so moderator deletions remove messages from the overlay.
- All chat text is HTML-escaped before display.
- StreamElements filtering is enabled by default through `SE_API.sanitize`.
- Google Fonts are loaded in the CSS. If the font service is unavailable, the widget falls back to Segoe UI.
