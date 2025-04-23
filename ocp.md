# Principio de Abierto/Cerrado (OCP)
El Principio de Abierto/Cerrado (OCP) establece que una clase debe estar abierta para su extensión pero cerrada para su modificación. Es decir, se debe poder agregar nuevas funcionalidades sin modificar el código ya existente.

En el sistema de gestión de turnos médicos, este principio permite agregar nuevos tipos de notificaciones (por ejemplo, por WhatsApp), validar nuevas reglas de disponibilidad médica, o cambiar el formato del historial de turnos, sin tener que modificar directamente las clases que ya funcionan correctamente.
