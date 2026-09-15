Plan de Documentación — App AsisGru

Versión: 0.1 — Borrador inicial de trabajo
Proyecto: AsisGru — Sistema de control y registro de asistencia de integrantes de un grupo a sus actividades programadas
Tecnologías utilizadas: C# sobre plataforma .NET MAUI · Blazor Hybrid · Base de datos SQLite local (funciona 100% en el dispositivo, sin requerir conexión a internet ni servidores externos)
1. Introducción

1.1 Propósito de este documento

El presente plan tiene como objetivo establecer de forma clara y ordenada toda la documentación que se elaborará a lo largo de cada etapa del desarrollo de la aplicación AsisGru. Aquí se define qué información se va a escribir, qué contenido debe llevar cada documento, a quién va dirigido cada material, en qué formato se entregará, quiénes son los responsables de su redacción y en qué momento del proyecto se debe elaborar o actualizar.

La finalidad principal es que cualquier persona que se integre al equipo —ya sea un desarrollador nuevo, quien asuma el mantenimiento del sistema en el futuro o cualquier usuario que desee conocerlo— pueda entenderlo, consultarlo, mantenerlo, operarlo y usarlo sin necesidad de depender de terceros ni de conocimientos previos específicos que no estén explicados. Todo debe quedar por escrito de forma accesible.

1.2 Alcance del plan

Este documento cubre la totalidad de la documentación del proyecto, desde la etapa inicial en la que se definen las necesidades y los requisitos que debe cumplir la aplicación, pasando por el diseño, la arquitectura, la programación, las pruebas, la preparación para su entrega, hasta la guía de uso, la operación diaria y el soporte. Incluye también la explicación del código fuente y toda la estructura de la base de datos que se almacena de forma local en el dispositivo del usuario.

1.3 Audiencia de cada documento

La información se organiza pensando en distintos tipos de lectores, según lo que cada uno necesita saber:

* Equipo de desarrollo: Encuentra la descripción de la arquitectura, las convenciones que se siguen al programar, las decisiones técnicas que se tomaron y los motivos por los cuales se eligieron ciertas herramientas o soluciones.

* Personal encargado de las pruebas: Cuenta con los casos de prueba, los criterios de aceptación y las condiciones que deben cumplirse para considerar que una funcionalidad está terminada y funciona correctamente.

* Quienes instalan y mantienen la aplicación: Disponen de las instrucciones para la instalación, la configuración inicial, la realización de copias de seguridad, la restauración de la información y la solución de problemas frecuentes.

* Usuarios finales, especialmente quien gestiona el grupo: Tienen una guía clara y sencilla para usar la aplicación sin confusiones, consultar la asistencia y generar reportes.

* Personas que continúen el proyecto en el futuro: Encuentran el código comentado, la estructura de la base de datos explicada y el historial de decisiones tomadas, de manera que puedan darle mantenimiento sin tener que empezar desde cero.

1.4 Referencias y normas aplicadas

Para elaborar todos los documentos se toman como referencia las siguientes pautas y estándares:

* Normas ISO/IEC/IEEE 26512 y 26513, que establecen las buenas prácticas para redactar documentación de sistemas

* Formato Markdown para todos los archivos, garantizando que se puedan leer y editar desde cualquier dispositivo y sistema operativo

* Generación automática de la documentación técnica del código mediante la herramienta DocFX

* Sistema de versionado SemVer para identificar cada versión de la aplicación y de la propia documentación

1.5 Contexto general de la aplicación

AsisGru es una aplicación móvil que funciona completamente sin conexión a internet, guardando toda la información directamente en el dispositivo del usuario. Está diseñada para cumplir con las siguientes funciones:

* Administrar uno o varios grupos, registrando los datos de cada uno

* Inscribir a las personas que integran cada grupo

* Programar actividades indicando la fecha, la hora, el lugar donde se realizarán y el tipo de actividad de que se trata

* Llevar el control de asistencia en cada actividad, marcando si cada integrante estuvo presente, llegó con retraso, no asistió o justificó su inasistencia

* Consultar el historial de asistencia de cada persona y de cada actividad

* Generar y exportar reportes con la información de asistencia en formato CSV o PDF

