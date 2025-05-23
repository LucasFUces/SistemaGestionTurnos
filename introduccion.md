
# Introduccion 

 - ¿Que es el Paradigma Orientado a Objetos?

 -  Es un paradigma de programación basado en el concepto de objetos, que son entidades que combinan datos 
    (atributos) y comportamientos (métodos). Este enfoque permite organizar el código de manera modular y 
    reutilizable, facilitando el desarrollo y mantenimiento de software.


# Fundamentos de la Programacion Orientada a Objetos 

 - Clase y Objetos : Son plantillas o moldes para crear objetos. Definen los atributos y métodos que tendrán los 
                    objetos.
 
 - Ejemplo : Piensa en una receta de pizza. La receta describe los ingredientes y los pasos para hacer una pizza, 
   pero no es una pizza real, sino solo un concepto.
   La receta es la clase.

    Cada pizza que cocinas usando la receta es un objeto basado en la clase "Receta de Pizza".


  - Objetos: Son instancias de una clase; cada objeto tiene su propio estado y comportamiento.

 
  - Encapsulamiento: Consiste en ocultar los detalles internos de un objeto y exponer solo lo necesario para su uso.
  El encapsulamiento oculta detalles internos y solo permite acceso a lo necesario.

  - Ejemplo:

     Un control remoto tiene botones para cambiar el canal y subir el volumen, pero no necesitas saber cómo funciona 
    internamente el circuito para usarlo.

  Los botones son la interfaz pública (lo que el usuario puede tocar).

  Los circuitos internos están ocultos dentro del control (no se pueden manipular directamente).


- Herencia: 
  Permite que una clase (subclase) herede atributos y métodos de otra clase (superclase), promoviendo la 
  reutilización del código.

La herencia permite que una entidad herede características de otra.

- Ejemplo:
   Imagina que tienes una bicicleta y una motocicleta.

    Ambas tienen ruedas, manubrio y frenos (atributos comunes).

    Pero la motocicleta tiene motor, mientras que la bicicleta no

  - Polimorfismo: Permite que un mismo método tenga diferentes comportamientos según el objeto que lo utilice.

    El polimorfismo permite que diferentes objetos respondan de manera diferente a una misma acción.

  - Ejemplo:

    Un músico toca diferentes instrumentos, pero cada uno suena distinto.

    Si le das una guitarra, tocará acordes.

    Si le das un piano, tocará notas.

    Si le das una batería, hará ritmos.

- Abstracción
  La abstracción oculta los detalles complejos y solo muestra lo esencial.

- Ejemplo:  

    Piensa en conducir un coche.

    Sabes que para arrancarlo solo giras la llave o presionas un botón.

    No necesitas conocer cómo funciona el motor internamente, la combustión, la transmisión, etc.

    La abstracción en POO funciona igual: te da herramientas sencillas sin mostrar la complejidad interna.


# Requisitos iniciales del sistema

- Registro de usuarios: El sistema debe permitir la creación y gestión de usuarios.

- Gestión de turnos: Los usuarios deben poder solicitar, cancelar y reprogramar turnos.

- Notificaciones: El sistema debe enviar recordatorios de turnos vía correo o mensaje.

- Historial de turnos: Se debe permitir consultar turnos pasados.

- Control de acceso:Solo usuarios registrados pueden acceder a ciertas funciones.


# Casos de Uso 
  
### Registrar Paciente

- Descripción:

  El paciente puede cambiar la fecha u hora de un turno previamente solicitado, siempre que haya disponibilidad.

- Precondiciones:

  El paciente no se encuentre registrado en el sistema 

- Postcondiciones:

  El paciente se registro de manera exitosa 

- Actores : Paciente, Recepcionista
- Flujo principal de eventos 
  Primer paso) El paciente se comunica con el centro de salud para registrarse  
  Segundo paso) La recepcionista ingresa al sistema en la seccion "Registrar paciente"  
  Tercer paso ) La recepcionista le consulta los datos al paciente   
  Cuarto paso) El paciente le brinda los datos solicitados  
  Quinto paso) La recepcionista los carga en el sistema  
  Sexto paso) El sistema registro un nuevo paciente  
  Septimo paso) Se genero idPaciente de manera exitosa   

  
