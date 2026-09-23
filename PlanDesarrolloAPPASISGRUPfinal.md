Plan para el desarrollo de la aplicación móvil de control de asistencia de participantes de grupos de diverso tipo, que se llamará AsisGru

 # Proyecto: AsisGru

Sistema de control y registro de asistencia de integrantes de un grupo a sus actividades programadas

Tecnologías utilizadas: C#, .NET MAUI, Blazor Hybrid y SQLite.

## 1. Introducción
1.1 Propósito del documento

Este documento tiene como propósito presentar y organizar la información relacionada con el desarrollo de la aplicación AsisGru. En él se describe la finalidad del sistema, las tecnologías utilizadas, su estructura general, las funciones principales y la forma en que se encuentra organizado el proyecto.

La documentación busca servir como apoyo durante el desarrollo y también como referencia para comprender el funcionamiento de la aplicación y facilitar futuras modificaciones o correcciones.

1.2 Alcance

AsisGru es una aplicación móvil desarrollada para facilitar el registro y control de asistencia de los integrantes de uno o varios grupos a las actividades que se realizan.

La aplicación permite administrar los grupos, registrar participantes, crear categorías de actividades, programar actividades y llevar el registro de asistencia de los participantes.

La información se almacena de manera local mediante SQLite, por lo que las funciones principales de la aplicación no dependen de una conexión a internet ni de un servidor externo.

1.3 Tecnologías utilizadas

Para el desarrollo de AsisGru se utilizaron las siguientes tecnologías:

Csharp como lenguaje principal de programación.
.NET 10 como plataforma de desarrollo.
.NET MAUI para la creación de la aplicación móvil.
Blazor Hybrid para desarrollar las interfaces utilizando componentes Razor.
SQLite para almacenar la información localmente.
Visual Studio como entorno principal de desarrollo.
1.4 Funcionamiento general

La aplicación está organizada en diferentes módulos que permiten administrar la información necesaria para llevar el control de asistencia.

Los principales módulos desarrollados son:

Grupos: permite registrar y administrar los grupos.
Participantes: permite registrar a las personas que pertenecen a cada grupo.
Categorías de actividades: permite organizar las actividades según su tipo.
Actividades: permite registrar las actividades programadas.
Asistencia: permite seleccionar una actividad y registrar qué participantes asistieron.
Reportes: permite consultar la información registrada.

La información de estos módulos se relaciona entre sí. Por ejemplo, una actividad pertenece a un grupo y a una categoría, mientras que los registros de asistencia relacionan una actividad con los participantes que asistieron.

## 2. Estructura principal del sistema

La aplicación se encuentra organizada principalmente en modelos, páginas y servicios.

***AsisGru***
es una aplicación móvil diseñada para facilitar la administración de integrantes y el control de asistencia en diferentes tipos de grupos y organizaciones. Puede adaptarse a grupos deportivos, educativos, religiosos, culturales, comunitarios, recreativos y otros grupos que necesiten llevar un registro organizado de sus integrantes y de las actividades que realizan.

La aplicación permite registrar los integrantes de cada grupo, organizar sus actividades y llevar un control de asistencia. Debido a que su estructura no está limitada a un tipo específico de organización, puede utilizarse en distintos contextos según las necesidades del grupo, por ejemplo, en actividades deportivas, educativas, religiosas, culturales, comunitarias o recreativas.
Los modelos representan la información que utiliza la aplicación.

Las páginas Razor corresponden a las diferentes pantallas o módulos con los que interactúa el usuario.

Los servicios se encargan de realizar las operaciones relacionadas con la información almacenada en la base de datos.

## 3. Entidades principales

3.1 Grupo

El grupo permite organizar a los participantes y las actividades que pertenecen a una misma organización o agrupación.

Entre los datos principales se encuentran:

Id
Nombre
Descripción
Responsable
Teléfono del responsable
Organización

3.2 Participante

Representa a cada persona que forma parte de un grupo.

Sus principales datos son:

Id
Nombres
Apellidos
Dirección
Teléfono
Grupo al que pertenece

3.3 Categoría de actividad

Permite clasificar las actividades para mantenerlas organizadas.

Sus datos principales son:

Id
Nombre
Descripción
Estado

3.4 Actividad

Representa una actividad programada por un grupo.

Sus principales datos son:

Id
Nombre
Descripción
Fecha
Hora
Categoría
Grupo
Estado


3.5 Asistencia

Registra la participación de una persona en una actividad.

Sus principales datos son:

Id
Participante
Actividad
Fecha de registro
Estado

La relación entre participante y actividad permite evitar que se registre dos veces la asistencia de una misma persona para una misma actividad.

##4. Organización del desarrollo

El desarrollo de AsisGru se realizó de manera progresiva, comenzando con la estructura de la aplicación y posteriormente incorporando los diferentes módulos.

Primero se definieron los modelos y la información que debía manejar el sistema. Después se trabajó en la conexión con SQLite y en los servicios encargados de administrar los datos.

Posteriormente se desarrollaron las diferentes páginas de la aplicación:

Grupos.
Participantes.
Categorías.
Actividades.
Asistencia.
Reportes.

Durante el desarrollo también fue necesario realizar diferentes correcciones en el código, solucionar errores de compilación y ajustar algunos componentes para que funcionaran correctamente dentro de .NET MAUI y Blazor Hybrid.

## 5. Registro de asistencia

El módulo de asistencia permite seleccionar una actividad previamente registrada y mostrar los participantes pertenecientes al grupo correspondiente.

El usuario puede marcar mediante casillas de selección a las personas que asistieron y posteriormente guardar el registro.

El sistema consulta las asistencias existentes antes de mostrarlas, por lo que los participantes que ya tienen una asistencia registrada aparecen seleccionados.

Al guardar, la aplicación comprueba si la asistencia ya existe antes de registrarla, evitando duplicados para la misma persona y actividad.

6. Base de datos

AsisGru utiliza SQLite como sistema de almacenamiento local.

La base de datos contiene la información necesaria para administrar los grupos, participantes, categorías, actividades y asistencias.

La información se almacena en el dispositivo donde se encuentra instalada la aplicación, permitiendo que las operaciones principales puedan realizarse sin depender de servicios externos.

## 7. Conclusión

AsisGru fue desarrollado como una solución para facilitar la organización de grupos y el control de asistencia a sus actividades.

La aplicación integra diferentes módulos relacionados entre sí y utiliza C#, .NET MAUI, Blazor Hybrid y SQLite para proporcionar una aplicación móvil con almacenamiento local.

Durante el desarrollo se realizaron diferentes pruebas y correcciones para solucionar errores y mejorar el funcionamiento de los módulos. El proyecto queda estructurado de manera que sea posible continuar agregando mejoras y nuevas funciones en el futuro.

Por si vas a poner eso
