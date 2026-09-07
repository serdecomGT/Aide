# Cuestionario: Motor de Base de Datos SQLite

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---

# Sección A — Conocimientos generales

1. ¿Qué es SQLite y quién lo desarrolló

SQLite es un sistema de gestión de bases de datos relacionales, ligero, sin servidor y autocontenido. Fue creado por D. Richard Hipp.

3. ¿En qué año se creó y cuál fue su objetivo principal?
   
El proyecto comenzó en mayo de 2000, con su primer lanzamiento oficial el 17 de agosto de 2000. Su objetivo era ser un motor de base de datos que no requiriera configuración ni servidor, para integrarlo directamente en programas y dispositivos.

4. ¿Qué significa que sea una base de datos "embebida"?
Que no funciona como un programa aparte al que se conecta, sino que se integra directamente dentro del código de la aplicación. No hay un servidor separado; todo funciona junto con el programa.

5. ¿Es un sistema relacional (RDBMS) o no relacional?
   
Sí, es relacional. Utiliza tablas, filas, columnas y el lenguaje SQL estándar, igual que MySQL o PostgreSQL.

6. Diferencia con MySQL, PostgreSQL o SQL Server
   
SQLite no tiene servidor — todo se guarda en un solo archivo. Los otros son cliente-servidor: requieren un programa servidor instalado aparte al que se conectan varios usuarios al mismo tiempo.

7. ¿Requiere servidor? ¿Por qué?
   
No. El motor funciona como parte de tu propia aplicación. Lee y escribe directamente en un archivo, sin procesos externos.


📌 Sección B — Características y arquitectura

8. ¿Cómo se almacenan los datos?
   
Todo se guarda en un solo archivo en el disco duro. No se guarda en memoria de forma permanente.

9. ¿Qué extensión tiene el archivo
   
Las más comunes son: .db, .sqlite, .db3. La extensión no es obligatoria, pero es la convención.

10. ¿Qué significa "serverless"?
    
Que no hay un servidor que administre la base de datos. No hay que iniciar, detener o configurar ningún servicio.

11. ¿Qué es "tipado dinámico"?
    
Que no se exige que el dato coincida estrictamente con el tipo declarado en la columna. Puedes guardar un texto en un campo numérico, por ejemplo. Otros motores son más estrictos.

12. ¿Soporta transacciones? ¿Qué propiedades ACID cumple?
Sí, completamente.

* Atomicidad: la transacción se completa toda o nada.

* Consistencia: la base pasa de un estado válido a otro.

* Isolation: transacciones simultáneas no se interfieren.

* Durabilidad: si se confirma, se queda aunque falle el sistema.

12. Limitaciones frente a motores cliente-servidor

* Solo un proceso puede escribir a la vez.

* No tiene administración de usuarios ni permisos.

* No escala tan bien con miles de conexiones simultáneas.

* Menos funciones avanzadas.

  
  # Sección C — SQL básico

13. ¿Qué es SQL y su relación con SQLite?
    
SQL es el lenguaje estándar para bases de datos. SQLite lo usa casi en su totalidad.

15. ¿Cómo crear una base desde la línea de comandos?

Escribe: sqlite3 nombre_base.db — si no existe, se crea automáticamente.

16. Crear tabla "estudiantes"
CREATE TABLE estudiantes (
  id INTEGER PRIMARY KEY,
  nombre TEXT,
  edad INTEGER,
  correo TEXT
);

17. Insertar un registro
INSERT INTO estudiantes (nombre, edad, correo)
VALUES ('Ana', 20, 'ana@correo.com');

18. Consultar todos los registros con edad mayor a 18
SELECT * FROM estudiantes WHERE edad > 18;
19. Diferencia entre DELETE y DROP TABLE

* DELETE borra los datos de la tabla, pero la tabla sigue existiendo.

* DROP TABLE elimina la tabla completa con su estructura.

19. ¿Qué es clave primaria (PRIMARY KEY

Es el campo que identifica de forma única cada registro. No se repite y no puede estar vacío.

20. ¿Qué es clave foránea (FOREIGN KEY)?
    
Es un campo que hace referencia a la clave primaria de otra tabla. Mantiene las relaciones entre datos. SQLite no las activa por defecto; hay que activarlas con: PRAGMA foreign_keys = ON;.

# Sección D — Operaciones e intermedios

22. ¿Qué es el comando .tables?
    
Muestra todas las tablas que existen en la base de datos abierta.

23. ¿Qué es .schema y para qué sirve
    
Muestra la estructura completa de las tablas: campos, tipos, claves, todo lo que se usó para crearlas.

24. Actualizar un registro
UPDATE estudiantes SET edad = 21 WHERE nombre = 'Ana';

25. ¿Qué son los índices (INDEX)?
    
Son como un índice de un libro: ayudan a encontrar datos más rápido. Se usan en campos que buscas mucho, pero ralentizan los cambios.

27. ¿Qué es consulta JOIN? Diferencia INNER y LEFT
    
Sirve para unir datos de dos o más tablas:

* INNER JOIN: solo trae filas que tienen coincidencia en ambas tablas.

* LEFT JOIN: trae todo de la tabla izquierda, aunque no haya coincidencia en la derecha.

26. ¿Qué es AUTOINCREMENT? ¿Funciona igual?

En SQLite, declarar INTEGER PRIMARY KEY ya genera un número automático. AUTOINCREMENT hace algo parecido pero no reutiliza números borrados.

# Sección E — Uso práctico

28. ¿Lo has usado en una app?
    
(Tu experiencia personal) — Se usa mucho en apps móviles, porque viene integrado en Android y iOS.

29. ¿Cómo integrarlo en .NET (C#, MAUI, Blazor)?
    
Usando paquetes como Microsoft.Data.Sqlite o SQLite-net. Se conecta con una cadena de conexión que apunta al archivo.

30. ¿Qué es un ORM? ¿Conoces Entity Framework o Dapper?
    
ORM = Mapeo Objeto-Relacional. Permite trabajar con clases de C# en lugar de escribir SQL manualmente. Entity Framework Core y Dapper son los más usados.

31. ¿En qué proyectos es la mejor opción?

* Apps móviles y de escritorio.

* Sistemas pequeños o medianos sin muchos usuarios a la vez.

* Prototipos y aprendizaje.

31. ¿Sirve para web con miles de usuarios concurrentes?
    
Generalmente no, porque solo admite una escritura a la vez. Para eso se recomienda MySQL o PostgreSQL.

# Sección F — Herramientas

33. ¿Conoces herramientas gráficas (GUI)?
    
Sí: DB Browser for SQLite, SQLiteStudio, DBeaver, VS Code con extensiones.

35. ¿Se puede abrir con un editor de texto común?
    
No. El archivo es binario, no es texto plano. Si lo abres en Notepad se ve con caracteres raros.

37. ¿Se usa desde línea de comandos?
    
Sí. Se escribe sqlite3 nombre_base.db y luego comandos como .tables, .schema, SELECT * FROM tabla;.

# Sección G — Pregunta reflexiva

(Aquí puedes escribir tu propia opinión, por ejemplo:)
SQLite nos enseña que lo más simple puede ser lo más útil. Aunque no sirva para todo, está en más dispositivos del mundo que cualquier otra base de datos, y eso dice mucho de su buen diseño.
