<h2 id="publications" style="margin: 2px 0 12px;">Publications</h2>

<div class="publications">
  <ol class="bibliography" style="list-style: none; padding: 0;">
    {% for link in site.data.publications.main %}
    <li style="margin-bottom: 30px;">
      <div class="pub-row" style="display: flex; gap: 20px; align-items: flex-start;">
        
        <div class="col-sm-3 abbr" style="width: 180px; flex-shrink: 0;">
          {% if link.image %}
          <img src="{{ link.image | relative_url }}" class="teaser img-fluid z-depth-1" style="width: 100%; height: auto; border-radius: 4px;" alt="publication preview">
          {% endif %}
          {% if link.conference_short %}
          <div style="margin-top: 6px; text-align: center;">
            <abbr class="badge" style="background-color: #0076df;">{{ link.conference_short }}</abbr>
          </div>
          {% endif %}
        </div>

        <div class="col-sm-9" style="flex: 1;">
          <div class="title" style="font-weight: bold; font-size: 1.1em; margin-bottom: 4px;">
            <a href="{{ link.pdf }}" target="_blank">{{ link.title }}</a>
          </div>
          <div class="author" style="font-size: 0.95em;">{{ link.authors }}</div>
          <div class="periodical" style="font-size: 0.9em; font-style: italic; color: #555;">
            {{ link.conference }}
          </div>

          <div class="links" style="margin-top: 8px;">
            {% if link.pdf %}
            <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; border: 1px solid #ccc; padding: 2px 8px; border-radius: 4px; text-decoration: none; color: inherit;">PDF</a>
            {% endif %}
            {% if link.code %}
            <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size: 12px; border: 1px solid #ccc; padding: 2px 8px; border-radius: 4px; text-decoration: none; color: inherit; margin-left: 4px;">Code</a>
            {% endif %}
          </div>
        </div>
        
      </div>
    </li>
    {% endfor %}
  </ol>
</div>