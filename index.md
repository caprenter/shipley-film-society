---
layout: default
title: Shipley Film Society
class: 'home-template'
navigation: True
logo: /assets/images/favicon_large.png
current: home
#Use 'our_id' below for the next film to be shown. The id is in the csv file
# we use {% assign film = site.data.films | where:"our-id", page.our-id | first  %}
# in _includes/head.html to make use of the data below using e.g. film.image
our-id: "smoke" 
# Defaults to use if no 'next film'
cover: /assets/images/resources/nightonearth.jpg

---
<!-- < default -->
<!-- The tag above means - insert everything in this file into the [body] of the default.hbs template -->

<!-- The big featured header  -->
<header class="main-header {% if film.image %}" style="background-image: radial-gradient(rgb(0,0,0,0.6),rgb(0,0,0,0)), url({{ site.baseurl }}/assets/images/{{ film.image }} {% elsif page.cover %}" style="background-image: radial-gradient(rgb(0,0,0,0.6),rgb(0,0,0,0)), url({{ site.baseurl }}{{ page.cover }}) {% else %}no-cover{% endif %}">
    
    <div class="vertical">
        <div class="main-header-content inner">
            <h2 class="page-title">Our Next Film</h2>


            <!-- TODO: This film listing format could be turned into an include-->
<div class="next-film" markdown="1">
# {{ film.name }}
{{ film.date | date: "%A %d %B %Y" | markdownify }}{:class="page-description"}
{{ film.short-description | markdownify }}{:class="page-description"}
<p class="page-description">
    at The Kirkgate Centre, Shipley<br>
    Certificate: {{ film.certificate }}<br>
    Doors: {{ film.doors | date: "%l:%M%P" }}<br>
    Film Starts: {{ film.start | date: "%l:%M%P" }}<br>
    £{{ film.price }} / £{{ film.discounted }} (unwaged)
</p>
</div>
        </div>
    </div>
    <a class="scroll-down icon-arrow-left" href="#content" data-offset="-45"><span class="hidden">Scroll Down</span></a>
    
</header>

<!-- The main content area on the homepage -->
<main id="content" class="content" role="main" markdown="1">
{% include main.md %}
</main>
