#  Principio de Sustitución de Liskov (LSP)

Este es un principio relacionado con la herencia en la programación orientada a objetos
y su objetivo es asegurar que las subclases puedan usarse en lugar de sus clases padre sin que el sistema se comporte de forma incorrecta. 
En el sistema de gestión de turnos médicos, se definió una clase base llamada Usuario, y de ella se derivaron subclases como Paciente, Médico y Administrador.
El problema surgió cuando algunas subclases sobrescribían métodos heredados de forma que rompían la lógica general. Por ejemplo, había situaciones en las que se esperaba un objeto Usuario, pero si se usaba un Administrador, el sistema podía fallar porque este no implementaba correctamente ciertas funciones, como la de agendar turnos. 
Esto violaba el principio ya que se supone que cualquier subclase de Usuario debería poder usarse sin que el sistema deje de funcionar como se espera. 



## Motivacion

En el sistema de turnos médicos, todos los usuarios —pacientes, médicos y administradores— estaban agrupados bajo una misma clase general. Esto causaba problemas, porque se asumía que todos podían realizar las mismas acciones, como pedir turnos, cuando en realidad solo los pacientes deberían tener ese permiso.

Para evitar que el sistema fallara o se volviera inconsistente, se agregaban excepciones manuales, lo que lo hacía más complejo y propenso a errores.

El principio de sustitución de Liskov dice que una subclase debe poder reemplazar a su clase base sin alterar el comportamiento del sistema. En este caso, si un Administrador no puede hacer lo que se espera de un Usuario (como pedir turnos), se está violando ese principio.

La solución fue redefinir claramente qué acciones puede realizar cada tipo de usuario. Así, cada uno cumple solo con sus responsabilidades, lo que hace el sistema más claro, seguro y fácil de mantener.

Ejemplo real :
Es como en una empresa, no todos los empleados deben tener acceso al laboratorio. Si se asignan permisos según el rol desde el inicio, no hace falta controlar cada caso especial.


![SolidLSP](https://github.com/user-attachments/assets/d5105b4a-a9ca-4a93-a3cf-78b6fb5cffef)

[Estructura de clases](https://drive.google.com/file/d/1n7wMSVBRR-60KryNBG9NTrlfk4r99Myr/view?usp=sharing)




