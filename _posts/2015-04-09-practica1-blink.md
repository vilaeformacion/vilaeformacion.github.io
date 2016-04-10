---
layout: post
title:  "Práctica 1: Introducción a Arduino"
date:   2016-03-20 00:00:00
curso: 4
categories: arduino, electronica
---

En esta primera práctica el alumno realizará su primer montaje; en este caso vamos a realizar el comunmente llamado "hola mundo" del hardware. El blink.

Lo que vamos a realizar, es que un led parpadee. Para ello necesitaremos los siguientes componentes:

* 1 resistencia de 220Ohmios.
* 1 led(no importa el color).
* 1 Arduino(en este ejemplo usaremos un modelo Arduino Uno).
* 1 breadboard.
* 1 cable USB.
* cables para la conexión.

Seguidamente mostramos el montaje que tenemos que realizar:

![montajeblink]({{ site.url }}/resources/arduino/practica1/blink.png)

Una vez hemos realizado este montaje, vamos a pasar a crear el programa; para ello, arrancamos el arduino IDE y nos dispondremos a crear nuestro primer programa o sketch para Arduino.

Seguidamente dejamos el código que hay que crear en el editor.

```c
/*
Primer ejemplo con Arduino: El Blink
Este programa hace parpadear un led que esta conectado en el pin 13.
 */

// La funcion Setup, se ejecuta una unica vez
void setup() {
  // Inicializamos el pin digital 13 como salida.
  pinMode(13, OUTPUT);
}

// La función loop se ejecuta en bucle una y otra vez.
void loop() {
  digitalWrite(13, HIGH);   // Encendemos el led 13
  delay(1000);              // Esperamos 1 segundo
  digitalWrite(13, LOW);    // Apagamos el led 13
  delay(1000);              // Esperamos 1 segundo
}
```

Cuando hayamos terminado de escribir el código anterior, vamos a pasar a subir nuestro código a nuestra placa Arduino; para ello, simplemente conectamos la placa a nuestro PC por medio del cable USB. Una vez conectado, vamos a seleccionar el puerto correcto en nuestro IDE; usando el menú ```Herramientas->puerto``` y seleccionaremos el puerto que indique que esta conectada nuestra placa(aparece el modelo entre parentesis).

![selecionarplaca]({{ site.url }}/resources/arduino/practica1/seleccionar placa.png)

Una vez tenemos el puerto seleccionado, pulsaremos el botón de subir(2º botón de la izquierda de la barra de herramientas). Veremos que parpadean los leds de nuestra placa mientras se esta subiendo nuestro programa. Si no hay ningún error, deberiamos de poder ver el blink parpadeando.

### Problemas en esta práctica.

1. Es normal, tener errores de compilación en los primeros programas a realizar. Por ello es conveniente tener a mano la Referencia del lenguaje que puede encontrar en los apuntes de este curso.

2. _El programa se ha subido pero el led no parpadea_: Es posible que hayas puesto el led con la polaridad al contrario. Cambia las patillas del led y verás como ahora si parpadea. Recuerda que el led es un diodo y solo deja pasar la corriente en un sentido.


### Ejercicios Opcionales

1. Intenta hacer que el blink parpadee más rápido.
2. Prueba a realizar un semaforo con 3 leds; dejamos aquí el montaje; el código lo dejamos como ejercicio a realizar.

![semaforo]({{ site.url }}/resources/arduino/practica1/semaforo.png)
