# Introducción

## ¿Qué es la programación orientada a objetos?

La programación orientada a objetos (POO) es un paradigma de programación que organiza el software en entidades llamadas objetos, que contienen tanto datos como comportamientos.
Es crucial para construir sistemas eficientes y escalables.

POO es importante porque permite:
- Reutilizar código
- Facilitar el mantenimiento
- Promover el diseño modular
- Reflejar de forma más natural el mundo real

---

## Ejemplos de los cuatro fundamentos de la POO

### 1. Abstracción
-Consiste en simplificar la complejidad del mundo real modelando solo los aspectos esenciales relevantes para el sistema.

**Ejemplo**: Un turno en un hospital representa solo la información necesaria (fecha, hora, paciente), sin detalles internos.

### 2. Encapsulamiento
-Es el proceso de ocultar la implementación interna de un objeto y exponer sólo las interfaces públicas.

**Ejemplo**: Un cajero automático solo muestra una interfaz al usuario, pero oculta cómo maneja internamente las transacciones.

### 3. Herencia
-Es un mecanismo que permite que un objeto herede propiedades y comportamientos de otro objeto.

**Ejemplo**: La clase `Empleado` puede ser la base para `Médico`, `Enfermero`, etc., que heredan sus propiedades básicas.

### 4. Polimorfismo
-Se refiere a la capacidad de los objetos de una misma jerarquía de clases para responder de manera diferente a un mismo mensaje.

**Ejemplo**: Un método `imprimirDatos()` puede actuar diferente según se aplique a un `Paciente` o a un `Turno`.

---

## Requisitos funcionales

1. El sistema debe permitir registrar pacientes.
2. El sistema debe permitir agendar turnos.
3. El sistema debe listar turnos agendados por fecha y hora.
4. El sistema debe cancelar un turno previamente registrado.
5. El sistema debe enviar notificaciones por correo electrónico o apps de mensajeria.

---

## Casos de uso

---

### 📘 Caso de uso 1: Registrar paciente

- **Actor(es) involucrado(s)**: Recepcionista
- **Descripción breve**: El recepcionista carga los datos de un nuevo paciente en el sistema.
- **Flujo principal de eventos**:
  1. El recepcionista inicia sesión en el sistema.
  2. Desde el menú principal, selecciona la opción “Registrar paciente”.
  3. El sistema muestra un formulario vacío de registro.
  4. El recepcionista solicita al paciente sus datos personales (nombre completo, DNI, fecha de nacimiento, email, número de teléfono, dirección, etc.).
  5. El recepcionista completa el formulario con la información proporcionada.
  6. El sistema valida los campos obligatorios y el formato de los datos (por ejemplo, que el email tenga formato válido, que el DNI no esté duplicado).
  7. Si hay errores en la validación, el sistema muestra mensajes indicando los campos que deben corregirse.
  8. Una vez corregidos los errores (si los hubo), el recepcionista confirma el registro.
  9. El sistema guarda los datos en la base de datos.
  10. El sistema muestra un mensaje de confirmación del alta del paciente.
  11. El sistema ofrece la opción de agendar un turno para el paciente recién registrado.
- **Precondiciones**:
- 1. El recepcionista debe haber iniciado sesión.
  2. El paciente no debe estar registrado previamente (el sistema debería verificar duplicados por DNI).
- **Postcondiciones**:
  1. El nuevo paciente queda registrado en el sistema con un ID único.
  2. Sus datos están disponibles para futuros turnos o consultas.

---

### 📘 Caso de uso 2: Agendar turno

- **Actor(es) involucrado(s)**: Recepcionista, Paciente
- **Descripción breve**: Permite asignar un turno entre un paciente y un profesional.
- **Flujo principal de eventos**:
  1. El paciente solicita un turno, de forma presencial o telefónica, indicando la especialidad que necesita.
  2. El recepcionista accede al sistema y selecciona la opción "Agendar turno".
  3. El sistema solicita identificar al paciente. El recepcionista busca por DNI o nombre.
  4. Si el paciente no está registrado, el sistema permite registrarlo (ver Caso de uso 1).
  5. Una vez identificado el paciente, el sistema solicita elegir:
      - Especialidad médica
      - Profesional (si ya tiene uno asignado)
      - Día y horario preferido
  6. El sistema muestra los profesionales disponibles según la especialidad y sus horarios libres.
  7. El recepcionista selecciona el profesional y el horario.
  8. El sistema verifica que el turno esté disponible y que no exista superposición con otros turnos asignados.
  9. Si todo es válido, el recepcionista confirma el turno.
  10. El sistema registra el turno en la base de datos, relacionando paciente, médico, fecha y hora.
  11. El sistema genera una notificación o comprobante del turno para el paciente.
  12. El sistema puede enviar automáticamente un aviso por correo o mensaje al paciente y al médico.
  13. El sistema muestra un mensaje de confirmación de que el turno fue asignado correctamente.    
