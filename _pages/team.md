---
title: "Schäberle Lab - Team"
layout: gridlay
excerpt: "Schäberle Lab: Team members"
sitemap: false
permalink: /team/
---

<style>
.team-lead {
  display: grid;
  grid-template-columns: minmax(220px, 280px) 1fr;
  gap: 28px;
  align-items: start;
  border: 1px solid #d9d9d9;
  border-radius: 18px;
  padding: 28px;
  margin: 24px 0 36px 0;
  background: #f8f9fb;
}
.team-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
  gap: 24px;
  margin: 18px 0 36px 0;
}
.team-card {
  border: 1px solid #e3e3e3;
  border-radius: 16px;
  padding: 18px;
  background: #fff;
  height: 100%;
}
.team-photo {
  width: 100%;
  max-width: 240px;
  aspect-ratio: 1 / 1;
  object-fit: cover;
  border-radius: 14px;
  display: block;
  margin: 0 auto 16px auto;
}
.team-lead .team-photo {
  max-width: 260px;
  margin: 0;
}
.team-role {
  font-weight: 700;
  margin-bottom: 8px;
}
.team-meta {
  font-size: 0.95em;
  color: #555;
  margin-bottom: 10px;
}
.team-project {
  font-size: 0.95em;
  margin: 10px 0;
}
.team-edu {
  margin: 10px 0 0 18px;
}
.team-papers {
  margin: 10px 0 0 18px;
}
.team-jump {
  margin: 14px 0 26px 0;
}
.team-jump a {
  white-space: nowrap;
}
.alumni-columns {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 28px;
  margin: 20px 0 30px 0;
}
.alumni-column {
  border: 1px solid #e3e3e3;
  border-radius: 16px;
  padding: 20px;
  background: #fff;
}
.alumni-column h3 {
  margin-top: 0;
  margin-bottom: 18px;
}
.alumni-entry {
  margin-bottom: 18px;
  padding-bottom: 14px;
  border-bottom: 1px solid #efefef;
}
.alumni-entry:last-child {
  margin-bottom: 0;
  padding-bottom: 0;
  border-bottom: none;
}
.alumni-name {
  font-weight: 700;
}
.alumni-role {
  font-weight: 600;
}
.alumni-years {
  color: #555;
  font-size: 0.95em;
}
.alumni-where {
  margin-top: 4px;
  font-size: 0.95em;
}
@media (max-width: 1100px) {
  .alumni-columns {
    grid-template-columns: 1fr;
  }
}
@media (max-width: 780px) {
  .team-lead {
    grid-template-columns: 1fr;
  }
  .team-lead .team-photo {
    margin: 0 auto 16px auto;
  }
}
</style>

{% assign pi_members = site.data.team_members | where: "group", "PI" %}
{% assign postdocs = site.data.team_members | where: "group", "postdoc" %}
{% assign project_scientists = site.data.team_members | where: "group", "project_scientist" %}
{% assign phds = site.data.team_members | where: "group", "phd" %}
{% assign masters = site.data.team_members | where: "group", "master" %}
{% assign admin = site.data.team_members | where: "group", "admin" %}

{% assign alumni_phd_postdoc = site.data.alumni | where: "column", "phd_postdoc" %}
{% assign alumni_visiting = site.data.alumni | where: "column", "visiting" %}
{% assign alumni_master = site.data.alumni | where: "column", "master" %}

# Team

**We are looking for new PhD students, Postdocs, and Master students to join the team**  
[(see openings)]({{ '/vacancies/' | relative_url }})

<div class="team-jump">
Jump to
<a href="#group-leader">Group Leader</a>,
<a href="#postdoctoral-researchers">Postdoctoral Researchers</a>,
<a href="#project-scientists">Project Scientists</a>,
<a href="#phd-students">PhD Students</a>,
<a href="#master-students">Master Students</a>,
<a href="#administration">Administration</a>,
<a href="#alumni">Alumni</a>.
</div>

## Group Leader

