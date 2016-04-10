---
layout: post
title:  "Tema 0: Introducción a la electrónica"
date:   2016-03-20 00:00:00
curso: 3
categories: linux,historia
---

Este curso trata de mostrar como utilizar Arduino para realizar proyectos electrónica. En las siguientes lecciones se tratarán los distintos aspectos a tratar a la hora de crear proyectos con electrónica aplicados a la placa programable Arduino.

En esta primera lección de introducción, estudiaremos los conceptos básicos de electrónica tales como la intensidad, voltaje y Resistencia.

Además mostraremos lo componentes electrónicos más utilizados como pueden ser los diodos, resistencias y transistores.

### 1. Voltaje, Intensidad y Resistencia

En este primer apartado, vamos a estudiar los distintos conceptos básicos a la hora de utilizar la electrónica ya que es necesario tener dichos conceptos a la hora de diseñar circuitos electricos o crear dispositivos con Arduino.

**Tensión**

El Voltaje, o tensión eléctrica es una magnitud física que cuantifica la diferencia de potencial eléctrico entre 2 puntos. La tensión entre dos puntos A y B es independiente del camino recorrido por la carga y depende exlusivamente del potencial eléctrico de dichos puntos A y B.

La tensión eléctrica se mide en Voltios(**V**).


**Intensidad**

La Intensidad eléctrica es el flujo de carga eléctrica por unidad de tiempo que recorre un material se debe al movimiento de las cargas en el interior del material. La Unidad de medida de la intensidad eléctrica es el Amperio(**A**).

**Resistencia**

Se denomina Resistencia Eléctrica a la igualdad de oposición que tienen los electrones al moverse a través de un material. Podemos usar resistencias en nuestros proyectos.

La unidad de medida de la resistencia eléctrica es el Ohmio(**Ω**) 

El simbolo de una resistencia es:

![simboloR]({{ site.url}}/resources/arduino/tema0/simboloR1.png)

Seguidamente mostramos como es una resistencia:

![Resistor]({{ site.url}}/resources/arduino/tema0/resistor.jpeg)

Como podemos observar tiene un código de colores que nos indica el valor de esta además de la tolerancia de esta. Seguidamente se muestra la tabla con el código de colores de las resistencias.

![Resistenciacolor]({{ site.url}}/resources/arduino/tema0/resistenciacolor.jpg)


## Ley de Ohm

La ley de Ohm es una ley física que establece la relación entre la tensión, intensidad y resistencia. Es una ley muy importante en el tema de electricidad y la electrónica ya que nos permite calcular todo lo necesario en los circuitos que realicemos.

La _ley de Ohm_ establece que la deiferencia de potencial entre dos extremos es proporcional a la intensidad de corriente y la resistencia de este.

```java 
V = R* I
```

```python
I = V/R
```

```python
R = V/I
```

Donde V es el voltage en voltios, I la intensidad en amperios y R la Resistencia en Ohmios.

Seguidamente mostramos una relga mnemothecnica para poder tener todas las formulas a mano. 

![ohmlaw]({{ site.url}}/resources/arduino/tema0/ohmlaw.jpg)

Además podemos completar la formulara para obtener la potencia(**P**) que es la relación de paso en un flujo por unidad de tiempo.

La potencia se mide en Wattios-Hora(W/h) y puede calcularse por medio de las siguientes formulas.

```java
P=V*I
```

```java
P=R* I^2
```
```java
P= V^2/R
```

Una vez hemos visto los conceptos básicos, vamos a hacer un pequeño repaso por los componentes electrónicos que podemos encontrarnos.

**1. Diodo**

Un diodo es un componente eléctrico que solo deja pasar la corriente en un sentido. Los diodos tienen una parte positiva llamada cátodo y una parte negativa llamada ánodo.

![diodo]({{ site.url}}/resources/arduino/tema0/diodo.png)

**2. batería o alimentación**

