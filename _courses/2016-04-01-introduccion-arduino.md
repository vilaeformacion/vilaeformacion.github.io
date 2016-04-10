---
layout: post
title:  "Introducción a Arduino"
date:   2016-04-01 00:00:00
categories: arduino, Electrónica
description: Curso de introducción a la electrónica con arduino.
---

Curso de introducción a la electrónica, usando la placa programable Arduino(o Genuino en Europa).

En las siguientes lecciones será capaz de crear sus propios dispositivos utilizando la placa plataforma de hardware libre Arduino.


### Temas de Teoria

{% for post in site.posts reversed %}
    	{% if post.curso == 3 %}
#### [{{post.title}}]({{post.url}})
 {% endif %}
 {% endfor %} 

### Prácticas

{% for post in site.posts reversed %}
    	{% if post.curso == 4 %}
#### [{{post.title}}]({{post.url}})
 {% endif %}
 {% endfor %} 
