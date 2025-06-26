# Anexo - Aplicación de Patrón de Diseño estructural - Adapter

## Propósito y Tipo del Patrón:
- El patrón `Adapter` facilita que componentes con interfaces incompatibles colaboren, envolviendo una interfaz existente para que se ajuste a lo que el cliente espera.
  
- Este patrón generalmente armoniza bien con los principios SOLID:

  SRP: El Adaptador tiene una única y clara responsabilidad: la de adaptar una interfaz a otra.
  
  OCP: Promueve el OCP porque se pueden añadir nuevos adaptadores para soportar servicios incompatibles sin necesidad de modificar el código del cliente existente. El cliente permanece "cerrado" a modificaciones.
  
  LSP: Lo apoya, ya que el Adaptador implementa una interfaz, lo que significa que un objeto Adaptador puede sustituir a cualquier otro objeto que implemente esa misma interfaz sin alterar la lógica del cliente.
  
  DIP: Facilita el DIP, dado que el cliente depende de una abstracción y no de los detalles concretos del servicio original.
  
  ISP: Eñ patrón Adapter es compatible con eeste y puede ser una herramienta valiosa para lograr una mejor segregación de interfaces al permitir que los clientes interactúen con interfaces más pequeñas y relevantes.

## Motivación:
El sistema de gestión de turnos envia notificaciones (por ejemplo, confirmaciones de turno, recordatorios, cancelaciones) a pacientes y médicos. Probablemente en una versión más avanzada del sistema se requieran diferentes canales de notificación (email, SMS, WhatsApp). Si el código actual está acoplado a un servicio de email específico, cambiar o añadir un nuevo canal implicaría modificar muchas partes del sistema.
Este patrón me permite integrar sistemas de notificación externos que tienen diferentes APIs (interfaces) sin modificar el código cliente (el `ServicioNotificacion` del sistema). 
Se puede crear un adaptador para cada servicio de notificación externo, y el `ServicioNotificacion` interactuará con una interfaz unificada.

## Estructura de Clases:
- Permite que ServicioNotificacion interactúe con ServicioEmailExistente a través de una interfaz común.
![Adapter](https://github.com/user-attachments/assets/406f0bfd-e951-4a9a-8cd6-65e76a35d60a)
