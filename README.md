# NCDA ONTAP — Projet Android (généré depuis votre HTML)

Ce projet encapsule votre fichier `Modele_chatbox.html` dans une application
Android native (Kotlin + WebView). Votre QCM est embarqué dans
`app/src/main/assets/index.html` et fonctionne hors ligne.

## Compiler l'APK

### Méthode A — GitHub Actions (rien à installer)
1. Créez un dépôt sur github.com.
2. Déposez TOUT le contenu de ce dossier (en respectant l'arborescence,
   y compris `.github/workflows/build-apk.yml`).
3. Onglet **Actions** : le workflow « Build APK » se lance automatiquement.
4. Téléchargez l'artifact **NCDA-ONTAP-apk** → il contient `app-debug.apk`.

### Méthode B — Android Studio
1. **File → Open** → sélectionnez ce dossier ; laissez Gradle synchroniser.
2. **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
3. APK : `app/build/outputs/apk/debug/app-debug.apk`.

### Méthode C — Ligne de commande (JDK 17 + Gradle 8.7+ + SDK 34)
    gradle :app:assembleDebug

## Installer
Copiez l'APK sur le téléphone (Android 8.0+), ouvrez-le, autorisez
« Installer des applications inconnues », puis installez. L'APK debug est signé
automatiquement : il s'installe directement.

## Fonctionnalités natives
- Bouton Retour Android → navigation interne dans le QCM.
- Export des données → sélecteur de fichiers Android (si le pont natif est activé).
- Partage → menu de partage Android (si le pont natif est activé).
- Barres système synchronisées avec le thème clair/sombre (si pont activé).
- Données du QCM conservées localement sur l'appareil (localStorage WebView).

© 2026 TMOBA — Base NS0-165 V10.02.
