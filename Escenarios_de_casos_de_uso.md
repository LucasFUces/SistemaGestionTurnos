# Escenario de Caso de Uso 

## Caso 1 : Consulta de turnos

### Descripcion general

 - Permite al usuario visualizar los turnos solicitados.

### Flujo principal de eventos

  - El usuario ingresa al sistema.

  - El usuario se dirige a "Consultar turnos".

  - El sistema muestra el historial de turnos del usuario.


### Precondiciones

 - El usuario debe estar registrado y autenticado en el sistema.

### Postcondiciones

 - El sistema muestra una lista de los turnos programados del usuario.
 - Se registra la consulta en el historial de actividades del usuario.

![Captura de pantalla 2025-04-13 161623](https://github.com/user-attachments/assets/8e824b00-6e14-49b4-8713-b5076364e00e)


## Caso 2 : Solicitar Turno

### Descripcion general

 - Permite al usuario solicitar turnos .


### Flujo principal de eventos
 
 - El usuario accede al sistema.

 - Selecciona una fecha y un profesional médico disponible.

 - Realiza la solicitud del turno.

 - El sistema registra y confirma la cita.

### Precondiciones

- El usuario debe haber iniciado sesión y contar con un método de pago activo.

### Postcondiciones
La transacción se completa con éxito y el usuario recibe una notificación de confirmación del turno.


![Captura de pantalla 2025-04-13 162811](https://github.com/user-attachments/assets/16a24525-fd11-46f0-9053-4f43db6f5b90)


## Caso 3: Notificaciones

### Descripcion general:

 - Cuando el usuario completa el turno , el sistema envía automáticamente una notificación al paciente 
   confirmando su turno. Esta notificacion del aviso se realiza por correo electrónico e incluye la fecha del turno, 
   el dia, la hora  y el médico asignado, funcionando como un recordatorio.

### Flujo de eventos

- El sistema reúne la información correspondiente al turno agendado.

- Con base en dicha información, genera un correo electrónico que contiene los datos relevantes de la cita.

- Finalmente, el sistema envía automáticamente la notificación al correo electrónico del usuario.


### Precondiciones

- El usuario debe encontrarse previamente registrado en el sistema.

- Es requisito que haya proporcionado un medio de contacto válido, ya sea una dirección de correo electrónico, número 
  telefónico u otro canal habilitado.

- El turno debe estar debidamente programado y contar con la confirmación correspondiente.


### Postcondiciones 

- El usuario recibe una notificación informándole acerca de su turno programado.

- La fecha y hora en la que se emite dicha notificación quedan registradas automáticamente en el sistema.


![Captura de pantalla 2025-04-12 175413](https://github.com/user-attachments/assets/34505b71-c2bd-4500-8de8-9840ab8a3c05)


## Caso 4 : Modificacion de Turnos 

### Descripcion general

 - El usuario puede realizar cambios en el turno pedido ingresando al sistema y dirigiendose a "Modificar turno".

### Flujo de eventos

 - El usuario ingresa a sistema.

 - El usuario se dirige a "Modificar turno".

 - El sistema analiza posibles modificaciones dentro de los cuales se encuentran el dia, la fecha, hora y el medico.

 - El sistema recibe la informacion del usuario y modifica el turno guardado.

### Precondiciones

 - El usuario debe estar registrado y autenticado en el sistema.
 - El turno original debe estar confirmado y no debe estar dentro del período de cancelación.
 - El nuevo turno solicitado debe estar disponible.

### Postcondiciones

 - El turno original se actualiza con la nueva información.
 - Se envía una notificación al usuario confirmando el cambio de turno.
 - Se registra el cambio en el historial de turnos del usuario.


![Captura de pantalla 2025-04-13 170147](https://github.com/user-attachments/assets/aab045c3-a4ef-4d53-9c1f-88d782c47071)


## Caso 5: Cancelar turno

### Descripcion general

 - Permite al usuario cancelar un turno ya solicitado .
 
### Flujo de eventos 

 - El usuario ingresa al sistema.

 - El usuario se dirige a "Cancelar turno".

 - El usuario cancela el turno previamente solicitado.

### Precondiciones

 - El usuario debe estar registrado y verificado en el sistema.
 - El turno debe estar confirmado y dentro del período de cancelación permitido.


### Postcondiciones

 - El turno se marca como cancelado en el sistema.
 - Se envía una notificación al usuario confirmando la cancelación.
 - Se actualiza la disponibilidad del turno en el sistema.


![Captura de pantalla 2025-04-13 172809](https://github.com/user-attachments/assets/6e635094-51ba-4563-914f-009a58195023)




   






