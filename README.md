# Birthday card for Mahi 🎂

An interactive scrapbook birthday card: cover → envelope & letter → cake you blow out with your mic → a wish note. Plain HTML/CSS/JS, no build step.

## Run it
Blowing into the mic only works over **https** (or `http://localhost`). Opening `index.html` by double-click will not allow the mic, but the **hold to blow** button and **spacebar** still work.

Local test:
```
python3 -m http.server 8000
# open http://localhost:8000
```

## Put it online (GitHub Pages, free https)
1. Create a new repo and upload everything in this folder (keep the `assets/` folder).
2. Repo **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder `/ (root)`.
3. After a minute your card is live at `https://<your-username>.github.io/<repo-name>/`. Share that link.

## Files
- `index.html` – page structure
- `style.css` – look and layout
- `script.js` – page flips, letter, flames, mic/blow detection, confetti, music
- `assets/` – your images (`cover`, `envelope`, `letter`, `cake`, `wish-note`), the three cut-out flames (`flame1–3.png`) and the song (`song.mp3`, trimmed to 60 s with fades)

## Easy edits
- Name in the wish note: `index.html` (`make a wish, Mahi`) and the page `<title>`.
- Song volume: `script.js` → `song.volume=.7`. To swap the song, replace `assets/song.mp3` (keep the name).
- Blow sensitivity: `script.js` → in `tick()`, the `.25` blow threshold and `.22` range.

## Heads-up
A public repo lets anyone with the link download `song.mp3` and your images. Use a private repo to keep them private (Pages on private repos needs a paid plan), or use music you have the rights to share.
