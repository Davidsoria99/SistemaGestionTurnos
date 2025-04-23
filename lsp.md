# Principio de Sustitución de Liskov (LSP)
Propósito y Tipo del Principio SOLID: Este principio establece que una subclase debe poder ser utilizada en lugar de su superclase sin que el comportamiento del sistema se vea alterado. El mismo asegura que el uso de la herencia respete la lógica del programa, manteniendo la coherencia en el comportamiento de los objetos.

En el sistema de gestión de turnos, este principio se aplica al definir una clase general Usuario, de la cual heredan subclases como Paciente, Médico y Recepcionista. Cada una de estas puede ser utilizada en contextos donde se espera un Usuario, sin provocar errores ni modificar la lógica del sistema.

Por ejemplo, si un módulo del sistema requiere mostrar los datos de contacto de un Usuario, debería funcionar correctamente tanto si se trata de un Paciente como de un Médico, siempre que estas subclases respeten la estructura y el comportamiento definidos por la superclase. Esto permite reutilizar funcionalidades y extender el sistema de forma más robusta y predecible.

---

## Motivación
En los primeros diseños del sistema de gestión de turnos, se trataba a cada tipo de usuario (paciente, médico, recepcionista) como entidades totalmente independientes, sin una estructura común. Esto generaba duplicación de código, dificultades para implementar nuevas funcionalidades compartidas (como acceder al perfil o actualizar datos de contacto), y problemas al usar estos objetos en módulos genéricos del sistema.

Al aplicar el Principio de Sustitución de Liskov, se introdujo una superclase común: **Usuario**, con atributos y métodos compartidos, como **nombre**, **email**, **telefono**, y métodos como **modificarDatos()**. Luego, **Paciente**, **Médico** y **Recepcionista** heredan de esta clase y especializan su comportamiento cuando es necesario, de esta manera se logro solucionar el problema de los primeros diseños del sistema.

Ejemplo del mundo real: Imaginemos que el sistema tiene una función para mostrar información de contacto de cualquier usuario del sistema.

Gracias al LSP, esa función puede recibir un objeto de tipo **Usuario** y funcionar sin problemas, sin importar si se trata de un **Paciente** o un **Médico**, porque ambos respetan el contrato definido por la superclase. Si el sistema intentara usar un objeto que no implementa correctamente esos métodos, se rompería la lógica.

Este principio garantiza que la herencia esté bien aplicada, evita errores inesperados y facilita que el sistema crezca de forma controlada, sin romper funcionalidades existentes

---

## Estructura de Clases
![LSP](https://github.com/user-attachments/assets/025d292f-5d9b-48b8-8c92-8695a0b52cf8)
* [Principio de Sustitución de Liskov (LSP)](https://drive.google.com/file/d/1BMB3sRRedLvNc4b_gSKdlSqU8fIrsjY2/view?usp=sharing)
