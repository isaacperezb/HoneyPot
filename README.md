# HoneyPot

## ¿Qué es una HoneyPot?

Es un señuelo ubicado en una red que nos ofrece un montón de servicios vulnerables y así para evitar posibles ataques al sistema informático al llevar al atacante hacia esa máquina vulnerable, es como dejarnos caer un reloj falso del bolsillo para ver quien es un atacante pero sin que nos quiten nada de valor, pero en un sistema informático ese reloj de millones son los datos. 
La función principal es detectar y obtener información del ataque informático y de la ubicación de donde procede dicho ataque.
En este caso vamos a instalar el sistema T-POT, el cual es una distribución de Debian que tiene todos los demonios HoneyPot.
Hay más formas de instalar una HoneyPot como crearla nosotros mismos, pero T-POT nos brinda una interfaz gráfica para poder ver análisis de los ataques.

Para empezar la instalación nos decargaremos la iso desde el siguiente enlace: [descarga la iso](https://github.com/dtag-dev-sec/tpotce/releases) 

![iso](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/1.JPG)

Una vez descargada nos creamos una máquina virtual, dicha máquina debe tener los siguientes requisitos mínimos:

- Arquitectura de 64 bits
- 1 GB 
- 10 GB de disco duro

Iniciamos la máquina y seguiremos los siguientes pasos para la configuración:

![configuracion1](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/3.JPG)

Deberemos configurar nuestra zona horaria, idioma, proxy.
En mi caso el proxy lo he dejado sin configurar ya que no utilizaré ninguno.

Vamos a elegir la primera versión que es la estandar, ya que vamos a realizar una prueba de funcionamiento y además no queremos instalar todos los servicios solo los necesarios para la prueba.
Al instalar una versión más profesional vendrán más servicios y por tanto necesitaremos más recursos hardware.

![configuracion10](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/12.JPG)

Nos pedirá que pongamos una contraseña y la confirmación de esta, para poder iniciar sesión en el sistema operativo.
Además nos pedirá el nombre de usuario y la contraseña y confirmación de la misma.

Una vez hayamos configurado todo lo anterior ya podremos acceder al sistema operativo. Debemos iniciar sesión con el usuario que viene por defecto (tsec) y la contraseña elegida por nosotros mismos.

![terminal](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/19.JPG)

Ahora actualizaremos el sistema.

![actualización](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/20.JPG)

![actualización2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/21.JPG)

Una vez que hemos actualizado el sistema abriremos el navegador web y pondremos las credenciales para iniciar sesión (WEB).

![admin](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/22.JPG)

Al ser un señuelo para los atacantes no tendremos ningún tipo de seguridad por lo que nos parecerá el mensaje de que es un sitio potencialmente peligroso,
para acceder deberemos darle a configuración avanzada y acceder al sitio web.

![web1](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/23.JPG)

Iniciamos sesion con el usuario por defecto tsec y la contraseña configurada anteriormente para nuestro usuario.

![web2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/24.JPG)

Una vez iniciemos sesión ya nos aparecerá el panel de control.
La primera sección del panel de control es la visualización de los recursos hardware del sistema, además de información de la máquina como el nombre del sistema, ID de la máquina, dominio...

![web3](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/25.JPG)

Otra sección es la del terminal para poder trabajar a través de en él en la página de la T-POT.



Una vez tengamos la T-POT instalada iremos a Kali Linux y escanearemos la red para ver las máquinas que hay y que puertos abiertos podemos explotar (en esta prueba utilizaremos una máquina ubuntu con puertos cerrados y la máquina T-POT con todos los puertos abiertos).

El puerto que vamos a explotar es el SSH para realizar un ataque de fuerza bruta. Buscaremos una máquina que tenga dicho puerto abierto.

Una vez que hemos escaneado la red y hemos visto que una máquina tiene el puerto 22 abierto atacaremos esa máquina (T-POT).

Primero crearemos un fichero de texto con varias contraseñas para el ataque de fuerza bruta. Como en este caso sabemos cual es la contraseña no llevará mucho tiempo pero en un caso real dependerá de la contraseña establecida en el servidor a atacar.

Lo segundo que haremos es abrir una consola de metasploit framework en nuestro kali.






## BIBLIOGRAFÍA

- http://www.reydes.com/d/?q=Conocer_si_un_Servidor_es_un_Honeypot_desde_Shodan_utilizando_el_Modulo_auxiliary_gather_shodan_honeyscore
- https://thesecuritysentinel.es/nuestro-primer-honeypot-paso-a-paso/
- https://github.com/fernandopaezmartin/SAD_2021--Metasploit
- https://openwebinars.net/academia/aprende/metasploit/
- https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-
