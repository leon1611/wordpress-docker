# Práctica # WordPress, contenedores MySQL y phpMyAdmin, conectados mediante red.

## 1. Título

**Práctica No 5**: WordPress y uso de comandos básicos para contenedores MySQL y phpAdmin

## 2. Tiempo de duración

La duración de esta práctica fue de aproximadamente 1 hora y media.

## 3. Fundamentos

En esta práctica, se aprenderán los conceptos básicos sobre la creación y configuración de contenedores Docker para gestionar una base de datos MySQL y una instalación de WordPress, utilizando phpMyAdmin para facilitar la administración de la base de datos. Docker permite la creación de entornos aislados y controlados para ejecutar aplicaciones, y en este caso, se utilizarán para instalar y administrar WordPress junto con su base de datos MySQL.

Durante la práctica, se abarcarán los siguientes conceptos clave:

- **Contenedores Docker:** Son entornos aislados que permiten ejecutar aplicaciones con sus dependencias en un entorno controlado.
    
- **Redes Docker:** Permiten la comunicación entre contenedores, asegurando que los servicios como WordPress y MySQL puedan interactuar sin problemas.
    
- **WordPress:** Es un sistema de gestión de contenido (CMS) que permite crear y administrar sitios web de manera sencilla.
    
- **phpMyAdmin:** Es una herramienta web que permite administrar bases de datos MySQL de forma sencilla y visual.
    

Los siguientes comandos se utilizaron para crear y configurar los contenedores y redes necesarias para el funcionamiento de WordPress:

- **`docker network create`**: Para crear una red personalizada que permita la comunicación entre contenedores.
    
- **`docker run -d \--name wordpress-site \ -v wordpress-data:/var/www/html \-e WORDPRESS_DB_HOST=wordpress-mysql:3306 \-e WORDPRESS_DB_NAME=wordpress \-e WORDPRESS_DB_USER=leon \-e WORDPRESS_DB_PASSWORD=leon1611 \ -p 8000:80 \
  wordpress`**: Para crear un contenedor de WordPress.
    
- **`docker run -d \ --name wordpress-mysql \ -v mysql-data:/var/lib/mysql \ -e MYSQL_ROOT_PASSWORD=leon1611 \ -e MYSQL_DATABASE=wordpress \ -e MYSQL_USER=leon \ -e MYSQL_PASSWORD=leon1611 \ mysql:5.7.`**: Para crear un contenedor de MySQL.
    

## 4. Conocimientos previos

Para realizar esta práctica, es necesario tener conocimientos básicos sobre Docker, la creación y gestión de contenedores, y cómo gestionar bases de datos MySQL. Además, se requiere conocer acerca de  WordPress, sus configuraciones y la gestión de bases de datos en MySQL.

MySQL es un sistema de gestión de bases de datos relacional (RDBMS) de código abierto que utiliza el lenguaje de consulta estructurado (SQL) para acceder y gestionar los datos almacenados en sus bases de datos. MySQL es ampliamente utilizado por desarrolladores web debido a su fiabilidad y velocidad, y es compatible con varios sistemas operativos, como Windows, Linux y macOS. Se usa comúnmente en aplicaciones web y de servidor, y es la base de muchas aplicaciones de código abierto, como WordPress y Drupal, según lo afirma **(Davis, 2015).**

De acuerdo con **(Wikimedia Foundation, 2022)**, phpMyAdmin es una herramienta de administración de bases de datos escrita en PHP, diseñada para facilitar la administración de MySQL y MariaDB a través de una interfaz web. Permite realizar tareas como la creación de bases de datos, la ejecución de consultas SQL, la gestión de tablas y la exportación e importación de datos. Su facilidad de uso y accesibilidad a través de navegadores web lo convierte en una herramienta popular entre los administradores de bases de datos.

WordPress es un sistema de gestión de contenidos (CMS) de código abierto que permite a los usuarios crear y administrar sitios web sin necesidad de conocer código, afirma **(McGrath, 2018)**. Es especialmente popular para la creación de blogs, pero también se utiliza para desarrollar sitios web más complejos. WordPress se basa en PHP y MySQL, lo que le permite ser altamente personalizable a través de plugins y temas, y es utilizado por millones de usuarios en todo el mundo 
## 5. Objetivos a alcanzar

- Crear un contenedor de MySQL con credenciales personalizadas.
    
- Crear un contenedor de WordPress y configurarlo para conectarse a la base de datos MySQL.
    
- Crear una red Docker personalizada para asegurar la comunicación entre los contenedores.
    
- Acceder a phpMyAdmin para gestionar la base de datos MySQL de WordPress
    
- Crear un volumen para WordPress y MySQL.

## 6. Equipo necesario

- Computador con sistema operativo **MacOS 13.7.1**.
    
