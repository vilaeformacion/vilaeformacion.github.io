---
layout: post
title:  "Tema 6: Creacion y Configuración Servidor Web"
date:   2016-03-31 00:00:00
curso: 1
categories: web,servidor
---

Tras familiarizarnos con la consola de comandos, ya estamos en disposición de instalar servicios en nuestro entorno Linux. Como por ejemplo crear nuestro propio servidor web. Además de otros servicios como una base de datos que utilizaremos para nuestras webs.

En este apartado, instalaremos un servidor web apache2 junto a un servidor de base de datos mysql con soporte para php.

### Apache2

Empezaremos instalando el servidor web apache2. El servidor apache2 nos permite acceder a nuestras páginas web que podamos tener instaladas en nuestra Raspberry Pi.

Para instalar el servidor web utilizaremos el comando _apt-get_.

```
pi@zerasul:~$ sudo apt-get install apache2
```

Aceptamos la instalación y si todo va bien tendremos nuestro servidor ya instalado. Para probar que realmente funciona nuestro servidor web, utilizaremos un navegador web y accederemos a la siguiente dirección:

[http://localhost/](http://localhost)

Si todo esta correctamente instalado, accederemos a la página de prueba del servidor web.

![imagenapache]({{ site.url }}/resources/tema6/apache2.png)

Con esto ya podemos crear nuestra propia página web usando html básico. Para poder modificar esta página de prueba y además poder crear nuestras propias webs, tenemos que acceder a la carpeta _/var/www/html_.

Sin embargo, necesitaremos instalar algo más para poder crear páginas dinámicas; que son necesarias para aplicaciones como _Wordpress_, o _Prestashop_. Para instalar php, utilizaremos el siguiente comando.

```
pi@zerasul:~$ sudo apt-get install php5 libapache2-mod-php5 php5 php5-mcrypt
```

Esto instalara PHP, y las liberías necesarias de este.

Tras instalar esto, pasaremos a instalar el servidor de base de datos Mysql.

### Mysql

Mysql es un servidor de base de datos que nos permitirá almacenar la información de nuestras webs. Para instalar el servidor Mysql, ejecutaremos el siguiente comando:

```
pi@zerasul:~$ sudo apt-get install mysql-server mysql
```

Durante la instalación se nos pedirá introducir 2 veces la contraseña del usuario root de la base de datos. **Es importante guardarla**.

![mysqlroot]({{ site.url }}/resources/tema6/mysqlroot.png)

Tras instalar el servidor, podemos acceder a el con el siguiente comando.

```
pi@zerasul:~$mysql -u root -p
```
e introducimos la contraseña que hemos puesto antes. Para salir simplemente pondremos _exit_.

Sin embargo, vamos a instalar algo más para acceder a nuestras bases de datos de forma visual; sin necesidad de aprender comandos extensos. Por lo que instalaremos _phpmyadmin_. Para instalar _phpmyadmin_ ejecutaremos el siguiente comando.

```
pi@zerasul:~$ sudo apt-get install phpmyadmin php5-mysql
```

Durante la instalación tendreos que introducir la contraseña de root que hemos introducido anteriormente. Además de seleccionar el servidor web correspondiente. En este caso, apache2.

![seleccionarserver]({{ site.url }}/resources/tema6/phpmyadmin.png)

Tras terminar la instalación, accederemos a través de un navegador con la siguiente dirección:

[http://localhost/phpmyadmin](http://localhost/phpmyadmin)

Accederemos como usuario root y contraseña la que hemos introducido antes.

![phpmyadmin]({{ site.url }}/resources/tema6/phpmyadmin2.png)

Tras terminar esto, vamos a crear una base de datos. la cual llamaremos _wordpress_. Para ello hacemos click en bases de datos, introducimos el nombre en el campo de texto y hacemos click en crear.

**NOTA**: Si no esta en español por defecto puede cambiarse el lenguaje en el desplegable que aprece en appareance.

![phpmyadminbasededatos]({{ site.url }}/resources/tema6/phpmyadmin3.png)

### Wordpress

Para comprobar que nuestro servidor esta listo, vamos a instalar un blog usando wordpress. Para ello lo primero que haremos será descargarlo; lo cual lo haremos con el comando _wget_.

```
pi@zerasul:~$ wget https://es.wordpress.org/wordpress-4.4.2-es_ES.tar.gz
```

![wordpressdescarga]({{ site.url }}/resources/tema6/wordpress1.png)

Tras descargarlo, descomprimimos el contenido usando _tar_.


```
pi@zerasul:~$ tar xvf wordpress-4.4.2-es_ES.tar.gz
```

Tras descomprimirlo vamos a copiar la carpeta wordpress al directorio _/var/www_.

Por supuesto, necesitaremos permisos de superadministrador para hacerlo.

```
pi@zerasul:~$ sudo cp -R wordpress /var/www/html
```

Para tener todos los permisos de escritura desde el servidor web, vamos a añadir como usuario propietario al usuario _www-data_ y con el grupo _www-data_ esto se realiza con la orden _chown_.

```
pi@zerasul:~$ sudo chown -R www-data:www-data /var/www/html/wordpress
```

Tras esto, ya podemos pasar al instalador de wordpress. Para ello accederemos a la siguiente dirección en nuestro navegador.

[http://localhost/wordpress](http://localhost/wordpress)


![wordpressinstalador]({{ site.url }}/resources/tema6/wordpress2.png)


En primer lugar, aparecerán los datos de la base de datos.

Pondremos los datos de nuestra base de datos. DE usuario _root_; de contraseña la contraseña que hemos introducido anteriormente y de base de datos introduciremos _wordpress_ que es el nombre de la base de datos que hemos añadido anteriormente.

![wordpress base de datos]({{ site.url }}/resources/tema6/wordpress3.png)

Tras poner esto, seguiremos las instroducciones de pantalla y en el último paso añadiremos los datos de nuestro usuario administrador. 

Para acceder a nuestra web, accederemos a la siguiente dirección [http://localhost/wordpress](http://localhost/wordpress)

![wordpress final]({{ site.url }}/resources/tema6/wordpress5.png)


Esta ha sido la última leccion de este curso de introducción a Linux usando Raspbian y la Raspberry Pi. Esperemos que haya disfrutado. En breve habrá más cursos en Vilae Formación.

### Referencias

* [apache2](https://httpd.apache.org)
* [mysql](https://www.mysql.com)
* [pypmyadmin](https://www.phpmyadmin.net)
* [wordpress](https://es.wordpress.org)
* [booleanbite](http://booleanbite.com)