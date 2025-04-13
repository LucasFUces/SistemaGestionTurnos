## Tarjetas CRC 

- Las tarjetas CRC (Clase-Responsabilidad-Colaboración) son una herramienta clave en la programación orientada a objetos. Sirven para reconocer y describir las clases 
  más importantes de un sistema, especificando qué funciones deben cumplir y con qué otras clases deben interactuar. 




### Tarjeta CRC: Consultar Turno 

**Nombre de la Clase:**  Consultar Turno 

**Superclase:** Sistema 

**Subclase:** -

- Pensamiento del objeto: Se presenta el usuario en recepcion con sus respectivos datos (DNI)  para consultar un turno con el medico y la especialidad del medico que 
  requiera, 
  teniendo en cuenta la fecha, el dia y la hora a su conveniencia . Conociendo la agenda medica 

- Responsabilidades: Poder consultar por un turno medico, Conocer el id Usuario, sus datos generales, datos del turno consultado, que medico solicitar 

- Colaboradores: Solicitar turno 

- Propiedad:  Nro de Usuario , DNI, correo, telefono ,  dia, hora y fecha del turno, medico, especialidad del medico .


 ![Captura de pantalla 2025-04-13 190606](https://github.com/user-attachments/assets/34973169-cdcc-43e7-a33a-b824f9fbde9a)



 ### Tarjeta CRC: Solicitar Turnos  

**Nombre de la Clase:**  Solicitar Turnos 

**Superclase:** Sistema 

**Subclase:** -


 - Pensamiento del objeto: El usuario debe registrar su turno con sus datos correspondientes, solicitando fecha, dia , hora y la especialidad del medico a su 
   conveniencia. 

- Responsabilidades: Poder solicitar un turno medico, conocer la agenda del medico para saber la disponibilidad de turnos.  

- Colaboradores: Notificacion del turno , consulta de turnos.  

- Propiedad:  Usuario, medico, agenda 



![Captura de pantalla 2025-04-13 191851](https://github.com/user-attachments/assets/788edab3-495d-4297-8725-b471640b3911)




### Tarjeta CRC: Notificacion Turnos  

**Nombre de la Clase:**  Notificacion de Turnos

**Superclase:** Notificacion de Turnos 

**Subclase:** -


 - Pensamiento del objeto: El usuario tiene que conocer los datos sobre el turno y el medico que fue designado al turno para enviar el correo y o mensaje al usuario,

- Responsabilidades: Poder notificar a los pacientes.

- Colaboradores: Solicitud de turno y cambio de turno.

- Propiedad:  Dia, hora, fecha  y especialidad el medico. 



### Tarjeta CRC: Modificacion de Turnos  

**Nombre de la Clase:** Modificacion de Turnos

**Superclase:** Modificacion de Turnos 

**Subclase:** -


- Pensamiento del objeto: El usuario debe conocer sus datos, los datos del turno , sus posibles cambios. 

- Responsabilidades: Poder modificar los turnos en base a la agenda.

- Colaboradores: Solicitud de turno , Notificacion de turno.

- Propiedad: Dia, fecha , hora id Usuario , especialidad del medico. 




### Tarjeta CRC: Cancelar Turnos  

**Nombre de la Clase:** Cancelar Turnos

**Superclase:** Cancelar Turnos 

**Subclase:** -


- Pensamiento del objeto: El usuario debe conocer los datos del turno que va a cancelar y notificar la cancelacion del turno  

- Responsabilidades: El usuario debe poder cancelar el turno y notificar la cancelacion.

- Colaboradores: Solicitud de Turno, Notificacion.

- Propiedad: Usuario, turno, especialidad, medico. 




