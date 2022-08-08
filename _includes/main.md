<!--<article class="post">
  <header class="post-header">
    <h2 class="post-title">{{ film.name }}</h2>
  </header>
  <section class="post-excerpt">
    <div>
    {{ film.description | markdownify }}
    </div>
  </section>    
</article>-->

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
<div class="post-content film-item" markdown="1">
{% include upcoming-film.md %}
</div>
{% endif %}
{% endfor %}

# Get Involved
If you would like to get involved [contact]({{ '/contact' | relative_url }}) us:
</div>

</section>    

  

</article>

