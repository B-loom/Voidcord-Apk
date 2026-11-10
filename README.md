<div align="center">

<img src="icon.png" alt="Voidcord" width="120">

# Voidcord Apk

**Voidcord on your Android phone — your Discord accounts and your bots in one app**

[Website](https://b-loom.github.io/Voidcord-Apk/) · [Voidcord for PC](https://github.com/B-loom/Voidcord) · [What's new](CHANGELOG.md)

</div>

---

## English

Voidcord Apk is [Voidcord](https://github.com/B-loom/Voidcord) running on Android. It is not a
rewrite: it is the same server, the same API routes, the same settings screens, the same startup
animation and the same Vencord layer as the desktop version. Only what went through Electron
had to be replaced.

### How it works

On a computer, Voidcord is a local server with an Electron window in front of it, and Electron
makes the Discord client believe it is talking to `discord.com`. A WebView cannot redirect a
domain name, so the client is served from `http://127.0.0.1` — which Chromium treats as a secure
origin — and Node.js runs inside the app itself, through
[nodejs-mobile](https://github.com/nodejs-mobile/nodejs-mobile).

```
WebView ──► http://127.0.0.1:<port>/app ──► Voidcord server (Node) ──► Discord
```

### Install

Download the APK for your phone from the [releases](https://github.com/B-loom/Voidcord-Apk/releases),
open it from your file manager, and allow installation from unknown sources when Android asks.
Almost every phone sold since 2019 needs the `arm64-v8a` file.

Android 8.0 or newer. No root needed.

### What does not work yet

Some of this is Voidcord, some of it is Discord. Discord deliberately cuts features out of its
mobile web client: voice, file uploads and the GIF picker are not ours to give back. Screen
sharing has no equivalent in a WebView, game detection reads Windows processes, and Android
requires you to confirm an APK install yourself, so updates are announced rather than applied.

### Build it yourself

```bash
npm run mobile:deps   # once: downloads Node.js for Android
npm run apk:debug     # a test APK, installable as is
```

You need the Android SDK (platform 37, build-tools 36, NDK 28, CMake 3.31) and a JDK 21.

### Licence

GPL-3.0, like Voidcord.

---

## Français

Voidcord Apk, c'est [Voidcord](https://github.com/B-loom/Voidcord) sur un téléphone Android. Rien
n'a été réécrit : c'est le même serveur, les mêmes routes, les mêmes écrans de réglages, la même
animation de démarrage et le même calque Vencord que sur l'ordinateur. Seul ce qui passait par
Electron a dû être remplacé.

### Comment ça marche

Sur un ordinateur, Voidcord est un serveur local devant lequel Electron place une fenêtre, en
faisant croire au client Discord qu'il parle à `discord.com`. Une WebView ne sait pas détourner un
nom de domaine : le client est donc servi depuis `http://127.0.0.1` — que Chromium traite comme une
origine sûre — et Node.js tourne à l'intérieur de l'application, par
[nodejs-mobile](https://github.com/nodejs-mobile/nodejs-mobile).

```
WebView ──► http://127.0.0.1:<port>/app ──► serveur Voidcord (Node) ──► Discord
```

### Installer

Télécharge l'APK qui correspond à ton téléphone depuis les
[versions](https://github.com/B-loom/Voidcord-Apk/releases), ouvre-le depuis ton gestionnaire de
fichiers, et autorise l'installation de sources inconnues quand Android le demande. Presque tous
les téléphones vendus depuis 2019 veulent le fichier `arm64-v8a`.

Android 8.0 ou plus récent. Pas besoin de root.

### Ce qui ne marche pas encore

Une partie vient de Voidcord, l'autre de Discord. Discord ampute volontairement son client web
mobile : le vocal, l'envoi de fichiers et le sélecteur de GIF ne sont pas à nous de rendre. Le
partage d'écran n'a pas d'équivalent dans une WebView, la détection de jeux lit les processus de
Windows, et Android exige que tu confirmes toi-même l'installation d'un APK — les mises à jour sont
donc annoncées, pas appliquées.

### Compiler soi-même

```bash
npm run mobile:deps   # une fois : télécharge Node.js pour Android
npm run apk:debug     # un APK de test, installable tel quel
```

Il faut le SDK Android (plateforme 37, build-tools 36, NDK 28, CMake 3.31) et un JDK 21.

### Licence

GPL-3.0, comme Voidcord.
