# PRACTICA 4
# COMPROBAR RENDIMIENTO DE SERVIDORES WEB

**1. APACHE BENCHMARK**

  **1.1. Instalación**

    Instalamos en nuestro sistema operativo nativo (en este caso bajo Win7), nuestro servidor apache.

  

  **1.2. 5 Ejecuciones "ab" contra M1**

  Para este primer caso, utilizamos la herramienta AB contra la M1 sin ningun balanceador de carga.

  El comando a introducir en nuestro sistema navito es el siguiente:

  ab -n 1000 -c 10 http://192.168.131.130/hola.php


  *Primera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20M1/ejecucion%201.PNG)

  *Segunda ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20M1/ejecucion%202.PNG)

  *Tercera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20M1/ejecucion%203.PNG)

  *Cuarta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20M1/ejecucion%204.PNG)

  *Quinta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20M1/ejecucion%205.PNG)


  **1.3. 5 Ejecuciones "ab" contra LB (M3) con Nginx** 

  En este punto, utilizamos un balanceador de carga instalado en nuestra M3, en este caso utilizamos Nginx junto con Apache Benchmark.
  
  Introducimos el siguiente comando, similar al del punto anterior, sin embargo debemos añadir la IP de nuestro balanceador:

  ab -n 1000 -c 10 http://192.168.131.132/hola.php
  
  
  *Primera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20nginx/ejecucion%201.PNG)


  *Segunda ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20nginx/ejecucion%202.PNG)


  *Tercera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20nginx/ejecucion%203.PNG)


  *Cuarta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20nginx/ejecucion%204.PNG)


  *Quinta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20nginx/ejecucion%205.PNG)


  **1.4. 5 Ejecuciones "ab" contra LB (M3) con Haproxy**

  En este punto, utilizamos un balanceador de carga instalado en nuestra M3, en este caso utilizamos Haproxy junto con Apache Benchmark.
  
  Introducimos el siguiente comando, similar al del punto anterior, sin embargo debemos añadir la IP de nuestro balanceador:

  ab -n 1000 -c 10 http://192.168.131.132/hola.php

  *Primera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20haproxy/ejecucion%201.PNG)


  *Segunda ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20haproxy/ejecucion%202.PNG)


  *Tercera ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20haproxy/ejecucion%203.PNG)


  *Cuarta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20haproxy/ejecucion%204.PNG)


  *Quinta ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Ejecuciones%20LB%20haproxy/ejecucion%205.PNG)


  **1.5. Gráfica de Rendimientos**

  Una vez probado las 5 ejecuciones por cada tipo, hemos creado una gráfica de barras, en la cual se muestran los campos más resaltados del resultado de las ejecuciones.
  En esta gráfica se muestra la media de las 5 ejecuciones de los campos: Time take for test, Failed Request y Request per second.  

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/Grafica.PNG)





**2. SIEGE**

  **2.1. Instalación**

  Una vez descargado el paquete siege y añadido al directorio C/ de Win7 (digo que hay que añadirlo a C/, porque en el caso de que se guarde el directorio de siege en otro unidad, este no va a poder ejecutarse, ya que Windows es así), 
  ejecutamos en nuestra terminal el ejecutable y podemos iniciar las ejecuciones contra las máquinas.

  **2.2. 5 Ejecuciones "siege" contra M1.**

  *Comando a ejecutar*

  siege -b -t 60s -v http://192.168.131.130/hola.php

  *Primera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/M1/ejecucion%201.PNG)

  *Segunda Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/M1/ejecucion%202.PNG)

  *Tercera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/M1/ejecucion%203.PNG)

  *Cuarta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/M1/ejecucion%204.PNG)

  *Quinta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/M1/ejecucion%205.PNG)

  **2.3. 5 Ejecuciones "siege" contra LB con "nginx".**

  *Comando a ejecutar*

  siege -b -t 60s -v http://192.168.131.132

  *Primera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20nginx/ejecucion%201.PNG)

  *Segunda Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20nginx/ejecucion%202.PNG)

  *Tercera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20nginx/ejecucion%203.PNG)

  *Cuarta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20nginx/ejecucion%204.PNG)

  *Quinta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20nginx/ejecucion%205.PNG)

  **2.4. 5 Ejecuciones "siege" contra LB con "haproxy".**

  *Comando a ejecutar*

  siege -b -t 60s -v http://192.168.131.132

  *Primera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20haproxy/ejecucion%201.PNG)

  *Segunda Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20haproxy/ejecucion%202.PNG)

  *Tercera Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20haproxy/ejecucion%203.PNG)

  *Cuarta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20haproxy/ejecucion%204.PNG)

  *Quinta Ejecución*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/LB%20haproxy/ejecucion%205.PNG)

  **2.5. Gráfica de Rendimientos**

  En este punto, hemos tomado como datos como "Elapsed time", "Transaction Rate", la cual se mide en transacciones por segundo, y "Succesfull Transaction". 
  He dividido cada una de las gráficas por separado, ya que en el conjunto de las tres no se apreciaban correctamente los datos de alguno de los datos.

  *Gráfica Elapsed Time*
 
  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/elapsed.PNG)

  *Gráfica Transaction Rate*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/transaction.PNG)

  *Gráfica Succesful Transaction*

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/siege/Grafica%20Succesful.PNG)


  **3. SCRIPT UTILIZADO.**   

  Para cada una de las ejecuciones realizas en todos y cada uno de los ejercicios propuestos, se ha utilizado el siguiente script:

  ![imagen](https://github.com/JaviMancilla/swap/blob/master/PRACTICAS/Practica_4/Capturas/AB/script.PNG)