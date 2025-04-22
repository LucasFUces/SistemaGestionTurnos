# Principio de Inversión de Dependencias (DIP


En el sistema de gestión de turnos médicos, varios módulos clave estaban directamente vinculados a servicios específicos, como una base de datos en particular o un sistema concreto de envío de correos.
Esto significaba que cualquier modificación en esos servicios impactaba en todo el sistema, lo que generaba errores y complicaba el proceso de adaptación a nuevas tecnologías o migraciones.
Este principio sugiere cambiar esa estructura, haciendo que la lógica principal del sistema no dependa directamente de servicios específicos. En su lugar, se utilizan abstracciones (como un "servicio de notificación" en vez de un "servicio de correo"). 
De esta manera, es posible modificar o sustituir los servicios sin afectar el funcionamiento principal del sistema, lo que aumenta su flexibilidad, reutilización y capacidad de adaptación a lo largo del tiempo.



## Motivación

En el sistema de gestión de turnos médicos, uno de los mayores problemas era que los módulos de alto nivel, como la lógica principal que gestiona las citas y asigna médicos, dependían directamente de componentes de bajo nivel, como bases de datos específicas o sistemas de notificación como el correo electrónico.
Esto significaba que cualquier cambio en estos elementos de bajo nivel afectaba toda la aplicación.

Al aplicar el principio de inversión de dependencias (DIP), el sistema se reorganizó para que la lógica principal dependiera de abstracciones (como interfaces de notificación, bases de datos y servicios), en lugar de depender de implementaciones concretas.
Por ejemplo, en lugar de que el sistema de turnos dependiera de un servicio específico de correo electrónico, se creó una interfaz común llamada "Servicio de Notificación", y el sistema solo interactúa con esa interfaz sin preocuparse por qué servicio de notificación se utiliza realmente. 
Esto permitió cambiar o reemplazar el sistema de notificación sin alterar el resto del sistema. El código de alto nivel se desacopló de los detalles de implementación, lo que hizo el sistema más flexible, fácil de probar y mantener a largo plazo.


Ejemplo del mundo real :

Imaginemos que un restaurante tiene una aplicación para gestionar pedidos en línea. La aplicación está directamente conectada a un sistema de pago específico, como una pasarela de pagos.
Si el restaurante decide cambiar de proveedor de pagos, tendría que modificar toda la aplicación para adaptarse a las nuevas herramientas del nuevo proveedor.
Sin embargo, si la aplicación estuviera diseñada para depender de una interfaz común de pago (en lugar de depender de un proveedor específico), solo necesitarían cambiar la implementación del sistema de pago sin tocar el resto de la aplicación. Esto haría que la app sea más flexible y fácil de actualizar, reduciendo el riesgo de errores al modificar solo una pequeña parte del sistema.
