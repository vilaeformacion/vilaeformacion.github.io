---
layout: post
title:  "Tema 6: Funciones"
date:   2017-04-04 00:05:00
curso: 6
categories: python,funciones
---

Hasta ahora, nuestros programas solo estaban compuestos de un programa monolitico que contenia todas las instrucciones; sin embargo, muchas veces es necesario dividir nuestros programas en subtareas para reutilizar código o para hacer más legible nuestro programa. Es por esto que en python existen las funciones.

Una función en Python es un subprograma que realiza una tarea concreta a partir de una serie de parámetros y que puede devolver un resultado. Es importante que nuestro programa este dividido correctamente; ya que permitirá que sea modificado más facilmente y además permitirá que sea reutilizado.

En python se pueden definir funciones con la palabra reservada _def_ seguido de un nombre que será el nombre de la función. Al igual que los nombres de las variables, las funciones no pueden empezar por numero sino por un caracter seguido de varios caracteres más. 

Aunque no es estrictamente necesario, el nombre de una función debe empezar por una letra minuscula; según dice las guias de estilo de programación Python conocidas como PEP8. Además de que si una función tiene como nombre la unión de dos palabras estas deben estar separadas por el caracter subrayado _ . Tras el nombre de la función, debe ir unos parentesis y en estos debe ir una lista de parametros(o vacio si no tiene ninguna) de manera que cada parametro debe ir separado por una coma; por último debe ir el caracter : que indica un bloque de código por lo que todo código que pertenezca a una función debe ir indentado. Os dejo un ejemplo:

```python
def suma(a,b):
    return a+b
```

Como podemos ver en la funcion anterior, comenzamos por la palabra _def_; indicando que es una definición de función; después seguimos con el nombre de esta y entre parentesis una lista de 2 parámetros; tras el cierre del paréntesis vemos los dos puntos. Por lo que añadimos una tabulación al código de la función. Vemos que en cuerpo de la función existe una palabra reservada _return_ la cual nos indica que va a devolver un resultado de la función. En este caso, la suma de a+b; los cuales son los parámetros que le hemos pasado(En este caso a y b son consideradas dos variables).

Con esto hemos definido nuestra función; pero se nos falta un paso importante y es poder usarla en nuestro programa. El uso de una función tiene como nombre llamada; mientras que el definir la función tiene como nombre declaración de la función. Para llamar a una función, simplemente ponemos el nombre de esta y entre parentesis los valores de los parametros que tendrá. Por ejemplo.

```python
>>> suma(2,2)
4
```
Como hemos visto en el ejemplo anterior al llamar a ```suma(2,2)``` nos ha devuelto el valor 4; siendo este el resultado de la llamada a la función. Es importante pasar correctamente los valores de los parámetros ya que en python cuenta el orden de estos. Además, en python se puede añadir a la llamada la definición de los nombres de los parametros. Por ejemplo.

```python
>>> suma(a=2,b=2)
4
```

Como vemos en ejemplo anterior, pasamos los valores pero indicando a que parámetro corresponde; de esta manera da el mismo valor.

Otro aspecto importante en python, es que podemos dar valores por defecto a los parámetros para que en caso de no ser pasado, este tome un valor. Por ejemplo.

```python
 def suma2(a,b=2):
	return a+b
```

En este caso, la función suma2 tiene el parámetro b un valor por defecto de dos; por lo que al hacer la llamada ```suma2(2)``` debería devolver el mismo resultado.

```python
>>> suma2(2)
4
```

Es importante tener esto en cuenta ya que así podemos definir una función para distintos casos a partir de los parámetros que le pasemos. Más adelante en la Programación Orientada a Objetos retomaremos el uso de funciones especiales llamadas métodos.

En el próximo tema hablaremos de Tuplas y Diccionarios para terminar de hablar de las estructuras de datos en Python.

### Ejercicios

1. A partir de una lista que será pasada por parámetro, devolver la suma de todos los números.
2. Escribir una función en Python que reciba una cadena y nos diga el número de vocales que tiene.
3. Escribir una función en Python que indique si un número es primo o no.

### Referencias

* [Funciones Python](https://www.tutorialspoint.com/python/python_functions.htm)
* [Tutorial Interactivo sobre funciones](http://www.learnpython.org/es/Functions)