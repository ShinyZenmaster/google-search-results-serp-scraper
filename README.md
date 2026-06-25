[Google Search Results Serp Scraper](https://apify.com/vtrdev/google-search-results-serp-scraper?fpr=data)

![Google SERP Scraper](https://images.apifyusercontent.com/mlQgpnqLMsbEISN4QPQvl1pm09mDHczdlILDf1dI9wM/w:1800/cb:1/aHR0cHM6Ly9yZXMuY2xvdWRpbmFyeS5jb20vZGpvNW9oMmM2L2ltYWdlL3VwbG9hZC92MTc1ODE4ODAxNi9zZXJwLWFjdG9yX3FpZ3VhZy53ZWJw.webp)

# 🔍 Google Search Results (SERP) Scraper

Extract Google search results in seconds with **99%+ accuracy**. Get clean, structured JSON data ready for your SEO tools, market research, and competitive analysis.

---

## 🚀 Why Choose This Scraper?

- **Lightning Fast** → Results in 3-5 seconds per page
- **99%+ Success Rate** → Reliable extraction, even when Google changes layouts
- **Multi-Page Support** → Scrape up to 10 pages (100+ results) in one run
- **100+ Countries** → Localized results from any country
- **Smart Title Recovery** → Complete titles, even when Google truncates them
- **Ready-to-Use JSON** → Drop directly into your databases and applications

---

## 💼 Perfect For

| Use Case | What You Get |
| --- | --- |
| **SEO Professionals** | Track rankings, monitor competitors, analyze SERP features |
| **Marketers** | Market research, trend analysis, content gap discovery |
| **Business Owners** | Lead generation, brand monitoring, reputation management |
| **Researchers** | Academic studies, consumer behavior analysis, data collection |
| **Agencies** | Client reporting, competitive intelligence dashboards |

---

## 💸 Simple, Transparent Pricing

**$5.00 per 1,000 results**

- **Free trial**: Up to 50 results to test the scraper
- Pay only for what you use
- No setup fees
- No monthly commitments
- Upgrade anytime to unlock unlimited results

---

## 🎯 How It Works

```
┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
│   1. Input      │  →   │   2. Scrape     │  →   │   3. Export     │
│                 │      │                 │      │                 │
│  • Keyword      │      │  • Google SERP  │      │  • JSON Dataset │
│  • Pages (1-10) │      │  • All Results  │      │  • Ready to Use │
│  • Country      │      │  • Metadata     │      │                 │
└─────────────────┘      └─────────────────┘      └─────────────────┘
      1 min                    3-5 sec                Instant
```

---

## ⚡ Performance You Can Count On

- **Speed**: 3-5 seconds per page
- **Scale**: Up to 10 pages per run (100+ results)
- **Success Rate**: 99%+ accurate extraction
- **Global**: 100+ countries supported

---

## 📝 Input Parameters

| Parameter | Type | Description | Default |
| --- | --- | --- | --- |
| `keyword` | string | Search term to scrape | *Required* |
| `pages` | integer | Number of pages (1-10) | `1` |
| `country` | string | Country code (US, UK, ID, etc.) | `"US"` |
| `language` | string | Language code (en, id, fr, etc.) | `"en"` |

---

## 💡 Quick Start

```
{
  "keyword": "best coffee shops NYC",
  "pages": 2,
  "country": "US",
  "language": "en"
}
```

That's it! Get 20+ results in under 10 seconds.

---

## 📊 What You Get

```
[
  {
    "title": "The 10 Best Coffee Shops in NYC - 2025 Guide",
    "url": "https://example.com/best-nyc-coffee",
    "displayedUrl": "example.com › guides › nyc-coffee",
    "description": "Discover New York's best coffee shops...",
    "position": 1,
    "page": 1,
    "query": "best coffee shops NYC",
    "search_country": "US",
    "timestamp": "2025-01-03T10:30:00.000Z"
  }
]
```

**Every result includes:**

- Title (auto-recovered if truncated)
- URL and displayed URL
- Meta description
- Position and page number
- Search metadata
- Timestamp

---

## 🌍 Supported Countries

United States, United Kingdom, Canada, Australia, Germany, France, Spain, Italy, Netherlands, Japan, South Korea, Indonesia, Singapore, India, Brazil, Mexico, and **100+ more**.

Just use the country code: `US`, `UK`, `ID`, `JP`, `BR`, etc.

---

## ❓ Frequently Asked Questions

**Q: Is this legal to use?**
A: Yes! Public search results are legal to scrape for research and analysis purposes.

**Q: How accurate is the data?**
A: We maintain 99%+ accuracy with our dual-strategy parsing that adapts to Google's layout changes.

**Q: Can I scrape multiple pages at once?**
A: Yes! Scrape up to 10 pages (100+ results) in a single run.

**Q: What if Google blocks the request?**
A: Our built-in redundancy handles blocks automatically with retries and fallbacks.

**Q: Do I need to provide my own proxies?**
A: No! Everything is included. Just run the actor and get your data.

**Q: Can I try before I buy?**
A: Absolutely! Start with free test runs to see the results yourself.

---

## 📞 Need Help?

Check out our documentation or reach out through Apify's support channels. We're here to help you get the data you need!

---

**Ready to scrape?** Click "Try" to get started in seconds.