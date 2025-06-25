
# Aplicación del Patrón de Diseño Estructural - Facade
Los patrones de diseño estructurales indican cómo organizar clases y objetos para formar sistemas más grandes sin perder flexibilidad ni eficiencia. 
En particular, el patrón Facade sirve para ofrecer una interfaz sencilla que permite interactuar con sistemas internos complejos sin necesidad de conocer su funcionamiento interno.
Este patrón está alineado con el principio SOLID de Responsabilidad Única, que propone que cada clase debe encargarse de una sola tarea específica, como puede ser registrar pacientes, gestionar turnos, entre otros.
La idea principal es facilitar el uso del sistema brindando una interfaz común que agrupe varias funciones internas.
Así, se puede resolver el problema de clases como Recepcionista, que actualmente asume muchas responsabilidades distintas.

## Motivación
En nuestro sistema de gestión de turnos, la clase Recepcionista asumía múltiples responsabilidades como registrar pacientes, asignar turnos y administrar coberturas médicas. Esto entra en conflicto con el Principio de Responsabilidad Única, ya que concentra tareas que deberían estar distribuidas en distintas partes del sistema.
Para resolver esta situación, se introdujo una clase fachada llamada SistemaAdministradorFacade. Esta clase actúa como punto central de acceso, coordinando todas las operaciones necesarias para el proceso de atención médica y gestionando la interacción entre distintos subsistemas.
Gracias a esta estructura, la clase Recepcionista puede delegar completamente las acciones operativas en la fachada, limitándose a cumplir el rol de cliente de alto nivel del sistema.
Las clases que forman parte de esta nueva organización son:


sistemaAdministradorFacade: La fachada principal que ofrece una interfaz unificada para interactuar con el sistema.

sistemaRegistro: Un subsistema encargado de la lógica relacionada con el alta de pacientes.

gestorTurno: Otro subsistema que se ocupa de la creación y administración de turnos.

Las entidades Paciente y Medico, que participan activamente en las operaciones coordinadas por los subsistemas.

## Estructura de Clases

[Facade](https://drive.google.com/file/d/1aJ_drdXnkwp1rrJWLr4bojBkBIE-n2AJ/view?usp=sharing)
(![Facade](https://github.com/user-attachments/assets/8aa5ff3f-0b58-4d42-836c-b6557967f633)
