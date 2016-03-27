---
layout: post
title:  "Tema 5: Consola de comandos"
date:   2016-03-27 10:00:00
curso: 1
categories: escritorio, raspbian
---

Tras ver como esta estructurado el sistema de ficheros en Linux, vamos a pasar a estudiar la consola de comandos. la consola de comandos es una interfaz de texto que nos permite realizar comandos y operaciones sin depender de una interfaz gráfica. En la consola de comandos, tenemos mucha más funcionalidad que en el escritorio gráfico. Muchas de las configuraciones avanzadas que realizaremos en Raspbian, vamos a realizarlas con la consola de comandos.

como hemos mostrado en anteriores lecciones, podemos acceder a la consola de comandos a través del botón superior izquierda ![consolacomandos]({{ site.url }}/resources/tema3/iconoconsola.png). Tras entrar en la consola de comandos, podemos escribir una serie de comandos u ordenes para poder ejemplo manejarnos en el sistema de ficheros, copiar ficheros, comprimir, etc...

![imagenconsola]({{ site.url }}/resources/tema5/consola1.png)

### La consola de comandos

La consola de comandos nos permite realizar acciones de forma que podemos realizar acciones más avanzadas que con la interfaz gráfica.

La consola de comandos nos muestra un promt o mensaje que muestra el usuario con el que estamos conectados, y por otro lado en que máquina estamos conectados. Por ejemplo:

``` 
pi@zerasul:~$ _
```

para introducir un comando pondremos el comando en concreto y pulsaremos enter. Por ejemplo el comando _pwd_ nos muestra en que carpeta del sistema nos encontramos.

``` 
pi@zerasul:~$ pwd
/home/pi
```

vemos que nos encontramos en la carpeta _/home/pi_ es decir, nuestra carpeta de usuario. tambien podemos mostrar el listado del directorio donde nos encontramos con la orden _ls_.

``` 
pi@zerasul:~$ ls
Desktop
Documents
Downloads
Music
Pictures
Public
Videos
```

SI queremos cambiar de directorio, usaremos el comando _cd_ seguido del nombre del directorio al que queremos movernos. 

**NOTA**: Si no nos acordamos correctamente del comando o del nombre del directorio, podemos usar la tecla < tabulador > y nos mostrara una pequeña ayuda.

``` 
pi@zerasul:~$ cd Dekstop
pi@zerasul:~/Dekstop$ _
```

Como podemos ver al cambiar de directorio, nos aparece en el Prompt. Si por el contrario queremos ir al directorio anterior, usaremos la orden anteriormente mencionada, pero añadiremos "..". Esto indica que queremos ir al directorio padre. Si por el contrario queremos mencionar al directorio actual, usaremos solo 1 punto.

``` 
pi@zerasul:~/Desktop$ cd ..
pi@zerasul:~$ _
``` 
Por último, si usamos la orden _clear_ borraremos la pantalla para tener más espacio.

### Historial

En todo momento podemos ver el historial de los últimos comandos introudciros con la orden _history_. Esto nos mostrara la lista de comandos. Además podemos usar las teclas < arriba > y < abajo > para poder ver los anteriores comandos.

![imagenhistory]({{ site.url }}/resources/tema5/consola2.png)

### Sudo

Como hemos visto anteriormente, hay una serie de permisos que tienen los usuarios del sistema. Hay que diferenciar que hay 2 modos de usuario por asi decirlo. El modo usuario, que tiene permisos limitados que podemos diferenciarlo que el prompt acaba en '$'. Mientras que el segundo modo es el modo superadministrador que su prompt acaba en '#' hay que decir, que tenemos que tener cuidado con el uso de permisos de administración ya que podemos dejar nuestra Raspberry Pi **INUTILIZADA**.

``` 
pi@zerasul:~$ _ # modo usuario
 pi@zerasul:~# _ # modo administrador
```

Podemos usar el comando _sudo_ para ejecutar un único comando en modo administrador.

``` 
pi@zerasul:~$ sudo ls /root
```

o si no queremos estar introduciendo la orden sudo, podemos entrar con el usuario administrador con la orden _sudo su_.

**NOTA**: no es recomendable usar mucho el modo administrador.

``` 
pi@zerasul:~$ sudo su
root@zerasul:~# _
```

Vemos como se ha cambiado el usuario a root. Esto quiere decir que somos el superadministrador.

