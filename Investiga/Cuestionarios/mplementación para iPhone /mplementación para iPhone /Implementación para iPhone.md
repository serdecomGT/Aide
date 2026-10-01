
# Implementación para iPhone / iOS


# INFORME: IMPLEMENTACIÓN EN SISTEMA iOS


1. INTRODUCCIÓN

La aplicación que estamos desarrollando fue creada con la herramienta .NET MAUI, que permite hacer un solo proyecto y que funcione tanto en Android como en iPhone, sin tener que escribir todo el código desde cero otra vez. En este informe explico todo lo que se necesita, los pasos que hay que seguir y cómo se logra que la aplicación corra en dispositivos con sistema operativo iOS.
2. REQUISITOS NECESARIOS

Para que la aplicación funcione en iPhone no basta con la computadora que uso normalmente, hacen falta elementos adicionales:
Requisito Propósito 
Computadora con sistema operativo Mac Es obligatoria para compilar y generar la versión de iPhone 
Cuenta de desarrollador de Apple Permite que la aplicación se pueda instalar y publicar oficialmente 
Programa Xcode instalado en la Mac Es la herramienta oficial de Apple para crear y preparar aplicaciones 
Conexión entre Visual Studio y la Mac Mi computadora se comunica con la Mac para que ella realice la compilación 
Dispositivo iPhone o simulador Sirve para probar que todo se vea y funcione correctamente 

3. PREPARACIÓN DEL PROYECTO

3.1 Verificar la configuración

Primero se revisa que el proyecto tenga activado el sistema iOS como plataforma de destino. En la configuración debe aparecer que el proyecto está preparado para funcionar en ambos sistemas, Android e iOS.

3.2 Lo que no se debe modificar

La base de datos SQLite funciona exactamente igual en iPhone que en Android, por lo que no hay que cambiar nada en esa parte. Todo el código escrito en C# se mantiene igual, no se reescribe nada. Las pantallas se adaptan solas al tamaño de la pantalla del iPhone gracias a .NET MAUI. Las listas, los mensajes, las búsquedas y todas las funciones trabajan de la misma forma en ambos dispositivos.

3.3 Lo que sí se debe ajustar

Se prepara el icono y la imagen de inicio con las medidas que pide Apple. Se asigna un nombre único para identificar la aplicación. Se verifican los permisos que necesita, como acceso a internet y guardado de información.
4. PASOS PARA IMPLEMENTAR Y PROBAR

Paso 1 — Conectar con la computadora Mac

En la computadora Mac se abre el programa Xcode para que instale todo lo que necesita. Desde mi computadora, dentro de Visual Studio, busco la opción para conectar con la Mac. Aparece el nombre de la computadora, le doy conectar y pongo los datos de acceso. Quedan conectadas.

Paso 2 — Seleccionar el sistema iOS

En la parte superior de la pantalla, donde aparece el nombre de Android, se cambia y se elige iOS o el nombre del iPhone que está conectado.

Paso 3 — Probar la aplicación

Se presiona el botón de ejecutar. La computadora se comunica con la Mac, ella prepara la aplicación, la envía al iPhone y se instala automáticamente. Se revisa que todo funcione igual que en Android.

Paso 4 — Generar el archivo de instalación

Cuando ya todo funciona bien, se cambia el modo de trabajo de depuración a versión final. Se selecciona la opción de publicar para iOS, se firma con la cuenta de desarrollador y se genera el archivo listo para instalar o compartir.
5. DIFERENCIAS Y CUIDADOS
Aspecto Detalle 
Código Se mantiene igual, no se cambia nada 
Base de datos Funciona igual, no requiere ajustes 
Pantallas Se adaptan solas al tamaño de cada iPhone 
Instalación En iPhone es más estricta, hay que firmar todo correctamente 
Actualizaciones Cada cambio se vuelve a compilar con el mismo proceso 
Costo La cuenta de Apple tiene un costo anual que se debe considerar 

6. CONCLUSIÓN

