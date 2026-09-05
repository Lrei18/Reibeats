# Reibeats

Overlay Spotify pour Windows, pensé pour rester discret au-dessus d'un jeu en mode fenêtré sans bordure.

## Version actuelle

**Reibeats 2.7.0**

Principales fonctions :
- contrôle Spotify : lecture/pause, précédent/suivant, shuffle, répétition, volume ;
- bibliothèque, favoris, recherche, récents et playlists ;
- mode compact ;
- thèmes et thème personnalisé ;
- verrouillage de fenêtre ;
- assistant de connexion Spotify via OAuth PKCE ;
- mises à jour intégrées via les GitHub Releases.

## Télécharger

Les versions publiques de Reibeats seront publiées dans **Releases**. L'utilisateur final n'a besoin que du fichier :

`Reibeats-Setup-X.Y.Z.exe`

À partir de la 2.7.0, Reibeats peut vérifier automatiquement si une version plus récente est disponible.

## Configuration Spotify

Chaque utilisateur crée sa propre application dans Spotify for Developers et renseigne son propre **Client ID**.

Redirect URI :

`http://127.0.0.1:8888/callback`

Aucun Client Secret n'est intégré dans Reibeats.

## Mises à jour

Le dépôt utilisé par l'updater est :

`Lrei18/Reibeats`

Pour publier une nouvelle version, voir `PUBLISH_UPDATE.md`.
