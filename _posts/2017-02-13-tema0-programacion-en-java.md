---
layout: post
title:  "Tema 0: Programación en Java"
date:   2017-02-13 00:00:00
curso: 5
categories: Java, Programación
---

En este primer tema, estudiaremos como programar en el lenguaje de Programación Java; en este caso, se estudiará su sintaxis y como realizar programas en este lenguaje de Programación.

En primer lugar, mostraremos como instalar las librerías de desarrollo o JDK. La cual utilizaremos en este curso la versión 1.8 del entorno de Desarrollo de Java realizadas por Oracle.

Para poder instalar las librerías de desarrollo, las descargaremos de la [página oficial](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

**NOTA**: La versión de la descarga puede variar; en el momento de la creación de este curso se instaló la versión _1.8_u121_.

## Hola Mundo

Una vez descargadas e instaladas, vamos a mostrar el primer programa en Java o "Hola Mundo".

```java

public class HolaMundo{
public static void main(String[] args){
    System.out.println("Hola Mundo");
}
}
```

Este es el primer programa en Java el cual simplemente muestra un mensaje por pantalla "Hola Mundo". Para tomar familirización con el lenguaje, vamos a crear un fichero de texto llamado "HolaMundo.java", y guardaremos el contenido el código anterior.

Una vez guardado el fichero con el contenido anterior, vamos a Compilar el código Java; por lo que utilizaremos el compilador java ```javac```. Para ello abriremos una consola de comandos y ejecutaremos el siguiente comando:

```bash
$javac HolaMundo.java
```

Al comprobar el directorio donde se encuentra el archivo HolaMundo.java, encontraremos un nuevo archivo llamado HolaMundo.class. Este archivo es el código ByteCode Java. El cual contiene el programa compilado en ByteCode. Java es un lenguaje SemiInterpretado por lo que se compila hasta un código que es independiente de la plataforma.

Para poder ejecutar este programa, necesitaremos el interprete Java el cual se ejecuta con la orden:

```bash
$java HolaMundo
Hola Mundo
```

Con esto ya hemos ejecutado nuestro primer programa Java. Pero antes de indagar más, vamos a mostrar algunos conceptos necesarios sobre los lenguajes Orientados a Objetos.

### Programación Orientada a Objetos

Java es un lenguaje de programación a Objetos. La Programación Orientada a Objetos o POO, es un paradigma de la programación que viene a innovar la forma de obtener resultados. Los objetos manipulan los datos de entrada para la obtención de datos de salida específicos, donde cada objeto ofrece una funcionalidad especial. Este paradigma tuvo gran auge en la decada de los 90 pero comenzó a utilizarse en los años 60.

Una de las principales caracteristicas de los Lenguajes orientados a objetos, es que todo objeto es una entidad que permite almacenar una serie de datos y proveer comportamientos especificos de cada entidad.

Los conceptos más importantes de la programación a objetos son los conceptos de _Clase_ y _Objeto_.

Una _Clase_ es una entidad que define una serie de datos que almacena como _propiedades_ y que define un comportamiento como _métodos_.

Un objeto es una _instancia_ de una clase. Es decir, es la manifestación de la entidad que almacena unos datos concretos.

Los datos definidos en una _clase_ se llaman _propiedades_. Mientras que los comportamientos de una _clase_ se llama _método_. Una clase puede tener definidas varias propiedades y varios métodos.

La programación orientada a objetos, tiene una serie de caracteristicas que en mayor o menor medida implementa Java o cualquier otro Lenguaje orientado a Objetos.

Existe un acuerdo acerca de qué características contempla la "orientación a objetos". Las características siguientes son las más importantes:

**Abstracción**

Denota las características esenciales de un objeto, donde se capturan sus comportamientos. Cada objeto en el sistema sirve como modelo de un "agente" abstracto que puede realizar trabajo, informar y cambiar su estado, y "comunicarse" con otros objetos en el sistema sin revelar "cómo" se implementan estas características. Los procesos, las funciones o los métodos pueden también ser abstraídos, y, cuando lo están, una variedad de técnicas son requeridas para ampliar una abstracción. El proceso de abstracción permite seleccionar las características relevantes dentro de un conjunto e identificar comportamientos comunes para definir nuevos tipos de entidades en el mundo real. La abstracción es clave en el proceso de análisis y diseño orientado a objetos, ya que mediante ella podemos llegar a armar un conjunto de clases que permitan modelar la realidad o el problema que se quiere atacar.

**Encapsulamiento**

Significa reunir todos los elementos que pueden considerarse pertenecientes a una misma entidad, al mismo nivel de abstracción. Esto permite aumentar la cohesión (diseño estructurado) de los componentes del sistema. Algunos autores confunden este concepto con el principio de ocultación, principalmente porque se suelen emplear conjuntamente.

**Polimorfismo**

Comportamientos diferentes, asociados a objetos distintos, pueden compartir el mismo nombre; al llamarlos por ese nombre se utilizará el comportamiento correspondiente al objeto que se esté usando. O, dicho de otro modo, las referencias y las colecciones de objetos pueden contener objetos de diferentes tipos, y la invocación de un comportamiento en una referencia producirá el comportamiento correcto para el tipo real del objeto referenciado. Cuando esto ocurre en "tiempo de ejecución", esta última característica se llama asignación tardía o asignación dinámica. Algunos lenguajes proporcionan medios más estáticos (en "tiempo de compilación") de polimorfismo, tales como las plantillas y la sobrecarga de operadores de C++.

**Herencia**

Las clases no se encuentran aisladas, sino que se relacionan entre sí, formando una jerarquía de clasificación. Los objetos heredan las propiedades y el comportamiento de todas las clases a las que pertenecen. La herencia organiza y facilita el polimorfismo y el encapsulamiento, permitiendo a los objetos ser definidos y creados como tipos especializados de objetos preexistentes. Estos pueden compartir (y extender) su comportamiento sin tener que volver a implementarlo. Esto suele hacerse habitualmente agrupando los objetos en clases y estas en árboles o enrejados que reflejan un comportamiento común. Cuando un objeto hereda de más de una clase se dice que hay herencia múltiple; siendo de alta complejidad técnica por lo cual suele recurrirse a la herencia virtual para evitar la duplicación de datos.

**Modularidad**

Se denomina "modularidad" a la propiedad que permite subdividir una aplicación en partes más pequeñas (llamadas módulos), cada una de las cuales debe ser tan independiente como sea posible de la aplicación en sí y de las restantes partes. Estos módulos se pueden compilar por separado, pero tienen conexiones con otros módulos. Al igual que la encapsulación, los lenguajes soportan la modularidad de diversas formas.

**Principio de ocultación**

Cada objeto está aislado del exterior, es un módulo natural, y cada tipo de objeto expone una "interfaz" a otros objetos que especifica cómo pueden interactuar con los objetos de la clase. El aislamiento protege a las propiedades de un objeto contra su modificación por quien no tenga derecho a acceder a ellas; solamente los propios métodos internos del objeto pueden acceder a su estado. Esto asegura que otros objetos no puedan cambiar el estado interno de un objeto de manera inesperada, eliminando efectos secundarios e interacciones inesperadas. Algunos lenguajes relajan esto, permitiendo un acceso directo a los datos internos del objeto de una manera controlada y limitando el grado de abstracción. La aplicación entera se reduce a un agregado o rompecabezas de objetos.

**Recolección de basura**

La recolección de basura (garbage collection) es la técnica por la cual el entorno de objetos se encarga de destruir automáticamente, y por tanto desvincular la memoria asociada, los objetos que hayan quedado sin ninguna referencia a ellos. Esto significa que el programador no debe preocuparse por la asignación o liberación de memoria, ya que el entorno la asignará al crear un nuevo objeto y la liberará cuando nadie lo esté usando. En la mayoría de los lenguajes híbridos que se extendieron para soportar el Paradigma de Programación Orientada a Objetos como C++ u Object Pascal, esta característica no existe y la memoria debe desasignarse expresamente.

Tras ver las caracteristicas de la Programación Orientada a Objetos, vamos a pasar a ver la sintaxis de este lenguaje de Programación.

### El Lenguaje de Programación Java

Java es un lenguaje de programación de propósito general, concurrente, orientado a objetos que fue diseñado específicamente para tener tan pocas dependencias de implementación como fuera posible. Su intención es permitir que los desarrolladores de aplicaciones escriban el programa una vez y lo ejecuten en cualquier dispositivo (conocido en inglés como WORA, o "write once, run anywhere"), lo que quiere decir que el código que es ejecutado en una plataforma no tiene que ser recompilado para correr en otra. Java es, a partir de 2012, uno de los lenguajes de programación más populares en uso, particularmente para aplicaciones de cliente-servidor de web, con unos 10 millones de usuarios reportados.

El lenguaje de programación Java fue originalmente desarrollado por James Gosling de Sun Microsystems (la cual fue adquirida por la compañía Oracle) y publicado en 1995 como un componente fundamental de la plataforma Java de Sun Microsystems. Su sintaxis deriva en gran medida de C y C++, pero tiene menos utilidades de bajo nivel que cualquiera de ellos. Las aplicaciones de Java son generalmente compiladas a bytecode (clase Java) que puede ejecutarse en cualquier máquina virtual Java (JVM) sin importar la arquitectura de la computadora subyacente.

El lenguaje de Programación Java tiene las siguientes caracteristicas:

* Orientado a Objetos

Java es orientado a objetos por lo que tiene la gran mayoria de las caracteristicas de la programación orientada a objetos; como el poliformismo, ocultación, modularidad, herencia,etc...

* Independencia de la Plataforma

La segunda característica, la independencia de la plataforma, significa que programas escritos en el lenguaje Java pueden ejecutarse igualmente en cualquier tipo de hardware. Este es el significado de ser capaz de escribir un programa una vez y que pueda ejecutarse en cualquier dispositivo, tal como reza el axioma de Java, "write once, run anywhere".

Para ello, se compila el código fuente escrito en lenguaje Java, para generar un código conocido como “bytecode” (específicamente Java bytecode)—instrucciones máquina simplificadas específicas de la plataforma Java. Esta pieza está “a medio camino” entre el código fuente y el código máquina que entiende el dispositivo destino. El bytecode es ejecutado entonces en la máquina virtual (JVM), un programa escrito en código nativo de la plataforma destino (que es el que entiende su hardware), que interpreta y ejecuta el código. Además, se suministran bibliotecas adicionales para acceder a las características de cada dispositivo (como los gráficos, ejecución mediante hebras o threads, la interfaz de red) de forma unificada. Se debe tener presente que, aunque hay una etapa explícita de compilación, el bytecode generado es interpretado o convertido a instrucciones máquina del código nativo por el compilador JIT (Just In Time).

* Recolector de basura

En Java el problema fugas de memoria se evita en gran medida gracias a la recolección de basura (o automatic garbage collector). El programador determina cuándo se crean los objetos y el entorno en tiempo de ejecución de Java (Java runtime) es el responsable de gestionar el ciclo de vida de los objetos. El programa, u otros objetos pueden tener localizado un objeto mediante una referencia a éste. Cuando no quedan referencias a un objeto, el recolector de basura de Java borra el objeto, liberando así la memoria que ocupaba previniendo posibles fugas (ejemplo: un objeto creado y únicamente usado dentro de un método sólo tiene entidad dentro de éste; al salir del método el objeto es eliminado).

#### Sintaxis

El lenguaje de programación Java, tiene una sintaxis de forma que permita declarar clases como sus propiedades y sus métodos.

* Clase

Para definir una clase utilizaremos un archivo por cada clase que debera llamarse igual que la clase. 

```java

public class HolaMundo{

}
```

Como podemos ver en el ejemplo antes primero empezaremos con la palabra reservada ```public``` la cual nos indica el acceso de esta clase. En Java se define los siguientes modificadores de acceso:

* _public_: indica que el acceso es publico y que todas las clases pueden acceder a esta clase, objeto o propiedad.
* _private_: indica que solo la propia clase puede acceder a sus propiedades, metodos u otras clases internas.
* _protected_: Indica que solo la propia clase y las que hereden esta, pueden acceder a sus propiedades o métodos.

Por último, si no se especifica un modificador de acceso, se tomará por defecto el acceso por paquete. Esto quiere decir que solo las clases de la misma carpeta tienen acceso a él.

Una vez vistos los modificadores de acceso, veremos que esta la palabra reservada _class_ la cual indica que estamos definiendo una clase. Después establecemos el nombre de esta que debe ser igual que el nombre del fichero; por ejemplo en este caso, la clase se llama _HolaMundo_ por lo que el fichero debe llamarse _HolaMundo.java_ sino habrá un error de compilación.

Seguidamente vemos que se abre y cierran llaves la cual define un bloque de código o definición.


### Referencias

* [Programación Orientada a Objetos](https://es.wikipedia.org/wiki/Programaci%C3%B3n_orientada_a_objetos)
* [Lenguaje de programación Java](https://es.wikipedia.org/wiki/Java_(lenguaje_de_programaci%C3%B3n))