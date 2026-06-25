[Google Search Results Serp Scraper](https://apify.com/scraperlink/google-search-results-serp-scraper?fpr=data)

# Google Search Results (SERP) Scraper

## Introduction

Our **Google Search Results (SERP) Scraper** is a **cost-effective, high-speed** Apify Actor designed to retrieve **real-time** Google Search results. With an **affordable pricing model of $1 per 1,000 searches (up to 100 results per search)**, it outperforms competitors by being **cheaper and faster**.

Compared to other actors, this scraper offers:

- **The lowest cost per search** among all tested solutions.
- **Faster execution times** (2 seconds per search).
- **Per-search pricing**, ensuring **cost efficiency** for all users.

---

## Why Choose This Actor?

| Feature | This Actor | Other Actors |
| --- | --- | --- |
| **Cost per 1M searches** | **$500** | $2,907 - $1,000,000 |
| **Billing Model** | **$0.50 per 1,000 searches (up to 100 results per search)** | **$3.50+ per 1,000 searches or per listing fees** |
| **Speed** | **2 seconds per search** | 6 - 280 seconds |
| **Supported Countries** | **Multiple (US, CA, etc.)** | Limited |
| **Pricing Type** | **Fixed-price** | Varies |

Unlike traditional **per-listing** pricing (charging $3.50 per 1,000 results or higher), this actor charges **only $0.50 per 1,000 searches** (which can have up to 100 results each), making it the **cheapest option available**.

---

## Head-to-Head Cost & Performance Comparison

To ensure fairness, we ran the **same query for "Nike" (100 results) across all platforms**. For rental actors, average resource consumption was calculated based on Apify's pricing model, considering **compute units, storage, request queue operations, and proxy fees where applicable**. For **"per listing" pricing models**, it was assumed **100 listings are returned per search**.

It's worth noting that not all "results" are the same. While we consider a result the **entire search** (which can have to up 100 listings), others charge **per listing** in the search. Put differently, they are charging for every single of the 100 listings in the search result, while we charge once for the entire results.

Below is the cost breakdown for each competitor:

| Actor | Cost per 1M Searches | Price | Billing Model | Duration (s) | Formula |
| --- | --- | --- | --- | --- | --- |
| **scraperlink/google-search-results-serp-scraper (This Actor)** | **$500** | **$0.50 / 1,000 results** | **Per Search** | **2.0** | **Fixed: ($0.50 per 1K searches * 1M searches)** |
| devisty/google-search | $3,422 | $7/month + Actor usage fees | Compute-Based | 25.0 | ((0.0009 CU * 1M * $0.40) + (100M dataset writes * $0.40)) |
| apify/google-search-scraper | $3,500 | $3.50 / 1,000 results | Per Search | 7.0 | Fixed: ($3.50 per 1K searches * 1M searches) |
| serping/fast-google-search-results-scraper | $3,500 | $3.50 / 1,000 results | Per Search | 9.0 | Fixed: ($3.50 per 1K searches * 1M searches) |
| epctex/google-search-scraper | $2,907 | $20/month rental + Actor fees | Compute-Based | 6.0 | ((0.0002 CU * 1M * $0.40) + (1M KV reads * $0.40)) |
| hooli/easy-google-scraper | $100,000 | $1.00 / 1,000 results | Per Listing | 16.0 | Fixed: ($1.00 per 1K results * 1M searches * 100 listings) |
| quaking_pail/google-serp-scraper | $1,000,000 | $10.00 / 1,000 results | Per Listing | 280.0 | Fixed: ($10.00 per 1K results * 1M searches * 100 listings) |

**Actors That Failed to Generate Valid Results**

The following actors **failed to return valid results** in our tests:

- **caprolok/google-scraper**
- **glavier/google-web-search**
- **parse/google-search**

This highlights the importance of using **reliable, tested solutions** like this actor.

---

## How It Works

This actor makes API calls to retrieve Google Search results based on your query and stores them in Apify's dataset.

1. **Provide a keyword** (e.g., `"Nike shoes"`).
2. **Set additional parameters** (limit, page number, location, etc.).
3. **Receive structured search results** in JSON format.

---

## Input Parameters

| Parameter | Required | Default | Type | Description |
| --- | --- | --- | --- | --- |
| `keyword` | **Yes** | N/A | String | Search term (e.g., `"Elon Musk"` or `"Adidas site:youtube.com"`) |
| `limit` | No | `"10"` | Number | Results per page (`10`, `20`, `30`, `40`, `50`, `100`) |
| `page` | No | `"1"` | Number | Page number (overrides `start`) |
| `start` | No | N/A | Number | Custom starting index (ignored if `page` is used) |
| `country` | No | `"US"` | String | Automatically sets `proxy_location` and `gl` |
| `gl` | No | N/A | String | Country for localized results (ISO 3166 A-2) |
| `hl` | No | N/A | String | Google UI language (e.g., `"en"`, `"fr"`, `"zh-CN"`) |
| `tbs` | No | N/A | String | Time-based filter (e.g., `"qdr:d"` or `"cdr:1,cd_min:01/01/2023,cd_max:01/31/2023"`) |
| `lr` | No | N/A | String | Language restriction (e.g., `"lang_en"`, `"lang_fr"`) |
| `cr` | No | N/A | String | Country restriction (e.g., `"countryUS"`, `"countryCA"`) |
| `proxy_location` | No | `"us"` | String | Proxy location (`us`, `ca`, etc.) |

---

## Usage Examples

### Basic Search

```
{ "keyword": "Nike" }
```

### Paginated Search

```
{ "keyword": "Nike", "page": 2 }
```

### Location-Based Search

```
{ "keyword": "Nike", "country": "CA" }
```

### Use GL and HL for Localized Results

```
{ "keyword": "Nike", "gl": "FR", "hl": "fr" }
```

### Custom Result Limit

```
{ "keyword": "Nike", "limit": 50 }
```

### Time-Based Filter (TBS)

```
{ "keyword": "Nike", "tbs": "qdr:w" }
```

### Custom Date Range

```
{ "keyword": "Nike", "tbs": "cdr:1,cd_min:01/01/2023,cd_max:01/31/2023" }
```

---

## Output Format

The actor returns results in **JSON** format:

```
{
  "query": "Nike",
  "results": [
    {
      "position": 1,
      "title": "Nike Official Site",
      "url": "https://www.nike.com",
      "description": "Shop the latest Nike products."
    },
    ...
  ],
  "next_page": 2,
  "next_start": 10
}
```

To fetch the next page, simply update the `page` parameter.

---

## Rate Limits & Concurrent Runs

The actor allows up to **5 requests per second (RPS)** per account. Since keywords are processed sequentially within a single run, bulk keyword lists in a single run will not hit this limit.

If you run multiple instances simultaneously, please limit to **5 concurrent runs** at a time. For higher throughput requirements, contact us at: [info@scraperlink.com](mailto:info@scraperlink.com)

## Error Handling

If an invalid query or unsupported location is provided, the actor returns an error message:

```
{ "error": "Invalid location. Supported locations: US, CA." }
```

---

## Conclusion

- **Most cost-effective** Google Search Scraper available.
- **Per search pricing** ($1 per 1,000 searches) instead of high per-listing fees.
- **Fastest execution time** (2 seconds per search).
- **Supports multiple countries**.
- **Fixed pricing**, while competitors charge **varied, higher fees**.
- **Fully customizable** with pagination, location filtering, and more.

Start using our **Google Search Results (SERP) Scraper** today and experience **the best combination of speed, affordability, and accuracy**!