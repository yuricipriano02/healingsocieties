---
title: "Team"
layout: page
permalink: /team/
---

# PI

<div class="section-card" style="position: relative;">
<div class="pi-card">
<img src="{{ site.photo | prepend: '/images/' | relative_url }}" class="pi-photo" alt="{{ site.card_name }}" width="160" height="160">
<div>
<h3 class="pi-name"><a href="https://www.su.se/english/profiles/s/sace4538" target="_blank" rel="noopener" style="text-decoration: none; color: inherit;">{{ site.card_name }}<span style="position: absolute; inset: 0; z-index: 1;"></span></a></h3>
<p style="font-style: italic; color: var(--text-secondary);">{{ site.card_title }}, {{ site.institution }}</p>
<p class="team-bio" style="margin-top: 0.75rem;"></p>
<div class="pi-links" style="position: relative; z-index: 2;">
{% if site.email %}<a href="mailto:{{ site.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if site.links.google_scholar and site.links.google_scholar != "" %}<a href="{{ site.links.google_scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if site.links.cv and site.links.cv != "" %}<a href="{{ site.links.cv | prepend: '/' | relative_url }}" class="icon-link" title="CV" aria-label="CV">{% include icon.html name="cv" %}</a>{% endif %}
{% if site.links.github and site.links.github != "" %}<a href="{{ site.links.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
{% if site.links.researchgate and site.links.researchgate != "" %}<a href="{{ site.links.researchgate }}" class="icon-link" title="ResearchGate" aria-label="ResearchGate">{% include icon.html name="researchgate" %}</a>{% endif %}
</div>
{% if site.data.pi[0].education %}
<ul style="margin-top: var(--space-4);">
{% for education in site.data.pi[0].education %}
<li>{{ education | replace: "-","–" }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
</div>
</div>


{% if site.data.team_members.size > 0 %}
## Members

<div class="team-grid">
{% for member in site.data.team_members %}
<div class="team-card" style="position: relative;">
<img src="{{ member.photo | prepend: '/images/' | relative_url }}" class="team-photo" alt="{{ member.name }}" width="100" height="100" loading="lazy">
<h3 class="team-name">
{% if member.website %}
<a href="{{ member.website | relative_url }}" style="text-decoration: none; color: inherit;">{{ member.name }}<span style="position: absolute; inset: 0; z-index: 1;"></span></a>
{% else %}
{{ member.name }}
{% endif %}
</h3>
<p class="team-info">{{ member.info }}</p>
{% if member.bio %}<p class="team-bio" style="font-size: 0.9rem; margin-top: 0.5rem;">{{ member.bio }}</p>{% endif %}
<div class="team-links" style="position: relative; z-index: 2;">
{% if member.email %}<a href="mailto:{{ member.email }}" class="icon-link" title="Email" aria-label="Email">{% include icon.html name="envelope" %}</a>{% endif %}
{% if member.website %}<a href="{{ member.website | relative_url }}" class="icon-link" title="Website" aria-label="Website">{% include icon.html name="house" %}</a>{% endif %}
{% if member.scholar %}<a href="{{ member.scholar }}" class="icon-link" title="Google Scholar" aria-label="Google Scholar">{% include icon.html name="google-scholar" %}</a>{% endif %}
{% if member.github %}<a href="{{ member.github }}" class="icon-link" title="GitHub" aria-label="GitHub">{% include icon.html name="github" %}</a>{% endif %}
</div>
</div>
{% endfor %}
</div>
{% endif %}

{% if site.data.alumni.size > 0 %}
## Alumni

<div class="section-card">
<table class="alumni-table">
<thead>
<tr><th>Name</th><th>Duration</th><th>Current Position</th></tr>
</thead>
<tbody>
{% for member in site.data.alumni %}
<tr>
<td>{{ member.name }}</td>
<td>{{ member.duration }}</td>
<td>{{ member.info }}</td>
</tr>
{% endfor %}
</tbody>
</table>
</div>
{% endif %}
