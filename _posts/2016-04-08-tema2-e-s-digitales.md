---
layout: post
title:  "Tema 2: Entradas/Salidas Digitales"
date:   2016-03-21 00:00:00
curso: 3
categories: arduino, digital, electronica
---


Tras ver una introducción a arduino, vamos a estudiar una parte importante sobre la electrónica y es las Entradas/Salidas Digitales.

Como hemos visto en la anterior lección, arduino tiene una serie de entradas/salidas digitales que en el modelo Uno, estan numeradas de 0 a 13. 

En primer lugar, vamos a ver que es una entrada/salida digital, y para que podemos utilizarla; después estudiaremos un componente utilizado en electrónica digital; el pulsador. Aunque ya lo hemos visto en la lección 0, vamos a estudiar en más detalle este componente.

## ¿Qué es un sistema Digital?

Un sistema digital, es aquel que utiliza una señal que consta de 2 estados; el 0 y e 1. Como por ejemplo los microprocesadores de nuestros ordenadores son sistemas digiales ya que funcionan por medio del sistema binario (0 o 1).

Arduino funciona de manera digital ya que tiene un microprocesador; aunque posee la capacidad de trabajar con datos analogicos; este tema se abordará en la siguiente lección.

## Entrada/Salida

Otro concepto que vamos a ver en este curso, es la diferencia entre entrada y salida:

* Una entrada es cualquier señal que venga del exterior a nuestro sistema.

* Una salida es cualquier señal que salga de nuestro sistema al exterior.

![entradasalida]({{ site.url }}/resources/arduino/tema2/entradasalida.png)

Un ejemplo de Entrada puede ser un sensor o un pulsador.

Un ejemplo de salida, puede ser un led, o una pantalla LCD.

![es]({{ site.url }}/resources/arduino/tema2/es.png)

## El pulsador

Uno de los componentes mas comunes a la hora de trabajar en electrónica digital, es el pulsador. Este componente nos permite abrir y cerrar el circuito.

![pulsador]({{ site.url }}/resources/arduino/tema2/pulsador.png)

Un pulsador tiene 4 patillas que estan conectadas entre si 2 a 2. Por lo que tenemos que tener en cuenta esto a la hora de conectar el resto de componentes.

![pulsadorbb]({{ site.url }}/resources/arduino/tema2/pulsadorbb.png)

Para montar correctamente un pulsador, debemos utilizar una resistencia conectada en el puerto negativo para evitar los falsos positivos. Quedaría de la siguiente manera.

![pulsadorre]({{ site.url }}/resources/arduino/tema2/pulsadorres.png)

También puede ser necesario añadir un condensador para evitar rebotes en la señal del pulsador.

## Ejemplo de Montaje de un pulsador

Seguidamente mostramos un ejemplo de montaje con un pulsador.

![montajepulsador]({{ site.url }}/resources/arduino/tema2/ejemplo1.png)

## Interactuar con el pulsador en arduino

Tras ver como montar un pulsador, pasaremos a mostrar como podemos utilizar arduino para comprobar cuando se ha pulsado el botón. Para ello pulsaremos la función ```digitalRead(pin)```.

Esta función devuelve los valores ```HIGH``` o ```LOW``` si en el pin que hemos pasado por parámetro esta activa la señal o no. usando una esctructura de control _if_ podemos saber si se ha pulsado el botón o no.

Seguidamente dejamos un fragmento de código para encender el led anterior al pulsar el botón.

```c

void setup(){
 pinMode(13,OUTPUT);
 //NOTA: por defecto todos los puertos estan en modo INPUT por lo que no es necesario definir el modo.	
}

void loop(){
	if(digitalRead(7)==HIGH){//Si se pulsa el botón se activa el led
		digitalWrite(13,HIGH);
	}else{
		digitalWrite(13,LOW);//En caso contrario se apaga.
	}
	delay(500);
}
```

## Referencias

1. [Página de Arduino Oficial](https://arduino.cc)
2. [Artículo sobre pulsadores](http://booleanbite.com/web/electronica-basica-pulsadores-y-diodos-led/)
3. [Tutorial sobre Pulsadores](https://www.arduino.cc/en/Tutorial/Button)

