<h2 id="projects">Projects</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.projects.main %}

<li class="project-card">
<div class="pub-row">
  {% if link.image %}
  <div class="col-sm-3 abbr">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="{{ link.title }} teaser">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  {% endif %}
  <div class="col-sm-9 project-content">
      <div class="title">{{ link.title }}</div>
      <div class="author">{{ link.authors }}</div>
      {% if link.description %}
      <p class="project-description">{{ link.description }}</p>
      {% endif %}
      {% if link.tags %}
      <div class="project-tags">{{ link.tags }}</div>
      {% endif %}
    <div class="links">
      {% if link.Video %} 
      <a href="{{ link.Video }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Video</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <i style="color:#e74d3c">{{ link.notes }}</i>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>
