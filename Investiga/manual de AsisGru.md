# MANUAL DE USUARIO — ASISGRU
1. PORTADA

ASISGRU

Sistema de control y registro de asistencia de integrantes de un grupo a sus actividades programadas

MANUAL DE USUARIO

Desarrolladoras:

Daniela Alejandra López de León
Idania Aide Rubio Barrios

Escuela Normal de Maestras de Educación para el Hogar
“Humberto Miranda Fuentes”

Quinto Bachillerato en Ciencias y Letras con Orientación en Computación

Quetzaltenango, Guatemala

2026

2. INTRODUCCIÓN

ASISGRU es una aplicación móvil desarrollada para facilitar el control y registro de asistencia de los integrantes de un grupo durante las diferentes actividades que se realizan.

La aplicación permite organizar la información del grupo, registrar a sus participantes, crear categorías para clasificar las actividades, registrar las actividades programadas y llevar un control de la asistencia de los participantes.

ASISGRU fue desarrollada como una aplicación para dispositivos móviles Android y utiliza almacenamiento local mediante SQLite. Esto permite que la información utilizada por la aplicación se gestione directamente en el dispositivo.

La aplicación puede ser utilizada por diferentes tipos de grupos, entre ellos grupos comunitarios, religiosos, deportivos, culturales, educativos y otros grupos que necesiten llevar un registro organizado de sus integrantes y de su participación en actividades.

El presente manual tiene como finalidad explicar de manera sencilla y ordenada el funcionamiento de ASISGRU, mostrando cada uno de sus módulos y las acciones que el usuario puede realizar dentro de la aplicación.

3. OBJETIVO DEL MANUAL

El objetivo de este manual es proporcionar al usuario una guía para aprender a utilizar correctamente la aplicación ASISGRU.

A través de las instrucciones presentadas, el usuario podrá conocer el funcionamiento de cada módulo, registrar y administrar la información del grupo, gestionar participantes, crear categorías y actividades y registrar la asistencia correspondiente.

También se busca facilitar el uso de la aplicación a personas que no tengan experiencia previa con sistemas de control de asistencia.

4. OBJETIVO DE LA APLICACIÓN

ASISGRU tiene como objetivo facilitar el control y registro de asistencia de integrantes de un grupo a sus actividades programadas.

La aplicación permite centralizar la información necesaria para llevar un registro organizado y evitar que el control de asistencia tenga que realizarse únicamente de forma manual.

Entre sus principales funciones se encuentran:

Configurar la información del grupo.
Registrar participantes.
Buscar participantes.
Filtrar participantes según su estado.
Crear categorías de actividades.
Registrar actividades.
Establecer fecha y hora para las actividades.
Registrar la asistencia de los participantes.
Consultar la información registrada.
5. REQUISITOS PARA UTILIZAR ASISGRU

Para utilizar ASISGRU se necesita un dispositivo móvil compatible con la versión de Android para la cual fue preparada la aplicación.

El usuario debe instalar la aplicación en el dispositivo y posteriormente abrirla desde el menú de aplicaciones.

ASISGRU utiliza una base de datos local mediante SQLite, por lo que la información registrada por la aplicación se almacena localmente en el dispositivo.

Consideraciones

Antes de comenzar a utilizar la aplicación se recomienda:

Contar con suficiente espacio de almacenamiento en el dispositivo.
Instalar correctamente ASISGRU.
Abrir la aplicación y verificar que funcione correctamente.
Registrar primero la información general del grupo.
Mantener actualizada la información de participantes y actividades.
6. INICIO DE LA APLICACIÓN

Al abrir ASISGRU, el usuario podrá acceder a las diferentes opciones disponibles mediante el menú de navegación.

La aplicación está organizada mediante diferentes módulos, cada uno destinado a una función específica.

Los principales módulos son:

Configuración del grupo
Participantes
Categorías
Actividades
Registro de asistencia
Créditos

Cada módulo permite administrar una parte específica de la información utilizada por ASISGRU.

7. MÓDULO DE CONFIGURACIÓN DEL GRUPO
7.1 Descripción

El módulo Configuración del grupo permite registrar la información general correspondiente al grupo que utilizará ASISGRU.

Esta sección debe ser configurada antes de comenzar a utilizar las demás funciones de la aplicación.

7.2 Registrar la información del grupo

Para configurar el grupo:

Ingrese al módulo Configuración del grupo.
Se mostrará el formulario correspondiente.
Complete los campos solicitados.
Revise que la información ingresada sea correcta.
Presione el botón Guardar.

Después de guardar la información, los datos registrados podrán visualizarse dentro de la sección correspondiente.

7.3 Editar la configuración

