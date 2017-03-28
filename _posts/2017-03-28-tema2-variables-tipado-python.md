---
layout: post
title:  "Tema 2: Variables y Tipado Python"
date:   2017-03-28 00:03:00
curso: 6
categories: python,variable, tipado
---

Tras ver una introducción a Python y tener todo listo, vamos a mostrar en este segundo tema como utilizar los operadores básicos de Python y como usar variables para crear nuestros programas.

En primer lugar, vamos a mostrar los operadores matemáticos de Python:

|   **Operador**|   **Descripción**
|   +|  suma
|   -|  resta
|   *|  producto
|   /|  Cociente
|   %|  módulo (resto)
|   //| Cociente entero

Estos son los operadores que podemos utilizar en Python; como podemos ver en estos ejemplos:

```python
>>>2+2
4
>>>2-2
0
```

Antes de continuar, es bueno aprender a documentar nuestros programas; esto se realiza  a través de comentarios. De forma que si ponemos algo en comentario no se tendrá en cuenta para la ejecución del programa. O podemos añadir anotaciones para entender este. Una buena documentación, es importante a la hora de realizar desarrollos.

```python
# Comentario de Línea; todo lo que este en esta línea es un comentario
```

```python
'''
Comentario de bloque; todo lo que este entre el triple caracter ' sera comentario
''' 
```

Tras observar los comentarios y los operadores matemáticos vamos a mostrar los operadores de Comparación; ya que en programación, a veces será necesario comparar valores para decidir sobre nuestro programa u obtener conclusiones.

|   **Operador**|  **Descripción**
|   >|  Mayor que
|   <|  Menor que
|   >=| Mayor o igual que
|   <=| Menor o igual que
|   ==| Igual que
|   !=| Distinto de

Estos operadores nos permitiran obtener un valor Booleano. Un Valor Booleano es aquel que tiene 2 valores; verdadero(```True```) o falso(```False```). Por ejemplo:

```python
>>> 2>1
False
>>> 2==2
True
>>> 1<2
True
```

Tras ver los operadores de Comparación, podemos pasar a mostrar los operadores Lógicos; que nos permitiran combinar condiciones Booleanas. Esto se realiza con 3 operadores. Que veremos por separado; mostrando sus Tablas de Verdad.

**Operador and**

El operador and, solo es verdadero(True) si todas las condiciones son verdaderas.

|   | **True**| **False**
|   **True**|   True|   False
|   **False**|  False|   False

**Operador Or**

El operador or, solo es falso(False) si todas las condiciones son Falsas.

|   | **True**| **False**
|   **True**|   True|   True
|   **False**|  True|   False

Tras ver los operadores de comparación y lógicos, vamos a mostrar como usar variables en Python.

### Variables

Las variables en un lenguaje de programación, nos permiten almacenar un valor o un dato. Son importantes a la hora de programas ya que nos permitiran hacer nuestro código más legible por lo que elegir un buen nombre es importante. En python podemos usar variables de forma que tienen un nombre y un valor.

```python
a=1
```

'a' es una variable que almacena el valor '1'. De forma que a en dicho momento vale 1. Para crear una variable en python, solo tenemos que ponerle un nombre. Las reglas de nombrado de Python especifican que el nombre de una variable se compone de 1 letra, seguida de 0 o más letras, números o subrayados. Nunca pueden empezar por un número. Además, python distingue entre mayusculas y minúsculas.

```python
nombre='aaa'# variable de tipo cadena de caracteres
Nombre='aaa'# otra variable ya que no es el mismo nombre.
2aaa=2 # Error no puede empezar por nombre.
```

Otra parte importante de un lenguaje de programación, es el tipo que almacena esa variable. En otros lenguajes de programación como Java, las variables deben tener explicitamente un tipo; mientras que en Python, esto no es necesario.

```java
String a="hola"; //En java debemos establecer el tipo de dato.
```

```python
a='hola' # En python esto no es necesario
```

En python el tipo se comprueba en tiempo de ejecución, es decir que una variable puede cambiar de tipo mientras el programa se esta ejecutando. Por ejemplo:

```python
a=1 # Tipo Entero
a=1.0 #Tipo Decimal
a='1' #Tipo Cadena
a=True # Tipo Booleano
```

Tras ver el tipado dinámico de Python, vamos a mostrar un ejemplo de programa real para que puedas ejecutarlo en tu interprete python.

```python
'''
Este programa calcula el area de un cuadrado
'''
lado = 2.0
area = lado**2 # Este es otro operador matemático indica potencia; en este caso estamos elevando lado al cuadrado.
print("El area de un cuadrado de lado "+str(lado)+" es "+str(area))
```

Con este pequeño script, podemos calcular el area de un cuadrado. Para ejecutar este script lo guardaremos en un fichero de texto y lo llamaremos _area.py_. Tras esto abriremos una consola de comandos y ejecutaremos el siguiente comando.

```bash
$ python area.py
El area de un cuadrado de lado 2.0 es 4.0
```

Os habreis fijado el uso de la función _str_. Esto es necesario para poder transformar el valor de una variable decimal, a un valor de cadena de texto. Existen una serie de funciones que nos permiten transformar estos valores entre ellos.

|   **Función**|    **Descripción**
| str(a)|  Convertir a cadena de caracteresTrue
| int(a)|  Convertir a número entero
| long(a)|  Convertir a número entero largo
| float(a)|  Convertir a número decimal

Tras ver las funciones de conversión y como funciona el tipado, damos por concluida esta lección. Seguidamente dejamos algunos ejercicios.

### Ejercicios

1. Crear un programa que muestre el IGIC de una cantidad(IGIC:7%)
2. Crear un programa que calcule el area de un circulo. Sabiendo que PI=3.141592
3. Crear un programa que muestre el resto de una division entera.


### Referencias

* [Python Documentación Oficial](https://www.python.org/)
* [Presentación Introducción a Python](http://slides.com/zerasul/python#/)

