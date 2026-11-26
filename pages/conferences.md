---
layout: default
lang: es
title: Congresos y estancias
description: Participación en congresos y estancias de investigación
background: assets/theme/backgrounds/network-rope.jpg
permalink: /conferences/
translation_url: /conferences-en/
---

En esta sección se recogen los congresos científicos
y las estancias de investigación en los que participan
los miembros del Laboratorio LaCoMaRCA.

{% assign eventos = site.data.eventos | sort: "fecha" | reverse %}

### Congresos científicos

{% assign congresos = eventos | where: "tipo", "congreso" %}

{% if congresos.size > 0 %}
<ul>
{% for e in congresos %}
  <li style="margin-bottom: 1em;">
    <div>
      <strong>Congreso:</strong> {{ e.titulo_es | escape }}
      {% if e.lugar != "" %}
        — {{ e.lugar | escape }}
      {% endif %}
      — {{ e.fecha_es | escape }}
    </div>

    {% if e.participantes != "" %}
    <div>
      <strong>Participantes:</strong> {{ e.participantes | escape }}
    </div>
    {% endif %}

    {% if e.charla_es != "" %}
    <div>
      <strong>Comunicación:</strong> {{ e.charla_es | escape }}
      {% if e.modo_es != "" %}
        ({{ e.modo_es | escape }})
      {% endif %}
    </div>
    {% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
No hay congresos registrados.
{% endif %}

### Estancias de investigación

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
