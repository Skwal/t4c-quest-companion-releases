# FAQ

[Accueil](../README.md) · [Guide](guide.md) · [Chronométrage](chronometrage.md) · **FAQ**

### L'application dit « Aucun journal du jeu ne bouge »

La journalisation est désactivée pour ce personnage. Dans le jeu : **Options > Journaux >
Journalisation activée**. C'est un réglage par personnage.

### L'application dit « Dossier des logs du jeu introuvable »

Ouvrez les paramètres et choisissez le dossier `Logs` du jeu avec « Parcourir… » : c'est
`%LOCALAPPDATA%\Dialsoft\Logs` sous Windows, ou le même chemin dans le préfixe Wine sous
Linux (`…/drive_c/users/<utilisateur>/AppData/Local/Dialsoft/Logs`).

### La fenêtre n'apparaît pas par-dessus le jeu

Le jeu doit être en mode fenêtré ou fenêtré sans bordure. En plein écran exclusif, rien ne
peut s'afficher par-dessus.

### Windows : un clic sur l'application fait marcher mon personnage

Lancez l'application en administrateur (voir [Avant de jouer](../README.md#avant-de-jouer)).
Le jeu tourne en administrateur et voit les clics faits sur les autres fenêtres ; avec les
mêmes droits, l'application prend la main quand le curseur reste un instant sur un de ses
boutons.

### SteamOS : ça marche en mode Jeu ?

Non, seulement en mode Bureau. Le mode Jeu ne permet pas d'afficher une autre fenêtre
par-dessus un jeu.

### Une quête n'est pas reconnue, ou sa fin n'est pas détectée

Le jeu affiche parfois un texte que l'application ne connaît pas encore. Ouvrez une
[issue](../../../issues) en joignant le fichier `non_reconnues_AAAA-MM-JJ.log` du jour (dossier
des logs de l'application, accessible depuis les paramètres) et, si possible, le journal du
jeu de ce jour-là.

### Pourquoi la carte me demande quelle quête est terminée ?

La mission et la tâche en cours finissent par le même message du jeu, l'application ne peut
pas savoir laquelle vous avez finie. Voir [« Objectif peut-être atteint »](guide.md#objectif-peut-être-atteint).

### Le compteur du jour est faux

Une quête abandonnée compte comme une quête rendue, comme pour le PNJ. Le compteur repart à
zéro à 5 h UTC (7 h en été, 6 h en hiver, heure de Paris). Une quête prise la veille et rendue
après la remise à zéro compte pour la veille, comme pour le PNJ. Les jours de bonus du serveur
(une tâche de plus), le compteur dépasse le maximum (6 / 5) : l'application ne connaît pas les
bonus.

### Je ferme l'application, je perds quelque chose ?

Non. Au lancement, l'application relit les journaux du jeu d'hier et d'aujourd'hui et retrouve
où vous en êtes, chrono compris.

### Mon temps est faussé, j'étais absent

Supprimez sa ligne dans `temps_quetes.log` : voir [Chronométrage](chronometrage.md#le-fichier-des-temps).

### L'application envoie quelque chose ?

Non. Elle lit seulement les journaux que le jeu écrit sur votre ordinateur. Au lancement, elle
demande seulement à GitHub le numéro de la dernière version publiée, sans rien envoyer
d'autre.
