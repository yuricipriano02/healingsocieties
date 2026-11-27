---
title: "Home"
layout: homelay
permalink: /
---

<section class="editorial-hero">
  <div class="editorial-hero-copy">
    <p class="editorial-kicker">Intergroup relations · Social change</p>
    <h1 class="home-hero">Healing<br>Societies</h1>
    <p class="home-hero-sub">{{ site.title }} at {{ site.institution }}</p>
    <a class="editorial-button" href="{{ '/projects' | relative_url }}">Explore our research <span aria-hidden="true">→</span></a>
  </div>
  <div class="hero-animation" aria-hidden="true">
    <svg class="hero-weave" viewBox="0 0 1000 460" fill="none" xmlns="http://www.w3.org/2000/svg">
      <g class="network-back">
        <path d="M5 210 C150 25 280 30 420 205 S700 405 995 130"/>
        <path d="M0 250 C155 420 290 410 430 235 S730 15 1000 300"/>
        <path d="M0 170 C180 90 300 110 460 225 S760 360 1000 190"/>
        <path d="M0 300 C190 180 300 170 470 250 S770 300 1000 80"/>
        <path d="M70 70 C220 230 310 300 500 210 S770 50 940 390"/>
        <path d="M30 390 C200 260 320 90 510 180 S790 430 970 250"/>
        <path d="M0 115 C220 20 330 75 500 220 S760 370 1000 340"/>
        <path d="M0 345 C200 430 320 350 500 215 S790 40 1000 115"/>
      </g>
      <g class="network-front">
        <path d="M0 225 C170 110 290 105 455 220 S740 340 1000 205"/>
        <path d="M0 275 C170 360 310 340 470 220 S760 95 1000 255"/>
        <path d="M95 30 C250 150 320 310 500 225 S780 75 920 420"/>
        <path d="M30 420 C220 290 330 110 520 215 S780 370 980 30"/>
      </g>
      <g class="network-nodes">
        <circle cx="92" cy="210" r="5"/><circle cx="210" cy="118" r="4"/><circle cx="330" cy="165" r="6"/>
        <circle cx="455" cy="220" r="11"/><circle cx="590" cy="300" r="5"/><circle cx="710" cy="160" r="7"/>
        <circle cx="835" cy="110" r="4"/><circle cx="930" cy="250" r="6"/><circle cx="790" cy="360" r="4"/>
        <circle cx="260" cy="335" r="4"/><circle cx="570" cy="90" r="4"/><circle cx="675" cy="390" r="5"/>
      </g>
    </svg>
  </div>
</section>

<section class="editorial-research" aria-labelledby="research-heading">
  <div class="editorial-section-heading">
    <div>
      <p class="editorial-kicker"><span></span> Research areas</p>
      <h2 id="research-heading">Understanding the forces that divide — and connect — societies</h2>
    </div>
    <p>Our research aims to understand the psychological processes and mechanisms of improving intergroup relations in societies affected or threatened by conflict. Using experimental methods across different social contexts, we study attitudes and emotions in order to develop effective intergroup interventions that promote positive social change.</p>
  </div>
  <div class="research-topics">
    <a href="{{ '/projects' | relative_url }}">Social Psychology <span>↗</span></a>
    <a href="{{ '/projects' | relative_url }}">Conflict and Reconciliation <span>↗</span></a>
    <a href="{{ '/projects' | relative_url }}">Interventions <span>↗</span></a>
    <a href="{{ '/projects' | relative_url }}">Group Dynamics <span>↗</span></a>
    <a href="{{ '/projects' | relative_url }}">Intergroup Relations <span>↗</span></a>
    <a href="{{ '/projects' | relative_url }}">Social Identity <span>↗</span></a>
  </div>
</section>

<section class="editorial-about" id="about" aria-labelledby="about-heading">
  <a class="editorial-about-image" href="{{ '/team' | relative_url }}">
    <img src="{{ site.photo | prepend: '/images/' | relative_url }}" alt="{{ site.card_name }}" loading="lazy">
  </a>
  <div class="editorial-about-copy">
    <p class="editorial-kicker"><span></span> About the group</p>
    <h2 id="about-heading">Research for more peaceful and inclusive societies</h2>
    <p>{{ site.name }} is the {{ site.title }} at {{ site.institution }}. Led by {{ site.card_name }}, our group investigates how social context shapes intergroup relations, reconciliation and opportunities for positive social change.</p>
    <p class="editorial-address"><strong>Department of Psychology — Campus Albano</strong><br>Albanovägen 12, House 4, 114 19 Stockholm, Sweden</p>
    <a class="editorial-text-link" href="{{ '/team' | relative_url }}">Meet the team <span>→</span></a>
  </div>
</section>

<section class="editorial-news" aria-labelledby="news-heading">
  <div class="editorial-news-title">
    <p class="editorial-kicker"><span></span> News</p>
    <h2 id="news-heading">Updates from our research community</h2>
    <a class="editorial-text-link" href="{{ '/allnews.html' | relative_url }}">All news <span>→</span></a>
  </div>
  <div class="editorial-news-list">
    {% for article in site.data.news limit:5 %}
    <article class="editorial-news-item">
      <time>{{ article.date }}</time>
      <p>{{ article.headline }}</p>
    </article>
    {% endfor %}
    {% unless site.data.news.size > 0 %}
    <p>News and updates from the group will appear here.</p>
    {% endunless %}
  </div>
</section>

{% capture selected %}{% bibliography --query @*[selected=true] %}{% endcapture %}
{% if selected contains "pub-entry" %}
<section class="editorial-publications">
  <div>
    <p class="editorial-kicker"><span></span> Selected publications</p>
    <h2>Research and scholarship</h2>
  </div>
  <div class="editorial-publications-list">
    {{ selected }}
    <a class="editorial-text-link" href="{{ '/publications' | relative_url }}">All publications <span>→</span></a>
  </div>
</section>
{% endif %}
