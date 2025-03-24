---
layout: page
permalink: /publications/
title: Publications
description:
years: [2025, 2024, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2003]
nav: true
---

<style>
.publications {
  margin-top: 4rem;
}

.publications h2.year {
  margin-top: 2rem;
  font-size: 1.5rem;
  color: #333;
  border-bottom: 1px solid #ccc;
  padding-bottom: 0.5rem;
}
</style>

<div class="publications">
  {% for y in page.years %}
    <h2 class="year">{{ y }}</h2>
    {% bibliography -f papers -q @*[year={{ y }}]* %}
  {% endfor %}
</div>
