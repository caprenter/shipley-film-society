---
title: Films
layout: page
cover: resources/RussianArk_1.jpg #no leading slash
image-credit: Russian Ark
navigation: true
---

{% assign dateToday = 'now' | date: "%Y-%m-%d" %}

<!--# Upcoming Films-->

{% assign films = site.data.films | sort: "screening-date" | reversed  %}
{% for film in films %}
{% if film.screening-date > dateToday  %}
<div class="film-item" markdown="1">
{% include upcoming-film.md %}
</div>
{% endif %}
{% endfor %}


<div id="past-films" markdown="1">
# Previous Films
{% assign films = site.data.films | sort: "film-title" %}
{% for film in films %}
{% if film.screening-date < dateToday  %}
<div class="film-item" markdown="1">
## [{{ film.film-title }}]({{ site.url }}/films/{{ film.our-id }})
{{ film.screening-date | date: "%A %d %B %Y" }}
{:class="film-date"}
{% if film.main-image %}
![{{ film.film-title }}](/assets/images/{{ film.main-image }}){:class="img-responsive"}
{% endif %}
</div>
{% endif %}

{% endfor %}
</div>
