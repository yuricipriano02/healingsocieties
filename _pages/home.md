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
<a href="{{ '/research' | relative_url }}" class="chip">Interventions</a>
<a href="{{ '/research' | relative_url }}" class="chip">Group Dynamics</a>
<a href="{{ '/research' | relative_url }}" class="chip">Intergroup Relations</a>
<a href="{{ '/research' | relative_url }}" class="chip">Social Identity</a>
</div>

Our research aims to understand the psychological processes and mechanisms of improving intergroup relations in societies affected or threatened by conflict. Using experimental methods across different social contexts, we study attitudes and emotions in order to develop effective intergroup interventions that promote positive social change.

<!-- Callout box: callout-success, callout-warning, or callout-info -->
<div class="callout callout-success" markdown="0">
<div class="callout-title">{% include icon.html name="award" class="callout-icon" %} </div>
<p></p>
</div>

<!-- Banner image with caption; place the image in images/ -->
<div class="banner-frame" markdown="0">
<img src="{{ '/images/banner/banner.webp' | relative_url }}" alt="Describe the image" width="1400" height="449" loading="lazy">
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

I am a Full Professor of Social Psychology at Stockholm University, where I lead the research group on Intergroup Relations and Social Change. My research focuses on improving intergroup relations in contexts of conflict. It is supported by various governmental research councils and agencies, including the European Research Council, the Swedish Research Council, Riksbankens Jubileumsfond, ESRC, and the British Academy. In addition to my research, I serve as an Associate Editor for Peace and Conflict: Journal of Peace Psychology and as a Consulting Editor for the Journal of Personality and Social Psychology, European Journal of Social Psychology, and Political Psychology. I also teach courses in social and political psychology, with a particular focus on group processes and intergroup relations.
