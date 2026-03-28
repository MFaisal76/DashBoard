# USDT/EGP Dashboard V2 (Netlify backend)

This version keeps the dashboard UI as a single `index.html` file and adds a Netlify Function backend at:

`/.netlify/functions/prices`

## What changed
- Live prices now go through the backend function instead of calling exchange APIs directly from the browser.
- Better for phone access from anywhere.
- Same UI flow, alerts, amount slider, payment-method filter, and fallback watchlist links.

## Files
- `index.html` — frontend
- `netlify/functions/prices.js` — backend proxy/function
- `netlify.toml` — tells Netlify where the functions directory is
- `package.json` — optional local dev support

## Deploy on Netlify
### Recommended
1. Put these files in a GitHub repository.
2. In Netlify, choose **Import an existing project**.
3. Pick the GitHub repo.
4. Deploy.
5. Open your site URL and test `/.netlify/functions/prices`.

### Or use Netlify CLI
1. Install Node.js and Netlify CLI.
2. In this folder run:
   - `npm install`
   - `netlify login`
   - `netlify init`
   - `netlify deploy --prod`

## Local test
- `npm install`
- `npx netlify dev`

Then open the local URL shown by Netlify Dev.
