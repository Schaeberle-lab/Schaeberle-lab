---
title: "Schäberle Lab - Team"
layout: gridlay
excerpt: "Schäberle Lab: Team members"
sitemap: false
permalink: /team/
---

<style>
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
}
.team-photo {
  width: 100%;
  max-width: 220px;
  aspect-ratio: 1 / 1;
  object-fit: cover;
  border-radius: 12px;
  display: block;
  margin: 0 auto 14px auto;
}
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
.team-lead .team-photo {
  max-width: 260px;
  margin: 0;
}
.team-role {
  font-weight: 700;
  margin-bottom: 8px;
}
.team-meta {
  color: #666;
  font-size: 0.95em;
  margin-bottom: 8px;
}
.alumni-columns {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 24px;
  margin: 18px 0 36px 0;
}
.alumni-column {
  border: 1px solid #e3e3e3;
  border-radius: 16px;
  padding: 18px;
  background: #fff;
}
.alumni-entry {
  margin-bottom: 16px;
  padding-bottom: 12px;
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
  color: #666;
  font-size: 0.95em;
}
.alumni-where {
  margin-top: 4px;
  font-size: 0.95em;
}
@media (max-width:1100px){
  .alumni-columns { grid-template-columns:1fr; }
}
@media (max-width:780px){
  .team-lead { grid-template-columns:1fr; }
  .team-lead .team-photo { margin:0 auto 16px auto; }
}
.member-row {
  display: grid;
  grid-template-columns: 180px 1fr;
  gap: 22px;
  align-items: start;
  margin: 18px 0 28px 0;
}

.member-photo {
  width: 180px;
  height: 220px;
  object-fit: cover;
  border-radius: 12px;
  display: block;
}

.member-info h4 {
  margin-top: 0;
  margin-bottom: 8px;
}

@media (max-width: 780px) {
  .member-row {
    grid-template-columns: 1fr;
  }

  .member-photo {
    margin: 0 auto 14px auto;
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
    {% if member.description %}<p>{{ member.description }}</p>{% endif %}
    {% if member.project_title %}<p><strong>Research focus:</strong> {{ member.project_title }}</p>{% endif %}
    {% if member.email != "" %}<p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>{% endif %}
  </div>
</div>
{% endfor %}

## Postdoctoral Researchers
{% for member in postdocs %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="member-row">
  <div>
    {% if member.photo %}
    <img class="member-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
    {% endif %}
  </div>

  <div class="member-info">
    <h4>{{ member.name }}</h4>

    <div class="team-role">{{ member.info }}</div>

    {% if member.joined %}
    <div class="team-meta"><strong>Joined:</strong> {{ member.joined }}</div>
    {% endif %}

    {% if member.description %}
    <p>{{ member.description }}</p>
    {% endif %}

    {% if member.project_title %}
    <p><strong>Project:</strong> {{ member.project_title }}</p>
    {% endif %}

    {% if member.role_in_group %}
    <p><strong>Role in group:</strong> {{ member.role_in_group }}</p>
    {% endif %}

    {% if member.number_educ and member.number_educ > 0 %}
    <p><strong>Education</strong></p>
    <ul>
      {% if member.number_educ >= 1 %}<li>{{ member.education1 }}</li>{% endif %}
      {% if member.number_educ >= 2 %}<li>{{ member.education2 }}</li>{% endif %}
      {% if member.number_educ >= 3 %}<li>{{ member.education3 }}</li>{% endif %}
      {% if member.number_educ >= 4 %}<li>{{ member.education4 }}</li>{% endif %}
      {% if member.number_educ >= 5 %}<li>{{ member.education5 }}</li>{% endif %}
    </ul>
    {% endif %}
  </div>
</div>

---
{% endfor %}

## PhD Students
{% for member in phds %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="member-row">
  <div>
    {% if member.photo %}
    <img class="member-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
    {% endif %}
  </div>

  <div class="member-info">
    <h4>{{ member.name }}</h4>

    <div class="team-role">{{ member.info }}</div>

    {% if member.joined %}
    <div class="team-meta"><strong>Joined:</strong> {{ member.joined }}</div>
    {% endif %}

    {% if member.description %}
    <p>{{ member.description }}</p>
    {% endif %}
    
    {% if member.email %}
    <p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    {% endif %}
    
    {% if member.project_title %}
    <p><strong>Project:</strong> {{ member.project_title }}</p>
    {% endif %}

    {% if member.role_in_group %}
    <p><strong>Role in group:</strong> {{ member.role_in_group }}</p>
    {% endif %}

    {% if member.number_educ and member.number_educ > 0 %}
    <p><strong>Education</strong></p>
    <ul>
      {% if member.number_educ >= 1 %}<li>{{ member.education1 }}</li>{% endif %}
      {% if member.number_educ >= 2 %}<li>{{ member.education2 }}</li>{% endif %}
      {% if member.number_educ >= 3 %}<li>{{ member.education3 }}</li>{% endif %}
      {% if member.number_educ >= 4 %}<li>{{ member.education4 }}</li>{% endif %}
      {% if member.number_educ >= 5 %}<li>{{ member.education5 }}</li>{% endif %}
    </ul>
    {% endif %}
    
    {% if member.orcid %}
    <p><strong>ORCID:</strong> <a href="{{ member.orcid }}" target="_blank">{{ member.orcid }}</a></p>
    {% endif %}
    
  </div>
</div>

---
{% endfor %}

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
  {% if member.project_title %}<p><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
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
  {% if member.project_title %}<p><strong>Project:</strong> {{ member.project_title }}</p>{% endif %}
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
</div>
{% endfor %}
</div>

## Alumni

<div class="alumni-columns">
  <div class="alumni-column">
    <h3>PhD Graduates, Postdocs &amp; Fraunhofer PhDs</h3>
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
    <h3>Visiting Scientists, Fellows &amp; Internships</h3>
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
    <h3>Master Students &amp; Hiwi</h3>
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
