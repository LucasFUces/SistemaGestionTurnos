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

Ejemplo: Sistema de Gestión de Biblioteca
Supongamos que estamos diseñando un sistema para gestionar una biblioteca. Aquí hay cinco requisitos funcionales en términos de POO:

## Gestión de usuarios

El sistema debe permitir registrar, editar y eliminar usuarios.

Cada usuario tendrá atributos como nombre, ID, tipo (estudiante/profesor).

Se pueden definir clases como Usuario, Estudiante y Profesor, donde Estudiante y Profesor hereden de Usuario.

## Préstamo de libros

Un usuario puede tomar prestado un libro si está disponible.

Cada préstamo tendrá una fecha de inicio y una fecha de devolución esperada.

Podría haber una clase Prestamo con atributos como usuario, libro, fecha_prestamo y fecha_devolucion.

##  Devolución de libros

El sistema debe permitir registrar la devolución de un libro.

Si la devolución se hace tarde, se aplicará una multa según los días de retraso.

Se puede manejar con un método en la clase Prestamo que calcule el retraso y aplique la multa.

## Búsqueda de libros

Los usuarios pueden buscar libros por título, autor o categoría.

Cada libro tendrá atributos como título, autor, ISBN, estado (disponible/no disponible).

Se puede definir una clase Libro con métodos para realizar la búsqueda.

## Generación de reportes

El sistema debe generar reportes de libros prestados, usuarios con multas, y historial de préstamos.

Se puede implementar una clase Reporte con métodos que consulten datos de las clases Libro y Prestamo.

 
 #Desarrollar cinco casos de uso con el formato
adecuado:

 
 Caso de Uso: Registrar Usuario
 Actor(es): Bibliotecario
📌 Descripción: Permite registrar un nuevo usuario en el sistema.

 Flujo Principal de Eventos:
El bibliotecario accede al sistema.

Selecciona la opción "Registrar Usuario".

Ingresa los datos del usuario (nombre, ID, tipo de usuario).

Confirma la información y guarda el registro.

El sistema almacena al usuario en la base de datos.

Se muestra un mensaje de confirmación.

⚠️ Precondiciones:

El bibliotecario debe estar autenticado en el sistema.

✅ Postcondiciones:

El nuevo usuario queda registrado en el sistema.

2️ Caso de Uso: Buscar Libro
 Actor(es): Usuario (Estudiante/Profesor)
📌 Descripción: Permite buscar un libro en la biblioteca por título, autor o categoría.

 Flujo Principal de Eventos:
El usuario accede al sistema.

Selecciona la opción "Buscar Libro".

Introduce un criterio de búsqueda (título, autor, categoría).

El sistema muestra una lista de libros coincidentes.

El usuario puede seleccionar un libro para ver más detalles.

⚠️ Precondiciones:

El usuario debe estar registrado en el sistema.

✅ Postcondiciones:

Se muestra la lista de libros disponibles según la búsqueda.

3️⃣ Caso de Uso: Prestar Libro
 Actor(es): Bibliotecario, Usuario
📌 Descripción: Permite que un usuario tome prestado un libro si está disponible.

 Flujo Principal de Eventos:
El usuario solicita un préstamo de libro.

El bibliotecario verifica la disponibilidad del libro.

Si el libro está disponible, el sistema registra el préstamo con la fecha de devolución esperada.

El sistema marca el libro como "No Disponible".

Se genera un recibo con los detalles del préstamo.

⚠️ Precondiciones:

El usuario debe estar registrado en el sistema.

El libro debe estar disponible.

✅ Postcondiciones:

El libro queda registrado como prestado y no disponible.

4️ Caso de Uso: Devolver Libro
 Actor(es): Bibliotecario, Usuario
📌 Descripción: Registra la devolución de un libro y calcula si hay multa por retraso.

 Flujo Principal de Eventos:
El usuario devuelve el libro al bibliotecario.

El bibliotecario busca el préstamo en el sistema.

El sistema verifica si la devolución es dentro del plazo.

Si hay retraso, el sistema calcula la multa.

El sistema actualiza el estado del libro a "Disponible".

Si hay multa, se informa al usuario.

Se genera un recibo de devolución.

⚠️ Precondiciones:

El libro debe haber sido prestado previamente.

✅ Postcondiciones:

El libro queda disponible para otros usuarios.

Si hay multa, se registra en la cuenta del usuario.

5️ Caso de Uso: Generar Reporte de Préstamos
 Actor(es): Bibliotecario
📌 Descripción: Permite generar un informe con la lista de libros prestados y usuarios que tienen libros pendientes.

 Flujo Principal de Eventos:
El bibliotecario accede al sistema.

Selecciona la opción "Generar Reporte de Préstamos".

El sistema consulta la base de datos y genera un listado de libros prestados.

Se muestra el reporte en pantalla y se puede imprimir.

⚠️ Precondiciones:

El bibliotecario debe estar autenticado en el sistema.

✅ Postcondiciones:

Se genera un informe con el estado de los préstamos.

# Tabla Sistema de Gestion de turnos 

https://drive.google.com/file/d/1J3fUEufcSSQtmo6P_uzmzKNsp3pljCgJ/view?usp=sharing



 
