# Apache

## Introducción
El servidor HTTP Apache es un servidor web HTTP de código abierto, para múltiples
plataformas que implementa el protocolo HTTP/1.1 La funcionalidad principal de este
servicio web es servir a los usuarios todos los ficheros necesarios para visualizar la
web. Siguiendo los pasos de la memoria, se podrá instalar y utilizar Apache sin
problemas.
### Índice
- Instalación de Apache
- Ajustar el firewall
- Comprobar su servidor web
#### Instalación de Apache
En los repositorios de software de Ubuntu disponemos de Apache, lo que nos permitirá
instalarlo con la administración de paquetes. Lo primero que tenemos que hacer es
actualizar los paquetes con:
```
$ sudo apt update
```
Seguido de la intalación del paquete de apache:
```
$ sudo apt install apache2
```
#### Ajustar el firewall
Es necesario modificar lo ajustes de firewall para permitir el acceso externo a los
puertos predeterminados. Siguiendo los pasos anteriores, se tiene un firewall UFW
configurado para restringir el acceso al servidor
Para mostrar los perfiles de aplicación:
```
$ sudo ufw app list
```
Seguido deberemos habilitar el tráfico en el puerto 80:
```
$ sudo ufw allow 'Apache'
```
Para verificarlo:
```
$ sudo ufw status
```
Si lo tenemos deshabilitado:
```
$ sudo ufw enable
```
#### Comprobar su servidor web
Al final de este proceso, ya estará la instalación de Apache y el servidor web ya está
activo, para comprobar podemos usar este comando:
```
$ sudo systemctl status apache2
```
Otra forma de comprobar que funciona:
```
$ hostname -I
```
Con este comando obtendremos nuetra IP y la tendremos que poner en nuestro navegador
escribiendo esta dirección:
```
http://your_server_ip
```

## Configuración
