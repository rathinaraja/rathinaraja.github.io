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
/* Scoped CV design: compact profiles, stronger hierarchy, and responsive cards. */
.cv-profile{max-width:1120px;margin:0 auto;line-height:1.7;--cv-accent:var(--global-theme-color,#2563eb);}
.cv-actions{display:flex;flex-wrap:wrap;gap:.7rem;margin:.8rem 0 1.65rem;}
.cv-action{display:inline-flex;align-items:center;gap:.6rem;padding:.68rem 1.15rem;border:1px solid var(--cv-accent);border-radius:11px;text-decoration:none!important;font-weight:700;transition:background .2s,transform .2s,box-shadow .2s;}
.cv-action:hover,.cv-action:focus-visible{background:var(--cv-accent);color:white!important;transform:translateY(-2px);box-shadow:0 5px 16px rgba(0,0,0,.13);}
.cv-profile-links{display:grid;grid-template-columns:repeat(5,minmax(0,1fr));gap:.44rem;margin:.85rem 0 1.8rem;}
.cv-profile-links a{display:flex;align-items:center;justify-content:flex-start;gap:.42rem;min-width:0;white-space:nowrap;text-decoration:none!important;font-size:.82rem;font-weight:600;line-height:1.3;padding:.48rem .55rem;border:1px solid var(--global-divider-color,#ddd);border-radius:9px;background:var(--global-card-bg-color,transparent);transition:border-color .18s,background .18s,transform .18s,box-shadow .18s;}
.cv-profile-links a i{color:var(--cv-accent);font-size:1rem;flex:0 0 1.1rem;text-align:center;}
.cv-profile-links a span{overflow:hidden;text-overflow:ellipsis;}
.cv-profile-links a:hover,.cv-profile-links a:focus-visible{border-color:var(--cv-accent);background:rgba(100,120,180,.07);transform:translateY(-2px);box-shadow:0 3px 10px rgba(0,0,0,.07);}
.cv-profile h2{margin:2.2rem 0 1rem;padding:0 0 .65rem;border-bottom:2px solid var(--global-divider-color,#ddd);font-size:1.5rem;font-weight:750;letter-spacing:-.02em;}
.cv-profile h2::before{content:"";display:inline-block;width:5px;height:1.05em;vertical-align:-.14em;background:var(--cv-accent);border-radius:5px;margin-right:.62rem;}
.cv-profile h3{display:flex;align-items:center;gap:.45rem;font-size:1.12rem;line-height:1.45;font-weight:750;color:var(--cv-accent);margin:1.35rem 0 .5rem;padding:.48rem .75rem;border-left:3px solid var(--cv-accent);background:rgba(100,120,180,.07);border-radius:0 8px 8px 0;}
.cv-profile h3 i{font-size:1rem;}
.cv-entry{margin:.6rem 0;padding:.85rem 1rem;border:1px solid var(--global-divider-color,#ddd);border-radius:10px;background:var(--global-card-bg-color,transparent);}
.cv-entry-head{display:flex;justify-content:space-between;align-items:baseline;gap:.6rem 1rem;flex-wrap:wrap;}
.cv-date{color:var(--global-text-color-light);font-size:.88em;white-space:nowrap;font-weight:600;}
.cv-subtle{color:var(--global-text-color-light);}
.cv-profile ul,.cv-profile ol{padding-left:1.5rem;}
.cv-profile li{padding:.13rem 0;}
@media(max-width:1000px){.cv-profile-links{grid-template-columns:repeat(4,minmax(0,1fr));}}
@media(max-width:720px){.cv-profile-links{grid-template-columns:repeat(3,minmax(0,1fr));}.cv-profile h2{font-size:1.33rem;}}
@media(max-width:490px){.cv-profile-links{grid-template-columns:repeat(2,minmax(0,1fr));}.cv-profile-links a{font-size:.78rem;padding:.43rem .5rem;}.cv-entry{padding:.75rem;}}
@media(prefers-reduced-motion:reduce){.cv-action,.cv-profile-links a{transition:none;}.cv-action:hover,.cv-profile-links a:hover{transform:none;}}
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
