---
layout: post
title:  "Tema 3: Escritorio Raspbian"
date:   2016-03-21 10:00:00
curso: 1
categories: instalacion, noobs
---

Tras instalar nuestro sistema operativo con NOOBS, pasaremos a ver todos los aspectos de la distribución RASPBIAN. En este tema, veremos desde el escritorio, los programas preinstalados y como configurar nuestra Raspberry Pi.

Para arrancar Raspbian, solo necesitaremos insertar la tarjeta SD donde inslatamos el sistema, y arrancar nuestra Raspberry Pi. El sistema arrancará Raspbian automáticamente.

**NOTA**: En anteriores versiones de Raspbian, el sistema pedia unas credenciales y arrancaba en modo texto por defecto. Las credenciales por defecto son usuario _pi_ y la contraseña es _raspberry_. Tras acceder al sistema solo tiene que ejecutar el siguiente comando:

_startx_

y al pulsar ENTER, entrará en el modo gráfico y podremos acceder al escritorio.

### Raspbian

Como hemos mencionado ya varias veces en este curso, Raspbian es una distribución basada en Debian optimizada para el minicomputador Raspberry Pi. En este tema veremos el escritorio y motraremos las principales características de este.

### El escritorio

Tras arrancar el sistema, observaremos el escritorio el cual tiene una interfaz amigable con un menú en la parte superior izquierda.

![escritorio]({{ site.url }}/resources/tema3/escritorio.png)

en la parte superior, veremos la barra de tareas donde podemos ver los programas que tenemos abiertos en este momento; pudiendo cambiar de uno a otro haciendo click en ellos con el cursor. 

También podemos observar en la parte superior derecha, la configuración de red para poder conectarnos a través de WIFI o cableada.

**NOTA**: Para modelos anteriores a la _Raspberry Pi 3_ no trae por defecto wifi necesitara un adaptador USB.

Y por último observaremos el control de volumen y la hora.

### El menú de Raspbian

Este menú que se encuentra en la parte superior izquierda, nos da acceso a los programas instalados en Raspbian. Ya sean los que trae por defecto, o los que hemos instalado nosotros.

![menu]({{ site.url }}/resources/tema3/menu.png)

El menú consta de las siguientes partes:

* **Programación**: En este submenú, tendremos acceso a los programas que podremos utilizar para realizar nuestros propios programas.

![programacion]({{ site.url }}/resources/tema3/programacion.png)

* **Oficina**: Conjunto de programas de ofimática; como un procesador de textos, hojas de calculo, presentaciones, bases de datos, etc...

![oficina]({{ site.url }}/resources/tema3/ofimatica.png)

* **Internet**: Conjunto de programas para acceder a internet; como un navegador, cliente de correo y recursos para aprendizaje.

![internet]({{ site.url }}/resources/tema3/internet.png)

* **Juegos**: Conjunto de pequeños juegos como pueden ser el Minecraft o juegos realizados con Python.

![juegos]({{ site.url }}/resources/tema3/juegos.png)

* **Accesorios**: Conjunto de programas accesorios como puede ser la calculadora, o el lector de PDFs.

### Configuracion de la Raspberry Pi

Tras ver los programas que tiene preinstalados la Raspberry Pi, vamos a pararnos en ver su configuración. Para acceder a la configuración de la Raspberry Pi, iremos al menú  _preferencias_-> _configuración Raspberry Pi_.

![configuracion]({{ site.url }}/resources/tema3/configuracion.png)

En esta ventana, podremos configurar el nombre de nuestra Raspberry Pi, la clave de nuestro usuario, o que nuestra raspberry Pi inicie directamente en modo gráfico.

También hay otras pestañas como la de interfaces, rendimiento o localización. Seguidamente mostraremos las opciones que contienen.

* **interfaces**: Esta pestaña nos permite activar o desactivar interfaces de conexión con nuestra Raspberry Pi; como puede ser _SSH_ o la interfaz de la camara.

![interfaces]({{ site.url }}/resources/tema3/configuracioninterfaces.png)

* **Rendimiento**: Esta pestaña nos permite modificar el rendimiento de la raspberry Pi. **NOTA**: Usar bajo propio riesgo.

![rendimiento]({{ site.url }}/resources/tema3/configuracionrendimiento.png)

* **localizacion**: En esta última pestaña, contiene los datos de configuración de la localización como el idioma o teclado.

![localizacion]({{ site.url }}/resources/tema3/configuracionlocalizacion.png)

Para terminar la configuración, pulsaremos aceptar y si es necesario, reiniciaremos nuestra raspberry Pi.

### Wifi y Bluetooth

Una de la parte importante, es poder configurar el Wifi o Bluetooth de nuestra Raspberry Pi. Por defecto los modelos anteriores a la _Raspberry Pi 3_ necesitaban adaptadores USB para poder tener WIfi o Bluetooth. 

**Wifi**

Para poder conectarnos a una wifi, utilizaremos el menu superior izquierda que tiene un icono de unos ordenadores conectados en red. al pulsar aquí, veremos la lista de redes inalambricas disponibles.

![wifi]({{ site.url }}/resources/tema3/wifi.png)

Para conectarnos a una, simplemente haremos click en ella e introduciremos la contraseña de esta. Si es correcta, se conectará nuestra Raspberry Pi.

![wifipass]({{ site.url }}/resources/tema3/wifipass.png)

Una vez hemos visto la conexión por wifi, pasaremos a ver la conexión por Bluetooth.

**Bluetooth**

Por defecto Raspberry Pi, no tiene un cliente gráfico para la comunicación Bluetooth. Es por esto que utilizaremos la consola de comandos y en concreto el comando _bluetoothctl_.


