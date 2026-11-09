# AI Spend Radar

[Open the live site](https://ai-spend-radar.shahanvik.chatgpt.site/)

AI Spend Radar tracks companies ranked **101–500 in the 2026 Fortune 500**. It excludes the first 100 companies. The interactive bubble chart plots Fortune rank against matching AI news signals. Bubble size represents the number of source-linked stories, **not dollars spent**. A missing story or spending figure is shown as missing evidence, not zero AI spend.

The company list comes from [Fortune's 2026 ranking](https://fortune.com/ranking/fortune500/). The checked ranks and profile links are also in [`fortune-500-ranks-101-500.csv`](fortune-500-ranks-101-500.csv). A dated news snapshot supplies initial stories. The **Scan this company now** action queries Bing News RSS for a selected company. **Refresh news** checks GDELT; external feeds can be unavailable or rate limited. The site drafts outreach emails but does not send them.

This is a dependency-free Cloudflare Worker ESM site hosted with Sites. Source is in `worker/index.js`. Build with `bash scripts/build.sh`; publish the generated `dist/` package through Sites.
