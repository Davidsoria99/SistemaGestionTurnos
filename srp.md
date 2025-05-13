# Principio de Responsabilidad Única (SRP)
Proposito y Tipo del Principio SOLID: Este principio establece que una clase debe tener una única razón para cambiar, es decir, debe encargarse de una única responsabilidad dentro del sistema.
  
---

## Motivación
En este sistema, SRP se aplica dividiendo las responsabilidades en clases específicas, cada una centrada en una funcionalidad:

La clase `Paciente` se encarga exclusivamente de solicitar y cancelar turnos, así como de consultar su historial.

La clase `Recepcionista` tiene la responsabilidad de agendar turnos, modificarlos y registrar nuevos pacientes.

La clase `Médico` gestiona únicamente su agenda, registra observaciones y modifica sus horarios de atención.

La clase `GestorDeTurnos` centraliza la lógica de creación, modificación y confirmación de turnos. Esto evita que Paciente o Recepcionista tengan que manejar la lógica directamente.

La clase `Historial` se responsabiliza de almacenar y mostrar el historial clínico del paciente, permitiendo agregar nuevas entradas de consulta.

Este diseño asegura que cada clase tenga una única razón para cambiar, según su rol específico en el sistema. Por ejemplo, si cambia la manera en la que se modifican turnos, solo debería modificarse `GestorDeTurnos`, sin afectar ni al `Médico` ni al `Paciente`.

Beneficios obtenidos al aplicar SRP:

- Claridad y organización del código.

- Facilidad para realizar cambios o mejoras sin romper otras funcionalidades.

- Facilidad para testear unidades individuales.

- Separación de lógica de dominio en componentes reutilizables

---

**Ejemplo del mundo real**:
Imaginando un recepcionista en un centro médico.

Si esa persona tuviera que:
- Cargar los datos del paciente
- Confirmar turnos
- Hacer llamadas de aviso
- Actualizar historiales clínicos
- Y además revisar la disponibilidad de los médicos

Probablemente cometería errores, se saturaría y las tareas no se harían bien. En cambio, si repartiera tareas con por ejemplo un/a secretario/a, el sistema es más eficiente y confiable.

Del mismo modo, en el sistema digital, lo mejor seria generar clases especificas para que en cada cambio notener que modificar la clase Recepcionista.

---

## Estructura de Clases
![SRP](https://github.com/user-attachments/assets/82942ab3-036a-4158-9a94-9db88fd62c68)
* [Principio de Responsabilidad Única (SRP)](https://drive.google.com/file/d/1v2ScP0652p8wsaqU7-FTzxxfZl7K-8tL/view?usp=sharing)
