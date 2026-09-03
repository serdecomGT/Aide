# Cuestionario: Lenguaje Markdown

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---


## Sección A — Conocimientos generales

1. ¿Qué es Markdown y para qué fue creado?
   
Es un lenguaje sencillo que sirve para darle formato al texto: poner títulos, negritas, listas, enlaces, imágenes, etc. Se escribió para que sea fácil de leer y de escribir, sin necesidad de usar programas complejos ni ver códigos largos.

3. ¿Quién creó Markdown y en qué año aproximadamente?
   
Lo crearon John Gruber junto con Aaron Swartz, y se publicó por primera vez en el año 2004.

4. ¿Es un lenguaje de programación, de marcado o de estilos? Justifica tu respuesta.
   
Es un lenguaje de marcado, porque se usa para dar estructura y formato al texto, no para crear programas ni calcular cosas. Solo le dice al texto cómo debe verse, no qué debe hacer.

5. Menciona al menos tres plataformas donde se usa Markdown.

* GitHub — para los archivos de información de los proyectos.

* Notion — para tomar notas y organizar información.

* Obsidian — para guardar y conectar apuntes.
  
## Sección B — Sintaxis básica

5. ¿Cómo se escribe un título de nivel 1, nivel 2 y nivel 3 en Markdown?

* Nivel 1: # Título principal

* Nivel 2: ## Título secundario

* Nivel 3: ### Título más pequeño

6. ¿Cuál es la diferencia entre usar *texto* y texto?

* *texto* → pone el texto en negrita.

* texto → pone el texto en cursiva o inclinado.

7. Escribe una lista con tres viñetas (no numeradas).
- Preparar el agua
- Calentar la taza
- Servir el café
8. Escribe una lista numerada con tres pasos para preparar un café.
1. Calentar el agua
2. Colocar el café en la taza
3. Verter el agua caliente y mezclar
9. ¿Cómo se inserta un enlace (hipervínculo) en Markdown? Da un ejemplo.
    
Se pone el texto que se verá entre corchetes y la dirección entre paréntesis:
[Ir a Google](https://www.google.com)
11. ¿Cómo se inserta una imagen en Markdown? ¿En qué se diferencia de un enlace?
    
Se pone igual que el enlace pero con un signo de exclamación al principio:
![Texto si la imagen no carga](imagen.jpg)
La diferencia es que el enlace lleva a otra página, y la imagen se muestra directamente dentro del texto.

## Sección C — Uso práctico en GitHub

12. ¿Qué archivo Markdown es el más importante en un repositorio de GitHub y qué función cumple?
    
El más importante se llama README.md. Es como la "tarjeta de presentación" del proyecto: explica de qué trata, cómo usarlo, cómo instalarlo y quién lo hizo. GitHub lo muestra automáticamente en la página principal del repositorio.

13. ¿Cómo se inserta un bloque de código en Markdown? Muestra un ejemplo con y sin especificar el lenguaje.
Se usan tres acentos graves ``` al principio y al final.

* Sin lenguaje:
function saludar() {
  console.log("Hola");
}
* Con lenguaje:
function saludar() {
  console.log("Hola");
}
13. ¿Cómo se crea una tabla en Markdown? Haz un ejemplo con dos columnas y tres filas.
Se usan guiones y barras verticales:

| Nombre  | Edad |
|---------|------|
| Ana     | 18   |
| Luis    | 19   |
| Marta   | 20   |
14. ¿Puedes usar HTML dentro de un archivo Markdown? Da un ejemplo de cuándo sería útil.

Sí, se puede. Markdown es sencillo, pero si necesitas algo más específico como poner un texto con color, usar una etiqueta de diseño o incrustar algo complejo, puedes escribir HTML directo. Por ejemplo: <span style="color:red;">texto en rojo</span>.

15. ¿Qué extensión de archivo tiene un documento Markdown?

Se guardan con la extensión .md o también .markdown. La más usada es .md.

## Sección D — Pregunta reflexiva
 
17. ¿Por qué crees que GitHub y las comunidades prefieren Markdown sobre Word o PDF?
    
Porque Markdown es muy ligero y se puede abrir en cualquier computadora sin necesidad de programas especiales. El texto se puede leer sin que se desconfigure, se mezcla bien con el código de programación y no pesa casi nada. En cambio, los archivos de Word pueden cambiar de formato al abrirse en otra computadora, y los PDF no se pueden editar fácilmente. Markdown es simple, rápido y universal.
