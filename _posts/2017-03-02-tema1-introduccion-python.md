---
layout: post
title:  "Tema 1: Introducción a Python"
date:   2017-03-02 00:03:00
curso: 6
categories: python,historia
---

En este primer tema aprenderemos a crear nuestro primer programa, utilizando el lenguaje de programación python. Comenzaremos por explicar que es la programación y la historia del lenguaje de programación python.

Mucha gente cuando comienza con la programación, le cuesta mucho comprender los conceptos de la propia programación. Por lo que este primer tema trata de suavizar ese primer contacto con la programación; de manera que aprendamos algunas ordenes basicas y conceptos de la que se trata en programación.

En primer lugar habras oido hablar de la expresión de que los _"programadores estan locos"_; esto es debido a que mucha gente no comprende la programación o como funciona esta. Por eso este primer tema para quitar ese miedo.

Lo primero que tenemos que comprender, es como funciona un programa de ordenador. Este simplemente es una serie de instrucciones que realizan una tarea. Esto se le llama _Algoritmo_. Un Algoritmo, permite realizar una tarea por medio de una serie de instrucciones.

Por ejemplo; supongamos que queremos _Freir un huevo_. Podemos pedirselo a nuestro amigo "Adrian"; o podemos hacerlo nosotros mismos por medio de una serie de pasos para crear la receta; por ejemplo:

1. Coger una sarten, un huevo, espumedera y aceite.
2. Vertir aceite en la sarten.
3. Poner la sarten al fuego.
4. Cuando el aceite este caliente, romper el huevo y vertir el contenido dentro del aceite.
5. dar algunos golpes con la espumedera al huevo para evitar que se rompa.
6. Cuando este al gusto, retirar el huevo de la sarten con la espumedera y servir en un plato.

estos, pasos que hemos realizado, corresponden al algoritmo de _freir un huevo_. Estas instrucciones, permiten freir un huevo y si transcribimos estas ordenes a un computador tenemos un _Programa informático_ que frie un huevo. Esta transcripcción, se realizaría a través de un lenguaje de programación que en este caso, utilizariamos _Python_.

Python es un lenguaje de programación interpretado cuya filosofía hace hincapié en una sintaxis que favorezca un código legible.  Se trata de un lenguaje de programación multiparadigma, ya que soporta orientación a objetos, programación imperativa y, en menor medida, programación funcional. Es un lenguaje interpretado, usa tipado dinámico y es multiplataforma. Que quiere decir esto, que python permite utilizarse de forma sencilla y es muy facil de comprender ya que se basa en una sintaxis muy sencilla; además es multiplataforma lo que quiere decir, que un programa escrito en python se podrá ejecutar tanto en sistemas Unix, Windows,etc...

Python es un lenguaje interpretado, esto quiere decir, que existe un interprete que es un programa que entiende el python y es quien ejecuta las acciones a realizar; a diferencia de otros lenguajes no interpretados que requieren de un programa especial llamado "compilador" que transforma un programa escrito en un lenguaje a código binario que es lo que entiende nuestro ordenador. Sin embargo con python esto no es necesario.

Por último, python es un lenguaje de tipado dinámico; aunque esto lo veremos bien en el segundo tema, hay lenguajes que requieren que definamos que "datos" vamos a utilizar. 

Seguidamente estudiaremos la historia de Python.

Python fue un lenguaje de programación que apareció en 1981; fue creado por Guido van Rossum en el centro de matemáticas e Informática de los paises bajos(CWI); aunque mucha gente cree que el nombre de python viene por el reptil de tal nombre(en inglés); sin embargo, el nombre de Python, viene por los humoristas britanicos Monty Python. Este lenguaje apareció su primera versión estable por 1994 a manos de su autor, tras varios años, python 2.1 fue librerado por la Python Software Fundation License. Ha continuado creciendo hasta hoy en día con la versión 3.6.

Tras ver un poco de la historia del lenguaje de programación, vamos a pasar a instalar y crear nuestro primer programa en python.

### Instalación de Python

En primer lugar, vamos a instalar el interprete Python. Para los Sistemas Operativos más conocidos:

*  Windows:

1. Nos vamos a la dirección de [descargas](https://www.python.org/downloads/release/python-360/). **NOTA**: La versión actual es la 3.6.0.
2. Descargamos el instalador correspondiente a nuestra arquitectura (x86 o x64). y descargaremos el _executable Installer_.
3. Seguimos las instrucciones en pantalla.

* MacOs:

1. Nos vamos a la dirección de [descargas](https://www.python.org/downloads/release/python-360/). **NOTA**: La versión actual es la 3.6.0.
2. Descargamos el instalador correspondiente a MacOs.
3. Seguimos las instrucciones en pantalla.

* Linux:

**Debian, ubuntu (.deb):**

```bash
$sudo apt-get install python
```

1. Buscamos utilizando el gestor de paquetes apt-get.

**Fedora, centos (.rpm):**

1. buscamos utilizando el gestor de paquetes _yum_:

```bash
$sudo yum install python
```

Una vez instalado, vamos a ejecutar el interprete que para ello utilizaremos el comando ```python```.

**NOTA**: en windows puedes utilizar _Python IDLE_ y mostrara una consola.

![python-shell]({{ site.url}}/resources/python/python-shell.png)

Una vez tenemos la consola abierta, vamos a ejecutar nuestro primer programa en Python. Para ello escribimos lo siguiente:

```python
print('Hola Mundo')
```

**NOTA**: Si tenemos instalada una versión 2.X tendremos que usar esta sintaxis:

```python
print "Hola Mundo"
```

Al pulsar enter veremos lo siguiente:

![python-hola-mundo]({{ site.url}}/resources/python/hola-mundo.png)

 Este es el primer programa en python y es el famoso "Hola Mundo"; simplemente muestra por pantalla un mensaje. por lo que podemos ver la primera instrucción que podemos utilizar en python. 
 La orden ```print``` esta orden muestra un mensaje por pantalla. El mensaje debe estar entre comillas ' '.

 Con esto hemos visto el primer tema; que trata de mostrar como instalar python y para que sirve este. En el próximo tema, mostraremos los operadores de python y veremos algunos ejercicios.

### Referencias

 * [Python (Wikipedia)](https://es.wikipedia.org/wiki/Python)
 * [Python Documentación Oficial](https://www.python.org/)
 * [Presentación Introducción a Python](http://slides.com/zerasul/python#/)