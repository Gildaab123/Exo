# Exercice 2 : Pull or Push ?

Votre objectif est d'utiliser le contexte `github` pour déterminer le type d'évènement qui a été déclenché.

Pour ce faire, vous créerez deux jobs différents qui réaliseront les actions suivantes :

- Si c'est un push : vous affichez "C'est un push !"
- Si c'est une pull request : vous afficherez "C'est une pull request !"

> Les messages doivent être tous deux présents dans une variable d'environnement située au top niveau de votre workflow !

Vous testez vos jobs avec un push et une pull request.

## Aides du poulet

- Vos deux jobs peuvent tourner sous `ubuntu-latest`
- Ils exécuteront tous les deux la commande `echo` et appéleront la variable d'environnement adaptée à la situation
- Vous déclarerez la variable d'environnement au top niveau, juste avant la liste des `jobs`
- Vous aurez besoin de la variable d'environnement `github.event_name` pour déterminer le type d'évènement qui a été déclenché

## Aides du poussin

- Via un bloc `if`, vous pouvez vérifier si la variable d'environnement `github.event_name` est égale à `push` ou `pull_request`
- N'oubliez pas que les triggers sont à indiquer sous forme de tableau !

### Pseudo code

```pseudocode
nom

trigger

variables d'environnement
    Push
    Pull Request

jobs
    job au push
        utilise ubuntu
        etapes
            chackout
            nom
            afficher le message
    
    job à la pull request
        utilise ubuntu
        condition si pull request
        etapes
            checkout
            nom
            afficher le message
```
