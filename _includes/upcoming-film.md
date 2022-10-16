#### [{{ film.film-title }}]({{ site.url }}/films/{{ film.our-id }})
{{ film.screening-date | date: "%A %d %B %Y" }}
{:class="film-date"}
{% if film.main-image %}
![{{ film.film-title }}](/assets/images/{{ film.main-image }}){:class="img-responsive"}
{% endif %}
{{ film.short-description }}<br/>
{% if film.imdb-link %}[{{ film.film-title }} on IMDB]({{ film.imdb-link }}){% endif %}

{% if film.doors %}Doors: {{ film.doors | date: "%l:%M%P" }} <br/>{% endif %}
{% if film.start %}Film Starts: {{ film.start | date: "%l:%M%P" }} <br/>{% endif %}
{% if film.price %}£{{ film.price }} / £{{ film.discounted }} (unwaged)  {% endif %}
