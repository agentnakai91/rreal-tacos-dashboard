# Mystery Shopper Email Monitor - Instructions for Agent

## What to do on every heartbeat/check:

1. Open Gmail (agentnakai91@gmail.com) in Chrome on Mac mini
2. Search for: "Shop Results" OR "A Closer Look"
3. For each NEW email not already in mystery_shopper_history.json:
   a. Open the email
   b. Extract: Location, Score, Date, Time, Category breakdowns
   c. If PDF attached: download to /Users/nakai/dashboard/pdfs/
   d. Add entry to mystery_shopper_history.json
   e. Update the dashboard HTML (Mystery Shopper tab)
   f. Recalculate averages

## How to identify NEW emails:
- Compare email dates against last_updated in history JSON
- Compare location+date combos against existing shops array

## Dashboard file: /Users/nakai/dashboard/index.html
## History DB: /Users/nakai/dashboard/data/mystery_shopper_history.json
## PDF folder: /Users/nakai/dashboard/pdfs/
## Dashboard URL: Current Cloudflare tunnel (check /tmp/dash_final.log for URL)

## Score categories (standard A Closer Look format):
- Arrival & Host Stand
- Server/Bartender Greeting & Performance
- Service Flow & Timing
- Food & Beverage Quality
- Cleanliness & Environment
- Manager Performance
- Checkout & Farewell
- Overall Experience & Emotional Impact
- Post-visit Call
- Net Promoter Score
- TOTAL SCORE

## When updating dashboard:
- Add new rows to the scores table (sorted by score descending)
- Update average score cards
- Add trend arrows (up/down vs previous shop for same location)
- If location has multiple shops, show history
