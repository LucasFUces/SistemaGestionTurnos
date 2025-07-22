# Encapsulamiento

El encapsulamiento consiste en ocultar la implementación interna de un objeto y exponer únicamente sus interfaces públicas. Esto permite que el estado interno del objeto permanezca protegido frente a accesos indebidos, promoviendo la seguridad y la modularidad del sistema.
Su importancia en el diseño radica en que resguarda la integridad de los datos del objeto, ya que impide su modificación directa desde el exterior. Además, facilita el mantenimiento y la evolución del software al limitar el acceso directo a los atributos y detalles internos. También permite modificar la implementación interna sin afectar a otras partes del sistema que utilizan ese objeto, lo que mejora la claridad y la organización del código al establecer qué puede ser accedido y qué no.
Este principio se vincula con el Principio de Abierto/Cerrado, ya que al ocultar la lógica interna de una clase se puede extender su funcionalidad sin modificar su estructura original. En cuanto a los patrones de diseño, se relaciona con el patrón de comportamiento Observer, ya que este patrón expone únicamente interfaces públicas para que los objetos interactúen, manteniendo oculta la lógica interna y garantizando la integridad del sistema.


# Ejemplo sobre el proyecto 

