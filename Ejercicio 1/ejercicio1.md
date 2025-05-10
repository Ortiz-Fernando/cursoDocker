# Tarea Evaluable Docker - Ejercicio 1

> Ejercicio 1 - Contenedores en red y Docker
> Desktop
>
> Realizado por ORTIZ GONZALEZ Fernando

[TOC]

## Configuraciones previas

Se debe crear un repositorio GitHub - debe ser público:

[Visualizar repositorio público aquí](https://github.com/Ortiz-Fernando/cursoDocker)

- Creación del repositorio en GitHub

![new-rep-git](./ejercicio1.assets/new-rep-git.JPG)

- Clonar repositorio en carpeta local

![clone-a-local-rep-git](./ejercicio1.assets/clone-a-local-rep-git.JPG)

- Configuración de ramas para cada ejercicio y su commit al repositorio.

![](./ejercicio1.assets/commit-local-carp-ejerc.JPG)



## 1. Crea una red bridge `redej1`

Luego de instalar la extension solicitada en los *pasos previos*  para la realizacion del ejercicio 1. Dentro de la extensión abrimos el panel de *network* y procedemos a crear la rede de tipo *bridge*`redej1`. En la misma se conectaran los contenedores creados posteriormente.



![ej-1-add-net](./ejercicio1.assets/ej-1-add-net.JPG)

![ej-1-create-net](./ejercicio1.assets/ej-1-create-net.JPG)

![ej-1-created-redej1](./ejercicio1.assets/ej-1-created-redej1.JPG)

## 2. Crea un contenedor con una imagen de ``mariaDB`` 

Crea un contenedor con una imagen de mariaDB que estará en la red **redej1** . Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306.

Se realiza una descarga de la imagen mariaDB del DockerHub y luego se genera el contenedor (*run*) comom se muestra en las imágenes.

![ej-1-container-run-mariadb](./ejercicio1.assets/ej-1-container-run-mariadb.JPG)

![ej-1-image-mariadb](./ejercicio1.assets/ej-1-image-mariadb.JPG)



- Definir una contraseña para el usuario root (elegimos *root*) , y un usuario con tu nombre de pila **fernando** y con contraseña **123123**. La BD por defecto será **DAW**

  

  ![ej-1-container-create-mariadb](./ejercicio1.assets/ej-1-container-create-mariadb.JPG)

  

- Genera un *script SQL* que cree una tabla *módulos* con algunos registros con los nombres de los módulos que estás estudiando (DIW, DWES, DWEC)

```sql
CREATE TABLE modulos (
id INT AUTO_INCREMENT PRIMARY KEY,
nombre VARCHAR(50) NOT NULL
);
INSERT INTO modulos (nombre) VALUES
('DIW'),
('DWEC'),
('DWES'),
('DAW');

```



## 3. Crear un contenedor con ``Adminer``

- Crear un contenedor con ``Adminer`` que se pueda conectar al contenedor de la BD.

  

  ![ej-1-image-adminer](./ejercicio1.assets/ej-1-image-adminer.JPG)

  ![ej-1-container-adminer](./ejercicio1.assets/ej-1-container-adminer.JPG)

- Descargamos la imagen correspondiente del Hub y luego *corremos* el nuevo contenedor y realizamos la conexión a la red junto a el contenedor de **mariaDB**.

  ![ej-1-containers-connected-visualizer-redej1](./ejercicio1.assets/ej-1-containers-connected-visualizer-redej1.JPG)

  ![ej-1-containers-connected-redej1](./ejercicio1.assets/ej-1-containers-connected-redej1.JPG)





## 4. Mostrar BD y tablas creadas

Desde la interfaz gráfica elegida, conéctate a la BD con tu usuario personal, ejecuta el script con los datos de los módulos y muestra la BD y la tabla creados

​		![ej-1-adminer-db](./ejercicio1.assets/ej-1-adminer-db.JPG)

​		

![ej-1-adminer-db-modif](./ejercicio1.assets/ej-1-adminer-db-modif.JPG)

​		![ej-1-adminer-db-modif-select](./ejercicio1.assets/ej-1-adminer-db-modif-select.JPG)



## 5. Opcion elegida: Disk Usage

- Instala la extensión **Disk Usage**. 

- Muestra el espacio ocupado.

  ![ej-1-disk-usage](./ejercicio1.assets/ej-1-disk-usage.JPG)

- Borramos red, contenedores y volumen ocupado por las persistencias.

  ![ej-1-delete-container](./ejercicio1.assets/ej-1-delete-container.JPG)

  ![ej-1-disk-usage-deleted](./ejercicio1.assets/ej-1-disk-usage-deleted.JPG)

​	

Se puede observar la diferencia en *Containers* y el *Total Size* que analiza la extensión para observar la eliminación de archivos, imágenes, red y contenedores.



