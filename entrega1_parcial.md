# mobile-hibrido-coderhouse
Programa Desarrollo Mobile Hibrido para Coderhouse

# Programa Mobile Hibrido

## Introduccion
### Historia
El desarrollo hibrido es una tecnologia que tenemos entre nosotros desde el anio 2010/2011. El principal problema que intenta solucionar este enfoque tecnologico entre otros que mencionaramos mas adelante, es minimizar la curva de aprendizaje del desarrollo de aplicaciones moviles, planteando a este con un enfoque de desarrollo Web, y reutilizando las mismas tecnologias que hoy en dia utilizamos para desarrollar aplicaciones web, pero terminar generando una aplicacion totalmente compatible con smartphones y lista para ser distribuida en los stores de cada plataforma.
El primer marco de trabajo (Framework) que propuso este enfoque fue Phonegap. Phonegap fue desarrollado en 2010 por la empresa Nitobi, bajo la licencia de software libre.
Tiempo despues en 2011, la empresa Adobe adquiere Nitobi
principalmente interesada por todo lo relacionado por el auge de HTML5. De esa manera, Phonegap queda bajo control de Adobe. Todo indicaba que Phonegap quedaria bajo un manejo propietario de Adobe y que su evolucion seria incierta o con fines netamente comerciales mas que tecnologicos. Pero afortunamente Adobe decide donar Phonegap a la fundacion Apache. Apache entonces emprende su propio camino, nombrando al proyecto como "Apache Cordova".

### Actualidad
En la actualidad Phonegap es la marca comercial que utiliza Adobe para seguir manteniendo el proyecto.
De la misma manera "Apache Cordova" es el nombre que utiliza la fundacion Apache para dicho proyecto.
Obviamente cada uno emprendio caminos diferentes, si bien
el punto de partida fue el mismo, hoy podemos optar
tanto por Apache Cordova como por Phonegap.
Ambos utilizan el mismo paradigma, generar aplicaciones web a base de HTML5 y Javascript y que son ejecutadas en un webbrowser embebido dentro de la aplicacion.
Actualmente, tenemos muchas alternativas a la hora de optar 
por un Framework u otro. Cada cual con sus ventajas, y desventajas. En este libro vamos a citar
algunos de los mas populares, pero nos enfocaremos
en explicar el desarrollo de aplicaciones hibridas basandonos en el Framework Ionic, que es sin duda,
el que mas auge tenido en el 2015, y que se perfila
para ser el lider absoluto por ventajas que contaremos mas adelante y que hacen de Ionic un ecosistema unico y completo. 

### Componentes del Desarrollo Hibrido
Cada vez que hablemos de desarrollo hibrido tendremos
que tener en claro y siempre presente que estaremos hablando
de la siguiente division de capas o componentes:

- HTML: Utilizaremos HTML para crear el layout de nuestra aplicacion. Con HTML definiremos los elementos que 
mostraremos en pantalla, como por ejemplo
listas, botones, imagenes, etc. Lo Utilizaremos
para crear nuestras pantallas o vistas.

- CSS: Utilizaremos CSS para darle estilos a nuestros
elementos HTML, definirles proporciones, tamanios,
colores. Mediante CSS haremos que nuestra aplicacion
parezca realmente una aplicacion nativa. 
Cabe destacar que al utilizar un Framework como Ionic
minimizaremos al maximo el uso de CSS, ya que Ionic ya nos
proporcionara estilos, que como primera instancia
nos permitira crear una aplicacion sin tener
que utilizar este componente. Obviamente
para interfases (layouts) complejos y customizados
deberemos utilizar CSS.

- Javascript (JS): Utilizaremos Javascript 
para crear la logica de nuestra aplicacion. Mediante
Javascript haremos que nuestra aplicacion sea capaz de guardar informacion, de responder a eventos
tales como "tap en un boton", recibir notificationes 
y mostrarlas. En esta capa definiremos tanto
las rutas que conectaran cada pantalla de nuestra
aplicacion como asi tambien los modelos que nos permitiran
que nuestra aplicacion se conecte con servicios externos
ya sea para consultar informacion, grabar
datos en un servidor, tomar fotografias con la camara, detectar la ubicacion del usuario, etc.

## Capitulo 1 - Nivelacion

### Conceptos previos
- Aplicaciones Nativas: 
Las aplicaciones nativas son aquellas que se desarrollan con el SDK y lenguaje que provee el sistema operativo
para el cual queremos desarrollar. 
Por ejemplo las aplicaciones nativas para Android se desarrollan en lenguaje Java utilizando el SDK Android Studio mientras que las aplicaciones nativas para 
la plataforma iOS se desarrollan en Objective-C o Swift utilizando el SDK provisto por Apple llamado xCode.
Las aplicaciones nativas, son aplicaciones compiladas
que generan codigo binario que luego es ejecutado en 
el movil.

