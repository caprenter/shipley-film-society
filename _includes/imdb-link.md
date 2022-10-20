{% if page.imdb-link %}
  <div>
  {% if page.film-title %}<a href="{{ page.imdb-link }}">{{ page.film-title }} at IMDB</a>
  {% else %}<a href="{{ page.imdb-link }}">IMDB page</a>
  {% endif %}
  </div>
{% endif %}
