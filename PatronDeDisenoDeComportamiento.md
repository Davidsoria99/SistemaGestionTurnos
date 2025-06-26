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

## Estructura de Clases:
