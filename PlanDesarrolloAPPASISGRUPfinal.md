


***Plan para el desarrollo de la aplicación móvil de control de asistencia de participantes de grupos de diverso tipo, que se llamará AsisGru***

Fundamentación 
Existe una diversidad de grupos comunitarios, religiosos, deportivos, culturales, educativos etc, que requieren realizar un control de asistencia de sus integrantes a las actividades que realizan; en este sentido AsisGru pretende ser una herramienta que los responsables de esos grupos puedan descargar en su dispositivo móvil y hacer el control de asistencia correspondiente

1. Objetivo
Desarrollar una aplicación móvil multiplataforma utilizando C#, Blazor, .NET MAUI y SQLite, cuyo propósito sea administrar un grupo de personas, organizar sus actividades por categorías y registrar las asistencias.

La aplicación permitirá conocer quién asistió a una actividad específica, cuántas veces asistió cada integrante a una categoría, cuántas veces participó en todas las actividades y cuántas personas asistieron por categoría, pudiendo realizar las consultas mediante rangos de fechas.

La aplicación estará diseñada para trabajar inicialmente de manera local, utilizando SQLite como base de datos.

2. Entidades de negocio
Se mantendrán las cinco entidades indicadas, sin agregar una entidad de empresa:

Grupo
Participante
Categoría de actividad
Actividad
Asistencia

Sin embargo, algunas entidades necesitan relaciones entre sí para que el sistema pueda cumplir correctamente con las consultas solicitadas.

Grupo

Contendrá la información general del grupo:

Identificador del grupo
Nombre del grupo
Descripción
Responsable del grupo
Teléfono del responsable
Organización a la que pertenece

Un grupo podrá tener muchos participantes y muchas actividades.

Participante

Representará a cada integrante del grupo:

Identificador del participante
Nombres
Apellidos
Dirección de residencia
Número de teléfono
Grupo al que pertenece

La información del teléfono debe considerarse un dato importante y debe ser obligatoria según el requerimiento.

Categoría de actividad

Permitirá clasificar las actividades.

Por ejemplo:

Deportivas
Educativas
Recreativas
Reuniones
Comunitarias

La categoría tendrá:

Identificador
Nombre
Descripción
Estado

Una categoría podrá contener muchas actividades.

Actividad

Representará cada actividad realizada por el grupo.

Debe contener:

Identificador
Nombre de la actividad
Descripción
Fecha
Hora, si se desea manejar con mayor precisión
Categoría
Grupo
Estado

Una actividad pertenecerá a una categoría y a un grupo.

Asistencia

Será la entidad encargada de registrar la participación.

Contendrá:

Identificador
Participante
Actividad
Fecha de registro
Estado de asistencia, si se desea permitir opciones como presente/ausente

La relación más importante será:

Participante + Actividad = Asistencia

Esto permitirá evitar que una misma persona sea registrada dos veces para la misma actividad.

3. Relaciones entre las entidades

La estructura principal sería:

Grupo → Participantes

Un grupo puede tener muchos participantes.

Grupo → Actividades

Un grupo puede organizar muchas actividades.

Categoría → Actividades

Una categoría puede tener muchas actividades.

Actividad → Asistencias

Una actividad puede tener muchas asistencias.

Participante → Asistencias

Un participante puede tener muchas asistencias.

Por lo tanto, las asistencias permiten relacionar indirectamente:

Participantes ↔️ Actividades

Esta estructura es fundamental para generar posteriormente los reportes.

4. Módulos de la aplicación

Mantendría tus seis módulos, pero haría una pequeña mejora en el último:

1. Configuración del grupo
2. Gestión de participantes
3. Gestión de categorías
4. Gestión de actividades
5. Registro de asistencia
6. Consultas y reportes

No agregaría módulos innecesarios. La aplicación puede mantenerse sencilla y organizada con estos seis.

5. Módulo de configuración del grupo

Será la primera sección que se configure.

Permitirá registrar y modificar:

Nombre del grupo
Descripción
Responsable
Teléfono del responsable
Organización

También sería conveniente mostrar un resumen del grupo:

Cantidad de participantes
Cantidad de categorías
Cantidad de actividades
Cantidad total de asistencias
Recomendación

Aunque el usuario pueda modificar la información, debería existir un solo registro de configuración del grupo si la aplicación está destinada a controlar un grupo específico.

Esto evita complicar innecesariamente el sistema.

6. Módulo de gestión de participantes

Permitirá administrar a todos los integrantes.

Funciones principales
Registrar participante
Editar participante
Consultar participante
Buscar por nombre o apellido
Ver información del participante
Consultar su historial de asistencia

Al seleccionar un participante sería útil mostrar:

