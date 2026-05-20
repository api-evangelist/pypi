---
title: "Preventing ZIP parser confusion attacks on Python package installers"
url: "https://blog.pypi.org/posts/2025-08-07-wheel-archive-confusion-attacks/"
date: "Thu, 07 Aug 2025 06:09:00 +0000"
author: "Seth Larson"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
The Python Package Index is introducing new restrictions to protect Python package installers and inspectors from confusion attacks arising from ZIP parser implementations. This has been done in response to the discovery that the popular installer uv has a different extraction behavior to many Python-based installers that use the ZIP parser implementation provided by the zipfile standard library module. Summary ZIP archives constructed to exploit ZIP confusion attacks are now rejected by PyPI.
