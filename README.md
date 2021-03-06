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


Cuando se complete la instalación deberemos borrar el directorio install, esto lo hacemos entrando en el contenedor Docker de Prestashop y eliminando la carpeta install desde ahí.

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
