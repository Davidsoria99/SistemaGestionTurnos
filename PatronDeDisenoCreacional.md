# Anexo - Aplicación de Patrón de Diseño estructural - Singleton
En este sistema de gestión de turnos, hay recursos que deben ser únicos a lo largo de toda la aplicación, como la conexión a una base de datos o un gestor de configuraciones. Si múltiples partes de la aplicación intentan conectarse o gestionar estos recursos de forma independiente, podría tener problemas de consistencia o sobrecarga de recursos. Por ejemplo, el `RepositorioTurnos` o el `RepositorioUsuario` necesitan una conexión a la base de datos. Crear múltiples conexiones por cada acceso puede causar problemas.

- El patrón `Singleton` asegura que una clase tenga una única instancia y proporciona un punto de acceso global a ella.

Es ideal para controlar el acceso a recursos compartidos o servicios centrales que no deberían tener múltiples instancias. En este caso, una única instancia de una clase que gestione la conexión a la base de datos o que actúe como un "Gestor de Configuraciones" es fundamental para la eficiencia y la coherencia.