Si posteriormente se necesita modificar algún dato del grupo:

Ingrese nuevamente a Configuración del grupo.
Seleccione la opción Editar configuración.
Modifique los datos que sean necesarios.
Revise la información.
Presione Guardar.

La información actualizada será mostrada nuevamente en la sección de configuración.

8. MÓDULO DE PARTICIPANTES
8.1 Descripción

El módulo Participantes permite administrar las personas que forman parte del grupo.

Desde esta sección se pueden registrar nuevos participantes y consultar los participantes que ya se encuentran registrados.

8.2 Registrar un participante

Para agregar un nuevo participante:

Ingrese al módulo Participantes.
Presione el botón + Nuevo participante.
Complete los datos solicitados.
Revise la información ingresada.
Presione Guardar.

Una vez guardado, el participante aparecerá en el listado correspondiente.

8.3 Buscar participantes

La aplicación permite localizar participantes mediante la búsqueda por nombre o apellido.

Para realizar una búsqueda:

Ingrese al módulo Participantes.
Ubique el campo de búsqueda.
Escriba el nombre o apellido del participante.
Revise los resultados mostrados.

Esto permite encontrar rápidamente a una persona sin necesidad de revisar manualmente todo el listado.

8.4 Filtrar participantes

El módulo permite organizar la visualización de participantes mediante filtros.

Las opciones disponibles son:

Activos
Inactivos
Todos

El usuario puede seleccionar el filtro que necesite para mostrar únicamente la información correspondiente.

8.5 Editar un participante

Para modificar la información de un participante:

Localice al participante en el listado.
Seleccione la opción correspondiente para editar.
Modifique la información necesaria.
Revise los datos.
Guarde los cambios.
8.6 Evitar participantes duplicados

ASISGRU incorpora una validación para evitar registrar dos veces a un participante con el mismo nombre completo.

La aplicación considera como iguales los nombres aunque se escriban utilizando diferentes mayúsculas o minúsculas y también considera los espacios innecesarios al principio o al final.

Esto ayuda a mantener organizado el registro de participantes.

9. MÓDULO DE CATEGORÍAS
9.1 Descripción

El módulo Categorías permite crear categorías que posteriormente pueden utilizarse para organizar las actividades del grupo.

Las categorías ayudan a mantener una clasificación ordenada de las diferentes actividades.

9.2 Crear una categoría

Para crear una categoría:

Ingrese al módulo Categorías.
Seleccione la opción para crear una nueva categoría.
Escriba el nombre de la categoría.
Complete la descripción correspondiente.
Revise la información.
Presione Guardar.

La categoría quedará registrada y podrá utilizarse posteriormente en las actividades.

9.3 Validación de categorías repetidas

ASISGRU cuenta con una validación para evitar que se registren categorías con el mismo nombre.

Por ejemplo, si ya existe una categoría llamada “Reuniones”, el sistema evita que se registre nuevamente otra categoría con el mismo nombre, aunque se escriba utilizando mayúsculas, minúsculas o espacios adicionales.

Esta función permite mantener una organización adecuada de las categorías.

10. MÓDULO DE ACTIVIDADES
10.1 Descripción

El módulo Actividades permite registrar las actividades que serán realizadas por el grupo.

Cada actividad puede relacionarse con una categoría y contener información como fecha y hora.

10.2 Registrar una actividad

Para registrar una nueva actividad:

Ingrese al módulo Actividades.
Seleccione la opción para crear una nueva actividad.
Escriba el nombre o información correspondiente de la actividad.
Seleccione la categoría correspondiente.
Establezca la fecha.
Establezca la hora cuando corresponda.
Revise la información.
Presione Guardar.

Una vez guardada, la actividad aparecerá en el listado correspondiente.

10.3 Administración de actividades

Las actividades registradas pueden ser administradas desde el mismo módulo.

El usuario debe revisar la información de cada actividad antes de realizar el registro de asistencia, especialmente la fecha y actividad seleccionadas.

11. MÓDULO DE REGISTRO DE ASISTENCIA
11.1 Descripción

El módulo Registro de asistencia es una de las funciones principales de ASISGRU.

Permite seleccionar una actividad y registrar cuáles de los participantes estuvieron presentes.

11.2 Registrar asistencia

Para registrar la asistencia:

Ingrese al módulo Registro de asistencia.
Seleccione la actividad correspondiente.
Se mostrará el listado de participantes.
Seleccione a los participantes que asistieron.
Revise que la selección sea correcta.
Guarde el registro de asistencia.

El sistema asociará el registro realizado con la actividad seleccionada.

11.3 Importancia de seleccionar correctamente la actividad

