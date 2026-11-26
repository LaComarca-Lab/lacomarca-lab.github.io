---
layout: default
lang: en
title: Conferences and Research Visits
description: Conferences and research visits by our members
background: assets/theme/backgrounds/network-rope.jpg
permalink: /conferences-en/
translation_url: /conferences/
---

This section presents the scientific conferences and
research visits in which members of the LaCoMaRCA
Laboratory participate.

{% assign eventos = site.data.eventos | sort: "fecha" | reverse %}

### Scientific Conferences

Participation in national and international
scientific conferences.

{% assign congresos = eventos | where: "tipo", "congreso" %}

{% if congresos.size > 0 %}
<ul>
{% for e in congresos %}
  <li style="margin-bottom: 1em;">
    <div>
      <strong>Congress:</strong> {{ e.titulo_es | escape }}
      {% if e.lugar_en != "" %}
        — {{ e.lugar_en | escape }}
      {% endif %}
      — {{ e.fecha_en | escape }}
    </div>

    {% if e.participantes != "" %}
    <div>
      <strong>Participants:</strong> {{ e.participantes | escape }}
    </div>
    {% endif %}

    {% if e.charla_en != "" %}
    <div>
      <strong>Comunication:</strong> {{ e.charla_en | escape }}
      {% if e.modo_en != "" %}
        ({{ e.modo_en | escape }})
      {% endif %}
    </div>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
There are no registered congresses.
{% endif %}

### Research Visits

Research visits undertaken by members of the
Laboratory.

{% assign estancias = eventos | where: "tipo", "estancia" %}

{% if estancias.size > 0 %}
<ul>
{% for e in estancias %}
  <li>
    <strong>{{ e.fecha_en }}</strong>:
    {{ e.titulo_en | escape }}
    {% if e.lugar != "" %}
      — {{ e.lugar | escape }}
    {% endif %}
    {% if e.participantes != "" %}
      — {{ e.participantes | escape }}
    {% endif %}
    {% if e.detalle_en != "" %}
      — {{ e.detalle_en | escape }}
    {% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
No hay estancias registradas.
{% endif %}
