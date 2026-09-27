
# Implementación para iPhone / iOS

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
