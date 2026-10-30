# Lemmy Scraper – Posts, Comments & Communities (Fediverse)

Search Lemmy posts, comments and communities or export a community's posts from any instance via the public Lemmy API. Fediverse Reddit-alternative data, LLM-ready, pay per result.

**[Run it on Apify →](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)** (pay per result, free Apify account to start)


**Lemmy Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Reddit-alternative social listening
- Community research for marketing
- Datasets for NLP/LLM work
- Monitoring keywords with incremental mode

## Data source

The public Lemmy API (v3) of the instance you choose (e.g. lemmy.world). Public data only; no login.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "instance": "lemmy.world",
  "mode": "search",
  "queries": [
    "linux"
  ],
  "maxItems": 20
}
```

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/lemmy-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper) for current pay-per-result pricing.

## More data actors

- [Bluesky Scraper & API – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [Companies House Scraper – UK Company Data, Directors & Filings](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [Hacker News Scraper – Stories, Comments & Who Is Hiring Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [npm Scraper – Package Downloads, Dependencies & Maintainers](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=lemmy-scraper)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
