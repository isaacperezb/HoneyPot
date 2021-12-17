# HoneyPot

## ¿Qué es una HoneyPot?

Es un señuelo ubicado en una red para evitar posibles ataques al sistema informático. La función principal es detectar y obtener información del ataque informático y de la ubicación de donde procede dicho ataque.
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

Vamos a elegir la primera versión que es la estandar.

![configuracion10](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/12.JPG)

Nos pedirá que pongamos una contraseña y la confirmación de esta, para poder iniciar sesión en el sistema operativo.
Además nos pedirá el nombre de usuario y la contraseña y confirmación de la misma.

Una vez hayamos configurado todo lo anterior ya podremos acceder al sistema operativo. Debemos iniciar sesión con el usuario que viene por defecto (tsec) y la contraseña elegida por nosotros mismos.

![terminal](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/19.JPG)

Ahora actualizaremos el sistema.

![actualización](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/20.JPG)

![actualización2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/21.JPG)

Una vez que hemos actualizado el sistema abriremos el navegador web y pondremos las credenciales para iniciar sesión (Las de ADMIN).

![admin](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/22.JPG)

Al ser un señuelo para los atacantes no tendremos ningún tipo de seguridad por lo que nos parecerá el mensaje de que es un sitio potencialmente peligroso,
para acceder deberemos darle a configuración avanzada y acceder al sitio web.

![web1](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/23.JPG)

Iniciamos sesion con el usuario por defecto tsec y la contraseña configurada anteriormente para nuestro usuario.

![web2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/24.JPG)

Una vez iniciemos sesión ya nos aparecerá el panel de control.

![web3](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/25.JPG)



## BIBLIOGRAFÍA

- http://www.reydes.com/d/?q=Conocer_si_un_Servidor_es_un_Honeypot_desde_Shodan_utilizando_el_Modulo_auxiliary_gather_shodan_honeyscore
- https://thesecuritysentinel.es/nuestro-primer-honeypot-paso-a-paso/
