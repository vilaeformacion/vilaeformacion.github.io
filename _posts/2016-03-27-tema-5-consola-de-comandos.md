---
layout: post
title:  "Tema 5: Consola de comandos"
date:   2016-03-27 10:00:00
curso: 1
categories: escritorio, raspbian
---

Tras ver como esta estructurado el sistema de ficheros en Linux, vamos a pasar a estudiar la consola de comandos. la consola de comandos es una interfaz de texto que nos permite realizar comandos y operaciones sin depender de una interfaz gráfica. En la consola de comandos, tenemos mucha más funcionalidad que en el escritorio gráfico. Muchas de las configuraciones avanzadas que realizaremos en Raspbian, vamos a realizarlas con la consola de comandos.

como hemos mostrado en anteriores lecciones, podemos acceder a la consola de comandos a través del botón superior izquierda ![consolacomandos]({{ site.url }}/resources/tema3/iconoconsola.png). Tras entrar en la consola de comandos, podemos escribir una serie de comandos u ordenes para poder ejemplo manejarnos en el sistema de ficheros, copiar ficheros, comprimir, etc...


### La consola de comandos

La consola de comandos nos permite realizar acciones de forma que podemos realizar acciones más avanzadas que con la interfaz gráfica.

La consola de comandos nos muestra un promt o mensaje que muestra el usuario con el que estamos conectados, y por otro lado en que máquina estamos conectados. Por ejemplo:

```bash
pi@zerasul:~$ _
```

para introducir un comando pondremos el comando en concreto y pulsaremos enter. Por ejemplo el comando _pwd_ nos muestra en que carpeta del sistema nos encontramos.

```bash
pi@zerasul:~$ pwd
/home/pi
```