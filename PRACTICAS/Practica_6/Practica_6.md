# PRACTICA 6
# DISCOS EN RAID.

**1.Añadimos dos disco nuevos en la máquina mientras esta se encuentre apagada.**
  
  foto 1.1

**2. Instalamos el software necesario con el comando:**

     sudo apt-get install mdadm

**3. Podemos ver en la siguiente imagen la informacion de los discos, que se mostrará con el comando:**

     sudo fdisk -l 

     foto 1.2

**4. Creamos el RIAD1:

     FOTO 1.3

**5. Damos formato al RAID1:**

     foto 1.4

**6. Creamos el direcctorio donde se montará el RAID:**

     foto 1.5.

** y Comprobamos que se ha creado correctamente con el comando:**

     sudo mount

     foto 1.6


**7. Comprobamos el estado del RAID con el comando: **

     sudo mdadm --detail /dev/md0

**8. Para terminar el proces, necesitamos configurar el sistema para que se monte el dispositivo RAID al arrancar el sistema.**
** Para ello hay que editar el fichero /etc/fstab.**
** Utilizaremos para ello el UUID de cada dispositivo en lugar de su nombre, y para ello haremos lo siguiente:**

   foto 1.8

** Utilizaremos el UUID de nuestro RAID, que en nuestro caso es el primero.**

** Ahora en el fichero /etc/fstab añadimos al final del archivo la linea correspondiente y se finaliza el proceso de creacion.**

   foto 1.9



**9. Simulacion de un fallo en uno de los discos.**

**10. Retirar "en caliente" el disco que esta marcado como que ha fallado.**

**11. Añadir "en caliente" un nuevo disco que reemplazaría al disco que hemos retirado.**
 