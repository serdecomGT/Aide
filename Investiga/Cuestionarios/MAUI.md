# Cuestionario: Marco de Trabajo .NET MAUI

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---

## Sección A — Conocimientos generales

1. ¿Qué significa la sigla MAUI y qué es .NET MAUI?
   
Significa Multi-platform App UI, o sea "Interfaz de Aplicación Multiplataforma". Es una herramienta de Microsoft que permite hacer una sola aplicación que sirva para celulares, tabletas y computadoras con distintos sistemas operativos, todo usando el mismo código.

3. ¿Quién desarrolló .NET MAUI y en qué año se lanzó oficialmente?
   
Lo creó Microsoft y se lanzó oficialmente en mayo de 2022.

4. ¿De qué marco de trabajo anterior es MAUI el sucesor? ¿Por qué se creó MAUI como reemplazo?
   
Es el sucesor de Xamarin.Forms. Se creó para unificar todo en un solo lugar, mejorar el rendimiento, facilitar el trabajo y aprovechar las novedades más recientes de .NET.

5. ¿Qué plataformas o sistemas operativos permiten apuntar una aplicación desarrollada con MAUI?

* Android

* iOS (iPhone y iPad)

* Windows

* macOS (computadoras Apple)

5. ¿Qué lenguaje de programación se utiliza principalmente para desarrollar con .NET MAUI?
Se usa C#, junto con un lenguaje de marcado llamado XAML para diseñar las pantallas.

## Sección B — Arquitectura y estructura

7. ¿Qué es un proyecto .NET MAUI y cómo se estructura? Menciona las carpetas o archivos principales.
Es todo lo que necesitas para construir tu aplicación. Viene organizado con carpetas donde pones las imágenes, las fuentes, los estilos y las pantallas. Los archivos principales son: MauiProgram.cs, App.xaml junto con App.xaml.cs, y AppShell.xaml.

8. ¿Qué es el archivo MauiProgram.cs y qué función cumple?
   
Es como el "arranque" de la aplicación. Ahí se configuran los servicios que va a usar, se inicializan las herramientas y se prepara todo para que la app empiece a funcionar.

9. ¿Cuál es el archivo App.xaml / App.xaml.cs y cuál es su rol en la aplicación?
   
Aquí es donde se definen los estilos generales, los colores y las fuentes que van a usar todas las pantallas. También es el punto de partida donde se indica qué pantalla se va a mostrar primero.

10. ¿Qué es el archivo AppShell.xaml y para qué sirve?
Es como el "esqueleto" o estructura de navegación. Sirve para organizar los menús, las pestañas y cómo se mueve el usuario entre las distintas pantallas de la aplicación.

11. ¿Qué son las carpetas de plataformas específicas y qué contiene cada una?
    
Son carpetas donde se guarda el código que funciona solo en un sistema en particular: Android, iOS, Windows o macOS. Ahí puedes personalizar cosas que son distintas en cada dispositivo, como permisos o características especiales.
Sección C — Interfaz y componentes

12. ¿Qué es XAML y cómo se utiliza en .NET MAUI
    
Es un lenguaje que sirve para diseñar las pantallas. Con él puedes decir "aquí va un botón, aquí un cuadro de texto, aquí una imagen" sin tener que dibujar todo a mano. Se mezcla con C# para darle comportamiento a lo que se ve.

13. ¿Cuál es la diferencia entre escribir la interfaz en XAML y escribirla directamente en C#?

* XAML es más visual y ordenado: separas lo que se ve de lo que hace. Es más fácil de diseñar y de cambiar después.

* C# es más flexible: puedes crear todo desde el código y hacerlo cambiar según lo que pase en el programa.

13. Menciona al menos cinco controles disponibles en .NET MAUI.

* Label → para mostrar texto.

* Entry → para que el usuario escriba.

* Button → para hacer acciones al tocarlo.

* Image → para mostrar fotos o gráficos.

* CollectionView → para mostrar listas largas de cosas.

14. ¿Qué es un Layout en MAUI?
Menciona al menos tres tipos de diseño y explica cuándo usar cada uno.
Un Layout es cómo acomodas los elementos en la pantalla.

* VerticalStackLayout → pone todo uno debajo del otro; sirve para formularios.

* HorizontalStackLayout → pone todo uno al lado del otro; sirve para botones juntos.

* Grid → acomoda todo en filas y columnas; sirve para diseños más ordenados como tablas.

15. ¿Qué es el enlace de datos en MAUI? Escribe o describe un ejemplo sencillo.
    
Es conectar lo que se ve en la pantalla con los datos del programa. Por ejemplo: si tienes una variable con el nombre del usuario, la conectas con un texto en la pantalla y automáticamente se muestra ahí sin tener que escribirlo aparte.

17. ¿Qué es el patrón MVVM y por qué se recomienda usarlo en MAUI?
    
Significa Model-View-ViewModel. Es una forma de organizar el código para que lo que se ve (la pantalla) esté separado de lo que hace (la lógica). Así se puede cambiar el diseño sin dañar el funcionamiento y viceversa. Todo queda más ordenado y fácil de mantener.

## Sección D — Funcionalidades y servicios

18. ¿Qué es la inyección de dependencias y cómo se configura en MAUI?
    
Es una forma de organizar el código: creas un servicio una sola vez y lo "pides" donde lo necesites, en lugar de crearlo cada vez. En MAUI se configura en el archivo MauiProgram.cs, donde se registran los servicios para que estén disponibles en toda la app.

