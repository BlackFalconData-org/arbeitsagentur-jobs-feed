# Arbeitsagentur Jobs Feed

Extract structured job listings from arbeitsagentur.de — Germany's official federal employment portal with 1M+ active listings. Includes detail enrichment, employer profiles, contact data, incremental monitoring, and compact output for AI-agent workflows.

Available on:
- **Apify:** https://apify.com/blackfalcondata/arbeitsagentur-scraper

## Example request

Run the actor via the Apify API:

POST https://api.apify.com/v2/acts/blackfalcondata~arbeitsagentur-jobs-feed/runs

Example input:
```json
{
  "query": "Software Developer",
  "location": "Berlin",
  "maxResults": 50,
  "includeDetails": true
}
```

## Example response
```json
{
  "referenceId": "10001-1002790098-S",
  "title": "Krankenschwester/-pfleger",
  "employer": "Häusliche Kinderkrankenpflege Manuela Götz GmbH",
  "occupation": "Gesundheits- und Krankenpfleger/in",
  "location": "München",
  "postalCode": "80636",
  "region": "BAYERN",
  "lat": 48.1519402,
  "lng": 11.5392859,
  "isFullTime": true,
  "contractType": "UNBEFRISTET",
  "publishedDate": "2026-03-19",
  "portalUrl": "https://www.arbeitsagentur.de/jobsuche/suche?id=10001-1002790098-S",
  "description": "Wir suchen zum nächstmöglichen Zeitpunkt examinierte Gesundheits- und Krankenpfleger/in...",
  "contactName": "Manuela Götz",
  "contactEmail": "bewerbung@kinderkrankenpflege-goetz.de"
}
```

## Key features

- Structured core listings with geo-coordinates, postal code, and federal state
- Full job description and employer profile enrichment
- Contact enrichment: name, email, phone, application URL
- Incremental mode for scheduled monitoring (new/changed jobs only)
- Smart employer resolution (e.g. "BMW" → "BMW AG" → 666 results)
- Compact output mode for AI-agent and MCP workflows
- Description truncation for token budget control
- Bundesland filtering across all 16 German federal states

## Filters

- Query (keyword or job title)
- Location (city or region)
- Federal state (Bundesland)
- Contract type (permanent / fixed-term)
- Work type (full-time / part-time / home office / mini job / shift)
- Job type (employment / apprenticeship / internship / self-employment)
- Remote only
- Published within N days
- Employer name
- Search radius (km)

## Pricing

- $0.01 per run start
- $0.002 per job listing

## Use cases

- Recruitment and staffing
- Sales intelligence
- Labour market research
- Job aggregation platforms
- Employer profiling
- Geographic analysis
- Change monitoring pipelines

## Documentation

Full documentation, input/output reference, and sample output:
https://apify.com/blackfalcondata/arbeitsagentur-scraper

## Related

- [StepStone Jobs API](https://github.com/BlackFalconData-org/stepstone-jobs-api) — search and extract job listings from 18 StepStone Group portals
- [Indeed Jobs Feed](https://github.com/BlackFalconData-org/indeed-jobs-feed) — extract job listings from Indeed
- [Glassdoor Jobs Feed](https://github.com/BlackFalconData-org/glassdoor-jobs-feed) — extract job listings from Glassdoor
- [Company Jobs Tracker](https://github.com/BlackFalconData-org/company-jobs-tracker-api) — track new and removed job listings per company
