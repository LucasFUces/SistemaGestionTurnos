# Polimorfismo

El polimorfismo es la capacidad que tienen los objetos dentro de una misma jerarquía de clases para responder de manera diferente a un mismo mensaje o llamada a método. 
Esto significa que, aunque se invoque un método con el mismo nombre, cada objeto puede ejecutar su propia versión adaptada a su tipo específico.
Su importancia en el diseño orientado a objetos radica en que permite escribir código genérico que funciona con distintos tipos de objetos sin necesidad de conocer sus detalles internos. 
Además, fomenta el uso de interfaces o clases base que definen contratos comunes, los cuales son implementados por las subclases según sus necesidades particulares.
El polimorfismo también se puede relacionar con el Principio de Segregación de Interfaces, ya que este establece que las clases no deben estar obligadas a implementar métodos que no utilizan. 
Por lo tanto, si este principio se respeta, cada subclase implementa únicamente los métodos que le corresponden, y el código puede hacer uso del polimorfismo para invocar métodos comunes —como por ejemplo getDatos()—, obteniendo una respuesta diferente según la implementación específica de cada clase.

# Ejemplo del Proyecto 

* [Diagrama de Clases](https://drive.google.com/file/d/10vrPryA6Za3yyEBxLM8I6_cHeOIMNuuI/view?usp=sharing)

  ![Polimorfismo](https://github.com/user-attachments/assets/371d0ffe-ccaf-432a-9b8a-a990a49bc649)




# Ejemplo CODIGO

class Persona {
    String solicitarRegistrarse() {
        return "Registro genérico";
    }
}

class Medico extends Persona {
    String solicitarRegistrarse() {
        return "Registro médico";
    }
}

class Paciente extends Persona {
    String solicitarRegistrarse() {
        return "Registro paciente";
    }
}

El diagrama representa el polimorfismo a través de la jerarquía de herencia entre la superclase Persona y las subclases Médico y Paciente. Ambas clases comparten atributos y métodos comunes definidos en Persona, pero cada una puede implementar o redefinir dichos métodos según sus necesidades específicas.

Por ejemplo, el método solicitarRegistrarse() está definido en la clase Persona, pero puede ser implementado de manera distinta en Médico y Paciente para adaptarse al comportamiento particular de cada uno.
