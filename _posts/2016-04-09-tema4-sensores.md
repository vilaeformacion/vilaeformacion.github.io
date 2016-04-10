---
layout: post
title:  "Tema 4: Sensores"
date:   2016-04-01 00:00:00
curso: 3
categories: arduino, electronica
---

Tras ver las entradas y salidas analógicas, ya podemos pasar a utilizar distintos sensores que podemos encontrar para arduino como el sensor de humedad o de ultrasonidos. Normalmente cada sensor tiene asociada una librería que nos da la funcionalidad extra para poder utilizar este tipo de sensores.

Existen distintos tipos de sensores en función del protocolo que utilizan y como se realiza la conexión de estos. En este tema veremos el ejemplo del sensor de Humedad y temperatura _DHT11_; este sensor nos muestra la humedad y la temperatura ambiente actual.

### Sensor DHT11

Los sensores _DHT_ permiten obtener la humedad y la temperatura ambiente. Existen distintos modelos que nos permiten dar con mayor o menos precisión los datos.

![dht11]({{site.url}}/resources/arduino/tema4/dht11.png)

Seguidamente se muestra el montaje de un arduino UNO con un sensor DHT11 conectado. 

![montajedht]({{site.url}}/resources/arduino/tema4/dht11ejemplo.png)

Antes de pasar a realizar la programación, vamos a mostrar una serie de funciones que necesitaremos para comunicar nuestro arduino, con el pc a través pro ejemplo del propio cable USB con el que cargarmos el programa.

Esta comunicación se realiza a través del puerto serie. utilizando el objeto _Serial_. Seguidamente mostramos una tabla con las funciones del objeto _Serial_.

|	**Función**	|	**Descripción**	|
|	```Serial.begin()```	|	Inicializa el puerto serie; esta función recibe por parámetro la velocidad de comunicación en baudios; pudiendo ser ```2400```,```4800```,```9600```,```14900```	|
|	```Serial.print()```	|	Manda un mensaje por el puerto serie al pc.	|
|	```Serial.read()```	|	Lee un caracter del puerto serie que sera enviado desde el PC.	|
|	```Serial.println()```	|	Manda un mensaje por el pueerto serie al PC y además un salto de linea	|
|	```Serial.available()```	|	Comprueba si hay caracteres esperando a ser leidos.	|

Una vez hemos visto estas funciones, vamos a mostrar el programa que hay que realizar en el ide de arduino.

Pero antes de eso, tenemos que descargarnos la librería que nos permitirá leer de un sensor DHT. Esta librería se llama _dhtlib_ y podemos descargarla en el siguiente [enlace]({{site.url}}/resources/arduino/tema4/dhtlib.zip "Libreria DHTLib").	

Tras descargar esta librería, tenemos que añadirlo a nuestro IDE Arduino. Para ello, vamos a la opción _sketch->Importar Libreria...->Add Library..._.

![libreria]({{site.url}}/resources/arduino/tema4/libreria.png)

Añadiremos el archivo .zip descargado y pasará a estar disponible para todos nuestros proyectos.

Seguidamente crearemos un nuevo programa y añadiremos la librería dhtlib; accediendo al anterior menú y seleccionandola.

Seguidamente se muestra el programa a realizar y que se muestra como debe usarse la librería.

```c
#include <dht.h>

dht DHT;
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
  DHT.read11(12);
  Serial.print("Temp: ");
  Serial.println(DHT.temperature,1);
  Serial.print("Humidity: ");
  Serial.println(DHT.humidity,1);
  delay(5000);
}
```

Para probar nuestro programa lo cargaremos en nuestra placa arduino, y utilizaremos el botón de la lupa de la derecha. Esto abrirá el serial Monitor.

![serialmonitor]({{site.url}}/resources/arduino/tema4/serialmonitor.png)

Observaremos que en el monitor serie se muestra los datos de la humedad y temperatura.

---
* [DHTLib](http://playground.arduino.cc/Main/DHTLib)
* [Serial](https://www.arduino.cc/en/Reference/Serial)
* [Booleanbite](http://booleanbite.com)