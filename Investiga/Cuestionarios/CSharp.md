# Cuestionario: Lenguaje de Programación C#

**Nombre del entrevistado:**
**Fecha:**
**Nivel de experiencia:** Principiante

---

## Sección A — Conocimientos generales

1. ¿Quién desarrolló el lenguaje C# y en qué año se lanzó oficialmente?
   
Lo creó Microsoft, dirigido por el programador Anders Hejlsberg. Salió oficialmente en el año 2002 junto con la primera versión de .NET.

3. ¿C# es un lenguaje compilado, interpretado o ambos? Explica brevemente.
   
Es compilado: el código que escribimos se traduce primero a un lenguaje que la computadora entiende, y luego se ejecuta. No se interpreta línea por línea mientras corre, como pasa con otros lenguajes. Por eso suele ser más rápido al ejecutarse.

5. ¿Qué significa que C# sea un lenguaje de tipado estático?
   
Significa que cuando creamos una variable, tenemos que decir de qué tipo es desde el principio (si es número, texto, etc.), y ya no se puede cambiar después. Así el programa detecta errores antes de ejecutarse y todo queda más ordenado.

7. ¿Qué es el framework .NET y cuál es su relación con C#?
   
.NET es como una caja de herramientas y reglas que creó Microsoft. C# es el lenguaje que usamos para darle instrucciones, y .NET es el "motor" que lo hace funcionar y le da acceso a muchas funciones ya listas, como guardar archivos, conectarse a internet o mostrar ventanas.

9. Menciona al menos tres tipos de aplicaciones que se pueden desarrollar con C#.

* Páginas y sistemas web

* Aplicaciones de celular y computadora




## Sección B — Sintaxis y conceptos básicos

6. ¿Cómo se declara una variable de tipo entero en C#? Escribe un ejemplo.
Se pone primero el tipo de dato y luego el nombre. Ejemplo:

int edad = 18;
8. ¿Cuál es la diferencia entre var, int y string al declarar una variable?

* int = es para números enteros.

* string = es para textos o frases.

* var = le decimos al programa que adivine qué tipo es según lo que le pongamos. Si le pones un número, él sabe que es int; si le pones texto, sabe que es string.

8. ¿Qué diferencia hay entre const y readonly?

* const = es un valor fijo que se sabe desde antes de que empiece a correr el programa y ya nunca cambia.

* readonly = su valor se puede definir cuando se crea el objeto, y después ya no se puede cambiar. Es más flexible.

9. Escribe un ejemplo de una estructura condicional if-else en C#.
int nota = 85;
if (nota >= 60)
{
    Console.WriteLine("¡Aprobaste!");
}
else
{
    Console.WriteLine("Reprobaste");
}
10. Escribe un ejemplo de un ciclo for que imprima los números del 1 al 5.
for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);
}
11. ¿Qué es un método en C#? Escribe un ejemplo de un método que reciba dos números y devuelva su suma.
Un método es un bloque de código que hace una tarea específica y se puede reutilizar. Ejemplo:
int Sumar(int numero1, int numero2)
{
    return numero1 + numero2;

    
## Sección C — Programación Orientada a Objetos

12. ¿Qué es una clase en C#? Escribe un ejemplo básico.
Una clase es como un plano o modelo para crear cosas. Dice qué características y qué acciones van a tener. Ejemplo:
class Persona
{
    public string Nombre;
    public int Edad;
}
13. ¿Qué es un objeto y cómo se relaciona con una clase?
    
El objeto es algo real que se crea siguiendo el plano de la clase. Si la clase es el plano de una casa, el objeto es la casa construida. De una sola clase se pueden crear muchos objetos distintos.

15. Explica con tus propias palabras los conceptos de encapsulamiento, herencia y polimorfismo.

* Encapsulamiento: es como guardar los datos y solo dejarlos cambiar por medio de las formas que nosotros decidamos, para que no se dañen.

* Herencia: es cuando una clase "hereda" las características de otra y además le agrega cosas nuevas. Así no se vuelve a escribir lo mismo.

* Polimorfismo: significa que algo puede tener muchas formas. Por ejemplo, un mismo método puede funcionar de manera distinta según el objeto que lo esté usando.

15. ¿Qué son los modificadores de acceso public, private y protected? ¿Cuándo usarías cada uno?

* public = todos pueden ver y usar esa parte del código.

* private = solo se puede usar dentro de esa misma clase; nadie más lo toca.

* protected = lo pueden usar la clase y las clases que hereden de ella, pero no el resto.

16. ¿Qué es un constructor y para qué sirve?
    
Es un método especial que se ejecuta automáticamente en el momento en que se crea un objeto. Sirve para preparar todo y darle valores iniciales a las variables desde el principio.


## Sección D — Conceptos adicionales

17. ¿Qué es un namespace y por qué es útil?
    
Es como una carpeta donde guardamos nuestros códigos organizados. Así no se nos mezclan nombres de cosas que se llaman igual, y todo queda más ordenado.

19. ¿Qué son las excepciones en C#? ¿Cómo se manejan?
    
Son los errores que pueden pasar mientras el programa corre, como intentar dividir por cero o buscar un archivo que no existe. Se manejan con try-catch: intentamos hacer algo, y si sale mal, lo atrapamos y le avisamos al usuario sin que se cierre el programa.

21. ¿Qué es LINQ y para qué se utiliza?
    
Es una forma sencilla de buscar, ordenar y filtrar información, ya sea de una lista, de una base de datos o de cualquier conjunto de datos. No necesitamos escribir ciclos largos; usamos palabras como "donde", "ordena por", "selecciona" y lo hace solo.

23. ¿Conoces algún IDE o editor de código para programar en C#? ¿Cuál has utilizado?
    
Sí, el más común es Visual Studio, que es completo y trae todo listo para trabajar. También se usa Visual Studio Code, que es más ligero y se le agregan las extensiones que necesitemos. (Puedes poner cuál has usado tú).
Sección E — Pregunta reflexiva

## Sección E — Pregunta reflexiva

21. ¿En qué situaciones considerarías que C# es una buena elección frente a otros lenguajes como Python o Java?
    
Lo elegiría cuando quiera hacer aplicaciones que se vean bien y funcionen rápido en computadoras, celulares o páginas web, especialmente si usamos el ecosistema de Microsoft. También para videojuegos con Unity. En cambio, para empezar a programar muy rápido o para análisis de datos, Python puede ser más sencillo. Si queremos que funcione en cualquier sistema sin instalar mucho, Java puede ser otra opción. Pero si ya aprendemos C#, sirve para muchísimos tipos de proyectos distintos.
