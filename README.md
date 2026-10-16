# PROVAC TECH ASSIST — Prototype GitHub Pages

Application web progressive (PWA) de démonstration pour l'assistance technique SAV.

## Contenu du dépôt
- `index.html` : application responsive (recherche, création de fiches, validation et tableau de bord)
- `manifest.json` : installation sur l'écran d'accueil Android
- `sw.js` : cache des fichiers statiques pour accès hors connexion après première ouverture
- `icons/logo.svg`, `icon-192.png`, `icon-512.png`, `favicon.png` : identité visuelle du prototype
- `.nojekyll` : publication directe sous GitHub Pages

## Mise en ligne depuis un téléphone
1. Créer un dépôt GitHub, idéalement **privé** tant que le projet n'est pas autorisé en interne.
2. Ajouter le contenu du ZIP **à la racine** du dépôt, et non le dossier parent.
3. Pour publier une démo sur GitHub Pages, vérifier l'autorisation de l'entreprise et les règles de visibilité du dépôt. Ouvrir Settings > Pages > Build and deployment > Deploy from a branch, choisir `main` et `/ (root)`, puis enregistrer.
4. Quand la page est disponible, l'ouvrir dans Chrome Android. Menu ⋮ > Installer l'application (ou Ajouter à l'écran d'accueil).

## Test du scénario
- Mode technicien : menu `Signaler` → remplir et envoyer une fiche fictive.
- Mode référent : menu déroulant du rôle → `Validation` → approuver la fiche.
- Mode technicien : revenir à `Consulter` pour rechercher la fiche publiée.
- Le rôle est simulé par un simple menu : **ce n'est pas une authentification**.

## Limites et sécurité
- Aucun cloud, aucun login, aucun partage inter-appareils. Les fiches sont sauvegardées dans le localStorage du navigateur, sur l'appareil courant.
- Le mode référent et les niveaux d'accès sont uniquement une simulation d'interface et ne protègent pas les données.
- Ne pas ajouter de documents internes, données clients, photos réelles ou procédures confidentielles.
- Les exemples de panne sont fictifs et ne constituent pas des instructions techniques.
- Les fiches importées depuis JSON ne doivent contenir que des données fictives.
- Pour une vraie utilisation collective : accord de Provac/DSI, authentification professionnelle côté serveur, rôles vérifiés côté serveur, stockage sécurisé, validation des procédures et conformité RGPD.
- L'installation PWA et le cache nécessitent HTTPS (GitHub Pages le fournit) ou localhost.

## Évolution possible
Une fois le prototype validé, brancher une API sécurisée sur un stockage professionnel approuvé (Microsoft 365 / SharePoint, ou autre solution validée par la DSI) pour permettre la synchronisation et un véritable workflow d'approbation.
