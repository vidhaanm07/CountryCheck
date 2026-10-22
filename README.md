# 🌍 Guess the Country — Atlas Arcade

A fast-paced, interactive geography game. Find a country or locate a city on the world map before the 10-second timer runs out.

## Features

- **Country Mode:** identify a country by clicking its shape on the world map.
- **City Mode:** locate the named city by clicking near its position on the map. Zoom in for precision.
- **Endless Mode:** keep playing and build your streak.
- **10-second countdown:** live numeric timer and circular countdown indicator.
- **Scoring:** 100 points for a correct answer plus a speed bonus of up to 50 points.
- **Streak tracking:** current and best streak, round progress, score, accuracy, and end-of-run summary.
- **Map controls:** zoom in, zoom out, reset zoom, and drag/pan around the map.
- **Responsive UI:** designed for desktop and mobile screens.
- **No backend or account required:** game logic runs in the browser.

## Play locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser such as Chrome or Edge.
3. Keep an internet connection available so the map data and JavaScript libraries can load.
4. Select a mode and press **Let's play**.

If your browser blocks network requests when opening a local file, run a tiny local web server from the project directory instead:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.

## Deploy with GitHub Pages

1. Push these files to a GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder, then save.
5. Wait for GitHub Pages to publish the site. The URL will appear in the Pages settings.

The included workflow at `.github/workflows/pages.yml` can alternatively deploy the site with GitHub Actions. If using the workflow, open **Settings → Pages** and set the source to **GitHub Actions**.

## Tech stack

- HTML5 and CSS3
- Vanilla JavaScript
- [D3.js](https://d3js.org/) for map projection, interaction, and zooming
- [TopoJSON Client](https://github.com/topojson/topojson-client) for converting world topology to GeoJSON
- [World Atlas](https://github.com/topojson/world-atlas) country boundary data, with a GeoJSON fallback

Libraries and map data are loaded from public CDNs at runtime, so this project does not need a build step or npm install.

## Project structure

```text
guess-the-country/
├── index.html
├── README.md
├── LICENSE
├── .gitignore
└── .github/
    └── workflows/
        └── pages.yml
```

## Notes

- The game requires internet access to load external libraries and geographic boundary data.
- City mode includes a curated set of major world cities. It checks whether the click is near the city's projected map location; zooming makes precise selection easier.
- Country/city boundary and name sources can vary. The game normalizes common country-name variants to improve matching.

## License

Released under the MIT License. See [`LICENSE`](LICENSE).

---

Made for curious minds. One planet, many places.
