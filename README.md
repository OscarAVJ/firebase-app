# Firebase App con React Native y Expo

Aplicación Expo que administra productos en tiempo real con Cloud Firestore.

## Configuración

Requisitos: Node.js LTS y Expo Go instalado en el dispositivo, o un emulador de Android/iOS.

1. Instala las dependencias:

   ```bash
   npm install
   ```

2. Crea tu archivo local de variables de entorno a partir de la plantilla:

   **PowerShell**

   ```powershell
   Copy-Item .env.example .env
   ```

   **macOS/Linux**

   ```bash
   cp .env.example .env
   ```

3. En Firebase Console, abre **Configuración del proyecto > General > Tus apps**. Registra o selecciona una aplicación web y copia los valores de `firebaseConfig` al archivo `.env`.

4. En Firebase Console, crea una base de datos de **Cloud Firestore** y configura sus reglas según las necesidades de tu entorno.

5. Inicia la aplicación:

   ```bash
   npm start
   ```

Escanea el código QR con Expo Go. También puedes usar `npm run android`, `npm run ios` o `npm run web`.

## Variables requeridas

```dotenv
EXPO_PUBLIC_FIREBASE_API_KEY=
EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN=
EXPO_PUBLIC_FIREBASE_PROJECT_ID=
EXPO_PUBLIC_FIREBASE_STORAGE_BUCKET=
EXPO_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=
EXPO_PUBLIC_FIREBASE_APP_ID=
```

Expo incluye las variables `EXPO_PUBLIC_*` en el bundle de la aplicación. La configuración de cliente de Firebase está diseñada para ser pública; protege los datos mediante reglas de seguridad de Firestore y nunca coloques claves privadas o credenciales de servidor en estas variables.
