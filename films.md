---
title: Films
layout: page
cover: assets/images/resources/RussianArk_1.jpg
navigation: true
---
# Upcoming Films

{% for film in site.data.filmsp %}
{% if film.date > 'now' %}
## {{ film.name }}
{{ film.description }}
{{ film.date | date: "%A %d %B %Y" }}
{% if film.link %}
[{{ film.name }} on IMDB]({{ film.link }})
{% endif %}
Doors: {{ film.doors }}
Film Starts: {{ film.start }}
£{{ film.price }} / £{{ film.discounted }} (unwaged)
{% endif %}
{% endfor %}



# Previous Films
{% assign films = site.data.filmsp | sort: "name" %}
{% for film in films %}
## {{ film.name }}
{{ film.description }}
{{ film.date | date: "%A %d %B %Y" }}
{% if film.link %}
[{{ film.name }} on IMDB]({{ film.link }})
{% endif %}
{% endfor %}