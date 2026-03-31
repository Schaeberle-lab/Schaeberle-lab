---
title: "Schäberle Lab - Team"
layout: gridlay
excerpt: "Schäberle Lab: Team members"
sitemap: false
permalink: /team/
---

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/jpswalsh/academicons@1/css/academicons.min.css">

<style>
h2 {
  margin-top: 52px;
  margin-bottom: 20px;
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
}

.team-photo {
  width: 200px;
  height: 250px;
  object-fit: cover;
  display: block;
  margin: 0 auto 14px auto;
  border-radius: 10px;
}

.team-lead-nature {
  display: grid;
  grid-template-columns: 250px 1fr;
  gap: 34px;
  align-items: start;
  margin: 28px 0 44px 0;
  padding: 30px 0;
  border-top: 1px solid #d9d9d9;
  border-bottom: 1px solid #d9d9d9;
  background: #fff;
}

.team-lead-photo-block {
  text-align: center;
}

.team-lead-photo {
  width: 220px;
  height: 270px;
  object-fit: cover;
  border-radius: 0;
  display: block;
  margin: 0 auto;
}

.team-lead-links {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 12px;
  flex-wrap: wrap;
  font-size: 18px;
  margin-top: 12px;
}

.team-lead-links a {
  text-decoration: none;
  color: #444;
  transition: opacity 0.2s ease;
}

.team-lead-links a:hover {
  opacity: 0.65;
}

.team-lead-info {
  min-width: 0;
}

.team-lead-badge {
  display: none;
}

