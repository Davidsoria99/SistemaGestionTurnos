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
Uno de los problemas que enfrenta el sistema actual es que distintas clases tienen que adaptarse a una estructura genérica de funcionalidades, incluso cuando muchas de esas funcionalidades no se relacionan con su propósito. Por ejemplo, si todos los usuarios (**paciente**, **médico**, **recepcionista**) implementaran una interfaz **IUsuario** con métodos como **asignarTurno()**, **cancelarTurno()**, **verHistorial()**, etc., estaríamos obligando a subclases como **Paciente** o **Médico** a implementar métodos que no les corresponden, generando confusión, código innecesario y una arquitectura rígida.

Aplicar ISP permite definir interfaces más pequeñas y específicas como:
- **IPaciente:** consultar turnos, cancelar turno, actualizar datos.
- **IMedico:** ver agenda, registrar observaciones de consulta.
- **IRecepcionista:** agendar turnos, cancelar turnos, registrar nuevos pacientes.

Ejemplo del mundo real: Supongamos que tenemos una interfaz *IUsuarioSistema* que incluye métodos como *registrarPaciente()*, *cancelarTurno()*, *verHistorialMedico()*, *crearAgendaMedica()* y *modificarEspecialidades()*.
Si tanto el Paciente como el Recepcionista implementan esa interfaz completa, estarían obligados a implementar métodos que no les corresponden.

La solucón aplicando ISP seria definir interfaces más pequeñas y especificas:

IPaciente con métodos como solicitarTurno(), cancelarTurno(), verHistorial()

IRecepcionista con métodos como registrarPaciente(), crearTurno(), modificarDatos()

Así, cada clase solo implementa lo que realmente necesita.

---

## Estructura de Clases
![ISP](https://github.com/user-attachments/assets/00860814-b977-489d-8eda-7c79741525e6)
* [Principio de Segregación de Interfaces (ISP)](https://drive.google.com/file/d/1_j09-WbK4J3YFS2VdBCh5wqw48rvJI2O/view?usp=sharing)

