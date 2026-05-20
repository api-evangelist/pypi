---
title: "PyPI now serves project status markers in API responses"
url: "https://blog.pypi.org/posts/2025-08-14-project-status-markers/"
date: "Thu, 14 Aug 2025 06:09:00 +0000"
author: "William Woodruff"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
PyPI now serves project status markers in its standard index APIs . This allows downstream consumers (like Python package installers and index mirrors) to retrieve project statuses programmatically and use them to inform users when a project is archived or quarantined. Summary PyPI has implemented project status markers as proposed and accepted in PEP 792 .
