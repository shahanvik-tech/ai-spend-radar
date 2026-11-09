# AI Spend Radar

[Open the GitHub Pages site](https://shahanvik-tech.github.io/ai-spend-radar/)

The GitHub Pages edition shows the dated snapshot with the chart, searchable company list, source links, and email drafts. GitHub Pages is static, so it does not run the live news scan. The [server-backed edition](https://ai-spend-radar.shahanvik.chatgpt.site/) retains that feature.

AI Spend Radar covers companies ranked **101–500 in the 2026 Fortune 500** and excludes the first 100. The list and source profile links are in [`fortune-500-ranks-101-500.csv`](fortune-500-ranks-101-500.csv), based on [Fortune's 2026 ranking](https://fortune.com/ranking/fortune500/).

The dated November 9, 2026 snapshot uses a broad company-name-plus-AI news query over roughly 180 days. After title filtering, 192 of 400 companies have at least one AI news mention in the snapshot; 24 have a headline with spending language among the first three retained stories. **These are discovery signals, not verified AI spending amounts.** The chart uses story counts for bubble size and vertical position. The site separately shows the count of sourced spending figures, currently zero for this cohort.

**Scan 400 companies** refreshes the browser view in 20 batches. **Scan this company now** checks one company. Both depend on external news feed availability. The site preserves its dated snapshot if a live query returns no result or fails. It drafts outreach emails but does not send them.

This is a dependency-free Cloudflare Worker ESM site hosted with Sites. Source is in `worker/index.js`. Build with `bash scripts/build.sh`; publish the generated `dist/` package through Sites.
