---
layout: post
title:  "Tema 4: Sistema de Archivos en Linux"
date:   2016-03-21 10:00:00
curso: 1
categories: escritorio, raspbian
---

Tras el anterior tema sobre el escritorio Raspbian y los programas que trae, vamos a hablar de los archivos en Linux y como se tratan en este sistema operativo. 

En este tema, aprenderemos como esta compuesto un sistema Linux y que partes importantes podemos encontrar.

### Archivos en Linux

Para comenzar, definiremos que es un fichero en Linux; un fichero es una colección de datos que se agrupan con un nombre y unas propiedades. En linux todos los dispositivos, controladores, programas, carpetas, etc... son archivos. Los cuales tendran un contenido y unas propiedades características.

En Raspbian podemos acceder a todos los ficheros desde el explorador de ficheros que podemos acceder desde el acceso directo que tenemos en la parte superior; con el icono de un archivador.![iconofichros]({{ site.url }}/resources/tema4/iconoficheros.png)

![exploradorarchivos]({{ site.url }}/resources/tema4/ficheros.png)

En esta ventana podemos ver en primer lugar los ficheros del directorio donde nos encontremos que aparecerá en el titulo seguidamente veremos los ficheros que podemos abrir haciendo doble click.

Tras ver como manejarnos en el explorador de ficheros, vamos a definir como esta estructurado el sistema de ficheros de un sistema Linux. Ya que difiere del conocido sistema de ficheros Windows.

Todos los sistemas Linux, comienzan por una carpeta especial llamada **/** o Carpeta Raiz. De esta carpeta, es desde donde todos los ficheros y carpetas dependeran. ya que un sistema linux se organiza en carpetas y ficheros.

Una carpeta es un fichero especial que contiene ficheros u otras carpetas pudiendo así organizar mejor la información.

![carpetaslinux]({{ site.url }}/resources/tema4/carpetaslinux.png)

Como podemos ver en la anterior figura, todos los ficheros y carpetas se organizan en forma de arbol de manera que podemos acceder a cualquier fichero a través de su ruta en el arbol de directorios.

Seguidamente vamos a ver una serie de carpetas especiales del sistema, para poder conocer mejor el arbol de directorios de un sistema Linux. EN este caso se trata de la distribución _Raspbian_ por lo que en otras distribuciones puede cambiar su estructura.

### Carpeta Raiz /

Como hemos mencionado antes, la carpeta Raiz o **/**, es la carpeta donde todos los ficheros dependen; a partir de esta carpeta se puede acceder a todo el sistema. De esta carpeta es desde la cual se pueden ver los ficheros de configuración, dispositivos o cualquier programa del sistema.

![carpetaraiz]({{ site.url }}/resources/tema4/ficheros.png)

### /home

Esta carpeta es la carpeta donde guardaran los ficheros los usuarios. Linux es un sistema multiusuario por lo que cada usuario tendrá su carpeta que solo el y el administrador (conocido como _root_) puede acceder. dentro de la carpeta _Home_ encontrará otras carpetas una por cada usuario.

**NOTA**: en Raspbian el usuario por defecto es Pi. por lo que en la carpeta home encontrará una carpeta llamada Pi.

![home]({{ site.url }}/resources/tema4/home.png)

### /var

Esta carpeta contiene los ficheros especiales para el administrador; como pueden ser los logs del sistema(registros), información de los servidores, etc...

![var]({{ site.url }}/resources/tema4/var.png)

### /proc

Contienen ficheros que envian o reciben información del núcleo de linux; como por ejemplo información del procesador.

![proc]({{ site.url }}/resources/tema4/proc.png)

### /etc

Contiene archivos con la configuración de programas o utilidades para la administración.

![etc]({{ site.url }}/resources/tema4/etc.png)

### Permisos de archivo

Tras ver las carpetas más importantes de un sistema linux, vamos a ver las propiedades de un fichero y sus permisos. Los permisos de un fichero, definen que usuarios tienen acceso a este y que operaciones pueden realizar.

Todo fichero en linux, tiene un usuario al que pertenece y un grupo al que pertenece también. Por ejemplo si nuestro usuario es _pi_ los ficheros que tenga tendran asignados a este usuario los permisos pertinentes.

Todo fichero tiene asociadas 3 operaciones que puede realizarse con él. El primero es que pueda leerse, el segundo que pueda escribir en él, y el último, es que se pueda ejecutar operaciones con él(como por ejemplo un programa).

Sabiendo esto, en linux se pueden establecer una serie de permisos con respecto al usuario al que pertenece, a los usuarios que pertenezcan al mismo grupo y por último a otros usuarios.

![permisostabla]({{ site.url }}/resources/tema4/permisostabla.png)


Como podemos ver en la tabla anterior, el fichero tiene todos los permisos para el usuario al que pertenece, solo lectura para el usuario que pertenezca al mismo grupo, y para el resto de usuario no tiene ningún permiso.

Podemos ver los permisos de cualquier archivo a traves de las propiedades de este. para ello haremos click derecho en el fichero desde el explorador de archivos y pulsaremos la opción de propiedades.

![permisos]({{ site.url }}/resources/tema4/permisos.png)

Podemos observar a quien pertenece, a que grupo pertenece y los permisos que tiene.

Si cambiamos los permisos y pulsamos aceptar se cambiarán dichos permisos.

**NOTA:** Hay que tener cuidado a la hora de cambiar los permisos ya que podemos dejar el sistema inutilizado.

En posteriores temas, veremos los permisos de usuario a través de la consola de comandos.

### Referencias

* [carpetas importantes linux](http://mural.uv.es/oshuso/823_directorios_ms_importantes_en_linux.html)
* [permisos linux](http://www.ite.educacion.es/formacion/materiales/85/cd/linux/m1/permisos_de_archivos_y_carpetas.html)
* [Booleanbite](http://booleanbite.com)