- **Precondiciones**:
  - El paciente debe existir en el sistema.
  - Debe existir al menos un médico disponible para la especialidad solicitada.
  - El recepcionista debe tener acceso autorizado al sistema.
- **Postcondiciones**:
  - Se genera un turno asignado a un paciente y un médico con fecha y hora específicas.
  - Se actualiza la disponibilidad del médico para reflejar ese turno como ocupado.

---

### 📘 Caso de uso 3: Consultar turnos

- **Actor(es) involucrado(s)**: Recepcionista
- **Descripción breve**: El sistema muestra los turnos agendados en una fecha y hora específica.
- **Flujo principal de eventos**:
  1. El actor (recepcionista) accede al sistema con sus credenciales.
  2. Desde el menú principal, selecciona la opción "Mis turnos", luego "Consultar agenda".
  3. El sistema solicita los filtros de búsqueda: profesional, fecha o rango de fechas.
  4. El actor elige el profesional (puede ser él mismo si es médico) y la fecha deseada.
  5. El sistema consulta la base de datos y muestra la agenda correspondiente:
      - Horarios disponibles y ocupados
      - Nombre del paciente asignado
      - Especialidad del turno (si aplica)
      - Estado del turno (activo, cancelado, finalizado)
  6. El actor puede cambiar de fecha o profesional desde la misma vista para navegar por la agenda.
  7. El sistema permite imprimir o exportar la agenda.
  8. Se muestra una opción para volver al menú principal.
- **Precondiciones**:
  - El sistema debe contener al menos un turno agendado.
- **Postcondiciones**:
  - Se muestra la información solicitada.

---

### 📘 Caso de uso 4: Cancelar turno

- **Actor(es) involucrado(s)**: Paciente, Recepcionista
- **Descripción breve**: Se cancela un turno previamente asignado.
- **Flujo principal de eventos**:
  1. El actor (paciente o recepcionista) inicia sesión en el sistema con sus credenciales.
  2. Desde el menú principal, selecciona la opción "Mis turnos", luego "Cancelar turno".
  3. El sistema muestra una lista de los turnos que tiene agendados el paciente.
  4. El paciente selecciona el turno que desea cancelar.
  5. El sistema muestra los detalles del turno seleccionado y solicita confirmación para cancelarlo.
  6. El paciente o recepcionista confirma la cancelación.
  7. El sistema actualiza el estado del turno en la base de datos a “cancelado”.
  8. El sistema libera ese turno para que pueda ser tomado por otro paciente.
  9. Se muestra un mensaje de confirmación de la cancelación al usuario.
- **Precondiciones**:
  - El paciente debe tener un turno previamente asignado.  
  - El turno debe estar vigente (no pasado).
- **Postcondiciones**:
  - El turno queda registrado como “cancelado”.  
  - La fecha y hora quedan disponibles nuevamente para otros pacientes.

---

### 📘 Caso de uso 5: Enviar notificación por email

- **Actor(es) involucrado(s)**: Sistema
- **Descripción breve**: El sistema envía una notificación automática cuando se agenda o cancela un turno.
- **Flujo principal de eventos**:
  1. El sistema detecta un evento relevante que requiere notificación (por ejemplo: confirmación de turno, recordatorio, cancelación, modificación).
  2. El sistema obtiene los datos del paciente destinatario (nombre, email, tipo de turno, fecha, etc.).
  3. Se genera automáticamente el contenido del correo según el tipo de notificación.
  4. El sistema establece conexión con el servidor de correo configurado.
  5. Se envía el email al destinatario.
  6. El sistema registra el envío en la base de datos con estado "enviado" y la fecha/hora.
  7. Si ocurre un error en el envío, el sistema:
      - Lo registra como "fallido"
      - Notifica al administrador del sistema para su seguimiento.
  8. El usuario (si corresponde) recibe confirmación del envío (en pantalla o como mensaje de estado).
- **Precondiciones**:
  - El paciente debe tener un email registrado.
- **Postcondiciones**: 
  - El paciente recibe la notificación correspondiente.
    
---

## Boceto inicial del diseño de clases

![Boceto inicial del diseño de clases](https://github.com/user-attachments/assets/0302a2d2-520b-45d3-bdfb-b5b53ec9e684)

🔗 [Ver diseño en línea](https://www.canva.com/design/DAGfZdsR-3I/9b2ppf3IxeTbV9T1gSPsUg/edit?utm_content=DAGfZdsR-3I&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
