## Registrar paciente: Registro exitoso de nuevo paciente

- **Nombre del caso de uso:** Registro exitoso de nuevo paciente  
- **ID Única:** 001  
- **Área:** Administración 
- **Actor(es):** Personal administrativo, Paciente  
- **Descripción:** Permite al personal administrativo  y al paciente registrar/se en el sistema, incluyendo datos personales y de contacto.  
- **Activar Evento:** El personal administrativo accede al módulo de pacientes y selecciona “Registrar nuevo”.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados (ruta principal):
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

* [Registrar paciente Registro exitoso de nuevo paciente](https://drive.google.com/file/d/1n-REjpnBQGjxBw0wlTqkmhAAZClYWyFV/view?usp=sharing)
---
## Agendar turnos: Turno agendado exitosamente

- **Nombre del caso de uso:** Agendar turnos  
- **ID Única:** 002  
- **Área:** Administración  
- **Actor(es):** Personal administrativo, Paciente  
- **Descripción:** El personal administrativo o el paciente agenda un nuevo turno para una consulta médica, eligiendo fecha, hora, médico y motivo.  
- **Activar Evento:** El usuario accede al módulo de turnos y selecciona “Mis turnos”.  
- **Tipo de señal:** Externa.  

### Pasos desempeñados (ruta principal):
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

### Pasos desempeñados (ruta principal):
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

* [Consultar turnos: Correcta consulta de turnos](https://drive.google.com/file/d/1vtU10rtQjH3yAkoneho9cRf5hPVfbuuB/view?usp=sharing)
---
