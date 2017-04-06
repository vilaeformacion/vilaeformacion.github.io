---
layout: post
title:  "Tema 8: Orientación a Objetos"
date:   2017-04-06 00:05:00
curso: 6
categories: python,poo,objetos
---

Tras estudiar las estructuras básicas de la programación estructurada usando python, podemos ver el siguiente paso. Que se trata de utilizar el paradigma de la programación a objetos. La programación orientada a objetos es un paradigma que permite modelar objetos que podemos encontrar en el mundo real, en un lenguaje de programación. Permite de manera sencilla representar las características y comportamientos que tienen los objetos del mundo real.

En Python, como lenguaje multiparadigma, es también un lenguaje orientado a objetos; al igual que otros  lenguajes como Java, o C++. En esta lección, vamos a mostrar como se realiza la orientación a objetos y lo aplicaremos al lenguaje python.

La principal caracteristica de la orientación a objetos, es que todo objeto del mundo real, puede tener su representación como "objeto" a través de una definición, llamada _clase_ una clase es una definición de como es un objeto y que comportamiento tiene. Además de que los objetos o clases pueden tener relaciones entre ellos.

![clasecoche]({{ site.url}}/resources/python/clasecoche.png)

Como vemos en la figura anterior, es la clase que representa un coche. Un coche tiene una serie de características que lo definen; además de que tiene una serie de comportamientos que puede realizar. Esto es la definición de una clase que es como esta definido un objeto del mundo real.

Una vez tenemos la clase, si queremos utilizarla como tal tenemos que crear objetos a partir de esta definición para darle las características mas concretas y poder cambiar su comportamiento. Es por esto que existe el concepto de _Objeto_ Que se trata de una particularización de una clase.

![clasecoche]({{ site.url}}/resources/python/cocheobjetos.png)

Tras ver los conceptos de clase y objeto, ya podemos definir otros conceptos que son importantes a la hora de programar orientado a objetos. Se tratan de las propiedades y métodos.

Una _propiedad_ es una característica de la clase que tendrá un valor concreto cuando se instancie un objeto.

Un _método_ es una función que realiza una acción para definir un comportamiento del objeto.

En python, para declarar una clase utilizaremos la palabra reservada _class_; seguido del nombre de esta. Recuerda que debe empezar por Mayuscula según la guia de estilos PEP 8, y nunca empezar por un número. Tras esto añadiremos el caracter : que indica bloque de código por lo que en su interior todo lo que escribamos debe estar indentado. Tras definir la clase debe aparecer la palabra reservada _pass_. Seguidamente mostramos un ejemplo:

```python
class Coche:
    color=''
    marca=''
    modelo=''
    matricula=''

    def arrancar(self):
        print('El coche ha arrancado')

    def parar(self):
        print(' El coche ha parado')

    def acelerar(self):
        print('El coche esta acelerando')

    pass

```

Como vemos en el ejemplo anterior, estamos definiendo la clase Coche la cual tiene una serie de propiedades; como son color, marca, modelo y matricula. Estas propiedades se definen como variables dentro de la clase.
También estamos viendo que hemos definido dentro de la clase una serie de funciones; llamadas métodos los cuales definen el comportamiento de un coche. Vemos que tienen un parámetro especial llamado _self_ esto es un apuntador que podemos utilizar que apunta siempre al propio objeto o a la clase. Esto lo veremos más detenidamente después.

Con esto sabemos ya como definir propiedades y métodos de una clase; sin embargo, para poder utilizarlo, necesitaremos crear objetos o instancias de esta clase. Por lo que crearemos objetos de esta clase. Veremos un ejemplo de como se utilizan los objetos.

```python
coche1= Coche()
coche1.color='blanco'
coche1.marca='kia'
coche1.modelo='Rio'
coche1.matricula='2233HFD'
```

Como hemos visto en el ejemplo anterior hemos definido una variable llamada _coche1_ la cual la hemos asignado un objeto con la llamada a _Coche()_ Esta llamada a una función con el nombre de la clase se llama _instanciación_ y es la llamada a un método especial llamado _constructor_. Después, observamos como utilizamos el operador '.' para acceder a las propiedades del objeto y asignarle un valor. Seguidamente veremos como llamar a métodos de una clase.

```python
coche1=Coche()
>>>coche1.arrancar()
El coche ha arrancado
>>>coche1.parar()
El coche ha parado
>>>coche1.acelerar()
El coche esta acelerando
```

Como vemos utilizamos el mismo operador que para las propiedades y llamamos al método correspondiente. Un aspecto importante es que no pasamos ningún parámetro aunque en la declaración si esta. Esto es por que el parámetro self no es necesario pasarlo.

Seguidamente veremos como crear un método especial llamado __init__ el cual es el constructor de la clase y permite inicializar las propiedades de esta. Vemos un ejemplo con la clase anterior:

```python
class Coche:
    color=''
    marca=''
    modelo=''
    matricula=''

    def __init__(self, color, marca,modelo,matricula):
        self.color=color
        self.marca=marca
        self.modelo=modelo
        self.matricula=matricula

    def arrancar(self):
        print('El coche ha arrancado')

pass

```

Como vemos en el anterior ejemplo tenemos el método __init__ el cual nos permite inicializar los valores de la clase por unos que pasemos por parámetro. Vemos también el uso del parámetro self. Este parámetro permite usar las propiedades y métodos de la clase ya que es un apuntador al propio objeto. Para crear un objeto usando el constructor, lo usaremos como si de una función con el nombre de la clase se tratara. Por ejemplo:

```python
coche1=Coche(color='blanco',marca='Kia',modelo='rio',matricula='22233HFG')
```

Como vemos en el anterior ejemplo pasamos los datos de forma implicita (aunque pueden pasarse de forma explicita también). Con esto ya hemos visto la introducción a la programación orientada a objetos. En la siguiente lección, estudiaremos más características de la Programación Orientada a Objetos.

### Ejercicios

1. Escribe una clase con 2 métodos:
a) Obtener un valor por teclado. utilizar la función raw_input()
b) Mostrar un valor por pantalla.

2. A partir de la clase Coche, haz un programa que permita Almacenar en una lista una serie de Coches. Pista: Utilizar la clase anterior para introducir los datos.

### Referencias

* [Orientación a objetos](http://librosweb.es/libro/python/capitulo_5/programacion_orientada_a_objetos.html)
* [Raw_input](https://showthebytes.wordpress.com/2011/04/13/python-uso-de-input-y-raw_input/)
* [100 Ejercicios Python](https://github.com/zhiwehu/Python-programming-exercises/blob/master/100%2B%20Python%20challenging%20programming%20exercises.txt)