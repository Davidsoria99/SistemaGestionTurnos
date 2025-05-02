# Escenarios de Casos de Uso
## Registrar paciente: Registro exitoso de nuevo paciente

- **Nombre del caso de uso:** Registro exitoso de nuevo paciente  
- **ID Única:** 001  
- **Área:** Administración 
- **Actor(es):** Personal administrativo, Paciente  
- **Descripción:** Permite al personal administrativo  y al paciente registrar/se en el sistema, incluyendo datos personales y de contacto.  
- **Activar Evento:** El personal administrativo accede al módulo de pacientes y selecciona “Registrar nuevo”.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados:
1. El paciente o personal administrativo accede al sistema.  
2. Selecciona el módulo “Pacientes”.  
3. Hace clic en “Registrar nuevo paciente”.  
4. Completa el formulario de registro.  
5. El sistema valida los datos ingresados.  
6. El personal confirma el registro.  
7. El sistema crea un perfil del paciente y muestra una confirmación exitosa.

### Información para los pasos:
- Usuario y contraseña
- Interfaz del sistema
- Interfaz del sistema
- Nombre, DNI, fecha de nacimiento, datos de contacto.
- Verificación de datos
- Resgistro del nuevo paciente
- Mensaje de confirmación

### Precondiciones:
- El usuario debe tener permisos administrativos.  

### Poscondiciones:
- El paciente queda registrado en el sistema. 

### Suposiciones: 
- El sistema valida duplicados por DNI.  

### Reunir requerimientos:
- Interfaz clara para registrar pacientes.  

### Aspectos sobresalientes:
- ¿Se puede editar la información una vez guardada?

### Prioridad:
Media  

### Riesgo:
Bajo