Nombre → teléfono → dirección → actividades a las que asistió → cantidad de asistencias.

También conviene permitir que un participante sea marcado como activo/inactivo, en lugar de eliminarlo directamente.

Así se conserva su historial de asistencias.

7. Módulo de gestión de categorías

Permitirá crear y administrar las categorías de actividades.

Funciones
Crear categoría
Editar categoría
Consultar categoría
Activar/desactivar categoría
Ver las actividades pertenecientes a una categoría

Por ejemplo:

Categoría: Deportiva

→ Fútbol
→ Entrenamiento
→ Torneo

Esto facilitará posteriormente las consultas por categoría.

8. Módulo de gestión de actividades

Aquí se registrarán las actividades que realiza el grupo.

Para crear una actividad se solicitará:

Nombre
Descripción
Categoría
Fecha
Hora
Estado

Por ejemplo:

Actividad: Entrenamiento de fútbol
Categoría: Deportiva
Fecha: 07/09/2026
Hora: 15:00

Una vez creada la actividad, podrá pasar directamente al módulo de registro de asistencia.

9. Módulo de registro de asistencia

Este será uno de los módulos principales de la aplicación.

Primero se seleccionará la actividad:

Actividad: Entrenamiento de fútbol
Fecha: 07/09/2026

Después aparecerá la lista de participantes:

Participante	Asistencia
Juan Pérez	✓
María López	✓
Carlos García	
Ana Morales	✓

El responsable podrá marcar quién asistió.

Recomendación importante

La aplicación debe impedir registrar dos veces la asistencia del mismo participante para una misma actividad.

Es decir:

Una persona no puede tener dos registros de asistencia para la misma actividad.

Esto evita errores en las estadísticas.

10. Módulo de consultas y reportes

Aquí haría la mayor mejora respecto a tu planteamiento original.

En lugar de tener únicamente una pantalla de reportes, se dividirían las consultas en diferentes opciones.

A. Asistencia a una actividad específica

Permitir seleccionar:

Fecha inicial
Fecha final
Categoría
Actividad

El sistema mostrará:

Quiénes asistieron a determinada actividad.

Por ejemplo:

Entrenamiento de fútbol — 07/09/2026
Asistieron: 18 participantes.

B. Asistencia por categoría
Permitir seleccionar:

Categoría + rango de fechas

Y mostrar:

Participante	Cantidad de asistencias
Juan Pérez	8
María López	6
Carlos García	4

Esto responde directamente a:

¿Quiénes y cuántas veces asistieron a las actividades de determinada categoría?

C. Asistencia general

Permitirá consultar todas las categorías y actividades dentro de un rango de fechas.

Mostrará:

Participante	Total de asistencias
Juan Pérez	15
María López	13
Carlos García	10

Esto responde a:

¿Quiénes y cuántas veces asistieron a todas las actividades?

D. Cantidad de asistentes por categoría

Esta consulta será especialmente útil para obtener estadísticas.

Ejemplo:

Categoría	Actividades	Asistencias
Deportiva	8	125
Educativa	5	72
Recreativa	4	58

También podría mostrar el número de participantes únicos por categoría, que es diferente del número total de asistencias.

Por ejemplo:

Deportiva: 25 participantes únicos, 125 asistencias.

Esto evitará confundir "personas que asistieron" con "cantidad de veces que asistieron".

11. Filtro por rango de fechas

Este punto debe estar presente en las consultas desde el principio.

La aplicación debe permitir:

Fecha inicial → Fecha final → Consultar

Por ejemplo:

01/09/2026 — 30/09/2026

A partir de ese rango se calcularán los resultados.

Recomendación

No hacer que cada reporte tenga una lógica diferente para las fechas.

Lo ideal es utilizar un filtro de consulta común, para que todos los reportes trabajen de manera uniforme.

12. Pantalla principal

La pantalla inicial podría funcionar como un pequeño panel de control.

Mostraría:

Grupo

Nombre del grupo

Resumen
Participantes registrados
Categorías
Actividades
Asistencias registradas

Y accesos directos:

Configuración
Participantes
Categorías
Actividades
Registrar asistencia
Consultas y reportes

Esto permitirá que el usuario llegue rápidamente a las funciones principales.

13. Arquitectura requerida
Para C#, Blazor, .NET MAUI y SQLite, se debe separar la aplicación en varias capas.

Capa de presentación

Responsable de las pantallas y la interacción con el usuario.

Blazor / .NET MAUI

Aquí estarán:

