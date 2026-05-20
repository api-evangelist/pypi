---
title: "Incident Report: Organizations Team privileges"
url: "https://blog.pypi.org/posts/2025-04-14-incident-report-organization-team-privileges/"
date: "Mon, 14 Apr 2025 06:09:00 +0000"
author: "Ee Durbin"
feed_url: "https://blog.pypi.org/feed_rss_created.xml"
---
On April 14, 2025 security@pypi.org was notified of a potential security concern relating to privileges granted to a PyPI User via Organization Teams membership persisting after the User was removed from the PyPI Organization the Team belongs to. We validated the report as a true finding, identified all cases where this scenario had occurred, notified impacted parties, and released a fix. A full audit determined that all instances were accounted for, with no unauthorized actions taken as a result of the issue.
