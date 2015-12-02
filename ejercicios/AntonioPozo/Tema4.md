###Ejercicio 1
**Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 1.0.**

Instalamos la última versión disponible con: sudo apt-get -t trusty-backports install lxc
Para comprobar la versión instalada tecleamos lxc-ls --version. 
En mi caso, tengo instalada la versión 1.1.5

###Ejercicio 2
**Comprobar qué interfaces puente se han creado y explicarlos.**

Creamos un contenedor: sudo lxc-create -t ubuntu -n una-caja
![exito instalacion](http://s2.subirimagenes.com/imagen/previo/thump_9491377success.png)

Una vez creado, lo iniciamos: sudo lxc-start -n una-caja
Vemos las interfaces creadas:
La siguiente interfaz es la que conecta el contenedor con Internet.
![salida ifconfig interfaz1](http://s2.subirimagenes.com/imagen/previo/thump_9491378ifconfig.png)
Y ésta la que se utiliza para conexión entre contenedores.
![salida ifconfig interfaz2](http://s2.subirimagenes.com/imagen/previo/thump_9491379ifconfig2.png)




###Ejercicio 3
**1. Crear y ejecutar un contenedor basado en Debian.**

Lo creamos con: sudo lxc-create -t debian -n otra-caja

**2. Crear y ejecutar un contenedor basado en otra distribución, tal como Fedora. Nota En general, crear un contenedor basado en tu distribución y otro basado en otra que no sea la tuya. Fedora, al parecer, tiene problemas si estás en Ubuntu 13.04 o superior, así que en tal caso usa cualquier otra distro. Por ejemplo, Óscar Zafra ha logrado instalar Gentoo usando un script descargado desde su sitio, como indica en este comentario en el issue.**

###Ejercicio 4
**1. Instalar lxc-webpanel y usarlo para arrancar, parar y visualizar las máquinas virtuales que se tengan instaladas.**

**2. Desde el panel restringir los recursos que pueden usar: CPU shares, CPUs que se pueden usar (en sistemas multinúcleo) o cantidad de memoria.**

###Ejercicio 5
**Comparar las prestaciones de un servidor web en una jaula y el mismo servidor en un contenedor. Usar nginx.**

###Ejercicio 6
**Instalar docker.**


###Ejercicio 7
**1. Instalar a partir de docker una imagen alternativa de Ubuntu y alguna adicional, por ejemplo de CentOS.**

**2. Buscar e instalar una imagen que incluya MongoDB.**


###Ejercicio 8
**Crear un usuario propio e instalar nginx en el contenedor creado de esta forma.**


###Ejercicio 9
**Crear a partir del contenedor anterior una imagen persistente con commit.**


###Ejercicio 10
**Crear una imagen con las herramientas necesarias para el proyecto de la asignatura sobre un sistema operativo de tu elección.**