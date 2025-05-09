# Ejercicio 3 - imagen con Dockerfile -
Aplicación web

> Para la realización de este ejercicio es necesario tener una cuenta en
> Docker Hub.
> Este ejercicio se puede resolver utilizando comandos, o Docker Desktop,
> o combinando ambos
>
> Realizado por ORTIZ GONZALEZ Fernando

----------------------------

--- **TABLA DE CONTENIDOS** ---

[TOC]

-----------------------------------

## Escribir un fichero ``Dockerfile``

Necesitamos un fichero **Dockerfile** que automatice las siguientes
operaciones para crear una imagen que contenga un servidor con un sitio
web y un script php. Características de la imagen:

- Usa un contenedor que ejecute una instancia de la imagen ``php:7.4-
  apache`` , que se llame ``ejercicio3`` y que sea accesible desde un
  navegador en el puerto 8000.
- Coloca en el directorio raíz del servicio web ( ``/var/www/html`` ) un "sitio
  web" donde figure tu nombre - el sitio deberá tener al menos un
  archivo``index.html`` sencillo y un archivo ``.css``
- Coloca en ese mismo directorio raíz el siguiente script php , llámalo
  ``fecha.php``



```php
<?php
setlocale(LC_TIME, "es_ES.UTF-8");
$mes_actual = strftime("%B");
$fecha_actual = date("d/m/Y");
$hora_actual = date("H:i:s");
echo "<h1>Información< h1>";
echo "<p>Hoy es $fecha_actual< p>";
echo "<p>El mes es: <strong>$mes_actual< strong>< p>";
echo "<p>Hora: $hora_actual< p>";
?>
```



- Ver la salida del script ``fecha.php`` y de la página ``index.html`` en el
  navegador.



## Subir a la cuenta de Docker Hub

**Una vez creada la imagen, súbela a tu cuenta de Docker Hub**

- Borra la imagen de tu Docker local
- Baja ('pull') de tu cuenta la imagen que acabas de subir
- Muestra las imágenes que tienes
- Ejecuta un contenedor usando esa imagen



## Capturas de pantalla

Deberás entregar, al menos, las siguientes capturas de pantalla, los
comandos empleados y/o operaciones con Docker Desktop para resolver
cada apartado:

- creación inicial del contenedor - documenta los pasos hasta el borrado del mismo
- bloque de código con el **Dockerfile**
- creación de la nueva imagen.
- subida de la imagen a tu cuenta de Docker Hub.
- operación de **'pull'** de la imagen de Docker Hub
- creación de un nuevo contenedor con esa imagen y su ejecución. Cambia el puerto del contenedor, por ejemplo, ``- p 1234:80``
- el acceso al navegador con la página ``html`` y con el script ``php``





## Videoclip

**Realiza un videoclip con el siguiente contenido:**

- Preséntate, debe verse tu cara
- Entra en GitHub y muestra tu repositorio
- Escoge uno de los tres ejercicios y resuelve alguno de los puntos solicitados, por ejemplo, del ejercicio 1, muestra que se están ejecutando los dos contenedores y conéctate a la BD utilizando tu usuario personal