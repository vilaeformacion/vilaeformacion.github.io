---
layout: post
title:  "Tema 3: Analógico VS Digital"
date:   2016-03-21 00:00:00
curso: 3
categories: arduino, analogico, electronica
---


En la anterior lección, estudiamos los sistemas digitales y como podemos usar las Entradas/salidas digitales de nuestro arduino, por medio de componentes como un pulsador o un led.

En esta lección, vamos a estudiar las entradas/salidas analógicas que podemos utilizar en nuestro arduino estas entradas y salidas con capaces de trabajar con más de 2 valores a diferencia de los sistemas digitales.

En esta lección, utilizaremos los componentes analogicos como son el potenciometro y la fotoresistencia para poder realizar mediciones para nuestros circuitos.

## ¿Qué es un sistema Analógico?

Un sistema analógico es un sistema que acepta más de 2 valores a diferencia del sistema digital. 

La televisión (antiguo sistema) es un sistema analógico, o las cintas de casette eran sistemas analógicos.

## Componentes Analógicos del Arduino UNO.

Seguidamente se muestra el esquema de un modelo Arduino UNO indicando donde estan las entradas y salidas analógicas.

![esanalogicas]({{ site.url }}/resources/arduino/tema3/canalogico.png)

Como podemos ver en la figura, tenemos una serie de entradas numeradas desde A0 a A5 las cuales permiten leer valores aleatorios.

Además, vemos que hay unas salidas digitales que estan marcadas con el simbolo ~; estas salidas permiten realizar escritura analógica y por lo tanto son salidas analógicas.

Tras revisar los componentes analógicos de nuestro arduino Uno, vamos a mostrar como se realizan las lecturas y escrituras analógicas.

## Lectura analógica

Para leer de manera analógica utilizaremos una de las entradas analógicas que dispone nuestro Arduino. 

Como hemos dicho anteriormente, arduino es un sistema Digital y por lo tanto no trabaja con magnitudes analogicas. La manera de leer magnitudes analógicas se realiza por medio de un conversor ADC; este conversor es capaz de convertir magnitudes analogicas en digitales. UN conversor analógico a digital del arduino UNO, tiene una precisión de 10 bits. Por lo que es capaz de convertir de 0 a 1023 niveles.

Estos niveles se miden como niveles de voltaje por lo que podemos usar estos niveles para medir de manera analógica.

A nivel de código arduino dispone de funciones para leer magnitudes analógicas. usando la función ```analogRead()```. 

La función ```analogRead```, lee el valor de un pin analógico determinado por parámetro y devuelve un número entre 0 y 1023.

Ejemplo:

```c
analogRead(A0)//Devuelve un valor entre 0 y 1023.
```

## Escritura Analógica

De igual manera que el arduino dispone de entradas analógicas, también disponemos de salidas analógicas. Estas salidas son unas salidas especiales que estan indicadas con el simbolo ~; estas señales significan que utilizan una tecnica llamda _PWM_ para modular el valor que quieren realizar por medio de un conversor _DAC_. La precisión de este conversor esd e 8 bits el cual nos da un valor entre 0 y 255.

A nivel de código arduino dispone de funciones para las salida analógica; la función para escribir en analógico es ```analogWrite```; esta función acepta 2 parámetros; el primero es el pin (siempre que sea PWM) y el segundo es un valor entre 0 y 255.

Ejemplo:

```c
analogWrite(6,255);//el segundo parametro es un valor entre 0 y 255.
```

### PWM

La modulación por ancho de pulsos (también conocida como PWM, siglas en inglés de pulse-width modulation) de una señal o fuente de energía es una técnica en la que se modifica el ciclo de trabajo de una señal periódica (una senoidal o una cuadrada, por ejemplo), ya sea para transmitir información a través de un canal de comunicaciones o para controlar la cantidad de energía que se envía a una carga.

La construcción típica de un circuito PWM se lleva a cabo mediante un comparador con dos entradas y una salida. Una de las entradas se conecta a un oscilador de onda dientes de sierra, mientras que la otra queda disponible para la señal moduladora. En la salida la frecuencia es generalmente igual a la de la señal dientes de sierra y el ciclo de trabajo está en función de la portadora.

## Referencias

1. [Página Oficial Arduino](https://arduino.cc)
2. [PWM](https://es.wikipedia.org/wiki/Modulación_por_ancho_de_pulsos)
