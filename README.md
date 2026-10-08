# EliteAEO AEO Agency Dataset 2026

The dataset behind [EliteAEO](https://eliteaeo.ai/about)'s rankings of AEO, GEO and AI SEO providers: one row for each of the 398 agencies and consultants EliteAEO has profiled, with the evidence checks, scores and ranks it publishes, plus every answer collected for the AI Visibility Index, September 2026.

EliteAEO is an independent ranking and research publisher covering AEO, GEO and AI SEO agencies and consultants. Founded in 2026 and based in West Palm Beach, Florida, EliteAEO publishes evidence-checked provider rankings, its methodology, market data and AI visibility research. It does not sell AEO or SEO services.

EliteAEO's editor and head of research is [David Quaid](https://eliteaeo.ai/about#david-quaid) and its publisher is [Bike Hawley](https://eliteaeo.ai/about#bike-hawley).

**Snapshot 2026-10-07.788349** · data as of October 7, 2026 · methodology 2.0 · license [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) · DOI [10.5281/zenodo.23249511](https://doi.org/10.5281/zenodo.23249511)

The files in `data/` are byte-for-byte copies of the files published on eliteaeo.ai. The `dataset_snapshot` column matches the snapshot printed in the footer of every eliteaeo.ai page built from the same data, so any copy can be traced back to the version of the site it came from.

## Files

| File | Rows | What it is |
|---|---|---|
| `data/aeo-agency-market-2026.csv` | 398 | One row per profiled provider ([download on eliteaeo.ai](https://eliteaeo.ai/data/aeo-agency-market-2026.csv)) |
| `data/ai-visibility-index-2026-09-answers.csv` | 358 | One row per AI answer in the [AI Visibility Index, September 2026](https://eliteaeo.ai/research/ai-visibility-index-september-2026) |
| `data/ai-visibility-index-2026-09.json` | | Summary tables of the same index |

## Key figures for this snapshot

| Figure | Value | Base |
|---|---|---|
| Providers profiled | 398 | every row (12 consultants, the rest agencies) |
| Eligible for rankings | 355 | 398 providers |
| Verified by evidence | 342 | 398 providers |
| Publish proof of AI search results for a client | 106 | 355 eligible providers |
| Say they report AI visibility to clients | 199 | 355 eligible providers |
| Median published monthly starting price | $1,500 | 88 monthly prices from eligible providers |

These are the same figures the [State of the AEO Agency Market 2026](https://eliteaeo.ai/research/state-of-the-aeo-agency-market-2026) report shows for this snapshot. Head offices are in 9 countries; most providers serve US businesses.

## How the data is collected

EliteAEO opens each provider's own pages (service pages, case studies, results pages and pricing) and an independent third-party profile, records what it finds with the page address, and dates every check. Proof of AI search results counts only for clients: EliteAEO records the single strongest item and the page it is on, and a provider's own AI visibility does not count. Every ranked provider's evidence is rechecked at least every 90 days. Providers can claim their profile to correct any fact or send newer evidence, which counts once EliteAEO has opened it.

Scores follow [methodology 2.0](https://eliteaeo.ai/methodology). Seven factors add up to 100 points: AI SEO specialization 25, vertical evidence 20, demonstrated outcomes 25, AI measurement capability 10, third-party reputation 10, relevant market coverage 5 and transparency 5. Providers with the same score share a rank, shown with a T. Payment plays no part in eligibility, scores or ranks; paid placements on eliteaeo.ai are labeled and never change the editorial order.

## Columns: `aeo-agency-market-2026.csv`

| Column | Type | Meaning |
|---|---|---|
| `provider` | string | Provider name as EliteAEO shows it. |
| `eliteaeo_profile_url` | string | The provider's profile on eliteaeo.ai. |
| `website` | string | The provider's own website. |
| `provider_type` | string | agency or consultant. |
| `hq_city` | string | City of the head office, where known. |
| `hq_state` | string | State or region code of the head office, where known. |
| `hq_country` | string | ISO 3166-1 two-letter country code of the head office (US, GB, CA, IN and so on). Blank when not established. |
| `eligible` | string | yes when the provider is eligible for EliteAEO rankings: a live, legitimate company that offers answer engine or AI search services, serves at least one industry EliteAEO ranks, and whose evidence passed our checks. Eligibility is decided before scoring and never considers payment. |
| `verified` | string | yes when a dated verification review confirmed that the website is live and belongs to a real company, that at least one independent third-party profile exists, and that at least one piece of evidence ties the provider to a ranked industry. Verified is not a scoring factor. |
| `verified_date` | date | Date of the verification review (YYYY-MM-DD). |
| `evidence_last_checked` | date | Latest date any of the provider's evidence was opened, in the verification review or the AI outcome check. Shown, never scored. |
| `verticals_ranked` | string | Industries the provider is eligible to be ranked in, separated by "; ". Values: dental, legal, healthcare, saas, home-services, local. |
| `evidence_by_vertical` | string | Strongest evidence per industry, as "industry: type" pairs. Types: case_study, only_agency (works only with that industry), named_client, service_page, blog_post, none. |
| `aeo_offering` | string | What the provider sells: full_service, advisory, content, tools or unclear. |
| `reports_ai_visibility` | string | Whether the provider says it reports AI visibility to clients: yes, no or not stated. |
| `ai_results_proof` | string | Strongest proof of AI search results for a client, from strongest to weakest: AI outcome case study; Tracked AI visibility gains; AI result shown for a named client; AI results claimed, no example; No AI results shown. Blank when not eligible. A provider's own AI visibility does not count. |
| `ai_results_url` | string | Page that holds that proof. Blank when there is none or the provider is not eligible. |
| `published_search_results` | string | yes when the provider publishes a case study with measured search results (traffic, rankings or leads) in any industry. Blank when not eligible. |
| `third_party_profile_url` | string | An independent third-party profile of the provider (for example Clutch or DesignRush). |
| `years_active` | integer | Years in business, from the provider's own pages or its third-party profile. |
| `team_size` | string | Team size as published. |
| `starting_price_usd` | number | Published starting price in US dollars. Blank when the provider does not publish one. |
| `price_basis` | string | How that price is billed: monthly, project (minimum project size), one_time, program (multi-month) or unspecified. Only monthly prices enter the monthly medians. |
| `national_scores` | string | EliteAEO Score (0 to 100) on each national industry ranking, as "industry: score" pairs. |
| `national_ranks` | string | Rank on each national industry ranking, as "industry: rank" pairs. T marks a shared rank (tied score). |
| `methodology_version` | string | Version of the scoring methodology behind the scores and ranks. |
| `dataset_snapshot` | string | Snapshot ID: the data date plus a six-character fingerprint of every published fact, score and rank. It matches the snapshot in the footer of every eliteaeo.ai page built from the same data. |

## Columns: `ai-visibility-index-2026-09-answers.csv`

Thirty fixed buyer queries, asked three times each on ChatGPT, Gemini, Perplexity and Google AI Overviews and collected on September 28, 2026. The [index page](https://eliteaeo.ai/research/ai-visibility-index-september-2026) explains the method and shows the base behind every share.

| Column | Type | Meaning |
|---|---|---|
| `engine` | string | ChatGPT, Gemini, Perplexity or Google AI Overviews. |
| `query` | string | The buyer query asked, one of 30 fixed queries. |
| `vertical` | string | Industry the query is about. |
| `query_type` | string | hub (national), city or directory. |
| `run` | integer | Run number, 1 to 3. Each query was asked three times on each engine. |
| `collected` | date | Date the answer was collected. |
| `providers_named` | string | Providers in the EliteAEO dataset that the answer names, separated by "; ". |
| `cited_domains` | string | Domains the answer cites as sources, separated by "; ". |
| `eliteaeo_named` | string | yes when the answer names EliteAEO. |
| `eliteaeo_cited` | string | yes when the answer cites an eliteaeo.ai page. |

## License and credit

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Reuse, share and adapt the data, including commercially, with credit to EliteAEO and a link to the source, for example:

> EliteAEO, AEO Agency Dataset 2026, snapshot 2026-10-07.788349, https://doi.org/10.5281/zenodo.23249511

The DOI (10.5281/zenodo.23249511, archived on Zenodo) always resolves to the newest snapshot; each snapshot also has its own version DOI on Zenodo.

## Corrections and questions

Providers can correct or claim their listing at [eliteaeo.ai/claim](https://eliteaeo.ai/claim). For data questions, email [hello@eliteaeo.ai](mailto:hello@eliteaeo.ai). Corrections are made on eliteaeo.ai first and reach this copy with the next snapshot.

## More from EliteAEO

- [About EliteAEO](https://eliteaeo.ai/about)
- [Methodology](https://eliteaeo.ai/methodology)
- [State of the AEO Agency Market 2026](https://eliteaeo.ai/research/state-of-the-aeo-agency-market-2026)
- [AI Visibility Index, September 2026](https://eliteaeo.ai/research/ai-visibility-index-september-2026)

## Cite

GitHub shows a "Cite this repository" box built from `CITATION.cff`. Column types for tools that read them are in `datapackage.json`. Changes between snapshots are in `CHANGELOG.md`.
