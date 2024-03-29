---
layout: post
title:  "Arte, código y actualizaciones"
date:   2021-07-09 01:00:00 -0500
lang: es
lang-ref: art-code-and-updates
published: true
categories: art code updates ros
comments: true
---



![Artwork banner](/assets/img/posts/art-code-and-updates.png)

Desde el último post me he dedicado a la actualización y mantenimiento de mis códigos en GitHub. Esto debido a mi repositorio de llevar mis conocimientos a más personas, he realizado varias acciones para hacerlo más atractivo. Parte de ello ha caído en la adición del arte para su difusión por las redes sociales, con lo que espero pueda aumentar la exposición de estas contribuciones a la comunidad.


## El arte

El arte que llevo hasta el momento está distribuido a lo largo de este post, espero que su función haya sido cumplida y te hayas dedicado a observarlos primero antes de empezar con el texto.

Para la realización de estos dibujos utilice el programa Clip Art Studio, el cuá es usado para la creación de dibujos, cómics y mangas, por lo que resulta ser el mejor candidato para el trabajo, eso y que no había podido encontrar la excusa perfecta de usarlo desde que lo compré. 

Además, he comprobado una vez más lo terapéutico que la realización de arte es, así como tomar fotografías, tienen mi sello de aprobación 🤓. 

Ahora, hablando de la inspiración para este estilo de arte, me basé en las etiquetas que he visto en las laptops de las personas, y aunque no las use en la mía (me gusta mantener el exterior original de mis computadoras) me gusta ver el nivel de personalización y atractivo visual que causan en quienes las observan, por lo que quise copiar ese efecto en mi arte. 

La adición de nuevo arte va a ser agregada de manera intermitente, ya que debo recuperar algo de ritmo para terminar proyectos atrasados, pero eventualmente cubriré todos los repositorios más importantes 

Como siempre, agradezco infinitamente que me hagan llegar sus comentarios acerca de las imágenes.

## El código

Cada una de las ilustraciones da imagen a los repositorios más visitados por la comunidad desde que inicié mi viaje por la plataforma de ROS o Robot Operating System. Para quienes no lo conozcan, ésta herramienta hace la función de Middleware, en otras palabras, es el traductor que se encuentra entre el Software y el Hardware, y que en términos prácticos nos ayuda a tener una fácil y mejor comunicación entre los nodos (programas que controlan cada una de las funciones en ROS) de manera distribuida. Cada uno de estos nodos te ayuda separar los componentes de un robot y su controlador de software por sus tareas, fuente o destino. Cada uno de estos nodos pueden estar enfocados ya sea a la adquisición de datos a través de los sensores, la acción de los actuadores, el procesamiento de la información o un controlador de nodos que se encarga de gestionar la interacción entre dos o más nodos. Me gusta verlo como una especie de "pegamento", ya que te ayuda a partir un problema gigante en problemas más pequeños y fáciles de manejar. 

![Bebop_ROS_Examples_image](https://toton95.github.io/assets/img/posts/BebopROSExamples_3.jpg)

### "Bebop_ROS_Examples"

La primera ilustración es acerca de mi primer repositorio hecho con una colección de experimentos que hice junto con mis compañeros durante mi estancia en Texas A&M University en 2017. Tengo un cariño especial por este código, ya que fue el que me llevo a tener mis primeros seguidores y empezar a aparecer en la mira de varios desarrolladores y docentes sobre el campo. La colección está diseñada para el drone Parrot Bebop (y en teoría es compatible con Parrot Bebop 2) y contiene códigos de experimentos de lazo abierto, de vehículos múltiples, y otros ejercicios usando un sistema de captura de movimiento.

Finalmente, para 2018, la colección recibió su última adición para documentar el código para la competencia del Torneo Nacional de Robótica en México, específicamente en la categoría de vehículos aéreos autónomos, donde se consiguió el segundo lugar por el ejercicio de seguimiento de objetos, y nuestra solución fue la mejor de la competencia. 

![ROS Pyparrot Artwork](https://toton95.github.io/assets/img/posts/ros-pyparrot_7.jpg)

### "ros_pyparrot"

Este repositorio fue creado para formar una plataforma de drones lo suficientemente pequeños para que pudiesen funcionar en grupo y ejecutara comandos de manera independiente. Otros factores como el tamaño de la zona de vuelo y el costo influyeron en la elección del Mambo Parrot como el principal objetivo. 

El código como un todo, funciona igual que un "driver", esto quiere decir que coordina las comunicaciones entre la computadora y el drone para poder realizar las acciones solicitadas. Al hacer un poco de investigación al respecto, encontré que el método tradicional de comunicación con los celulares o tablets era por medio de Bluetooth y WiFi, con los cuales me sentía muy cómodo, ya que había trabajado con ello en otra ocasión. Sin embargo, ya al investigar más a fondo, descubrí que hacía uso de la versión Bluetooth más reciente, que en ese tiempo era la 4.0, la que introducía una forma de transmisión ahorradora de energía, llamado formalmente como Bluetooth Low Energy (BLE). 

La mayor diferencia entre la versión que yo usé y la BLE es que se necesita "despertar" y "mantener despierta" la vía de comunicación entre ambos extremos de la transmisión. Esto se me presentó como un nuevo reto, así que me puse a investigar sobre algún medio para comunicar el Mambo Parrot con ROS o algún SDK del que pudiera hacer uso para mis experimentos. 

Por desgracia, mis esfuerzos por buscar algo ya hecho fracasaron, así que la única esperanza que me quedaba era intentar hacer Ingeniería Inversa, para ello invertí en un BLE Sniffer, una herramienta para interceptar los paquetes mandados entre ambos extremos de la transmisión y un Mambo Parrot personal por si lo llegaba a romper (los drones sobre los que iba a trabajar eran de la universidad).

Los primeros esfuerzos dieron pocos resultados, pero me ayudaron a entender mejor el comportamiento del drone, así como   conocer la manera en que esta versión de Bluetooth funcionaba, sin tener que estudiar gran parte del manual oficial. Al poco tiempo, y dentro de las conversaciones en varios foros sobre la Ingeniería Inversa en este drone, me encontré con el trabajo de la Dra. Amy McGovern, quién ya casi descifró todo lo necesario para que el drone funcionara, el nombre de su [proyecto](https://github.com/amymcgovern/pyparrot) es `pyparrot`. 

Un vistazo y una prueba rápida después me convencieron para crear una interface entre su trabajo y la plataforma ROS, en base a lo que Autonomy Lab había establecido con `bebop_autonomy`. Poco tiempo después, obtuve los resultados que buscaba, e incluso pude incluir funcionalidades que aún no habían sido agregadas, como el auto despegue, donde lanzas el drone al aire para que éste se mantenga volando. Gracias a ROS, era posible hacer despegar hasta 8 drones al mismo tiempo (por especificaciones de BLE). Al ver volar a todos esos drones, lo llamé un éxito y me fui a dormir.

Aún espero agregar un par de funcionalidades que me hacen falta...

![Mambo ROS Examples Artwork](https://toton95.github.io/assets/img/posts/Mambo_ROS_Examples_2.jpg)

### "Mambo_ROS_Examples"

Este repositorio es el sucesor espiritual de "Bebop_ROS_Examples", el cual contiene varios de esos experimentos pero mejorados y otros más que involucran a dos o más drones. El proyecto se basó completamente en las necesidades de la prueba del drone mismo y realizar los experimentos para un artículo de conferencia en ["IEEE Globecom Workshop on Computing Centric Drone Networks" ](https://doi.org/10.1109/GCWkshps45667.2019.9024528) y una entrada al Journal ["IEEE Transactions on Control Systems Technology"](https://doi.org/10.1109/TCST.2020.3020783). 

Necesité bastante tiempo para completar esta serie de experimentos, sin embargo, me alegra que lo hice y además me tomé el tiempo de hacerlo bien, ya que tanto este repositorio como los dos anteriores están sirviendo de material de apoyo para alumnos en varias universidades alrededor del mundo, y me doy cuenta por quienes los siguen y la temporada en que son vistos o clonados.

Espero poder continuar expandiendo con este proyecto pronto. 

![ros-gopro-driver Artwork](https://toton95.github.io/assets/img/posts/ros_gopro_driver_6.jpg)



### "ros-gopro-driver"

Ya por último, este es el repositorio de ROS más nuevo que he publicado, casi al igual que con `pyparrot`, no encontré una manera de poder grabar mis experimentos con mi GoPro y ROS de manera independiente (eran parte de otros paquetes y solo ciertas funciones), sin que tuviera que meterme dentro de la zona de pruebas a iniciar la grabación. Claro, podía usar la aplicación para smartphones, pero a veces lo usaba para monitorear otras cosas del experimento, datos de ubicación, estado, entre otras cosas. 

Así que tuve que acostumbrarme a ello hasta que concluí la maestría. Después de que me mudé a Las Cruces, Nuevo México, tuve el tiempo de trabajar de nuevo sobre el tema, poco después encontré una [API por WiFi recolectada por KonradIT]( https://github.com/KonradIT/goprowifihack), fue allí que encontré una forma directa de interactuar con las cámaras mediante la librería `requests` de Python y extender los comandos e información a ROS. 

Hasta este punto, ya era capaz de manejar la cámara y hacer uso de varias de las funciones principales de la cámara, ahora solamente me hacía falta encontrar la manera de transmitir vídeo en vivo para incluirlo dentro de ROS. Afortunadamente, ya había tenido tiempo jugando con el proyecto [FFMPEG](http://ffmpeg.org/) y los tutoriales de [Leandro Moreira](https://github.com/leandromoreira/ffmpeg-libav-tutorial) (los cuales ayudé a traducir al idioma español, como agradecimiento), y fueron estas herramientas las que me pusieron en buen camino para capturar y decodificar cada uno de los paquetes que se reciben a la mayor velocidad posible, comparándose de forma similar a lo que se entrega en la aplicación oficial, al menos de manera subjetiva (más pruebas serán efectuadas en el futuro).

El código se encontraba listo y solo faltaba probarlo, para mi suerte funcionó de maravilla, claro había varias regiones con corrupciones de píxeles pero se encontraban de igual manera en la aplicación oficial, así que mi teoría se centra en la calidad de la conexión de la antena WiFi (estoy considerando consultar a Leandro por alguna idea).

Ya solo me hacía falta que alguien lo probara en su computadora para confirmar que se podía reproducir el mismo resultado, así que decidí enviarlo a mi amigo [Evan Krell](https://github.com/ekrell) de la Texas A&M University - Corpus Christi, quien confirmó su funcionamiento, e hizo uso práctico del programa en su [proyecto](https://ekrell.github.io/underwater-gopro-stream/) y se convirtió como contribuidor del repositorio, con toda esa evidencia hice un Tweet con el estado actual del código... y a la comunidad le encantó. 🖤

Tanto les encantó que salimos en el [resumen semanal de ROS](https://discourse.ros.org/t/ros-news-for-the-week-of-2-19-2021/19051) y tiempo después en un [artículo de Ubuntu](https://ubuntu.com/blog/the-state-of-robotics-february-2021). Fue asombroso, y para rematar nos publicaron en la misma semana que el Perseverance e Ingenuity habían aterrizado sobre Marte, así que fuimos el segundo lugar en clicks (el primero después de la noticia en Marte).

Esto me motivó a intentar empujar el limite un poco más para aceptar más cámaras y funcionalidades en el futuro, así como ver la forma de contribuir dentro del código fuente de ROS 2, ya que se ha hecho pública su utilización en la misión lunar del 2023 por la NASA, y yo quiero poder contribuir a algo así (eso y que por el éxito de Perseverance e Ingenuity en Marte, estuvieron regalando insignias especiales a todos los contribuidores de las librerías Open Source que se utilizan en la misión).

## ... y las actualizaciones

Ahora en cuanto a las actualizaciones de código, he estado trabajando en el mantenimiento de viejo código así como la adición de nuevas características para el "driver" de la cámara GoPro con ROS como la obtención del estado de la cámara,   hacer un registro que relacione los vídeos con los experimentos automáticamente, todo con el fin de terminar los proyectos pendientes y saltar a la siguiente versión de la plataforma, ROS 2.

En este punto, me tomaré un tiempo para entender más el mecanismo interno de ROS 2, con lo que espero ahondar mi conocimiento sobre la plataforma y tomar las decisiones necesarias para la migración de mis repositorios más importantes. Sin embargo, es importante conocer que es posible entrelazar nodos de ambas versiones, así que siempre está la posibilidad de continuar con solamente mantener las herramientas en ROS y no llevar a cabo la migración.

## Pero antes, un mensaje final:

Si tienes un buen ojo y has revisado los repositorios e imágenes que aquí se presentan, te darás cuenta de una  actualización sorpresa que esta por salir al publico. 

También dentro de este ambiente secreto (temporal), les digo que tengo varios proyectos atrasados en los que voy a reanudar los esfuerzos de desarrollo, van a tardar un poco, y más con las nuevas adiciones de conocimiento gracias Nvidia y su evento de la GTC 2021. 

Al momento de finalizar la escritura de este post, acabo de finalizar mi asistencia a TalentLand 2021, un evento donde compañías y personas del área de tecnología se reúnen para instruir y aconsejar a estudiantes para involucrarse en ese mundo, hablaré más de ello en el siguiente post.

Espero que hayas disfrutado de la lectura, ahora a disfrutar un buen café... ☕
