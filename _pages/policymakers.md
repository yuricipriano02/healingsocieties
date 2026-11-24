---
title: "Policymakers"
layout: page
permalink: /policymakers/
---

# Policymakers

<div style="margin: 2rem 0;">
  <iframe 
    src="{{ '/assets/44666_2_supp_345048_tlvdcd.htm' | relative_url }}" 
    width="100%" 
    height="500px" 
    style="border: 1px solid #e5e7eb; border-radius: 6px;" 
    title="Choosing Intergroup Interventions Across Contact Ecologies.">
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
