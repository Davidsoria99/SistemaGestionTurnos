# Anexo - Aplicación de Patrón de Diseño de Comportamiento - Strategy

## Propósito y Tipo del Patrón:

- El patrón `Strategy` permite definir una familia de algoritmos intercambiables, encapsulando cada uno en una clase separada. Esto desacopla el algoritmo de la clase que lo utiliza.

- Su relación los principios SOLID:

  SRP: Cada clase de estrategia concreta tiene una única responsabilidad: implementar un algoritmo específico.
  
  OCP: Promueve el OCP. Permite añadir nuevas estrategias (nuevos algoritmos) sin modificar la clase que los utiliza. El sistema está abierto a extensión pero cerrado a modificación.
  
  LSP: Lo apoya directamente. Todas las estrategias concretas implementan la misma interfaz de estrategia, lo que significa que cualquier estrategia concreta puede ser sustituida por otra sin afectar la funcionalidad del cliente.
  
  DIP: Facilita el DIP. La clase depende de una abstracción y no de las implementaciones concretas de los algoritmos. Esto reduce el acoplamiento y aumenta la flexibilidad.
  
  ISP: Es neutral. Si la interfaz de la estrategia es pequeña y cohesiva, el ISP se mantiene. El patrón no fuerza a los clientes a depender de métodos que no necesitan.

## Motivación:
El sistema de gestión de turnos necesita de diferentes algoritmos o reglas para la asignación de turnos a los médicos. Por ejemplo, la asignación podría ser:
* Por Disponibilidad: El primer horario disponible que cumpla los criterios.
* Por Menor Carga: Asignar al médico con menos turnos agendados en el día.
Si estos algoritmos están codificados directamente en la lógica del ServicioGestionTurnos, cada cambio o adición de una nueva regla requeriría modificar esa clase, violando el principio OCP.

Este patrón permite cambiar el algoritmo de asignación de turnos en tiempo de ejecución o de forma sencilla, sin modificar la clase principal. Se pueden añadir nuevas estrategias de asignación sin afectar las existentes.

## Estructura de Clases:

- Permite intercambiar algoritmo de asignación de turnos.
  
![Strategy](https://github.com/user-attachments/assets/33e51ff0-bdc6-4ea7-a2dd-bf5ffd91a8d2)
