# T4C Quest Companion

Petite application compagnon pour **The 4th Coming** (serveur Neerya), affichée en overlay
par-dessus le jeu. Elle lit le journal de discussion du jeu en direct et détecte toute seule les
**missions** (Auxiliaire de mission) et **tâches** (Préposé aux tâches) journalières : quête en
cours, progression, objectif atteint, nombre de quêtes rendues dans la journée, et la solution
du wiki.

<img width="491" height="651" alt="image" src="https://github.com/user-attachments/assets/46f05ac8-0a28-4332-ba88-249c7223a0f2" />


## Télécharger

Dernière version : page [Releases](../../releases/latest).

- **Windows** : `t4c-quest-companion-vX.Y.Z-windows.zip`, décompresser et lancer
  `t4c-quest-companion.exe`. Windows SmartScreen peut avertir que l'application n'est pas
  signée : « Informations complémentaires » > « Exécuter quand même ».
- **Linux / SteamOS (mode Bureau)** : `t4c-quest-companion-vX.Y.Z-linux.zip`, décompresser et
  lancer `t4c-quest-companion.x86_64`.

## Avant de jouer

- La journalisation doit être activée dans le jeu, pour chaque personnage :
  **Options > Journaux > Journalisation activée**. Sans elle, le jeu n'écrit aucun journal et
  l'application ne voit rien.
- L'overlay ne peut s'afficher par-dessus T4C que si le jeu tourne en mode fenêtré
  (ou fenêtré sans bordure), pas en plein écran exclusif.
- **Windows : lancez l'application en administrateur.** Le jeu tourne en administrateur et
  réagit aux clics même quand ils sont faits sur une autre fenêtre placée par-dessus lui : sans
  droits administrateur, un clic sur l'overlay fait aussi marcher votre personnage. Pour ne pas
  avoir à y penser : clic droit sur `t4c-quest-companion.exe` > Propriétés > Compatibilité >
  cocher « Exécuter ce programme en tant qu'administrateur ». Windows demandera alors la
  confirmation à chaque lancement.
  Avec les droits administrateur, l'overlay prend le contrôle quand le curseur reste un instant
  sur un bouton (paramètres, fermer, liste des personnages…) et le rend au jeu dès que le
  curseur s'en va : vos clics sur ces boutons n'atteignent plus le jeu.

Le dossier des logs du jeu est détecté automatiquement :

- Windows : `%LOCALAPPDATA%\Dialsoft\Logs`
- Linux (Bottles, Proton, Wine) : `…/drive_c/users/<utilisateur>/AppData/Local/Dialsoft/Logs`
  dans le préfixe Wine

Sinon, le choisir dans les paramètres (icône d'engrenage).

## Signaler un problème

Ouvrir une [issue](../../issues) en joignant, si une quête n'est pas détectée, le fichier
`non_reconnues_AAAA-MM-JJ.log` du jour. Il se trouve dans `%APPDATA%\T4C Quest Companion\logs`
(Linux : `~/.local/share/T4C Quest Companion/logs`), accessible depuis les paramètres.

## Crédits

© 2026 Skwal. Application non officielle, sans lien avec Dialsoft ni avec le serveur Neerya.

- Graphismes de l'interface et police : *The 4th Coming* © Dialsoft, empruntés au jeu.
- Textes des solutions : [wiki Neerya](https://t4c-neerya.com/wiki).
- Police Noto Sans : SIL Open Font License.
