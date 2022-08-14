---
title: Films
layout: page
cover: assets/images/resources/RussianArk_1.jpg
image-credit: Russian Ark
navigation: true
---

{% assign dateToday = 'now' | date: "%Y-%m-%d" %}

# Upcoming Films

{% assign films = site.data.films | sort: "date" | reversed  %}
{% for film in films %}
{% if film.date > dateToday  %}
<div class="film-item" markdown="1">
{% include upcoming-film.md %}
</div>
{% endif %}
{% endfor %}


<div id="past-films" markdown="1">
# Previous Films
{% assign films = site.data.films | sort: "name" %}
{% for film in films %}
{% if film.date < dateToday  %}
<div class="film-item" markdown="1">
## {{ film.name }}
{{ film.date | date: "%A %d %B %Y" }}
{:class="film-date"}
{% if film.image %}
![{{ film.name }}](/assets/images/{{ film.image }}){:class="img-responsive"}
{% endif %}
{% if film.link %}
[{{ film.name }} on IMDB]({{ film.link }})
{% endif %}
</div>
{% endif %}

{% endfor %}
</div>