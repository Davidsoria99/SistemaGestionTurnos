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
