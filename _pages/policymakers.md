---
title: "Policymakers"
layout: page
permalink: /policymakers/
---

# Policymakers

<div class="callout callout-info" markdown="0" style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem;">
  <div>
    <div class="callout-title">Department of Psychology — Campus Albano</div>
    <p style="margin: 0;">Albanovägen 12, House 4, 114 19 Stockholm, Sweden</p>
  </div>
  <a href="https://google.com" target="_blank" rel="noopener" class="chip">Open in Google Maps →</a>
</div>

{% if site.posts.size > 0 %}
<div class="section-card" markdown="0">
{% for post in site.posts %}
<div class="news-item" style="padding: 1rem 0; border-bottom: 1px solid var(--border-color);">
<span class="news-date">{{ post.date | date: "%b %-d, %Y" }}</span><br>
<a href="{{ post.url | relative_url }}" style="font-weight: 600;">{{ post.title }}</a>
</div>
{% endfor %}
</div>
{% else %}
<p class="text-muted">No posts yet.</p>
{% endif %}
