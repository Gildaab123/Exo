# Hello world

Comme le veut la tradition tacite des dev : Toute nouveauté commence par un hello world !

Votre objectif sera donc de créer un workflow qui va démarrer un serveur Ubuntu, et afficher "Hello world !"

Vous pouvez utiliser le même répo que lors de l'exercice précédent, ou en créer un nouveau.

## Aides du poulet

Votre workflow se déclenchera lors du push devra être composé de 3 étapes :

- Définir le trigger
- Créer un serveur qui tourne sur Ubuntu
- Réaliser le checkout
- Ecrire "hello world"

## Aides du poussin

Rédigez votre workflow dans le fichier "hello-world.yml", que vous placerez dans `/.github/workflows`. Vous pouvez vous aider du pseudo-code suivant :

```pseudocode
nom

trigger : push

jobs:
    nom_du_job:
        etapes:
            - action : checkout
            - nom etape
            exécute : echo hello world
```

> Faites attention à bien respecter l'indentation si vous voulez que votre workflow soit fonctionnel !
