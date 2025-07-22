# Encapsulamiento

El encapsulamiento consiste en ocultar la implementación interna de un objeto y exponer únicamente sus interfaces públicas. Esto permite que el estado interno del objeto permanezca protegido frente a accesos indebidos, promoviendo la seguridad y la modularidad del sistema.
Su importancia en el diseño radica en que resguarda la integridad de los datos del objeto, ya que impide su modificación directa desde el exterior. Además, facilita el mantenimiento y la evolución del software al limitar el acceso directo a los atributos y detalles internos. También permite modificar la implementación interna sin afectar a otras partes del sistema que utilizan ese objeto, lo que mejora la claridad y la organización del código al establecer qué puede ser accedido y qué no.
Este principio se vincula con el Principio de Abierto/Cerrado, ya que al ocultar la lógica interna de una clase se puede extender su funcionalidad sin modificar su estructura original. En cuanto a los patrones de diseño, se relaciona con el patrón de comportamiento Observer, ya que este patrón expone únicamente interfaces públicas para que los objetos interactúen, manteniendo oculta la lógica interna y garantizando la integridad del sistema.


# Ejemplo sobre el proyecto 

[Encapsulamiento](https://drive.google.com/file/d/1c8yZK1gv4f6WrGNg9CoQ5bLVIZjXNq-6/view?usp=sharing)

  ![Encapsulamiento](https://github.com/user-attachments/assets/ba522f81-118f-4382-929f-d5a4b53cbd31)


En una clase Paciente, puede que no sea necesario acceder directamente a atributos internos como la fecha o la hora del turno. Lo único que se desea conocer, por ejemplo, es si el turno está confirmado, pendiente o cancelado.

Gracias al principio de encapsulamiento, esos detalles internos permanecen privados, y la clase Paciente expone un método público, como obtenerEstadoDelTurno(), que informa únicamente el estado del turno. De esta manera, se accede a la información relevante sin necesidad de conocer o manipular directamente los atributos internos.
Esto garantiza la protección del estado interno del objeto, facilita el mantenimiento del código, y permite cambiar la implementación interna sin afectar a otras partes del sistema. Además, mejora la organización del código al establecer claramente qué parte de la información está disponible externamente y cuál no.

# Ejemplo codigo 


public class Paciente {
    private String nombre;
    private String estadoTurno;
    private String fechaTurno;
    private String horaTurno;

    public Paciente(String nombre, String estadoTurno, String fechaTurno, String horaTurno) {
        this.nombre = nombre;
        this.estadoTurno = estadoTurno;
        this.fechaTurno = fechaTurno;
        this.horaTurno = horaTurno;
    }

    // Método público que expone solo lo necesario
    public String obtenerEstadoDelTurno() {
        return estadoTurno;
    }

    // Otros métodos internos o privados podrían gestionar cambios
    private void modificarFecha(String nuevaFecha) { 
        this.fechaTurno = nuevaFecha;
    }
}