La aplicación que estamos haciendo sí puede funcionar en iPhone. No hay que crearla de nuevo, solo hay que seguir los pasos que permiten a .NET MAUI prepararla para ese sistema. La mayor diferencia es que se necesita una computadora Mac y una cuenta especial para poder hacerlo. Todo lo que ya hicimos se aprovecha igual, solo hay que agregar la parte de compilación y firma para que Apple lo permita. Así la aplicación podrá ser usada en ambos tipos de celular, llegando a más personas.


 REQUISITOS QUE NECESITAS ANTES

 Lo indispensable

• Una Mac (computadora Apple) — o bien conectar tu Visual Studio con una Mac en la misma red

• Cuenta de Desarrollador Apple → cuesta aprox. $99 USD al año en developer.apple.com

• Xcode instalado en la Mac (desde la App Store)

• Visual Studio 2026 con la carga de trabajo .NET Multiplataforma instalada

 Tu proyecto ya está listo:

•  Lenguaje: C#

• Marco: .NET 10

• Plataforma: .NET MAUI

•  Base de datos: SQLite (funciona perfecto en iOS 

🔧 PASO 1 — Preparar el proyecto

1. Abre tu solución en Visual Studio 2026

2. Haz clic derecho en tu proyecto → Propiedades

3. En Plataformas de destino, asegúrate de que iOS esté marcado 

4. En el archivo .csproj debe verse algo así:
<TargetFrameworks>net10.0-android;net10.0-ios;net10.0-maccatalyst</TargetFrameworks>
<UseMaui>true</UseMaui>
5. En MauiProgram.cs tu SQLite funciona igual — iOS lo soporta sin cambios 
   
 PASO 2 — Crear cuenta y certificados en Apple

1. Entra a developer.apple.com e inicia sesión con tu Apple ID

2. Ve a Certificates, Identifiers & Profiles

3. Crea tu Bundle ID (ej: com.tunombre.nombreapp) — debe ser igual en tu proyecto

4. Crea un Certificado de Desarrollador y uno de Distribución

5. Genera los Perfiles de Aprovisionamiento (para desarrollo y para App Store
   
🔗 PASO 3 — Conectar Visual Studio con tu Mac

1. En la Mac, instala Xcode y abrelo una vez para que se configuren las herramientas

2. En Visual Studio (Windows): ve a Herramientas → Opciones → Entorno de ejecución de iOS

3. Selecciona tu Mac en la lista y conéctate 🔌

4. Te pedirá el usuario y contraseña de la Mac — se vinculan automáticamente
   
    PASO 4 — Compilar para iOS

Opción A: Probar en un iPhone propio (Desarrollo)

1. Conecta tu iPhone a la Mac por cable

2. En Visual Studio, arriba cambia Android por iOS o Dispositivo Remoto

3. Presiona Ejecutar — se compila y se instala en tu iPhone

Opción B: Crear archivo .ipa para instalar o publicar

1. Cambia el modo de Depuración a Versión / Release

2. Haz clic derecho en el proyecto → Publicar → iOS

3. Elige App Store o Distribución Ad Hoc

4. Firma con tu certificado de Apple

5. Se genera el archivo .ipa — este es el instalable para iPhone

Opción C: Desde la línea de comandos
dotnet publish -f net10.0-ios -c Release
Esto genera el paquete listo para subir
 PASO 5 — Subir a la App Store

1. Entra a App Store Connect

2. Crea tu aplicación con el mismo Bundle ID

3. Sube tu .ipa con la app Transporter o desde Xcode

4. Completa la información: nombre, descripción, capturas, precio

5. Envía a revisión — Apple tarda de 1 a 3 días en aprobarla
 Cosas importantes a saber
Punto Detalle 
 SQLite Funciona igual que en Android no necesitas cambiar nada 
 Tamaño iOS tiene límite de 200 MB por App Store; si pesa más, usa recursos en la nube 
 Compartir código Todo tu código C# y lógica funciona igual en Android e iOS 
 Interfaz .NET MAUI adapta los controles al diseño de iPhone automáticamente 
 Costos La cuenta de desarrollador Apple cuesta $99 USD/año 
 Sin Mac Puedes usar servicios de compilación en la nube como GitHub Actions o MacinCloud 

 Si NO tienes una Mac

Puedes usar compilación en la nube:

• GitHub Actions — gratuito en muchos casos

• MacinCloud — renta una Mac por horas

• Azure DevOps — también tiene agentes de compilación para iOS
