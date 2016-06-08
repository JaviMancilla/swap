# PRACTICA 5
# REPLICACION DE BASES DE DATOS MySQL

**1. CREACION DE UNA BASE DE DATOS.**

  **1.1. Entramos a MySQL.**

	foto 1.1

  **1.2. Creamos la BD con resigistros.**

	foto 1.2


**2. REALIZAR COPIA DE SEGURIDAD DE LA BASE DE DATOS USANDO MySQLDUMP.**

  **2.1. Evitamos que se acceda a la BD para cambiar nada con los siguientes comandos:**

	foto 2.1

  **2.2. Hacemos el mysqldum para guardar los datos en la maquina 1.**

	foto 2.2

  **2.3. Copiamos el archivo .sql en nuestra maquina 2 con el siguiente comando:**

	foto 2.3

  **2.4. En nuestra maquina 2, es necesario crear la BD, ya la copia no la creará, solo importa los datos.**
  ** y ya podremos restaurar los contedinos de nuestra BD.**		
	
	foto 2.4.
	foto 2.5.


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

		foto 3.1

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

		foto 3.2

