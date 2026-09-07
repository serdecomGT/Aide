
Plan de Desarrollo — App de Control de Asistencia

# Objetivo

Crear una aplicación móvil multiplataforma (Android, iOS, Windows) que funcione completamente en modo local, para registrar y consultar la asistencia de integrantes de grupos a actividades organizadas por categorías, filtrando siempre por un rango de fechas.

# Diseño de la Base de Datos (SQLite)

Definimos las tablas necesarias para guardar toda la información:

 ## Tabla 1: Organizaciones

* ID (clave primaria)

* Nombre de la organización

* Dirección

* Teléfono

## Tabla 2: Grupos

* ID (clave primaria)

* Nombre del grupo

* ID_Organización (clave foránea → vincula con la organización)

* ID_Encargado (clave foránea → vincula con el integrante que es el responsable)

## Tabla 3: Integrantes

* ID (clave primaria)

* Nombres

* Apellidos

* Dirección de residencia

* Número de teléfono

* ID_Grupo (clave foránea → a qué grupo pertenece)

* ¿Es encargado? (Sí / No)

## Tabla 4: Categorías

* ID (clave primaria)

* Nombre de la categoría (ej: reunión, capacitación, deporte, cultural)

## Tabla 5: Actividades

* ID (clave primaria)

* Nombre de la actividad

* Fecha y hora

* Lugar

* ID_Categoría (clave foránea)

* ID_Grupo (clave foránea)

## Tabla 6: Asistencia

* ID (clave primaria)

* ID_Actividad (clave foránea)

* ID_Integrante (clave foránea)

* ¿Asistió? (Sí / No)

* Fecha de registro
  
# Estructura de Pantallas / Módulos

## Módulo 1 — Configuración Inicial

* Registrar los datos de la organización.

* Registrar los grupos que pertenecen a la organización.

* Asignar al encargado de cada grupo, seleccionándolo de la lista de integrantes ya registrados.

## Módulo 2 — Gestión de Integrantes

* Formulario para registrar cada integrante con: nombres, apellidos, dirección y teléfono.

* Asignar al grupo al que pertenece.

* Posibilidad de marcarlo como encargado del grupo.

* Permitir consultar, editar y eliminar integrantes.

## Módulo 3 — Gestión de Categorías

* Crear, editar y eliminar las categorías que agruparán las actividades.

## Módulo 4 — Gestión de Actividades

* Crear actividades: nombre, fecha, hora, lugar, categoría y grupo responsable.

* Editar o eliminar actividades.

## Módulo 5 — Registro de Asistencia

* Seleccionar una actividad.

* Mostrar la lista de integrantes del grupo asignado a esa actividad.

* Marcar quién asistió y quién no.

* Guardar el registro en la base de datos.


## Módulo 6 — Consultas y Reportes
Siempre se debe seleccionar un rango de fechas (fecha inicial y fecha final) antes de consultar. Las consultas requeridas son:

1. ¿Quiénes asistieron a una actividad específica?
→ Seleccionar la actividad y mostrar la lista de personas que asistieron en el período.

2. ¿Quiénes y cuántas veces asistieron a las actividades de una categoría?
→ Seleccionar categoría → listar personas y contar cuántas veces asistieron en ese rango de fechas.

3. ¿Quiénes y cuántas veces asistieron a todas las actividades?
→ Listar todos los integrantes y mostrar su total de asistencias en el período seleccionado.

4. ¿Cuántos asistentes hubo por categoría?
→ Mostrar un resumen: nombre de la categoría y cantidad total de personas que asistieron en cada una, dentro del rango de fechas.
🛠️ 3. Tecnologías a Utilizar

* Base de datos: SQLite → todo se guarda localmente en un archivo, sin servidor.

* Lenguaje de programación: C#

* Framework de interfaz: .NET MAUI + Blazor → permite crear la app una sola vez y que funcione en Android, iOS y Windows.
* 
  ## 4. Pasos del Desarrollo

***Paso 1 — Diseño de la Base de Datos***

* Definir las tablas y sus relaciones.

* Crear el archivo de base de datos SQLite y estructurar las tablas.

* Activar las claves foráneas para mantener la integridad de los datos.

***Paso 2 — Configuración del Proyecto***

* Crear el proyecto en Visual Studio con la plantilla de .NET MAUI Blazor.

* Instalar los paquetes necesarios para conectar con SQLite.

* Establecer la conexión con el archivo de base de datos local.

***Paso 3 — Desarrollo de los Módulos de Registro***

* Crear las pantallas y la lógica para registrar organizaciones, grupos, integrantes, categorías y actividades.

