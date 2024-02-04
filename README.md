# 1-HTTPS-con-Let-s-Encrypt-Docker-y-Docker-Compose

En esta primera práctica de ejemplo se busca desplegar mediante un archivo **.yml** de **docker-compose** desplegar un sitio web de **prestashop** haciendo uso de **HTTPS-PORTAL** que es una imagen **Docker** que contiene un servidor **HTTPS** totalmente automatizado que hace uso de las tecnologías **Nginx** y **Let’s Enctrypt**. Los certificados **SSL** se obtienen y renuevan de Let’s Encrypt **automáticamente**.

 # Estructura de Directorios:

```
    │   ├── .env
    │   ├── docker-compose.yml

```

## 1. Pasos previos a realizar:

Antes de nada deberemos de realizar la instalación de **docker** y **docker-compose**, no sin antes lanzar este comando:

```
sudo apt update && sudo apt upgrade -y
```
Aquí procedo con la instalación de **docker.io**; paquete que proporciona la versión oficial de **Docker** y **docker-compose**:

```
sudo apt install docker.io docker-compose -y
```
Habilitamos **Docker**:
```
sudo systemctl enable docker
```
Y lo iniciamos por si no se ha llegado a empezar:

```
sudo systemctl start docker
```
Mediante el siguiente comando agregamos al usuario **ubuntu** al grupo **docker** para que pueda usar comandos de docker si hacer uso de **sudo**:

```
sudo usermod -aG docker ubuntu
```
Útil para que el usuario pueda cambiar de grupo sin tener que cerrar la sesión actual:

```
newgrp docker
```
 ## 2 Archivo de variables:

 Dentro de el archivo **.env** estás serán las únicas variables que hará falta en este caso tener:
 
```
MYSQL_ROOT_PASSWORD=root
MYSQL_DATABASE=prestashop
MYSQL_USER=ps_user
MYSQL_PASSWORD=ps_password
```
 ## 3 Explicación del archivo docker-compose.yml:
