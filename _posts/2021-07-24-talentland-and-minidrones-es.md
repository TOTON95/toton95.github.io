---
layout: post
title:  "TalentLand y Minidrones"
date:   2021-07-20 01:00:00 -0500
lang: es
lang-ref: talentland-and-minidrones
published: true
categories: code updates ros drones parrot
comments: true
---

Hola de nuevo, espero y sigas bien, con un buen café a tu lado y acomodado en tu silla favorita para trabajar desde casa. 

En este post voy a develar el secreto que dejé en el blog anterior, también voy a hablar acerca de las diferentes conferencias que he asistido durante el transcurso de la pandemia.  Todas ellas relacionadas a la ciencia y tecnología, algunos eventos son el pasado All Things Open 2020, GTC 2021 de Nvidia y más recientemente TalentLand 2021.

## TalentLand 2021

Este evento es realizado año con año desde el 2018, y cuyo propósito es  la reunión de estudiantes, amantes de la tecnología y profesionales del sector en un mismo lugar.  Por causa de la pandemia, no fue posible de realizar el evento en  persona como se hacía en pasadas ediciones, sin embargo tanto como en esta conferencia como otras que se han efectuado en este periodo de contingencia , se realizaron de manera virtual, y en muchas ocasiones hasta de manera gratuita u otras facilidades poco frecuentes para los asistentes, por lo que recomiendo estar atento a la aparición de estas oportunidades, ya que aunque la experiencia no es la misma, si permite tener acceso a material de calidad que no es posible concentrar en otras condiciones que no sean en conferencias.

