# PRACTICA 4
# COMPROBAR RENDIMIENTO DE SERVIDORES WEB

**1. APACHE BENCHMARK**

  **1.1 Instalación**

    Instalamos en nuestro sistema operativo nativo (en este caso bajo Win7), nuestro servidor apache.

  

  **1.2 5 Ejecuciones "ab" contra M1**

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