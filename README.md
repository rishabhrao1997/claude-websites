# Find clients by building their website first

Thanks for commenting **coffee**! This is the exact setup from the reel: one prompt in Claude Code finds local businesses with no website, then five agents build a one-page site for each, in parallel.

## What you need
- **Claude Code** (https://claude.com/claude-code): install it, then run `claude` in an empty folder.
- About 15 minutes for the run.

## The prompt
Open `prompt.txt`, replace `[AREA]` and `[CITY]` with your neighbourhood, and paste it into Claude Code. It:
1. finds 5 real local businesses near you that have no website (OpenStreetMap + web search, chains skipped);
2. launches 5 agents at the same time, one per business, each building a clean one-page site (menu or services, hours, address, contact) in `./sites/<business>/index.html`;
3. writes `leads.csv`: name, category, area, phone, site path.

Open each `index.html` in your browser to see the sites.

## Then pitch
- Walk in and show the owner the site on your phone. "I built this for you. Want it live?"
- Agree a price before you publish anything. Hosting a one-page site is free or nearly free (Netlify, Vercel, GitHub Pages).

## Ground rules
- The agents only use publicly listed information and never contact anyone. Check every detail with the owner before the site goes live.
- Don't publish a business's site without their OK.