* Establecer parámetros personalizados, como el límite de inasistencias que se consideran significativas, y crear copias de seguridad de toda la información almacenada

Las entidades principales que se manejan y se documentan son:
Grupo, Miembro, Actividad, Tipo de Actividad, Registro de Asistencia, Estado de Asistencia y Configuración de la Aplicación.

Las decisiones técnicas más relevantes que se explican detalladamente:

* Se optó por usar Blazor Hybrid dentro de .NET MAUI en lugar de desarrollar la interfaz únicamente con XAML nativo

* El acceso a la base de datos se realiza mediante Entity Framework Core junto con SQLite

* La base de datos se almacena localmente en el dispositivo y se protege mediante cifrado, sin sincronizarse con servidores externos

* Los datos personales de los integrantes también se manejan con medidas de protección y privacidad

* Se establece un procedimiento para exportar el archivo de la base de datos como respaldo y restaurarlo cuando sea necesario

* La información que se comparte entre distintas pantallas de la aplicación se gestiona mediante servicios de inyección de dependencias propios de Blazor y de ASP.NET Core
2. Estructura de carpetas y archivos del repositorio

Todos los documentos se organizan en carpetas claramente identificadas, de manera que cualquier persona pueda encontrar rápidamente lo que busca:
/asisgru
├── docs/
│   ├── 00-plan/          — Este plan de documentación y el plan general del proyecto
│   ├── 01-requisitos/    — Todo lo que la aplicación debe hacer y las condiciones que debe cumplir
│   ├── 02-arquitectura/  — Diseño interno del sistema, diagramas y decisiones técnicas
│   ├── 03-diseno/        — Diseño de las pantallas, flujos de navegación y apariencia general
│   ├── 04-datos/         — Estructura de la base de datos, tablas, relaciones y diccionario de datos
│   ├── 05-desarrollo/    — Normas de programación, guías de estilo y configuración del entorno de trabajo
│   ├── 06-pruebas/       — Plan de pruebas, casos de prueba y reporte de errores detectados
│   ├── 07-despliegue/    — Instrucciones de instalación, preparación para entregar y notas de versión
│   ├── 08-operacion/     — Mantenimiento, respaldo, recuperación y solución de problemas frecuentes
│   ├── 09-usuario/       — Manual de uso para quien maneje la aplicación
│   ├── plantillas/       — Modelos en blanco para redactar documentos nuevos con el mismo formato
│   └── _img/             — Imágenes, diagramas y capturas que se usan en los distintos documentos
├── src/                   — Código fuente con explicaciones y comentarios en cada parte
└── README.md              — Presentación general del proyecto, propósito y forma de empezar a trabajar
3. Inventario detallado de documentos

A continuación se describe cada documento que forma parte del proyecto, indicando qué información contiene, a quién está dirigido y en qué momento se elabora o actualiza.

3.1 Gestión general del proyecto

DOC-GES-01 — Plan del Proyecto

* Contenido: Se describe el alcance del trabajo, las metas que se quieren alcanzar, las fechas importantes, los recursos con los que se cuenta y los posibles riesgos que podrían presentarse y cómo se van a atender.

* Audiencia: Todo el equipo de desarrollo.

* Etapa: Se redacta al inicio del proyecto y se revisa cuando haya cambios importantes.

DOC-GES-02 — Plan de Documentación

* Contenido: Es el documento que estás leyendo. Aquí se detalla toda la lista de materiales que se van a producir, cómo deben redactarse, qué formato llevarán y cómo se mantienen actualizados.

* Audiencia: Todo el equipo y quienes se integren después.

* Etapa: Se elabora desde el inicio y se revisa y ajusta a lo largo de todo el proyecto.

3.2 Requisitos y necesidades del sistema

DOC-REQ-01 — Especificación de Requisitos

* Contenido: Se detalla cada función que la aplicación debe realizar, las condiciones de funcionamiento, lo que debe cumplir y lo que no hará. Se separa entre requisitos funcionales y no funcionales, y se establecen prioridades.

* Audiencia: Equipo de desarrollo y quienes validan el sistema.

* Etapa: Se escribe al principio y se actualiza cuando surjan cambios o nuevas necesidades.

DOC-REQ-02 — Casos de Uso

