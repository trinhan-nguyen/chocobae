# 💌 Anniversary Card

A little self-contained web card for your 2-year anniversary. Open as a sealed envelope →
tap → it unfolds into your letter, a photo timeline of your two years, floating hearts, and
your song. Works on any phone or computer, no internet needed to open locally.

---

## 1. Make it yours (5 minutes)

Open **`index.html`** in any text editor and edit the **`CONFIG` block near the top of the
`<script>`** — it's clearly marked with `✏️ EDIT EVERYTHING IN THIS BLOCK`. You only touch
this part:

- `herName` / `fromName` — her name and how you sign off.
- `anniversaryDate` — the day you got together (`YYYY-MM-DD`). Powers the "days together" counter.
- `letterText` — your message. Line breaks are kept, so write it however feels right.
- `memories` — your milestones. Each entry is flexible (see below).

## 2. The timeline — moments vs. trips

The timeline adapts to how many photos each entry has, so the early days don't need photos to
look good:

- **A text-only "moment"** — just `{ date, title, text }`, no photos. Renders as a slim note.
  Great for the early days when you don't have pictures.
- **A "trip"** — add `place: "Da Lat"` to give it a 📍 pin and show the location.
- **Photos** — add `photos: ["assets/photos/dalat-1.jpg", "assets/photos/dalat-2.jpg"]`.
  One photo shows as a single card; two or more become a **swipeable photo strip** with dots.

Example:

```js
{ date: "Aug 2024", title: "Our first trip", place: "Da Lat",
  text: "Getting lost together and not minding one bit.",
  photos: ["assets/photos/dalat-1.jpg", "assets/photos/dalat-2.jpg"] },
```

## 3. Add photos

Drop your photos into **`assets/photos/`** and reference them by path in each entry's `photos`
array (any filenames you like, e.g. `dalat-1.jpg`). Landscape-ish photos look best (shown 4:3).
Missing photos just hide themselves — nothing breaks.

## 4. Add the song (when you have it)

Put the audio file at **`assets/song.mp3`** (or change `songFile` in `CONFIG` to its path).
The song **starts playing automatically the moment she taps to open the envelope** (that tap
counts as the user gesture browsers require, so it isn't blocked). A round ♪ button in the
corner lets her **pause/resume**. If no song is added yet, nothing plays and the button stays
hidden — the rest of the card works fine.

## 5. Preview it

Just double-click `index.html` to open it in your browser. Tap the envelope to test the
whole thing. Use your browser's responsive/phone view to see how it'll look on her screen.

---

## 6. It's already online 🎉

The card is live at:

```
https://trinhan-nguyen.github.io/chocobae/
```

(repo: `trinhan-nguyen/chocobae`, GitHub Pages serving the `master` branch).

**To publish any change** — after editing the letter, photos, or memories — just push:

```bash
cd /Users/trinhannguyen/Documents/Card
git add .
git commit -m "Update card"
git push
```

The live link rebuilds automatically in about a minute. Open it on your own phone to check,
then send it to her. 💕

### ⚠️ Privacy note
Free GitHub Pages serves from a **public** repo, so anyone who has the exact URL could open it
(it won't be indexed or linked from anywhere, but it isn't secret). Don't put anything in the
card you'd mind a stranger seeing. If you ever want it truly private, you can make the repo
private (which turns the Pages link off) and keep it as a local file instead.
