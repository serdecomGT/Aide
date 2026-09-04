# Cuestionario: Motor de Base de Datos SQLite

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---

## Sección A — Conocimientos generales

1. ¿Qué es SQLite y quién lo desarrolló?
2. ¿En qué año aproximadamente se creó SQLite y cuál fue su objetivo principal?
3. ¿Qué significa que SQLite sea una base de datos **embebida** (*embedded*)?
4. ¿SQLite es un sistema de gestión de bases de datos relacional (RDBMS) o no relacional? Justifica tu respuesta.
5. ¿Cuál es la diferencia fundamental entre SQLite y sistemas como MySQL, PostgreSQL o SQL Server?
6. ¿SQLite requiere un servidor para funcionar? Explica por qué.

## Sección B — Características y arquitectura

7. ¿Cómo se almacenan los datos en SQLite? ¿Utiliza archivos o mantiene todo en memoria?
8. ¿Qué extensión de archivo tiene normalmente una base de datos SQLite?
9. ¿Qué significa que SQLite sea **serverless** (sin servidor)?
10. ¿Qué significa que SQLite use **tipado dinámico** (*type affinity*) en lugar de tipado estricto como otros motores SQL?
11. ¿SQLite soporta transacciones? ¿Qué propiedades ACID cumple? Explica cada una brevemente.
12. ¿Cuáles son las limitaciones principales de SQLite frente a motores de bases de datos cliente-servidor?

## Sección C — SQL básico en SQLite

13. ¿Qué es SQL y cuál es su relación con SQLite?
14. ¿Cómo se crea una base de datos nueva en SQLite desde la línea de comandos?
15. Escribe la sentencia SQL para crear una tabla llamada `Estudiantes` con los campos: `Id` (entero, clave primaria), `Nombre` (texto), `Edad` (entero) y `Correo` (texto).
16. Escribe la sentencia SQL para insertar un registro en la tabla `Estudiantes`.
17. Escribe la sentencia SQL para consultar todos los registros de la tabla `Estudiantes` donde la edad sea mayor a 18.
18. ¿Cuál es la diferencia entre `DELETE` y `DROP TABLE`?
19. ¿Qué es una clave primaria (*PRIMARY KEY*) y por qué es importante?
20. ¿Qué es una clave foránea (*FOREIGN KEY*)? SQLite soporta claves foráneas por defecto o hay que activarlas. ¿Sabes cómo?

## Sección D — Operaciones y conceptos intermedios

21. ¿Qué es el comando `.tables` en el intérprete de línea de comandos de SQLite?
22. ¿Qué es el comando `.schema` y para qué sirve?
23. ¿Cómo se actualiza un registro existente en una tabla? Escribe un ejemplo.
24. ¿Qué son los índices (*INDEX*) en SQLite y cuándo son útiles?
25. ¿Qué es una consulta `JOIN`? Describe con un ejemplo sencillo la diferencia entre `INNER JOIN` y `LEFT JOIN`.
26. ¿Qué es `AUTOINCREMENT` en SQLite y cómo funciona? ¿Es igual que en otros motores de bases de datos?

## Sección E — Uso práctico en el ecosistema de desarrollo

27. ¿Has utilizado SQLite dentro de alguna aplicación? Si es así, describe con qué tecnología o lenguaje.
28. ¿Cómo se integra SQLite en una aplicación .NET (C#, MAUI o Blazor)? ¿Conoces alguna librería o ORM para ello?
29. ¿Qué es un ORM (*Object-Relational Mapping*)? ¿Has oído hablar de Entity Framework o Dapper en relación con SQLite?
30. ¿En qué tipo de proyectos o situaciones considerarías que SQLite es la mejor opción?
31. ¿SQLite es adecuado para aplicaciones web con miles de usuarios concurrentes? Justifica tu respuesta.

## Sección F — Herramientas y exploración

32. ¿Conoces alguna herramienta gráfica (GUI) para administrar bases de datos SQLite? Menciona al menos una.
33. ¿Puedes abrir y explorar un archivo de base de datos SQLite con un editor de texto común? ¿Por qué sí o por qué no?
34. ¿SQLite se puede usar desde la línea de comandos? ¿Qué comando ejecutarías para abrir una base de datos existente?

## Sección G — Pregunta reflexiva

35. ¿Por qué crees que SQLite es uno de los motores de bases de datos más utilizados en el mundo a pesar de no ser un sistema cliente-servidor? ¿En qué situaciones lo considerarías ideal y en cuáles no?
