# Anexo - Aplicación de Patrón de Diseño estructural - Singleton

## Propósito y Tipo del Patrón:

- El patrón `Singleton` es un patrón de diseño creacional que tiene como propósito garantizar que una clase tenga solo una instancia y proporcionar un punto de acceso global a esa instancia. En otras palabras, restringe la instanciación de una clase a un solo objeto.
- Por esto suele tener ciertos conflictos con los principios SOLID, ya que al forzar una instancia única y un punto de acceso global, tiende a introducir rigidez en el diseño y acoplamiento fuerte.
especialmente:
SRP: La clase asume doble responsabilidad (lógica de negocio y control de instancia).

OCP: Dificulta la extensión sin modificación, ya que el cliente se acopla a una implementación concreta.

DIP: Rompe la inversión de dependencias al obligar a los clientes a depender de una clase concreta en lugar de una abstracción.

LSP e ISP: no tienen relación con Singleton, debido a que su aplicación depende más del diseño general de las interfaces y la herencia, no del patrón en sí.

## Motivación:
  
En este sistema de gestión de turnos, hay recursos que deben ser únicos a lo largo de toda la aplicación, como la conexión a una base de datos o un gestor de configuraciones. Si múltiples partes de la aplicación intentan conectarse o gestionar estos recursos de forma independiente, podría tener problemas de consistencia o sobrecarga de recursos. Por ejemplo, el `RepositorioTurnos` o el `RepositorioUsuario` necesitan una conexión a la base de datos. Crear múltiples conexiones por cada acceso puede causar problemas.

Es ideal para controlar el acceso a recursos compartidos o servicios centrales que no deberían tener múltiples instancias. En este caso, una única instancia de una clase que gestione la conexión a la base de datos o que actúe como un "Gestor de Configuraciones" es fundamental para la eficiencia y la coherencia.

## Estructura de Clases


