# Changelog — Voidcord Apk

This changelog covers the Android app only. Voidcord for PC has
[its own](https://github.com/B-loom/Voidcord).

Ce changelog ne concerne que l'application Android. Voidcord PC a
[le sien](https://github.com/B-loom/Voidcord).

---

## 1.0.0

**The first version.** Voidcord runs on Android: the whole server, its 133 API routes, the
settings screens, the account sign-in, the startup animation and the Vencord layer — the same
code as the desktop version, with Node.js running inside the app.

**La première version.** Voidcord tourne sur Android : tout le serveur, ses 133 routes, les écrans
de réglages, la connexion par compte, l'animation de démarrage et le calque Vencord — le même code
que sur l'ordinateur, avec Node.js qui tourne dans l'application.

### English

- The Voidcord server runs inside the app through nodejs-mobile, and a WebView loads the Discord
  client from `http://127.0.0.1`.
- Electron is replaced by a layer of its own: `net.fetch` and `net.request`, the log, the IPC, the
  preloads and the branding redirects.
- The startup animation plays in landscape, then the phone returns to its own orientation.
- The settings, accounts, language, message editor and captcha screens are the desktop pages,
  unchanged.
- The window title bar is hidden, and a long press opens Discord's menu instead of selecting text.

### Français

- Le serveur Voidcord tourne dans l'application par nodejs-mobile, et une WebView charge le client
  Discord depuis `http://127.0.0.1`.
- Electron est remplacé par un calque : `net.fetch` et `net.request`, le journal, l'IPC, les
  préchargements et les redirections d'images.
- L'animation de démarrage se joue en paysage, puis le téléphone retrouve son orientation.
- Les écrans de réglages, de comptes, de langue, d'éditeur de message et de captcha sont ceux du
  bureau, sans modification.
- La barre de titre est masquée, et un appui long ouvre le menu de Discord au lieu de sélectionner
  le texte.
