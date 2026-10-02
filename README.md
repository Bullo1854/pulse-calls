# Pulse · Calls

Page 2 of Pulse. Who is off pace, by how many dollars and what percent, what to tell the manager, and whether that kind of coaching has held after weather.

Fictitious practice data. Safe to publish.

## Preview on GitHub Pages

This is a static site. No build. The easiest preview link is GitHub Pages.

1. Create a new public repository, for example `pulse-calls`.
2. Unzip this folder and put its contents at the repository root, not inside another folder. You should see `index.html` next to `README.md`.
3. Commit and push to `main`.

```bash
cd pulse
git init
git add .
git commit -m "Pulse page 2: who is off pace"
git branch -M main
git remote add origin git@github.com:YOU/pulse-calls.git
git push -u origin main
```

4. On GitHub: Settings → Pages → Build and deployment → Deploy from a branch → `main` / root → Save.
5. Wait about a minute. The preview link is `https://YOU.github.io/pulse-calls/`.

`.nojekyll` is already in the folder so Pages will not try to process the files.

If you do not want to use git, drag the unzipped folder onto [https://app.netlify.com/drop](https://app.netlify.com/drop). Netlify gives a preview link immediately. That link is the fastest way to send it to someone.

## What is in the folder

| File | What it is |
| --- | --- |
| `index.html` | The call list. Tap a store to log a corrective action. |
| `notes.html` | Definitions: pace, weather, coaching, tie-out. |
| `data.js` | The call list the phone reads. |
| `data/pulse.json` | Same payload, as JSON. |
| `data/weather.json` | Simulated weather by store and day, this year and last year, plus the regional inch costs. |
| `data/actions-log.sample.json` | The shape of a logged action and a review tag. |
| `preview/` | Screenshots of the list, the action sheet, and the definitions page. |

## Weather

Simulated for the climate. Not a forecast feed.

- An inch of snow on the New England coast costs about 6% of a day.
- An inch of snow in Georgia or Alabama costs about 40%.
- An inch of rain on the Florida Gulf costs about 5%. The same inch in New England costs about 10%.

North is the Northeast. Central is the Carolina piedmont and Tennessee. South is the Florida Gulf, Georgia, and Alabama.

## Corrective actions

On a store sheet, enter your name and role (regional manager or executive), pick the action, add a note, and press Log action. It stays on that phone under `localStorage` key `pulse2.z.v1.logs`, including who entered it. Tagging a past flag (`pulse2.z.v1.reviews`) folds that weather-adjusted result into the coaching rate.

The sample log is not observed. It shows the fields: store, region, driver, action, note, time.

## This close

Fairhaven, Tennessee, −58% and −$45.3k after weather. Yarrow Point, Carolina piedmont, −58% and −$43.4k, drier than last year. Northgate, New England coast, −45% and −$25.1k. The miss there is the deals, not the rain.

Week net $1,878,375.72 across 161 rows. Ties to net sales.
