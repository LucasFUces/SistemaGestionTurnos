# Herencia

La herencia es un concepto que permite que una clase o un objeto adquiera atributos y comportamientos de otra clase.
Este mecanismo favorece la reutilización del código y la creación de jerarquías, donde las clases hijas (subclases) pueden ampliar o redefinir las funcionalidades de las clases padre (superclases).
Su relevancia en el diseño radica en que evita la duplicación de código al compartir atributos y métodos comunes, y también mejora la organización y claridad del sistema, ya que permite modelar relaciones jerárquicas naturales entre diferentes entidades.
Este principio se vincula con el Principio de Sustitución de Liskov, ya que una subclase puede ser utilizada en cualquier lugar donde se espere una instancia de la clase base, sin afectar el funcionamiento del sistema.
Por ejemplo, un método que reciba un objeto del tipo Persona puede operar tanto con un Paciente como con un Medico, sin necesidad de modificar su implementación.
En cuanto a su relación con los patrones de diseño, se asocia con el patrón creacional Factory Method, que permite instanciar objetos de diferentes subclases a partir de una clase base común (como Persona). 
Por ejemplo, el sistema puede decidir si crear un Medico o un Paciente según el caso, sin conocer los detalles internos de cada clase. La herencia asegura que todas estas clases compartan una interfaz común, lo que permite tratarlas de manera uniforme.


# Ejemplo sobre el proyecto

* [Herencia](https://drive.google.com/file/d/1pEgJMDhQB8PJhytlgOwEFiEF_Cae_2Tu/view?usp=sharing)

  ![Herencia](https://github.com/user-attachments/assets/c85e6e19-d355-4220-99a7-f9ccdcaf95b1)
