---
title: "Policymakers"
layout: page
permalink: /policymakers/
---

# Policymakers

<div style="width: 100%; border-radius: 8px; overflow: hidden; margin: 1.5rem 0;">
  <iframe 
    src="https://google.com" 
    width="100%" 
    height="350" 
    style="border: 0; display: block;" 
    allowfullscreen="" 
    loading="lazy" 
    referrerpolicy="no-referrer-when-downgrade">
  </iframe>
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
