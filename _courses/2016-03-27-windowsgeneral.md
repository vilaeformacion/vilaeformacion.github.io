---
layout: post
title:  "Informática General para Usuarios"
date:   2016-03-27 00:00:00
categories: alfabetización informática, informática, informática usuario, curso de informática, windows 7
description: Curso enfocado a todas aquellas personas que desean introducirse al Uso de un Ordenador bajo Windows 7/8/10, así como para aquellos que deseen refrescar conocimientos, etc.
---
# Informática General para Usuarios.

![tux]({{ site.url }}/resources/logowin.png)

En este curso trataremos de explicar de una manera sencilla y cercana conceptos, y teoría suficientes para aquellos Usuari@s que se acercan por primera vez en lo que refiere al uso de un Ordenador y al Sistema Operativo Windows, en sus versiones Windows 7/8/10.

Este Curso se encuentra dividido en diferentes temas, para su comprensión, y en ocasiones de algunas prácticas "guiadas".

Por otro lado tambien encontraremos en este curso algunas tareas consideradas de "uso cotidiano", así como tambien algunas curiosidades que pudieran interesar a los alumnos, en cuanto a la realización de algunas tareas varias, o la utilización de algunas herramientas varias, no incluidas en el Sistema Operativo en sí mismo.

{% for post in site.posts reversed %}
    	{% if post.curso == 2 %}
#### [{{post.title}}]({{post.url}})
 {% endif %}
 {% endfor %} 