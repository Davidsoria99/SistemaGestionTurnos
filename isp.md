# Principio de Segregación de Interfaces (ISP)
Propósito y Tipo del Principio SOLID: Este principio establece que una clase no debe verse obligada a depender de interfaces que no utiliza. Es decir, cada interfaz debe estar enfocada en un conjunto específico y coherente de funcionalidades.

---

## Motivación

En el sistema de gestión de turnos, este principio se aplica separando las responsabilidades de cada actor en interfaces más pequeñas. Por ejemplo:

`IVisualizadorTurno` contiene solo el método `verTurno()` y es implementada por clases encargadas de mostrar los turnos.

`IConfirmadorTurno` contiene solo `confirmarTurno()` y lo implementan las clases que validan o aceptan turnos.

`IModificadorTurno` define `reprogramarTurno()` y lo implementan las clases que permiten modificar turnos existentes.

De esta forma, cada clase depende únicamente de las operaciones que realmente necesita usar.

---

**Ejemplo del mundo real**: Suponiendo que se define una interfaz genérica `ITurno` con métodos como `verTurno()`, `confirmarTurno()`, `reprogramarTurno()`. Si todas las clases (como `Visualizador`, `confirmaciónTurno` y `modificarTurno`) implementaran esta interfaz, estaríamos obligando a todas a tener métodos que no necesitan.

En cambio, aplicando ISP, cada clase implementa solo una interfaz específica: `Visualizador` implementa `IVisualizadorTurno`, `confirmaciónTurno` implementa `IConfirmadorTurno`, y así sucesivamente.

---

## Estructura de Clases
![ISP](https://github.com/user-attachments/assets/00860814-b977-489d-8eda-7c79741525e6)
* [Principio de Segregación de Interfaces (ISP)](https://drive.google.com/file/d/1_j09-WbK4J3YFS2VdBCh5wqw48rvJI2O/view?usp=sharing)

