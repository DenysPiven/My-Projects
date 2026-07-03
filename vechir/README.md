# Vechir

Mobile-first date planner questionnaire. **Questionnaire UI is in Ukrainian**; code, docs, and comments are in English.

Static site — runs on GitHub Pages with no build step.

## Features

- Basic info: name, Instagram, Telegram, city
- Tinder-style swipe cards: food, activities, vibe
- Date & time picker
- Meeting place on map (Leaflet + OpenStreetMap)
- Generated date plan message — copy or open Telegram

## Cities

Kyiv, Lviv, Odesa — with curated meeting spots. Places are ranked by swipe answers.

## Live demo

After enabling GitHub Pages:

```
https://YOUR_USERNAME.github.io/vechir/
```

## Local dev

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Project structure

```
vechir/
├── index.html
├── css/style.css
├── js/
│   ├── i18n.js   # Ukrainian UI strings (questionnaire)
│   ├── data.js   # Swipe cards & places (Ukrainian)
│   └── app.js    # App logic (English comments)
└── README.md
```

## GitHub Pages setup

1. Create a **new public repo** (e.g. `vechir`)
2. Push this folder contents to the repo root
3. **Settings → Pages → Source: GitHub Actions**
4. The included workflow deploys on push to `main`

### Push to a new repo

```bash
cd vechir
git init
git add .
git commit -m "Initial commit: Vechir date planner"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/vechir.git
git push -u origin main
```

## Stack

- Vanilla HTML / CSS / JavaScript
- [Leaflet](https://leafletjs.com/) + OpenStreetMap
- 100% client-side

## License

MIT
