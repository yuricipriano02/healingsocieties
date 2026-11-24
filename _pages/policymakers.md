---
title: "Policymakers"
layout: page
permalink: /policymakers/
---

# Policymakers

[Choosing Intergroup Interventions Across Contact Ecologies]({{ '/assets/44666_2_supp_345048_tlvdcd.htm' | relative_url }}){:target="_blank"}

{% if site.posts.size > 0 %}
<div class="section-card" markdown="0">
{% for post in site.posts %}
<div class="news-item" style="padding: 1rem 0; border-bottom: 1px solid var(--border-color);">
<span class="news-date">{{ post.date | date: "%b %-d, %Y" }}</span><br>
<a href="{{ post.url | relative_url }}" style="font-weight: 600;">{{ Choosing Intergroup Interventions Across Contact Ecologies }}</a>
</div>
{% endfor %}
</div>
{% else %}
<p class="text-muted">No posts yet.</p>
{% endif %}
