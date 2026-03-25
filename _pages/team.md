---
title: "Schäberle Lab - Team"
layout: gridlay
excerpt: "Schäberle Lab: Team members"
sitemap: false
permalink: /team/
---

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

Jump to [Group Leader](#group-leader), [Postdoctoral Researchers](#postdoctoral-researchers), [Project Scientists](#project-scientists), [PhD Students](#phd-students), [Master Students](#master-students), [Administration](#administration), [Alumni](#alumni).

## Group Leader {#group-leader}

{% for member in pi_members %}
### {{ member.name }}

**{{ member.info }}**

{% if member.description %}{{ member.description }}{% endif %}

{% if member.project_title %}**Research focus:** {{ member.project_title }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

{% if member.number_educ and member.number_educ > 0 %}
**Position / background**
{% if member.number_educ >= 1 %}- {{ member.education1 }}{% endif %}
{% if member.number_educ >= 2 %}- {{ member.education2 }}{% endif %}
{% if member.number_educ >= 3 %}- {{ member.education3 }}{% endif %}
{% if member.number_educ >= 4 %}- {{ member.education4 }}{% endif %}
{% if member.number_educ >= 5 %}- {{ member.education5 }}{% endif %}
{% endif %}

---
{% endfor %}

## Postdoctoral Researchers {#postdoctoral-researchers}

{% for member in postdocs %}
### {{ member.name }}

**{{ member.info }}**

{% if member.joined %}**Joined:** {{ member.joined }}{% endif %}

{% if member.description %}{{ member.description }}{% endif %}

{% if member.project_title %}**Project:** {{ member.project_title }}{% endif %}

{% if member.role_in_group %}**Role in group:** {{ member.role_in_group }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

---
{% endfor %}

## Project Scientists {#project-scientists}

{% for member in project_scientists %}
### {{ member.name }}

**{{ member.info }}**

{% if member.joined %}**Joined:** {{ member.joined }}{% endif %}

{% if member.description %}{{ member.description }}{% endif %}

{% if member.project_title %}**Project:** {{ member.project_title }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

---
{% endfor %}

## PhD Students {#phd-students}

{% for member in phds %}
### {{ member.name }}

**{{ member.info }}**

{% if member.joined %}**Joined:** {{ member.joined }}{% endif %}

{% if member.description %}{{ member.description }}{% endif %}

{% if member.project_title %}**Project:** {{ member.project_title }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

{% if member.papers and member.papers.size > 0 %}
**Selected papers**
{% for paper in member.papers %}
- {{ paper }}
{% endfor %}
{% endif %}

---
{% endfor %}

## Master Students {#master-students}

{% for member in masters %}
### {{ member.name }}

**{{ member.info }}**

{% if member.project_title %}**Project:** {{ member.project_title }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

---
{% endfor %}

## Administration {#administration}

{% for member in admin %}
### {{ member.name }}

**{{ member.info }}**

{% if member.description %}{{ member.description }}{% endif %}

{% if member.project_title %}**Role:** {{ member.project_title }}{% endif %}

{% if member.email != "" %}**Email:** {{ member.email }}{% endif %}

---
{% endfor %}

## Alumni {#alumni}

### PhD Graduates, Postdocs & Fraunhofer PhDs

{% for member in alumni_phd_postdoc %}
**{{ member.name }}**  
{% if member.position %}{{ member.position }}{% endif %}  
{% if member.years != "" %}{{ member.years }}{% endif %}  
{% if member.whereabouts != "" %}**Now:** {{ member.whereabouts }}{% endif %}

---
{% endfor %}

### Visiting Scientists, Fellows & Internships

{% for member in alumni_visiting %}
**{{ member.name }}**  
{% if member.position %}{{ member.position }}{% endif %}  
{% if member.years != "" %}{{ member.years }}{% endif %}  
{% if member.whereabouts != "" %}**Now:** {{ member.whereabouts }}{% endif %}

---
{% endfor %}

### Master Students & Hiwi

{% for member in alumni_master %}
**{{ member.name }}**  
{% if member.position %}{{ member.position }}{% endif %}  
{% if member.years != "" %}{{ member.years }}{% endif %}  
{% if member.whereabouts != "" %}**Now:** {{ member.whereabouts }}{% endif %}

---
{% endfor %}
