---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub">{{ site.title }}, {{ site.institution }}</p>

<!-- Research-area chips (link to /research) -->
<div class="chip-container" markdown="0">
<a href="{{ '/research' | relative_url }}" class="chip">Social Psychology</a>
<a href="{{ '/research' | relative_url }}" class="chip">Conflict and Reconciliation</a>
<a href="{{ '/research' | relative_url }}" class="chip">Emotions</a>
<a href="{{ '/research' | relative_url }}" class="chip">Interventions</a>
<a href="{{ '/research' | relative_url }}" class="chip">Group Dynamics</a>
<a href="{{ '/research' | relative_url }}" class="chip">Dehumanization</a>
<a href="{{ '/research' | relative_url }}" class="chip">Victimization</a>
<a href="{{ '/research' | relative_url }}" class="chip">Empathy</a>
<a href="{{ '/research' | relative_url }}" class="chip">Intergroup Relations</a>
<a href="{{ '/research' | relative_url }}" class="chip">Social Emotions</a>
<a href="{{ '/research' | relative_url }}" class="chip">Forgiveness</a>
<a href="{{ '/research' | relative_url }}" class="chip">Social Identity</a>
</div>

Introduce your research in a few sentences. This first paragraph is set slightly larger than the rest.

<!-- Callout box: callout-success, callout-warning, or callout-info -->
<div class="callout callout-success" markdown="0">
<div class="callout-title">{% include icon.html name="award" class="callout-icon" %} Nobel Prize in Physics, 1965</div>
<p>One or two sentences.</p>
</div>

<!-- Banner image with caption; place the image in images/ -->
<div class="banner-frame" markdown="0">
<img src="{{ '/images/banner.webp' | relative_url }}" alt="Describe the image" width="1400" height="449" loading="lazy">
<div class="banner-caption">Healing Societies</div>
</div>

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Selected publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>
{% endif %}

## About me

Your biography goes here. The README shows how to add research-area chips, callout boxes, and a banner image.
