Plan de Documentación — App AsisGru

Versión: 0.1 (borrador inicial) Producto: AsisGru — Control de asistencia de integrantes de un grupo a sus actividades Stack: C# · .NET MAUI · Blazor (Blazor Hybrid) · SQLite (100% local y off-line)

1. Introducción
1.1 Propósito

Definir qué documentos se producirán durante el ciclo de vida de AsisGru, su contenido mínimo, audiencia, formato, responsables y momento de elaboración. El plan busca que cualquier persona (desarrollador nuevo, maintainer, usuario) pueda entender, mantener, operar y usar la App sin conocimiento tribal.

1.2 Alcance

Cubre la documentación desde el análisis de requisitos hasta la operación y soporte, incluyendo la documentación del código fuente y de la base de datos local.

1.3 Audiencias
Audiencia	Necesidad principal
Equipo de desarrollo	Arquitectura, convenciones, decisiones técnicas
QA / pruebas	Casos de prueba, criterios de aceptación
Instalador / operador	Instalación, respaldo, solución de problemas
Usuario final (gestor del grupo)	Manual de uso de la App
Mantenidores futuros	Código documentado, ADRs, esquema de datos
1.4 Referencias
ISO/IEC/IEEE 26512 y 26513 (documentación para desarrolladores y usuarios).
Markdown como formato universal; DocFX para documentación de API generada.
SemVer para versionado de la App y su documentación.
2. Contexto del producto (resumen a documentar)

AsisGru es una aplicación móvil que funciona en local y sin conexión, permitiendo:

Gestionar uno o más grupos y sus integrantes.
Definir actividades del grupo (con fecha, hora, lugar, tipo).
Registrar la asistencia de cada integrante a cada actividad (estados: presente, ausente, tardanza, justificado).
Consultar históricos, porcentajes de asistencia y exportar reportes (CSV/PDF).
Configurar parámetros locales (umbral de inasistencias, datos del grupo, respaldo).

Entidades del dominio a documentar: Grupo, Miembro, Actividad, TipoActividad, RegistroAsistencia, EstadoAsistencia, Configuracion, AuditoriaCambios (opcional).

Decisiones técnicas clave que deberán quedar registradas en ADRs:

ADR-001: Uso de Blazor Hybrid dentro de MAUI (UI web compartible) vs. XAML nativo.
ADR-002: Acceso a datos: EF Core + SQLite vs. sqlite-net-pcl.
ADR-003: Estrategia off-line pura en v1 (sin sincronización) y punto de extensión futuro.
ADR-004: Cifrado de la base local (SQLCipher) y protección de datos personales de los integrantes.
ADR-005: Estrategia de respaldo/restauración (exportar archivo de BD).
ADR-006: Gestión de estado compartido en Blazor (servicios DI, Microsoft.AspNetCore.Components).
3. Estructura del repositorio documental

text

/asisgru

├── docs/

│ ├── 00-plan/ # Plan de proyecto y de documentación

│ ├── 01-requisitos/

│ ├── 02-arquitectura/ # SAD, diagramas, ADRs

│ ├── 03-diseno/ # UI/UX, flujos, wireframes

│ ├── 04-datos/ # Esquema SQLite, migraciones, diccionario

│ ├── 05-desarrollo/ # Guías, convenciones, CI/CD

│ ├── 06-pruebas/

│ ├── 07-despliegue/

│ ├── 08-operacion/

│ ├── 09-usuario/

│ ├── plantillas/ # Plantillas de documentos y ADR

│ └── _img/ # Imágenes compartidas

├── src/ # Código con XML comments

└── README.md

4. Inventario de documentos

Leyenda de columnas: Código (identificador de versión documental), Contenido mínimo, Audiencia, Etapa (momento de elaboración/actualización).

