# Practica-Prestashop
En esta práctica lo que se va a hacer es crear una tienda de Prestashop mediante contenedores Docker.

## Instalación Docker y Docker-Compose
Para poder llevar a cabo esta práctica hay que tener instalada las herramientas de Docker y Docker-compose, esto lo haremos mediante los siguientes comandos:

- Actualizamos repositorios:
```
sudo apt update
sudo apt upgrade -y
```

- Instalamos las utilidades:
```
 apt install docker docker-compose
```

- Habilitamos e iniciamos el servicio Docker para que se arranque cada vez que iniciemos el sistema:
```
sudo systemctl enable docker
sudo systemctl start docker
```

- Para evitar estar siempre poniendo el comando sudo al usar Docker metemos al usuario en el grupo de usuarios Docker:
```
sudo usermod -aG docker $USER
```

## Ejecución Docker-Compose
Docker-compose permitque que creemos un archivo de configuracion para que mediante un comando levantemos toda la infraestructura que tenemos creada dentro del archivo `docker-compose.yml`.

El comando que consigue poner en marcha todas las instalaciones es el siguiente: `docker-compose up`

Se pueden y es recomendable hacer uso de variables para no tener que escribir los parametros a cada rato, para poder usarlas necesitamos un archivo `.env` que se encontrará en la misma carpeta que el `docker-compose.yml`

## Instalación y puesta en marcha de Prestashop
Para llevar a cabo la instalación hay que seguir los pasos que se ven en las siguientes capturas

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/install.PNG?token=AOMWPNJCJXWEQ5SBBBUW3MTAIN25G)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/install2.PNG?token=AOMWPNOUY5T54U7YPA5UUOTAIN26C)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/info.PNG?token=AOMWPNLOJONEZNXYHH5GSEDAIN3EA)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/datosbd.PNG?token=AOMWPNLYRHPTFT2SFJYOK3DAIN3FO)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/fininstall.PNG?token=AOMWPNPKNLXMIYG7DY2TPTTAIN3HI)


Cuando se complete la instalación deberemos borrar el directorio install, esto lo hacemos entrando en el contenedor Docker de Prestashop y eliminando la carpeta install desde ahí.

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/rm-install.PNG?token=AOMWPNLXAUTEE2UY5JPUEM3AIN2YO)

Después de esto entramos en el sitio y en la sección de administración.

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/prestashop.PNG?token=AOMWPNKHLDRJ6YKN4O6CKM3AIN3LW)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/admin1.PNG?token=AOMWPNPTES5TKFKWNIFVUUTAIN3MQ)

![](https://raw.githubusercontent.com/joseean29/Practica-Prestashop/main/images/admin2.PNG?token=AOMWPNPR65WLT6QTPQJ22W3AIN3NS)


## Credenciales e IP
```
correo: josean@demo.com
contraseña: asir2aJAAJ
```

```
base de datos: mysql
usuario: ps_user
contraseña: ps_password
```

IP:
