# CID · Environnement de démonstration

Réplique du Centre d'Intelligence des Données destinée aux présentations et aux
démonstrations fonctionnelles.

## Nature des données

**Les valeurs affichées dans cet environnement sont simulées.** Elles servent à
montrer le fonctionnement des modules et à faire tourner des simulations sur
vingt-quatre mois. Elles n'ont aucune valeur officielle et ne doivent être ni
citées, ni exportées, ni transmises comme des résultats du système de santé.

Les données réelles du MSPP se trouvent sur l'environnement de production :
https://ups-sante.github.io/CID/

## Fonctionnement

La couche de simulation est isolée dans `demoValue()`. Elle intervient uniquement
lorsque la source réelle ne renvoie rien. Les modules alimentés par un export réel
présent dans le dépôt continuent d'afficher ces valeurs.

La génération est déterministe : une même métrique, province et période produit
toujours le même nombre, ce qui permet de rejouer une démonstration à l'identique.
Une petite part des couples reste volontairement non renseignée pour que le
traitement ND demeure visible.

Période couverte : juillet 2024 à juin 2026. L'affichage est borné à juin 2026.

## Retour au réel

Quand un export réel arrive, il suffit de le déposer dans le dépôt de production.
Aucune modification de cet environnement n'est nécessaire.
