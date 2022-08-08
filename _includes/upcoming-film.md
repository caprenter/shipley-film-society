#### {{ film.name }}
*{{ film.date | date: "%A %d %B %Y" }}*
{% if film.image %}
![{{ film.name }}](/assets/images/{{ film.image }}){:class="img-responsive"}
{% endif %}
{{ film.short-description }}


{% if film.link %}
[{{ film.name }} on IMDB]({{ film.link }})
{% endif %}
{% if film.doors %}
Doors: {{ film.doors | date: "%l:%M%P" }}  <br/>
{% endif %}
{% if film.start %}
Film Starts: {{ film.start | date: "%l:%M%P" }}  <br/>
{% endif %}
{% if film.price %}
£{{ film.price }} / £{{ film.discounted }} (unwaged)  
{% endif %}
