# Principio de Segregación de Interfaces (ISP)
Propósito y Tipo del Principio SOLID: Este principio establece que una clase no debe verse obligada a depender de interfaces que no utiliza. Es decir, cada interfaz debe estar enfocada en un conjunto específico y coherente de funcionalidades.

En el sistema de gestión de turnos, este principio ayuda a evitar que clases como **Paciente**, **Médico** o **Recepcionista** implementen métodos que no les son relevantes. Por ejemplo, no tendría sentido que un **Paciente** tenga que implementar métodos como **crearTurnoParaOtro** o **verAgendaCompleta**, que sí corresponden a un **Recepcionista**.

Al aplicar este principio:
- Se crean interfaces específicas para cada rol (como **IConsultaTurnos**, **IGestionAgenda**, **IActualizaDatos**, etc.).
- Las clases solo implementan las interfaces necesarias según su responsabilidad.
- Se reduce el acoplamiento y se facilita la extensión del sistema.

Esto hace que el código sea más limpio, intuitivo y fácil de mantener, especialmente cuando el sistema crece o cambian los requisitos.

---

## Motivación
Uno de los problemas que enfrenta el sistema actual es que distintas clases tienen que adaptarse a una estructura genérica de funcionalidades, incluso cuando muchas de esas funcionalidades no se relacionan con su propósito. Por ejemplo, si todos los usuarios (**paciente**, **médico**, **recepcionista**) implementaran una interfaz **<<IUsuario>>** con métodos como **asignarTurno()**, **cancelarTurno()**, **verHistorial()**, etc., estaríamos obligando a subclases como **Paciente** o **Médico** a implementar métodos que no les corresponden, generando confusión, código innecesario y una arquitectura rígida.
