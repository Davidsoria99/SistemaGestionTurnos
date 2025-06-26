# Anexo - Aplicación de Patrón de Diseño estructural - Singleton

## Propósito y Tipo del Patrón:

- El patrón `Singleton` es un patrón de diseño creacional que tiene como propósito garantizar que una clase tenga solo una instancia y proporcionar un punto de acceso global a esa instancia. En otras palabras, restringe la instanciación de una clase a un solo objeto.

## Motivación:
  
En este sistema de gestión de turnos, hay recursos que deben ser únicos a lo largo de toda la aplicación, como la conexión a una base de datos o un gestor de configuraciones. Si múltiples partes de la aplicación intentan conectarse o gestionar estos recursos de forma independiente, podría tener problemas de consistencia o sobrecarga de recursos. Por ejemplo, el `RepositorioTurnos` o el `RepositorioUsuario` necesitan una conexión a la base de datos. Crear múltiples conexiones por cada acceso puede causar problemas.

Es ideal para controlar el acceso a recursos compartidos o servicios centrales que no deberían tener múltiples instancias. En este caso, una única instancia de una clase que gestione la conexión a la base de datos o que actúe como un "Gestor de Configuraciones" es fundamental para la eficiencia y la coherencia.

## Estructura de Clases


