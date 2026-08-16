---
title: "The HTML representation of the index API is now frozen"
url: "https://blog.pypi.org/posts/2026-08-11-html-index-is-frozen/"
date: "2026-08-11"
author: "William Woodruff"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
PyPI has adopted PEP 833 , which "freezes" the HTML representation of the index API , which is also sometimes called the "simple API" or the "simple repository API." New packages and releases will continue to appear in the HTML representation, meaning this has no breaking implications for downstream index consumers. However, future standardization and development efforts will focus on the JSON representation, and downstreams that consume only the HTML representation are strongly encouraged to transition to the JSON representation to ensure access to the latest and greatest index features. Back
