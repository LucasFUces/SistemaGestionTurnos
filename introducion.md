-[Introduccion](#introduccion)
-[Fundamentos](#Fundamentos)
-[Requisitos Iniciales](#Requisitos)
-[Casos de Uso](#casos)
-[Boceto Inicial](#Boceto)

# Introduccion (#Introduccion)

## ¿Que es la Programacion Orientada a Objetos?

### La Programación Orientada a Objetos (POO) es un paradigma de programación basado en el concepto de objetos, que son entidades que combinan datos (atributos) y comportamientos (métodos). Este enfoque permite organizar el código de manera modular y reutilizable, facilitando el desarrollo y mantenimiento de software.


## Fundamentos de la Programacion Orientada a Objetos (#Fundamentos)

  ###Clase y Objetos : Son plantillas o moldes para crear objetos. Definen los atributos y métodos que tendrán los objetos.
 Ejemplo : Piensa en una receta de pizza. La receta describe los ingredientes y los pasos para hacer una pizza, pero no es una pizza real, sino solo un concepto.
 La receta es la clase.

Cada pizza que cocinas usando la receta es un objeto basado en la clase "Receta de Pizza".


  ### Objetos: Son instancias de una clase; cada objeto tiene su propio estado y comportamiento.

 
  ### Encapsulamiento: Consiste en ocultar los detalles internos de un objeto y exponer solo lo necesario para su uso.
  El encapsulamiento oculta detalles internos y solo permite acceso a lo necesario.

 Ejemplo:
Un control remoto tiene botones para cambiar el canal y subir el volumen, pero no necesitas saber cómo funciona internamente el circuito para usarlo.

Los botones son la interfaz pública (lo que el usuario puede tocar).

Los circuitos internos están ocultos dentro del control (no se pueden manipular directamente).


   ### Herencia: 
  Permite que una clase (subclase) herede atributos y métodos de otra clase (superclase), promoviendo la reutilización del código.
 La herencia permite que una entidad herede características de otra.

 Ejemplo:
Imagina que tienes una bicicleta y una motocicleta.

Ambas tienen ruedas, manubrio y frenos (atributos comunes).

Pero la motocicleta tiene motor, mientras que la bicicleta no

  ### Polimorfismo: Permite que un mismo método tenga diferentes comportamientos según el objeto que lo utilice.

 El polimorfismo permite que diferentes objetos respondan de manera diferente a una misma acción.

 Ejemplo:
Un músico toca diferentes instrumentos, pero cada uno suena distinto.

Si le das una guitarra, tocará acordes.

Si le das un piano, tocará notas.

Si le das una batería, hará ritmos.

### Abstracción
La abstracción oculta los detalles complejos y solo muestra lo esencial.
 Ejemplo:
Piensa en conducir un coche.

Sabes que para arrancarlo solo giras la llave o presionas un botón.

No necesitas conocer cómo funciona el motor internamente, la combustión, la transmisión, etc.

La abstracción en POO funciona igual: te da herramientas sencillas sin mostrar la complejidad interna.


#Requisitos iniciales del sistema


## Gestión de usuarios

# User Registration 
El sistema debe permitir registrar, editar y eliminar usuarios.

Cada usuario tendrá atributos como nombre, ID, tipo (estudiante/profesor).

Se pueden definir clases como Usuario, Estudiante y Profesor, donde Estudiante y Profesor hereden de Usuario.


#Desarrollar cinco casos de uso con el formato
adecuado:

# Sing UP
Actores involucrados: Usuario y sistema
Descripción breve: Permite a un nuevo usuario crear una cuenta en la plataforma.
Flujo principal de eventos
El usuario accede a la página de registro.
El usuario ingresa su información personal (nombre, correo, contraseña).
El sistema valida la información ingresada.
El sistema crea una nueva cuenta y envía un correo de confirmación.
El usuario recibe el correo y confirma su registro.
Precondiciones: El usuario no debe tener una cuenta existente.
Postcondiciones: El usuario tiene una cuenta activa en el sistema.



# Login
Actores involucrados: Usuario, Sistema
Descripción breve: Permite a un usuario registrado acceder a su cuenta.
Flujo principal de eventos:
El usuario accede a la página de inicio de sesión.
El usuario ingresa su correo y contraseña.
El sistema valida las credenciales.
El sistema redirige al usuario a su panel de control.
Precondiciones: El usuario debe tener una cuenta registrada.
Postcondiciones: El usuario está autenticado y tiene acceso a su cuenta.

# Password recovery
1️⃣ Ir a "Olvidé mi contraseña" en la pantalla de inicio de sesión.
2️⃣ Ingresar correo o usuario para verificar la identidad.
3️⃣ Recibir un código o enlace por correo o SMS.
4️⃣ Ingresar el código o acceder al enlace de recuperación.
5️⃣ Crear una nueva contraseña segura.
6️⃣ Confirmar el cambio y recibir notificación.
7️⃣ Iniciar sesión con la nueva contraseña.

# Solicitar Turnos 
1️⃣ Iniciar sesión en el sistema con usuario y contraseña.
2️⃣ Seleccionar "Solicitar Turno" en el menú principal.
3️⃣ Elegir especialidad y médico disponible.
4️⃣ Seleccionar fecha y hora según la disponibilidad.
5️⃣ Confirmar el turno y agregar observaciones si es necesario.
6️⃣ Recibir confirmación del turno por correo o SMS.

# Cierre de Sesion 
1️⃣ Ir al menú de usuario (generalmente en la esquina superior).
2️⃣ Seleccionar "Cerrar sesión" o "Salir".
3️⃣ Confirmar la acción si el sistema lo solicita.
4️⃣ Ser redirigido a la pantalla de inicio de sesión.



#EJEMPLO : 
## Ejemplo de Gestión de Turnos en un Centro de Salud
1️⃣ Registro de Médicos y Especialidades
El sistema almacena los datos de los médicos, incluyendo su especialidad, horario de atención y datos de contacto.

El Dr. Juan Pérez es especialista en Cardiología y atiende de lunes a viernes de 9:00 a 14:00. Su contacto es 123-456789 y su correo electrónico es juan@salud.com.

La Dra. Ana Gómez, especialista en Pediatría, atiende los martes y jueves de 10:00 a 16:00, con contacto 234-567890 y correo ana@salud.com.

El Dr. Carlos Ruiz se especializa en Dermatología y atiende los lunes, miércoles y viernes de 8:00 a 12:00. Su contacto es 345-678901 y su correo carlos@salud.com.

2️⃣ Registro de Pacientes
El sistema también guarda la información de los pacientes.

Por ejemplo, María López tiene el documento 12345678, nació el 15 de abril de 1985, su teléfono es 555-1234, y su correo electrónico es maria@gmail.com.

Otro paciente, Pedro Ramírez, tiene el documento 87654321, nació el 22 de agosto de 1992, y sus datos de contacto son el teléfono 555-5678 y el correo pedro@gmail.com.

3️⃣ Asignación de Turno
María López necesita un turno con un especialista en Cardiología, por lo que solicita una cita con el Dr. Juan Pérez.

El sistema verifica la disponibilidad del médico y agenda el turno para el 5 de abril de 2024 a las 10:30. El estado del turno queda "Confirmado".

El motivo de la consulta es un chequeo de presión arterial, y en las observaciones se registra que la paciente tiene antecedentes de hipertensión.

4️⃣ Cambio o Cancelación de Turno
Si María decide cancelar su turno, el estado del mismo cambia a "Cancelado", y el sistema envía una notificación con la actualización.

Por ejemplo, el mensaje de notificación podría ser:

"Estimado/a María López, su turno con el Dr. Juan Pérez el 05/04/2024 a las 10:30 ha sido cancelado. Para reprogramar, comuníquese al 123-456789."

📌 Resumen del Proceso
Se registran los médicos con sus especialidades y horarios de atención.

Se almacenan los datos de los pacientes con su historial de turnos.

Se asignan turnos de acuerdo con la disponibilidad del profesional de salud.

Los turnos pueden ser confirmados, cancelados o modificados según sea necesario.

El sistema envía notificaciones a los pacientes cuando hay cambios en sus turnos.

 


# Boceto inicial del diseño de clases!

https://drive.google.com/file/d/1J3fUEufcSSQtmo6P_uzmzKNsp3pljCgJ/view?usp=sharing



 
