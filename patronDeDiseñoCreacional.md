
# Aplicación de Patrón de Diseño Creacional – Singleton
Los patrones de diseño creacionales se enfocan en el proceso de creación de objetos, encapsulando la lógica necesaria para instanciarlos de manera flexible y controlada. El patrón Singleton asegura que una clase tenga una única instancia y proporciona un punto global de acceso a ella.

En el contexto de nuestro sistema de gestión de turnos, es fundamental garantizar que toda la lógica relacionada con la gestión de turnos se centralice en una única instancia. Esto evita inconsistencias, duplicación de turnos o colisiones al operar sobre los mismos datos desde distintas partes del sistema.

Este patrón respeta principios SOLID como el principio de Responsabilidad Única, ya que encapsula la gestión completa de los turnos en una  sola clase (GestorTurnos) sin dispersar esa lógica por el sistema. También cumple con el principio de Acceso Controlado a Recursos Compartidos, asegurando que todos los actores del sistema (recepcionista, médicos, etc.) operen sobre la misma fuente de verdad.


## Motivación
En un sistema de turnos, puede ser problemático que múltiples clases creen o modifiquen turnos sin coordinación. Esto podría generar datos inconsistentes o errores de sincronización.
Al utilizar el patrón Singleton, se garantiza que exista una única instancia de la clase GestorTurnos, encargada de centralizar toda la lógica vinculada a la creación, modificación, cancelación y consulta de turnos.
De este modo, todos los componentes del sistema acceden a un punto común y coordinado, reduciendo el acoplamiento y evitando errores de concurrencia o duplicación.
Este enfoque es especialmente útil en sistemas donde múltiples usuarios interactúan al mismo tiempo (por ejemplo, una recepcionista y varios médicos).

## Estructura de Clases


[Singleton](https://drive.google.com/file/d/1FAOxV1BouHRgWNHyYu3o4kwVSGTVHf3t/view?usp=sharing)


![Singleton](https://github.com/user-attachments/assets/f7ab52b7-abc8-4878-95c8-db3d680777fd)

