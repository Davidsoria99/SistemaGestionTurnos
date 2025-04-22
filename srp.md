# Principio de Responsabilidad Única (SRP)
Proposito y Tipo del Principio SOLID: Este principio establece que una clase debe tener una única razón para cambiar, es decir, debe encargarse de una única responsabilidad dentro del sistema.

En el caso del sistema de gestión de turnos, este principio permite separar claramente las funcionalidades: registrar pacientes, asignar turnos, enviar notificaciones, o gestionar historiales, en clases independientes. Esto evita que una sola clase controle múltiples procesos a la vez, lo cual genera acoplamiento innecesario, errores frecuentes y un diseño difícil de mantener.

Al aplicar este principio:
- El código es más claro y más fácil de testear.
- Cada clase se enfoca en hacer bien una sola cosa.
- El mantenimiento del sistema se vuelve más sencillo y menos propenso a errores.
---
## Motivación

