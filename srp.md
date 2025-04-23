# Principio de Responsabilidad Única (SRP)

El Principio de Responsabilidad Única (Single Responsibility Principle, SRP) tiene como propósito asegurar que una clase tenga una sola razón para cambiar. 
Esto significa que una clase debe tener una única responsabilidad y que todas sus funciones deben estar relacionadas con esa responsabilidad.

En el sistema de gestión de turnos médicos, había componentes que mezclaban varias responsabilidades en una sola unidad. Por ejemplo, una parte del sistema se encargaba al mismo tiempo de gestionar los turnos, validar la disponibilidad médica, notificar al paciente y registrar la información en la base de datos.
El principio de responsabilidad única propone separar esas funciones en partes independientes, donde cada una se ocupe de una sola cosa: una se encarga de crear turnos, otra de validar horarios, otra de enviar notificaciones y otra de guardar la información.



## Motivacion


Uno de los principales problemas en el sistema de gestión de turnos médicos era que muchos componentes estaban encargados de realizar múltiples tareas al mismo tiempo. Por ejemplo, una sola unidad del sistema se encargaba de registrar un turno, verificar la disponibilidad del médico, enviar una notificación al paciente y almacenar toda esa información en la base de datos. Este enfoque de "hacer todo en uno" generaba varios problemas: el código era complicado de entender, cualquier ajuste afectaba al sistema entero y los errores resultaban más difíciles de identificar y corregir.

Al aplicar este principio, el sistema fue reorganizado para que cada función fuera manejada por un componente independiente. 
Se creó una parte exclusiva para gestionar los turnos, otra para verificar la disponibilidad de los médicos, otra para enviar notificaciones y otra para almacenar la información. De esta manera, cada módulo podía ser modificado, desarrollado o corregido sin afectar los demás. Esto no solo mejoró la estructura del sistema, sino que también redujo los errores, facilitó el mantenimiento y permitió que el sistema fuera más fácil de escalar.

Ejemplo del mundo real ; 

Imaginemos una tienda donde un solo empleado se encarga de todo: atender a los clientes, hacer las ventas, gestionar el inventario, ordenar el almacén y hasta limpiar el local. 
Si hay un cambio en el sistema de ventas, todo su trabajo se ve afectado. Además, si comete un error, no es fácil saber en qué parte de su trabajo ocurrió. En cambio, si cada tarea está asignada a una persona distinta (uno para las ventas, otro para el inventario, otro para la limpieza), el trabajo es mucho más organizado, especializado y eficiente. 
Cada empleado se enfoca en una tarea específica, lo que permite que cualquier cambio se implemente de manera más controlada y sin complicaciones.






## Estructuras de Clases 

![Solid(SRP)](https://github.com/user-attachments/assets/c2500381-d78d-46d7-ab0b-18cccc0eb7a9)

[SRP](https://drive.google.com/file/d/1Nk84bHqLgRxeM7SRluQu1j2AHNx_4jye/view?usp=sharing)














