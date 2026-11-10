MY SCHOOL PLANNER 14.7 — NATIVE STARTER

This package prepares the current web app for Capacitor-based iOS and Android builds.
It is NOT a compiled iOS .ipa or Android .aab yet.

Contents:
- www/: current web app files from version 14.7
- package.json: Capacitor 8 dependencies and scripts
- capacitor.config.json: app identity and web asset directory

Important checks before store release:
1. Confirm appId (com.myschoolplanner.app) is the permanent reverse-domain identifier.
2. Review privacy policy and data handling. Current app stores its data locally in the browser/device.
3. Test local storage migration and backup/restore on iOS and Android.
4. Configure push notifications separately. OneSignal dashboard setup alone does not activate push:
   web push requires browser permission and service worker setup; native iOS requires APNs credentials;
   native Android requires Firebase/FCM credentials and SDK integration.
5. Build/sign iOS with a macOS/Xcode or a compatible cloud build service; Android with Android SDK/Gradle
   or a compatible cloud build service.
6. Do not upload this starter directly as an App Store or Google Play binary.

To initialize native platforms in a build environment:
  npm install
  npx cap add ios
  npx cap add android
  npx cap sync

The current web app archive had older README/service-worker version labels; update notes are informational.
Do not delete the existing Cloudflare deployment or browser data.


Actualizare 14.7: lista materiilor a fost simplificată la discipline școlare uzuale. În toate listele de materii există opțiunea „Adaugă o materie...”; materiile personalizate se salvează local și rămân disponibile în orar, teme, evaluări și note.
