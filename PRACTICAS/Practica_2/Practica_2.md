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



**3. Tarea en Crontab.**

