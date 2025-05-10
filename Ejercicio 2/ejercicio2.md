# Ejercicio 2 - Docker Compose

> Este ejercicio se puede resolver utilizando comandos, o Docker Desktop,
> o combinando ambos
> Explorar la imagen de la aplicación FileBrowser en este repositorio en
> GitHub: https://hub.docker.com/r/hurlenko/filebrowser
> El usuario por defecto es admin con contraseña 'admin'
>
> Realizado por ORTIZ GONZALEZ Fernando

----------------------------

--- **TABLA DE CONTENIDOS** ---

[TOC]

-----------------------------------

## Aplicación FileBrowser

Explicación breve de cómo funciona esta aplicación y qué hace.

La aplicación permite gestionar y visualizar archivos y directorios desde un navegador web (localhost en este caso), como si fuera un explorador de archivos (parecido al *Explorador de Windows* , permitiendo subir, descargar, renombrar y eliminar archivos. Además, se puede compartir, limitar el acceso por contraseña, crear usuarios y privilegios, limitar el tiempo que se comparte y muchas otras funciones. 

## Escribir un fichero ``compose.yaml``

1. Escribir un fichero ``compose.yaml`` para desplegarla. Los datos se pueden guardar utilizando volúmenes (/config) y utilizando bind-mount (/data).

​	![2-archivo-yaml](./ejercicio2.assets/2-archivo-yaml.JPG)



![2-composefile-filebrowser](./ejercicio2.assets/2-composefile-filebrowser.JPG)



## Almacenamiento en FileBrowser

- Captura de pantalla donde se vean los volúmenes/carpetas donde se han almacenado los datos.

![2-container-volume-and-mounts](./ejercicio2.assets/2-container-volume-and-mounts.JPG)



## Cambios en FileBrowser

- Captura de pantalla donde se vea la aplicación funcionando, sube algún fichero, cambia el lenguaje a español, cambio de tema a colores claros.

​	

![2-container-ej2-nav](./ejercicio2.assets/2-container-ej2-nav.JPG)

![2-filebrowser-create-files](./ejercicio2.assets/2-filebrowser-create-files.JPG)

![2-filebrowser-files-volume](./ejercicio2.assets/2-filebrowser-files-volume.JPG)



![2-filebrowser-config-change](./ejercicio2.assets/2-filebrowser-config-change.JPG)









