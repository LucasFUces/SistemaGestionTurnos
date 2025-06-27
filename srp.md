# Principio de Responsabilidad Única (SRP)
Este principio establece que una clase debe estar enfocada en cumplir un único propósito, y por ello debería existir solo un motivo que la lleve a modificarse. Cuando una clase se encarga de diversas tareas no relacionadas entre sí, se quiebra este principio, ya que cualquier cambio en alguna de esas funciones obliga a alterar la clase entera.

En nuestro caso, la clase Recepcionista del sistema cumple varias funciones que no están del todo cohesionadas. Si quisiéramos suprimir o reformular alguna de esas funciones, terminaríamos modificando toda la clase.


## Motivacion
Dentro de nuestro Sistema de Turnos, la clase Recepcionista se ocupa de cuatro tareas distintas: "Dar de alta pacientes", "Dar de alta médicos", "Programar turnos" y "Anular turnos". Si más adelante decidiéramos permitir que los propios médicos y pacientes gestionen su alta de manera autónoma, sería necesario reestructurar la clase Recepcionista.
Ejemplo cotidiano (Centro de Salud):
En un centro de salud, si el sistema obliga al recepcionista a registrar pacientes y también a gestionar turnos, un cambio en la forma de registro (por ejemplo, que los pacientes se inscriban por la web) obligaría a modificar todo el módulo.
Dividir estas responsabilidades en partes separadas del sistema permite adaptarlas por separado, sin afectar el resto.




## Estructuras de Clases 

![Solid(SRP)](https://github.com/user-attachments/files/20936635/SRP.MD)


[SRP](https://drive.google.com/file/d/1o96sVTsnwkWbtZguOxj2h4OruCpfJZm_/view?usp=sharing)














