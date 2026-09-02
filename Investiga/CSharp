C# (pronunciado C-Sharp) es un lenguaje de programación multiparadigma, moderno y orientado a objetos, desarrollado por Microsoft en el año 2000 como parte de su plataforma .NET.Puedes consultar todos los detalles técnicos en la guía oficial de Microsoft Learn ¿Para qué sirve?Desarrollo web: Creación de aplicaciones y APIs robustas con ASP.NET Core y frontend interactivo con Blazor.Aplicaciones de escritorio: Construcción de software para Windows usando WPF o WinForms.Desarrollo móvil: Programación de aplicaciones nativas para Android e iOS mediante .NET MAUI.Videojuegos: Es el lenguaje principal del motor Unity, uno de los más usados ​​del mundo.Servicios en la nube: Creación de microservicios y aplicaciones escalables optimizadas para entornos cloud.Sintaxis de C#Es un lenguaje de tipado fuerte (las variables deben tener un tipo de dato definido) y su sintaxis es muy similar a la de C, C++ y Java. Para que el código sea mejor, más limpio, moderno y rápido de escribir, C# introdujo características avanzadas en sus últimas versiones. Esta es la sintaxis "mejorada" y profesional que se utiliza hoy en día:1. Sentencias Superiores (Top-Level Statements)Ya no necesitas escribir clases, namespaces ni el método Main para programas sencillos. El archivo se lee directamente de arriba a abajo.Antes: 15 líneas de estructura pesada.Ahora (Mejor):csharpusing System;

string saludo = "¡Hola, mundo!";
Consola.WriteLine(saludo);
Utilice el código con precaución.2. Coincidencia de Patrones (Pattern Matching)Reemplaza los bloques if/else largos o los switch antiguos por una sintaxis ultra compacta y expresiva.csharpint edad = 20;

// Expresión switch directa
string categoria = edad switch
{
< 12 => "Niño",
< 18 => "Adolescente",
_ => "Adulto" // El guion bajo (_) es el caso por defecto
};

Console.WriteLine(categoría);
Utilice el código con precaución.3. Inicialización de Objetos SimplificadaNo hace falta repetir el nombre de la clase al usar new. El compilador ya sabe qué objeto estás creando.csharp// Antes: Persona usuario = new Persona("Carlos");
Persona usuario = new("Carlos");

// Inicialización de propiedades sin constructor
Producto item = new() { Id = 1, Nombre = "Laptop", Precio = 899.99 };
Utilice el código con precaución.4. Tipos Registro (Records)Ideales para modelar datos puros de forma inmutable (que no cambian). Cree una clase completa con propiedades, constructor y comparadores en una sola línea.csharppublic record Cliente(int Id, string Nombre, string Email);

// Uso automático
Cliente cliente1 = new(1, "Ana", " ana@email.com ");
Utilice el código con precaución.5. Expresiones Lambda para Métodos CortosSi una función solo tiene una línea de código, elimina las llaves {} y el return usando el operador flecha (=>).csharp// Antes: public int Sumar(int a, int b) { return a + b; }
public int Sumar(int a, int b) => a + b;

public void MostrarMensaje() => Console.WriteLine("Acción ejecutada");
Utilice el código con precaución.


¿Qué es C#?  (se pronuncia "C Sharp") es un lenguaje de programación moderno, orientado a objetos y fuertemente tipado, desarrollado por Anders Hejlsberg y su equipo en Microsoft en el año 2000. Forma parte del ecosistema .NET, siendo uno de los lenguajes principales de esta plataforma. Su diseño combina la potencia de lenguajes como C++ con la facilidad de uso de lenguajes como Java, permitiendo a los desarrolladores crear aplicaciones de manera eficiente y segura.
C# es multiplataforma y versátil: con él se pueden desarrollar desde simples programas de consola hasta complejas aplicaciones empresariales, videojuegos, aplicaciones móviles, servicios en la nube y sistemas embebidos. A lo largo de los años ha evolucionado constantemente, incorporando características como programación asincrónica, manejo de valores nulos, registros y funcionalidades de inteligencia artificial.

