# PRACTICA 2

## CLONAR LA INFORMACION DE UN SITIO WEB


**1. Clonado de una carpeta entre dos m�quinas.**



**2. Configuracion de ssh para acceder sin contrase�a.**

   - Ejecutaremos la siguiente orden:
  
     *ssh -keygen -t dsa*

     Incluimos captura de pantalla.
  
     ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_2/Capturas/generar_ssh_keygen.PNG)

   - Nos pedir� el passphrase el cual dejaremos en blanco.

   - En nuestro directorio se habr� creado un nuevo directorio .ssh donde se guarda
     "ide_dsa" e "id_dsa.pub", para las claves privadas y p�blicas.


   - Con la siguiente orden copiamos la clave a nuestra maquina 1
   
     *ssh-copy-id -i .ssh/id_dsa.pub mancilla@ubuntu-uno*

     A continuacion ya podremos conectarnos a nuestro equipo sin contrase�a.
     Incluimos captura de pantalla.

     ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_2/Capturas/conexcion_sin_pass.PNG)



**3. Tarea en Crontab.**

   - En la maquina 2 (mancilla@ubuntu-2), editaremos el archivo /etc/crontab y a�adiremos la siguiente orden:

     *01 * * * * mancilla rsync -avz -e ssh 192.168.131.130:/var/www/ /var/www/

     Y el archivo quedar� de la siguiente manera:

     ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_2/Capturas/tarea_crontab.PNG)

     
     Una vez guardado, cada hora de cada dia del a�o se ejecutara la orden indicada.
