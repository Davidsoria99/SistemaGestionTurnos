# Principio de Abierto/Cerrado (OCP)
Proposito y Tipo del Principio SOLID: Este establece que una clase debe estar abierta para su extensión pero cerrada para su modificación. Es decir, se debe poder agregar nuevas funcionalidades sin modificar el código ya existente.

En el sistema de gestión de turnos, este principio permite agregar nuevos tipos de notificaciones (por ejemplo, por WhatsApp), validar nuevas reglas de disponibilidad médica, o cambiar el formato del historial de turnos, sin tener que modificar directamente las clases que ya funcionan correctamente.

Al aplicar OCP:
- Se reduce el riesgo de introducir errores al modificar código probado.
- Se facilita el crecimiento del sistema sin romper lo anterior.
- Se promueve el uso de interfaces y clases abstractas para definir comportamientos que luego pueden extenderse con nuevas implementaciones.

Este enfoque es ideal en un entorno como el del centro de salud, que puede ir incorporando mejoras al sistema sin reescribir funcionalidades ya implementadas.

---

## Motivación
Antes de aplicar este principio, el sistema de gestión de turnos presentaba un diseño rígido: cada vez que se necesitaba agregar una nueva forma de notificar al paciente (por ejemplo, pasar de solo email a también SMS), era necesario modificar directamente la clase que manejaba las notificaciones. Esto hacía que los cambios fuesen riesgosos, propensos a errores, y requerían mucho tiempo de prueba y ajuste.

Ejemplo del mundo real: 
Inicialmente el sistema solo enviaba confirmaciones por correo electrónico.

Cuando el centro de salud pidió agregar notificaciones por apps de mensajeria, se tuvo que modificar la clase Notificador, lo que causó que ciertas notificaciones dejaran de funcionar o se enviaran de manera incorrecta. Ese error afectó a varios pacientes que no recibieron su confirmación de turno.

Gracias a la implementación de este principio, el sistema puede tener una interfaz como *INotificador*, y distintas implementaciones (NotificadorEmail, NotificadorSMS, NotificadorWhatsApp, etc.). Si se quiere agregar una nueva vía de comunicación, solo se crea una nueva clase que implemente la interfaz, sin tocar las clases existentes. Esto evita romper funcionalidades que ya funcionan bien y permite crecer el sistema de forma controlada y segura.

---

## Estructura de Clases
![OCP](https://github.com/user-attachments/assets/141a6b00-1f60-4a21-8d9c-d7ec40177209)
* [Principio de Abierto/Cerrado (OCP)](https://drive.google.com/file/d/1hGglA7Rqw3hrvE2vyh7IpR8Cb6cGiar1/view?usp=sharing)
