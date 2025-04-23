# Principio de Abierto/Cerrado (OCP)


El objetivo principal del Principio de Abierto/Cerrado es permitir que el software sea extensible para nuevas funcionalidades sin necesidad de modificar su código ya existente.
  En el sistema de gestión de turnos médicos, la funcionalidad de notificaciones estaba diseñada de forma rígida. Toda la lógica para enviar correos, mensajes de texto o llamadas estaba dentro de una misma estructura. Cada vez que se necesitaba agregar un nuevo tipo de notificación (como WhatsApp o notificaciones móviles), era necesario modificar directamente el código existente. Esto generaba errores, rompía funcionalidades previas y complicaba el mantenimiento del sistema.

El principio OCP propone que el sistema debe estar abierto para extenderse, pero cerrado para ser modificado. Es decir, debería poder agregarse una nueva funcionalidad (como un nuevo tipo de notificación) sin tocar el código que ya funciona. Para lograrlo, se reorganizó la lógica en componentes independientes, donde cada tipo de notificación tiene su propia estructura. Así, si se quiere añadir otro canal de aviso, se hace como una extensión, sin afectar lo anterior. Esto vuelve al sistema más flexible, seguro y preparado para el cambio.


## Motivacion


En el sistema de turnos médicos, surgían problemas cada vez que se querían incorporar nuevas funciones, como distintos tipos de notificaciones para pacientes y médicos. Al principio solo se usaba el correo electrónico, pero luego se quisieron añadir SMS, notificaciones push, etc.

El inconveniente era que cada vez que se sumaba un nuevo canal, se tenía que modificar el código que ya estaba funcionando. Eso podía romper funciones estables, hacer más difícil probar el sistema y aumentar su complejidad.

El principio de abierto/cerrado (OCP) propone que los sistemas estén diseñados para permitir extensiones sin tener que cambiar lo que ya funciona. Es decir, agregar cosas nuevas sin tocar lo viejo.

Ejemplo cotidiano: 
Imaginá un sistema de iluminación de una casa que viene con interruptores fijos para cada lámpara. Si querés agregar una lámpara nueva y tenés que rehacer toda la instalación, el sistema es rígido.
Pero si está pensado con enchufes o conexiones modulares, podés sumar luces nuevas sin modificar lo que ya está —solo enchufás y listo. Eso mismo busca este principio: que lo nuevo se integre sin romper lo que ya existe.





