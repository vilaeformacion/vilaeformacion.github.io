---
layout: post
title:  "Tema 2: Instalacion con NOOBS"
date:   2016-03-21 00:00:00
curso: 1
categories: instalacion, noobs
---

Tras ver en el tema anterior una introducción a linux y más concretamente a Raspberry Pi, pasaremos a instalar una distribución, utilizando el instalador NOOBs, podemos instalar cualquier distribución que nos provea el sistema.

### NOOBS

NOOBS(Network Out of the Box) es un instalador de sistema operativos que nos permite instalar una serie de sistemas operativos que puede descargarse a través de internet.

![noobs]({{ site.url }}/resources/noobs.png)

Para usar NOOBS, necesitaremos una tarjeta SD formateada en FAT de al menos 8Gb. 

Normalmente con NOOBS, por defecto solo podemos instalar _Raspbian_; un sistema operativo basado en debian; aunque podemos tener el resto de sistemas operativos a través de internet.

En este tema, realizaremos la instalacion de un sistema operativo a través de este instalador.

### Raspbian

Como hemos comentado anteriormente, Raspbian es un sistema operativo de proposito general basado en Debian, para la raspberry Pi. Es uno de los sistemas operativos más utilizados para este micro computador.

![raspbianlogo]({{ site.url }}/resources/raspbian-logo.png)

Seguidamente utilizaremos NOOBS para instalar este Sistema operativo o cualquier otro.

### Instalacion con NOOBS

NOOBS, nos permite instalar un sistema operativo de forma sencilla. Para ello vamos a descargarnos una imagen de NOOBS. Esta imagen la descargaremos desde la página oficial de Raspberry Pi.

La descarga puede encontarse [aquí](https://www.raspberrypi.org/downloads/noobs/).

![downloadnoobs]({{ site.url }}/resources/download.png)

En la página de descargas, hay 2 versiones la primera viene con el sistema Operativo Raspbian PreInstalado; y la segunda viene sin sistema operativo Pre instalado. Elegiremos la primera versión descargando la version en .zip.

Tras descargas esta imagen, descompremiremos el zip y copiaremos su contenido en una tarjeta SD vacia.

Tras pasar estos datos a una Tarjeta SD, la introduciremos en nuestra Raspberry Pi, y arrancaremos esta.

Tras realizar algunas acciones, nos aparecerán los sistemas operativos que hay disponibles.

![noobsinstall]({{ site.url }}/resources/noobs.png)

Como podemos ver en la lista, algunos sistemas operativos tienen un logo como una tarjeta SD; estos sistemas operativos ya estan instalados en la tarjeta y no requieren conexion a internet, y otros que tienen un icono de una conexion de red requeriran descargarse los archivos desde internet. Elegiremos el o los Sistemas operativos que necesitemos y pulsaremos en la opción de instalar. Tras esto NOOBS de forma automatica se encargará de instalar directamente todos los sistemas operativos que hemos seleccionado.

### Referencias

* [Raspberry Pi](http://raspberrypi.org)
* [NOOBS](https://www.raspberrypi.org/documentation/installation/noobs.md)
* [BooleanBite](http://booleanbite.com)