- **Procesador:** 2,3 GHz Intel Core i5.
    
- **Memoria:** 8 GB.
    
- Conexión a Internet para acceder a los materiales de apoyo y al repositorio de Docker.
    

## 7. Material de apoyo

- Documentación oficial de Docker.
    
- Videos y tutoriales sobre Docker y WordPress.
    
- Foros y comunidades sobre Docker y WordPress.
      
- Material de Apoyo (EVA)

## 8. Procedimiento
---
**Paso 1:** Crear un volumen para MySQL.

Figura 1. **"Comando docker volume create "**.

<img width="470" alt="3" src="https://github.com/user-attachments/assets/cda4a3a0-ee1d-49fc-b18c-f96e0bd552ff" />

---
**Paso 2:** Crear un contenedor para MySQL.

Figura 2. Comando **"docker run -d --name "**.

<img width="566" alt="4" src="https://github.com/user-attachments/assets/28ee6d56-7d68-45ca-baef-422458bb9025" />

---
**Paso 3:** Crear un volumen para WordPress .

Figura 3. Comando **"Comando docker volume create"**.

<img width="519" alt="2" src="https://github.com/user-attachments/assets/7f16d09e-648f-47fb-9bb9-3eb22817a1ff" />

---
**Paso 4:** Crear una red personalizada llamada `wordpress-net`.

Figura 4. Comando **"docker network create wordpress-net"**.

<img width="539" alt="1" src="https://github.com/user-attachments/assets/3d5a2585-a93c-48b7-b8a3-910acee5d8fc" />

---
**Paso 5:** Crear un contenedor para phpMyAdmin.

Figura 5. Comando **"docker run -d --name phpmyadmin"**.

<img width="569" alt="5" src="https://github.com/user-attachments/assets/1498b2d5-3a5b-4117-bc30-a05860473fe6" />

---
**Paso 6:** Crear un contenedor para WordPress .

Figura 6. Comando **"docker run -d --name wordpress "**.

<img width="566" alt="6" src="https://github.com/user-attachments/assets/a6b24a66-6550-47a6-ac22-01409309692a" />

---
**Paso 7:** Conectar los contenedores a la red personalizada `wordpress-net`.

Figura 7. Comando **"docker network connect wordpress-net "**.

<img width="705" alt="7" src="https://github.com/user-attachments/assets/ee67fc7f-78cd-4741-9ad1-fe77084aee69" />


---
## 9. Resultados esperados

La práctica permitió crear y gestionar contenedores Docker para WordPress y MySQL, y aprender a conectar estos contenedores entre sí mediante una red personalizada en Docker. 

<img width="1047" alt="dockers" src="https://github.com/user-attachments/assets/9972866b-d0df-4ed0-bf58-385246f4be2d" />
<img width="533" alt="vols" src="https://github.com/user-attachments/assets/133a7f6d-537d-49af-b2fe-b9bb3811b944" />  



<img width="382" alt="redes" src="https://github.com/user-attachments/assets/d79f76fe-0fd1-4fcd-bd63-73cc306e0c7f" />  



Después de completar todos los pasos, se logró configurar un entorno funcional de WordPress con su base de datos, y se pudo acceder correctamente al panel de administración en `http://localhost:8000` para realizar la instalación y configuración inicial del sitio.  


<img width="1060" alt="8" src="https://github.com/user-attachments/assets/9b25b33d-6201-4649-a4c5-243dfdc0d53b" />  


Además, al acceder a phpMyAdmin mediante `http://localhost:8080`, fue posible visualizar y administrar la base de datos de WordPress de forma sencilla y gráfica, facilitando la gestión de tablas, usuarios y datos relacionados al sitio web.

<img width="1059" alt="9" src="https://github.com/user-attachments/assets/a6ecda41-e103-4d5d-aa16-54d393aafd49" />

La creación de una red personalizada en Docker garantizó una comunicación eficiente y segura entre los contenedores de WordPress, MySQL y phpMyAdmin.


## 10. Bibliografía

- Davis, P. (2015). _MySQL: The comprehensive guide to building, programming, and administering MySQL databases_. O'Reilly Media.
    
- Docker Documentation. (2025). _Docker: Documentation_. Recuperado de [https://docs.docker.com](https://docs.docker.com)
    
- McGrath, M. (2018). _WordPress for dummies_. Wiley.
    
- phpMyAdmin Development Team. (2025). _phpMyAdmin: MySQL Administration_. Recuperado de [https://www.phpmyadmin.net/](https://www.phpmyadmin.net/)
    
- Wikimedia Foundation. (2022). _phpMyAdmin_. Recuperado de [https://www.phpmyadmin.net/](https://www.phpmyadmin.net/)
    
- WordPress. (2025). _WordPress Codex_. Recuperado de [https://wordpress.org](https://wordpress.org)
