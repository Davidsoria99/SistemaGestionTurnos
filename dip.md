# Principio de Inversión de Dependencias (DIP)
Propósito y Tipo del Principio SOLID: Establece que los módulos de alto nivel no deben depender de módulos de bajo nivel, sino que ambos deben depender de abstracciones. Además, las abstracciones no deben depender de los detalles, sino que los detalles deben depender de las abstracciones.

En el contexto del sistema, el principio DIP permite desacoplar componentes clave del sistema —como el envío de notificaciones o la asignación de turnos— de sus implementaciones específicas. Esto facilita el mantenimiento, mejora la escalabilidad y permite reemplazar o modificar partes del sistema sin afectar a toda la aplicación.

---

## Motivación
Originalmente en el sistema de gestión de turnos los módulos de alto nivel estaban directamente acoplados a implementaciones específicas. Por ejemplo, el módulo que asigna turnos llamaba directamente a métodos de una clase **notificadorEmail** o **notificadorSMS**. Esto generaba varios problemas: si se quería cambiar la forma de notificar (por ejemplo, agregar notificaciones por apps de mensajeria), había que modificar también el módulo de asignación de turnos. Esto complicaba el mantenimiento y las pruebas.

Aplicando el principio de Inversión de Dependencias, creamos una interfaz general llamada **INotificador**. Los módulos de alto nivel, como **Notificador**, solo dependen de esta interfaz, sin saber ni importar cómo se implementa el envío del mensaje. Así, se puede cambiar o extender el tipo de notificación sin afectar la lógica principal del sistema.

---

**Ejemplo del mundo real**: En este sistema, una funcionalidad clave es la de notificar a los pacientes sobre la confirmación de sus turnos, los recordatorios o las cancelaciones.


Si el sistema dependiera directamente de implementaciones de bajo nivel como 'NotificadorEmail', crearía un fuerte acoplamiento, forzando modificaciones en Sistema si el método de notificación cambiara, por ejemplo, al pasar a WhatsApp o SMS.
Para evitar este problema, se aplicaria el **DIP**. Definiendo una abstracción: la interfaz 'INotificador'. Esta interfaz ayudaria para cualquier tipo de envío de notificación.
Así, la clase 'Notificador', solo interactúa con la interfaz 'INotificador', sin preocuparse por los detalles específicos del canal de envío. Esto permite intercambiar entre 'NotificadorEmail', 'NotificadorSMS' o 'NotificadorWhatsapp' sin modificar la lógica central del Sistema o de Notificador. Simplemente modificaria la implementación deseada. Este enfoque garantiza un diseño flexible, ya que los cambios en los detalles de comunicación no afectan la lógica de negocio principal del sistema.

---

## Estructura de Clases
![DIP](https://github.com/user-attachments/assets/fdd198b0-51de-451b-a253-1c3f785f7cd5)
* [Principio de Inversión de Dependencias (DIP)](https://drive.google.com/file/d/1Fq2h0u69KMExmMZev9LNLkRadwxSAmml/view?usp=sharing)
