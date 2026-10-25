# Chronométrage

[Accueil](../README.md) · [Guide](guide.md) · **Chronométrage** · [FAQ](faq.md)

Le but : savoir combien de temps prend chaque quête et combien d'expérience par heure elle
rapporte, pour voir lesquelles valent le coup. À activer dans les paramètres :
**Chronométrer les quêtes**.

## Ce qui est mesuré

- Le temps va du moment où le PNJ vous donne la quête à celui où vous la rendez.
- **Seules les quêtes faites seules sont chronométrées** : si une mission et une tâche sont
  en cours en même temps, aucune des deux n'est mesurée (le temps de l'une compterait celui
  de l'autre). Les cartes n'affichent alors pas de chrono, et un message sous les cartes le
  rappelle.
- **Pour ne chronométrer que les missions (ou que les tâches)**, masquez l'autre type dans les
  paramètres (« Afficher les tâches » / « Afficher les missions ») : une quête prise pendant
  que l'autre type est masqué est chronométrée, même si une quête de l'autre type est en
  cours. Si vous réaffichez l'autre type alors qu'une quête de chaque type est en cours, le
  chrono s'arrête.
- Une quête abandonnée n'est pas mesurée, ni une quête rendue plus d'une heure après l'avoir
  prise (absence, quête terminée la veille et rendue le lendemain) : le chrono disparaît
  au bout d'une heure.
- Fermer et relancer l'application pendant une quête ne fait pas perdre son temps.
- Seules les quêtes faites avec le paramètre activé comptent : les anciens journaux ne sont pas
  importés.
- Il n'y a pas de pause : si vous vous absentez pendant une quête, supprimez ce temps (voir
  plus bas).

## Sur la carte

```
Temps moyen : 2:38 (2 fois) · 18,2 M xp/h
Chrono : 1:35
```

- **Chrono** : le temps écoulé depuis que vous avez pris la quête.
- **Temps moyen** : la moyenne des fois où vous l'avez faite, tous personnages confondus.
  « Temps : pas encore mesuré » tant qu'elle ne l'a jamais été.
- **xp/h** : l'expérience que la quête rapporte **à votre personnage, à son niveau actuel**,
  divisée par le temps moyen. Elle s'affiche dès que l'application connaît le niveau du
  personnage (une montée de niveau, ou une mission ou une tâche rendue).
  - En **vert** : parmi le tiers des quêtes les plus rapides de son type (mission ou tâche).
  - En **orange** : parmi le tiers des plus lentes.
  - Il faut au moins 3 quêtes du même type chronométrées pour les couleurs.

Bon à savoir : à un niveau donné, toutes les missions rapportent la même expérience, et toutes
les tâches aussi (moins qu'une mission, mais avec un bon de ravitaillement). L'application
retient ce que vos dernières mission et tâche vous ont rapporté et suit vos montées de niveau,
donc l'xp/h reste juste quand vous montez. Pour les tâches, l'xp/h ne compte pas le bon de
ravitaillement.

## Le fichier des temps

Les temps sont dans `temps_quetes.log`, dans le dossier des logs de l'application
(paramètres > « Ouvrir le dossier des logs de l'application »), classés par quête :

```
== L'orbe de tromperie (mission) ==
2026-10-22 13:35:48 | Bearh Naise | 2:39 | 780000 xp | niv. 78
2026-10-23 12:06:30 | Bearh Naise | 2:38 | 800000 xp | niv. 80
```

Chaque ligne : début, personnage, durée, expérience gagnée et niveau du personnage (absent
quand l'application ne le connaît pas encore). Pour retirer un temps faussé
(absence, déconnexion…), **supprimez sa ligne** et enregistrez le fichier, même avec
l'application ouverte. La carte en tient compte au prochain temps enregistré ou au prochain
lancement.
