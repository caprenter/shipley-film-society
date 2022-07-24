<article class="post">
  <header class="post-header">
    <h2 class="post-title">{{ film.title }}</h2>
  </header>
  <section class="post-excerpt">
    <div>
    {{ film.description | markdownify }}
    </div>
  </section>    

  

</article>
<article class="post">
  <header class="post-header">
    <h1 class="post-title">2022/23 Film Season</h1>
  </header>
  <section class="post-excerpt">
<div markdown="1">

Our season runs between September and March each year. 

{% assign dateToday = 'now' | date: "%Y-%m-%d" %}

### Upcoming Films

{% assign films = site.data.films | sort: "date" | reversed  %}
{% for film in films %}
{% if film.date > dateToday  %}
#### {{ film.name }}
{{ film.short-description }}
{{ film.date | date: "%A %d %B %Y" }}
{% if film.link %}
    [{{ film.name }} on IMDB]({{ film.link }})
{% endif %}
Doors: {{ film.doors }}  <br/>
Film Starts: {{ film.start }}  <br/>
£{{ film.price }} / £{{ film.discounted }} (unwaged)  
{% endif %}
{% endfor %}

# Get Involved
If you would like to get involved [contact]({{ '/contact' | relative_url }}) us:
</div>

</section>    

  

</article>