4.1 Gestión del proyecto
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-GES-01	Plan de proyecto	Alcance, hitos, recursos, riesgos	Equipo	Inicio
DOC-GES-02	Plan de documentación (este documento)	Inventario, estándares, flujo	Todos	Inicio, revisión periódica
DOC-GES-03	Registro de riesgos	Riesgo, impacto, mitigación	Equipo	Continuo
DOC-GES-04	Registro de decisiones (ADRs)	Contexto, decisión, consecuencias	Desarrollo	Por cada decisión
DOC-GES-05	Changelog / notas de versión	Cambios por versión (SemVer)	Todos	Cada release
4.2 Requisitos
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-REQ-01	Visión y alcance	Problema, usuarios, límites, supuestos	Todos	Inicio
DOC-REQ-02	Especificación de requisitos (SRS)	RF-xx funcionales (ABML grupos, miembros, actividades, registro de asistencia, reportes, respaldo) y RNF-xx (off-line, rendimiento, privacidad, tamaño de BD)	Dev, QA	Análisis
DOC-REQ-03	Historias de usuario + criterios de aceptación	Formato "Como [gestor del grupo] quiero…"	Dev, QA	Análisis/sprints
DOC-REQ-04	Matriz de trazabilidad	RF ↔ casos de uso ↔ pruebas ↔ código	QA	Continuo
DOC-REQ-05	Reglas de negocio	Ej.: cálculo de % de asistencia, umbral de inasistencias, gestión de miembros dados de baja	Dev, QA	Análisis
4.3 Arquitectura y diseño
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-ARQ-01	Documento de arquitectura (SAD)	Vista lógica (capas: UI Blazor, servicios, datos), vista de despliegue en dispositivo, dependencias NuGet	Dev	Diseño
DOC-ARQ-02	Diagramas C4 / UML	Contexto, contenedores (MAUI shell, Blazor WebView, SQLite), componentes, secuencias clave (registrar asistencia)	Dev	Diseño
DOC-ARQ-03	Diseño de UI/UX	Flujos de navegación (Shell/rutas Blazor), wireframes, mockups, guía visual (colores, tipografía), estados vacíos y de error	Dev, usuario	Diseño
DOC-ARQ-04	Modelo de dominio	Diagrama de clases de entidades y servicios de dominio	Dev	Diseño
DOC-ARQ-05	Plantillas ADR individuales	Una por decisión (ver §2)	Dev	Por decisión
4.4 Datos (SQLite)
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-DAT-01	Esquema de base de datos	Diagrama ER, DDL, índices, claves foráneas, restricciones	Dev	Diseño
DOC-DAT-02	Diccionario de datos	Tabla por entidad: campo, tipo, nulabilidad, significado, valores de EstadoAsistencia	Dev, QA	Diseño
DOC-DAT-03	Estrategia de migraciones	Herramienta, versión del esquema por versión de App, scripts	Dev	Por release
DOC-DAT-04	Respaldo y restauración	Formato del respaldo, procedimiento desde la App y manual, verificación de integridad	Operador	Diseño/op.
DOC-DAT-05	Privacidad y protección de datos	Datos personales almacenados localmente, retención, borrado seguro (desvinculación de miembro), consideraciones legales	Todos	Análisis
4.5 Desarrollo
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-DEV-01	Guía de configuración del entorno	SDK .NET, workload MAUI, emuladores/dispositivos, IDE, pasos "de cero a correr la App"	Dev	Inicio
DOC-DEV-02	Convenciones de código C#	Estilo (editorconfig), nomenclatura, organización de proyectos/solution, inyección de dependencias	Dev	Inicio
DOC-DEV-03	Guía de componentes Blazor	Catálogo de componentes reutilizables (tarjeta de miembro, selector de fecha, badge de estado), props, cuándo reutilizar	Dev	Continuo
DOC-DEV-04	Estándares de documentación de código	XML comments obligatorios en APIs públicas, README por proyecto de la solution	Dev	Continuo
DOC-DEV-05	Guía de control de versiones	Ramas (main/develop/feature), mensajes de commit, revisión de PRs, vinculación con RF/historias	Dev	Inicio
DOC-DEV-06	Guía de manejo de errores y logging	Registro local de errores, niveles, dónde se consultan los logs en dispositivo	Dev	Desarrollo
DOC-DEV-07	Guía de CI/CD	Pipeline de build (Android/Windows/iOS), análisis estático, artefactos	Dev	Desarrollo
4.6 Calidad y pruebas
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-QA-01	Plan de pruebas	Alcance, niveles (unitarias xUnit, integración con SQLite, UI con Appium/maui-test), entorno	QA, Dev	Antes de probar
DOC-QA-02	Casos de prueba	ID, precondición, pasos, esperado, RF vinculado; casos críticos: registro masivo de asistencia, integridad tras cierre abrupto, BD corrupta	QA	Desarrollo
DOC-QA-03	Registro de defectos	Plantilla de bug, severidad, estado	Todos	Continuo
DOC-QA-04	Informe de resultados por release	Cobertura, defectos abiertos, criterio de salida	Todos	Por release
4.7 Despliegue y distribución
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-DES-01	Guía de build y empaquetado	Comandos, configuraciones Debug/Release, firma (keystore Android, certificados iOS/MSIX)	Dev	Pre-release
DOC-DES-02	Guía de distribución	Opciones: tienda, instalación directa de APK (side-load) para grupos sin tienda, actualización de versiones y migración de BD existente	Operador	Pre-release
DOC-DES-03	Checklist de release	Pasos verificables antes de publicar una versión	Dev	Por release
4.8 Operación y soporte
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-OP-01	Manual de instalación	Requisitos del dispositivo (SO, memoria), pasos de instalación, primera configuración	Operador	Release
DOC-OP-02	Manual de operación	Rutinas periódicas: respaldo, verificación de espacio, exportación de reportes	Operador	Release
DOC-OP-03	Guía de solución de problemas	Tabla síntoma → causa → acción (App no abre, BD corrupta, respaldo fallido, datos no visibles)	Operador	Release, continuo
DOC-OP-04	Procedimiento de recuperación ante fallos	Restauración desde respaldo, escenario de pérdida de dispositivo	Operador	Release
4.9 Usuario final
Código	Documento	Contenido mínimo	Audiencia	Etapa
DOC-USU-01	Manual de usuario	Por pantalla: grupos, miembros, actividades, registro de asistencia, reportes; con capturas	Usuario final	Release
DOC-USU-02	Guía rápida (1 página)	Flujo esencial: crear grupo → cargar miembros → crear actividad → pasar asistencia	Usuario final	Release
DOC-USU-03	FAQ	Dudas comunes (respaldo, cambio de dispositivo, estados de asistencia)	Usuario final	Post-release
5. Estándares de redacción
Formato: Markdown (diagramas en Mermaid o Draw.io exportados a _img/).
Encabezado obligatorio en cada documento: título, código, versión, fecha, autor, estado (borrador/revisión/aprobado).
Idioma: español; código e identificadores en inglés.
Numeración de requisitos: RF-###, RNF-###; de casos de prueba: TC-###; de ADRs: ADR-###.
Toda captura de pantalla del manual de usuario debe indicar versión de la App con la que se tomó.
6. Documentación del código fuente
XML comments (///) obligatorios en clases y métodos públicos de servicios y entidades.
DocFX configurado para generar el sitio de documentación de API desde src/.
README.md por proyecto de la solution (propósito, dependencias, puntos de entrada).
Los comentarios explican el porqué, no el qué.
7. Herramientas
Necesidad	Herramienta propuesta
Repositorio y versionado de docs	Git (mismo repo que el código)
API docs	DocFX
Diagramas	Mermaid / Draw.io
Diseño UI	Figma o similar
Gestión de tareas/defectos	GitHub Projects / Azure DevOps / Jira
Revisión de docs	Pull requests con revisor designado
8. Roles y responsabilidades (RACI)
Actividad	Responsable	Consultado
Plan de documentación	Líder técnico	Equipo
SRS y reglas de negocio	Analista / PO	Usuario clave del grupo
SAD y ADRs	Arquitecto / Líder técnico	Equipo dev
Documentos de datos	Dev backend/datos	QA
Casos de prueba	QA	Dev
Manuales de operación	Dev senior	Operador
Manual de usuario	Técnico documental / PO	Usuario final
Revisión y aprobación	Líder técnico	—

(Ajustar según el tamaño real del equipo; en equipos pequeños una persona puede acumular roles.)

9. Flujo de trabajo documental
Creación a partir de plantilla (carpeta plantillas/).
Revisión por par mediante PR.
Aprobación del responsable.
Publicación en docs/ (y generación del sitio DocFX si aplica).
Actualización obligatoria ante: cambio de requisito, ADR nuevo, release, defecto relevante. La documentación desactualizada se trata como defecto.
10. Alineación con el ciclo de vida
Fase	Documentos que se elaboran/actualizan
Inicio	DOC-GES-01/02, DOC-REQ-01, ADR-001…006
Análisis	DOC-REQ-02…05, DOC-DAT-05
Diseño	DOC-ARQ-01…04, DOC-DAT-01/02, DOC-DEV-02
Desarrollo	DOC-DEV-03…07, DOC-QA-01/02, DOC-DAT-03, código documentado
Pruebas	DOC-QA-02…04
Release	DOC-DES-01…03, DOC-OP-01…04, DOC-USU-01…03, DOC-GES-05
Operación/mantenimiento	DOC-OP-03, FAQ, ADRs nuevos, changelog
11. Métricas de calidad documental (sugeridas)
% de requisitos con al menos un caso de prueba trazado.
% de ADRs con estado "aceptado" para decisiones mayores.
Revisión documental incluida en la definición de "terminado" (DoD) de cada historia.
Verificación del manual de usuario en cada release mayor (capturas vigentes).
12. Próximos pasos sugeridos
Validar y priorizar este inventario según el tamaño del equipo (podría recortarse a un conjunto mínimo esencial).
Crear las plantillas de: ADR, SRS, caso de prueba, encabezado de documento.
Elaborar primero: DOC-REQ-01, DOC-REQ-02, ADR-001…003 y DOC-DEV-01, que desbloquean el resto.
