# 1-HTTPS-con-Let-s-Encrypt-Docker-y-Docker-Compose

En esta primera práctica de ejemplo se busca desplegar mediante un archivo **.yml** de **docker-compose** desplegar un sitio web de **prestashop** haciendo uso de **HTTPS-PORTAL** que es una imagen **Docker** que contiene un servidor **HTTPS** totalmente automatizado que hace uso de las tecnologías **Nginx** y **Let’s Enctrypt**. Los certificados **SSL** se obtienen y renuevan de Let’s Encrypt **automáticamente**.

 # Estructura de Directorios:

```
    │   ├── .env
    │   ├── docker-compose.yml

```
 ## 1. Archivo de variables:

 Dentro de el archivo **.env** estás serán las únicas variables que hará falta en este caso tener:
 
```
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=prestashop
MYSQL_USER=ps_user
MYSQL_PASSWORD=ps_password
```
