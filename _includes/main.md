<!--<article class="post">
  <header class="post-header">
    <h2 class="post-title">{{ film.film-title }}</h2>
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
    <h1 class="post-title">Coming soon..</h1>
  </header>
  <section class="main-page">
<div markdown="1">

Shipley Film Society has shown films at the [Kirkgate Centre](http://www.kirkgatecentre.org.uk/) in the winter months (because it's too light to show films in the summer) for the past 13 years or so.

With the centre closing for a refurbishment soon, our 2023 - 2024 season is both up in the air and open to suggestions.

If you'd like to be involved, or have ideas to share, please [get in touch]({% link contact.md %}) and [sign up for our newsletter](https://shipleyfilmsociety.us4.list-manage.com/subscribe?u=866985097deeb0313d3c363a7&id=ae720000b9).



### Our 2022 - 23 Film Season is over
Our season kicked off on Friday September 23rd 2022, and ended with our final film on the 28th April 2023.

In reverse order we showed:
* [Riders of Justice]({% link _films/riders_of_justice.md %})
* [Le Doulos]({% link _films/ledoulos.md %})
* [Cold War]({% link _films/cold_war.md %})
* [9 to 5]({% link _films/nine_to_five.md %})
* [Lucky]({% link _films/lucky.md %})
* [8 Women]({% link _films/8-women.md %})
* [Smoke]({% link _films/smoke.md %})
* [Night On Earth]({% link _films/night_on_earth.md %})


This season marked our return after the covid cancellations of recent years.

We  brought back a couple of films that had to be cancelled during the pandemic, and our volunteers selected a bunch of other great films for our audience to discover, revisit, and enjoy.

<!--Films are shown on the 4th Friday of the month.-->

{% assign dateToday = 'now' | date: "%Y-%m-%d" %}

<!--### Upcoming Films

{% assign films = site.data.films | sort: "screening-date" | reversed  %}
{% for film in films %}
{% if film.screening-date > dateToday  %}
<div class="post-content film-item" markdown="1">
{% include upcoming-film.md %}
</div>
{% endif %}
{% endfor %}-->

{% capture get-involved %}{% include get-involved.md %}{% endcapture %}
{{ get-involved | markdownify }}
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