19. ¿Qué es el Shell Navigation y cómo se define una ruta de navegación entre páginas?

Es un sistema que ya trae MAUI para moverse entre pantallas sin tener que programar todo desde cero. Defines cada pantalla con un nombre o dirección y luego puedes decir "ve a esta página" llamándola por ese nombre.

20. ¿Cómo se accede a funcionalidades nativas del dispositivo como la cámara, el GPS o los sensores? ¿Qué es el patrón Essentials?
    
MAUI trae algo llamado .NET MAUI Essentials, que es como una caja de herramientas lista para usar. Con él puedes llamar a la cámara, saber dónde estás, consultar la batería o vibrar el celular, todo con el mismo código para cualquier dispositivo.

21. ¿Qué es .NET MAUI Essentials y menciona al menos tres servicios que ofrecen

Es una biblioteca que ya viene integrada y da acceso a cosas del celular sin tener que escribir código distinto por cada sistema. Ofrece:

* Acceso a la cámara y galería.

* Lectura de la ubicación GPS.

* Información del estado de la batería.

21. ¿Cómo se manejan los recursos como imágenes, fuentes, estilos de forma multiplataforma en MAUI?
    
Se ponen en carpetas especiales dentro del proyecto, y MAUI se encarga de adaptarlos a cada dispositivo. Las imágenes se escalan solas según la pantalla, los estilos se definen una sola vez y las fuentes se registran para que se vean bien en todos lados.

## Sección E — Comparación y contexto

23. ¿Cuál es la diferencia entre .NET MAUI y Xamarin.Forms?

MAUI es la versión más moderna y mejorada. Se conecta más directo con los sistemas operativos, es más rápido, se actualiza junto con las versiones nuevas de .NET y tiene más herramientas integradas. Xamarin.Forms ya no se va a seguir mejorando.

25. ¿Cuál es la diferencia entre desarrollar una aplicación con MAUI y una aplicación web con Blazor?

* MAUI crea aplicaciones que se instalan en el dispositivo y pueden usar sus funciones como cámara o GPS.

* Blazor crea páginas que se abren en el navegador, igual que cualquier sitio web.

* También existe Blazor Hybrid, que mezcla ambos: la interfaz es de Blazor pero corre dentro de una app de MAUI.

24. ¿Qué es .NET MAUI Blazor Hybrid y en qué caso lo utilizaría?
    
Es una combinación donde usas las páginas y el código de Blazor (como si fuera una web) pero todo se ejecuta dentro de una aplicación que se instala en el celular o la computadora. Lo usarías si ya sabes hacer páginas web y quieres convertirlas en una app sin volver a escribir todo desde cero.

26. ¿Qué ventajas ofrece MAUI frente a frameworks como Flutter o React Native?
    
Si ya sabes C# y .NET, no tienes que aprender otro lenguaje. Se integra muy bien con todo lo que ya existe de Microsoft y puedes compartir mucho código entre el programa de la computadora y la aplicación del celular.

27. ¿MAUI genera una aplicación nativa para cada plataforma o una aplicación web? Explica.
    
Genera aplicaciones nativas, o sea, que se instalan y funcionan como cualquier otra app hecha especialmente para ese celular o computadora. No es una página web disfrazada; aprovecha la velocidad y el diseño propio de cada sistema.

## Sección F — Herramientas y desarrollo

28. ¿Qué IDE o editor de códigos utilizarías para desarrollar con .NET MAUI?
    
Lo más recomendado es Visual Studio 2022 o versiones más recientes, que trae todo listo para trabajar. También se puede usar Visual Studio Code con las extensiones necesarias.

29. ¿Es necesario tener una Mac para desarrollar aplicaciones iOS con MAUI? ¿Qué opciones hay disponibles?
    
Para hacer la versión final y probarla en un dispositivo de Apple, sí se necesita una Mac o una máquina virtual con macOS. Pero se puede escribir el código en Windows y conectarse a una Mac para compilarlo y ver cómo queda.

30. ¿Qué es Hot Reload y por qué es útil durante el desarrollo?
    
Es una función que hace que los cambios que escribas en el código aparezcan de inmediato en la aplicación sin tener que cerrarla y volver a abrirla desde el principio. Ahorra muchísimo tiempo al diseñar y probar.

31. ¿Cómo se compila y ejecuta una aplicación MAUI en un dispositivo Android durante el desarrollo?
    
Puedes hacerlo de dos formas: usar un emulador que simula un celular en la computadora, o conectar un celular real por cable y activar el modo de desarrollador. En ambos casos le das "ejecutar" y se instala y abre la app automáticamente.

## Sección G — Pregunta reflexiva

32. ¿Crees que .NET MAUI es una buena opción para desarrolladores que ya conocen C# y quieren crear aplicaciones móviles y de escritorio? ¿Por qué? ¿Qué limitaciones o desafíos anticipas?
    
Sí, creo que es una excelente opción porque no tienes que aprender un lenguaje nuevo. Todo lo que ya sabes de C# te sirve de inmediato. Puedes hacer celulares y computadoras con el mismo proyecto. Las limitaciones que veo son que todavía no tiene tantos componentes listos como otros sistemas, y para publicar en Apple sí se necesita equipo de Apple, lo que puede ser un reto. Pero para quienes ya conocen C#, vale mucho la pena.
¿Quieres que lo ajuste o así está bien? 😊
