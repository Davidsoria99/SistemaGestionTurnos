# Introducción

## ¿Qué es la programación orientada a objetos?

La programación orientada a objetos (POO) es un paradigma de programación que se basa en la abstracción de datos y comportamiento dentro de "objetos". Estos objetos son instancias de clases que agrupan atributos (estado) y métodos (comportamiento).

POO es importante porque permite:
- Reutilizar código
- Facilitar el mantenimiento
- Promover el diseño modular
- Reflejar de forma más natural el mundo real

---

## Los cuatro fundamentos de la POO

### 1. Abstracción
**Ejemplo**: Un "Turno" en un hospital representa solo la información necesaria (fecha, hora, paciente), sin detalles internos.

### 2. Encapsulamiento
**Ejemplo**: Un cajero automático expone una interfaz al usuario, pero oculta cómo maneja internamente las transacciones.

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

### Caso de uso 1: Registrar paciente
- **Actor(es)**: Recepcionista
- **Descripción**: El recepcionista registra los datos de un nuevo paciente.
- **Flujo principal**:
  1. El recepcionista ingresa al sistema.
  2. Accede a la opción “Registrar paciente”.
  3. Completa el formulario con los datos requeridos.
  4. Confirma el registro.
- **Precondiciones**: El usuario debe estar autenticado.
- **Postcondiciones**: El paciente queda registrado en la base de datos.

(Si querés, después te ayudo a completar los otros 4 casos de uso)

---

## Boceto inicial del diseño de clases

![Diseño de clases](diseño_clases.png)

🔗 [Ver diseño en línea](https://excalidraw.com/)
