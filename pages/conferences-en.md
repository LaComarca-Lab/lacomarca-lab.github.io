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
  <li>
    <strong>{{ e.fecha_en }}</strong>:
    {% if e.url and e.url != "" %}
      <a href="{{ e.url }}">{{ e.titulo_en | escape }}</a>
    {% else %}
      {{ e.titulo_en | escape }}
    {% endif %}
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
No hay congresos registrados.
{% endif %}

### Research Visits

Research visits undertaken by members of the
Laboratory.

{% assign estancias = eventos | where: "tipo", "estancia" %}

{% if estancias.size > 0 %}
<ul>
{% for e in estancias %}
  <li>
    <strong>{{ e.fecha_es }}</strong>:
    {{ e.titulo_es | escape }}
    {% if e.lugar != "" %}
      — {{ e.lugar | escape }}
    {% endif %}
    {% if e.participantes != "" %}
      — {{ e.participantes | escape }}
    {% endif %}
    {% if e.detalle_es != "" %}
      — {{ e.detalle_es | escape }}
    {% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
No hay estancias registradas.
{% endif %}
