# Cuestionario: Arquitectura Cliente-Servidor

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---



## Sección A — Conceptos fundamentales

1. ¿Qué es la arquitectura cliente-servidor? Explica con tus propias palabras.
   
Es una forma de organizar programas donde hay dos partes: la que pide algo y la que lo entrega. El cliente es quien hace la petición, y el servidor es quien tiene la información o el servicio y se lo envía de vuelta. Por ejemplo, cuando entras a una página web, tu celular o computadora es el cliente y la máquina que tiene la página guardada es el servidor.

3. ¿Qué es un cliente en esta arquitectura? Da un ejemplo cotidiano.
   
Es el programa o dispositivo que usa la persona para pedir algo. Es quien "pide y recibe". Por ejemplo: el navegador de internet en tu celular cuando abres Facebook, o la app de WhatsApp en tu teléfono.

4. ¿Qué es un servidor en esta arquitectura? Da un ejemplo cotidiano.
   
Es la máquina o programa que está esperando las peticiones y tiene la información o los recursos. Por ejemplo: la máquina donde están guardadas todas las publicaciones y fotos de Facebook, que te las envía cuando entras a la app.

5. ¿Cuál es la diferencia entre un cliente y un servidor?
   
El cliente es el que pide y recibe la información; el servidor es el que la tiene y la entrega. El cliente es lo que usa la persona, y el servidor trabaja "detrás de escena" respondiendo las peticiones de muchos clientes a la vez.

6. Describe el flujo de comunicación entre un cliente y un servidor cuando visitas una página web.
   
Primero escribes la dirección en el navegador (el cliente). El cliente envía una petición por internet diciendo "quiero ver esta página". El servidor recibe la petición, busca los archivos de la página y los envía de vuelta. El navegador recibe todo y lo arma para que tú lo veas en pantalla.
Sección B — Protocolos y comunicación

7. ¿Qué es el protocolo HTTP y qué función cumple en la arquitectura cliente-servidor?
   
Es el conjunto de reglas que se usan para que cliente y servidor se entiendan. Es como el "idioma" en el que se hablan. Define cómo se pide la información y cómo se envía de vuelta, para que ambos se entiendan sin confusiones.

8. ¿Cuál es la diferencia entre HTTP y HTTPS?
   
La diferencia es la seguridad. En HTTP la información viaja "al descubierto" y cualquiera podría leerla. En HTTPS la información se cifra o se vuelve ilegible mientras viaja, así nadie más la puede ver. Por eso las páginas que piden contraseñas o datos bancarios usan HTTPS.

9. ¿Qué son los métodos HTTP GET, POST, PUT y DELETE? Explica cuándo se usa cada uno.

* GET: es para pedir información. Por ejemplo, cuando abres una página o buscas algo.

* POST: es para enviar información nueva que se va a guardar. Por ejemplo, cuando llenas un formulario o creas una cuenta.

* PUT: es para cambiar o actualizar algo que ya existe. Por ejemplo, cuando editas tu perfil y cambias tu contraseña.

* DELETE: es para borrar algo. Por ejemplo, cuando eliminas una publicación o un mensaje.

9. ¿Qué es una API REST y cómo se relaciona con la arquitectura cliente-servidor?
    
Es una forma ordenada de comunicarse entre cliente y servidor. El servidor ofrece "puntos de entrada" donde el cliente puede pedir, enviar, cambiar o borrar información usando reglas sencillas y el protocolo HTTP. Así el cliente y el servidor pueden ser programas distintos hechos en lenguajes distintos y aun así funcionan juntos.

11. ¿Qué es un código de estado HTTP? Menciona el significado de 200, 404 y 500.
    
Son números que el servidor devuelve para decir cómo le fue a la petición:

* 200 = Todo salió bien, la información se envió correctamente.

* 404 = No se encontró lo que se pidió; la página o el archivo no existe.

* 500 = Hubo un error dentro del servidor; algo salió mal en el programa de allá.
  
## Sección C — Componentes y tipos