### Consulta de turnos del paciente

-  Descripción:
   El paciente puede ver los turnos que tiene registrados, ya sea próximos o pasados.

-  Precondiciones:

   El paciente debe haber iniciado sesión.

- Postcondiciones:

   Se muestra la información de los turnos asociados al paciente.

- Actores : Paciente

- Flujo principal de eventos:  
  Primer paso) El paciente accede a la pagina del centro de salud   
  Segundo paso) El paciente se dirige a la seccion de pacientes  
  Tercer paso) El paciente se loguea y pone sus datos de ingreso  
  Cuarto paso) Se dirige a la seccion consultar turnos  
  Quinto paso) Consulta los turno disponibles   
  Sexto paso) El paciente cierra su sesion   


### Solicitud de turno


- Descripción:
  El paciente accede al sistema para solicitar un turno con un médico en una fecha y hora disponibles según la 
  especialidad de cada medico.

- Precondiciones:

  El paciente debe estar registrado e iniciar sesión en el sistema.


- Postcondiciones:

  Se registra un nuevo turno en el sistema.


- Actores  : Paciente y Recepcionista

- Flujo principal de eventos:  
Primer paso) El paciente se comunica con el centro para solicitar un turno  
Segundo paso) La recepcionista le consulta con que medico quisiera antenderse   
Tercer paso) El paciente le indica con que medico desea y el motivo de la solicitud   
Cuarto paso) La recepcionista le informa al paciente los turnos disponibles   
 Quinto paso) El paciente no acepta el turno y solicita otra fecha   
 Sexto paso) La recepcionista le indica otra fecha y horario disponible  
Septimo paso) El paciente acepta el turno disponible  
Octavo paso) La recepcionista le pide los datos al paciente  
Noveno paso) El turno fue registrado correctamente  


### Consulta de agenda del médico 

-  Descripción:
   El medico puede ver los turnos que tiene registrados, ya sea próximos o pasados.

-  Precondiciones:

   El medico debe haber iniciado sesión.

- Postcondiciones:

   Se muestra la información de los turnos asociados al médico.

- Actores : Médico 

- Flujo principal de eventos:  
  Primer paso) El médico accede a la pagina del centro de salud
     
  Segundo paso) El médico se dirige a la seccion de especialidades
  
  Tercer paso) El médico se loguea y pone sus datos de ingreso
  
  Cuarto paso) Se dirige a la seccion consultar agenda
  
  Quinto paso) Consulta los turno que posee asignados
  
  Sexto paso) El médico cierra su sesion   



### Cancelar turno

- Descripción:

  El paciente puede cancelar un turno registrado en el sistema si no puede asistir.

- Precondiciones:

  El turno debe estar activo y no haber pasado aún.

- Postcondiciones:

  El turno es eliminado del sistema.


- Actores : Paciente y Recepcionista

- Flujo principal de eventos:  
Primer Paso) El paciente se comunica con el centro para cancelar turno  
Segundo Paso) La recepcionista le consulta el turno que debe cancelar   
Tercer paso) El paciente le indica el turno a cancelar  
Cuarto paso) La recepcionista accede al registro del paciente  
Quinto paso) La recepcionista selecciona el turno a cancelar  
Sexto paso) El turno fue cancelado correctamente  
Septimo paso) La recepcionista informa al paciente que el turno fue cancelado correctamente   
Octavo paso) El sistema le informa al medico que el turno fue cancelado  

## Boceto Inicial del Diseño de Clases

![BocetoDiseñodeClases](https://github.com/user-attachments/assets/4be072dc-5104-4c39-b7ad-580748208e22)

[Enlace del Boceto](https://drive.google.com/file/d/1SlO7HctTub8Lo6XmJcWPBYab94fEVdOa/view?usp=sharing)





 
