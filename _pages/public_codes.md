---
title:
layout: default
permalink: /_public_codes/
published: true
---


<div class="codesContainer">

	<div class="gallery">


  {% for codes in site.codess %}

  {% if codes.redirect %}
  <div class="codesTile">
          <a href="{{ codes.redirect }}" target="_blank">
          <span>
              <h2>{{ codes.title }}</h2>
              <br/>
              <p>{{ codes.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="codesTile">
          <a href="{{ codes.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ codes.title }}</h2>
              <br/>
              <p>{{ codes.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
