# TALLY

A daily arithmetic puzzle game. Everyone gets the same 4 numbers and target each day; combine tiles with +, −, ×, ÷ until one tile is left. Streaks and a shareable result grid are built in — these are the retention mechanics (daily habit loop + streak loss aversion + social sharing), the same pattern that makes daily puzzle games sticky.

It's a single file: `index.html`. No build step, no backend, no dependencies beyond two Google Fonts.

## Deploy it (free options)

- **GitHub Pages**: create a repo, upload `index.html`, enable Pages in repo settings. Live in ~2 minutes.
- **Netlify / Vercel**: drag-and-drop the folder onto their dashboard.
- **Cloudflare Pages**: same drag-and-drop flow.

Any of these gives you a real URL, which you need before Google will approve AdSense.

## Turning on ads

1. Apply at https://www.google.com/adsense/ once the site's been live for a bit with the URL you're using. New/empty sites often get rejected — it helps to let people actually play it first.
2. Once approved, you'll get a publisher ID (`ca-pub-XXXXXXXXXXXXXXXX`) and ad unit snippets.
3. Open `index.html`:
   - Paste your loader `<script>` tag in `<head>` where it says `GOOGLE ADSENSE — SETUP INSTRUCTIONS`.
   - Replace the two `<div class="ad-slot">` placeholders (search for `AD SLOT`) with your `<ins class="adsbygoogle">` snippets.
4. Don't add more ad slots than that at first. The two placements (top banner, and the slot that appears after someone finishes the day's puzzle) were chosen so ads don't interrupt actual play — that matters more for revenue than ad count, because daily return visits are what compound.

## What drives the retention (and therefore the revenue)

- **One puzzle a day, shared by everyone** — creates a reason to come back at a predictable time, and lets people compare/share results.
- **Streak counter** — loss aversion; missing a day resets it.
- **Can't replay after solving** — prevents burning through content, which is what keeps daily games alive for years instead of weeks.
- **Share button** — free distribution, no ad spend needed.

If you want to grow it past organic traffic, the honest next steps are: post daily results/puzzles somewhere with an existing audience (Reddit puzzle communities, a small Twitter/X account), and just be consistent — daily games live or die on whether the daily puzzle actually goes out every day.

## Notes

- All state is stored in the visitor's browser (`localStorage`) — no backend, no user accounts, no data collection beyond whatever AdSense itself does.
- Fully responsive, keyboard-accessible, and respects `prefers-reduced-motion`.
