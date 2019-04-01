# ENTRENAMIENTO DE LA IA </p> <br> <br> <br>
## WATSON ASSISTANT  <br> <br> <br>
<p> Watson Assistant permite crear chatbots o asistentes virtuales en diferentes canales. </p> <br> <br>
<img src="imagenes1/Imagen1.png"> <br> <br> <br>
<b> EJERCICIO 1: ASISTENTE PARA RESERVAR MESA EN UN RESTAURANTE </b> <br> <br> <br>
<p> Para comenzar a trabajar, crearemos un servicio de Watson Assistant en IBM Cloud y una vez creado, accedemos a él. </p> <br> <br>
<img src="imagenes1/Imagen2.png"> <br> <br> <br>
<p> A continuación, hacemos clic sobre el botón azul "Iniciar Herramienta" para acceder a la herramienta de trabajo. </p> <br> <br> <br>
<img src="imagenes1/Imagen3.png"> <br> <br> <br>
<p> Una vez dentro, crearemos un espacio de trabajo (Workspace). Lo llamaremos "Reserva de mesa" y el idioma será español. </p> <br> <br> <br>
<img src="imagenes1/Imagen4.png"> <br> <br> <br>
<p> ¡Ya podemos empezar a entrenar a Watson! </p> <br> <br> <br>
<p> <b> INTENCIONES (INTENTS) </b> </p> <br> <br> <br>
<p> Los Intents hacen referencia a la acción que quiere realizar el usuario (verbos). <br> 
El grupo de ejemplos de frases que el usuario puede utilizar para expresar una idea o un objetivo específico se etiquetan <br> <br> <br>
de la siguiente forma: #Idea. <br> <br> <br>
Para este ejercicio vamos a utilizar los siguientes Intents. <br> <br> <br> </p>
<img src="imagenes1/cuadro1.png"> <br> <br> <br>
<img src="imagenes1/Imagen5.png"> <br> <br> <br>
<p> <b> ENTIDADES (ENTITIES) </b></p> <br> <br> <br>
<p> Las entidades son los objetos sobre los que el usuario quiere actuar y son entradas que alteran la forma en que Watson <br>
responde a la intención del usuario. <br>
Para este ejercicio vamos a utilizar las siguientes Entities. </p> <br> <br> <br>
<img src="imagenes1/cuadro2.png"> <br> <br> <br>
<p> DIÁLOGO (DIALOG) </p> <br> <br> <br>
<p> El diálogo es la secuencia que va a seguir nuestra conversación. Cuando creamos el diálogo, automáticamente nos crea <br> 
dos nodos: "Bienvenido" y "En otras cosas". El nodo "Bienvenida" será el primero de la conversación y el nodo "En otras cosas" <br>
servirá para dar respuesta cuando no entendamos algo. <br> <br> <br> </p>
<img src="imagenes1/Imagen6.png"> <br> <br> <br>
<p> Si hacemos clic sobre el nodo "Bienvenida" podemos configurarlo. </p> <br> <br> <br>
<img src="imagenes1/Imagen7.png"> <br> <br> <br>
<p> Para darnos la bienvenida, Watson dirá: "Hola. ¿Cómo puedo ayudarte?" Podemos cambiar esa frase por, por ejemplo, "Hola" <br>
y "Buenos días" (podemos añadir diferentes respuestas para que no siempre diga lo mismo). <br> <br> <br> </p>
<img src="imagenes1/Imagen8.png"> <br> <br> <br>
<p> Si queremos que responda aleatoriamente "Hola" o "Buenos días", debemos pulsar el botón "Set to random". <br>
Ahora vamos a probar nuestra pequeña conversación; para ello hacemos clic sobre el símbolo de chat que hay arriba a <br> 
la derecha. Observaremos que directamente Watson nos dirá "Hola" (también podría decir "Buenos días" ya que es aleatorio). <br> <br> <br> </p>
<img src="imagenes1/Imagen9.png"> <br> <br> <br>
<p> Vamos a comenzar creando un nuevo nodo, cuya función será responder al usuario cuando este salude. Por lo tanto, la condición será: <br> </p>
<ul> 
<li>Si reconoce #saludar entonces ofrecer ayuda.</li>
</ul> <br> <br> <br>
<img src="imagenes1/Imagen10.png"> <br> <br> <br>
<p> Vemos que hemos escrito las posibles respuestas, esto es para que el bot no siempre conteste lo mismo. Para ello, cambiamos la opción <br>
"Set to random". Ahora que hemos creado nuestro primer nodo, podemos probar la conversación. Para ello hacemos clic sobre el símbolo <br>
de diálogo arriba a la derecha. <br> <br> <br> </p>
<img src="imagenes1/Imagen11.png"> <br> <br> <br>
<p> Probamos a contestar saludando y comprobamos que nos responde lo que le habíamos indicado en la configuración. </p> <br> <br> <br>
<img src="imagenes1/Imagen12.png"> <br> <br> <br>
<p> Ahora crearemos otro nodo para dar respuesta a las peticiones de reservas del usuario. Por lo tanto, la condición será: </p> <br>
<ul> 
<li>Si #Nueva_Reserva entonces preguntar por tipo de cocina</li>
</ul> <br> <br> <br>
<img src="imagenes1/Imagen13.png"> <br> <br> <br>
<p> Probamos la conversación. </p> <br> <br> <br>
<img src="imagenes1/Imagen14.png"> <br> <br> <br>
<p> Lo último que faltaría, sería identificar el tipo de comida que desea el usuario. Para ello, añadimos un nuevo nodo a la <br>
conversación al que llamaremos "Confirmar cocina". <br>
En este caso, la condición será que el usuario especifique el tipo de restaurante que desea: <br> </p>
<ul> 
<li>Si @Tipo_Cocina entonces confirmar reserva.</li>
</ul> <br> <br> <br>
<img src="imagenes1/Imagen15.png"> <br> <br> <br>
<p> Y probamos. </p>
<img src="imagenes1/Imagen16.png"> <br> <br> <br>
<p> Para finalizar, vamos a dar las gracias al agente y a despedirnos. Para ello, vamos a crear un nuevo <br>
Intent: #agradecer. <br> </p> <br> <br>
<img src="imagenes1/Imagen17.png"> <br> <br> <br>
<p> Volvemos al árbol de diálogo y creamos un nuevo nodo llamado "Gracias" y otro "Despedida" </p> <br> <br> <br>
<img src="imagenes1/Imagen18.png"> <br> <br> <br>
<img src="imagenes1/Imagen19.png"> <br> <br> <br>
<p> Probamos la conversación completa </p> <br> <br> <br>
<img src="imagenes1/Imagen20.png"> <br> <br> <br>
<p> <b> ¡ Ya tenemos creada nuestra conversación con Watson Assistant! </b> </p>
