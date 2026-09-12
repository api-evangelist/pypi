---
title: "Metadata requests no longer tracked in PyPI download counts"
url: "https://blog.pypi.org/posts/2026-08-31-download-counts/"
date: "2026-08-31"
author: "Mike Fiedler"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
On 2026-08-24 I shipped a change to the configuration that emits PyPI's download logs so that only requests for actual distribution artifacts are counted. A request has to end in .whl , .tar.gz , or .zip to produce a download record. The counts are more accurate now, and existing systems based on PyPI's BigQuery dataset , like pypistats.org will display a different shape going forward.
