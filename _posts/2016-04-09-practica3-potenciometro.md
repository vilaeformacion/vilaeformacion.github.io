---
layout: post
title:  "Práctica 3: El potenciometro"
date:   2016-03-20 00:00:00
curso: 4
categories: arduino, electronica
---

En esta práctica, vamos a utilizar las entradas y salidas analógicas para hacer que un led aumente o disminuya su brillo; usando un potenciometro. 

El potenciometro, es una resistencia variable que podemos cambiar su valor moviendo una pequeña rueda. Consta de 3 patillas:

* La primera se trata de la alimentación que se conectará a 5V.
* La segunda se trata de la salida que será donde mediremos con la entrada analógica.
* La tercera se trata de la salida a tierra que conectaremos a la toma GND.

![potenciometro]({{ site.url }}/resources/arduino/practica3/potenciometro2.png)

Tras ver como funciona el potenciometro, vamos a mostrar los componentes que necesitaremos para esta práctica.

* 1 led
* 1 Resistencia 220Ohmios.
* 1 Potenciometro
* 1 Arduino.
* 1 Breadboard.
* cables para conexión.

Con los componentes ya listos, vamos a pasar a realizar nuestro circuito. Se muestra a continuación.

![practica3]({{ site.url }}/resources/arduino/practica3/practica3.png)

Como podemos ver en el montaje la entrada A0 la usaremos para leer el valor del potenciometro; y la salida PWM 6(marcada con ~) la usaremos como salida analógica.

Con el circuito ya montado, vamos a programar nuestro arduino uno; pero antes vamos a mostraros la función ```map```; ya que la entrada A0 nos da valores entre 0 y 1023 y la salida 6, nos permite tener valores entre 0 y 255. por ello necesitamos una función que nos convierta los 2 rangos.

```map(valor, limtinf1, limtsup1, limtinf2, limsup2);```

Los parámetros de esta función son:
* _valor_: valor a convertir.
* _liminf1_: Limite inferior del primer rango.
* _limsup1_: Limite superior del segundo rango.
* _limtinf2_: Limite inferior del segundo rango.
* _limtsup2_: Limite suprior del segundo rango.

La función devuelve un valor del segundo rango.

Seguidamente se muestra el código de la práctica.

```c
void setup(){
	//NO hay que usar pinMode ya que vamos a usar la salida analógica.
}

void loop(){
	//Leemos el valor de la entrada analogica
	int valorentrada = analogRead(A0);
	//convertimos el valor de entrada en valor de salida.
	int valorsalida= map(valorentrada,0,1023,0,255);
	//Escribimos el valor de salida.
	analogWrite(6,valorsalida);
}
```

Una vez que hemos pasado el programa, podemos observar que cambiando el potenciometro, se cambia el brillo del led.

## Ejercicios Opcionales

1. Usando el ejemplo del Blink, vamos a hacer que se pueda cambiar el tiempo de parpadeo usando un potenciometro.
