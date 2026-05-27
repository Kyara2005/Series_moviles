# Proyecto App Multimedia

## 🔗 Web App
https://vibe-u.web.app/videojuegos

## 🎥 Video integrado
Se consume vides de YouTube para los trailes dentro de la app.

## 🔊 Audio
Reproducción de audio sin salir de la aplicación usando MediaPlayer.

## ☁️ Supabase Storage
Se utiliza Supabase para almacenar imágenes y audios en la nube.

## 📦 Builds
- APK Debug
- APK Release (firmado)
- AAB Debug
- AAB Release (firmado)

## ⚙️ Tecnologías
- Android
- Supabase
- Firebase





# Generación de APK y AAB en Ionic + Capacitor 📱
---

# 🔹 Requisitos Previos

Tener instalado:

* Node.js
* Ionic CLI
* Android Studio
* Capacitor

Instalar Ionic CLI:

```bash
npm install -g @ionic/cli
```

---

# 🔹 Compilar el Proyecto Ionic

Generar la carpeta `www`:

```bash
ionic build
```

---

# 🔹 Sincronizar con Android

```bash
ionic cap add android
npx cap sync android
```

---

# 🔹 Abrir el Proyecto en Android Studio

```bash
npx cap open android
```

---

# 🔹 Generar APK No Firmada (Debug)

En Android Studio:

```text
Build > Build APK(s)
```

Ruta del archivo generado:

```text
android/app/build/outputs/apk/debug/app-debug.apk
```

Esta APK sirve para pruebas y desarrollo. Tambien se puede encontrar la APK al presionar en el boton "locate".

---

# 🔹 Generar APK Firmada (Release)

## Paso 1: Abrir el asistente

En Android Studio:

```text
Build > Generate Signed Bundle / APK
```

---

## Paso 2: Seleccionar APK

Elegir:

```text
APK
```

Luego presionar:

```text
Next
```

---

## Paso 3: Crear o Seleccionar Keystore

Si no existe una keystore:

```text
Create new...
```

Completar:

* Key store path
* Password
* Alias
* Validity

Guardar el archivo `.jks` en un lugar seguro ya que no se puede recuperar la contraseña en dado caso que se olvide.

---

## Paso 4: Seleccionar Release

Marcar:

```text
release
```

Finalmente:

```text
Finish
```

---

## Ruta del APK firmado

```text
android/app/build/outputs/apk/release/app-release.apk
```

---

# 🔹 Generar AAB Firmado

El formato `.aab` es requerido por Google Play Store.

## Paso 1

En Android Studio:

```text
Build > Generate Signed Bundle / APK
```

---

## Paso 2

Seleccionar:

```text
Android App Bundle
```

Luego:

```text
Next
```

---

## Paso 3

Seleccionar la keystore y la configuración `release`.

---

## Paso 4

Presionar:

```text
Finish
```

---

## Ruta del archivo AAB

```text
android/app/build/outputs/bundle/release/app-release.aab
```

---

---

# 🔹 Comandos Principales

```bash
ionic build
ionic cap add android
npx cap sync android
npx cap open android
```

---

