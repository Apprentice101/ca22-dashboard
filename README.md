# CA-22 Voting Procedures Dashboard (v2)

Built from `voting-dashboards-source` repo, district config `client/src/configs/ca-22.ts`.

## v2 changes from initial build
- Review Queue tile now shows "Rules pending review" count (was missing)
- District map now shows California (Kings/Tulare/Kern), not US-wide fallback
- Active tab styling is much more visible (blue background, white text, font weight)
- Updates panel now shows 3 initial-build entries (sources verified, primary called, QA pending)
- Conflicts panel shows 1 initial conflict (ballot curing window — statute vs county guidance)
- Top banner sources changed from "AZ IRC · TIGERweb" to "House.gov district lookup · Census TIGERweb"

## Deploy to GitHub Pages

```bash
# In Apprentice101/ca22-dashboard repo:
git add .
git commit -m "Deploy CA-22 dashboard"
git push -u origin main
```

Enable GitHub Pages from main branch root in repo settings.

## Files
- `index.html` — entry point
- `snapshot.json` — district data (data layer)
- `assets/` — bundled JS/CSS

## QA status (2026-06-11)
- 12 rules: `needsReview: true, confidence: "unconfirmed"` — verify with CA SOS / county elections offices before publish
- 17 events: `confidence: "unconfirmed"` — verify with county elections offices
- 17 sources verified reachable; Votebeat dropped (robots.txt)
- 6 news cards
- 3 updates + 1 conflict (initial-build inventory)
