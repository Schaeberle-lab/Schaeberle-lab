---
title: "Schäberle Lab - Team"
layout: gridlay
excerpt: "Schäberle Lab: Team members"
sitemap: false
permalink: /team/
---

# Team

**We are looking for new PhD students, Postdocs, and Master students to join the team**
[(see openings)]({{ '/vacancies/' | relative_url }}) **!**

Jump to [Group Leader](#group-leader), [Postdoctoral Researchers](#postdoctoral-researchers), [PhD Students](#phd-students), [Master Students](#master-students), [Administrative Support](#administrative-support), [Alumni](#alumni).

{% assign leader = site.data.team_members | where: "group", "pi" %}
{% assign postdocs = site.data.team_members | where: "group", "postdoc" %}
{% assign project_scientists = site.data.team_members | where: "group", "project_scientist" %}
{% assign phds = site.data.team_members | where: "group", "phd" %}
{% assign masters = site.data.team_members | where: "group", "master" %}
{% assign admin = site.data.team_members | where: "group", "admin" %}

## Group Leader

{% for member in leader %}
<div style="display:flex; gap:24px; align-items:center; border:1px solid #d9d9d9; border-radius:14px; padding:24px; margin:24px 0; background:#f8f9fb;">
  {% assign photo_path = '/images/teampic/' | append: member.photo %}
  <div style="flex:0 0 220px; text-align:center;">
    <img src="{{ photo_path | relative_url }}" alt="{{ member.name }}" style="width:220px; border-radius:12px;">
  </div>
  <div style="flex:1;">
    <h3 style="margin-top:0;">{{ member.name }}</h3>
    <p><strong>{{ member.info }}</strong></p>
    {% if member.description %}<p>{{ member.description }}</p>{% endif %}
    {% if member.email != "" %}<p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}

    {% if member.number_educ >= 1 %}<p>{{ member.education1 }}</p>{% endif %}
    {% if member.number_educ >= 2 %}<p>{{ member.education2 }}</p>{% endif %}
    {% if member.number_educ >= 3 %}<p>{{ member.education3 }}</p>{% endif %}
    {% if member.number_educ >= 4 %}<p>{{ member.education4 }}</p>{% endif %}
    {% if member.number_educ >= 5 %}<p>{{ member.education5 }}</p>{% endif %}
  </div>
</div>
{% endfor %}

## Postdoctoral Researchers

{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div style="border:1px solid #e1e1e1; border-radius:12px; padding:18px; margin-bottom:20px;">
  <img src="{{ photo_path | relative_url }}" alt="{{ member.name }}" style="width:220px; border-radius:10px; display:block; margin-bottom:12px;">
  <h4>{{ member.name }}</h4>
  <p><strong>{{ member.info }}</strong></p>
  {% if member.description %}<p>{{ member.description }}</p>{% endif %}
  {% if member.email != "" %}<p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>

## PhD Students

{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div style="border:1px solid #e1e1e1; border-radius:12px; padding:18px; margin-bottom:20px;">
  <img src="{{ photo_path | relative_url }}" alt="{{ member.name }}" style="width:220px; border-radius:10px; display:block; margin-bottom:12px;">
  <h4>{{ member.name }}</h4>
  <p><strong>{{ member.info }}</strong></p>
  {% if member.description %}<p>{{ member.description }}</p>{% endif %}
  {% if member.email != "" %}<p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>

## Master Students

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(260px, 1fr)); gap:24px; margin:24px 0;">
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div style="border:1px solid #e1e1e1; border-radius:12px; padding:18px; margin-bottom:20px;">
  <img src="{{ photo_path | relative_url }}" alt="{{ member.name }}" style="width:220px; border-radius:10px; display:block; margin-bottom:12px;">
  <h4>{{ member.name }}</h4>
  <p><strong>{{ member.info }}</strong></p>
  {% if member.description %}<p>{{ member.description }}</p>{% endif %}
  {% if member.email != "" %}<p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>

## Administrative Support

{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div style="border:1px solid #e1e1e1; border-radius:12px; padding:18px; margin-bottom:20px;">
  <img src="{{ photo_path | relative_url }}" alt="{{ member.name }}" style="width:220px; border-radius:10px; display:block; margin-bottom:12px;">
  <h4>{{ member.name }}</h4>
  <p><strong>{{ member.info }}</strong></p>
  {% if member.description %}<p>{{ member.description }}</p>{% endif %}
  {% if member.email != "" %}<p><a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>

## Alumni

{% for member in site.data.alumni_members %}
### {{ member.name }}

{{ member.duration }}  
Role: {{ member.info }}

{% if member.number_educ >= 1 %}
  * {{ member.education1 | markdownify }}
{% endif %}
{% if member.number_educ >= 2 %}
  * {{ member.education2 | markdownify }}
{% endif %}
{% if member.number_educ >= 3 %}
  * {{ member.education3 | markdownify }}
{% endif %}
{% if member.number_educ >= 4 %}
  * {{ member.education4 | markdownify }}
{% endif %}
{% if member.number_educ >= 5 %}
  * {{ member.education5 | markdownify }}
{% endif %}

{% if member.email != "" %}
Email: <a href="mailto:{{ member.email }}">{{ member.email }}</a>
{% endif %}

{% endfor %}
