# LiveOps Cadences

A two-page static site documenting the team's cadence-oriented operating flow:
for every cadence, the intended outcome, the owner, the actions, the timing, and
the issue that change is expected to fix.

## Pages

| Path | Source | Contents |
| --- | --- | --- |
| `/` | `plans/visuals/team-scrum-flow-review.html` | Cadence timeline and per-cadence detail |
| `/team-scrum-flow-issues.html` | `plans/visuals/team-scrum-flow-issues.html` | Open issues and follow-ups |

Both pages are self-contained HTML with inline CSS and JavaScript. The only
external dependency is Google Fonts.

## Local preview

Serve the pages directory over HTTP so the relative links between the two pages
resolve:

```bash
python3 -m http.server 8000 --directory plans/visuals
```

Then open <http://localhost:8000/team-scrum-flow-review.html>.

## Deployment

Hosted on Vercel as a static site with no build step. The project's root
directory is `plans/visuals`, so its `vercel.json` lives there too and rewrites
`/` to the review page, keeping the relative link between the two pages working
unchanged.