Formularios
Listados
Botones
Filtros
Apariencia de la aplicación AsisGru 
Toma en cuenta que la aplicación debe presentarse en dos temas opcionales: un tema claro y un tema oscuro. Al momento de cargarse, el AsisGru debe adoptar el tema del dispositivo, es decir, si el dispositivo tiene tema oscuro, AsisGru se presentará en el tema oscuro. El usuario podrá cambiar al tema claro mediante un objeto apropiado para esta función. La apariencia de los temas se tiene que considerar al principio para el diseño de todas las interfaces.

Para efectos de los temas y para contar con un favicon o un logotipo, te adjunto la imagen en el archivo llamado Asis Gru 3.png (logotipo) . De igual manera, te adjunto una paleta de colores en el archivo que también adjunto llamado Asis Gru 2.png.

De manera predeterminada Blazor viene con Bootstrap si puedes usar este marco de trabajo de CSS no hay inconveniente, sin embargo estamos abiertos a si sugieres otro marco de CSS 

Tablas
Navegación
Capa de lógica de negocio

Será la encargada de las reglas del sistema.

Por ejemplo:

No permitir duplicar asistencias.
Validar participantes.
Validar actividades.
Obtener estadísticas.
Procesar los rangos de fechas.
Capa de acceso a datos

Será la encargada de comunicarse con SQLite.

Aquí estarán las operaciones de:

Crear
Consultar
Modificar
Desactivar
Obtener estadísticas
Base de datos

SQLite

Será la base de datos local de la aplicación.

14. Estructura general

La aplicación quedaría conceptualmente así:

INTERFAZ

↓

LÓGICA DE NEGOCIO

↓

ACCESO A DATOS

↓

SQLite

Y las entidades:

Grupo
↓
Participantes

Grupo
↓
Actividades
↓
Categorías

Participantes + Actividades
↓
Asistencias

15. Validaciones importantes

Antes de guardar información se deben realizar validaciones.

Participante
Nombres obligatorios
Apellidos obligatorios
Dirección
Teléfono obligatorio
Evitar registros duplicados innecesarios
Grupo
Nombre obligatorio
Responsable obligatorio
Teléfono del responsable
Organización
Categoría
Nombre obligatorio
Evitar categorías duplicadas
Actividad
Nombre obligatorio
Categoría obligatoria
Fecha obligatoria
Grupo correspondiente
Asistencia
Participante obligatorio
Actividad obligatoria
No permitir duplicados
16. Orden recomendado de desarrollo

Yo no comenzaría desarrollando las pantallas. Primero construiría la base que las sostiene.

Fase 1 — Análisis

Definir:

Reglas del sistema
Relaciones
Datos obligatorios
Consultas necesarias
Flujo de la aplicación
Fase 2 — Modelo de datos

Crear conceptualmente:

Grupo → Participante → Categoría → Actividad → Asistencia

Y definir correctamente las relaciones.

Fase 3 — Base SQLite

Preparar la estructura de almacenamiento y las restricciones necesarias.

Fase 4 — Acceso a datos

Crear las operaciones para consultar y modificar la información.

Fase 5 — Lógica de negocio

Implementar las reglas:

Validaciones
Duplicados
Cálculos
Estadísticas
Rangos de fechas
Fase 6 — Interfaz

Desarrollar las pantallas de los seis módulos.

Fase 7 — Consultas y reportes

Desarrollar las consultas de:

Actividad específica
Categoría
Todas las actividades
Asistencias por categoría
Rangos de fechas
Fase 8 — Pruebas

Probar casos como:

Participante sin asistencias
Actividad sin asistentes
Varias actividades de la misma categoría
Mismo participante en varias actividades
Rangos de fechas sin resultados
Intento de registrar dos veces una asistencia
Fase 9 — Publicación

Finalmente preparar la aplicación para ejecutarse en las plataformas móviles que se hayan definido.

17. Mi propuesta final de módulos

Yo dejaría exactamente estos seis módulos, pero con esta organización:

1. Configuración del grupo
Datos generales y responsable.

2. Gestión de participantes
Registro, modificación, búsqueda e historial.

3. Gestión de categorías
Creación y administración de categorías.

4. Gestión de actividades
Creación, modificación y consulta de actividades.

5. Registro de asistencia
Selección de actividad y registro de participantes asistentes.

6. Consultas y reportes

Por actividad
Por participante
Por categoría
General
Por rango de fechas
Estadísticas de asistentes por categoría
La clave del diseño

La parte más importante es que Asistencia no debe estar ligada directamente a una categoría, porque la categoría ya pertenece a la actividad.

La relación correcta es:

Categoría → Actividad → Asistencia ← Participante

De esta manera, cuando quieras saber cuántas veces asistió una persona a una categoría, el sistema puede recorrer sus asistencias y determinar a qué categoría pertenecían las actividades.

Ahorita utilizaré Visual Studio.10,MAGUI+Blazor
