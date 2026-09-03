# Cuestionario: Git — Control de Versiones

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---


## Sección A — Conocimientos generales

1. ¿Qué es un sistema de control de versiones (VCS) y por qué es importante?
   
Es como una "máquina del tiempo" para nuestros archivos. Guarda cada cambio que hacemos, quién lo hizo y cuándo. Si nos equivocamos o algo se daña, podemos volver a una versión anterior sin perder nada. También permite que varias personas trabajen en el mismo proyecto sin estorbarse.

3. ¿Quién creó Git y en qué año?
   
Lo creó Linus Torvalds, el mismo que hizo el sistema operativo Linux, en el año 2005.

4. ¿Cuál es la diferencia entre Git y GitHub?

* Git es el programa que se instala en tu computadora para llevar el control de los cambios.

* GitHub es una página web donde se guardan esos proyectos en internet para que otras personas los vean, los descarguen o trabajen juntos. Git es la herramienta; GitHub es el lugar donde se comparten los proyectos.

4. ¿Qué es un repositorio (repository) en Git?
   
Es la carpeta principal del proyecto donde Git guarda todo: los archivos y el historial de todos los cambios que se han hecho. Puede estar guardado solo en tu computadora o también en internet.

6. ¿Git es un sistema distribuido o centralizado? ¿Qué implica eso?
   
Es distribuido. Esto significa que cada persona que trabaja en el proyecto tiene una copia completa del historial en su propia computadora. No todo depende de un solo servidor; si uno falla, las copias de los demás siguen funcionando.

## Sección B — Comandos básicos

7. ¿Qué hace el comando git init?
   
Prepara una carpeta para que Git empiece a llevarle el control. Crea los archivos necesarios para que Git empiece a registrar los cambios. Se usa la primera vez que empezamos un proyecto nuevo.

8. ¿Qué hace git clone? ¿Cuándo lo usarías?
   
Descarga una copia completa de un proyecto que ya existe en internet y la guarda en tu computadora. Lo usas cuando vas a trabajar en algo que alguien más ya empezó y quieres tener todo en tu equipo.

9. Explica el flujo: git add → git commit → git push. ¿Qué hace cada paso?

* git add: selecciona los archivos que están listos para guardar. Los pone en "la lista de espera".

* git commit: guarda los cambios definitivamente con un mensaje que dice qué se modificó. Ya queda registrado en el historial.

* git push: envía todos esos cambios guardados a la versión que está en internet, así los demás los pueden ver.

9. ¿Qué es el staging area (área de preparación)?
    
Es como una "sala de espera". Antes de guardar los cambios para siempre, los agregamos ahí para revisar qué vamos a guardar y qué no. Así podemos elegir exactamente qué archivos van en la siguiente versión.

11. ¿Cuál es la diferencia entre git pull y git fetch?

* git pull: descarga los cambios nuevos que otros hicieron y los mezcla de inmediato con tus archivos.

* git fetch: solo descarga los cambios nuevos pero no los mezcla todavía; tú los revisas primero y decides cuándo unirlos.

11. ¿Qué hace git status y por qué es útil?
    
Te dice en qué estado está todo: qué archivos cambiaron, cuáles están en la sala de espera y si hay cosas que todavía no has guardado. Sirve para no perderte y saber qué sigue.

## Sección C — Ramas y colaboración

13. ¿Qué es una rama (branch) en Git y para qué se utiliza?
    
Es como una "línea de tiempo" separada. Sirve para trabajar en algo nuevo sin estorbar lo que ya funciona. Por ejemplo, puedes crear una rama para diseñar el menú y otra para arreglar un error, sin que se mezclen antes de tiempo.

15. ¿Cómo se crea y cambia a una nueva rama? Escribe los comandos.

* Para crearla: git branch nombre-de-la-rama

* Para cambiarte a ella: git checkout nombre-de-la-rama

* O más fácil, crea y cambia de una vez: git checkout -b nombre-de-la-rama

14. ¿Qué es un merge (fusión) y cuándo se realiza?
    
Es cuando unes los cambios de una rama a otra. Por ejemplo, cuando ya terminaste de trabajar en una parte nueva, la unes a la rama principal para que ya forme parte del proyecto completo.

16. ¿Qué es un conflicto de fusión y cómo se resuelve?
    
Pasa cuando dos personas cambiaron la misma línea de un archivo de forma distinta y Git no sabe cuál elegir. Entonces te avisa y tú tienes que abrir el archivo, decidir cuál versión se queda, borrar las marcas que sobran y volver a guardar y hacer commit.

17. ¿Qué es un pull request (PR) en GitHub y cuál es su propósito?
    
Es cuando terminas de trabajar en una rama y pides permiso para unirla a la principal. Sirve para que otras personas revisen tus cambios, dejen comentarios y aprueben si todo está bien antes de que se mezcle definitivamente.

## Sección D — Conceptos intermedios

18. ¿Qué es un archivo .gitignore y para qué sirve? Da un ejemplo.
    
Es un archivo donde escribes los nombres de cosas que Git no debe guardar. Por ejemplo, contraseñas, archivos pesados que no cambian, o carpetas que se generan solas. Así no se suben cosas que no le sirven a nadie o que pueden ser peligrosas.

20. ¿Qué es un commit y qué información debe tener un buen mensaje?
    
Es como una "foto" de los cambios en ese momento. Un buen mensaje dice claramente qué se hizo y por qué. Por ejemplo: "Agregado formulario de contacto" o "Corregido error en el cálculo del total". Así después se entiende el historial sin adivinar.

21. ¿Qué es git log y qué información te muestra?
    
Te muestra el historial completo de todos los cambios guardados: quién hizo cada uno, cuándo, el mensaje que escribió y un código único para identificar cada versión. Sirve para ver cómo ha avanzado el proyecto.

22. ¿Qué es un fork en GitHub y cómo se diferencia de un clone?

* clone = descargas una copia del proyecto en tu computadora para trabajar.

* fork = haces una copia del proyecto dentro de tu propia cuenta de GitHub. Así puedes experimentar sin afectar el original y luego proponer tus cambios al dueño con un pull request.
  
## Sección E — Pregunta reflexiva

21. Imagina que trabajas con dos compañeros. ¿Cómo usarías Git y GitHub para colaborar sin perder el trabajo?

Primero creamos un proyecto en GitHub y cada uno se lo descarga a su computadora. Cada quien trabaja en su propia rama: uno en el diseño, otro en los datos y otro en las funciones. Cuando terminan, suben su rama y hacen un pull request para que los demás revisen antes de unirlo a la versión principal. Así nadie se escribe encima del trabajo de otro y todo se puede arreglar si algo sale mal. Si alguien se equivoca, siempre se puede volver a una versión anterior.
¿Quieres que lo deje más corto o así está bien? 😊
