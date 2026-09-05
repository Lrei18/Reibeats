# Publier une mise à jour Reibeats

Reibeats 2.7+ peut se mettre à jour automatiquement via les **GitHub Releases** de ce dépôt public.

## Configuration unique

Le dépôt officiel est :

`Lrei18/Reibeats`

Dans ton dossier source Reibeats :

1. lance `CONFIGURE_UPDATES.bat` ;
2. entre exactement `Lrei18/Reibeats` ;
3. relance `BUILD_EXE.bat` ;
4. teste `dist\Reibeats\Reibeats.exe` ;
5. lance `BUILD_INSTALLER.bat` ;
6. réinstalle cette build configurée et partage-la.

## À chaque nouvelle version

1. Mets à jour le numéro de version dans Reibeats et les métadonnées de build.
2. Lance `BUILD_EXE.bat` puis `BUILD_INSTALLER.bat`.
3. Dans GitHub, ouvre **Releases** puis **Draft a new release**.
4. Crée un tag du type `v2.7.1`.
5. Ajoute les deux fichiers produits dans `installer_output` :
   - `Reibeats-Setup-X.Y.Z.exe`
   - `SHA256.txt`
6. Publie la Release.

Au prochain démarrage, Reibeats consulte la dernière Release publique. S'il trouve une version plus récente, il propose de la télécharger, vérifie le SHA-256 lorsqu'il est disponible, lance l'installateur puis ferme Reibeats.

## Règles importantes

- Le nom de l'installateur doit commencer par `Reibeats-Setup-` et finir par `.exe`.
- Le tag doit contenir la version, idéalement `vX.Y.Z`.
- Garde le même `AppId` Inno Setup pour que les mises à jour remplacent proprement l'installation précédente.
- Le dépôt doit rester public pour que Reibeats puisse consulter les Releases sans compte GitHub ni token.