### Manejo de ficheros (cd, copy, mv, rm, etc..)

Con la consola de comandos podemos realizar una serie de operaciones para manejar los ficheros del sistema de igual forma que con el modo gráfico. Seguidamente vamos a mostrar una serie de comandos para manejar ficheros con la consola de comandos.

**cd**

Nos permite cambiar de directorio.

``` 
pi@zerasul:~$ cd Desktop
```

**copy**

Nos permite copiar archivos funciona de la siguiente forma.

copy < origen > < destino >

``` 
pi@zerasul:~$ copy hola.txt hola2.txt
```

**NOTA**: si queremos copiar un directorio tenemos que añadir la opcion -R.

``` 
pi@zerasul:~$ copy -R hola hola2
```

**mv**

Permite mover archivos.

copy < origen > < destino >

``` 
pi@zerasul:~$ mv hola.txt hola2.txt # si es en el mismo directorio renombra el fichero.
```

**NOTA**: si queremos mover un directorio tenemos que añadir la opcion -R.

``` 
pi@zerasul:~$ mv -R hola hola2
```

**rm**

Permite borrar un fichero. Hay que tener cuidado al utilizar esta orden.

rm < fichero o directorio (con la opcion -R ) >

``` 
pi@zerasul:~$ rm fichero.txt
```

**NOTA**: para borrar directorios usar la opción -R.

**NOTA2**: A veces es requerido el uso de _sudo_.

**cat**

Permite ver el contenido de un archivo.

``` 
pi@zerasul:~$ cat /proc/cpuinfo
```

### El editor te Textos Nano

El editor de textos nano permite editar archivos de texto de forma sencilla a traves de una serie de comandos. Existen otros editores de texto como el _vi_ o el _vim_. Para acceder al editor de textos nanos usaremos la siguiente orden.

``` 
pi@zerasul:~$ nano fichero.txt
```

![nano]({{ site.url }}/resources/tema5/consola3.png)

Para guardar un fichero en nano pulsaremos la combinación de teclas _ctrl+O_ y para salir _ctrl+x_. Puede verse una pequeña leyenda de ayuda en la parte inferior.

### Comprimir y Descomprimir archivos

Una parte importante del uso de la consola es poder comprimir y descomprimir archivos. Para ello usaremos la orden _tar_. Tar es un compresor y descompresor de código fuente abierto. Que a diferencia de _zip_ y _rar_ no lo son. 

Para comprimir un archivo usaremos la siguiente sintaxis.

 tar cvf archivo.tar < lista de ficheros>

``` 
pi@zerasul:~$ tar miarchivo.tar fichero1.txt fichero2.txt
```

Para descomprimir un archivo usaremos la siguiente sintaxis.

 tar xvf archivo.tar

``` 
pi@zerasul:~$ tar xvf miarchivo.tar
```

### wget

Con la orden wget podemos descargarnos un fichero usando una dirección web. Por ejemplo

``` 
pi@zerasul:~$ wget http://miweb.com/miarchivo.txt
```

### apt-get

Con apt-get en raspbian y el las distribuciones basadas en Debian, podemos instalar nuevos paquetes y funcionalidades a nuestro sistema. Este manejador de paquetes permite acutalizar los paquetes existentes y obtener nuevos. Seguidamente mostraremos la opción de como instalar el reproductor multimedia vlc.

``` 
pi@zerasul:~$ apt-get install vlc # esta orden dara error ya que necesitamos permisos de administrador.
```

``` 
pi@zerasul:~$ sudo apt-get install vlc
```

Para actualizar nuestro software primero debemos actualizar los repositorios con la orden _update_.

``` 
pi@zerasul:~$ sudo apt-get update
```

Por último, para actualizar nuestro software usaremos la orden upgrade.

``` 
pi@zerasul:~$ sudo apt-get upgrade
```

Con este ultimo apartado, nos quedaremos para el último tema de este curso de introducción que lo utilizaremos para instalar nuestro propio servidor web.

### Referencias

* [Linux Commands](http://ss64.com/ /)
* [Nano](http://mintaka.sdsu.edu/reu/nano.html)
* [Vim](http://www.vim.org/docs.php)
* [Tar](http://www.computerhope.com/unix/utar.htm)
* [Apt-get](https://help.ubuntu.com/12.04/serverguide/apt-get.html)
* [Booleanbite](http://booleanbite.com)