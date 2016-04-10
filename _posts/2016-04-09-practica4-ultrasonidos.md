---
layout: post
title:  "Práctica 4: Sensor de presencia"
date:   2016-04-01 00:00:00
curso: 4
categories: arduino, electronica
---

En esta práctica, vamos a utilizar el sensor de ultrasonidos SH-04. Este sensor nos permite medir distancia a través de ultrasonido.

![ultrasonido]({{site.url}}/resources/arduino/practica4/sensorultrasonido.png)

En primer lugar, vamos a mostrar el montaje de esta práctica. Esta práctica haremos que se encienda una luz, si se detecta algo por el sensor. En este caso, si hay un objeto por menos de 10 centimetros.

Antes de nada mostraremos los componentes necesarios:

* 1 Arduino UNO.
* 1 Resistencia 220 Ohmios.
* 1 BreadBoard.
* 1 Sensor ultrasonido SH-04.
* 1 led.
* cables para conectarlos

Tras tener todos los componentes mostraremos el montaje de este ejercicio.

![montajeultrasonido]({{site.url}}/resources/arduino/practica4/montajrepractica4.png)

Para poder utilizar el sensor, necesitaremos la librería ultrasonic. Esta librería nos permitirá utilizar el sensor de ultrasonidos pudiendo obtener la distancia en centimetros o pulgadas.

La librería puede encontrarse [aqui]({{site.url}}/resources/practica4/Ultrasonic.zip). La descargamos y añadimos a nuestro IDe como vimos en el tema 4.

Tras realizar el montaje y añadir la librería, vamos a mostrar el código fuente.

```c
#include <Ultrasonic.h>
Ultrasonic us(12,11);
byte cms;
void setup()
{
  pinMode(4,OUTPUT);
  Serial.begin(9600);
}

void loop()
{
  cms=us.Ranging(CM);
  Serial.print(cms);
  Serial.println(" cm");
  if(cms<10)
    digitalWrite(8,HIGH);
   else
    digitalWrite(8,LOW);
  delay(100);
}

```

En este caso veremos que si hay un objeto con menos de 10 centimetros se encederá la luz.

### Ejercicios opcionales

* Utilizando el ejemplo del blink, cambiar la frecuencia de parpadeo en función de la distancia.

### Referencias

* [Ultrasonido](http://playground.arduino.cc/Main/UltrasonicSensor)
* [Booleanbite](http://booleanbite.com)