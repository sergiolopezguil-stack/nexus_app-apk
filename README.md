# Nexus app — APK

Esta carpeta sirve para **almacenar y versionar** el paquete instalable de la aplicación **Nexus** en Android.

## ¿Qué hay aquí?

- **`app-release.apk`**: instalador Android (APK) de la app **Nexus**, generado a partir del proyecto Capacitor del frontend (`frontend/frontend/android`). La app es en esencia la **misma aplicación web** (Next.js en Vercel) ejecutándose dentro de un **WebView** nativo.

No incluye el código fuente del ERP; solo el **binario** listo para instalar en dispositivos compatibles (sideload, pruebas internas, etc.).

## Cómo se genera

1. En el repo del frontend, con la URL de producción si aplica:
   ```powershell
   $env:CAPACITOR_SERVER_URL="https://tu-dominio.vercel.app"
   npm run android:sync
   ```
2. Build firmado desde **Android Studio** (*Build → Generate Signed App Bundle / APK* → **APK**) o, según tu flujo, copiar aquí el APK release que Gradle deje en  
   `frontend/frontend/android/app/build/outputs/apk/release/`.

## Instalación en el móvil

1. Copia `app-release.apk` al teléfono (USB, nube, etc.).
2. Ábrelo y acepta instalar desde **orígenes desconocidos** si el sistema lo pide.
3. **Google Play** no interviene**: es instalación directa del APK.

## Notas

- Para **publicar en Play Store** lo habitual es subir un **Android App Bundle** (`.aab`), no este APK.
- **Paquete de la app:** `com.colabstudio.nexus` (debe coincidir con el firmado).
- Mantén alineadas **versión** y **notas de versión** con lo que publiques en otros sitios (por ejemplo `CHANGELOG.md` del frontend).
