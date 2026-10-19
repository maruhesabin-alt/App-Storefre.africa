# App Store Free — prototype

## Lancer en local (Visual Studio Code)
1. Dézippe le dossier et ouvre-le dans VS Code.
2. Installe l'extension **Live Server** (Ritwick Dey).
3. Clic droit sur `index.html` > **Open with Live Server**.

## Contenu
- `index.html`, `css/`, `js/` : le magasin (front-end)
- `apps/` : 2 mini-applications (calculatrice, agenda), fichiers HTML autonomes
- `files/` : 3 livres PDF d'exemple + 3 rapports ETIMARKI (documents fournis par Sabin)
- `assets/icon.svg`, `manifest.json`, `sw.js` : logo et base PWA

## Ce qui fonctionne
Navigation, recherche, installation/ouverture des mini-apps, lecture et téléchargement des PDF, création de compte, connexion avec code, récupération par questions, publication (statut « en attente »).

## Limites (honnêtes)
- Les comptes sont stockés dans le navigateur (localStorage) : un compte n'existe que sur l'appareil où il est créé.
- Le code de connexion s'affiche à l'écran : aucun e-mail n'est envoyé. Pour de vrais e-mails, il faut un backend (ex. Supabase) et un service d'envoi.
- Les fichiers publiés ne sont pas téléversés ; pas d'espace administrateur ni de modération ; pas de vrai APK.
- Icônes PWA en SVG : ajoute des PNG 192 et 512 px avant de publier en production.

## Étape suivante
Brancher Supabase (authentification, base PostgreSQL, stockage) puis héberger sur Cloudflare Pages ou Vercel.