Simbolo común para cualquier elemento que suministre energía; puede ser una pila, una batería o cualquier otro dispositivo. Hay que tener encuenta el voltaje que suministra en el paso de una pila de petaca, son 4,5V.

![pila]({{ site.url}}/resources/arduino/tema0/pila.png)

**3. Pulsador**

Un pulsador es un componente utilizado para abir y cerrar un circuito. Cuando presionamos el pulsador se cierra el circuito y se mantiene así hasta que lo cerramos.

![pulsador]({{ site.url}}/resources/arduino/tema0/pulsador.png)

**4. Led**

Un led es un diodo emisor de luz; como diodo solo deja pasar la corriente en un sentido; mientras que cuando pasa corriente, se emite luz. La patilla más larga siempre es el negativo.

![led]({{ site.url}}/resources/arduino/tema0/led.png)

**5. potenciometro**

Un Potenciometro es un componente con el que podemos variar la resistencia a través de una pequeña rueda que gira para dar una mayor o menor resistencia.

![potenciometro]({{ site.url}}/resources/arduino/tema0/potenciometro.png)

**6. condensador**

Un condensador es un componente que permite almacenar carga eléctrica. Este tipod e componentes se utilizan tanto para alimentar a un ciruito, como para absorber picos de tensión o suavizar una señal. **NUNCA SE DEBE SUPERAR EL VOLTAJE DE UN CONDENSADOR EN MAS DE 10 VOLTIOS**.

![condensador]({{ site.url}}/resources/arduino/tema0/condensador.png)

**7. Oscilador cerámico**

Este componente permite simular un metrónomo digital; permitiendo tener una señal base para todos los dispositivos que dependen de una señal de reloj. 

![oscilador]({{ site.url}}/resources/arduino/tema0/oscilador.png)

**8. Motor**

Un motor es un componente que convierte la energía electrica en movimiento. Existen varios tipos de motores como los standar, paso a paso o servomotores.

![motor]({{ site.url}}/resources/arduino/tema0/motor.png)

**9. Relé**

Un rele es un componente electromecánico que permite activar un circuito u otro en función de una señal. Normalmente estan conpuestos de un interruptor que es accionado por medio de un electroiman.

![rele]({{ site.url}}/resources/arduino/tema0/rele.png)

**10 Regulador de Voltaje**

Un regulador de voltaje, es un componente electrónico que permite regular el voltaje de entrada en uno de salida. Normalmente este tipo de dispositivos se utilizan para suavizar la señal y poder tenerlo a un voltaje en concreto.

![regulador]({{ site.url}}/resources/arduino/tema0/regulador.png)

### Transistores

El último componente que vamos a tratar en este tema introductorio es el transistor; el transistor es un componente que se comporta como un interruptor accionado electrónicamente. Este componente es uno de los más importantes ya que todos los procesadores tienen millones de ellos y cada vez más(vease Ley de Moore). 

Un transistor se compone de 3 terminales Emisor(E), Colector(C) y la base(B) modificando la tensión eléctrica de la base, se permite el paso de corriente del emisor al colector.

![transistor]({{ site.url}}/resources/arduino/tema0/transistor3.png)

Los transistores estan formados por 3 cristales semiconductores que se combinan 2 a uno; PNP o NPN.

Puede ser utilizado como interruptor, amplificador de señales, oscilador, conmutador o rectificador.

Por último, un transistor puede tener 3 estados:

* En activa: deja pasar una parte de la corriente.
* En corte: no deja pasar la corriente.
* En saturación: deja pasar toda la corriente.

## Referencias

* [Tensión Eléctrica](https://es.wikipedia.org/wiki/Tensión_(electricidad))
* [Intensidad Eléctrica](https://es.wikipedia.org/wiki/Corriente_eléctrica)
* [Resistencia Eléctrica](https://es.wikipedia.org/wiki/Resistencia_eléctrica)
* [Ley de Ohm](https://es.wikipedia.org/wiki/Ley_de_Ohm)
* [Potencia Eléctrica](https://es.wikipedia.org/wiki/Potencia_eléctrica)