* Validar que los campos obligatorios (nombre, teléfono, etc.) no queden vacíos.

***Paso 4 — Desarrollo del Módulo de Asistencia***

* Crear la pantalla para seleccionar la actividad y marcar la asistencia de cada integrante.

* Guardar cada registro en la tabla de asistencia.

***Paso 5 — Desarrollo del Módulo de Reportes***

* Diseñar la selección de rango de fechas.

* Programar las 4 consultas requeridas filtrando por el período seleccionado.

* Mostrar los resultados de forma clara y legible en pantalla.

***Paso 6 — Pruebas y Ajustes***

* Probar que se guarden y se lean bien los datos.

* Verificar que las consultas filtren correctamente por fechas.

* Comprobar que la app funcione sin conexión a internet.

* Corregir errores y mejorar la facilidad de uso.
* 

## Consideraciones Importantes

* Todo funciona en modo local: no hay servidores en la nube, no se necesita internet.

* Cada grupo tiene un encargado, que es uno de los integrantes registrados.

* Los datos personales son obligatorios: nombres, apellidos, dirección y teléfono de cada integrante.

* Todas las consultas se filtran por fechas: el usuario siempre debe indicar desde qué fecha hasta qué fecha quiere ver la información.

* No hay límite de grupos ni organizaciones: la base de datos debe permitir registrar varios si la aplicación se usa para más de uno.





# version 2

## 1. Nombre de la Aplicación

App de Control de Asistencia para Grupos y Actividades

2. Objetivo General

Crear una aplicación móvil multiplataforma que funcione en modo local, sin necesidad de conexión a internet, para registrar, consultar y gestionar la asistencia de los integrantes de uno o más grupos a actividades organizadas por categorías. La aplicación permitirá filtrar toda la información por un rango de fechas determinado.
3. Funcionalidades Principales

La aplicación debe cumplir con las siguientes funciones:

3.1 Gestión de Configuración

• Registrar los datos de una o más organizaciones.

• Crear y gestionar grupos pertenecientes a cada organización.

• Asignar un encargado a cada grupo.

3.2 Gestión de Integrantes

• Registrar los datos personales de cada integrante.

• Asignar cada integrante a un grupo específico.

• Identificar si un integrante es encargado de un grupo.

• Consultar, editar y eliminar registros de integrantes.

3.3 Gestión de Categorías

• Crear categorías para clasificar las actividades.

• Editar y eliminar categorías según sea necesario.

3.4 Gestión de Actividades

• Registrar actividades con su nombre, fecha, hora, lugar, categoría y grupo responsable.

• Editar o eliminar actividades ya registradas.

3.5 Registro de Asistencia

• Seleccionar una actividad registrada.

• Mostrar la lista de integrantes del grupo asignado a esa actividad.

• Marcar quiénes asistieron y quiénes no.

• Guardar el registro de asistencia en la base de datos.

3.6 Consultas y Reportes

Todas las consultas deben permitir seleccionar un rango de fechas para filtrar la información.

Las consultas requeridas son:

1. ¿Quiénes asistieron a una actividad específica?

2. ¿Quiénes y cuántas veces asistieron a las actividades de una categoría determinada?

3. ¿Quiénes y cuántas veces asistieron a todas las actividades registradas?

4. ¿Cuántos asistentes hubo por categoría en un período determinado?
4. Tecnologías a Utilizar

• Base de datos: SQLite
Permite almacenar toda la información localmente en un solo archivo, sin necesidad de un servidor.

• Lenguaje de programación: C#
Lenguaje orientado a objetos, adecuado para el desarrollo de aplicaciones móviles y de escritorio.

• Framework de interfaz: .NET MAUI + Blazor
Permite desarrollar la aplicación una sola vez y ejecutarla en Android, iOS y Windows.
5. Diseño de la Base de Datos

La base de datos estará compuesta por seis tablas principales:

5.1 Tabla: Organizaciones
Campo Tipo Descripción 
ID Clave primaria Identificador único de la organización 
Nombre Texto Nombre de la organización 
Dirección Texto Dirección física de la organización 
Teléfono Texto Número de contacto de la organización 

5.2 Tabla: Grupos
Campo Tipo Descripción 
ID Clave primaria Identificador único del grupo 
Nombre Texto Nombre del grupo 
ID_Organización Clave foránea Relaciona el grupo con su organización 
ID_Encargado Clave foránea Relaciona el grupo con su encargado 

