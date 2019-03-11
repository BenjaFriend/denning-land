---
layout: page
title: Activities
permalink: /activities/
---

This is the activities page! Here you will find a list of possible activities to do at the lakehouse. 


<div id="activities">

{% for item in site.data.activites %}

<div id="activity">
{% if item.Name %}
    <h1>{{ item.Name }}</h1>
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