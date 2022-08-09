<p align="center">
  <a href="" target="blank"><img src="Img/JMeriseLogoPetit.png" width="200" alt="merise Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

  <p align="center">Une méthodologie de modélisation à usage général dans le domaine du
développement de systèmes d’information.</p>
    <p align="center">
<a href="#" target="_blank"><img src="https://img.shields.io/badge/merise-merise-green" alt="Merise" /></a>
 
</p>
   

## Description

Merise est une méthodologie de modélisation à usage général dans le domaine du
développement de systèmes d’information, du génie logiciel et de la gestion de projet.
Introduit pour la première fois au début des années 1980, il était largement utilisé en France.
Il a été développé et perfectionné à un point tel que la plupart des grandes organisations
gouvernementales, commerciales et industrielles françaises l'ont adopté.

## Trois cycles fondamentaux 

```bash
 
MERISE présente dans sa démarche d’analyse trois cycles fondamentaux :
    - le cycle d’abstraction,
    - le cycle de vie (de developpement),
    - le cycle de décision.
  
```
  <p align = 'center' ><img src="Img/Synoptique_Methode_Merise_2.jpg" width="200" alt="merise Logo" /> </P>

## Le Dictionnaire de Données
  Le dictionnaire des données est un document qui regroupe toutes les données que vous aurez à conserver dans votre base (et qui figureront donc dans le MCD). Pour chaque donnée, il indique :

    - Le code mnémonique : il s'agit d'un libellé désignant une donnée (par exemple «titre_l» pour le titre d'un livre)

    - La désignation : il s'agit d'une mention décrivant ce à quoi la donnée correspond (par exemple «titre du livre»)

    - Le type de donnée :

        A ou Alphabétique : lorsque la donnée est uniquement composée de caractères alphabétiques (de 'A' à 'Z' et de 'a' à 'z')

        N ou Numérique : lorsque la donnée est composée uniquement de nombres (entiers ou réels)

        AN ou Alphanumérique : lorsque la donnée peut être composée à la fois de caractères alphabétiques et numériques

        Date : lorsque la donnée est une date (au format AAAA-MM-JJ)

        Booléen : Vrai ou Faux

    La taille : elle s'exprime en nombre de caractères ou de chiffres. Dans le cas d'une date au format AAAA-JJ-MM, on compte également le nombre de caractères, soit 10 caractères. Pour ce qui est du type booléen, nul besoin de préciser la taille (ceci dépend de l'implémentation du SGBDR).

    Et parfois des remarques ou observations complémentaires (par exemple si une donnée est strictement supérieure à 0, etc).
     

## Règles de gestion

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```
## MCD
## MLD
## MPD

## Breif

pire2pire.com : Conception BDD avec MERISE

Votre mission est de concevoir la base de données d’une plateforme de formation en ligne nommée pire2pire.com à l'aide de la méthode MERISE.

## Livrables

- Un dépôt Github recensant : 
    - Un README explicite et soigné
    - Une définition de l'acronyme MERISE dans le README.md
    - Un dictionnaire de données
    - Des règles de gestion
    - Un MCD
    - Un MLD
    - Un MPD
    - Un script SQL de la base de données

## Stay in touch

-  Prasanna Balasubramaniyam

 

 