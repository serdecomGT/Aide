# MAUI

## ¿Para qué se usa? Desarrollo multiplataforma:
Permite programar una aplicación una sola vez y desplegarla en Android, iOS, macOS y Windows. Interfaz de usuario única: Utiliza elementos visuales compartidos que se transforman automáticamente en los componentes nativos de cada sistema operativo. ligero. Tecnologías que utilizaC#: El lenguaje de programación principal para escribir la lógica del negocio.XAML: El lenguaje usuario de marcado utilizado para diseñar y estructurar la interfaz.MVVM / Blazor Hybrid: Soporta patrones de diseño modernos y permite integrar componentes web de Blazor dentro de la aplicación nativa. Ventajas frente a otras opcionesCódigo unificado: Las imágenes, fuentes y configuraciones de cada plataforma se gestionan desde una única carpeta del proyecto.Rendimiento nativo: No utiliza contenedores web pesados; el código se compila directamente para el procesador de cada dispositivo. Respaldo corporativo: Cuenta con el soporte oficial de Microsoft y una integración total con Visual Studio. Si quieres empezar a desarrollar con esta tecnología, dime si te gustaría que revisemos: Los requisitos e instalación en Visual Studio La estructura de un proyecto Hola Mundo en MAUI Las diferencias clave contra competidores como Flutter o React Native

**¿Qué es NET MAUI?**

.NET MAUI (acrónimo de Multi-platform App UI, o Interfaz de Aplicación Multiplataforma) es un framework de interfaz de usuario de código abierto y gratuito, desarrollado por Microsoft, que permite crear aplicaciones nativas para Android, iOS, macOS y Windows a partir de un único código base compartido. Es la evolución moderna de Xamarin.Forms, llevando el desarrollo multiplataforma al ecosistema unificado de .NET.

