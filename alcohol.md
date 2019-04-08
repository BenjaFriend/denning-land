---
layout: page
title: Alcohol
permalink: /alcohol/
---

<p>A short list of what breweries, wineries, and distilleries are in the area</p>

<div id="alcohol">

{% for item in site.data.alcohol %}

<div id="place">
{% if item.Name %}
    <h2>{{ item.Name }}</h2>
{% endif %}

{% if item.Hours %}
    <h3>Hours: {{ item.Hours }}</h3>
{% endif %}

{% if item.Cost %}
    <p>Cost ($-$$$): <strong>{{ item.Cost }}</strong></p>
{% endif %}

{% if item.Distance and item.MapLink %}
    <a href=" {{ item.MapLink }} " target="blank" ><p>Distance: {{ item.Distance }}</p></a>
{% endif %}

{% if item.Description %}
    <p id="activity_desc"><i>{{ item.Description }}</i></p>
{% endif %}

{% if item.Website %}
    <a href="{{ item.Website }}" target="blank">For more info, click here</a>
{% endif %}

</div>

{% endfor %}

</div>
