# Principio de Abierto/Cerrado (OCP)
Proposito y Tipo del Principio SOLID: Este establece que una clase debe estar abierta para su extensión pero cerrada para su modificación. Es decir, se debe poder agregar nuevas funcionalidades sin modificar el código ya existente.

En el sistema de gestión de turnos médicos, este principio permite agregar nuevos tipos de notificaciones (por ejemplo, por WhatsApp), validar nuevas reglas de disponibilidad médica, o cambiar el formato del historial de turnos, sin tener que modificar directamente las clases que ya funcionan correctamente.

Al aplicar OCP:
- Se reduce el riesgo de introducir errores al modificar código probado.
- Se facilita el crecimiento del sistema sin romper lo anterior.
- Se promueve el uso de interfaces y clases abstractas para definir comportamientos que luego pueden extenderse con nuevas implementaciones.

Este enfoque es ideal en un entorno como el del centro de salud, que puede ir incorporando mejoras al sistema sin reescribir funcionalidades ya implementadas.
