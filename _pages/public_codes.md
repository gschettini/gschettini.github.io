---
title:
layout: default
permalink: /public_codes/
published: true
---


<div class="public_codesContainer">

	<div class="gallery">


  {% for public_codes in site.public_codes %}

  {% if public_codes.redirect %}
  <div class="public_codesTile">
          <a href="{{ public_codes.redirect }}" target="_blank">
          <span>
              <h2>{{ public_codes.title }}</h2>
              <br/>
              <p>{{ public_codes.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="public_codesTile">
          <a href="{{ public_codes.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ public_codes.title }}</h2>
              <br/>
              <p>{{ public_codes.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
