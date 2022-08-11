<!--<article class="post">
  <header class="post-header">
    <h2 class="post-title">{{ film.name }}</h2>
  </header>
  <section class="post-excerpt">
    <div>
    {{ film.description | markdownify }}
    </div>
  </section>    
</article>

-->


<article class="post"> <!-- centres the content in the page -->
  <header class="post-header">
    <h1 class="post-title">Our 2022-23 Film Season</h1>
  </header>
  <section class="main-page">
<div markdown="1">

Our season kicks off on Friday September 23rd 2022 and runs through until our final film on the 24th March 2023.

This season marks our return after the covid cancellations of recent years. 

We've brought back a couple of films that had to be cancelled during the pandemic, and our volunteers have selected a bunch of great films for you to discover, revist, and enjoy.

Films are shown on the 4th Friday of the month.

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

<article class="post">
  <header class="post-header">
    <h2 class="post-title">About your visit</h2>
  </header>
  <section class="main-page">
<div>
{% capture bar-info %}{% include bar-info.md %}{% endcapture %}
{{ bar-info | markdownify }}
{% capture comfort %}{% include comfort.md %}{% endcapture %}
{{ comfort | markdownify }}
{% capture foodbank %}{% include foodbank.md %}{% endcapture %}
{{ foodbank | markdownify }}
{% capture venue %}{% include venue.md %}{% endcapture %}
{{ venue | markdownify }}
    </div>
  </section>    
</article>