Para TalentLand 2021, específicamente, agradezco a Ramón Roche ([@mrpollo](https://twitter.com/mrpollo?s=20)) por la oportunidad, Roche es Product Manager de la Foundation Dronecode, esta fundación es quien gestiona y mantiene la plataforma [PX4](https://px4.io/). Además, Roche dió una muy buena introspección e historia de la fundación y cómo el Open Hardware y Source han permeado entre la industria. Como dato adicional, también he trabajado con PX4 en mis experimentos anteriormente y de los cuales espero pueda compartir algo de ellos junto su interacción con ROS y ROS2 en un futuro.

Volviendo a TalentLand, me parece una gran idea para los jóvenes en México y Latino América, para esta edición fueron capaces de traer personas de alto nivel en sus respectivos campos, entre ellos se encuentran Steve Wozniak, Adam Savage, Seth Godin y John Cohn. Por otra parte, también participaron personajes de la comunidad maker como Ana Karen Ramírez ([@anaqueenmaker](https://www.instagram.com/anaqueenmaker/)) y Ricardo Muñoz ([@nquehmx](https://www.instagram.com/nquehmx/)).

El evento fue dividido en diferentes tracks, los cuáles iban dependiendo del público objetivo de los temas a discutir, siendo Business Channel para los interesados en los temas de finanzas, inversiones y estilos de negocio como el E-Commerce; Developer Channel para quienes se dedican a la Inteligencia Artificial, DevOps y Ciberseguridad; Creative Channel para artistas y generadores de contenido; Blockchain Channel dirigido a CryptoMonedas y NFTs; Iron Channel buscó concentrar a los makers, IoT y robótica; Gamer Channel que abarcó todo lo relacionado a la creación, distribución y consumo de videojuegos; Superpoderes Channel que se centró en la creación de buenos hábitos y competencias interpersonales e intrapersonales; finalmente tenemos a Talent World Channel que fue para temas especializados. Por otra parte, también existieron dos talleres Workshop Tech and Human, los cuales enseñaron temas de manera interactiva relacionados a las hard skills de la tecnología y las soft skills de las relaciones humanas, respectivamente.

El evento en sí resulto muy entretenido y me permitió entender el estado actual del sector tecnológico en México y Latino América, viendo cómo nombres importantes de la industria consideraban como importante la localización de esta región para el desarrollo y fabricación de productos tecnológicos.  

Aunque al inicio del evento no fue posible lo que aparentemente era el plan A de los organizadores (ya que se reportaban una cantidad considerable de quejas en las redes sociales), fueron rápidos en establecer un plan de respaldo para la realización del evento. Por lo que kudos ahí por la planeación y reacción del equipo.

Otro de los aspectos que me gustó fue la capacidad de hacer networking entre los asistentes al evento, esta actividad era realizada a través de la aplicación oficial. La manera en que se manejaba, sin embargo, era algo fuera de lo usual, desconozco si es la forma correcta de gestionar las posibles interacciones entre personas, y digo esto por un estilo similar a Tinder (me han dicho) y pues podría ponerse difícil el escoger las palabras correctas para darse a conocer y esto si lo llegasen a leer, ya que es muy fácil estar deslizando de izquierda a derecha a alta velocidad. Sin embargo, encontré muy buenas pláticas con la comunidad y me ayudó a entender un poco más la inercia interna de la industria y la academia.

En general, pienso que los ponentes fueron bastante buenos en la forma que comunicaron sus temas, además de motivar a las personas que estuviesen interesadas por cada uno de los campos, pasé la mayoría del tiempo en Developer y Iron Channel (creo que nadie imaginó eso). Un extra fue que cada una de las sesiones fue grabada para su uso On-Demand, lo cual es bueno y me mantendrá entretenido por bastante tiempo (a menos que lo vea de una sola vez jaja). 

Para cerrar, pienso volver para el siguiente año, espero y esta vez sea de forma presencial aunque sea para vivir "la experiencia completa", una experiencia que es alta recomendada por otros asistentes.  Mientras tanto, te comparto otras conferencias a las cuales tengo planeado asistir en lo que resta del año, éstas son SIGGRAPH 2021 (cortesía de Nvidia), PX4 Developer Summit 2021 y All Things Open 2021.

Así que si hazme saber si vas a asistir a estos eventos, para compartir ideas y observaciones, también puedes compartir si me estoy perdiendo de alguna conferencia que consideres importante.

## Visión para ros_pyparrot

En este tiempo me estuve dedicando a la mejora de mis repositorios, especialmente en el código para los Minidrones Parrot Mambo, espero hayas podido encontrar la respuesta al secreto del post anterior, y si el título e imagen no te lo han dicho aún, te digo que muy probablemente estás en lo correcto, he logrado hacer que los Minidrones te sirvan un espresso macchiato en tiempo record ☕🤓 (bueno no por ahora pero en un futuro espero que sí). 

Fuera de broma, es la adición del código de visión para la cámara a bordo que se encuentra en el drone, que pensándolo bien es necesario para servirte ese delicioso café, por ahora me enfocaré en hacerlo funcionar de forma correcta, depurar cualquier error e intentar usar algunas técnicas para hacer el flujo de imágenes lo más cercano al tiempo real. Ésto es muy importante, ya que sin ello el drone no podrá ser capaz de obtener información importante de su entorno, como lo sería su posición en el espacio, la existencia de obstáculos, objetivos a alcanzar, entre otros. Todo ello lo obtendría de forma desfasada a lo que tiene en realidad, y eso puede traducirse directamente en un muy mal desempeño, más esfuerzo para la estimación de posición y las estrategias de control, pero sobre todo en una cantidad considerable de choques y accidentes que tanto tú, como tu presupuesto van a resentir.  

![ROS Pyparrot Artwork](https://toton95.github.io/assets/img/posts/ros-pyparrot_7.jpg)

Así que al final del cuento, estos esfuerzos son muy importantes para mantener esas lagrimas fuera del esquema y mejor dejarlas para tus propios experimentos usando esta interfaz. Si bien aún no se encuentra del todo completa, ya está en una etapa operativa para empezar a experimentar en un ambiente controlado. Cuando me refiero a que está incompleto, hablo de un detalle del cual me tengo que documentar más para su correcta resolución, el problema cae en la forma en que el drone permite la transmisión de los datos desde la cámara al cliente que los solicita, ya que parece tener un temporizador interno que pausa el flujo de imágenes, que solo se restablece al pedir que el drone se mueva con los comandos para accionar los motores, y una vez detenidos el temporizador eventualmente acaba y las imágenes se detienen. Al parecer no es nada raro, ya que en la aplicación oficial parece pasar lo mismo, esto me hace sospechar de que es una forma de ahorrar energía, lo cual parece sensato y más por el tamaño del Minidrone y su batería.

Sin embargo, me gustaría poder saber si es posible mantener la transmisión abierta de manera indefinida para fines prácticos, como era posible con los Parrot Bebop y Bebop 2. Por lo pronto, voy a colocar un mecanismo que permita reconocer que ya no se han recibido nuevos frames y mandar una señal al entorno de ROS. Por otra parte, para al usuario agregaré una imagen que indique el drone no ha recibido nuevas imágenes y posiblemente alguna codificación al inicio de la imagen para que los programas que dependan de solamente la imagen (igual lo termino removiendo, veré como se comporta). Además, voy a investigar a fondo los puertos expuestos por `nmap` y ver si existe la posibilidad de obtener esta característica.

Otra limitación es que se debe considerar de momento es que la cámara solo actúa como un `Access Point` o `AP` y tanto la imposibilidad de mantener el stream abierto y cambiar el modo de el adaptador WiFi  solo podría ser eliminada con la modificación del firmware, lo que no siempre es conveniente.

Ya una vez teniendo el nuevo nodo operativo para la visión del drone, decidí dar un vistazo a la comunidad de [Twitter](https://twitter.com/alexis_guijarro/status/1415558596633391104?s=20), quiénes han aceptado muy bien la forma en que ando desarrollando la herramienta. Al momento de la escritura de este articulo, el tweet ya lleva más de 4000 interacciones y me permitió hablar con la autora del código base (`pyparrot`, por la Dra. Amy McGovern) que utilicé para crear mi proyecto `ros-pyparrot`. Lo cual me sirvió para entender un poco mejor el cómo fue el razonamiento que tuvo para crear su código y que experiencias obtuvo durante el desarrollo del mismo, de ahí me abre a otras opciones que posiblemente explore en caso de que sean necesarias o la carga de trabajo no esté muy pesada.

Este tweet me permitió también volver a formar parte de las noticias semanales de ROS, lo cual siento que es bueno, ya que reconoce y difunde los esfuerzos de las personas que desarrollan alrededor de la plataforma.  

Ya para finalizar, espero poder traer nuevas noticias acerca del driver de GoPro para ROS, así como un experimento de muestra nuevo para `Mambo_ROS_Examples` que haga uso del nuevo nodo para la visión en el Parrot Mambo drone.

Mientras tanto, sigamos esperando por ese espresso macchiato. 🤤
