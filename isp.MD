# Principio de Segregación de Interfaces (ISP) 

En el sistema de turnos médicos, algunos módulos estaban conectados a interfaces demasiado grandes, que incluían funciones que no necesitaban. Por ejemplo, un módulo que solo debía gestionar turnos también tenía que incorporar funcionalidades de reportes o configuraciones, lo que generaba dependencias innecesarias.

Esto hacía que cualquier cambio en una función ajena pudiera afectar otras partes del sistema, aumentando el riesgo de fallos.

El principio de segregación de interfaces (ISP) busca evitar esto, dividiendo las interfaces grandes en otras más pequeñas y específicas. Así, cada componente solo usa lo que realmente necesita. Gracias a esto, se reorganizó el sistema en interfaces más enfocadas: una para turnos, otra para notificaciones y otra para reportes.



## Motivacion 

En el sistema de gestión de turnos médicos, uno de los problemas que se detectó fue que ciertos módulos del sistema estaban obligados a depender de funcionalidades que no utilizaban. Por ejemplo, un componente que solo se encargaba de mostrar turnos también tenía que incluir funciones relacionadas con reportes estadísticos, configuración del sistema o administración de usuarios.Este problema se debe a una violación del principio de segregación de interfaces (ISP), que propone que ningún módulo debe estar obligado a depender de métodos que no necesita. Es decir, cada parte del sistema debe contar solo con lo justo y necesario para funcionar.

Para aplicar este principio, se dividieron las grandes estructuras en interfaces más pequeñas y especializadas, enfocadas en tareas concretas. Así, por ejemplo, el módulo de visualización de turnos depende únicamente de una interfaz que contiene funciones de visualización; el módulo de reportes depende de una interfaz que solo maneja reportes, y así sucesivamente. Esto hace que cada parte del sistema sea más sencilla, más estable y más fácil de mantener o modificar sin riesgos innecesarios.

Ejemplo del mundo real: 

Imaginá que una recepcionista solo necesita una lista con los nombres de los pacientes del día y sus horarios. Pero en vez de eso, le entregan un archivo enorme con historiales médicos completos, reportes administrativos y datos contables. No solo es innecesario, sino que hace su trabajo más difícil y aumenta las chances de cometer errores.

En cambio, si solo recibe la información que le corresponde, puede trabajar de forma más rápida, clara y segura. Ese es justamente el objetivo del principio de segregación de interfaces: que cada parte del sistema acceda solo a lo que realmente necesita.






## Estructura de Clases

![SolidISP](




