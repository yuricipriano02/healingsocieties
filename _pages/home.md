---
title: "Home"
layout: homelay
permalink: /
---

<h1 class="home-hero">{{ site.name }}</h1>
<p class="home-hero-sub">{{ site.title }}, {{ site.institution }}</p>

<!-- Animated line-art motif: a visual metaphor for connection and reconciliation. -->
<div class="hero-animation" aria-hidden="true">
  <svg class="hero-weave" viewBox="0 0 900 230" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path class="weave-line weave-line-a" d="M92 116C166 14 282 14 356 116S546 218 620 116 764 14 838 116" />
    <path class="weave-line weave-line-b" d="M92 116C166 218 282 218 356 116S546 14 620 116 764 218 838 116" />
    <path class="weave-line weave-line-c" d="M92 116H808M356 116C356 65 397 35 450 35S544 65 544 116 503 197 450 197 356 167 356 116Z" />
    <circle class="weave-node node-a" cx="92" cy="116" r="7" />
    <circle class="weave-node node-b" cx="356" cy="116" r="7" />
    <circle class="weave-node node-c" cx="544" cy="116" r="7" />
    <circle class="weave-node node-d" cx="808" cy="116" r="7" />
  </svg>
</div>

<!-- Research-area chips (link to /projects) -->
<div class="chip-container" markdown="0">
<a href="{{ '/projects' | relative_url }}" class="chip">Social Psychology</a>
<a href="{{ '/projects' | relative_url }}" class="chip">Conflict and Reconciliation</a>
<a href="{{ '/projects' | relative_url }}" class="chip">Interventions</a>
<a href="{{ '/projects' | relative_url }}" class="chip">Group Dynamics</a>
<a href="{{ '/projects' | relative_url }}" class="chip">Intergroup Relations</a>
<a href="{{ '/projects' | relative_url }}" class="chip">Social Identity</a>
</div>

<!-- Banner image with caption; place the image in images/ -->
<div class="banner-frame" markdown="0">
<img src="{{ '/images/banner/banner.webp' | relative_url }}" alt="Describe the image" width="1400" height="449" loading="lazy">
</div>

Our research aims to understand the psychological processes and mechanisms of improving intergroup relations in societies affected or threatened by conflict. Using experimental methods across different social contexts, we study attitudes and emotions in order to develop effective intergroup interventions that promote positive social change.

<!-- Callout box: callout-success, callout-warning, or callout-info -->
<div class="callout callout-info" markdown="0" style="display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 1rem;">
  <div>
    <div class="callout-title">Department of Psychology — Campus Albano</div>
    <p style="margin: 0;">Albanovägen 12, House 4, 114 19 Stockholm, Sweden</p>
  </div>
  <a href="https://www.google.com/maps/place/Department+of+Psychology+-+Stockholm+University/@59.3552945,18.0556447,17z/data=!3m1!4b1!4m6!3m5!1s0x465f9d0f1f8233af:0x83225cd81274bb19!8m2!3d59.3552945!4d18.058225!16s%2Fg%2F1hc3dqc0j?entry=ttu&g_ep=EgoyMDI2MTExNy4wIKXMDSoASAFQAw%3D%3D" target="_blank" rel="noopener" class="chip">Open in Google Maps →</a>
</div>

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
## Selected publications

<div class="section-card selected-pubs" markdown="0">
{{ selected }}
<p style="margin: var(--space-4) 0 0;"><a href="{{ '/publications' | relative_url }}">All publications &rarr;</a></p>
</div>
{% endif %}
