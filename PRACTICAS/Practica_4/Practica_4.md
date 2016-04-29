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

    ![imagen]()

    *Segunda ejecución*

    ![imagen]()

    *Tercera ejecución*

    ![imagen]()

    *Cuarta ejecución*

    ![imagen]()

    *Quinta ejecución*

    ![imagen]()