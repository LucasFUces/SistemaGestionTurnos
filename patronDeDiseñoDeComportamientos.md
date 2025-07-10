
 # Aplicación de Patrón de Diseño de Comportamiento – Command
Los patrones de comportamiento se enfocan en cómo los objetos interactúan y distribuyen la responsabilidad del comportamiento entre sí. El patrón Command encapsula una solicitud como un objeto, permitiendo parametrizar acciones, almacenarlas, deshacerlas o ejecutarlas en distintos momentos.

En nuestro sistema de gestión de turnos, este patrón se aplica para manejar de manera flexible las operaciones de solicitar, modificar o cancelar turnos. Cada una de estas acciones se encapsula dentro de un objeto comando, que conoce cómo ejecutar la acción específica.

Este patrón promueve el principio de Abierto/Cerrado, ya que se pueden agregar nuevas operaciones (como reprogramar turno, duplicar turno, etc.) sin modificar las clases existentes. También puede integrarse fácilmente con funciones como un historial de operaciones o un sistema de deshacer (undo).

## Motivación
En el sistema actual, la gestión de turnos involucra múltiples acciones que pueden requerir ser registradas, deshechas o programadas para más adelante. Sin un enfoque flexible, estas operaciones estarían dispersas y acopladas a la interfaz de usuario o a componentes específicos.
Al utilizar el patrón Command, cada operación se encapsula como un objeto independiente (ComandoSolicitarTurno, ComandoCancelarTurno, etc.), lo que permite ejecutar acciones de forma uniforme, registrar las acciones realizadas, y en un futuro implementar funcionalidades como deshacer, rehacer o programar comandos.
De este modo, el sistema se vuelve más modular, reutilizable y fácil de extender.

## Estructura de Clases

[Command](https://drive.google.com/file/d/1wO6bj-j1hU6TdC9oG2gIHX9sZ74488tE/view?usp=sharing)

![Command](https://github.com/user-attachments/assets/9dda9896-c71a-4008-abc4-bfc167620d2a)



