---
layout: post
title:  "Tema 4: Bucles"
date:   2017-03-31 00:03:00
curso: 6
categories: python,bucles,if
---

Tras ver las condicionales en la lección anterior, vamos a mostrar otras estructuras de control que son necesarias a la hora de realizar nuestros desarrollos. Estas estructuras de control son los bucles.

Un bucle, es una estructura de control que permite repetir una serie de acciones en función de una condicion u otros factores. 

![bucle]({{ site.url}}/resources/python/bucle.png)

Como podemos ver en la figura anterior, un bucle consta de una condición; que si se cumple, realiza una acción y regresa a comprobar la condición; si se sigue cumpliendo, repite la acción; si la condición deja de cumplirse, se parara el bucle.

Es importante comprender el concepto de bucle ya que es muy importante a la hora de programar.

La condición del bucle, es importante ya que si no esta correctamente creada o la lógica no esta bien construida, pueden ocurrir un "bucle imposible" o un "bucle infinito".
* Un bucle imposible, es un bucle cuya condición, nunca va a ocurrir por lo que nunca se ejecutaria.
* Un bucle infinito es un bucle cuya condición, siempre se cumple por lo que jamas saldrá de el y podrán ocurrir problemas de memoria o desbordamiento.

En python existen distintos tipos de bucles; vamos a ver 2 tipos; los ```while``` y los ```for```.

El bucle ```while``` es un bucle que se ejecuta "mientras" se cumpla una condición.

```python

while a>1:
    a-=1
```

El bucle anterior se ejecutara mientras la variable a sea mayor que uno. Cuando esta sea igual el bucle dejará de ejecutarse. Recuerda que es importante que la condición se cumpla y deje de cumplirse llegado su momento.

El otro bucle importante es el bucle ```for``` este bucle nos permite iterar; ya sea en una serie de numeros como en una cadena de caracteres o una colección de objetos.

El bucle for no tiene una condición como tal sino que recorrera una "lista" de objetos hasta terminarla.

```python
for n in range(1,10):
    print(n)
```

En el anterior ejemplo vemos que hay una variable n que tomara el valor en cada iteración del bucle del rango que se ha definido. En este caso del 1 al 10. Por lo que n tomará el valor 1,2,3,4,etc...

**NOTA**: ```range(1,10)``` es una función de python que permite crear un rango entre 2 limites.

Es importante decir que el bucle for iterara en cualquier colección de objetos; por ejemplo, una cadena de caracteres. AUnque no se ha mencionado en este curso, una cadena de caracteres es una sucesión de caracteres que estan dentro de los caracteres ' '. Por ejemplo ``` 'hola' ``` es una cadena de caracteres. Esta cadena de caracteres se interpreta como una colección de caracteres por lo que un bucle for puede iterarlo.

```python
for a in 'hola que tal':
    print(a+'\n') # el caracter \ n corresponde al salto de linea
```

Otro aspecto importante a la hora de usar el bucle for, es el uso de listas; aunque lo veremos en la siguiente lección, una lista den python es una colección de objetos mutable.

```python
a=['banana','pera','manzana']
for n in a:
    print(a)
```

Con todo esto, ya hemos visto los bucles y en la siguiente lección, veremos las listas y su uso.

### Ejercicios

1. Obtener los 100 primeros numeros divisibles por 5.
2. Recorrer una cadena y contar sus posiciones.
3. Realizar la sucesión de pibonacci de los 10 primeros numeros. La sucesión de pibonacci es aquella que para 1 y 0 vale 1. para el resto de valores se calculan multiplicando los anteriores.

### Rerencias

* [Bucles en Python](https://www.tutorialspoint.com/python/python_loops.htm)
* [Cadenas en Python](https://docs.python.org/2/library/string.html)
* [Sucesión de pibonacci](https://es.wikipedia.org/wiki/Sucesi%C3%B3n_de_Fibonacci)