* Contenido: Se explica paso a paso qué hace cada persona dentro de la aplicación, desde que entra hasta que completa una tarea, describiendo también situaciones que pueden presentarse de forma distinta a lo esperado.

* Audiencia: Equipo de desarrollo y usuarios que participan en la validación.

* Etapa: Se elabora durante la etapa de diseño.

DOC-REQ-03 — Historias de Usuario

* Contenido: Se describe desde la perspectiva de quien usa la aplicación qué funcionalidad necesita, para qué le sirve y cuándo se puede decir que está bien hecha.

* Audiencia: Equipo de desarrollo.

* Etapa: Se va redactando y revisando durante toda la etapa de programación.

3.3 Arquitectura y diseño del sistema

DOC-ARQ-01 — Documento de Arquitectura

* Contenido: Se explica cómo está dividida la aplicación, qué partes la componen, cómo se comunican entre sí, qué tecnologías se usan y por qué se tomaron esas decisiones.

* Audiencia: Equipo de desarrollo.

* Etapa: Se redacta en la etapa de diseño y se complementa mientras se avanza en el desarrollo.

DOC-ARQ-02 — Diagrama de Componentes

* Contenido: Se muestra gráficamente qué partes conforman el sistema, cómo se conectan y qué información pasa de una a otra.

* Audiencia: Equipo de desarrollo.

* Etapa: Se elabora durante la etapa de diseño.

DOC-ARQ-03 — Registros de Decisión Técnica (ADR)

* Contenido: Cada vez que se elige una solución técnica, se explica la situación, las opciones que se consideraron, cuál se seleccionó y qué consecuencias tiene esa decisión.

* Audiencia: Equipo de desarrollo y quienes mantengan el sistema después.

* Etapa: Se redacta a lo largo de todo el proyecto, cada vez que se define una decisión importante.

DOC-DIS-01 — Diseño de Interfaz y Experiencia de Uso

* Contenido: Se describe cómo se ven las pantallas, cómo se navega entre ellas, qué colores y estilos se usan y cómo se organizan los menús y botones.

* Audiencia: Equipo de desarrollo y usuarios que participan en la validación.

* Etapa: Se elabora en la etapa de diseño y se ajusta durante el desarrollo.

DOC-DIS-02 — Diccionario de Datos y Modelo del Dominio

* Contenido: Se explican todos los datos que se manejan, qué información guarda cada elemento, cómo se relacionan entre sí y qué reglas deben cumplir.

* Audiencia: Equipo de desarrollo.

* Etapa: Se define en la etapa de diseño y se actualiza si cambia la estructura.

3.4 Base de datos y almacenamiento de información

DOC-DAT-01 — Esquema de la Base de Datos

* Contenido: Se detallan cada una de las tablas que se crean, los campos que tienen, el tipo de información que guardan, las relaciones entre ellas y las reglas de integridad.

* Audiencia: Equipo de desarrollo.

* Etapa: Se diseña desde el inicio y se actualiza con cada cambio de estructura.

DOC-DAT-02 — Estrategia de Migraciones y Respaldo

* Contenido: Se explica cómo se actualiza la base de datos cuando cambia la versión de la aplicación, cómo se crea una copia de seguridad de la información y cómo se recupera si algo falla.

* Audiencia: Equipo de desarrollo y quien administre la aplicación.

* Etapa: Se define durante el desarrollo y se mantiene actualizado.

3.5 Desarrollo y programación

DOC-DEV-01 — Guía de Estilo y Convenciones de Código

* Contenido: Se establecen las normas de cómo escribir el código, cómo nombrar cada elemento, cómo organizar la información y cómo manejar los mensajes que aparecen cuando algo sale mal, para que todo el equipo escriba de la misma forma.

* Audiencia: Quienes programan.

* Etapa: Se define desde el inicio del proyecto.

DOC-DEV-02 — Guía de Preparación del Entorno de Desarrollo

* Contenido: Se detalla qué programas y herramientas hay que instalar, cómo configurar el equipo, cómo descargar el código y cómo ponerlo en marcha para empezar a trabajar.

* Audiencia: Quienes se integren al equipo.

* Etapa: Se mantiene disponible durante todo el proyecto.

DOC-DEV-03 — Integración y Entrega Continua

