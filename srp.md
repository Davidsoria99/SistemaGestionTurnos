# Principio de Responsabilidad Única (SRP)
Proposito y Tipo del Principio SOLID: Este principio establece que una clase debe tener una única razón para cambiar, es decir, debe encargarse de una única responsabilidad dentro del sistema.

En el caso del sistema de gestión de turnos, este principio permite separar claramente las funcionalidades: registrar pacientes, asignar turnos, enviar notificaciones, o gestionar historiales, en clases independientes. Esto evita que una sola clase controle múltiples procesos a la vez, lo cual genera acoplamiento innecesario, errores frecuentes y un diseño difícil de mantener.

Al aplicar este principio:
- El código es más claro y más fácil de testear.
- Cada clase se enfoca en hacer bien una sola cosa.
- El mantenimiento del sistema se vuelve más sencillo y menos propenso a errores.
---
## Motivación
Antes de aplicar el principio de Responsabilidad Única, el sistema agrupaba múltiples tareas dentro de una misma clase, como por ejemplo una clase Turno que no solo almacenaba información sobre el turno, sino que también se encargaba de verificar disponibilidad, enviar notificaciones, validar horarios y registrar historial. Este enfoque hacía que cualquier pequeño cambio en una funcionalidad (por ejemplo, cambiar cómo se envía una notificación) afectara todo el sistema, generando errores inesperados y dificultando el mantenimiento.

Con SRP, se decide dividir las responsabilidades:
- La clase *Turno* se encarga exclusivamente de almacenar la información del turno.
- La verificación de disponibilidad se delega a la clase *Agenda*.
- Las notificaciones las gestiona una clase *Notificador*.
- El historial lo maneja la clase *HistorialPaciente*.

Ejemplo del mundo real:
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
