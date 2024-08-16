---
layout: page
title: Home
id: home
permalink: /
---

# Xin chào! 🌱

<p style="padding: 3em 1em; background: #f5f7ff; border-radius: 4px;">
  Để tìm hiểu về cách viết note hãy ấn vào đây <span style="font-weight: bold">[[Your first note]]</span> để tìm hiểu.
</p>

Đây là nơi ghi chép các ý tưởng của Nam the Man.
Nơi chia sẻ những hiểu biết vụn vặt

<strong>Các bài viết mới nhất</strong>

<ul>
  {% assign recent_notes = site.notes | sort: "last_modified_at_timestamp" | reverse %}
  {% for note in recent_notes limit: 5 %}
    <li>
      {{ note.last_modified_at | date: "%Y-%m-%d" }} — <a class="internal-link" href="{{ site.baseurl }}{{ note.url }}">{{ note.title }}</a>
    </li>
  {% endfor %}
</ul>

<style>
  .wrapper {
    max-width: 46em;
  }
</style>