* Contenido: Se explica cómo se verifica que el código funciona correctamente, cómo se realizan las pruebas automáticas y cómo se prepara la aplicación para entregarla a los usuarios.

* Audiencia: Equipo de desarrollo.

* Etapa: Se implementa durante la etapa de desarrollo.

3.6 Pruebas y verificación

DOC-PRU-01 — Plan General de Pruebas

* Contenido: Se define qué partes de la aplicación se van a probar, qué tipos de pruebas se van a realizar, en qué orden y cuándo se considera que está lista para entregarse.

* Audiencia: Equipo de desarrollo y personal de pruebas.

* Etapa: Se elabora en la etapa de diseño.

DOC-PRU-02 — Casos de Prueba Detallados

* Contenido: Se describe paso a paso qué se hace para probar cada función, qué resultado se espera y qué sucedió realmente.

* Audiencia: Personal de pruebas y equipo de desarrollo.

* Etapa: Se ejecuta y se actualiza durante todo el proyecto.

DOC-PRU-03 — Reporte de Incidencias y Errores

* Contenido: Se anota todo lo que no funciona correctamente, cómo se puede repetir el problema, qué gravedad tiene y en qué estado se encuentra su solución.

* Audiencia: Equipo de desarrollo.

* Etapa: Se actualiza cada vez que se encuentra o resuelve un problema.

3.7 Entrega, instalación y liberación de versiones

DOC-DES-01 — Guía de Instalación y Configuración

* Contenido: Se detallan los requisitos que debe tener el dispositivo, los pasos para instalar la aplicación y la configuración inicial que se debe realizar.

* Audiencia: Quien instala la aplicación y usuarios avanzados.

* Etapa: Se prepara antes de la primera entrega y se actualiza con cada versión.

DOC-DES-02 — Notas de Cada Versión

* Contenido: Se informa qué novedades trae cada entrega, qué se mejoró, qué se corrigió y si hay cosas que todavía están en proceso.

* Audiencia: Todos los usuarios.

* Etapa: Se publica con cada versión que se entrega.

DOC-DES-03 — Lista de Verificación antes de Liberar

* Contenido: Se reúne todo lo que hay que confirmar antes de entregar una versión nueva: que todo funciona, que se hizo respaldo y que está lista para salir.

* Audiencia: Responsable de cada entrega.

* Etapa: Se revisa antes de cada publicación.

3.8 Uso diario, soporte y mantenimiento

DOC-OPE-01 — Manual del Usuario

* Contenido: Explicación clara y sencilla de cómo usar la aplicación desde el primer momento, cómo registrar un grupo, cómo inscribir personas, cómo marcar asistencia y cómo generar reportes.

* Audiencia: Usuario final y quien gestiona el grupo.

* Etapa: Se elabora con la primera versión y se actualiza cuando cambien las funciones.

DOC-OPE-02 — Solución de Problemas Frecuentes

* Contenido: Se presentan las situaciones que pueden confundir al usuario, qué las causa y qué pasos seguir para resolverlas.

* Audiencia: Usuarios y quien brinde soporte.

* Etapa: Se amplía a medida que aparecen situaciones nuevas.

DOC-OPE-03 — Procedimiento de Respaldo y Recuperación

* Contenido: Se explica con qué frecuencia guardar copia de la información, dónde hacerlo y cómo recuperar los datos si se cambia de dispositivo o se pierde la información.

* Audiencia: Quien administra el grupo.

* Etapa: Disponible desde la primera versión.

3.9 Control de cambios y actualizaciones

DOC-VER-01 — Registro Histórico de Versiones

* Contenido: Se anota cada versión que se entrega, la fecha, qué cambios trae y quiénes participaron.

* Audiencia: Todos los usuarios y el equipo.

* Etapa: Se actualiza con cada nueva versión.
4. Forma de trabajar con la documentación

* Cada documento se guarda en su carpeta correspondiente con su código de identificación

* Antes de considerarse terminado, lo revisa al menos otra persona para asegurar que se entienda bien

* Cuando algo cambia en la aplicación, se actualiza también su documento; no se deja información desactualizada

* Los cambios importantes se anotan en el registro de versiones para que quede constancia

* El proceso sigue estos pasos: se redacta → se revisa → se aprueba → se publica
