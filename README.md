The Second Opinion - TAKE ANOTHER LOOK

## Ticker overlay

This repo hosts a self-contained HTML broadcast lower-third ticker overlay for **The Second Opinion**. Load it in **OBS** as a **Browser Source** to show a scrolling news crawl with themed callouts, RSS headlines, and on-screen controls.

The site is a single static file (`index.html`) — no build step, bundler, or dependencies.

## GitHub Pages / OBS setup

1. Enable GitHub Pages on this repo (see below).
2. In OBS, add a **Browser Source**.
3. Set the URL to your GitHub Pages URL (see below).
4. Set width **1920** and height **1080**.
5. Uncheck **Shutdown source when not visible**.
6. Uncheck **Refresh browser when scene becomes active**.

## Keyboard controls

| Key | Action |
|-----|--------|
| **Space** | Pause / resume the crawl |
| **← →** | Decrease / increase scroll speed |
| **H** | Hide or show the ticker strip |
| **B** | Toggle solid background (useful for preview) |
| **R** | Refresh feeds now |
| **D** | Toggle feed diagnostics panel |
| **?** | Show controls help card |

## Editing content and feeds

Open `index.html` in a text editor. Near the top of the `<script>` block (marked **EDIT BELOW**), you can change:

- **`CALLOUTS`** — rotating phrases shown in the upper crawl lane.
- **`FEEDS`** — RSS sources (name, tier, URL). Add, remove, or fix URLs here.
- **`TIERS`** — turn entire feed categories on or off (`national`, `legal`, `factcheck`, `business`, `foreign`) without editing individual feeds.
- **`FILTER`** — headline limits: `maxAgeHours`, `perOutlet`, `maxItems`, `minChars`.

Related knobs in the same section include `BLOCK`, `BLOCK_WORDS`, `PRIORITY`, and `CONFIG` (speed, refresh interval, etc.).

## Logo

Drop a file named **`logo.png`** in the repo root (transparent PNG, roughly **200px tall**). The overlay loads it automatically and replaces the fallback blackletter wordmark in the masthead.
