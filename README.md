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
- `memories` — your milestones. Add or remove as many `{ date, title, text, photo }` entries as you like.

## 2. Add photos

Drop your photos into **`assets/photos/`** and name them to match the `photo:` paths in
`CONFIG` (e.g. `1.jpg`, `2.jpg`, …). Landscape-ish photos look best (they're shown 4:3).
Missing photos just hide themselves — nothing breaks.

## 3. Add the song (when you have it)

Put the audio file at **`assets/song.mp3`** (or change `songFile` in `CONFIG` to its path).
A round ♪ button appears once a valid song loads; tap it to play/pause. (Phones block
auto-play, so it's a deliberate tap — that's expected.)

## 4. Preview it

Just double-click `index.html` to open it in your browser. Tap the envelope to test the
whole thing. Use your browser's responsive/phone view to see how it'll look on her screen.

---

## 5. Put it online with GitHub Pages

So you can text her a link:

```bash
cd /Users/trinhannguyen/Documents/Card
git init
git add .
git commit -m "Anniversary card"
```

Then create a repo and push. If you have the GitHub CLI:

```bash
gh repo create my-card --public --source=. --push
```

(or create an empty repo on github.com and follow its "push existing repo" commands).

Finally: on the repo page → **Settings → Pages → Source: `main` / `/ (root)` → Save**.
After ~1 minute your link is live at:

```
https://<your-username>.github.io/<repo-name>/
```

Open that link on your own phone first to check it, then send it to her. 💕

### ⚠️ Privacy note
Free GitHub Pages serves from a **public** repo, so anyone who has the exact URL could open
it (it won't be indexed or linked from anywhere, but it isn't secret). For something this
personal, give the repo a **non-obvious name** (e.g. a random word) and don't include
anything you'd mind a stranger seeing. If you want it truly private, keep it as a local file
and AirDrop it instead — though texted HTML files don't always open cleanly on phones.
