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

  ![imagen]()


  *Segunda ejecución*

  ![imagen]()


  *Tercera ejecución*

  ![imagen]()


  *Cuarta ejecución*

  ![imagen]()


  *Quinta ejecución*

  ![imagen]()