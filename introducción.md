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

### 📘 Caso de uso 1: Registrar paciente: Registro exitoso de nuevo paciente

- **Actor(es) involucrado(s)**: Recepcionista, Paciente
- **Descripción breve**: El recepcionista carga los datos de un nuevo paciente en el sistema.
- **Flujo principal de eventos**:
  1. El recepcionista accede al sistema.
  2. Ingresa usuario y contraseña.
  3. Selecciona modulo “Pacientes”.
  4. Ingresa a “Registrar nuevo paciente” .
  5. Ingresa DNI del paciente.
  6. El sistema recibe el DNI del paciente.
  7. El sistema verifica si el usuario ya existe en la base de datos.
  8. Si el usuario ya existe se muestra mensaje de usuario existente.
  9. Si el usuario es nuevo semuestra el formulario de registro.
  10. El sistema valida los datos ingresados.
  11. Si los datos ingresados son incorrectos se extiende un mensaje de error.
  12. En caso de ser correctos se confirma el registro.
  13. Se guardan los datos en la base de datos.
  14. Se genera un nuevo usuario.
- **Precondiciones**:
- 1. El recepcionista debe haber iniciado sesión.
  2. El paciente no debe estar registrado previamente (el sistema debería verificar duplicados por DNI).
- **Postcondiciones**:
  1. El nuevo paciente queda registrado en el sistema con un ID único.
  2. Sus datos están disponibles para futuros turnos o consultas.

---

### 📘 Caso de uso 2: Agendar turno: Turno agendado exitosamente

- **Actor(es) involucrado(s)**: Recepcionista, Paciente
- **Descripción breve**: Permite asignar un turno entre un paciente y un profesional.
- **Flujo principal de eventos**:
  1. El recepcionista accede al sistema.
  2. Ingresa usuario y contraseña.
  3. Selecciona modulo “Mis turnos”.
  4. Selecciona especialidad.
  5. Selecciona médico.
  6. El sistema valida las fechas y horarios disponibles.
  7. Consulta disponibilidad al médico.
  8. En caso de no haber disponibilidad se extiende mensaje de error.
  9. En caso de haber disponibilidad guarda la fecha y hora como disponible.
  10. El recepcionista selecciona fecha y horario.
  11. El sistema genera una notificación o comprobante del turno para el paciente.
  12. El sistema valida que no exista superposición ni conflictos.
  13. En caso de existir un conflicto se extiende mensaje de error.
  14. En caso de que todo sea correcto se confirma la agenda.
  15. Se genera mensaje de turno confirmado.    
- **Precondiciones**:
  - El paciente debe existir en el sistema.
  - Debe existir al menos un médico disponible para la especialidad solicitada.
  - El recepcionista debe tener acceso autorizado al sistema.
- **Postcondiciones**:
  - Se genera un turno asignado a un paciente y un médico con fecha y hora específicas.
  - Se actualiza la disponibilidad del médico para reflejar ese turno como ocupado.

---

### 📘 Caso de uso 3: Consultar turnos: Correcta consulta de turnos

- **Actor(es) involucrado(s)**: Recepcionista, Paciente, Médico
- **Descripción breve**: El sistema muestra los turnos agendados en una fecha y hora específica.
- **Flujo principal de eventos**:
  1. El recepcionista accede al sistema.
  2. Ingresa usuario y contraseña.
  3. Selecciona modulo “Mis turnos”.
  4. Aplica filtro.
  5. El sistema busca resultados dependiendo del filtro aplicado.
  6. El sistema consulta la agenda en la base de datos.
  7. En caso de no encontrar resultados se extiende un mensaje de error.
  8. Si se encuentran resultados se muestra lista de turnos coincidentes.
  9. El recepcionista selecciona ver detalles.
  10. Se muestran los detalles del turno (fecha, hora).
  11. El usuario observa los detalles de su turno.
- **Precondiciones**:
  - El sistema debe contener al menos un turno agendado.
- **Postcondiciones**:
  - Se muestra la información solicitada.

---

### 📘 Caso de uso 4: Cancelar turno: Turno cancelado con éxito

- **Actor(es) involucrado(s)**: Paciente, Recepcionista, Médico
- **Descripción breve**: Se cancela un turno previamente asignado.
- **Flujo principal de eventos**:
  1. El recepcionista accede al sistema.
  2. Ingresa usuario y contraseña.
  3. Selecciona modulo “Mis turnos”.
  4. Aplica filtro.
  5. El sistema busca resultados dependiendo del filtro aplicado.
  6. El sistema consulta la agenda en la base de datos.
  7. En caso de no exixtir resultados se extiende un mensaje de error.
  8. Si se encuentran resultados se muestra lista de turnos coincidentes.
  9. El recepcionista selecciona ver detalles.
  10. Se muestran los detalles del turno (fecha, hora, médico).
  11. Observa los detalles de su turno.
  12. Selecciona la opción de “Cancelar turno”.
  13. El sistema envia notificación de cancelación al médico y al paciente.
- **Precondiciones**:
  - El paciente debe tener un turno previamente asignado.  
  - El turno debe estar vigente (no pasado).
- **Postcondiciones**:
  - El turno queda registrado como “cancelado”.  
  - La fecha y hora quedan disponibles nuevamente para otros pacientes.

---

### 📘 Caso de uso 5: Enviar notificación: 

- **Actor(es) involucrado(s)**: Sistema, Recepcionista
- **Descripción breve**: El sistema envía una notificación automática cuando se agenda o cancela un turno.
- **Flujo principal de eventos**:
  1. El recepcionista accede al sistema.
  2. Ingresa usuario y contraseña.
  3. Selecciona modulo “Agenda”.
  4. Aplica filtro.
  5. El sistema busca resultados dependiendo del filtro aplicado.
  6. El sistema registra el envío en la base de datos con estado "enviado" y la fecha/hora.
  7. El sistema consulta la agenda en la base de datos.
  8. En caso de no encontrar resultados se extiende un mensaje de error.
  9. En caso de encontrar resultados se muestra lista de turnos coincidentes.
  10. El recepcionista selecciona ver detalles.
  11. Se muestran los detalles del turno (fecha, hora, paciente, médico).
  12. Selecciona enviar recordatorio.
  13. El sistema envia recordatorio de notificación.
  14. El paciente recibe notificación.
- **Precondiciones**:
  - El paciente debe tener un email registrado.
- **Postcondiciones**: 
  - El paciente recibe la notificación correspondiente.
    
---

## Boceto inicial del diseño de clases

![Boceto inicial del diseño de clases](https://github.com/user-attachments/assets/18f1f42e-c8fa-4fa2-96cd-c6677142bc95)

🔗 [Ver diseño en línea](https://drive.google.com/file/d/1UOw3Kq7-UQuhZ02jkWhHSQsnGpOgHLhV/view?usp=sharing)
