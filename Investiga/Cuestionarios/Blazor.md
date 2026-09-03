# Cuestionario: Marco de Trabajo Blazor

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---

## Sección A — Conocimientos generales
1. ¿Qué es Blazor y quién lo desarrolló?
   
Blazor es una herramienta que nos permite crear páginas web interactivas usando C# en vez de usar principalmente JavaScript. Lo creó la empresa Microsoft.

3. ¿Qué lenguaje de programación utiliza Blazor para crear interfaces web?
   
Usa C# junto con una sintaxis que mezcla código con HTML, que se llama Razor. Así no necesitamos aprender otro lenguaje distinto para la parte visual.

5. ¿Qué significa que Blazor permite crear aplicaciones web con C# en lugar de JavaScript?
   
Significa que todo lo que normalmente se haría con JavaScript —como validar formularios o cambiar cosas en la página sin recargarla— lo podemos hacer directamente con C#. Así usamos el mismo lenguaje en el programa y en la página web.

7. ¿Cuál es la diferencia entre Blazor Server y Blazor WebAssembly?


* Blazor Server: el programa corre en el servidor, y el navegador solo recibe los cambios. Es rápido al iniciar pero necesita internet todo el tiempo.

* Blazor WebAssembly: el código se descarga al navegador y ahí se ejecuta. Puede funcionar incluso sin internet después de cargar.

5. ¿Qué es un componente en Blazor?
   
Es como una pieza o parte de la página: un botón, un formulario, una tarjeta. Cada uno está en su propio archivo y se puede reutilizar en varias páginas sin volver a escribir todo.

## Sección B — Conceptos fundamentales

6. ¿Qué extensión de archivo tienen los componentes de Blazor?
Los componentes se guardan con la extensión .razor.

7. ¿Qué son los parámetros de componente ([Parameter]) en Blazor? Da un ejemplo.
Son valores que le podemos mandar a un componente desde otro para que cambie su información o su comportamiento sin tener que escribirlo de nuevo. Por ejemplo, si tenemos un componente de tarjeta, le podemos mandar un título distinto cada vez que lo usamos.

8. ¿Qué es el data binding (enlace de datos) en Blazor? Explica la diferencia entre one-way binding y two-way binding.
Es la conexión automática entre lo que tenemos en el código y lo que se ve en la pantalla.

* One-way binding (unidireccional): la información va en un solo sentido: del código a la vista. Si cambia en el programa, se actualiza en la pantalla, pero no al revés.

* Two-way binding (bidireccional): la información va y vuelve. Si escribes en un campo de texto, se actualiza la variable en el código; y si cambias la variable desde el programa, se actualiza lo que se muestra en pantalla.

9. ¿Qué directiva usarías para enlazar dinámicamente el valor de un campo de texto con una variable? Escribe un ejemplo.
Usamos el enlace bidireccional con @bind-value. Por ejemplo:
Si tengo un cuadro de texto conectado a una variable llamada NombreUsuario, todo lo que se escriba en el cuadro se guarda automáticamente en esa variable, y si la variable cambia desde el código, se actualiza lo que se muestra en el cuadro.


## Sección C — Uso práctica

11. ¿Qué es @page en Blazor y para qué sirve?
Es una instrucción que le dice al programa en qué dirección o en qué enlace del navegador debe aparecer esa página. Por ejemplo, si ponemos @page "/inicio", cuando alguien visite esa dirección se mostrará ese contenido. Sirve para que cada componente funcione como una página distinta dentro de la aplicación.

12. ¿Cómo se navega entre páginas en una aplicación Blazor?
Se puede hacer de dos formas: con un enlace normal como en cualquier página web, o usando código para cambiar de página desde el programa. En el código se usa una herramienta que ya trae Blazor llamada NavigationManager y se le indica a qué dirección ir.

13. ¿Qué es la inyección de dependencias y cómo se usa en Blazor?
Es una forma de organizar el código para no repetir lo mismo en muchos lugares. Creamos una herramienta o servicio una sola vez y luego lo "pedimos" donde lo necesitemos, en lugar de crearlo cada vez. En Blazor se usa junto con @inject para traer el servicio y poder usarlo en ese componente.

14. ¿Cómo se consumen servicios o APIs REST desde una aplicación Blazor?
Se usa algo que ya viene integrado llamado HttpClient, que sirve para pedir o enviar información por internet. Con él podemos conectarnos a una dirección web y recibir datos, por ejemplo, una lista de productos o información de usuarios, y luego mostrarla en la página.

15. ¿Qué es @inject y cómo funciona?
Es la instrucción que usamos para pedirle a Blazor que nos entregue un servicio que ya está preparado. En lugar de escribir new Servicio() para crearlo nosotros mismos, simplemente lo pedimos con @inject y el sistema nos lo da listo para usar. Así todo queda más ordenado y es más fácil de cambiar después.

## Sección D — Comparación y contexto

16. ¿Qué ventajas ves en Blazor frente a frameworks como Angular, React o Vue?
La mayor ventaja es que si ya sabemos programar en C#, no necesitamos aprender JavaScript desde cero para hacer la parte visual de una página web. Todo se puede hacer con el mismo lenguaje que ya usamos en la parte del servidor. También se conecta muy fácil con otros programas de Microsoft y se puede reutilizar lo aprendido para hacer aplicaciones de celular y computadora con MAUI.

17. ¿Blazor reemplaza completamente a JavaScript? Justifica tu respuesta.
No, no lo reemplaza del todo. Aunque podemos hacer casi toda la página con C#, todavía hay cosas que se hacen mejor o que solo se pueden hacer con JavaScript, como usar algunas bibliotecas que ya existen o acceder a funciones muy específicas del navegador. Lo que sí hace es que escribamos mucho menos JavaScript del que escribiríamos con otros frameworks.

18. ¿En qué tipo de proyecto considerarías que Blazor es una buena opción?
Sería ideal para sistemas de gestión, como control de inventario, facturación, registro de notas escolares o cualquier programa que se conecte a una base de datos. También es muy útil cuando el equipo ya conoce C# y no quiere invertir mucho tiempo aprendiendo otro lenguaje nuevo solo para la parte visual.

19. ¿Qué es MAUI Blazor y cómo se relaciona con Blazor?
Es una forma de usar lo que ya sabemos hacer en Blazor —las páginas y los diseños— pero en lugar de que se vean solo en un navegador, se convierten en aplicaciones que se instalan en celulares, tabletas o computadoras. Así aprovechamos el mismo conocimiento para crear también apps móviles y de escritorio, sin tener que aprender a programar aparte para cada dispositivo.

20. ¿Has creado algún proyecto o ejemplo con Blazor? Si es así, descríbelo brevemente.
(Puedes completarlo con lo que tú hayas hecho, por ejemplo:)
He hecho una página sencilla donde se pueden agregar tareas, marcarlas como terminadas y borrarlas. Aprendí a separar las partes en componentes y a conectar los datos con lo que se ve en pantalla.

## Sección E — Pregunta reflexiva

21. ¿Crees que el ecosistema de Blazor tiene futuro para el desarrollo web profesional? ¿Por qué?
    
Sí, creo que sí tiene mucho futuro, porque cada vez más empresas usan C# y .NET en sus sistemas. Con Blazor pueden tener todo el proyecto —la parte visual y la parte de procesamiento— en un solo lenguaje, lo que ahorra tiempo y facilita mantener todo funcionando bien. Aunque todavía no es tan usado como otros frameworks, va creciendo y mejorando, y como se conecta también con el desarrollo de aplicaciones móviles, se vuelve más útil para los programadores que ya trabajan con estas herramientas.
