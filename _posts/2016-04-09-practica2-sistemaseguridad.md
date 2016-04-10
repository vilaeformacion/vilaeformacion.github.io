---
layout: post
title:  "Práctica 2: Sistema de Seguridad"
date:   2016-03-20 00:00:00
curso: 4
categories: arduino, electronica
---

En esta práctica vamos a realizar un sistema de seguridad de manera que solo se pueda encender una luz, si los 2 pulsadores estan pulsados.

Para ello, necesitaremos los siguientes materiales:

* 2 pulsadores
* 2 resistencias de 1K Ohmios.
* 1 Resistencia de 220 Ohmios.
* 1 led.
* 1 Arduino.
* 1 cable USB.
* cables para las conexiones.

Tras tener todos los materiales, vamos a pasar a realizar el montaje; lo montaremos como indica el siguiente esquema:

![esquema]({{ site.url }}/resources/arduino/practica2/practica2.png)

Una vez tenemos el esquema ya montado, vamos a pasar a programar nuestro arduino para ello, utilizaremos el siguiente código.

```c
/*Practica 2: Sistema de Seguridad.
En este caso solo se encendera el led si se pulsan los 2 botones.*/
void setup() {
  pinMode(13,OUTPUT);

}

void loop() {
   //el operador && significa y que sera verdadero si 
   // las 2 condiciones son ciertas.
  if(digitalRead(7)==HIGH && digitalRead(4)==HIGH){
     digitalWrite(13,HIGH); //Enciende el led
  }else{
     digitalWrite(13,LOW);  //Apaga el led.
  }
  delay(500);
}
```

## Ejercicios Opcionales

1. Cambiar el programa anterior para que parpadee el led si se pulsan los 2 botones.
2. Añadir un segundo led y que parpadee solo si se pulsan los 2 el primer led se parpadeera si no estan los 2 pulsadores activos.