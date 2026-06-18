# Arbeitsagentur Jobs Feed

Extract structured job listings from arbeitsagentur.de — Germany's official federal employment portal with 1M+ active listings. Includes detail enrichment, employer profiles, salary data, geo-coordinates, email/phone extraction, incremental monitoring, and compact output for AI-agent workflows. Scrape by search, or paste specific job URLs.

Available on:
- **Apify:** https://apify.com/blackfalcondata/arbeitsagentur-jobs-feed?fpr=1h3gvi

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
  "extractedEmails": ["bewerbung@kinderkrankenpflege-goetz.de"],
  "extractedPhones": ["+49 89 1234567"]
}
```

## Key features



**Export anywhere** — Download as JSON, CSV, or Excel. Stream via Apify API, webhooks, or integrations with Make, Zapier, Airbyte, Keboola.

**Structured data** — Clean JSON output with consistent field naming. All fields always present — `null` when unavailable, never omitted.

---

## About Black Falcon Data

Black Falcon Data builds production-grade web scrapers for job boards and marketplace data. Browse our full actor catalog at [www.blackfalcondata.com](https://www.blackfalcondata.com).

## Output fields

Every listing returns the same structured schema. Missing values are `null` — never omitted.

- `referenceId`
- `title`
- `employer`
- `occupation`
- `allOccupations`
- `location`
- `postalCode`
- `region`
- `country`
- `lat`
- `lng`
- `isFullTime`
- `isPartTime`
- `isPartTimeMorning`
- `isPartTimeAfternoon`
- `isPartTimeEvening`
- `isNightOrWeekendShift`
- `isMiniJob`
- `isRemote`
- `remoteType`
- `contractType`
- `contractDurationMonths`
- `salary`
- `startDate`
- `publishedDate`
- `firstPublishedDate`
- `modifiedDate`
- `isCareerChange`
- `isTemporaryStaffing`
- `isDisabilityFriendly`
- `cipherNumber`
- `externalUrl`
- `portalUrl`
- `distanceKm`
- `description`
- `allianzPartnerName`
- `allianzPartnerUrl`
- `employerDescription`
- `employerWebsite`
- `employerSize`
- `employerFoundedYear`
- `employerHQ`
- `employerBenefits`
- `employerSocialMedia`
- `employerContactInfo`
- `extractedEmails`
- `extractedPhones`
- `extractedUrls`
- `socialProfiles`
- `scrapedAt`

## Sample output

One object per listing. Here is a real example from a production run:

```json
{
  "referenceId": "11949-17168778-S",
  "title": "Softwareentwickler/in",
  "employer": "Magenta Telekom",
  "occupation": "Softwareentwickler/in",
  "allOccupations": [
    "Softwareentwickler/in"
  ],
  "location": "Wien,Landstraße",
  "postalCode": "1030",
  "region": "WIEN",
  "country": "OESTERREICH",
  "lat": null,
  "lng": null,
  "isFullTime": true
}
```

*Truncated — full records contain 52 fields. See Output fields for the complete schema.*

**[Try Arbeitsagentur Scraper - German Jobs now — $5 free credit, no credit card →](https://apify.com/blackfalcondata/arbeitsagentur-jobs-feed?fpr=1h3gvi)**

## Pricing

Pay only for what you extract. No subscription required — Apify's free $5 credit covers thousands of results.

| Event | Price (USD) |
| --- | --- |
| Actor Start | $0.01 |
| Result | $0.002 |

See the [actor on Apify](https://apify.com/blackfalcondata/arbeitsagentur-jobs-feed?fpr=1h3gvi) for current pricing.

## Getting started with Apify

New to Apify? [Create a free account with $5 credit](https://console.apify.com/sign-up?fpr=1h3gvi) — no credit card required.

1. [Sign up free](https://console.apify.com/sign-up?fpr=1h3gvi) — $5 credit included
2. Open the actor and paste your input
3. Click Start — results download as JSON, CSV, or Excel

Need more volume? [See pricing](https://apify.com/pricing?fpr=1h3gvi).

---
