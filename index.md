---
title: "Home"
---

{% assign p = site.data.profile %}

<section class="card hero" id="about">
  <div>
    <div class="h1">{{ p.name }}</div>
    <div class="subtitle">{{ p.affiliation }} · {{ p.location }}</div>
    <p class="small">{{ p.bio }}</p>

    <div class="pill-row">
      {% for it in p.interests %}
        <span class="pill">{{ it }}</span>
      {% endfor %}
    </div>
  </div>

  <div>
    <div class="links">
      {% for l in p.links %}
        <a href="{{ l.url }}" target="_blank" rel="noopener noreferrer">{{ l.label }}</a>
      {% endfor %}
      <a href="mailto:{{ p.email }}">{{ p.email }}</a>
    </div>
  </div>
</section>

<section class="card section" id="news">
  <h2>News</h2>
  <ul class="list">
    {% for n in site.data.news %}
      <li><span class="muted">{{ n.date }}</span> — {{ n.text }}</li>
    {% endfor %}
  </ul>
</section>

<section class="card section" id="publications">
  <h2>Publications</h2>
  <div class="muted small">(* Replace placeholder entries in <code>_data/publications.yml</code>.)</div>
  <div style="margin-top:10px">
    {% for block in site.data.publications %}
      <div class="muted" style="margin-top:12px; font-weight:650">{{ block.year }}</div>
      {% for pub in block.items %}
        <div class="pub">
          <div class="pub-title">{{ pub.title }}</div>
          <div class="pub-meta">{{ pub.authors }} · {{ pub.venue }}</div>
          {% if pub.links %}
            <div class="pub-links">
              {% for ln in pub.links %}
                <a href="{{ ln.url }}" target="_blank" rel="noopener noreferrer">[{{ ln.label }}]</a>
              {% endfor %}
            </div>
          {% endif %}
        </div>
      {% endfor %}
    {% endfor %}
  </div>
</section>

<section class="card section" id="projects">
  <h2>Projects</h2>
  <div style="margin-top:10px">
    {% for pr in site.data.projects %}
      <div class="pub">
        <div class="pub-title">{{ pr.name }}</div>
        <div class="pub-meta">{{ pr.period }} · {{ pr.org }}</div>
        {% if pr.bullets %}
          <ul class="list">
            {% for b in pr.bullets %}
              <li>{{ b }}</li>
            {% endfor %}
          </ul>
        {% endif %}
      </div>
    {% endfor %}
  </div>
</section>

<section class="card section" id="contact">
  <h2>Contact</h2>
  <div class="small">
    Email: <a href="mailto:{{ p.email }}">{{ p.email }}</a>
  </div>
</section>