Historia y evolución

* 2000: Nace C# 1.0 junto con .NET Framework 1.0, como parte de la estrategia de Microsoft para competir con Java.

* 2005: Con C# 2.0 llegan los genéricos, los tipos anulables y los métodos anónimos.

* 2007: C# 3.0 introduce las expresiones lambda, LINQ (Language Integrated Query) y la inicialización automática de propiedades, revolucionando la forma de escribir consultas de datos.

* 2010-2015: Se agregan características asincrónicas (async/await), interpolación de cadenas y manejo más limpio de referencias.

* 2020 en adelante: Con .NET 5 y versiones posteriores, C# se vuelve verdaderamente multiplataforma, corriendo nativamente en Windows, Linux y macOS. Se incorporan registros, mejora de rendimiento y soporte nativo para procesamiento de datos grandes.

Características principales

1. Orientado a objetos: Todo se organiza en clases y objetos, lo que facilita reutilizar código, mantenerlo y trabajarlo en equipo. Soporta herencia, polimorfismo, encapsulamiento y abstracción.

2. Fuertemente tipado: Cada variable tiene un tipo definido (entero, texto, booleano, etc.), lo que ayuda a detectar errores antes de que el programa se ejecute.

3. Recolección automática de basura: El sistema gestiona la memoria por ti, liberando espacio cuando algo ya no se usa, evitando fugas de memoria.

4. Multiplataforma: Gracias a .NET Core y .NET moderno, el mismo código puede correr en distintos sistemas operativos sin modificarlo.

5. Integración con otros lenguajes: Puede convivir con código escrito en Visual Basic .NET, F# o incluso bibliotecas nativas de C++.

6. Seguridad: Tiene mecanismos integrados para validar accesos, manejar datos sensibles y prevenir errores comunes de memoria.

Sintaxis básica

La sintaxis de C# es clara y estructurada:

* Las instrucciones terminan con punto y coma ;.

* Los bloques de código se encierran entre llaves { }.

* Es sensible a mayúsculas y minúsculas: Nombre no es igual a nombre.

using System;

namespace MiPrograma
{
    class ProgramaPrincipal
    {
        static void Main(string[] argumentos)
        {
            // Declaración de variables
            string nombre = "María";
            int edad = 18;

            // Salida en consola
            Console.WriteLine($"Hola, me llamo {nombre} y tengo {edad} años.");
            
            // Estructura de control
            if (edad >= 18)
            {
                Console.WriteLine("Eres mayor de edad.");
            }
            else
            {
                Console.WriteLine("Todavía eres menor de edad.");
            }
        }
    }
}

¿Para qué se usa?

* Aplicaciones de escritorio: Programas que se instalan en la computadora, como sistemas de facturación o control de inventario, usando Windows Forms o WPF.

* Desarrollo web: Con ASP.NET Core y Blazor, se crean sitios web dinámicos, tiendas en línea y plataformas educativas.

* Videojuegos: Es el lenguaje principal del motor Unity, uno de los más usados del mundo.

* Aplicaciones móviles: Con .NET MAUI se hace una misma app para Android, iOS, Windows y Mac.

* Servicios y APIs: Programas que se ejecutan en servidores y entregan datos a páginas web o apps móviles.

* Ciencia de datos e IA: Se integra con bibliotecas de procesamiento de datos y modelos de inteligencia artificial.

Ventajas y desventajas

Ventajas:

* Lenguaje muy documentado y con gran comunidad de apoyo.

* Integración total con herramientas de Microsoft como Visual Studio, Azure y SQL Server.

* Actualizaciones constantes que mejoran rendimiento y funcionalidades.

* Curva de aprendizaje accesible para quienes ya conocen otros lenguajes similares.

Desventajas:

* Históricamente estuvo muy ligado a Windows, aunque hoy en día ya es multiplataforma.

* Puede ser menos rápido que lenguajes de bajo nivel como C++ en tareas que exigen máximo rendimiento.

* El tamaño de los archivos compilados puede ser mayor que en lenguajes más ligeros.




* Todo programa debe tener un punto de entrada, que es el método Main.
