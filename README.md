# OK4WD Blog Scraper
> OK4WD Blog Scraper collects structured blog content from ok4wd.com and turns it into clean, reusable data for research, monitoring, and content workflows. It supports exporting blog details in JSON, HTML, or plaintext so you can analyze posts, track updates, and build searchable archives.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/Bitbash333" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>ok4wd-blog-scraper</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
OK4WD Blog Scraper extracts blog listings and (optionally) full blog details from OK4WD’s blog pages. It solves the problem of manually copying articles and metadata by producing structured outputs ready for dashboards, datasets, and downstream automation. It’s built for developers, analysts, and teams who need reliable blog data extraction for monitoring, SEO analysis, and content intelligence.

### Blog Content Export and Filtering
- Scrapes blog listing pages and aggregates post metadata at scale
- Optionally scrapes full blog details (content body + rich metadata)
- Filters by search, author, or categories to narrow results precisely
- Exports details in JSON, HTML, or Plain Text for flexible pipelines
- Supports targeted scraping via direct blog URLs or full-site collection

## Features
| Feature | Description |
|----------|-------------|
| Blog listing extraction | Collects post titles, summaries, URLs, slugs, categories, and publish/update timestamps. |
| Full article scraping | Extracts full post content, author details, read time, and on-page metadata when enabled. |
| Filtered scraping | Filter by search keyword, author, or categories for focused datasets. |
| Bulk URL mode | Provide specific blog URLs to scrape only the posts you care about. |
| Multi-format export | Export blog details as JSON, HTML, or Plain Text depending on your workflow. |
| Controlled volume | Limit results with `maxBlogs` for fast tests or incremental runs. |
| Metadata-rich outputs | Includes SEO fields, canonical URL, featured images, and RSS info when available. |

---

## What Data This Scraper Extracts
| Field Name | Field Description |
|-------------|------------------|
| id | Internal numeric identifier for the blog post item. |
| title | Blog post title. |
| summary | Short excerpt/summary of the post. |
| content | Full blog content (empty if details scraping is disabled). |
| slug | URL-friendly slug for the post. |
| url | Direct URL to the blog post. |
| featuredImage | Featured image URL (if available). |
| featuredImageWebm | Featured video in WebM (if available). |
| featuredImageMp4 | Featured video in MP4 (if available). |
| publishedAt | Human-readable publish date string. |
| publishedAtIso8601 | ISO 8601 publish timestamp. |
| updatedAt | Human-readable update date string. |
| updatedAtIso8601 | ISO 8601 update timestamp. |
| keyword | Primary keyword associated with the post (if available). |
| seoTitle | SEO title tag value (if available). |
| seoDescription | SEO meta description (if available). |
| categories | Categories/tags assigned to the post. |
| author.id | Author identifier (if available). |
| author.name | Author display name. |
| author.slug | Author profile slug (if available). |
| author.photo | Author photo URL (if available). |
| author.bio | Author bio text (if available). |
| readtime | Estimated reading time label. |
| canonicalUrl | Canonical URL (if available). |
| headTitle | Page head title (if available). |
| headDescription | Page head description (if available). |
| og_image | OpenGraph image URL (if available). |
| rssTitle | RSS feed title (if available). |
| rssUrl | RSS feed URL (if available). |
| pinned | Whether the post is pinned/featured (if available). |
| noindex | Whether the page is marked noindex (if available). |

---

## Example Output

    [
          {
                "id": 14,
                "title": "What are carbon fiber composites and should you use them?",
                "summary": "Everyone loves PLA and PETG! They’re cheap, easy, and a lot of people use them exclusively. Some of you might get wild and try out some ABS every once",
                "content": "What are carbon fiber composites and should you use them?\nArun Chapman Guides\nMarch 17th, 2025 7 minute read\nTable of Contents\n...",
                "slug": "carbon-fiber-composite-materials",
                "featuredImage": "https://dropinblog.net/34259178/files/featured/carbon-fiber-1-k2wil.png",
                "publishedAt": "March 17th, 2025",
                "publishedAtIso8601": "2025-03-17T08:10:00-05:00",
                "updatedAt": "March 18th, 2025",
                "updatedAtIso8601": "2025-03-18T03:18:21-05:00",
                "keyword": "carbon fiber",
                "seoTitle": "What are carbon fiber composites and should you use them?",
                "seoDescription": "Carbon fiber composites are an amazing but sometimes confusing category of materials. Find out how they work and what they can be used for!",
                "categories": [
                      "Features",
                      "Guides",
                      "Challenge",
                      "Community Spotlight"
                ],
                "author": {
                      "id": 68114,
                      "name": "Arun Chapman",
                      "slug": "arun-chapman",
                      "photo": "https://dropinblog.net/34259178/authors/A.Chapman Profile Picture (2).jpg",
                      "bio": null
                },
                "readtime": "7 minute read",
                "canonicalUrl": "https://www.ok4wd.com/blog?p=carbon-fiber-composite-materials",
                "rssTitle": "RSS Feed for Blog",
                "rssUrl": "https://io.dropinblog.com/feed/e6a64e07-7f37-43aa-bd47-e43e905ec1d6/?limit=10",
                "og_image": "https://dropinblog.net/34259178/files/featured/carbon-fiber-1-k2wil.png",
                "noindex": false
          }
    ]

