# App Builder

A collection of small web apps and games, each in its own folder, hosted free on
GitHub Pages. The homepage (`index.html`) is a menu linking to every app.

## 🔗 Live links

**Homepage (start here):** https://tayschub.github.io/app-builder/

| App | Live link |
| --- | --- |
| Settle It | https://tayschub.github.io/app-builder/settle-it/ |
| Echo | https://tayschub.github.io/app-builder/echo-memory/ |
| Make Ten | https://tayschub.github.io/app-builder/make-ten/ |
| Reflex Ring | https://tayschub.github.io/app-builder/reflex-ring/ |
| Tower Stack | https://tayschub.github.io/app-builder/tower-stack/ |
| Jumbl — Word Sprint | https://tayschub.github.io/app-builder/word-sprint/ |
| Tangle | https://tayschub.github.io/app-builder/tangle/ |
| Loop | https://tayschub.github.io/app-builder/loop/ |
| Driftbound | https://tayschub.github.io/app-builder/driftbound/ |
| Prism | https://tayschub.github.io/app-builder/prism/ |
| Bloom | https://tayschub.github.io/app-builder/bloom/ |

> Tip: open the homepage on your phone, then **Add to Home Screen** so it acts like an app.

## 📁 How it's organized

```
app-builder/
├─ index.html          ← homepage menu (links to all apps)
├─ README.md           ← this file
├─ settle-it/index.html
├─ echo-memory/index.html
├─ make-ten/index.html
├─ reflex-ring/index.html
├─ tower-stack/index.html
└─ word-sprint/index.html
```

Each app is just a folder containing an `index.html`. Its live link is the folder
name added to the homepage URL.

## ➕ Adding a new app

1. Create a folder inside `app-builder/` with a short, lowercase, hyphenated name
   (e.g. `color-match`) and put an `index.html` inside it.
2. Add a tile for it on the homepage (`index.html`) so it shows up in the menu.
3. Commit and push:
   ```
   git add -A
   git commit -m "Add color-match app"
   git push
   ```
4. Wait ~1–2 minutes for GitHub Pages to rebuild, then it's live at
   `https://tayschub.github.io/app-builder/color-match/`.

## ✏️ Updating an existing app

Edit the file(s), then run the same three commands (`add`, `commit`, `push`).
The live link stays the same and updates within a minute or two.

## ℹ️ Notes

- This repo is **public**, so the code and the live apps are visible to anyone.
- Hosting is **GitHub Pages** (Settings → Pages → deploy from `main` branch).
