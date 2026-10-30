QUIT
====

QUick Image Tagger. Flip through a folder of screenshots/pictures and sort each one into `keep/` or `delete/`. Nothing is ever deleted: files are only moved. Empty `delete/` yourself when you're sure.

<p>
  <img src="docs/screenshot-mobile.jpg" alt="QUIT on a phone, mid-swipe to keep" height="420">
  <img src="docs/screenshot-desktop.jpg" alt="QUIT on desktop" height="420">
</p>

<sub>Sample photos in the screenshots are from <a href="https://unsplash.com">Unsplash</a> (Unsplash License).</sub>

## Run

Open `index.html` in **Chrome or Edge** (desktop or Android). One file, no install, no server. Firefox and Safari can't write to local folders, so they get a notice instead.

Pick a folder (top-left). It shows the folder's `.png`, `.jpg`, `.jpeg` and `.gif` files (not subfolders).

| Do | Key | Action |
|----|-----|--------|
| Swipe right / ♥ | `K` | Keep: move into `keep/` |
| Swipe left / ✕ | `D` | Delete: move into `delete/` |
| Tap left half of picture | `F` | Back |
| Tap right half of picture | `J` | Next (skip) |
| ↶ | `Z` | Undo the last keep/delete (as far back as you like) |
| ⤢ | `V` | Open full size in a new tab, to zoom |
| 📁 | `B` | Pick folder |

Keys can be remapped in Settings (top-right); they're saved in the browser.

If `keep/` or `delete/` already holds a file with the same name, the move is refused and nothing is overwritten.

## On a phone

The browser only allows folder access on `https://` or `localhost`, so a plain LAN address (`http://192.168.x.x`) won't work. Host the file somewhere with https (e.g. GitHub Pages) and open it in Chrome for Android.

## Self-test

Serve the folder (`python3 -m http.server`) and open `http://localhost:8000/#selftest`. It runs in the browser's private storage, never on your files, and shows `SELFTEST PASS` or what failed.

## Style

Neo-brutalism, after lesson 04 of [Brutalist Substyles](https://www.brutalistwebdesign.com/pdf/brut111.pdf): flat loud colors, thick black outlines, hard offset shadows, simple interface, minimal motion (and none with `prefers-reduced-motion`).

## History

### Old QUIT

The first version was a Python/Tkinter window with a row of buttons; this repo started as that.

![Old QUIT](docs/old-quit.png)
