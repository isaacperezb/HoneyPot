# HoneyPot

## ¿Qué es una HoneyPot?

Es una máquina en nuestra red que actúa como señuelo cuando los atacantes planean un ataque a nuestra red. Es decir, cuano nos rastrean la red en busca de vulnerabilidades esta máquina será la primera a por la que vayan ya que tendrá los puertos y servicios que el atacante busca de forma vulnerables y con esto conseguimos que nuestras máquinas reales que no queremos que sean atacadas estén protegidas y además obtendremos información del atacante.
Es es como atraer a un carterista con una cartera falta mientras que la nuestra sabemos que está protegida porque se van a lanzar a robar la falsa, la "vulnerable".

La función principal de la HoneyPot es detectar y obtener información del ataque informático.
En este caso vamos a instalar PentBox, que es una suite de seguridad y pentesting basada en el lenguaje de programación ruby. Esta suite nos permite abrir el puerto que deseamos cubrir con la HoneyPot y una vez cerremos la HoneyPot este puerto volverá a cerrarse sin rigesgo a que se nos pueda olvidar cerrarlo.

Hay más formas de instalar una HoneyPot como instalar una T-POT, crearla nosotros mismos...


## INSTALACIÓN PentBox

Vamos a instalar PentBox en un Ubuntu Desktop 21.04 para simular que es la máquina vulnerable y con un máquina Kali Linux vamos a simular que es el atacante.

Pasos para la instalación:
- sudo apt install -y ruby-full --> instalamos el lenguaje ruby
- sudo apt install -y git --> instalamos la herramienta git
- git clone https://www.github.com/technicaldada/pentbox --> copiamos el repositorio de GitHub donde se encuentra la PentBox
- cd pentbox --> vamos al directorio pentbox
- tar -xf pentbox.tar.gz --> descomprimimos pentbox para poder usarlo

Tras estos pasos ya tendremos la máquina preparada para usar PentBox

## ENLACE AL VÍDEO



## BIBLIOGRAFÍA
- https://www.youtube.com/watch?v=rT55ghLqniE
- https://www.sevenlayers.com/index.php/255-pentbox-honeypot
- https://github.com/fernandopaezmartin/SAD_2021--Metasploit
- https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-
