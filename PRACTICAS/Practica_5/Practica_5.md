# PRACTICA 5
# REPLICACION DE BASES DE DATOS MySQL

**1. CREACION DE UNA BASE DE DATOS.**

  **1.1. Entramos a MySQL.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/1.1.PNG)

  **1.2. Creamos la BD con resigistros.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/1.2.PNG)


**2. REALIZAR COPIA DE SEGURIDAD DE LA BASE DE DATOS USANDO MySQLDUMP.**

  **2.1. Evitamos que se acceda a la BD para cambiar nada con los siguientes comandos:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/2.1.PNG)

  **2.2. Hacemos el mysqldum para guardar los datos en la maquina 1.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/2.2.PNG)

  **2.3. Copiamos el archivo .sql en nuestra maquina 2 con el siguiente comando:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/2.3.PNG)

  **2.4. En nuestra maquina 2, es necesario crear la BD, ya la copia no la creará, solo importa los datos.**
  ** y ya podremos restaurar los contedinos de nuestra BD.**		
	
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/2.4.PNG)
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/2.5.PNG)


**3.REPLICACIÓN DE LA BASE DE DATOS CON UNA CONFIGURACION MAESTRO-ESCLAVO.**

  **3.1. Editamos los archivos de configuracion /etc/mysql/my.cnf tanto en maesto (ubuntu-uno) como en esclavo (ubuntu-2) y reiniciamos los servicios de MySQL.**

     Para no generar tantas capturas de los archivos de configuracion de cada maquina, comentaré por aqui los cambios que hay que realizar:
 
     Del lado del maestro:
	- Comentar el parametro bind-address 127.0.0.1
		#bind-address 127.0.0.1

	- Indicar el archivo donde se almacenará el log de errores:
		log_error = /var/log/mysql/error.log
	
	- Establecer el id del servidor:
		server-id = 1

	- Indicar el archivo donde se almacenará el registro binario:
		log_bin = /var/log/mysql/bin.log

	- Reiniciamos el servicio y si no se da ningun error, vamos por el buen camino:

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.1.PNG)

	Del lado del esclavo:

	- Comentar el parametro bind-address 127.0.0.1
		#bind-address 127.0.0.1

	- Indicar el archivo donde se almacenará el log de errores:
		log_error = /var/log/mysql/error.log
	
	- Establecer el id del servidor:
		server-id = 2

	- Indicar el archivo donde se almacenará el registro binario:
		log_bin = /var/log/mysql/bin.log

	- Ya que mi version de MySQL es superior a la 5.5, no tengo que realizar mas cambios en el archivo de configuración.

	- Reiniciamos el servicio y si no se da ningun error, vamos por el buen camino:

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.2.PNG)		

  **3.2. En el maestro ejecutamos las siguientes sentencias:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.3.PNG)


  **3.3. En el esclavo le damos los datos del maestro e iniciamos el esclavo:**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.4.PNG)

  **3.4. Comprobamos que todo funciona y listo.**

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.5.PNG)
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_5/Capturas/3.6.PNG) 