---
layout: post
title:  "Tema 1: Introducción a Arduino"
date:   2016-03-20 00:00:00
curso: 3
categories: arduino, electronica
---

Tras estudiar y comprender los conceptos básicos de la electrónica y ver los componentes más comunes que vamos a utilizar, vamos a pasar a estudiar la placa programable arduino y que aplicaciones podemos realizar con ella.

En esta lección, nos centraremos en una introducción a Arduino estudiando sus componentes y como podemos utilizarla.

## ¿Qué es Arduino?

Arduino es una plataforma de Hardware libre, que sirve para realizar prototipado rápido de proyectos de electrónica; la placa esta basada en un microcontrolador, y un entorno de desarrollo.

Gracias a su bajo coste y sencillez, ha tenido gran éxito y se ha creado una gran comunidad con mucha información.

![arduinouno]({{ site.url }}/resources/arduino/tema1/arduinouno.png)

Arduino comenzó, por el año 2005 gracias a un profesor del instituto IVREA(Italia) Massimo Banzi; creó este microcontrolador como una solución barata para que los estudiantes pudieran crear sus propios proyectos ya que hasta la fecha utilizaban el microcontrolador Basic Stamp que tenía un coste de 100 $. Gracias a Arduino, se abarató el coste a 30 Euros creando una plataforma sencilla de programar, plug & play y que trabajara en las plataformas windows, Linux y Mac Os X. Se repartieron los primeros 300 modelos entre los estudiantes del instituto teniendo un gran éxito.

![primerprototipo]({{ site.url }}/resources/arduino/tema1/primerprototipo.jpg "Primer Prototipo de Arduino por Massimo Banzi")

 Tras este éxito, se juntaron los fundadores de Arduino en 2008 y crearón la marca como tal. Massimo Banzi, David Mellis, David Cuartielles, Tom Igoe y Gianluca Martino fuerón los fundadores de esta plataforma. Creando la plataforma como la conocemos hoy en día. 

![cuartielles]({{ site.url }}/resources/arduino/tema1/cuartielles.jpg "David Cuartielles Uno de los fundadores de Arduino")

En la foto anterior podemos observar a David Cuartielles uno de los fundadores de Arduino. Seguramente ahora encontrará que puede encontrar la marca Genuino y es que en europa se ha realizado un cambio de marca por problemas legales con uno de los fundadores.

Una de las características más importantes de Arduino, es que todos sus componentes son libres y que pueden encontrarse modelos de Arduino compatibles por un coste menor que el original.

Además se han creado muchos accesorios o Shields, que permiten ampliar la funcionalidad de estas placas programables como pueden ser añadirle conectividad a Internet, Bluetooth, etc...

## Modelos de Arduino

Existen ya varios modelos de arduino dependiendo del tipo de proyecto que se este realizando, podemos usar uno u otro; a continuación, se muestra una tabla de algunos de los más utilizados. Aunque podemos encontrar otros modelos más recientes.

![modelos]({{ site.url }}/resources/arduino/tema1/modelos.png)

El módelo más básico de Arduino, es el _Arduino UNO_; esta placa es la más indicada para aquellos que quieran comenzar a utilizar esta plataforma de prototipado ya que tiene unas buenas prestaciones y además, de ser una de las mas versátiles y que permite poder intercambiar el microcontrolador.

![genuinouno]({{ site.url }}/resources/arduino/tema1/genuinouno.jpg "Genuino UNO")

Estas son las características del Arduino UNO.

|	**Características**|	**Valor**	|
|	Memoría SRAM	|	2KB	|
|	Memoría Flash|	32KB	|
|	Memoría EEPROM|	1KB	|
|	Nº Salidas Digitales	|	14	|
|	Nº Entradas Analógicas	|	6	|
|	Microcontrolador	|	Atmel 328p	|

Componentes de un Arduino UNO.

![componentesarduinoUno]({{ site.url }}/resources/arduino/tema1/componentesarduinouno.png)

Como podemos ver en la figura, un Arduino uno, se compone de los siguientes elementos:

