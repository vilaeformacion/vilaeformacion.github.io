---
layout: post
title:  "Tema 3: Condicionales"
date:   2017-03-28 00:03:00
curso: 6
categories: python,condicionales,if
---

Tras ver como utilizar las variables y el tipado, necesitaremos aprender a utilizar las estructuras de control; estas permiten manejar el flujo de nuestro programa y poder hacer decisiones sobre este en función de distintas condiciones. En este apartado enseñaremos las condicionales simples y multiples en el lenguaje python.

Pero antes de empezar hay que explicar que mientras en otros lenguajes de programación la indentación no es algo extrictamente necesario para su compilación, en python esta es muy importante ya que la indentación(tabulaciones para indicar bloques de codigo) es necesaria. Por ejemplo:

```java

if(a>1){
b=1;//La indentación No es necesaria aunque suele usarse para mejorar la legibilidad.
}
```

Como vemos en el anterior fragmento de código Java, no es necesaria la indentación después de la llave. Sin embargo en python:

```python
if a>1:
    b=1
```

Si la indentación no estuviese, daría un error de compilación. 

**Nota:** La indentación debe hacerse con tabuladores no con espacios.

Tras ver esto, vamos a presentar la condicional simple. Se trata de una estructura de control que comprueba una condición; y si esta se cumple, se realizara una serie de acciones y si en caso contrario no, se realizarán otras.

![python-if]({{ site.url}}/resources/python/if.png)

Como podemos ver en el diagrama de flujo anterior, si se cumple una condición, se realiza una tarea, sino, realizará otra o no. Seguidamente mostramos como se realiza una condicional simple en Python.

```python
if a>1:
    b=1
else:
    b=2
```

Como podeis ver se compone de una primera condicion que utilizamos el operador Mayor que para comprobarla; si dicha comparación fuese verdadera la variable B valdría 1. En caso contrario, la variable B valdría 2. Esta es la condición simple y permite modificar el flujo de nuestro programa.

Existe otro tipo de condicional, que se llama condicional multiple. Este tipo de condicional permite comparar varias condiciones a la vez; y elegir la condición que mejor convenga. Esto se realiza con la estructura elif(else if). Dejamos un ejemplo de su uso.

```python
if a>1:
    b=1
elif a<1 and a >=0:
    b=0
else
    b=-1
```

En el anterior caso, existe una condicion que comprueba que la variable a sea mayor que uno. En caso contrario y si es menor que uno pero mayor o igual que 0, la variable b valdrá 0 y en caso contrario, valdrá -1.

Una vez hemos visto las condicionales, pasaremos a ver los bucles en la siguiente lección. A continuación, mostraremos unos ejercicios para realizar.

### Ejercicios

1. A partir de 2 números indicar cual es mayor.
2. Mostrar si un numero es par o impar (Un número es par, si es divisible por 2).
3. Crear un programa que compruebe una edad y muestre si es mayor de edad o no.

### Referencias

* [Python Conditionals](http://www.python-course.eu/conditional_statements.php)