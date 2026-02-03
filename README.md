# Flutter-Initial 🚀

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)

Un repositorio de introducción a Flutter que incluye un proyecto pequeño y una **guía completa** para la correcta instalación y configuración de Flutter en Windows 10/11.

---

## 📋 Tabla de Contenidos

- [Características](#-características)
- [Requisitos Previos](#-requisitos-previos)
- [Guía de Instalación](#-guía-de-instalación)
  - [1. Instalación de Visual Studio Code](#1-instalación-de-visual-studio-code)
  - [2. Instalación de Flutter SDK](#2-instalación-de-flutter-sdk)
  - [3. Verificación del Entorno](#3-verificación-del-entorno)
  - [4. Solución de Problemas Comunes](#4-solución-de-problemas-comunes)
- [Primeros Pasos](#-primeros-pasos)
- [Recursos Adicionales](#-recursos-adicionales)

---

## ✨ Características

- ✅ Proyecto inicial de Flutter listo para usar
- 📘 Guía paso a paso para Windows 10/11
- 🔧 Configuración completa del entorno de desarrollo
- 🛠️ Solución de problemas comunes con `flutter doctor`
- 📱 Configuración para desarrollo Android, Web y Windows

---

## 🔍 Requisitos Previos

Antes de comenzar, asegúrate de tener:

- Windows 10 (64-bit) o Windows 11
- Al menos 2 GB de espacio libre en disco
- Conexión a Internet estable

---

## 📚 Guía de Instalación

### 1. Instalación de Visual Studio Code

Visual Studio Code será nuestro editor principal para desarrollar con Flutter.

#### Paso 1.1: Descargar VS Code

1. Visita la página oficial: [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Haz clic en **"Download for Windows"**
3. Ejecuta el instalador descargado (`VSCodeUserSetup-x64-x.xx.x.exe`)
4. Sigue el asistente de instalación:
   - ✅ Acepta el acuerdo de licencia
   - ✅ Marca la opción **"Agregar a PATH"** (importante)
   - ✅ Marca **"Crear un icono en el escritorio"** (opcional)
   - ✅ Marca **"Agregar la acción 'Abrir con Code' al menú contextual"** (recomendado)

#### Paso 1.2: Instalar Extensiones de Flutter y Dart

1. Abre **Visual Studio Code**
2. Haz clic en el icono de **Extensiones** en la barra lateral izquierda (o presiona `Ctrl+Shift+X`)
3. Busca e instala las siguientes extensiones:

   **📦 Flutter**
   - Busca: `Flutter`
   - Autor: Dart Code
   - Haz clic en **"Install"**

   **📦 Dart**
   - Busca: `Dart`
   - Autor: Dart Code
   - Haz clic en **"Install"**

> **💡 Tip:** La extensión de Dart se instalará automáticamente junto con Flutter, pero es bueno verificar que ambas estén activas.

---

### 2. Instalación de Flutter SDK

Una vez instaladas las extensiones, VS Code te ayudará a instalar el SDK de Flutter automáticamente.

#### Paso 2.1: Iniciar la Instalación desde VS Code

1. Presiona `Ctrl+Shift+P` para abrir la **Paleta de Comandos**
2. Escribe: `Flutter: New Project`
3. VS Code detectará que no tienes Flutter instalado y te mostrará una notificación
4. Haz clic en **"Download SDK"** o **"Locate SDK"**

**Opción A: Dejar que VS Code descargue el SDK (Recomendado)**
- VS Code descargará automáticamente la última versión estable de Flutter
- Selecciona una ubicación en tu PC (por ejemplo: `C:\src\flutter`)
- Espera a que termine la descarga y extracción

**Opción B: Descarga Manual**
1. Ve a [https://flutter.dev/docs/get-started/install/windows](https://flutter.dev/docs/get-started/install/windows)
2. Descarga el archivo ZIP de Flutter SDK
3. Extrae el contenido en una ubicación de tu elección (por ejemplo: `C:\src\flutter`)
4. En VS Code, presiona `Ctrl+Shift+P` y selecciona `Flutter: Change SDK`
5. Navega hasta la carpeta donde extrajiste Flutter

#### Paso 2.2: Configuración Automática del PATH

Durante el proceso, VS Code te preguntará si deseas agregar Flutter al PATH del sistema:

- ✅ Selecciona **"Yes"** o **"Add to PATH"**
- Esto permitirá ejecutar comandos de Flutter desde cualquier terminal

> **⚠️ Importante:** Si VS Code no agrega Flutter al PATH automáticamente, hazlo manualmente:
> 1. Busca **"Variables de entorno"** en el menú de Windows
> 2. En **Variables del sistema**, selecciona `Path` y haz clic en **Editar**
> 3. Agrega la ruta: `C:\src\flutter\bin` (ajusta según tu ubicación)
> 4. Haz clic en **Aceptar**

#### Paso 2.3: Verificar la Instalación

1. Abre una **nueva terminal** en VS Code (`` Ctrl+` `` o `Terminal > New Terminal`)
2. Ejecuta el siguiente comando:

```bash
flutter --version
```

Deberías ver la versión de Flutter instalada. Por ejemplo:

```
Flutter 3.38.9 • channel stable • https://github.com/flutter/flutter.git
Framework • revision xxxxxxxx (X days ago) • 2025-XX-XX XX:XX:XX -XXXX
Engine • revision xxxxxxxx
Tools • Dart 3.x.x • DevTools 2.x.x
```

---

### 3. Verificación del Entorno

Ahora verificaremos que todo esté configurado correctamente usando `flutter doctor`.

#### Paso 3.1: Ejecutar Flutter Doctor

En la terminal de VS Code, ejecuta:

```bash
flutter doctor
```

Este comando analiza tu sistema y muestra un reporte del estado de tu instalación. Ejemplo de salida:

```
Doctor summary (to see all details, run flutter doctor -v):
[√] Flutter (Channel stable, 3.38.9, on Microsoft Windows [Versión 10.0.26200.7623], locale es-CO)
[√] Windows Version (Windows 11 or higher)
[X] Android toolchain - develop for Android devices
[X] Chrome - develop for the web (Cannot find Chrome executable)
[X] Visual Studio - develop Windows apps
[√] Connected device (1 available)
[√] Network resources
```

**Significado de los símbolos:**
- `[√]` = Configurado correctamente ✅
- `[!]` = Parcialmente configurado (puede funcionar pero con advertencias) ⚠️
- `[X]` = Falta configuración ❌

No te preocupes si ves errores `[X]`, los solucionaremos a continuación.

---

### 4. Solución de Problemas Comunes

#### 🔧 Problema 1: Android toolchain - develop for Android devices

**Error típico:**
```
[X] Android toolchain - develop for Android devices
    X Unable to locate Android SDK.
```

Este error indica que Flutter no puede encontrar el SDK de Android, necesario para desarrollar aplicaciones móviles.

---

##### **Opción A: Instalar Android Studio (Más Fácil) ⭐ Recomendado**

Esta es la forma más sencilla ya que Android Studio configura todo automáticamente.

1. **Descargar Android Studio**
   - Ve a: [https://developer.android.com/studio](https://developer.android.com/studio)
   - Haz clic en **"Download Android Studio"**
   - Ejecuta el instalador descargado

2. **Instalar Android Studio**
   - Sigue el asistente de instalación
   - Acepta la configuración estándar
   - Espera a que descargue e instale el SDK de Android (puede tardar varios minutos)

3. **Instalar Command-line Tools**
   - Abre **Android Studio**
   - En la pantalla de bienvenida, haz clic en **"More Actions"** → **"SDK Manager"**
   - O si ya tienes un proyecto abierto: **File** → **Settings** → **Appearance & Behavior** → **System Settings** → **Android SDK**
   
   - Ve a la pestaña **"SDK Tools"**
   - Marca la casilla: ✅ **"Android SDK Command-line Tools (latest)"**
   - Marca también (si no están instaladas):
     - ✅ **Android SDK Build-Tools**
     - ✅ **Android SDK Platform-Tools**
   - Haz clic en **"Apply"** → **"OK"**
   - Espera a que se descarguen e instalen las herramientas

4. **Aceptar las Licencias de Android**
   
   Abre una terminal y ejecuta:
   ```bash
   flutter doctor --android-licenses
   ```
   
   Te mostrará varias licencias. Para cada una:
   - Lee la licencia (puedes presionar `Enter` para avanzar)
   - Escribe `y` (yes) y presiona `Enter` para aceptar
   - Repite para todas las licencias

5. **Verificar**
   ```bash
   flutter doctor
   ```
   
   Ahora deberías ver:
   ```
   [√] Android toolchain - develop for Android devices (Android SDK version XX.X.X)
   ```

---

##### **Opción B: Instalar Solo Command-line Tools (Solo lo Necesario)**

Si no quieres instalar Android Studio completo, puedes instalar solo las herramientas de línea de comandos.

> **⚠️ Advertencia:** Esta opción requiere configuración manual y es más propensa a errores. Se recomienda solo para usuarios avanzados.

1. **Descargar Command-line Tools**
   - Ve a: [https://developer.android.com/studio#command-line-tools-only](https://developer.android.com/studio#command-line-tools-only)
   - Descarga **"Command line tools only"** para Windows
   - Guarda el archivo ZIP (por ejemplo: `commandlinetools-win-XXXXXXX_latest.zip`)

2. **Crear Estructura de Carpetas**
   
   Crea la siguiente estructura en tu PC:
   ```
   C:\Android\
   └── cmdline-tools\
       └── latest\
   ```

3. **Extraer el Contenido**
   - Extrae el contenido del ZIP descargado
   - Mueve **todo el contenido** a: `C:\Android\cmdline-tools\latest\`
   - La estructura final debe ser:
     ```
     C:\Android\
     └── cmdline-tools\
         └── latest\
             ├── bin\
             ├── lib\
             └── ...
     ```

4. **Configurar Variables de Entorno**

   a) Busca **"Variables de entorno"** en el menú de Windows
   
   b) En **Variables del sistema**, haz clic en **"Nueva..."** y agrega:
      - **Nombre:** `ANDROID_HOME`
      - **Valor:** `C:\Android`
   
   c) Edita la variable `Path` y agrega estas dos rutas:
      - `%ANDROID_HOME%\cmdline-tools\latest\bin`
      - `%ANDROID_HOME%\platform-tools`

5. **Instalar Componentes Necesarios**
   
   Abre una **nueva terminal como Administrador** (CMD o PowerShell) y ejecuta:
   
   ```bash
   sdkmanager "platform-tools" "platforms;android-34" "build-tools;34.0.0" "cmdline-tools;latest"
   ```
   
   Esto descargará e instalará los componentes esenciales del SDK.

6. **Aceptar Licencias**
   ```bash
   sdkmanager --licenses
   ```
   Acepta todas las licencias escribiendo `y` y presionando `Enter`.

7. **Configurar Flutter**
   ```bash
   flutter config --android-sdk C:\Android
   ```

8. **Verificar**
   ```bash
   flutter doctor
   ```

---

#### 🌐 Problema 2: Chrome - develop for the web

**Error típico:**
```
[X] Chrome - develop for the web (Cannot find Chrome executable at .\Google\Chrome\Application\chrome.exe)
    ! Cannot find Chrome. Try setting CHROME_EXECUTABLE to a Chrome executable.
```

Flutter busca Google Chrome por defecto para desarrollo web, pero puedes usar cualquier navegador basado en Chromium (Brave, Edge, etc.).

---

##### **Solución: Configurar un Navegador Alternativo**

**Ejemplo con Brave Browser:**

1. **Encontrar la Ruta del Navegador**
   
   La ruta típica de Brave es:
   ```
   C:\Program Files\BraveSoftware\Brave-Browser\Application\brave.exe
   ```
   
   Para otros navegadores:
   - **Microsoft Edge:** `C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe`
   - **Google Chrome:** `C:\Program Files\Google\Chrome\Application\chrome.exe`
   - **Chromium:** `C:\Program Files\Chromium\Application\chrome.exe`

2. **Verificar que el Archivo Existe**
   
   Abre el Explorador de Windows y navega a la ruta para confirmar que el archivo `.exe` existe.

3. **Configurar la Variable de Entorno**
   
   Abre una terminal (CMD o PowerShell) y ejecuta:
   
   ```bash
   setx CHROME_EXECUTABLE "C:\Program Files\BraveSoftware\Brave-Browser\Application\brave.exe"
   ```
   
   **⚠️ Importante:** Ajusta la ruta según tu navegador.

4. **Cerrar y Reabrir la Terminal**
   
   Para que los cambios surtan efecto, **cierra todas las ventanas de terminal** y abre una nueva.

5. **Verificar**
   ```bash
   flutter doctor
   ```
   
   Ahora deberías ver:
   ```
   [√] Chrome - develop for the web
   ```

**Método Alternativo (Configuración Global de Flutter):**

También puedes configurarlo directamente con Flutter:

```bash
flutter config --chrome-executable="C:\Program Files\BraveSoftware\Brave-Browser\Application\brave.exe"
```

---

#### 🪟 Problema 3: Visual Studio - develop Windows apps

**Error típico:**
```
[X] Visual Studio - develop Windows apps
    X Visual Studio not installed; this is necessary to develop Windows apps.
```

> **📝 Nota:** Esto es **Visual Studio** (el IDE completo), **NO** Visual Studio Code. Son productos diferentes.

Visual Studio es necesario solo si deseas desarrollar aplicaciones de escritorio para Windows.

---

##### **Solución: Instalar Visual Studio Community**

1. **Descargar Visual Studio**
   - Ve a: [https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)
   - Descarga **"Visual Studio Community"** (es gratis)
   - Ejecuta el instalador descargado

2. **Seleccionar Componentes Durante la Instalación**
   
   El instalador te mostrará diferentes "workloads" (cargas de trabajo). Debes seleccionar:
   
   ✅ **"Desarrollo para el escritorio con C++"** (Desktop development with C++)
   
   En el panel derecho, asegúrate de que estén marcados:
   - ✅ **MSVC v143 - VS 2022 C++ x64/x86 build tools** (o la versión más reciente disponible)
   - ✅ **Windows 10 SDK** o **Windows 11 SDK** (según tu sistema)
   - ✅ **C++ CMake tools for Windows**

3. **Completar la Instalación**
   - Haz clic en **"Instalar"**
   - La descarga e instalación puede tardar entre 30 minutos y 1 hora dependiendo de tu conexión
   - Es normal que descargue varios GB de datos

4. **Reiniciar el PC**
   
   Después de la instalación, **reinicia tu computadora** para que todos los componentes se configuren correctamente.

5. **Verificar**
   ```bash
   flutter doctor
   ```
   
   Ahora deberías ver:
   ```
   [√] Visual Studio - develop Windows apps (Visual Studio Community 2022 17.X.X)
   ```

---

#### ✅ Verificación Final Completa

Después de solucionar todos los problemas, ejecuta:

```bash
flutter doctor -v
```

El flag `-v` (verbose) te mostrará información detallada. Idealmente deberías ver algo como:

```
Doctor summary (to see all details, run flutter doctor -v):
[√] Flutter (Channel stable, 3.38.9, on Microsoft Windows [Versión 10.0.26200.7623], locale es-CO)
[√] Windows Version (Windows 11 or higher)
[√] Android toolchain - develop for Android devices (Android SDK version 36.1.0)
[√] Chrome - develop for the web
[√] Visual Studio - develop Windows apps (Visual Studio Community 2022 17.X.X)
[√] Connected device (3 available)
[√] Network resources

• No issues found!
```

**🎉 ¡Felicidades! Tu entorno de Flutter está completamente configurado.**

---

## 🚀 Primeros Pasos

Ahora que tienes Flutter instalado correctamente, puedes crear tu primer proyecto:

### Crear un Nuevo Proyecto

1. Abre VS Code
2. Presiona `Ctrl+Shift+P`
3. Escribe: `Flutter: New Project`
4. Selecciona **"Application"**
5. Elige una ubicación para tu proyecto
6. Escribe un nombre (por ejemplo: `mi_primera_app`)

### Ejecutar el Proyecto

1. Abre la terminal en VS Code (`` Ctrl+` ``)
2. Asegúrate de estar en la carpeta del proyecto
3. Ejecuta:

**Para Web:**
```bash
flutter run -d chrome
```

**Para Windows:**
```bash
flutter run -d windows
```

**Para Android (con emulador o dispositivo conectado):**
```bash
flutter run
```

### Comandos Útiles

```bash
# Ver dispositivos disponibles
flutter devices

# Ver información detallada del entorno
flutter doctor -v

# Limpiar el proyecto (útil cuando hay errores)
flutter clean

# Obtener dependencias
flutter pub get

# Actualizar Flutter a la última versión
flutter upgrade
```

---

## 📖 Recursos Adicionales

### Documentación Oficial
- [Flutter Documentation](https://flutter.dev/docs)
- [Dart Language Tour](https://dart.dev/guides/language/language-tour)
- [Flutter Cookbook](https://flutter.dev/docs/cookbook)

### Tutoriales y Guías
- [Flutter Codelabs](https://flutter.dev/docs/codelabs)
- [Flutter YouTube Channel](https://www.youtube.com/c/flutterdev)
- [Dart API Reference](https://api.dart.dev/)

### Comunidad
- [Flutter Community](https://flutter.dev/community)
- [Stack Overflow - Flutter](https://stackoverflow.com/questions/tagged/flutter)
- [Reddit - r/FlutterDev](https://www.reddit.com/r/FlutterDev/)

---

## 🤝 Contribuciones

¿Encontraste algún error o tienes sugerencias? ¡Las contribuciones son bienvenidas!

1. Fork este repositorio
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

---

## ⭐ Agradecimientos

- Al equipo de Flutter por crear este increíble framework
- A la comunidad de desarrolladores que comparten su conocimiento
- A todos los que contribuyen a mejorar esta guía

---

**¿Te fue útil esta guía? ¡No olvides dejar una ⭐ en el repositorio!**

---

<div align="center">

Hecho con ❤️ para la comunidad de Flutter

[Reportar un Problema](../../issues) · [Solicitar una Característica](../../issues)

</div>
