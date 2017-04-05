---
layout: post
title:  "Tema 7: Tuplas y Diccionarios"
date:   2017-04-04 00:05:00
curso: 6
categories: python,tuplas,diccionarios
---

Tras ver las funciones, vamos a ver otra caracteristica de python que son parecidas a las listas. Ya que se tratan de otras estructuras de datos que podemos utilizar para nuestros programas python.

En este tema, veremos las tuplas y los diccionarios. Las tuplas son muy parecidas a las listas; pero su principal diferencia es que son inmutables; es decir, que no pueden ser cambiadas. Para definir una tupla se utilizan los caracteres ( y ).

```python
tupla=(1,2,3,4)
```

Como vemos en el ejemplo anterior tenemos una tupla con 4 elementos; al igual que las listas, una tupla puede accederse a través de un indice. El indice empieza siempre por 0 y llega hasta n-1 donde n es el numero de elementos en la tupla. 

```python
tupla=(1,2,3,4)
>>>tupla[0]
1
```

Al igual que las listas, las tuplas utilizan el operador [:]; el cual indica el limite inferior y superior para obtener una subtupla.
```python
tupla=(1,2,3,4)
>>>tupla[0:2]
(1,2,3)
```

Además, podemos usar un bucle for para recorrerla.

```python
for num in tupla:
    print(num)

```

Con esto hemos visto las tuplas; ahora hablaremos de los diccionarios. Los diccionarios en python, son estructuras de datos basados en una clave y un valor. Estos permiten almacenar una cantidad de datos a partir de una clave. Estos se definen por los simbolos { y }.

```python
diccionario={}
diccionario['nombre']='zerasul'
```
En el ejemplo anterior, vemos que se inicia un diccionario vacio; y después asignamos a la clave 'nombre' el valor 'zerasul'. Si accedemos a dicha posición del diccionario, nos deolvera dicho valor.

```python
>>>diccionario['nombre']
'zerasul'
```

Por último, podemos inicializar un diccionario con distintos valores iniciales.

```python
diccionario={ 'nombre': 'zerasul','clase': 'Archimago subidito'}
```

Con esto ya hemos terminado esta lección y podemos pasar a la siguiente lección. La Programación Orientada a Objetos.

### Ejercicios
1. Crear un programa que permita buscar un elemento en una tupla.
2. Crear un programa que permita mostrar por pantalla los elementos de una tupla.

### Referencias

* [Tuplas Python](http://librosweb.es/libro/algoritmos_python/capitulo_7/tuplas.html)
* [Tuplas Ejercicios](http://www.w3resource.com/python-exercises/tuple/)
