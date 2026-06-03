# ZIP Code Finder

A static single-page web app that looks up U.S. ZIP codes by city and state.

## Usage

Open `index.html` in any browser, or serve the directory with any static web server (Nginx, `python3 -m http.server`, GitHub Pages, etc.). No build step, no backend.

1. Type a city name
2. Pick a state from the dropdown
3. Hit **Find ZIP Codes** — click any result to copy it

## How it works

The page calls the public [Zippopotam.us](https://www.zippopotam.us/) API directly from the browser:

```
GET https://api.zippopotam.us/us/{state}/{city}
```

The API is free, requires no key, and sends `Access-Control-Allow-Origin: *`, so no backend proxy is required.

## Files

- `index.html` — the entire app (HTML + CSS + JS in one file)
