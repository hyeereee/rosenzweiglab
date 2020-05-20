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

<div class="container pos_header">
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
{% endif %}
</div>

{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{site.baseurl}}/images/people/{{profile.avatar}}"></a>
          {% else %}
            <br><br>
          {% endif %}    
    {% endif %}
  {% endfor %}
</div>

{% else %}
<br>

| Name | Position | Where they went |
| :------------- |:--------------| :-------------|
| Antone Nour | Masters Student (2018 - 2020) | - |
| Elie Akoury | Postdoc (2020) | - |
| Sofia Garcia-Luna | Visiting Scholar (2018) | - |



{% endif %}
{% endfor %}
