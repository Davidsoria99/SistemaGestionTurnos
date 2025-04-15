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