Antes de guardar una asistencia es importante verificar que se haya seleccionado la actividad correcta.

Se recomienda revisar:

Nombre de la actividad.
Fecha.
Hora, cuando corresponda.
Participantes seleccionados.

Esto ayuda a evitar registros incorrectos.

12. CONSULTA Y ORGANIZACIÓN DE LA INFORMACIÓN

ASISGRU organiza la información mediante diferentes módulos relacionados entre sí.

La información general del grupo se encuentra en Configuración del grupo.

Los integrantes se administran desde Participantes.

Las clasificaciones de las actividades se encuentran en Categorías.

Las actividades programadas se registran desde Actividades.

Finalmente, la participación de los integrantes se registra mediante Registro de asistencia.

Esta organización permite que el usuario pueda encontrar la información de manera más sencilla y mantener un control ordenado.

13. RECOMENDACIONES PARA EL USO DE ASISGRU

Para obtener un funcionamiento adecuado de la aplicación se recomienda:

Registrar correctamente la información del grupo.
Verificar los datos antes de guardarlos.
Evitar registrar información duplicada.
Mantener actualizada la información de los participantes.
Utilizar categorías claras para organizar las actividades.
Verificar la fecha y hora antes de registrar una actividad.
Seleccionar correctamente la actividad antes de registrar asistencia.
Revisar los participantes seleccionados antes de guardar un registro.
Mantener disponible el dispositivo donde se encuentra instalada la aplicación.
14. SOLUCIÓN DE PROBLEMAS BÁSICOS
La información no aparece

Verifique que los datos hayan sido guardados correctamente. También puede salir del módulo y volver a ingresar para comprobar la información registrada.

No puedo registrar un participante

Revise que los campos requeridos hayan sido completados y compruebe que no exista previamente un participante con el mismo nombre.

No puedo registrar una categoría

Compruebe que el nombre de la categoría no se encuentre registrado anteriormente.

No encuentro un participante

Utilice el campo de búsqueda escribiendo correctamente su nombre o apellido. También revise el filtro seleccionado, ya que el participante podría encontrarse como activo o inactivo.

No encuentro una actividad

Revise el módulo Actividades y compruebe que la actividad haya sido registrada correctamente.

La asistencia no corresponde a la actividad

Revise la actividad seleccionada antes de guardar el registro. Es importante seleccionar la actividad correcta para evitar asociar la asistencia a una actividad diferente.

15. MÓDULO DE CRÉDITOS

El módulo Créditos contiene información relacionada con el desarrollo de ASISGRU.

En esta sección se puede consultar:

Información general de ASISGRU.
Equipo desarrollador.
Institución educativa.
Tecnologías utilizadas.
Información relacionada con consultas y soporte técnico.

También se encuentra la referencia correspondiente a Recurso Soporte para cuestiones de soporte técnico.

16. CONCLUSIÓN

ASISGRU es una aplicación desarrollada con el propósito de facilitar el control y registro de asistencia de los integrantes de un grupo en sus diferentes actividades.

Mediante sus diferentes módulos, el usuario puede organizar la información general del grupo, administrar participantes, crear categorías, registrar actividades y llevar un control de asistencia.

El uso adecuado de cada módulo permite mantener la información organizada y facilita el seguimiento de la participación de los integrantes.

Este manual tiene como finalidad servir como guía para que el usuario pueda conocer las principales funciones de ASISGRU y utilizarlas correctamente.

La aplicación fue desarrollada utilizando tecnologías como C#, .NET 10, .NET MAUI, Blazor, Visual Studio 2026 y SQLite, permitiendo crear una solución móvil enfocada en la administración local de la información.

17. SOPORTE TÉCNICO

Para consultas o requerimientos relacionados con soporte técnico, se puede contactar a:

Recurso Soporte

Recurso Soporte

📑 Orden final del manual

Para que no se te desordene cuando lo pases a Word, yo usaría este orden:

Portada
↓
Introducción
↓
Objetivo del manual
↓
Objetivo de ASISGRU
↓
Requisitos
↓
Inicio de la aplicación
↓
Configuración del grupo
↓
Participantes
↓
Categorías
↓
Actividades
↓
Registro de asistencia
↓
Consulta y organización de información
↓
Recomendaciones
↓
Solución de problemas
↓
Créditos
↓
Conclusión
↓
Soporte técnico

Y aquí sí te recomiendo algo: para que realmente parezca un manual de usuario y no solamente un documento escrito, en cada módulo podemos colocar una captura de pantalla de ASISGRU + una explicación debajo, con números señalando dónde debe hacer clic el usuario. Eso le va a dar muchísimo más aspecto de manual profesional.
