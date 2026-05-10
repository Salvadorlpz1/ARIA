# Guía de Compilación de APK con EAS Build

Esta guía proporciona instrucciones detalladas para compilar el archivo APK de la aplicación utilizando EAS Build, un servicio en la nube proporcionado por Expo. Este servicio es gratuito para compilaciones individuales.

## Requisitos Previos

Antes de comenzar, asegúrate de tener lo siguiente:

*   **Node.js**: Asegúrate de tener Node.js instalado en tu sistema. Puedes descargarlo desde [nodejs.org](https://nodejs.org/).
*   **Cuenta en Expo.dev**: Necesitarás una cuenta en [expo.dev](https://expo.dev/). Si no tienes una, puedes crear una de forma gratuita.

## Pasos para Compilar el APK

Sigue estos pasos para generar el APK de tu aplicación:

### Paso 1: Instalar EAS CLI

EAS CLI es la interfaz de línea de comandos de Expo Application Services. Instálala globalmente en tu sistema ejecutando el siguiente comando en tu terminal:

```bash
npm install -g eas-cli
```

### Paso 2: Iniciar Sesión en EAS

Una vez instalado EAS CLI, inicia sesión en tu cuenta de Expo.dev. Esto vinculará tu terminal con tu cuenta de Expo:

```bash
eas login
```

Se te pedirá que ingreses tus credenciales de Expo.dev.

### Paso 3: Configurar el Proyecto

Configura tu proyecto para usar EAS Build. Este comando creará un archivo `eas.json` si no existe (aunque ya lo hemos creado) y te guiará a través de algunas configuraciones iniciales:

```bash
eas build:configure
```

### Paso 4: Compilar el APK

Ahora puedes iniciar el proceso de compilación del APK. Utilizaremos el perfil `preview` para generar un APK de prueba. El `buildType` está configurado como `apk` en el archivo `eas.json`.

```bash
eas build --platform android --profile preview
```

Este comando subirá tu proyecto a los servidores de EAS Build y comenzará la compilación. El proceso puede tardar varios minutos, dependiendo del tamaño del proyecto y la carga del servicio.

### Paso 5: Descargar el APK

Una vez que la compilación haya finalizado con éxito, EAS CLI te proporcionará un enlace. Desde este enlace, podrás descargar directamente el archivo APK generado. Copia y pega el enlace en tu navegador para descargar el APK.

## Notas Importantes

*   **Servicio Gratuito**: EAS Build ofrece un nivel gratuito que es suficiente para compilaciones individuales y pruebas. Para necesidades más avanzadas o un mayor volumen de compilaciones, considera los planes de pago de Expo.
*   **Compilación Local (Alternativa)**: Si prefieres compilar el APK localmente o tienes problemas con EAS Build, puedes hacerlo si tienes el Android SDK configurado en tu máquina. Los pasos específicos para la compilación local varían, pero generalmente implican el uso de comandos de Gradle o herramientas de Android Studio. Para más detalles, consulta la documentación oficial de Expo sobre [compilación local](https://docs.expo.dev/build/local-builds/).

## Referencias

[1] Node.js. *Descargar Node.js*. Disponible en: [https://nodejs.org/](https://nodejs.org/)
[2] Expo.dev. *Expo Application Services (EAS)*. Disponible en: [https://expo.dev/](https://expo.dev/)
[3] Expo Documentation. *Local Builds*. Disponible en: [https://docs.expo.dev/build/local-builds/](https://docs.expo.dev/build/local-builds/)