5.3 Tabla: Integrantes
Campo Tipo Descripción 
ID Clave primaria Identificador único del integrante 
Nombres Texto Nombres del integrante 
Apellidos Texto Apellidos del integrante 
Dirección Texto Dirección de residencia 
Teléfono Texto Número de contacto 
ID_Grupo Clave foránea Relaciona el integrante con su grupo 
Es_Encargado Booleano Indica si el integrante es encargado del grupo 

5.4 Tabla: Categorías
Campo Tipo Descripción 
ID Clave primaria Identificador único de la categoría 
Nombre Texto Nombre de la categoría de actividades 

5.5 Tabla: Actividades
Campo Tipo Descripción 
ID Clave primaria Identificador único de la actividad 
Nombre Texto Nombre de la actividad 
FechaHora Fecha/Hora Fecha y hora de realización 
Lugar Texto Lugar donde se realiza la actividad 
ID_Categoría Clave foránea Relaciona la actividad con su categoría 
ID_Grupo Clave foránea Relaciona la actividad con el grupo responsable 

5.6 Tabla: Asistencia
Campo Tipo Descripción 
ID Clave primaria Identificador único del registro de asistencia 
ID_Actividad Clave foránea Relaciona el registro con la actividad 
ID_Integrante Clave foránea Relaciona el registro con el integrante 
Asistio Booleano Indica si el integrante asistió a la actividad 
FechaRegistro Fecha/Hora Fecha y hora en que se registró la asistencia 

6. Estructura de la Aplicación

La aplicación se organizará en los siguientes módulos:

6.1 Módulo de Configuración

• Registro de organizaciones.

• Registro de grupos.

• Asignación de encargados.

6.2 Módulo de Integrantes

• Registro de integrantes.

• Asignación a grupos.

• Consulta, edición y eliminación de integrantes.

6.3 Módulo de Categorías

• Creación, edición y eliminación de categorías.

6.4 Módulo de Actividades

• Registro de actividades.

• Edición y eliminación de actividades.

6.5 Módulo de Registro de Asistencia

• Selección de actividad.

• Visualización de integrantes del grupo.

• Registro de asistencia.

6.6 Módulo de Reportes

• Selección de rango de fechas.

• Consulta de asistencia por actividad.

• Consulta de asistencia por categoría.

• Consulta de asistencia general por integrante.

• Resumen de asistentes por categoría.
7. Flujo de Trabajo del Desarrollo

Paso 1: Diseñar la Base de Datos

• Definir las tablas, campos y relaciones.

• Crear el archivo de base de datos SQLite.

• Configurar las claves primarias y foráneas.

Paso 2: Configurar el Proyecto

• Crear el proyecto en Visual Studio con .NET MAUI Blazor.

• Instalar los paquetes necesarios para conectar con SQLite.

• Establecer la conexión al archivo de base de datos local.

Paso 3: Desarrollar los Módulos de Registro

• Crear las pantallas para registrar organizaciones, grupos, integrantes, categorías y actividades.

• Agregar validaciones para que los campos obligatorios no queden vacíos.

Paso 4: Desarrollar el Módulo de Asistencia

• Crear la pantalla para seleccionar actividades.

• Cargar la lista de integrantes correspondientes al grupo de la actividad.

• Implementar la función para marcar y guardar la asistencia.

Paso 5: Desarrollar los Reportes

• Agregar controles para seleccionar el rango de fechas.

• Programar las cuatro consultas requeridas.

• Mostrar los resultados en listas o resúmenes claros.

Paso 6: Probar la Aplicación

• Verificar que los datos se guarden correctamente.

• Comprobar que las consultas filtren por fechas.

• Asegurar que la aplicación funcione sin conexión a internet.

• Corregir errores y mejorar la usabilidad.

8. Consideraciones Importantes

• Toda la aplicación funciona en modo local.

• No se requiere servidor ni conexión a internet para utilizarla.

• Cada grupo tiene un encargado, que debe ser uno de los integrantes registrados.

• Los datos personales de los integrantes son obligatorios: nombres, apellidos, dirección y teléfono.

• Todas las consultas y reportes deben filtrarse por un rango de fechas.

• La base de datos permite registrar varias organizaciones, grupos, categorías y actividades.

• La aplicación debe ser fácil de usar, clara y adaptable a diferentes tamaños de pantalla.

9. Resultado Final Esperado

Una aplicación móvil y de escritorio funcional, que permita gestionar organizaciones, grupos, integrantes, categorías, actividades y registros de asistencia, almacenando toda la información en una base de datos SQLite local, y generando reportes filtrados por fechas de manera rápida y sencilla.