11. ¿Qué es un puerto de red y por qué es importante? Menciona los puertos comunes para HTTP y HTTPS.
Es como una "puerta" o número de entrada en la máquina del servidor. Sirve para saber a qué programa enviar la información. Por ejemplo, el servidor puede tener un programa para páginas web y otro para correos; los puertos sirven para distinguirlos.

* HTTP: usa el puerto 80.

* HTTPS: usa el puerto 443.

12. ¿Cuál es la diferencia entre arquitectura de dos capas y de tres capas (3-tier)?

* Dos capas: solo hay cliente y servidor. Todo lo que se ve y todo lo que se procesa está entre esos dos. Es más sencillo pero menos flexible.

* Tres capas: se separa en tres partes: lo que ve el usuario, la lógica del programa y la base de datos. Así se puede cambiar una parte sin dañar las otras y es más fácil de mantener.

13. ¿Qué es la capa de presentación, la capa lógica (de negocio) y la capa de datos?

* Capa de presentación: es lo que ve y toca el usuario: botones, menús, páginas.

* Capa lógica o de negocio: es donde se procesan las reglas y los cálculos: "si pasa esto, entonces hago aquello".

* Capa de datos: es donde se guarda todo: la base de datos con los usuarios, productos, registros, etc.

14. ¿Qué es un proxy y en qué situaciones se utiliza?
    
Es como un "intermediario" entre el cliente y el servidor. En lugar de conectarse directo, pasas por él. Sirve para bloquear páginas, guardar cosas que se usan mucho para que vaya más rápido, o para navegar sin que se sepa desde dónde te conectas.

16. ¿Qué diferencia hay entre un servidor web y un servidor de aplicaciones?

* Servidor web: se encarga de entregar archivos como páginas, imágenes y documentos. Es más básico.

* Servidor de aplicaciones: además de entregar archivos, puede ejecutar programas, hacer cálculos y trabajar con bases de datos. Tiene más "inteligencia" para procesar información.
  
## Sección D — Contexto práctico

16. En Blazor, ¿qué actúa como cliente y qué como servidor?
Depende del tipo:

* En Blazor Server, el servidor hace casi todo y el cliente solo muestra la página.

* En Blazor WebAssembly, el código se baja al navegador y ahí corre como cliente, y se conecta al servidor solo cuando necesita datos guardados.

17. ¿Qué es el hosting y cómo se relaciona con los servidores?
    
Es el servicio de alquilar un espacio en una máquina que está siempre encendida y conectada a internet. Ahí se guardan los archivos de la página o aplicación, así cualquier persona del mundo puede entrar cuando quiera. Sin hosting, nadie más podría ver tu trabajo.

19. ¿Qué es la latencia de red y cómo afecta la experiencia del usuario?
    
Es el tiempo que tarda la información en viajar desde tu dispositivo hasta el servidor y volver. Si la latencia es alta, todo se siente lento: al hacer clic tarda en responder, las páginas cargan despacio. Si es baja, todo se siente rápido y fluido.

20. ¿Qué es un endpoint? Da un ejemplo.
    
Es como una "dirección" o lugar específico en el servidor donde se puede pedir o enviar algo. Por ejemplo: www.mitienda.com/api/productos — ahí es donde el cliente pide la lista de productos.

21. ¿Qué es la escalabilidad y por qué es importante en un servidor?
    
Es la capacidad de ir creciendo o aumentando la fuerza del servidor cuando llegan más personas. Si de repente se conectan mil personas más, el servidor no debe colapsarse. Es importante para que la aplicación siga funcionando bien aunque tenga mucho uso.

## Sección E — Pregunta reflexiva

22. ¿Por qué crees que la arquitectura cliente-servidor es la más usada en Internet? ¿Conoces alguna alternativa?

Creo que se usa porque es muy práctica: se puede tener la información centralizada y todos acceden desde sus propios dispositivos. Además se puede actualizar todo en un solo lugar y todos ven la versión nueva. Una alternativa sería que cada dispositivo se conectara directo con otro sin un servidor en medio (llamado punto a punto), que se usa en cosas como compartir archivos, pero es más difícil de controlar y proteger.
¿Quieres que lo ajuste o lo dejamos así? 😊