* Unas _entradas /Salidas digitales_ con las que podemos realizar el montaje de nuestros circuitos.
* Unas entradas y salidas para alimentar u obtener _alimentación_ para nuestro circuito; el Arduino Uno puede dar corriente de **3.3V** y **5V**. Además de alimentarse por medio de 5V; NUNCA debe alimentarse la entrada **Vin** por encima de 5V.
* Unas _Entradas analógicas_ que reciben un voltaje intermedio y es capaz de medirlo en distintos niveles(en vez de 0 o 1); esto se verá en un tema posterior.
* Una entrada USB por la que programaremos la placa.

**NOTA**: En este apartado se ha estudiado el modelo Arduino UNO; sin embargo, para otros modelos puede cambiar la disposición de los componentes. Compruebe la documentación de su placa arduino o arduino compatible para más información.

## Montaje de un circuito eléctronico con Arduino UNO

Una vez hemos visto el modelo de Arduino UNO, vamos a pasar a realizar un pequeño montaje de un circuito electrónico; es por ello que necesitamos utilizar un nuevo componente que no hemos estudiado hasta ahora. Se trata de la _BreadBoard_ o Placa de prototipado.

![breadboard]({{ site.url }}/resources/arduino/tema1/breadboard.png)

Como podemos observar la breadboard, es una placa con una serie de zocalos donde podremos hacer las conexiones de nuestros circuitos sin necesidad de soldar. 

Las conexiones de la BreadBoard estan conectados usando un patron. Todos los zocalos del interior, estan conectados de manera _vertical_; mientras que las filas superiores e inferiores estan conectados de manera _horizontal_.

![breadboardesquema]({{ site.url }}/resources/arduino/tema1/breadboardesquema.png)

Como podemos ver en el esquema anterior las columnas conectdas a la resistencia, estan interconectadas pero solo para la parte inferior y podemos observar como la fila del - esta coenctado por medio de un cable y vemos como toda la fila esta interconectada.

Una vez hemos comprendido como se interconectan los componentes en una breadboard, vamos a explicar como conectar los componentes en serie y en paralelo.

**Serie**

Un componente esta en serie con respecto a otro, si esta conectado directamente después de él.

![serie]({{ site.url }}/resources/arduino/tema1/serie.png)

**Paralelo**

Un componente esta en paralelo si los 2 estan conectados entre si y coninciden sus terminales de entrada y de salida.

![paralelo]({{ site.url }}/resources/arduino/tema1/paralelo2.png)

## Ejemplo de montaje: Un Led

El primer ejemplo que vamos a realizar, es poder encender un led a partir de nuestro arduino. Para ello, necesitaremos los siguientes componentes.

* 1 Led .
* 1 resistencia 220Ohmios.
* 1 Arduino(En el ejemplo utilizaremos el Arduino Uno).
* Cables para la interconexión.

Seguidamente mostramos el montaje a realizar.

![esquemaled]({{ site.url }}/resources/arduino/tema1/esquemaled.png)

Como podemos ver, conectamos en serie el led junto a la resistencia; esto es debido a que el arduino uno, nos da una intensidad que puede dañar el led; por ello, añadimos una resistencia de 220 Ohmios antes del led. El circuito funciona de la siguiente manera; la salida de 5V alimenta la resistencia que a su vez esta conectada con el led; el cual al recibir la corriente, emite luz(si no esta correctamente conectado, cambiar la polaridad; recordad que la patilla larga siempre es la negativa); después conectamos la salida del led a tierra para cerrar el circuito.

Con esto último, hemos terminado nuestro primer montaje con Arduino; sin embargo, solo hemos realizado un montaje electrónico, y no hemos programado ninguna funcionalidad. Es por ello que necesitaremos utilizar otra de las grandes herramientas que nos da arduino y es su interfaz de programación.

## Arduino IDE

El software Arduino IDE; es un editor de texto que nos permite escribir y subir nuestros programas hechos con arduino. Además permite comunicarnos con la placa por medio de una interfaz serie.

![arduinoide]({{ site.url }}/resources/arduino/tema1/arduino ide.png)

A través de la barra de herramientas podemos manejar las funciones más comunes como el poder verificar nuestro código, subir el programa a la placa o guardar/cargar un nuevo programa.

## Referencia del Lenguaje

Arduino utiliza un lenguaje llamado processing. Processing es un lenguaje de programación basado en Java. El lenguaje es de código abierto que suele ser utilizado en entornos de enseñanza.

Seguidamente se muestra la referencia de este lenguaje.

### Estructura de un programa

