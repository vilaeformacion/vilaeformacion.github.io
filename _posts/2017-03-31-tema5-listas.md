---
layout: post
title:  "Tema 5: Listas"
date:   2017-03-31 00:05:00
curso: 6
categories: python,listas
---

En la anterior lección, hemos visto como utilizar los bucles pero hemos visto también que existen las listas. Las listas en python, permiten almacenar una colección de objetos. Por ejemplo; si queremos almacenar 20 numeros no es necesario crear 20 variables. Por eso se utilizan las listas.

```python
a1=1
a2=2
a3=3
...
a8=8
```

```python
a=[1,2,3,4,5,6,7,8]
# Aunque en python esto es equivalente a

a=range(1,8)
```

Las listas son colecciones de objetos mutables. Por lo que podemos cambiar su valor a partir de un indice númerico. Este indice numérico permite acceder a las posiciones de la lista. El indice numérico de una lista, siempre empieza por 0. Es importante saber este dato ya que si el indice queda fuera de los limites de la lista, nos dara un error. Además este indice siempre llegará hasta n-1 donde n  es el numero de posiciones.

En python para crear una lista usaremos los caracteres '[' y ']' los cuales definen el contenido separados por comas.

```python

a= [2,3,4]

```

Las listas pueden ser recorridas por un bucle ```for```.

```python
for n in [2,3,4]:
    print(n)
```

Podemos saber la longitud de una lista en python por el uso de la función ```len()``` esta función nos permite saber el número de elementos de una lista.

```python
a=[1,2,3,4]
print len(a)
4
```
Para acceder a una posición de una lista usaremos el operador '[]' el cual especificamos el indice en su interior.

```python
a=[1,2,3,5,6]
a[0]
1
a[4]
6
```

Además, podemos crear sublistas gracias al operador ':'; el cual nos permite obener una sublista a partir de uno o dos limites. Si no se indica ningun valor en uno de los valores se tomara desde el primer elemento o desde el último.

```python
a=[3,4,4,5,6,7]
a[1:3]
[4,4,5]
a[3:4]
[6,7]
a[:3]
[3,4,4]
a[3:]
[4,5,6,7]
```

Existen una serie de funciones que utilizan las listas que veremos a continuación.

|   **Función**|    **Descripción**
|   ```len()```|   retorna la longitud de una lista
|   ```max()```|   retorna el maximo de una lista
|   ```min()```|   retorna la minimo de una lista
|   ```cmp()```|   compara dos listas

Una vez vistas las funciones básicas de la listas veremos otras funciones que pueden utilizarse.

|   **Función**|    **Descripción**
|   ```list.append(a)```|   Añade un elemento al final de la lista
|   ```list.count(a)```|   retorna el indice de la primera posición donde aparece el elemento.
|   ```list.reverse()```|   invierte la posicion
|   ```list.sort()```|   Ordena la lista
|   ```list1+list2```|   Concatena la listas haciendo una lista con ambas.

Con estas funciones y tras ver como funciona una lista, vamos a pasar a ver los ejercicios.

**NOTA**: Recuerda que una cadena de caracteres se considera una lista de caracteres.

### Ejercicios

1. A partir de una frase, contar las vocales.
2. A partir de una lista de 10 elementos, retornar el mayor y el menor de ambos.
3. A partir de una lista de 20 elementos, retornas la media de estos.

### Referencias

* [Listas en Python](https://www.tutorialspoint.com/python/python_lists.htm)
* [Tutorial de cadenas de caracteres](https://docs.python.org/2/library/string.html)