# PRACTICA 6
# DISCOS EN RAID.

**1.Añadimos dos disco nuevos en la máquina mientras esta se encuentre apagada.**
  
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.1.PNG)

**2. Instalamos el software necesario con el comando:**

     sudo apt-get install mdadm

**3. Podemos ver en la siguiente imagen la informacion de los discos, que se mostrará con el comando:**

     sudo fdisk -l 

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.2.PNG)

**4. Creamos el RIAD1:

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.3.PNG)

**5. Damos formato al RAID1:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.4.PNG)     

**6. Creamos el direcctorio donde se montará el RAID:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.5.PNG)

** y Comprobamos que se ha creado correctamente con el comando:**

     sudo mount

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.6.PNG)


**7. Comprobamos el estado del RAID con el comando: **

     sudo mdadm --detail /dev/md0
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.7.PNG)

**8. Para terminar el proces, necesitamos configurar el sistema para que se monte el dispositivo RAID al arrancar el sistema.**
** Para ello hay que editar el fichero /etc/fstab.**
** Utilizaremos para ello el UUID de cada dispositivo en lugar de su nombre, y para ello haremos lo siguiente:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.8.PNG)

** Utilizaremos el UUID de nuestro RAID, que en nuestro caso es el primero.**

** Ahora en el fichero /etc/fstab añadimos al final del archivo la linea correspondiente y se finaliza el proceso de creacion.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/1.9.PNG)



**9. Simulacion de un fallo en uno de los discos.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/9.PNG)


**10. Retirar "en caliente" el disco que esta marcado como que ha fallado.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/10.PNG)


**11. Añadir "en caliente" un nuevo disco que reemplazaría al disco que hemos retirado.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_6/Capturas/11.PNG)
 