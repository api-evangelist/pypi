---
title: "Releases now reject new files after 14 days"
url: "https://blog.pypi.org/posts/2026-07-22-releases-now-reject-new-files-after-14-days/"
date: "2026-07-22"
author: "Seth Larson"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
The Python Package Index (PyPI) now rejects new files being uploaded to releases that are older than 14 days. This restriction was put in place to prevent old and long-stable releases from being poisoned in case publishing tokens or workflows of PyPI projects were compromised. As far as we are aware this has not yet been abused, but there is no technical reason beyond that attackers weren't aware it was possible.
