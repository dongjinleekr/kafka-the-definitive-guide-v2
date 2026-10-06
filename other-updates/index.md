---
layout: default
title: 기타 업데이트
---

{% assign other_updates = site.posts | where: "update_type", "other" %}
{% include update-archive.html title="기타 업데이트" updates=other_updates empty_text="기타 업데이트를 준비하고 있습니다." %}
