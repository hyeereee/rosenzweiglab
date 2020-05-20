---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|phd|masters|nonthesis|others|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="pos_header">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'phd' %}
<h3>PhD Students</h3>
 {% elsif role == 'masters' %}
<h3>Masters Students</h3>
 {% elsif role == 'nonthesis' %}
<h3>Non-thesis Masters Students</h3>
 {% elsif role == 'others' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
                <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
{% endif %}
  {% endfor %}
</div>
{% endif %}
  {% endfor %}

<hr>
