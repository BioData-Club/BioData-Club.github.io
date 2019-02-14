---
title: People
layout: splash
permalink: /people/
people:
  - title: "People"
    excerpt: "BioData Club consists of many staff, faculty, postdocs and students from many programs and departments across OHSU."
---
{% include feature_row %}

{% include feature_row id= "people" type = "center" %}

{% assign sorted_people = site.people | sort: 'last_name' %}
{% assign depts = "DMICE, CLSU, BME, Biostatistics, CompBio" | split: ", " %}
{% assign tags = "systems-biology, sleep-studies, interactive-visualization" | split: ", " %}

Filter by Group:

<div class="button-group filter-button-group">
	<a class="button active btn btn--info" data-filter="*">All</a>
	{% for tag in depts %}
		<a class="button btn btn--info" data-filter=".{{ tag }}">{{ tag }}</a>
	{% endfor %}
</div>

Filter by research interest:

<div class="button-group filter-button-group">
	<a class="button active btn btn--info" data-filter="*">All</a>
	{% for tag in tags %}
		<a class="button btn btn--info" data-filter=".{{ tag }}">{{ tag }}</a>
	{% endfor %}
</div>

<div class="grid__wrapper">
	{% for person in sorted_people %}
    {% include people.html type="grid" %}
  {% endfor %}
</div>

<script src="https://code.jquery.com/jquery-3.1.0.min.js" integrity="sha256-cCueBR6CsyA4/9szpPfrX3s49M9vUU5BgtiJj06wt/s=" crossorigin="anonymous"></script>
<script src="https://unpkg.com/isotope-layout@3.0/dist/isotope.pkgd.js"></script>
<script>
	// init Isotope
	var $grid = $('.grid__wrapper').isotope({
    layoutMode : 'masonry'
	  // options
	});
	// filter items on button click
	$('.filter-button-group').on( 'click', 'a', function() {
	  var filterValue = $(this).attr('data-filter');
	  $grid.isotope({ filter: filterValue });
	});
	$('.button-group a.button').on('click', function(){
		$('.button-group a.button').removeClass('active');
		$(this).addClass('active');
	});
</script>

<style type="text/css">
	a.button.active {
		background: #F76B48;
		border: 1px solid #F76B48;
		color: #fff;
	}

  .grid-item {
  float: left;
  background: #e6e5e4;
  border: 3px solid #b6b5b4;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2); /* this adds the "card" effect */
  padding: 16px;
  font-size: small;
  text-align: center;
  background-color: #f1f1f1;
}

.grid-item--width2 { width: 100px; }
.grid-item--height2 { height: 100px; }
</style>