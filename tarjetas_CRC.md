## Tarjetas CRC
Las tarjetas CRC (Clase, Responsabilidad, Colaboración) es una herramienta utilizada en el diseño de software orientado a objetos. Sirve como una forma visual y sencilla de explorar cómo interactúan las clases dentro de un sistema, ayudando a asignar tareas específicas a cada clase y a entender con qué otras clases necesita comunicarse para cumplir sus funciones.

- ### Tarjeta CRC: Médico
- **Nombre de la Clase:** Médico

- **Superclase:** Persona

- **Subclase:** (Ninguna)

- **Responsabilidades:** Atender turnos asignados, Consultar su agenda de turnos, Registrar observaciones de las consultas, Actualizar sus datos de contacto y horarios.

- **Colaboradores:** Turno, Paciente, Agenda, Recepcionista.

- **Pensamiento del objeto:** Atiendo a los pacientes en los horarios definidos. Estoy disponible según mi especialidad. Requiero ver mis turnos agendados y actualizar mis horarios si es necesario. Mis datos de contacto pueden cambiar.

- **Propiedad:** nombre, apellido, fechaNacimiento, DNI, especialidad, matrícula, horarioAtención, teléfono, email.

 ![CRC1](https://github.com/user-attachments/assets/c66694b3-a4d1-48c9-8545-c74a4ac54a7d)
 ---
- ### Tarjeta CRC: Agenda
- **Nombre de la Clase:** Agenda

- **Superclase:** (Ninguna)

- **Subclase:** (Ninguna)

- **Responsabilidades:** Registrar nuevos turnos en la agenda, Consultar disponibilidad de horarios, Actualizar el estado de un turno (pendiente, confirmado, cancelado).

- **Colaboradores:** Turno, Médico, Paciente, Recepcionista.

- **Pensamiento del objeto:** Registro todos los turnos asignados con fecha, hora y estado. Coordino los encuentros entre médicos y pacientes. Permito consultar la disponibilidad y actualizar la planificación según cancelaciones o nuevos turnos.

- **Propiedad:** listaTurnos, fecha, hora, estado, motivo, observaciones.

![CRC2](https://github.com/user-attachments/assets/638f9b5b-61ad-4c6c-864c-6b5d75d8672b)
---
- ### Tarjeta CRC: Turno
- **Nombre de la Clase:** Turno

- **Superclase:** (Ninguna)

- **Subclase:** (Ninguna)

- **Responsabilidades:** Almacenar los datos de la cita médica, Mostrar detalles del turno, Permitir reprogramación o anulación.

- **Colaboradores:** Agenda, Paciente, Médico, Recepcionista.

- **Pensamiento del objeto:** Represento una cita programada entre un paciente y un médico. Sé cuándo, dónde y con quién se realiza el encuentro. Puedo ser confirmado, cancelado o modificado si es necesario.

- **Propiedad:** fecha, hora, estado, motivo, observaciones, idPaciente, idMedico.

![CRC3](https://github.com/user-attachments/assets/0e101105-8d51-4bb2-ba4d-cba8eed849b7)
---
- ### Tarjeta CRC: Paciente
- **Nombre de la Clase:** Paciente

- **Superclase:** Persona

- **Subclase:** (Ninguna)

- **Responsabilidades:** Solicitar un turno, Consultar sus turnos programados, Cancelar un turno, Actualizar sus datos personales, Ver el historial de sus consultas.

- **Colaboradores:** Agenda, Turno, Médico, Recepcionista.

- **Pensamiento del objeto:** Sé qué especialista necesito y guardo mis datos personales. Quiero saber cuándo y con quién tengo turno. Aviso si no puedo asistir. Mis datos pueden cambiar. También me interesa ver mi historial de turnos.

- **Propiedad:** nombre, apellido, fechaNacimiento, DNI, telefono, email, idPaciente, idMedico.

![CRC4](https://github.com/user-attachments/assets/6faaa324-0d2c-46b2-a867-aad2255676ae)
---
- ### Tarjeta CRC: Recepcionista
- **Nombre de la Clase:** Recepcionista

- **Superclase:** Persona

- **Subclase:** (Ninguna)

- **Responsabilidades:** Registrar pacientes nuevos, Agendar turnos a solicitud de pacientes, Cancelar turnos cuando se solicite.

- **Colaboradores:** Paciente, Turno, Agenda, Médico.

- **Pensamiento del objeto:** Soy quien gestiona el ingreso y administración de los pacientes. Me encargo de registrar nuevos pacientes, programar y cancelar turnos, y mantener actualizada la agenda. Brindo asistencia básica a médicos y pacientes sobre el uso del sistema.

- **Propiedad:** idPaciente, idMedico, nombre, apellido, DNI, email, telefono.

![CRC5](https://github.com/user-attachments/assets/5f3fd80a-fdcb-413f-98e2-b8cb2ee929df)