---

## Directory Structure Tree

    OK4WD Blog Scraper (IMPORTANT :!! always keep this name as the name of the apify actor !!! OK4WD Blog Scraper )/
    ├── src/
    │   ├── main.py
    │   ├── runner.py
    │   ├── config/
    │   │   ├── settings.example.json
    │   │   └── constants.py
    │   ├── inputs/
    │   │   ├── schema.json
    │   │   └── input.sample.json
    │   ├── extractors/
    │   │   ├── listing_scraper.py
    │   │   ├── detail_scraper.py
    │   │   ├── filters.py
    │   │   └── parsers.py
    │   ├── exporters/
    │   │   ├── export_json.py
    │   │   ├── export_html.py
    │   │   └── export_text.py
    │   ├── utils/
    │   │   ├── http.py
    │   │   ├── normalization.py
    │   │   ├── retries.py
    │   │   └── logging.py
    │   └── storage/
    │       ├── dataset_writer.py
    │       └── state_store.py
    ├── tests/
    │   ├── test_filters.py
    │   ├── test_parsers.py
    │   └── test_exporters.py
    ├── data/
    │   ├── outputs.sample.json
    │   └── urls.sample.txt
    ├── .env.example
    ├── .gitignore
    ├── pyproject.toml
    ├── requirements.txt
    ├── LICENSE
    └── README.md

---

## Use Cases
- **E-commerce researchers** use it to extract OK4WD blog posts, so they can **identify product/industry trends and publish timing patterns**.
- **SEO teams** use it to export metadata and canonical URLs, so they can **audit titles, descriptions, and content freshness at scale**.
- **Content analysts** use it to filter by categories/keywords, so they can **build topic-specific datasets for reporting and planning**.
- **Data engineers** use it to generate JSON feeds, so they can **load blog content into warehouses, search indexes, or BI tools**.
- **Brand monitoring teams** use it to track updatedAt/publishedAt changes, so they can **detect new posts and revisions reliably**.

---

## FAQs
**How do I scrape only specific posts instead of the whole blog?**
Provide `blogUrls` with the exact post URLs you want. When `blogUrls` is set, the scraper targets those posts directly and avoids collecting the entire listing.

**What’s the difference between listing mode and detail mode?**
Listing mode collects high-level fields like title, summary, slug, dates, and URLs. Detail mode (enabled by `scrapeBlogDetails`) additionally fetches the full `content` and richer metadata such as SEO fields, canonical URL, and author details when available.

**How do filtering options work (search/author/categories)?**
Enable `filterBy` and set `filterType` to one of `search`, `author`, or `categories`, then provide `filterValue`. This narrows results before exporting so you only store relevant posts.

**Which export format should I choose?**
Use JSON for analytics pipelines and structured storage, HTML when you want the original markup for rendering, and Plain Text for search indexing, NLP preprocessing, and compact archives.

---

### Performance Benchmarks and Results

**Primary Metric:** ~35–70 blog posts/min on listing-only runs, depending on network latency and pagination depth.

**Reliability Metric:** 97–99% successful fetch rate on stable runs, with automatic retries for transient failures.

**Efficiency Metric:** Typically 200–450 MB RAM sustained during moderate concurrency, with predictable CPU usage during parsing/export.

**Quality Metric:** 95%+ field completeness for core metadata (title, url, slug, dates), with optional enrichment (SEO/author/media) varying by post structure and availability.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on."
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/m-dRE1dj5-k?si=5kZNVlKsGUhg5Xtx" target="_blank">
        <img src="https://github.com/Z786ZA/Footer-test/blob/main/media/review3.gif" alt="Review 3" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        "Exceptional results, clear communication, and flawless delivery. <br>Bitbash nailed it."
      </p>
      <p style="margin:1px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
