# HoneyPot

## ¿Qué es una HoneyPot?

Es un señuelo ubicado en una red para evitar posibles ataques al sistema informático. La función principal es detectar y obtener información del ataque informático y de la ubicación de donde procede dicho ataque.

Para crear la HoneyPot vamos a seguir las siguientes imágenes que explican detalladamente la instalación.
Nos decargamos la iso de HoneyPot desde el siguiente enlace: [descarga la iso](https://github.com/dtag-dev-sec/tpotce/releases) 

![iso](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/1.JPG)
Una vez descargada nos creamos una máquina virtual, dicha máquina debe tener los siguientes requisitos mínimos:
- Arquitectura de 64 bits
- 1 GB 
- 10 GB de disco duro

Iniciamos la máquina arrancándola desde la unidad optica y seguiremos los siguientes pasos para la configuración:

![configuracion1](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/3.JPG)

Primero debemos configurar la zona donde nos encontremos deberemos seguir los siguientes pasos si somos de España.

![configuracion2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/4.JPG)
![configuracion3](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/5.JPG)
![configuracion4](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/6.JPG)

![configuracion5](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/7.JPG)

![configuracion6](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/8.JPG)

![configuracion7](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/9.JPG)

En la configuración del proxy daremos aocntinuar ya que no configuraremos ninguno.

![configuracion8](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/10.JPG)

Cundo nos vuelva a mostrar la página de instalación deberemos apagar la máquina y configurarla para que arranque por el disco duro. Una vez hecho esto al arrancarla nos aparecerá la siguiente pantalla.

![configuracion9](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/11.JPG)

Vamos a elegir la primera versión que es la estandar.

![configuracion10](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/12.JPG)

Nos pedirá la contraseña y que la repitamos para confirmarlo. Como escribimos una contraseña débil nos solicitará confirmar que queremos una contraseña débil.

![configuracion11](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/13.JPG)

![configuracion12](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/14.JPG)

![configuracion13](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/15.JPG)

![configuracion14](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/16.JPG)

![configuracion15](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/17.JPG)

Ahora deberemos elegir el nombre de usuario y la contraseña para entrar en web. Deberemos repetir el proceso de la contraseña.

![configuracion16](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/18.JPG)

Una vez hayamos configurado todo lo anterior ya podremos acceder al sistema operativo. Debemos iniciar sesión con el usuario que viene por defecto (tsec) y la contraseña elegida por nosotros mismos.

![terminal](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/19.JPG)

Ahora actualizaremos el sistema.

![actualización](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/20.JPG)

![actualización2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/21.JPG)

Una vez que hemos actualizado el sistema abriremos el navegador web y pondremos las credenciales para iniciar sesión (Las de ADMIN).

![admin](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/22.JPG)

![web1](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/23.JPG)

Iniciamos sesion con el usuario por defecto tsec y la contraseña configurada anteriormente para nuestro usuario.

![web2](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/24.JPG)

Una vez iniciemos sesión ya nos aparecerá el panel de control.

![web3](https://github.com/isaacperezb/HoneyPot/blob/main/instalaci%C3%B3n/25.JPG)

## Registro en SHODAN

Para realizar una comprobación con shodan primero debemos registranos en su página web: [SHODAN](https://www.shodan.io/)

Una vez que nos hayamos registrado deberemos iniciar sesión y en nuestra página de usuario nos parecerá la APIKEY.

![shodan](https://github.com/isaacperezb/HoneyPot/blob/main/shodan/1.JPG)

Ahora que tenemos nuestra cuenta en SHODAN y la APIKEY deberemos irnos a la terminal de Kali Linux y poner el siguiente comando: pip install -U --user shodan 

![shodan terminal](https://github.com/isaacperezb/HoneyPot/blob/main/shodan/2.JPG)

Ahora iniciamos nuestra APIKEY.

![APIKEY](https://github.com/isaacperezb/HoneyPot/blob/main/shodan/3.JPG)

Como último paso vamos poner el terminal el comando msfconsole para inciar el Framework de Metaesploit.


![msfconsole](https://github.com/isaacperezb/HoneyPot/blob/main/shodan/4.JPG)

![metasploit iniciado](https://github.com/isaacperezb/HoneyPot/blob/main/shodan/5.JPG)

### En el siguiente vídeo mostraré como realizar la comprobación en SHODAN para ver si reconoce como HoneyPot la máquina que hemos creado.

[vídeo comprobación shadon](https://youtu.be/JgRTjfF9h_Q)

## BIBLIOGRAFÍA
- https://developer.shodan.io/api/requirements#
- http://www.reydes.com/d/?q=Conocer_si_un_Servidor_es_un_Honeypot_desde_Shodan_utilizando_el_Modulo_auxiliary_gather_shodan_honeyscore
- https://thesecuritysentinel.es/nuestro-primer-honeypot-paso-a-paso/