![ESC 1](https://github.com/user-attachments/assets/0250dc12-c8ab-4e2a-a33f-50b62a815138)


* [Registrar paciente: Registro exitoso de nuevo paciente](https://drive.google.com/file/d/1n-REjpnBQGjxBw0wlTqkmhAAZClYWyFV/view?usp=sharing)
---
## Agendar turnos: Turno agendado exitosamente

- **Nombre del caso de uso:** Agendar turnos  
- **ID Única:** 002  
- **Área:** Administración  
- **Actor(es):** Personal administrativo, Paciente  
- **Descripción:** El personal administrativo o el paciente agenda un nuevo turno para una consulta médica, eligiendo fecha, hora, médico y motivo.  
- **Activar Evento:** El usuario accede al módulo de turnos y selecciona “Mis turnos”.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados:
1. El usuario inicia sesión en el sistema.  
2. Accede al módulo “Mis turnos”.  
3. Selecciona al paciente (si es administrativo) o se autoidentifica (si es paciente).  
4. Selecciona especialidad y médico disponible.  
5. Visualiza el calendario con horarios disponibles. 
6. Selecciona fecha y hora.  
7. El sistema valida que no exista superposición ni conflictos.  
8. Confirma la agenda.
   
### Información para los pasos:
- Usuario y contraseña
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Mensaje de confirmación
- Mensaje de confirmación

### Precondiciones:
- El paciente debe estar registrado. 

### Poscondiciones:
- El turno queda registrado en el sistema.  

### Suposiciones:
- El sistema tiene actualizada la agenda de los médicos.  

### Reunir requerimientos:
- Validación de horarios y disponibilidad médica.  

### Aspectos sobresalientes:
- ¿Puede modificarse el turno después de agendado?  

### Prioridad:
Alta  

### Riesgo:
Medio

![ESC 2](https://github.com/user-attachments/assets/9f98fde5-c92d-40da-bc85-1f79b224cbb5)

* [Agendar turnos: Turno agendado exitosamente](https://drive.google.com/file/d/10z9Xa16iEWLl0yR-7WBe7_o61Tgi3ak4/view?usp=sharing)
---
## Consultar turnos: Correcta consulta de turnos

- **Nombre del caso de uso:** Correcta consulta de turnos  
- **ID Única:** 003  
- **Área:** Administración 
- **Actor(es):** Personal administrativo, Paciente, Médico  
- **Descripción:** Permite a los distintos actores del sistema consultar los turnos registrados, filtrando por estado, fecha, paciente o profesional.  
- **Activar Evento:** El actor accede al módulo de turnos y elige la opción de consulta.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados:
1. El usuario inicia sesión en el sistema.  
2. Accede al módulo “Mis turnos”.  
3. Aplica filtros según necesidad: fecha, estado, paciente, médico.  
4. El sistema muestra una lista de turnos coincidentes.  
5. El usuario puede seleccionar un turno para ver detalles.

### Información para los pasos:
- Usuario y contraseña
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema 

### Precondiciones:
- El usuario debe tener acceso autorizado al sistema.  

### Poscondiciones:
- El usuario visualiza los turnos solicitados.  

### Suposiciones:
- La base de datos está actualizada.  

### Reunir requerimientos:
- Interfaz intuitiva para aplicar filtros.  

### Aspectos sobresalientes:
- ¿Hay un límite en la cantidad de turnos que se pueden consultar a la vez? 

### Prioridad:
Media  

### Riesgo:
Bajo

![ESC 3](https://github.com/user-attachments/assets/87b733e1-a1e5-43bf-b726-0064f1349f80)

* [Consultar turnos: Correcta consulta de turnos](https://drive.google.com/file/d/1vtU10rtQjH3yAkoneho9cRf5hPVfbuuB/view?usp=sharing)
---
## Cancelar turnos: Turno cancelado con éxito

- **Nombre del caso de uso:** Turno cancelado con éxito  
- **ID Única:** 004  
- **Área:** Administración  
- **Actor(es):** Personal administrativo, Paciente, Médico  
- **Descripción:** Permite que los actores autorizados cancelen un turno previamente agendado, registrando el motivo de la cancelación.  
- **Activar Evento:** El usuario accede al listado de turnos y selecciona uno para cancelar.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados:
1. El usuario inicia sesión en el sistema.  
2. Accede al módulo “Mis turnos”.  
3. Aplica filtros según necesidad: fecha, estado, paciente, médico.  
4. El sistema muestra una lista de turnos coincidentes.  
5. Hace clic en la opción “Cancelar turno”.  
6. EIngresa el motivo de la cancelación. 
7. El sistema actualiza el estado del turno a “Cancelado” y registra el motivo.  
8. Se notifica al paciente y/o médico involucrado.

 ### Información para los pasos:
- Usuario y contraseña
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Interfaz del sistema
- Motivos de la cancelación
- Mensaje de confirmación
- Notificación del sistema 

### Precondiciones:
- El turno debe existir y estar en estado pendiente o confirmado. 

### Poscondiciones:
- El turno se marca como cancelado. 

### Suposiciones:
- La notificación llega correctamente al otro actor involucrado.  

### Reunir requerimientos:
- Opción clara y accesible para cancelar turnos.  

### Aspectos sobresalientes:
- ¿Existe una política de cancelación con límite de tiempo?  

### Prioridad:
Alta  

### Riesgo:
Medio

![ESC 4](https://github.com/user-attachments/assets/1442eadd-49ec-45ea-bde7-039e827be8f4)

* [Cancelar turnos: Turno cancelado con éxito](https://drive.google.com/file/d/1hKlgNY5VoIM8ncdrd4Yemolj1WTO0AWb/view?usp=sharing)
---
## Enviar notificación: Correcto funcionamiento del sistema de notificación

- **Nombre del caso de uso:** Comunicación y Alertas del Sistema				  
- **ID Única:** 005  
- **Área:** Comunicación del Sistema  
- **Actor(es):** Sistema (automático), Personal administrativo				  
- **Descripción:** Este caso de uso permite que el sistema, de forma automática o por acción del personal, envíe notificaciones a pacientes y médicos ante eventos relevantes como confirmaciones, recordatorios o          cancelaciones de turnos.  
- **Activar Evento:** Se confirma, modifica o cancela un turno, o se produce un evento programado para enviar recordatorios.				  
- **Tipo de señal:** Temporal.  

### Pasos desempeñados:
1. Se registra un evento relevante (nuevo turno, cancelación, recordatorio).		  
2. El sistema verifica el tipo de evento y destinatarios.		  
3. Se genera el contenido del mensaje (fecha, hora, tipo de turno, médico, etc.).		  
4. El sistema elige el canal de notificación (email, SMS, notificación en app).		  
5. 5. Se envía la notificación.
  
 ### Información para los pasos:
- Sucede un evento relevante		
- Sucede un evento relevante		
- Información del mensaje		
- Información de contacto		
- Mensaje de notificación 

### Precondiciones:
- Existen eventos configurados para generar notificaciones.				 

### Poscondiciones:
- El destinatario recibe la notificación.				  

### Suposiciones:
- Los datos de contacto son correctos.				  

### Reunir requerimientos:
- Configuración de plantillas de mensajes.				 

### Aspectos sobresalientes:
- ¿Qué pasa si el envío falla? ¿Hay reintentos?				  

### Prioridad:
Media  

### Riesgo:
Bajo

![ESC 5](https://github.com/user-attachments/assets/2e47107c-ea51-4bd7-b52c-86d9d2c2f6c6)

* [Enviar notificación: Correcto funcionamiento del sistema de notificación](https://drive.google.com/file/d/1xeJTyQlezZ6TF5h6CVGzmhROVfFpB-zB/view?usp=sharing)