La idea central es simple pero poderosa: escribir el código una sola vez y que funcione en todos los sistemas operativos. En lugar de aprender lenguajes distintos para cada plataforma (Swift para iPhone, Kotlin para Android, C# para Windows, Objective-C para Mac), se usa C# y XAML para definir tanto la lógica como el diseño, y MAUI se encarga de adaptar todo a las características de cada dispositivo.

**Historia y origen**

* 2014: Nace Xamarin.Forms, permitiendo compartir la interfaz de usuario entre móviles.

* 2020: Microsoft anuncia que unificará todos los modelos de aplicación en una sola plataforma: .NET MAUI.

* 2022: Se lanza la versión oficial junto con .NET 6.

* Actualidad: Se actualiza con cada versión de .NET, mejorando rendimiento, controles y herramientas.

**¿Cómo funciona?**

MAUI no crea una "aplicación web disfrazada": genera aplicaciones nativas reales. Esto significa que lo que se ve en la pantalla son los botones, menús y controles propios de cada sistema operativo, no copias que se parecen pero no funcionan igual.

La arquitectura se divide en dos partes:

* Código compartido: todo lo que es igual en todas partes: lógica, cálculos, conexiones con bases de datos, validaciones, etc.

* Código específico por plataforma: si necesitas algo exclusivo de un sistema (por ejemplo, usar una función que solo existe en Android), puedes escribir código especial solo para esa plataforma sin afectar a las demás.

Características principales

**Multiplataforma real**

* Android: se compila en una aplicación nativa con el mismo formato que las que se descargan de Google Play.

* iOS: se genera una app compatible con iPhone y iPad, siguiendo los estándares de Apple.

* macOS: se puede crear una aplicación de escritorio que se instala en computadoras Mac.

* Windows: se compila como aplicación moderna para Windows 10 y 11.

**Lenguajes y herramientas**

* Se programa principalmente en C# para la lógica y en XAML para el diseño visual.

* Se trabaja desde Visual Studio 2022 o Visual Studio para Mac, con herramientas visuales para arrastrar y soltar controles.

* Se integra con todo el ecosistema de .NET: bibliotecas, bases de datos, servicios en la nube, etc.

**Controles y diseño**

MAUI trae una biblioteca completa de controles que se adaptan solos a cada sistema: botones, campos de texto, listas, menús, calendarios, mapas, gráficas, cámaras, etc. También se puede personalizar todo: colores, fuentes, tamaños, formas.

Para organizar la pantalla se usan contenedores como:

* StackLayout: apila los elementos uno debajo de otro o uno al lado del otro.

* Grid: organiza todo en filas y columnas como una tabla.

* AbsoluteLayout: coloca los elementos en posiciones exactas de la pantalla.

* FlexLayout: distribuye los elementos de forma flexible según el tamaño de la pantalla.

***Acceso a funciones del dispositivo***

MAUI incluye una API que permite acceder a las capacidades del celular o computadora sin necesidad de escribir código especial por plataforma:

**Cámara y galería de fotos**

  **GPS y ubicación**

  **Estado de la conexión a internet**

  **Notificaciones**

  **Almacenamiento de archivos**

  **Contactos**

   **Estado de la batería**

  **Información del dispositivo**

**Arquitectura recomendada:** MVVM

***Para mantener el código ordenado, MAUI se recomienda usar el patrón MVVM (Model-View-ViewModel):***

* Modelo: representa los datos, por ejemplo: "Usuario", "Producto", "Nota".

* Vista: es lo que ve el usuario, la pantalla, escrita en XAML.

* ViewModel: es el puente entre la vista y los datos. Aquí va la lógica sin mezclarla con el diseño.

Esto permite que el diseño y la lógica evolucionen por separado, facilitando que una persona trabaje en lo visual y otra en la parte funcional.

***Ciclo de desarrollo con MAUI***

1. Diseñar la interfaz: en XAML, definir cómo se ven las pantallas.

2. Programar la lógica: en C#, definir qué pasa cuando se hace clic, qué datos se muestran, cómo se guarda la información.

3. Probar: usar el emulador para ver cómo se ve en celular o en computadora sin necesidad de tener los dispositivos físicos.

4. Corregir y ajustar: probar en diferentes tamaños de pantalla y orientaciones.

5. Publicar: generar los archivos de instalación para subir a las tiendas de aplicaciones o distribuir directamente.

Ventajas de .NET MAUI

✅ Menos código para mantener: no hay que escribir ni actualizar la misma aplicación 4 veces. Se hace una sola vez y se comparte.

✅ Equipos más pequeños: no necesitas especialistas en 4 lenguajes distintos. Quienes ya saben C# pueden empezar a desarrollar para móviles y escritorio sin aprender desde cero.

✅ Consistencia: si cambias algo en la lógica, se refleja en todas las plataformas al mismo tiempo.

✅ Rendimiento nativo: no es una página web metida en un marco vacío; es código que se ejecuta directamente en el sistema operativo.

✅ Integración con Blazor: puedes usar componentes web hechos en Blazor dentro de una app de MAUI, reutilizando conocimientos de desarrollo web.

Desventajas y retos

❌ Menos madurez que Xamarin.Forms: al ser más nuevo, todavía se están agregando controles y corrigiendo detalles.

❌ Comunidad más pequeña: hay menos tutoriales y respuestas en internet que para tecnologías con más años.

❌ Requiere conocimientos de .NET: si nunca has programado en C#, primero debes aprender ese lenguaje antes de empezar con MAUI.

❌ Dependencia de Microsoft: al ser una tecnología de Microsoft, su evolución depende de las decisiones de esa empresa.

Comparación con otras opciones

* vs. Xamarin.Forms: MAUI es el sucesor oficial. Xamarin.Forms dejará de recibir soporte en 2026. MAUI es más rápido, más ordenado y más moderno.

* vs. Flutter: Flutter usa el lenguaje Dart. MAUI usa C#. Si ya conoces C# y .NET, MAUI es más natural. Si empiezas desde cero, ambas son buenas opciones.

* vs. React Native: Usa JavaScript. MAUI es más cerrado pero más ordenado para equipos que ya trabajan con tecnologías de Microsoft.

* vs. Desarrollo nativo: Swift para iOS y Kotlin para Android dan máximo rendimiento, pero requieren mantener dos códigos separados y aprender dos lenguajes distintos.

Casos de uso en proyectos escolares y profesionales

* 📱 Aplicaciones de inventario: para negocios pequeños que quieren registrar entradas y salidas desde el celular.

* 📋 Sistemas de control escolar: donde maestros registran notas y estudiantes las consultan desde su celular.

* 📖 Guías y catálogos: aplicaciones que muestran información, imágenes y videos organizados por categorías.

* 📝 Formularios y encuestas: que funcionan incluso sin internet y luego sincronizan los datos cuando hay conexión.

* 🏠 Aplicaciones de gestión personal: gastos, tareas, recordatorios, agenda.

Buenas prácticas al trabajar con MAUI

* Organiza tu código desde el principio: separa las carpetas por Modelos, Vistas, Servicios, Herramientas.

* No pongas toda la lógica en el código de la vista: usa el patrón MVVM para que si cambias de diseño, no tengas que reescribir todo.

* Reutiliza controles: si vas a usar el mismo botón o la misma tarjeta en varias pantallas, créalo una sola vez y úsalo donde lo necesites.

* Prueba en tamaños de pantalla distintos: lo que se ve bien en un celular grande puede verse mal en uno pequeño.

* Usa recursos compartidos: define los colores y fuentes en un solo lugar para que si cambias el estilo, se actualice en toda la aplicación.

* Consume datos desde servicios: no conectes directamente a la base de datos desde la app; crea un servicio web que entregue la información de forma segura.

El futuro de .NET MAUI

Microsoft está apostando fuerte por MAUI como la plataforma oficial multiplataforma de .NET. Cada versión trae mejoras de rendimiento, nuevos controles y más estabilidad. A medida que las empresas migran desde Xamarin.Forms, la demanda de personas que sepan trabajar con MAUI va a crecer, especialmente en equipos que ya usan C# y .NET para otras partes de sus sistemas.
Va nn
