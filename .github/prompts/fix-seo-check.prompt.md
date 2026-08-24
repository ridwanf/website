---
description: you are a SEO expert. Fix the SEO issues based on the SEO check results. Use this prompt when you want to fix SEO issues on a page.
---

fix the SEO issues based on the SEO check results. Use the SEO check results to identify and correct any problems that may be affecting the page's search engine ranking.
this is the SEO check results:
{
"version": "1.0",
"url": "https://ridwanfansuri.com/",
"score": 61,
"summary": {
"total": 18,
"passed": 10,
"failed": 1,
"warnings": 7
},
"categories": [
{
"category": "meta-tags",
"score": 64,
"totalWeight": 42,
"earnedWeight": 27,
"checks": [
{
"id": "META001",
"rule": "Title Tag Exists",
"category": "meta-tags",
"passed": true,
"message": "Page has a title tag."
},
{
"id": "META002",
"rule": "Title Length",
"category": "meta-tags",
"passed": false,
"message": "Title length is 29 characters. Optimal is 30–60.",
"severity": "minor",
"recommendation": "Rewrite the title to be between 30 and 60 characters.",
"why": "Titles that are too short may not rank for enough keywords. Titles that are too long get truncated in search results.",
"fixExamples": [
{
"title": "Lengthen the Title",
"before": "<title>Ridwan Fansuri — Frontend Dev</title>",
"after": "<title>Ridwan Fansuri — Frontend Dev — Your Keyword & Benefit Here</title>",
"explanation": "Add more context, e.g., include your primary keyword + a benefit."
}
]
},
{
"id": "META003",
"rule": "Meta Description Exists",
"category": "meta-tags",
"passed": true,
"message": "Page has a meta description."
},
{
"id": "META004",
"rule": "Meta Description Length",
"category": "meta-tags",
"passed": false,
"message": "Meta description is 50 characters. Optimal is 120–160.",
"severity": "minor",
"recommendation": "Rewrite the meta description to be between 120 and 160 characters.",
"why": "Descriptions that are too short are less persuasive. Descriptions that are too long get truncated in search results.",
"fixExamples": [
{
"title": "Increase Meta Description Length",
"before": "<meta name=\"description\" content=\"Ridwan Fansuri —Frontend Developer. and Guitarist.\">",
"after": "<meta name=\"description\" content=\"Ridwan Fansuri —Frontend Developer. and Guitarist. Add more details to reach 120–160 characters, including a CTA.\">",
"explanation": "Optimal meta description length is 120–160 characters. Too short misses ranking signals; too long gets truncated."
}
]
},
{
"id": "META005",
"rule": "Viewport Meta Tag",
"category": "meta-tags",
"passed": true,
"message": "Viewport meta tag is present: \"width=device-width, initial-scale=1.0\"."
}
]
},
{
"category": "content",
"score": 100,
"totalWeight": 22,
"earnedWeight": 22,
"checks": [
{
"id": "CON001",
"rule": "H1 Heading Exists",
"category": "content",
"passed": true,
"message": "Page has one H1 heading: \"Hi, I'm Ridwan Fansuri\"."
},
{
"id": "CON002",
"rule": "Image Alt Text",
"category": "content",
"passed": true,
"message": "All 7 images have alt text."
},
{
"id": "CON003",
"rule": "Heading Hierarchy",
"category": "content",
"passed": true,
"message": "Proper heading hierarchy with 14 headings."
}
]
},
{
"category": "technical",
"score": 68,
"totalWeight": 37,
"earnedWeight": 25,
"checks": [
{
"id": "TECH001",
"rule": "Canonical URL",
"category": "technical",
"passed": false,
"message": "Page is missing a canonical URL.",
"severity": "major",
"recommendation": "Add <link rel=\"canonical\" href=\"https://yourdomain.com/page\"> to the <head> section.",
"why": "Canonical tags prevent duplicate content issues by telling search engines which URL is the preferred version.",
"fixExamples": [
{
"title": "Add a Canonical URL",
"before": "<head>\n <title>Page Title</title>\n</head>",
"after": "<head>\n <title>Page Title</title>\n <link rel=\"canonical\" href=\"https://example.com/preferred-url\">\n</head>",
"explanation": "The canonical tag tells search engines which URL is the master copy. This prevents duplicate content issues."
}
]
},
{
"id": "TECH003",
"rule": "HTML Lang Attribute",
"category": "technical",
"passed": true,
"message": "HTML lang attribute is set to \"en\"."
},
{
"id": "TECH004",
"rule": "Favicon",
"category": "technical",
"passed": false,
"message": "No favicon found.",
"severity": "minor",
"recommendation": "Add <link rel=\"icon\" href=\"/favicon.ico\"> to the <head> section.",
"why": "Favicons improve brand recognition and appear in browser tabs, bookmarks, and search results.",
"fixExamples": [
{
"title": "Use HTTPS",
"before": "http://example.com",
"after": "https://example.com",
"explanation": "HTTPS is a confirmed ranking signal. It encrypts data between the browser and server, protecting user privacy."
},
{
"title": "Set Up a Redirect",
"before": "// Old HTTP URL → returns 200 OK directly",
"after": "// Add a 301 redirect in your server config:\n// Apache: Redirect 301 / https://example.com/\n// Nginx: return 301 https://$host$request_uri;",
"explanation": "Set up a 301 permanent redirect from HTTP to HTTPS to preserve link equity and avoid duplicate content."
}
]
},
{
"id": "TECH002",
"rule": "HTTPS Protocol",
"category": "technical",
"passed": true,
"message": "Page uses HTTPS protocol."
},
{
"id": "TECH005",
"rule": "Robots Meta Tag",
"category": "technical",
"passed": true,
"message": "No robots meta tag — page is indexable by default."
}
]
},
{
"category": "social",
"score": 0,
"totalWeight": 13,
"earnedWeight": 0,
"checks": [
{
"id": "SOC001",
"rule": "Open Graph Tags",
"category": "social",
"passed": false,
"message": "Missing Open Graph tags: og:image.",
"severity": "minor",
"recommendation": "Add the missing Open Graph tags to the <head> section: og:image.",
"why": "Open Graph tags control how your page appears when shared on Facebook, LinkedIn, and other platforms."
},
{
"id": "SOC002",
"rule": "Twitter Card Tags",
"category": "social",
"passed": false,
"message": "Missing Twitter Card tags: twitter:card, twitter:title, twitter:image.",
"severity": "minor",
"recommendation": "Add the missing Twitter Card tags to the <head>: twitter:card, twitter:title, twitter:image.",
"why": "Twitter uses these tags to generate rich previews when your page is shared on Twitter/X."
}
]
},
{
"category": "performance",
"score": 44,
"totalWeight": 9,
"earnedWeight": 4,
"checks": [
{
"id": "PERF002",
"rule": "Inline CSS Size",
"category": "performance",
"passed": true,
"message": "Inline CSS size is acceptable (2.87KB)."
},
{
"id": "PERF001",
"rule": "External Scripts",
"category": "performance",
"passed": false,
"message": "1 of 2 external scripts are render-blocking.",
"severity": "minor",
"recommendation": "Add async or defer attribute to all external <script> tags.",
"why": "Render-blocking scripts delay page load by preventing the browser from parsing HTML until the script finishes downloading and executing.",
"fixExamples": [
{
"title": "Inline CSS Alternatives",
"before": "<p style=\"color: red; font-size: 16px; margin: 10px 0;\">Text</p>",
"after": "<p class=\"highlight\">Text</p>\n\n<!-- In your CSS file: -->\n<!-- .highlight { color: red; font-size: 16px; margin: 10px 0; } -->",
"explanation": "Move inline styles to an external stylesheet. This reduces HTML size, improves cacheability, and makes maintenance easier."
}
]
}
]
},
{
"category": "accessibility",
"score": 0,
"totalWeight": 5,
"earnedWeight": 0,
"checks": [
{
"id": "ACC001",
"rule": "ARIA Labels",
"category": "accessibility",
"passed": false,
"message": "1 of 2 interactive elements are missing labels.",
"severity": "minor",
"recommendation": "Add aria-label attributes or visible text to all buttons and interactive links.",
"why": "ARIA labels are used by screen readers to describe interactive elements to visually impaired users."
}
]
}
],
"crawl": {
"originalUrl": "https://ridwanfansuri.com",
"finalUrl": "https://ridwanfansuri.com/",
"status": 200,
"responseTime": {
"total": 675
},
"contentType": "text/html; charset=utf-8",
"pageSize": 51248,
"protocol": "HTTP/1.1",
"server": "GitHub.com",
"redirectChain": [],
"robots": {
"found": false
},
"sitemap": {
"found": false
},
"headers": {
"connection": "keep-alive",
"content-length": "9950",
"server": "GitHub.com",
"content-type": "text/html; charset=utf-8",
"last-modified": "Mon, 10 Aug 2026 05:06:11 GMT",
"access-control-allow-origin": "\*",
"etag": "W/\"6a795c43-c830\"",
"expires": "Mon, 24 Aug 2026 13:44:52 GMT",
"cache-control": "max-age=600",
"x-proxy-cache": "MISS",
"x-github-request-id": "64B0:0C3A:1A1F7F:1B804A:6A8C487A",
"x-github-edge-region": "southeastasia",
"accept-ranges": "bytes",
"age": "0",
"date": "Mon, 24 Aug 2026 13:34:52 GMT",
"via": "1.1 varnish",
"x-served-by": "cache-sin-wsss1830086-SIN",
"x-cache": "MISS",
"x-cache-hits": "0",
"x-timer": "S1787578492.222620,VS0,VE236",
"vary": "Accept-Encoding",
"x-fastly-request-id": "7f2098d35a949a9270b2cb85d71cba0bb6078af7"
}
},
"scoreBreakdown": {
"earnedWeight": 78,
"totalWeight": 128,
"percentage": 61
},
"createdAt": "2026-08-24T13:34:53.097Z"
}
