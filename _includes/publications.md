<h2 id="publications" style="margin: 2px 0 12px;">Publications</h2>

<div class="publications">
  <ol class="bibliography">
    {% for link in site.data.publications.main %}
    <li style="margin-bottom: 24px;">
      <div class="pub-row" style="display: flex; gap: 20px; align-items: flex-start;">
        <div class="col-sm-3 abbr" style="width: 180px; flex-shrink: 0;">
          {% if link.image %}
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto;" alt="publication preview">
          {% endif %}
          {% if link.conference_short %}
          <div style="margin-top: 6px;">
            <abbr class="badge">{{ link.conference_short }}</abbr>
          </div>
          {% endif %}
        </div>

```
    <div class="col-sm-9" style="flex: 1;">
      <div class="title">
        <a href="{{ link.pdf }}">{{ link.title }}</a>
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical">
        <em>{{ link.conference }}</em>
      </div>

      <div class="links" style="margin-top: 6px;">
        {% if link.pdf %}
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px;">PDF</a>
        {% endif %}
        {% if link.code %}
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px;">Code</a>
        {% endif %}
        {% if link.page %}
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %}
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px;">BibTeX</a>
        {% endif %}
        {% if link.notes %}
        <strong><i style="color: #e74d3c;">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %}
        {{ link.others }}
        {% endif %}
      </div>
    </div>
  </div>
</li>
{% endfor %}
```

  </ol>
</div>