en Arduino los programas tienen una estructura determinada por 2 funciones ```setup``` y ```loop```.

|	**Función**	|	**Descripción**	|
|	```void setup()```	|	Función que es llamada cuando se inicia el arduino. Esta funcion solo es llamada una única vez.	|
|	```void loop()```	|	Función que es llamada continuamente en forma de bucle.	|

### Sintaxys

Seguidamente se muestra la sintaxys que tiene un programa para Arduino.

|	**Símbolo**	|	**Descripción**	|
|	```//```	|	Comentario de Línea	|
|	```/* */```	|	Comentario de Bloque	|
|	```{ }```	|	Se usan para definir los bloques de código	|
|	```;```	|	Se usa para terminar una línea de código todas las líneas de código deben terminar con este simbolo	|

### Variables

En el lenguaje de programación Arduino, se utilizan variables para almacenar los datos con los que estemos trabajando.

|	**Tipo**	|	**Descripción**	|
|	```byte```	|	Número entero entre 0 y 255	|
|	```int```	|	Número entero entre -32768 y 32767.	|
|	```long```	|	Número entero entre -2.147.483.648 y 2.147.483.647.	|
|	```float```	|	Número decimal de 4 bytes de tamaño	|
|	```char```	|	Caracter alfanumerico de 1 byte de tamaño	|


### Operadores Aritmeticos

Para poder operar con los datos podemos utilizar los siguientes operadores aritmeticos.

|	**Operador**	|	**Descripción**	|
|	```=```	|	Operador de asignación	|
|	```%```	|	Operador Módulo(Resto)	|
|	```+```	|	Operador Suma	|
|	```-```	|	Operador Resta	|
|	```*```	|	Operador Multiplicación	|
|	```/```	|	Operador División	|

### Operadores de Comparación

|	**Operador**	|	**Descripción**	|
|	```==```	|	Operador igual que.	|
|	```!=```	|	Operador Distinto de. 	|
|	```<```	|	Operador menor que	|
|	```>```	|	Operador Mayor que	|

### Estructuras de control

|	**Estructura**	|	**Descripción**	|
|	```if(<condicion>){}```	|	Ejecuta el bloque de código si se cumple la <condicion>.	|
|	```if(<condicion>){}else{}```	|	Si se cumple la condición se ejecuta el primer bloque de código sino, se ejecuta el segundo.	|
|	```switch(<variable>){ case a: break; case b: break; finally: break;}```	|	En función del valor de la variable se ejecutara el bloque de código asiciado a cada caso. En todo caso se ejecuta el bloque ```finally```.	|	
|	```for(<inicializacion>;<condicion>;pasos){}```	|	Este bucle ejecuta en primer lugar el bloque inicializacion; tras esto, ejecuta en bucle el bloque de código interno y en cada iteración ejecuta el bloque pasos.	|
|	```while(<condicion>){}```	|	bucle que se ejecuta mientras se cumpla la condición.	|

### Funciones Digitales

Estas son las funciones para poder interactuar con las Entradas/Salidas digitales de nuestro Arduino.

|	**Función**	|	**Descripción**	|
|	```pinMode(pin, modo)```	|	Esta función establece el modo del pin correspondiente a un modo que puede ser ```OUTPUT```,```INPUT```, ```INPUT_PULLUP```.	|
|	```digitalWrite(pin, valor)```	|	Esta función escribe en un pin digital determinado. Los valores que acepta es ```HIGH```(1) o ```LOW``` (0).	|
|	```digitalRead(pin)```	|	Función que devuelve ```HIGH```(1) o ```LOW``` (0) si esta activo el pin determinado.	|

### Funciones Analógicas

Estas son las funciones para poder interactuar con las Entradas/Salidas analógicas de nuestro Arduino.

|	**Función**	|	**Descripción**	|
|	```analogRead(pin)```	|	Lee el valor analógico de una entrada anlógica. Este valor estará comprendido entre 0 y 1023.	|
|	```analogWrite(pin,valor)```	|	Escribe el valor analógico en una salida analógica(debe ser PWM) solo acepta valores entre 0 y 255.	|

## Referencias

1. [Página Oficial Arduino](https://www.arduino.cc/)
2. [Historia de Genuino](http://booleanbite.com/web/genuinamente-arduino/)
3. [Referencia Arduino](https://www.arduino.cc/en/Reference/HomePage)