.team-lead-name {
  margin: 0 0 8px 0;
  font-size: 2rem;
  line-height: 1.1;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.team-lead-info .team-role {
  font-size: 1rem;
  font-weight: 500;
  color: #555;
  margin-bottom: 16px;
}

.team-lead-info p {
  margin-bottom: 12px;
  line-height: 1.6;
}

.team-lead-info a {
  color: #111;
  text-decoration: none;
  border-bottom: 1px solid #cfcfcf;
}

.team-lead-info a:hover {
  border-bottom-color: #111;
}

.team-lead-education {
  margin-top: 18px;
}

.team-lead-education p {
  margin-bottom: 6px;
}

.team-lead-education ul {
  margin: 0;
  padding-left: 20px;
}

.team-lead-education li {
  margin-bottom: 6px;
  line-height: 1.5;
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

.member-row {
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: 22px;
  align-items: start;
  margin: 18px 0 10px 0;
}

.member-photo-block {
  width: 220px;
  text-align: center;
}

.member-photo {
  width: 200px;
  height: 250px;
  object-fit: cover;
  display: block;
  border-radius: 10px;
  margin: 0 auto;
}

.member-info h4 {
  margin-top: 0;
  margin-bottom: 8px;
}

.member-links {
  width: 100%;
  max-width: 220px;
  margin-top: 8px;
  line-height: 1.35;
  word-break: break-word;
}

.member-links.icons {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
  flex-wrap: wrap;
  font-size: 18px;
  margin-top: 10px;
  width: 100%;
}

.member-links a {
  text-decoration: none;
}

.member-links a:hover {
  opacity: 0.75;
}

.member-divider {
  border: 0;
  border-top: 1px solid #e9e9e9;
  margin: 18px 0 28px 0;
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

@media (max-width: 1100px) {
  .alumni-columns {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 780px) {
  .team-lead-nature {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .team-lead-photo {
    margin: 0 auto;
  }

  .team-lead-name {
    font-size: 1.65rem;
  }

  .member-row {
    grid-template-columns: 1fr;
  }

  .member-photo-block {
    width: 100%;
    max-width: 220px;
    margin: 0 auto;
  }

  .member-photo {
    margin: 0 auto 14px auto;
  }

  .member-links {
    text-align: center;
  }
}
  .team-lead-info p,
.member-info p,
.team-card p,
.alumni-where,
.alumni-role,
.alumni-years,
.team-lead-education li,
.member-info li {
  text-align: justify;
  text-justify: inter-word;
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
<div class="team-lead team-lead-nature">
  <div class="team-lead-photo-block">
    {% if member.photo %}
    <img class="team-photo team-lead-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
    {% endif %}

    {% if member.orcid or member.researchgate or member.linkedin %}
    <div class="team-lead-links">
      {% if member.orcid %}
      <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer" title="ORCID">
        <i class="ai ai-orcid"></i>
      </a>
      {% endif %}
      {% if member.researchgate %}
      <a href="{{ member.researchgate }}" target="_blank" rel="noopener noreferrer" title="ResearchGate">
        <i class="ai ai-researchgate"></i>
      </a>
      {% endif %}
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank" rel="noopener noreferrer" title="LinkedIn">
        <i class="fa-brands fa-linkedin"></i>
      </a>
      {% endif %}
    </div>
    {% endif %}
  </div>

  <div class="team-lead-info">
    <h3 class="team-lead-name">{{ member.name }}</h3>
    <div class="team-role">{{ member.info }}</div>

    {% if member.email %}
    <p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    {% endif %}

    {% if member.description %}
    <p>{{ member.description }}</p>
    {% endif %}

    {% if member.project_title %}
    <p><strong>Research focus:</strong> {{ member.project_title }}</p>
    {% endif %}

    {% if member.education1 or member.education2 or member.education3 or member.education4 or member.education5 %}
    <div class="team-lead-education">
      <p><strong>Education</strong></p>
      <ul>
        {% if member.education1 %}<li>{{ member.education1 }}</li>{% endif %}
        {% if member.education2 %}<li>{{ member.education2 }}</li>{% endif %}
        {% if member.education3 %}<li>{{ member.education3 }}</li>{% endif %}
        {% if member.education4 %}<li>{{ member.education4 }}</li>{% endif %}
        {% if member.education5 %}<li>{{ member.education5 }}</li>{% endif %}
      </ul>
    </div>
    {% endif %}
  </div>
</div>
{% endfor %}

## Postdoctoral Researchers

{% for member in postdocs %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="member-row">
  <div class="member-photo-block">
    {% if member.photo %}
    <img class="member-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
    {% endif %}

    {% if member.orcid or member.researchgate or member.linkedin %}
    <div class="member-links icons">
      {% if member.orcid %}
      <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer" title="ORCID">
        <i class="ai ai-orcid"></i>
      </a>
      {% endif %}
      {% if member.researchgate %}
      <a href="{{ member.researchgate }}" target="_blank" rel="noopener noreferrer" title="ResearchGate">
        <i class="ai ai-researchgate"></i>
      </a>
      {% endif %}
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank" rel="noopener noreferrer" title="LinkedIn">
        <i class="fa-brands fa-linkedin"></i>
      </a>
      {% endif %}
    </div>
    {% endif %}
  </div>

  <div class="member-info">
    <h4>{{ member.name }}</h4>

    <div class="team-role">{{ member.info }}</div>

    {% if member.email %}
    <p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    {% endif %}

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

    {% if member.education1 or member.education2 or member.education3 or member.education4 or member.education5 %}
    <p><strong>Education</strong></p>
    <ul>
      {% if member.education1 %}<li>{{ member.education1 }}</li>{% endif %}
      {% if member.education2 %}<li>{{ member.education2 }}</li>{% endif %}
      {% if member.education3 %}<li>{{ member.education3 }}</li>{% endif %}
      {% if member.education4 %}<li>{{ member.education4 }}</li>{% endif %}
      {% if member.education5 %}<li>{{ member.education5 }}</li>{% endif %}
    </ul>
    {% endif %}
  </div>
</div>
{% unless forloop.last %}
<hr class="member-divider">
{% endunless %}
{% endfor %}

## PhD Students

{% for member in phds %}
{% assign photo_path = '/images/teampic/' | append: member.photo %}
<div class="member-row">
  <div class="member-photo-block">
    {% if member.photo %}
    <img class="member-photo" src="{{ photo_path | relative_url }}" alt="{{ member.name }}" onerror="this.style.display='none';">
    {% endif %}

    {% if member.orcid or member.researchgate or member.linkedin %}
    <div class="member-links icons">
      {% if member.orcid %}
      <a href="{{ member.orcid }}" target="_blank" rel="noopener noreferrer" title="ORCID">
        <i class="ai ai-orcid"></i>
      </a>
      {% endif %}
      {% if member.researchgate %}
      <a href="{{ member.researchgate }}" target="_blank" rel="noopener noreferrer" title="ResearchGate">
        <i class="ai ai-researchgate"></i>
      </a>
      {% endif %}
      {% if member.linkedin %}
      <a href="{{ member.linkedin }}" target="_blank" rel="noopener noreferrer" title="LinkedIn">
        <i class="fa-brands fa-linkedin"></i>
      </a>
      {% endif %}
    </div>
    {% endif %}
  </div>

  <div class="member-info">
    <h4>{{ member.name }}</h4>

    <div class="team-role">{{ member.info }}</div>

    {% if member.email %}
    <p><strong>Email:</strong> <a href="mailto:{{ member.email }}">{{ member.email }}</a></p>
    {% endif %}

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

    {% if member.education1 or member.education2 or member.education3 or member.education4 or member.education5 %}
    <p><strong>Education</strong></p>
    <ul>
      {% if member.education1 %}<li>{{ member.education1 }}</li>{% endif %}
      {% if member.education2 %}<li>{{ member.education2 }}</li>{% endif %}
      {% if member.education3 %}<li>{{ member.education3 }}</li>{% endif %}
      {% if member.education4 %}<li>{{ member.education4 }}</li>{% endif %}
      {% if member.education5 %}<li>{{ member.education5 }}</li>{% endif %}
    </ul>
    {% endif %}
  </div>
</div>
{% unless forloop.last %}
<hr class="member-divider">
{% endunless %}
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
      {% if member.years %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
      {% if member.whereabouts %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
    </div>
    {% endfor %}
  </div>

  <div class="alumni-column">
    <h3>Visiting Scientists, Fellows &amp; Internships</h3>
    {% for member in alumni_visiting %}
    <div class="alumni-entry">
      <div class="alumni-name">{{ member.name }}</div>
      {% if member.position %}<div class="alumni-role">{{ member.position }}</div>{% endif %}
      {% if member.years %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
      {% if member.whereabouts %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
    </div>
    {% endfor %}
  </div>

  <div class="alumni-column">
    <h3>Master Students &amp; Hiwi</h3>
    {% for member in alumni_master %}
    <div class="alumni-entry">
      <div class="alumni-name">{{ member.name }}</div>
      {% if member.position %}<div class="alumni-role">{{ member.position }}</div>{% endif %}
      {% if member.years %}<div class="alumni-years">{{ member.years }}</div>{% endif %}
      {% if member.whereabouts %}<div class="alumni-where"><strong>Now:</strong> {{ member.whereabouts }}</div>{% endif %}
    </div>
    {% endfor %}
  </div>
</div>
