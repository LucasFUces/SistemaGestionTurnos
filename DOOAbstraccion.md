# Abstracción

La abstracción es el proceso de reducir la complejidad del mundo real representando únicamente los aspectos esenciales que son relevantes para el sistema. 
A través de ella, los objetos modelan entidades del dominio y sus interacciones, lo que facilita tanto la comprensión como el diseño del software.
Su valor en el desarrollo orientado a objetos radica en que permite enfocarse en las características y comportamientos fundamentales, dejando de lado los detalles innecesarios. 
Esto contribuye a una mejor organización del código, mayor claridad en los modelos y facilita tanto su mantenimiento como su escalabilidad.
La abstracción se relaciona directamente con el Principio de Responsabilidad Única, ya que al abstraer correctamente, cada clase se enfoca en una única función esencial dentro del sistema.
Además, es aplicada en patrones como el Factory Method, donde se crean objetos a partir de clases abstractas, permitiendo construir estructuras flexibles y extensibles.


# Ejemplo sobre el Proyecto 


 [Abstraccion](https://drive.google.com/file/d/1TyUh92y2P0w1qzt9Zm2MA6AglGMAF3Jf/view?usp=sharing)

  ![Abstraccion](https://github.com/user-attachments/assets/c10366b5-c151-4817-8e70-1d80a8e58dd0)

  

# Ejemplo codigo 

public abstract class Usuario {
    protected String nombre;

    public Usuario(String nombre) {
        this.nombre = nombre;
    }

   
    public abstract void accederAlSistema();
}


public class Paciente extends Usuario {

    public Paciente(String nombre) {
        super(nombre);
    }

    Override 
    public void accederAlSistema() {
        System.out.println(nombre + " accede al sistema como paciente.");
    }
}


public class Medico extends Usuario {

    public Medico(String nombre) {
        super(nombre);
    }

    
    public void accederAlSistema() {
        System.out.println(nombre + " accede al sistema como médico.");
    }
}
