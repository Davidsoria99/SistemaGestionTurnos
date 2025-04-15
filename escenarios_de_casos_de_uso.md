### Escenario de Caso de Uso 1

- **Nombre del caso de uso:** Solicitar Turno  
- **ID Única:** CU-001  
- **Área:** Gestión de Turnos  
- **Actor(es):** Paciente  
- **Descripción:** El paciente solicita un turno médico especificando especialidad, profesional, fecha y hora deseada.  
- **Activar Evento:** El paciente accede al sistema y elige la opción “Solicitar Turno”.  
- **Tipo de señal:** Externa (iniciada por el usuario paciente).  
- **Pasos desempeñados (ruta principal):**
  1. El paciente accede al sistema.  
  2. Elige la opción "Solicitar Turno".  
  3. Selecciona la especialidad médica.  
  4. El sistema muestra la lista de médicos disponibles.  
  5. El paciente elige un médico.  
  6. El sistema muestra los días y horarios disponibles.  
  7. El paciente selecciona fecha y hora.  
  8. El sistema confirma la solicitud y registra el turno como pendiente.  
- **Precondiciones:**
  - El paciente debe estar registrado en el sistema.  
  - El paciente debe haber iniciado sesión.  
- **Poscondiciones:**
  - El turno queda registrado en estado “pendiente”.  
  - El paciente recibe la confirmación del turno solicitado.  
- **Suposiciones:**
  - El paciente cuenta con acceso a internet y puede ingresar al sistema.  
  - Existen horarios disponibles para la especialidad solicitada.  
- **Reunir requerimientos:**
  - El sistema debe permitir navegar y filtrar por especialidad.  
  - Se debe validar la disponibilidad de horarios antes de confirmar.  
- **Aspectos sobresalientes:**
  - ¿Qué pasa si no hay disponibilidad en la fecha deseada?  
  - ¿Se permite cancelar o reprogramar más adelante?  
- **Prioridad:** Alta  
- **Riesgo:** Medio

---

### Escenario de Caso de Uso 2

- **Nombre del caso de uso:** Confirmar Turno  
- **ID Única:** CU-003  
- **Área:** Gestión de Turnos / Panel Médico  
- **Actor(es):** Médico  
- **Descripción:** El médico accede al sistema y confirma los turnos pendientes que tiene asignados.  
- **Activar Evento:** El médico inicia sesión en el sistema y accede a su agenda.  
- **Tipo de señal:** Externa (acción del médico).  
- **Pasos desempeñados (ruta principal):**
  1. El médico accede al sistema con sus credenciales.  
  2. Selecciona la opción “Ver agenda de turnos”.  
  3. El sistema muestra la lista de turnos asignados.  
  4. El médico revisa los turnos pendientes.  
  5. Selecciona un turno y hace clic en “Confirmar”.  
  6. El sistema actualiza el estado del turno a “confirmado”.  
  7. El paciente es notificado de la confirmación.  
- **Precondiciones:**
  - El turno debe estar previamente asignado a ese médico.  
  - El médico debe tener acceso al sistema.  
- **Poscondiciones:**
  - El estado del turno cambia a “confirmado”.  
  - El paciente puede ver la confirmación en su panel.  
- **Suposiciones:**
  - El médico tiene turnos pendientes que requieren confirmación.  
  - El sistema permite la modificación del estado del turno.  
- **Reunir requerimientos:**
  - El sistema debe permitir la confirmación individual de turnos.  
  - Debe notificar automáticamente al paciente.  
- **Aspectos sobresalientes:**
  - ¿Se puede confirmar masivamente más de un turno?  
  - ¿Qué sucede si el médico no confirma a tiempo?  
- **Prioridad:** Alta  
- **Riesgo:** Medio

---

### Escenario de Caso de Uso 3

- **Nombre del caso de uso:** Cancelar Turno  
- **ID Única:** CU-002  
- **Área:** Gestión de Turnos  
- **Actor(es):** Paciente  
- **Descripción:** Permite al paciente cancelar un turno previamente solicitado antes de la fecha del mismo.  
- **Activar Evento:** El paciente accede al sistema y selecciona un turno que desea cancelar.  
- **Tipo de señal:** Externa (iniciada por el paciente).  
- **Pasos desempeñados (ruta principal):**
  1. El paciente accede al sistema.  
  2. Se dirige a la sección "Mis turnos".  
  3. Visualiza la lista de turnos asignados.  
  4. Selecciona el turno que desea cancelar.  
  5. El sistema solicita confirmación.  
  6. El paciente confirma la cancelación.  
  7. El sistema cambia el estado del turno a “cancelado”.  
  8. El sistema actualiza el historial del paciente.  
- **Precondiciones:**
  - El paciente debe tener un turno previamente asignado.  
  - El turno debe estar vigente (no pasado).  
- **Poscondiciones:**
  - El turno queda registrado como “cancelado”.  
  - La fecha y hora quedan disponibles nuevamente para otros pacientes.  
- **Suposiciones:**
  - El paciente puede acceder al sistema y tiene permisos para cancelar.  
  - El turno aún no fue confirmado por el médico o el plazo de cancelación no expiró.  
- **Reunir requerimientos:**
  - El sistema debe ofrecer una forma clara de cancelar turnos.  
  - Debe guardar el estado de cancelación en el historial del paciente.  
- **Aspectos sobresalientes:**
  - ¿Hay límite de tiempo antes del cual se puede cancelar?  
  - ¿Se debe notificar al médico?  
- **Prioridad:** Alta  
- **Riesgo:** Bajo

