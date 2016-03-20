---
layout: post
title:  "Tema 1: Historia de Linux y Raspberry Pi "
date:   2016-03-20 00:00:00
curso: 1
categories: linux,historia
---
En este primer tema, vamos a comenzar a mostrar los conceptos básicos del Sistema operativo GNU/Linux estudiando su historia y de que partes se componen. Entre otros conceptos, estudiaremos que es una distribución, versiones del núcleo, desarrollos basados en GNU/Linux, y además estudiaremos que es una Raspberry Pi y que distribuciones o versiones tiene.

### GNU/Linux

GNU/Linux o Linux como se le conoce normalmente, es un sistema operativo de código abierto; esto quiere decir que el código fuente de este esta disponible para todo el mundo y es creado por una comunidad de desarrolladores por todo el mundo.

El núcleo de Linux, fue creado por Linus Torvals en el año 1992 presentando el núcleo del sistema operativo que conocemos hoy en día. Posteriormente la fundación GNU, presento el resto de herramientas necesarias para poder crear o poder utilizar el sistema Operativo como lo conocemos hoy en día.

![torvals]({{ site.url }}/resources/torvals.png)

### Partes del Sistema Operativo Linux

 Linux o GNU/Linux, se compone de distintas partes entre ellas el núcleo que es el encargado de gestionar la memoria, entrada salida y los procesos o programas que se ejecutan en el procesador.

 Después se encuentran las herramientas necesarias para poder utilizar el sistema operativo como tal; como pueden ser los entornos de escritorio, consola de comandos o compiladores e interpretes.

 El conjunto de todos estos componentes es la denominada **distribución**; existen muchas distribuciones que nos permitiran realizar unas funciones u otras en función de lo que necesitemos.

 Entre las más conocidas en entornos de escritorio podemos encontrar:

 * Debian
 * Fedora
 * Ubuntu
 * ArchLinux

En este curso nos centraremos en una distribución basada en Debian llamada _Raspbian_; esta distribución, creada para el minicomputador Raspberry Pi nos permitirá utilizar dicho computador de forma sencilla en un entorno de escritorio.

### Raspberry Pi

![Raspberrypi]({{ site.url }}/resources/rpi2.jpeg)

La Raspberry Pi, es un minicomputador de bajo coste pensado para que personas con pocos recursos puedan acceder a las ciencias de la computación. Existen varios modelos de esta y tiene un procesador basado en la arquitectura MIPS(ARM). Este computador, apareció en el año 2012 y desde entonces ha sido uno de los más utilziados. Entre otras por su bajo coste y gran comunidad que permite que su software sea actualizado constantemente.

Existen varios modelos de este computador; cada uno con sus características y funcionalidades.

![modelospi]({{ site.url }}/resources/modelosRpi.png)

 Tras ver los modelos de Raspberry pi que podemos encontrar, mostramos el esquema de los componentes hardware que tiene este micro computador.

 ![esquemapi]({{ site.url }}/resources/esquemapi.png)

Pero el aspecto también más importante de este microcomputador, es la gran cantidad de software que podemos encontrar para este. Como por ejemplo las distintas distribuciones que podemos encontrar.

**Distribuciones de proposito general** 

Seguidamente se muestran las distribuciones de proposito general.

![distgenerales]({{ site.url}}/resources/dispropositogeneral.png)

* Raspbian
* Pidora
* ArchiLinux
* Risc Os

**Distribuciones de Uso Especifico**

A continuación se muestran las distribuciones de uso especifico

![disusoespecifico]({{ site.url }}/resources/distespecificas.png)

* OpenElec (Centro multimedia)
* Lakka.tv (Retroconsola)
* Arkos (Nube Privada)
* Windows 10 (Internet de las cosas)

### Raspbian

Raspbian es una distribución para la Raspberry Pi basada en debian; es la más utilizada y suele ser la más recomendada a la hora de empezar a utilizar la Raspberry Pi. Esta distribución nos permite tener un ordenador de escritorio perfectamente funcional.

![raspbian]({{ site.url }}/resources/raspbian.jpg)

En próximas lecciones estudiaremos esta distribución y como instalarla utilizando NOOBS.

### Referencias

* [GNU/Linux](https://es.wikipedia.org/wiki/GNU/Linux)
* [Raspberry Pi](https://www.raspberrypi.org)
* [Raspbian](https://www.raspbian.org)
