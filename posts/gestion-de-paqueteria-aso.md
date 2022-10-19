---
title: "Ejercicios gestión de paquetería"
description: Vamos a trabajar con ejercicios sobre paquetería.
date: 2022-10-18
tags:
  - ASO
layout: layouts/post.njk
---


# Trabajo con apt, aptitude, dpkg
#### Prepara una máquina virtual con Debian bullseye, realizar las siguientes acciones:

### 1. Que acciones consigo al realizar apt update y apt upgrade. Explica detalladamente.

Al hacer un apt update, actualizas la lista de paquetes que hay disponible y sus versiones en los repositorios aunque no realiza ninguna instalación.
Después de hacer un apt update, hay que hacer un apt upgrade, permite instalar si no tiene instalado y actualiza versiones de los paquetes ya instalados.

### 2. Lista la relación de paquetes que pueden ser actualizados. ¿Qué información puedes sacar a tenor de lo mostrado en el listado?.

Para mostrar los paquetes que pueden ser instalados, se usa el siguiente comando:

```diff-js
# sudo apt list --upgradable
```
Muestro captura del comando ejecutado en mi máquina.
![img](/img/ASO-P3.1.png)

En la línea el resaltado verde apunta al nombre del paquete. oldstable indica que no es de la versión stable de debian(esa máquina es debian buster). Los números siguientes indican la versión del paquete y lo siguiente a la arquitectura del paquete(amd64).

### 3. Indica la versión instalada, candidata así como la prioridad del paquete openssh-client.

Para ver la versión instalada y la candidata de un paquete usamos el siguiente comando: 
```diff-js
# sudo apt policy openssh-client
```
En la siguiente captura veremos la ejecución del comando:
![img](/img/ASO-P3.2.png)

Como indica la imagen, la versión instalada es la 1.7.9, la candidata es la misma y la prioridad es 500. 

### 4. ¿Cómo puedes sacar información de un paquete oficial instalado o que no este instalado?

para ver información de un paquete oficial instalado, usariamos dpkg -s nombre_paquete.

Si no está instalado, se puede ver información de un paquete usando apt show nombre_paquete

### 5. Saca toda la información que puedas del paquete openssh-client que tienes actualmente instalado en tu máquina.

### 6. Saca toda la información que puedas del paquete openssh-client candidato a actualizar en tu máquina.

### 7. Lista todo el contenido referente al paquete openssh-client actual de tu máquina. Utiliza para ello tanto dpkg como apt.

### 8. Listar el contenido de un paquete sin la necesidad de instalarlo o descargarlo.

### 9. Simula la instalación del paquete openssh-client.

### 10. ¿Qué comando te informa de los posible bugs que presente un determinado paquete?

### 11. Después de realizar un apt update && apt upgrade. Si quisieras actualizar únicamente los paquetes que tienen de cadena openssh. ¿Qué procedimiento seguirías?. Realiza esta acción, con las estructuras repetitivas que te ofrece bash, así como con el comando xargs.

### 12. ¿Cómo encontrarías qué paquetes dependen de un paquete específico.

### 13. ¿Cómo procederías para encontrar el paquete al que pertenece un determinado fichero?

### 14. ¿Que procedimientos emplearías para liberar la caché en cuanto a descargas de paquetería?

### 15. Realiza la instalación del paquete keyboard-configuration pasando previamente los valores de los parámetros de configuración como variables de entorno.

### 16. Reconfigura el paquete locales de tu equipo, añadiendo una localización que no exista previamente. Comprueba a modificar las variables de entorno correspondientes para que la sesión del usuario utilice otra localización.

### 17. Interrumpe la configuración de un paquete y explica los pasos a dar para continuar la instalación.

### 18. Explica la instrucción que utilizarías para hacer una actualización completa de todos los paquetes de tu sistema de manera completamente no interactiva

### 19. Bloquea la actualización de determinados paquetes.

# Trabajo con ficheros .deb

### 1. Descarga un paquete sin instalarlo, es decir, descarga el fichero .deb correspondiente. Indica diferentes formas de hacerlo.

### 2. ¿Cómo puedes ver el contenido, que no extraerlo, de lo que se instalará en el sistema de un paquete deb?
 
### 3. Sobre el fichero .deb descargado, utiliza el comando ar. ar permite extraer el contenido de una paquete deb. Indica el procedimiento para visualizar con ar el contenido del paquete deb. Con el paquete que has descargado y utilizando el comando ar, descomprime el paquete. ¿Qué información dispones después de la extracción?. Indica la finalidad de lo extraído.

### 4. Indica el procedimiento para descomprimir lo extraído por ar del punto anterior. ¿Qué información contiene?

# Trabajo con repositorios

### 1. Añade a tu fichero sources.list los repositorios de bullseye-backports y sid.

### 2. Configura el sistema APT para que los paquetes de debian bullseye tengan mayor prioridad y por tanto sean los que se instalen por defecto.

### 3. Configura el sistema APT para que los paquetes de bullseye-backports tengan mayor prioridad que los de unstable.

### 4. ¿Cómo añades la posibilidad de descargar paquetería de la arquitectura i386 en tu sistema. ¿Que comando has empleado?. Lista arquitecturas no nativas. ¿Cómo procederías para desechar la posibilidad de descargar paquetería de la arquitectura i386?

### 5. Si quisieras descargar un paquete, ¿cómo puedes saber todas las versiones disponible de dicho paquete?

### 6. Indica el procedimiento para descargar un paquete del repositorio stable.

### 7. Indica el procedimiento para descargar un paquete del repositorio de buster-backports.

### 8. Indica el procedimiento para descargar un paquete del repositorio de sid.

### 9. Indica el procedimiento para descargar un paquete de arquitectura i386.

# Trabajo con directorios

### 1. Que cometidos tienen:

/var/lib/apt/lists/

/var/lib/dpkg/available

/var/lib/dpkg/status

/var/cache/apt/archives/