- Aplicaciones Hibridas:
Las aplicaciones hibridas son aquellas que se crean en base a HTML, CSS y Javascript. Su codigo no es compilado, y son ejecutadas en un Browser o navegador web (WebView). Usualmente el usuario no logra percibir 
que se trata de un navegador web, ya que este esta embebido
dentro del marco de la aplicacion gracias a la utilizacion 
de Phonegap o Apache Cordova. El usuario lanza una aplicacion nativa que dentro embebe nuestro codigo HTML y JS en un WebView y lo ejecuta. El hecho de que sea una aplicacion Hibrida no es un limitante, ya que podemos explotar diferentes recursos tales como: GPS, Camara, libreta de contactos, etc. El codigo HTML y JS
de nuestra aplicacion reside en la memoria del dispositivo.

- Web Apps:
Las WebApps no son mas que sitios webs, que esteticamente lucen como una aplicacion movil. Tambien se basan en HTML y JS, pero pueden ser escritas en otros lenguajes como Ruby por ejemplo. Mediante CSS y disenio responsivo logran
un estilo similar al de una aplicacion movil, pero
la principal diferencia es que estas residen en un servidor web, los recursos (HTML, JS, CSS) se descargan del servidor cada vez que el usuario ingresa a la web. 
Un ejemplo claro de esto, es por ejemplo la version movil del portal de noticias Infobae.
Si ingresamos a Infobae.com desde nuestro movil, veremos
que el disenio se adapta perfectamente a nuestro 
dispositivo. Y que los elementos lucen similar a los de una aplicacion. A esto llamaremos WebApp.

- Web View:
Llamamos WebView a una extension o instancia del componente navegador (Browser) que se inserta dentro de una aplicacion nativa. 
Como ya todos sabemos el Browser nos posibilita abrir sitios webs y recursos HTML, JS.
En este caso el WebView es un instancia del Browser
el cual es la clave de nuestra aplicacion hibrida.
Ya que todo el codigo que desarrollemos
sera ejecutado en el WebView similando ser una aplicacion nativa y permitiendo ejecutar nuestros recursos HTML, JS.
Tanto Phonegap como Apache Cordova utilizan el WebView 
para ejecutar nuestra aplicacion.

- SDK:
SDK significa "Software Development Kit"
Este es un un kit de desarrollo de software que nos provee
de las herramienta necesarias (editor de texto, compilador, emulador, api, etc.) para desarrollar bajo una plataforma especifica.

- Dispositivo:
El dispositivo sera lo que solemos llamar Smartphone o celular. Es el hardware en el cual se ejecutara nuestra aplicacion. Cuando hablamos de dispositivo siempre nos referimos a un dispositivo fisico, real, no un emulador.

- Plataforma:
La plataforma sera el sistema operativo que tendra nuestro dispositivo; para el caso de Iphone la plataforma sera iOS, para el caso de Samsung sera Android. Y asi podemos enumerar
otras marcas que poseen otros sistemas operativos tales como Nokia Lumia con Windows Phone. Es importante destacar que cada plataforma posee su propio SDK y su propio lenguaje 
por lo cual he aqui el primer punto fuerte de desarrollar una aplicacion Hibrida, donde nos olvidaremos en parte
del lenguaje propietario de cada plataforma, y nuestra aplicacion estara enfocada a tecnologia web HTML, JS.

- Framework:
Un framework es un marco de trabajo. Es decir, un conjunto de herramientas y reglas que nos facilitaran tareas (a veces repetitivas) y nos guiara a seguir un paradigma especifico o convenciones mediante las cuales podremos trabajar ordenadamente y estandarizando soluciones. 
Adaptandonos a un framework podremos desarrollar mas rapido enfocandonos en nuestra aplicacion y aplicacando las mejores soluciones para cada problema que se nos presente.

- Patron MCV:
El patron MVC responde en espaniol a (Modelo, Vista, Controlador). MVC es un patrón de arquitectura de software que separa los datos y la logica de nuestra aplicación de la interfaz de usuario y el módulo encargado de gestionar los eventos y las comunicaciones. En esta separacion de tres capas detallamos lo siguiente: 
	- Modelo: Es el encargado de representar los datos que manajera nuestra aplicacion. Por ejemplo si queremos realizar una aplicacion de compra y venta de articulos, necesitaremos un Modelo que represente la relacion entre compradores, vendedores y los items que estan en venta. Para ello en nuestro desarrollo hibrido utilizaremos Javascript.
	- Controlador: El controlador es la capa intermedia entre el Modelo y la Vista. Este es el encargado de recibir los eventos provenientes de la Vista y realizar las operaciones necesarias para consultar al Modelo (si es encesario) en busqueda de informacion, para luego procesarla y retornarla a la vista. En nuestra aplicacion Hibrida para el controlador utilizaremos Javascript.
	- Vista:
	La vista es la parte visible de nuestra aplicacion. (La capa de presentacion) Es con lo que interactuara el usuario. Definira los componentes que deben mostrarse y se conectara con el Controlador para mostrar informacion al usuario, permitir entrada de datos, etc. Para ello utilizaremos HTMl y CSS.

### Plataformas
- Android
- Iphone iOS
- Windows Phone
- Otras Plataformas

### Dispositivos
- Emulador VS Navegador
- Dispositivos Fisicos
- Que es la fragmentacion ?

### Porque elegir Hibrido?
- Ventajas
- Desvenjatas
- Limitaciones