{% for member in pi_members %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-lead">
<div>
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
</div>
<div>
<h3 style="margin-top:0;">{{ member.name }}</h3>
<div class="team-role">{{ member.info }}</div>

{% if member.description %}
<p>{{ member.description }}</p>
{% endif %}

{% if member.project_title %}
<p class="team-project"><strong>Research focus:</strong> {{ member.project_title }}</p>
{% endif %}

{% if member.email != "" %}
<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
{% endif %}

{% if member.number_educ and member.number_educ > 0 %}
<strong>Position / background</strong>
<ul class="team-edu">
{% if member.number_educ >= 1 %}<li>{{ member.education1 }}</li>{% endif %}
{% if member.number_educ >= 2 %}<li>{{ member.education2 }}</li>{% endif %}
{% if member.number_educ >= 3 %}<li>{{ member.education3 }}</li>{% endif %}
{% if member.number_educ >= 4 %}<li>{{ member.education4 }}</li>{% endif %}
{% if member.number_educ >= 5 %}<li>{{ member.education5 }}</li>{% endif %}
</ul>
{% endif %}
</div>
</div>
{% endfor %}

## Postdoctoral Researchers

<div class="team-grid">
{% for member in postdocs %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-card">
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
<h4>{{ member.name }}</h4>
<div class="team-role">{{ member.info }}</div>
{% if member.joined %}<div class="team-meta"><strong>Joined:</strong> {{ member.joined }}</div>{% endif %}
{% if member.description %}<p>{{ member.description }}</p>{% endif %}
{% if member.project_title %}<p class="team-project"><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
{% if member.role_in_group %}<p><strong>Role in group:</strong> {{ member.role_in_group }}</p>{% endif %}
{% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>
{% endfor %}
</div>

## Project Scientists

<div class="team-grid">
{% for member in project_scientists %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-card">
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
<h4>{{ member.name }}</h4>
<div class="team-role">{{ member.info }}</div>
{% if member.joined %}<div class="team-meta"><strong>Joined:</strong> {{ member.joined }}</div>{% endif %}
{% if member.description %}<p>{{ member.description }}</p>{% endif %}
{% if member.project_title %}<p class="team-project"><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
{% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>
{% endfor %}
</div>

## PhD Students

<div class="team-grid">
{% for member in phds %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-card">
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
<h4>{{ member.name }}</h4>
<div class="team-role">{{ member.info }}</div>
{% if member.joined %}<div class="team-meta"><strong>Joined:</strong> {{ member.joined }}</div>{% endif %}
{% if member.description %}<p>{{ member.description }}</p>{% endif %}
{% if member.project_title %}<p class="team-project"><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
{% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
{% if member.papers and member.papers.size > 0 %}
<strong>Selected papers</strong>
<ul class="team-papers">
{% for paper in member.papers %}
<li>{{ paper }}</li>
{% endfor %}
</ul>
{% endif %}
</div>
{% endfor %}
</div>

## Master Students

<div class="team-grid">
{% for member in masters %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-card">
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
<h4>{{ member.name }}</h4>
<div class="team-role">{{ member.info }}</div>
{% if member.project_title %}<p class="team-project"><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
{% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>
{% endfor %}
</div>

## Administration

<div class="team-grid">
{% for member in admin %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="team-card">
{% if member.photo %}
<img class="team-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
{% endif %}
<h4>{{ member.name }}</h4>
<div class="team-role">{{ member.info }}</div>
{% if member.description %}<p>{{ member.description }}</p>{% endif %}
{% if member.project_title %}<p class="team-project"><strong>Role:</strong> {{ member.project_title }}</p>{% endif %}
{% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
</div>
{% endfor %}
</div>

## Alumni

<div class="alumni-columns">
<div class="alumni-column">
<h3>PhD Graduates, Postdocs & Fraunhofer PhDs</h3>
{% for member in alumni_phd_postdoc %}
<div class="alumni-entry">
<div class="alumni-name">{{ member.name }}</div>
{% if member.position %}<div class="alumni-role">{{ member.position }}</div>{% endif %}
{% if member.years != "" %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
{% if member.whereabouts != "" %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
</div>
{% endfor %}
</div>

<div class="alumni-column">
<h3>Visiting Scientists, Fellows & Internships</h3>
{% for member in alumni_visiting %}
<div class="alumni-entry">
<div class="alumni-name">{{ member.name }}</div>
{% if member.position %}<div class="alumni-role">{{ member.position }}</div>{% endif %}
{% if member.years != "" %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
{% if member.whereabouts != "" %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
</div>
{% endfor %}
</div>

<div class="alumni-column">
<h3>Master Students & Hiwi</h3>
{% for member in alumni_master %}
<div class="alumni-entry">
<div class="alumni-name">{{ member.name }}</div>
{% if member.position %}<div class="alumni-role">{{ member.position }}</div>{% endif %}
{% if member.years != "" %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
{% if member.whereabouts != "" %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
</div>
{% endfor %}
</div>
</div>
