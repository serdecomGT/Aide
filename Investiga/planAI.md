# Entidades
1.Grupo
2.Participantes
3.Categoria - Aide
4.Actividades - Aide
5.Regristro de acistencia 




## Plan de Desarrollo — App de Control de Asistencia

# Objetivo

Crear una aplicación móvil multiplataforma (Android, iOS, Windows) que funcione completamente en modo local, para registrar y consultar la asistencia de integrantes de grupos a actividades organizadas por categorías, filtrando siempre por un rango de fechas.

# Diseño de la Base de Datos (SQLite)

Definimos las tablas necesarias para guardar toda la información:

 # Tabla 1: Organizaciones

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





##  Version 2

 
## Plan Alternativo — Versión 2

Nombre del proyecto: Segundo Olán — Control de Asistencia

Objetivo

Desarrollar una aplicación móvil multiplataforma (Android, iOS, Windows) que funcione completamente en modo local, para gestionar y registrar la asistencia de los integrantes de grupos a actividades organizadas por categorías, permitiendo consultar y filtrar la información por un rango de fechas específico.

 
 Entidades de Negocio Definidas

1. Grupo

• Nombre del grupo

• Descripción del grupo

• Responsable del grupo (seleccionado de entre los participantes)

• Teléfono del responsable

• Organización a la que pertenece

2. Participante

• Nombres y apellidos

• Dirección de residencia

• Número de teléfono

• Grupo al que pertenece

• ¿Es responsable del grupo? (Sí / No)

3. Categoría de Actividad

• Nombre de la categoría (ej: capacitación, deporte, reunión, cultural)

4. Actividad

• Nombre de la actividad

• Fecha y hora

• Lugar

• Categoría a la que pertenece

• Grupo responsable

5. Asistencia

• Actividad a la que se refiere

• Participante que se registra

• ¿Asistió? (Sí / No)

• Fecha de registro

📱 Estructura de Módulos

1. **Configuración de Grupo**

• Registrar los datos del grupo: nombre, descripción, organización.

• Asignar al responsable del grupo, seleccionándolo de los participantes ya registrados.

• Registrar el teléfono del responsable.

2. **Gestión de Integrantes (Participantes)**

• Registrar cada participante con: nombres, apellidos, dirección, teléfono.

• Asignar al grupo al que pertenece.

• Marcar si es el responsable del grupo.

• Permitir editar o eliminar registros.

3. **Gestión de Categorías de Actividades**

• Crear categorías para clasificar las actividades.

• Editar o eliminar categorías según sea necesario.

4. **Gestión de Actividades**

• Registrar cada actividad: nombre, fecha, hora, lugar, categoría y grupo responsable.

• Editar o eliminar actividades.

5. **Registro de Asistencia**

• Seleccionar la actividad de la lista.

• Aparece la lista de participantes del grupo responsable.

• Marcar quién asistió y quién no.

• Guardar el registro.

6. **Consultas y Reportes**

# Siempre se selecciona un rango de fechas antes de consultar:

1. ¿Quiénes asistieron a una actividad determinada? → Lista de participantes presentes.

2. ¿Quiénes y cuántas veces asistieron a las actividades de una categoría? → Nombres + contador de asistencias.

3. ¿Quiénes y cuántas veces asistieron a todas las actividades? → Todos los participantes con su total de asistencias.

4. ¿Cuántos asistentes hubo por categoría? → Resumen: categoría ↔ cantidad total de personas.
   
**Tecnologías**

• Base de datos: SQLite — todo en un archivo local, sin servidor.

• Interfaz y lógica: C#, Blazor, .NET MAUI — funciona en celular y computadora.

*Pasos de Desarrollo*

**Paso 1 — Diseñar la Base de Datos**

• Crear las 5 tablas con sus campos y relaciones.

• Configurar claves primarias y foráneas.

**Paso 2 — Crear el Proyecto**

• Abrir Visual Studio → nuevo proyecto .NET MAUI Blazor.

• Conectar con SQLite.

**Paso 3 — Desarrollar los Módulos**

• Pantalla por cada módulo: configuración, participantes, categorías, actividades, asistencia, reportes.

• Validar que los campos obligatorios no queden vacíos.

**Paso 4 — Probar**

• Verificar que se guarde todo bien.

• Comprobar que las consultas filtren por fechas correctamente.

• Asegurarse de que funcione sin internet.








