# weathercrab

A tiny weather app: a little crab checks the forecast and puts on the right layers for the day. Puffer and beanie when it's freezing, a coat and scarf when it's cold, a raincoat and umbrella when it rains, sunglasses and a sun hat when it's hot.

Idea from [@pauline_makes](https://x.com/pauline_makes/status/2042608561197297942)' weather bunny.

- Live 8-day forecasts (yesterday + the next 7 days) from [Open-Meteo](https://open-meteo.com). No API key needed.
- Search any city, or use your location. The header then shows the town you're in underneath, like "my location (delray beach)". Town names come from [BigDataCloud](https://www.bigdatacloud.com)'s free reverse-geocoding API.
- 220 places are saved in the page (every US state capital, the biggest US cities, more cities in California, Florida, New York and Texas, and a few world cities including Niamey, Niger). They load instantly and serve as a fallback forecast if the weather service can't be reached.
- An hourly strip under the high and low. Tap any hour and the crab dresses for that hour (today starts on "now"; at night it skips the sunglasses and the glow dims).
- The crab moves with the weather: it shivers in the cold, scuttles when it's mild, hops in the sun, melts in the heat and leans into the wind.
- At 100°F and up it changes into a swimsuit and sunglasses.
- When it's raining, drizzling, snowing or storming, it says how long for, like "thunderstorm for the next 23 minutes" (15-minute forecast data for the next few hours, hourly after that).
- °F / °C switch, swipe or arrow keys between days, and a widget preview.

It is one static `index.html` with no build step and no dependencies.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole app |
| `favicon.svg` | Browser tab icon |
| `apple-touch-icon.png` | Icon when added to an iPhone home screen |
| `icon-192.png`, `icon-512.png` | Icons for Android and installed web apps |
| `site.webmanifest` | Lets the site be added to a home screen as an app |

## Deploy

1. **GitHub:** create a new repository (for example `weathercrab`) at <https://github.com/new>. On the empty repo page, click **uploading an existing file**, drag in every file from this folder, and commit.
2. **Vercel:** go to <https://vercel.com/new>, import the repository, leave **Framework Preset** on **Other** with no build command, and click **Deploy**.

Every commit to the main branch redeploys automatically.

### Or with git from a terminal

```bash
git init
git add .
git commit -m "weathercrab"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/weathercrab.git
git push -u origin main
```

## Data and license notes

Weather data by [Open-Meteo.com](https://open-meteo.com), licensed CC BY 4.0. The page shows the credit at the bottom. Open-Meteo's free API is for non-commercial use (up to 10,000 calls a day). A commercial site needs one of their paid plans.
