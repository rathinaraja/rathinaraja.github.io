---
layout: page
permalink: /cv/
title: CV
nav: true
nav_order: 5
toc: false
---

{% assign resume = site.data.cv.cv %}

<style>
.cv-profile {max-width: 1050px; margin: 0 auto; line-height: 1.65;}
.cv-actions {display:flex;flex-wrap:wrap;gap:.85rem;margin:1rem 0 1.6rem;}
.cv-action {display:inline-flex;align-items:center;gap:.55rem;padding:.7rem 1.1rem;border:1px solid var(--global-theme-color);border-radius:9px;text-decoration:none!important;font-weight:650;}
.cv-action:hover {background:var(--global-theme-color);color:white!important;}
.cv-profile-links {display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:.55rem 1rem;margin:1rem 0 1.5rem;}
.cv-profile-links a {display:flex;align-items:center;gap:.5rem;min-width:0;overflow-wrap:anywhere;text-decoration:none;padding:.45rem .65rem;border:1px solid var(--global-divider-color);border-radius:8px;}
.cv-profile-links a:hover {border-color:var(--global-theme-color);}
.cv-profile h2 {margin-top:2rem;padding-bottom:.4rem;border-bottom:1px solid var(--global-divider-color);}
.cv-profile h3 {font-size:1.05rem;margin-top:1.15rem;}
.cv-entry {margin:.8rem 0 1.1rem;}
.cv-entry-head {display:flex;justify-content:space-between;align-items:baseline;gap:1rem;flex-wrap:wrap;}
.cv-date {color:var(--global-text-color-light);font-size:.9em;white-space:nowrap;}
.cv-subtle {color:var(--global-text-color-light);}
.cv-profile ul {padding-left:1.4rem;}
@media(max-width:700px){.cv-profile-links{grid-template-columns:repeat(2,minmax(0,1fr));}}
@media(max-width:430px){.cv-profile-links{grid-template-columns:1fr;}}
</style>

<div class="cv-profile">
  <div class="cv-actions" aria-label="Download documents">
    <a class="cv-action" href="{{ '/assets/pdf/Rathinaraja_Jeyaraj_Resume.pdf' | relative_url }}" target="_blank" rel="noopener" aria-label="Open Resume PDF"><i class="fa-solid fa-file-lines" aria-hidden="true"></i> Resume <i class="fa-solid fa-arrow-up-right-from-square" aria-hidden="true"></i></a>
    <a class="cv-action" href="{{ '/assets/pdf/Rathinaraja_Jeyaraj_CV.pdf' | relative_url }}" target="_blank" rel="noopener" aria-label="Open full CV PDF"><i class="fa-solid fa-file-pdf" aria-hidden="true"></i> CV <i class="fa-solid fa-arrow-up-right-from-square" aria-hidden="true"></i></a>
  </div>
  <h2>Contact Information</h2>
  <p><strong>{{ resume.name }}</strong><br>{{ resume.label }}<br>{{ resume.organization }}<br>
  {% for email in resume.emails %}<a href="mailto:{{ email }}">{{ email }}</a>{% unless forloop.last %} · {% endunless %}{% endfor %}<br>
  <i class="fa-solid fa-location-dot" aria-hidden="true"></i> {{ resume.location }}</p>

  <div class="cv-profile-links" aria-label="Professional profiles">
    {% for profile in resume.profile_links %}
      <a href="{{ profile.url }}" target="_blank" rel="noopener noreferrer" aria-label="{{ profile.name }}">
        {% case profile.name %}
        {% when 'Official' %}<i class="fa-solid fa-building-columns" aria-hidden="true"></i>
        {% when 'LinkedIn' %}<i class="fa-brands fa-linkedin" aria-hidden="true"></i>
        {% when 'GitHub' %}<i class="fa-brands fa-github" aria-hidden="true"></i>
        {% when 'Google Scholar' %}<i class="fa-solid fa-graduation-cap" aria-hidden="true"></i>
        {% when 'ResearchGate' %}<i class="fa-brands fa-researchgate" aria-hidden="true"></i>
        {% when 'OpenReview' %}<i class="fa-solid fa-file-pen" aria-hidden="true"></i>
        {% when 'Web of Science' %}<i class="fa-solid fa-book-open" aria-hidden="true"></i>
        {% when 'ORCID' %}<i class="fa-brands fa-orcid" aria-hidden="true"></i>
        {% when 'Scopus' %}<i class="fa-solid fa-book" aria-hidden="true"></i>
        {% when 'DBLP' %}<i class="fa-solid fa-database" aria-hidden="true"></i>
        {% when 'Semantic Scholar' %}<i class="fa-solid fa-brain" aria-hidden="true"></i>
        {% when 'SciProfiles' %}<i class="fa-solid fa-user-graduate" aria-hidden="true"></i>
        {% when 'Academia.edu' %}<i class="fa-solid fa-landmark" aria-hidden="true"></i>
        {% endcase %} <span>{{ profile.name }}</span></a>
    {% endfor %}
  </div>

  <h2>Professional Summary</h2>
  <p>{{ resume.summary }}</p>

  <h2>Research Interests</h2>
  {% for item in resume.sections.Interests %}
    <h3>{{ item.name }}</h3>
    <p>{{ item.keywords }}</p>
  {% endfor %}
  <h3>Selected Research Publications</h3>
  <ul>{% for item in resume.sections['Selected Publications'] %}<li>{{ item.name }}</li>{% endfor %}</ul>
  <h3>Professional Memberships</h3>
  <ul>{% for item in resume.sections.Memberships %}<li>{{ item.name }}{% if item.summary %} – {{ item.summary }}{% endif %}</li>{% endfor %}</ul>

  <h2>Education</h2>
  {% for item in resume.sections.Education %}
    <div class="cv-entry"><div class="cv-entry-head"><strong>{{ item.studyType }} in {{ item.area }}</strong><span class="cv-date">{{ item.start_date }} – {{ item.end_date }}</span></div>
    {{ item.institution }} · {{ item.location }}</div>
  {% endfor %}

  <h2>Experience</h2>
  {% for item in resume.sections.Experience %}
    <div class="cv-entry"><div class="cv-entry-head"><strong>{{ item.position }}</strong><span class="cv-date">{{ item.start_date }} – {{ item.end_date }}</span></div>
    {{ item.company }} · {{ item.location }}</div>
  {% endfor %}

  <h2>Technical Skills</h2>
  {% for item in resume.sections.Skills %}
    <h3>{% if item.icon %}<i class="{{ item.icon }}" aria-hidden="true"></i> {% endif %}{{ item.name }}</h3>
    <p>{{ item.keywords }}</p>
  {% endfor %}

  <h2>Research Projects Worked</h2>
  {% for item in resume.sections.Projects %}
    <div class="cv-entry"><div class="cv-entry-head"><strong>{{ item.name }}</strong><span class="cv-date">{{ item.start_date }} – {{ item.end_date }}</span></div></div>
  {% endfor %}

  <h2>Research Proposals</h2>
  <p>Contributed to the development of the following research proposals:</p>
  <ol>{% for item in resume.sections['Research Proposals'] %}<li>{{ item.name }} ({{ item.summary }})</li>{% endfor %}</ol>

  <h2>Professional Services</h2>
  {% for item in resume.sections['Professional Services'] %}
    <h3>{{ item.name }}</h3>
    <ul>{% assign entries = item.summary | split: '; ' %}{% for entry in entries %}<li>{{ entry }}</li>{% endfor %}</ul>
  {% endfor %}
</div>
