---
title: "Ní Leathlobhair Lab"
layout: homelay
excerpt: "Evolutionary genomics research at the Smurfit Institute of Genetics, Trinity College Dublin"
permalink: /
---
<div class="lab-home">
  <section class="lab-hero" aria-label="Introduction">
    <div class="lab-hero-media">
      <!-- Original three-slide carousel retained. Change the first slide once you have an approved microscopy image. -->
      <div id="carousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-pause="hover">
        <ol class="carousel-indicators">
          <li data-target="#carousel" data-slide-to="0" class="active"></li>
          <li data-target="#carousel" data-slide-to="1"></li>
          <li data-target="#carousel" data-slide-to="2"></li>
        </ol>
        <div class="carousel-inner">
          <div class="item active"><img src="{{ '/images/slider7001400/tcd-campus.jpg' | relative_url }}" alt="Trinity College Dublin campus" /></div>
          <div class="item"><img src="{{ '/images/slider7001400/lab1.png' | relative_url }}" alt="Ní Leathlobhair Lab group photograph" /></div>
          <div class="item"><img src="{{ '/images/slider7001400/smurfit-building.jpg' | relative_url }}" alt="Smurfit Institute of Genetics" /></div>
        </div>
        <a class="left carousel-control" href="#carousel" role="button" data-slide="prev"><span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span><span class="sr-only">Previous</span></a>
        <a class="right carousel-control" href="#carousel" role="button" data-slide="next"><span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span><span class="sr-only">Next</span></a>
      </div>
    </div>
    <div class="lab-hero-intro">
      <h1>Evolutionary genomics</h1>
      <p>We are a multidisciplinary research group based in the <strong>Smurfit Institute of Genetics</strong> at <strong>Trinity College Dublin</strong>.</p>
      <p>We study how genomes evolve, with a particular focus on the origins and consequences of ploidy change in cancer, the developmental history of tumours, and evolutionary variation across genomes.</p>
    </div>
  </section>

  <section class="lab-home-lower" aria-label="Research and news">
    <div class="lab-home-questions">
      <h2>Current questions</h2>
      <p>What processes determine the spectrum of ploidy changes observed across human cancers, and how do these changes influence tumour evolution and clinical outcome?</p>
      <p>What can the genomes of testicular germ cell and trophoblastic tumours reveal about the relationship between development and cancer?</p>
      <p>We are also interested in the evolution of endogenous viral elements and, separately, the evolutionary history of histone mRNA processing across eukaryotes.</p>
    </div>
    <aside class="lab-home-news">
      <h2>News</h2>
      {% for article in site.data.news limit:3 %}
      <div class="lab-news-entry"><span class="lab-news-date">{{ article.date }}</span><div>{{ article.headline | markdownify }}</div></div>
      {% endfor %}
      <a class="lab-news-all" href="{{ '/allnews.html' | relative_url }}">All news</a>
    </aside>
  </section>

  <!-- To display funder logos, add approved organisations to _data/funders.yml. -->
  {% if site.data.funders and site.data.funders.size > 0 %}
  <section class="lab-funders" aria-label="Funding and support">
    <h2>Funding and support</h2>
    <div class="lab-funder-logos">
      {% for funder in site.data.funders %}
      <a href="{{ funder.url }}" target="_blank" rel="noopener noreferrer"><img src="{{ funder.logo | relative_url }}" alt="{{ funder.name | escape }}" loading="lazy"></a>
      {% endfor %}
    </div>
  </section>
  {% endif %}
</div>
