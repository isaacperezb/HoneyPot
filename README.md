# HoneyPot

## ¿Qué es una HoneyPot?

Es una máquina en nuestra red que actúa como señuelo cuando los atacantes planean un ataque a nuestra red. Es decir, cuando nos rastrean la red en busca de vulnerabilidades esta máquina será la primera a por la que vayan ya que tendrá los puertos y servicios que el atacante busca de forma vulnerables y con esto conseguimos que nuestras máquinas reales que no queremos que sean atacadas estén protegidas y además obtendremos información del atacante.
Es como atraer a un carterista con una cartera falta mientras que la nuestra sabemos que está protegida porque se van a lanzar a robar la falsa, la "vulnerable".

La función principal de la HoneyPot es detectar y obtener información del ataque informático.
En este caso vamos a instalar PentBox, que es una suite de seguridad y pentesting basada en el lenguaje de programación ruby. Esta suite nos permite abrir el puerto que deseamos cubrir con la HoneyPot y una vez cerremos la HoneyPot este puerto volverá a cerrarse sin riesgo a que se nos pueda olvidar cerrarlo.

Hay más formas de instalar una HoneyPot como instalar una T-POT, crearla nosotros mismos...


# Instalación PentBox

Vamos a instalar PentBox en un Ubuntu Desktop 21.04 para simular que es la máquina vulnerable y con una máquina Kali Linux vamos a simular que es el atacante.

### IP UBUNTU
192.168.1.118

![ip_ubuntu](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/6.JPG)

### IP Kali
192.168.1.111

![ip_kali](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/12.JPG)

Pasos para la instalación:
- sudo apt install -y ruby-full --> instalamos el lenguaje ruby
- sudo apt install -y git --> instalamos la herramienta git
- git clone https://www.github.com/technicaldada/pentbox --> copiamos el repositorio de GitHub donde se encuentra la PentBox
- cd pentbox --> vamos al directorio pentbox
- tar -xf pentbox.tar.gz --> descomprimimos pentbox para poder usarlo
- cd pentbox-1.8 --> vamos al directorio descomprimido

![pentbox_instalada](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/1.JPG)

Tras estos pasos ya tendremos la máquina preparada para usar PentBox.
Ahora debemos actuar como root e iniciar el ejecutable. Para ello seguiremos lo siguientes pasos:

- sudo su --> actuamos como superusuario
- ./pentbox.rb --> ejecutamos pentbox

![pentbox_lanzada](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/2.JPG)

Una vez tengamos ejecutado la PentBox vamos a pasar a configurar la Honeypot.

# Configuración HoneyPot

Para configurar la HoneyPot deberemos seguir los siguientes pasos:
- Opción 2 --> Herramientas de la red
- Opción 3 --> HoneyPot
- Opción 2 --> Configurado manual
- Puerto deseado para que actúe de HoneyPot
- Insertar mensaje para el atacante
- Guardamos las intrusiones en el fichero log --> opción y
- Guardamos por defecto la ruta del fichero log o podemos configurarla nosotros
- Activamos o no un sonido cada vez que se registre una intrusión.

![configurar_honeypot1](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/3.JPG)

![configurar_honeypot2](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/4.JPG)

# Pruebas

Vamos a realizar una prueba primero con la HoneyPot configurado en el puerto 80.
Para ello debemos analizar nuestra red y mirar un puerto 80 que esté abierto para comprobar que página vamos a atacar.

Analizamos la red con el comando nmap 192.168.1.* para analizar todas las máquinas dentro de nuestra red

![analizar_red](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/5.JPG)

Una vez creada haremos primero una prueba con un navegador externo y luego con metasploit.

![navegador](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/7.JPG)

Vemos que se están registrando las intrusiones de forma automática en el fichero de registros, que se activa al iniciar la HoneyPot.

![metasploit](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/8.JPG)

Si cerramos la HoneyPot veremos que el puerto 80 se ha cerrado.

![puerto_cerrado](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/11.JPG)

Ahora vamos a configurar la HoneyPot en el puerto 21 y haremos una prueba de conexión con FileZilla.

![configurar_puerto_21](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/13.JPG)

![prueba_puerto_21](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/9.JPG)

Podemos ver que no se termina de inicializar la conexión y si cerramos la HoneyPot se cerrará la conexión por completo.

![conexion_finalizada](https://github.com/isaacperezb/HoneyPot/blob/main/PentBox/10.JPG)


En el siguiente vídeo configuraré la HoneyPot en el puerto 22 (SSH) e intentaremos realizar un ataque de fuerza bruta.

Además, miraremos el fichero de registro de intrusiones.

## ENLACE AL VÍDEO





## BIBLIOGRAFÍA
- https://www.youtube.com/watch?v=rT55ghLqniE
- https://www.sevenlayers.com/index.php/255-pentbox-honeypot
- https://github.com/fernandopaezmartin/SAD_2021--Metasploit
- https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-
- https://www.youtube.com/watch?v=UWh9vJujreA
