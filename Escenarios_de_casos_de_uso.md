# Escenario de Caso de Uso 


## Caso 1: Notificaciones

### Descripcion general:

 - Una vez que el usuario completa el turno , el sistema envía automáticamente una notificación al paciente 
   confirmando su turno. Este aviso se realiza por correo electrónico e incluye la fecha del turno y el médico 
   asignado, funcionando como un recordatorio.

### Flujo de eventos

- El sistema reúne la información correspondiente al turno agendado.

- Con base en dicha información, genera un correo electrónico que contiene los datos relevantes de la cita.

- Finalmente, el sistema envía automáticamente la notificación al correo electrónico del usuario.


### Precondiciones

- El usuario debe encontrarse previamente registrado en el sistema.

- Es requisito que haya proporcionado un medio de contacto válido, ya sea una dirección de correo electrónico, número 
  telefónico u otro canal habilitado.

- El turno debe estar debidamente programado y contar con la confirmación correspondiente.



### Poscondiciones 

- El usuario recibe una notificación informándole acerca de su turno programado.

- La fecha y hora en la que se emite dicha notificación quedan registradas automáticamente en el sistema.

![Captura de pantalla 2025-04-12 175413](https://github.com/user-attachments/assets/465bb905-a575-4852-b988-f6b535f9a67a)


