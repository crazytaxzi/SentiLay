# SentiLay

SentiLay is the StreamElements overlay pack for your Cinder-themed stream HUD.

Current widgets included:

1. **Cinder HellGlass Holo Chat**
2. **Cinder HellGlass Holo Trackers**

Both widgets use the same design language:

- dark transparent HellGlass surfaces
- neon green primary glow
- neon purple secondary refraction
- soft holographic projector field from the bottom
- subtle dust particles
- transparent backgrounds for OBS / StreamElements use

---

## 1) Cinder HellGlass Holo Chat

### Files

Use these files in a StreamElements **Custom Widget**:

- `HTML.txt`
- `CSS.txt`
- `JS.txt`
- `FIELDS.json`

These root-level files are the chat widget.

### Notable behavior

- keeps HellGlass chat bubbles
- adds holo-projector ambience behind the chat stack
- dust particles are visible only while at least one message is on screen
- pushes older messages out for newer ones using both message count and actual visible height
- optional compact bot styling
- optional full hiding of listed bot usernames
- supports badge rendering, emotes, moderator deletions, and StreamElements message filtering

### Recommended starting size

- **900 × 520** on a 2560 × 1440 overlay
- place near the lower-left corner

### Suggested starting settings

- Maximum visible messages: `7`
- Message lifetime: `26`
- Hide listed bots entirely: `off`
- Compact listed bots: `on`
- Dust particle count: `16`

---

## 2) Cinder HellGlass Holo Trackers

### Files

Use a second StreamElements **Custom Widget** with the files in the `trackers/` folder:

- `trackers/HTML.txt`
- `trackers/CSS.txt`
- `trackers/JS.txt`
- `trackers/FIELDS.json`

### What it includes

One combined tracker module containing:

- Bits Goal
- Subscription Goal
- Follower Goal

### Behavior

- three stacked HellGlass goal cards
- one shared holo-projector field behind the whole stack
- subtle dust particles inside the projection field
- animated sheen pulse when a goal updates
- progress bars fill in neon green with purple edge tint
- listens for `cheer-latest`, `subscriber-latest`, and `follower-latest`
- starts from the current and goal values defined in Fields

### Recommended starting size

- **520 × 180** to **620 × 220**
- place near the lower-right corner

### Suggested starting values from your current layout

- Bits: `1505 / 5000`
- Subs: `168 / 250`
- Followers: `1713 / 1800`

---

## Install steps

1. Open your StreamElements overlay.
2. Add a **Custom Widget** for chat.
3. Paste the root `HTML.txt`, `CSS.txt`, `JS.txt`, and `FIELDS.json` into the widget editor.
4. Add a second **Custom Widget** for trackers.
5. Paste `trackers/HTML.txt`, `trackers/CSS.txt`, `trackers/JS.txt`, and `trackers/FIELDS.json` into that widget editor.
6. Save both widgets and save the overlay.
7. Test chat with **Emulate > Chat message**.
8. Test tracker reactions with StreamElements event emulation if available, or wait for live events.

---

## Notes

- If you want bot usernames fully hidden in chat, enable **Hide listed bots entirely**.
- If you want bot messages visible but quieter, leave hiding off and keep **compact styling** on.
- The tracker widget uses configured starting values and then increments from live events.
- The next visual step after this pack would be matching alert styling.
