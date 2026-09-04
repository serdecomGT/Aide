# Cliente _ servidores

El modelo cliente-servidor es una arquitectura de red que divide las tareas entre un programa o dispositivo que solicita un servicio (el cliente) y otro que lo proporciona (el servidor).Se usa para organizar la comunicación y el intercambio de información en una red de computadoras, permitiendo que múltiples usuarios accedan a datos, programas y recursos centralizados de forma ordenada y segura.¿Cómo funciona?El Cliente: Es el dispositivo o aplicación (como tu navegador web, una app en el celular o un programa de correo) que usa el usuario y envía una petición (request).El Servidor: Es una máquina o programa potente que recibe esa petición, la procesa, busca la información o realiza los cálculos necesarios y devuelve una respuesta al cliente.Ejemplos de uso cotidianoPáginas web: Tu navegador es el cliente que pide ver un sitio; el servidor web almacena las páginas y se las envía para que las veas. Correo electrónico: Lees tus mensajes en una app (cliente) conectado a un servidor de correo que guarda todos tus mensajes. Bases de datos y aplicaciones de empresas: Muchos empleados usan sus computadoras para consultar o guardar datos que se guardan en un único servidor central de la compañía. ( P2P )

## ¿Qué es la arquitectura cliente-servidor?

La arquitectura cliente-servidor es una forma de organizar programas que se conectan por una red. En lugar de que todo el programa funcione en una sola computadora, se divide en dos partes que se comunican entre sí: el cliente, que es lo que ve y usa el usuario, y el servidor, que es quien guarda los datos y procesa la información.

Esta arquitectura es la base de internet: cada vez que abres una página web, tu celular o computadora actúa como cliente y solicita información a un servidor que puede estar en cualquier parte del mundo.

**El Cliente**

El cliente es la interfaz visible de la aplicación. Es la ventana, la página web o la pantalla del celular donde aparecen los botones, los formularios, los menús y los resultados. Su trabajo es:

* Mostrar la información de forma clara y ordenada.

* Recibir lo que el usuario escribe o selecciona.

* Enviar esa información al servidor y esperar la respuesta.

* Mostrar el resultado que el servidor devolvió.

El cliente no guarda la información de forma permanente. Si cierras la aplicación y la vuelves a abrir, todo se vuelve a cargar desde el servidor. Esto es bueno porque puedes entrar desde cualquier dispositivo y ver tus mismos datos.

***El Servidor***

El servidor es el programa que recibe las peticiones del cliente, las procesa y responde. Generalmente está instalado en una computadora más potente que está encendida las 24 horas, para que cualquiera pueda conectarse en cualquier momento. Su trabajo es:

* Recibir los datos que envía el cliente.

* Validar que la información sea correcta y que el usuario tenga permiso.

* Consultar o guardar información en la base de datos.

* Hacer cálculos o procesos que requieran seguridad o lógica compleja.

* Enviar la respuesta de vuelta al cliente.

Un servidor puede atender a muchos clientes al mismo tiempo. Por ejemplo, en una red social, miles de personas publican y leen al mismo tiempo, y el servidor se encarga de organizar todo.

**¿Cómo se comunican?**

Para entenderse, cliente y servidor usan protocolos, que son como reglas de conversación. Los más comunes son:

* HTTP/HTTPS: el mismo que se usa en los navegadores web. Es simple y funciona desde cualquier lugar.

* WebSocket: permite una comunicación en tiempo real, ideal para chats o notificaciones instantáneas.

**El flujo de información suele ser así:**

1. El usuario llena un formulario y da clic en "Guardar".

2. El cliente envía los datos al servidor.

3. El servidor revisa que todo esté bien y lo guarda en la base de datos.

4. El servidor responde: "se guardó correctamente" o "hubo un error".

5. El cliente muestra el mensaje al usuario.

**Ventajas de esta arquitectura**

* Centralización: la información se guarda en un solo lugar, lo que facilita hacer copias de seguridad y mantenerla segura.

* Accesibilidad: puedes entrar desde casa, la escuela o el trabajo y siempre verás la misma información actualizada.

* Seguridad: los datos importantes no se quedan en el celular de nadie, sino protegidos en el servidor.

* Mantenimiento: si hay que actualizar algo, se cambia en el servidor y todos los usuarios lo ven al instante, sin tener que instalar nada.

* Escalabilidad: si aumenta la cantidad de usuarios, se puede mejorar el servidor sin tener que cambiar las computadoras de todos.

**Desventajas y retos**

* Depende de la red: si se va el internet, no se puede usar la aplicación.

* Costo del servidor: mantener una computadora encendida todo el tiempo y con conexión requiere recursos.

* Seguridad: al estar conectado a la red, hay que protegerse contra intentos de acceso no autorizados.

**Variantes de la arquitectura**

* Arquitectura de dos capas: la más simple, cliente se conecta directo al servidor y a la base de datos.
* Arquitectura en la nube: el servidor no está en tu escuela o casa, sino en empresas como Microsoft Azure o Amazon Web Services, que se encargan de mantenerlo funcionando.

## Ejemplo práctico

**Imagina un sistema de notas escolares:**

* Cliente: la página web donde el maestro escribe las calificaciones y donde el estudiante las consulta.

* Servidor: recibe la calificación que el maestro envió, verifica que tenga permiso para modificarla, la guarda y avisa que se registró.

* Base de datos: donde quedan guardadas todas las calificaciones para siempre.

