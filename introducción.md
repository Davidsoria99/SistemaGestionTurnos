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
**Ejemplo**: Un turno en un hospital representa solo la información necesaria (fecha, hora, paciente), sin detalles internos.

### 2. Encapsulamiento
**Ejemplo**: Un cajero automático solo muestra una interfaz al usuario, pero oculta cómo maneja internamente las transacciones.

### 3. Herencia
**Ejemplo**: Una clase `Empleado` puede ser la base para `Médico`, `Enfermero`, etc., que heredan sus propiedades básicas.

### 4. Polimorfismo
**Ejemplo**: Un método `imprimirDatos()` puede actuar diferente según se aplique a un `Paciente` o a un `Turno`.

---

## Requisitos funcionales

1. El sistema debe permitir registrar pacientes.
2. El sistema debe permitir agendar turnos.
3. El sistema debe listar turnos agendados por fecha.
4. El sistema debe cancelar un turno previamente registrado.
5. El sistema debe enviar notificaciones por correo electrónico.

---

## Casos de uso

---

### 📘 Caso de uso 1: Registrar paciente

- **Actor(es) involucrado(s)**: Recepcionista
- **Descripción breve**: El recepcionista carga los datos de un nuevo paciente en el sistema.
- **Flujo principal de eventos**:
  1. Inicia sesión en el sistema.
  2. Selecciona la opción “Registrar paciente”.
  3. Completa los datos requeridos (nombre, DNI, contacto, etc.).
  4. Guarda el registro.
- **Precondiciones**: El usuario debe estar autenticado.
- **Postcondiciones**: El paciente queda almacenado en la base de datos.

---

### 📘 Caso de uso 2: Agendar turno

- **Actor(es) involucrado(s)**: Recepcionista, Paciente
- **Descripción breve**: Permite asignar un turno entre un paciente y un profesional.
- **Flujo principal de eventos**:
  1. El usuario selecciona un paciente registrado.
  2. Elige un profesional y un horario disponible.
  3. Confirma la asignación del turno.
- **Precondiciones**: El paciente debe existir en el sistema.
- **Postcondiciones**: El turno queda registrado y vinculado al paciente y profesional.

---

### 📘 Caso de uso 3: Consultar turnos

- **Actor(es) involucrado(s)**: Recepcionista
- **Descripción breve**: El sistema muestra los turnos agendados en una fecha específica.
- **Flujo principal de eventos**:
  1. Selecciona la fecha en el calendario.
  2. El sistema lista todos los turnos programados para ese día.
- **Precondiciones**: El sistema debe contener al menos un turno agendado.
- **Postcondiciones**: Se muestra la información solicitada.

---

### 📘 Caso de uso 4: Cancelar turno

- **Actor(es) involucrado(s)**: Paciente, Recepcionista
- **Descripción breve**: Se elimina un turno previamente asignado.
- **Flujo principal de eventos**:
  1. Se busca el turno por paciente o fecha.
  2. Se selecciona y se confirma la cancelación.
- **Precondiciones**: El turno debe estar registrado.
- **Postcondiciones**: El turno se elimina del sistema.

---

### 📘 Caso de uso 5: Enviar notificación por email

- **Actor(es) involucrado(s)**: Sistema
- **Descripción breve**: El sistema envía una notificación automática cuando se agenda o cancela un turno.
- **Flujo principal de eventos**:
  1. Se agenda o cancela un turno.
  2. El sistema detecta el evento.
  3. Genera y envía un correo al paciente.
- **Precondiciones**: El paciente debe tener un email registrado.
- **Postcondiciones**: El paciente recibe la notificación correspondiente.
  
---

## Boceto inicial del diseño de clases

![Boceto inicial del diseño de clases](https://github.com/user-attachments/assets/59c3fd4e-bbbe-4435-a837-3fa483259885)
.png)

🔗 [Ver diseño en línea](https://excalidraw.com/)
