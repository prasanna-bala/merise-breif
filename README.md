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
  
  <p align = 'center' ><img src="Img/Entity.png" width="200" alt=" " /> </P>

## Règles de gestion
  

  Une règle de gestion peut représenter une disposition légale, une exigence formulée par un client ou un article de règlement interne. A l'origine des règles de gestion, on trouve souvent de simples observations telles que "les clients appellent un numéro vert pour passer commande". Lors du processus de conception, ces observations sont formulées plus en détails (par exemple, "quelles sont les informations fournies par un client lorsqu'il passe commande ou combien un client peut-il dépenser en fonction du crédit dont il dispose".

  Les règles de gestion complètent vos diagrammes avec des informations qui ne peuvent pas être facilement représentées de façon graphique, et peuvent guider la création d'un modèle. Par exemple, la règle "un employé ne peut appartenir qu'à une seule division à la fois" peut vous aider à créer de façon graphique le lien entre un employé et une division. Les règles de gestion sont générées dans le cadre de la génération intermodèle et peuvent être spécifiées plus en détails dans le modèle généré.
 

    - Un apprenant est caractérisé par un code d'inscription unique (UUID), un nom, un prénom, une adresse, une date de naissance.
    - Un formateur est caractérisé par un code unique (auto-incrément), un nom, un prénom.
    - Un module est caractérisé par un numéro en Sémantique Versionning, un intitulé, un objectif pédagogique, un contenu (un texte et/ou une image et/ou une vidéo), une durée (heures), - - un ou plusieurs tags, un auteur (formateur).
    - Une formation est un nom.
    - Un module contient un ou plusieurs contenus et un contenu à un seul module.
    - Un module contient un ou plusieurs tags et un tag à un plusieurs module.
    - Un module peut concerner un ou plusieurs formations et une formation à un ou plusieurs module.
    - Une formation est organisé par un seul formateur et un formateur organise une à plusieurs formations.
    - Un formateur peut être auteur d'un ou plusieurs modules et un module est écris par un seul formateur.
    - Un apprenant peut s'inscrire à un ou plusieurs formations et une formation à un ou plusieurs apprenants.
    - Un apprenant est évaluer pour un ou plusieurs modules (avec un état de fin de module: OK / KO) et un module est évaluer par zéro ou plusieurs apprenants.


## MCD -Modèle conceptuel des données
  Le modèle conceptuel des données (MCD) a pour but d'écrire de façon formelle les données qui seront utilisées par le système d'information. Il s'agit donc d'une représentation des données, facilement compréhensible, permettant de décrire le système d'information à l'aide d'entités.  

  <p align = 'center' ><img src="Img/MCD.png" width="200" alt="merise Logo" /> </P>

  ### Relations et classes de relation

  Une relation (appelée aussi parfois association) représente les liens sémantiques qui peuvent exister entre plusieurs entités. Une classe de relation contient donc toutes les relations de même type (qui relient donc des entités appartenant à des mêmes classes d'entité). Une classe de relation peut lier plus de deux classes d'entité. Voici les dénominations des classes de relation selon le nombre d'intervenants :

    une classe de relation récursive (ou réflexive) relie la même classe d'entité
    une classe de relation binaire relie deux classes d'entité
    une classe de relation ternaire relie trois classes d'entité
    une classe de relation n-aire relie n classes d'entité


## MLD Modèle Logique de Données
  Un modèle logique de données (MLD) est la représentation des données d'un système d'information. Les données sont représentées en prenant en compte le modèle technologique qui sera utilisée pour leur gestion.
    <p align = 'center' ><img src="Img/mdl.png" width="200" alt="merise Logo" /> </P>

## MPD Modèle physique des données


Le Modèle Physique de Données est la transformation du MLD dans le format d'une base de données. Dans le MLD, nous avons découvert les tables, les champs, et les clefs. Le MPD est le schéma correspondant à une base de données spécifique : Oracle, MySQL, PostgreSQL, etc... Un MLD pourra générer plusieurs MPD, si vous décidez d'adapter votre base de données à votre client.

Le résultat final sera un script SQL qui permettra de créer la base dans le SGBDR. Ici va apparaître la valeur et longueur des données. Le résultat est beaucoup moins lisible. 
  ```bash
      apprenant = (apprenant_id SMALLINT, apprenant_nom VARCHAR(50) , apprenant_prenom VARCHAR(50) , apprenant_address VARCHAR(50) , apprenant_email VARCHAR(50) , 
        apprenant_password VARCHAR(50) , apprenant_datedenaissance DATE, formation_id SMALLINT, subscritiondate DATE, status_ VARCHAR(50) , createddate DATE, 
        updateddate DATE);
      formateur = (formateurs_id SMALLINT, formateurs_name VARCHAR(50) , formateurs_surname VARCHAR(50) , formateurs_status VARCHAR(50) , 
              formateurs_competance VARCHAR(100) );
      Module_formation = (Module_id SMALLINT, Module_name VARCHAR(100) , formation_id SMALLINT, Module_startdate DATE, Module_enddate DATE, Module_status VARCHAR(50) );
      course_material = (course_material_id SMALLINT, course_material_name VARCHAR(50) , course_material_file VARCHAR(100) , course_material_status VARCHAR(50) 
              , course_material_type VARCHAR(50) , module_id SMALLINT);
      Evaluation = (Evaluation_id SMALLINT, module_id SMALLINT, apprenant_id VARCHAR(50) , evaluation_date DATE, evaluation_status VARCHAR(50) , formationid SMALLINT);
      Formation = (formation_Id SMALLINT, formation_name VARCHAR(50) , formation_description VARCHAR(250) , formation_startdate DATE, formation_enddate DATE, 
                          formation_status VARCHAR(50) , #formateurs_id);
      participer = (#apprenant_id, formationindex SMALLINT, #formation_Id);
      course = (#formation_Id, #Module_id);
      include = (#Module_id, #course_material_id);
      evaluae = (#apprenant_id, #Evaluation_id, apprenant_evaluationindex SMALLINT);
      exame = (#Module_id, #Evaluation_id, evaluationmoduleindex SMALLINT);

  ```
 
 
  <p align = 'center' ><img src="Img/MDP1.png" width="200" alt="merise Logo" /> </P>
 
## SQL Script 
  ```bash
 
      CREATE TABLE apprenant(
        apprenant_id SMALLINT,
        apprenant_nom VARCHAR(50)  NOT NULL,
        apprenant_prenom VARCHAR(50)  NOT NULL,
        apprenant_address VARCHAR(50)  NOT NULL,
        apprenant_email VARCHAR(50)  NOT NULL,
        apprenant_password VARCHAR(50)  NOT NULL,
        apprenant_datedenaissance DATE,
        formation_id SMALLINT NOT NULL,
        subscritiondate DATE NOT NULL,
        status_ VARCHAR(50)  NOT NULL,
        createddate DATE NOT NULL,
        updateddate DATE,
        PRIMARY KEY(apprenant_id),
        UNIQUE(apprenant_email)
      );

      CREATE TABLE formateur(
        formateurs_id SMALLINT,
        formateurs_name VARCHAR(50)  NOT NULL,
        formateurs_surname VARCHAR(50)  NOT NULL,
        formateurs_status VARCHAR(50)  NOT NULL,
        formateurs_competance VARCHAR(100)  NOT NULL,
        PRIMARY KEY(formateurs_id)
      );

      CREATE TABLE Module_formation(
        Module_id SMALLINT,
        Module_name VARCHAR(100)  NOT NULL,
        formation_id SMALLINT NOT NULL,
        Module_startdate DATE NOT NULL,
        Module_enddate DATE NOT NULL,
        Module_status VARCHAR(50)  NOT NULL,
        PRIMARY KEY(Module_id)
      );

      CREATE TABLE course_material(
        course_material_id SMALLINT,
        course_material_name VARCHAR(50)  NOT NULL,
        course_material_file VARCHAR(100)  NOT NULL,
        course_material_status VARCHAR(50)  NOT NULL,
        course_material_type VARCHAR(50)  NOT NULL,
        module_id SMALLINT NOT NULL,
        PRIMARY KEY(course_material_id)
      );

      CREATE TABLE Evaluation(
        Evaluation_id SMALLINT,
        module_id SMALLINT NOT NULL,
        apprenant_id VARCHAR(50)  NOT NULL,
        evaluation_date DATE NOT NULL,
        evaluation_status VARCHAR(50)  NOT NULL,
        formationid SMALLINT NOT NULL,
        PRIMARY KEY(Evaluation_id)
      );

      CREATE TABLE Formation(
        formation_Id SMALLINT,
        formation_name VARCHAR(50)  NOT NULL,
        formation_description VARCHAR(250)  NOT NULL,
        formation_startdate DATE NOT NULL,
        formation_enddate DATE NOT NULL,
        formation_status VARCHAR(50)  NOT NULL,
        formateurs_id SMALLINT NOT NULL,
        PRIMARY KEY(formation_Id),
        UNIQUE(formation_name),
        FOREIGN KEY(formateurs_id) REFERENCES formateur(formateurs_id)
      );

      CREATE TABLE participer(
        apprenant_id SMALLINT,
        formationindex SMALLINT NOT NULL,
        formation_Id SMALLINT NOT NULL,
        PRIMARY KEY(apprenant_id),
        FOREIGN KEY(apprenant_id) REFERENCES apprenant(apprenant_id),
        FOREIGN KEY(formation_Id) REFERENCES Formation(formation_Id)
      );

      CREATE TABLE course(
        formation_Id SMALLINT,
        Module_id SMALLINT,
        PRIMARY KEY(formation_Id, Module_id),
        FOREIGN KEY(formation_Id) REFERENCES Formation(formation_Id),
        FOREIGN KEY(Module_id) REFERENCES Module_formation(Module_id)
      );

      CREATE TABLE include(
        Module_id SMALLINT,
        course_material_id SMALLINT,
        PRIMARY KEY(Module_id, course_material_id),
        FOREIGN KEY(Module_id) REFERENCES Module_formation(Module_id),
        FOREIGN KEY(course_material_id) REFERENCES course_material(course_material_id)
      );

      CREATE TABLE evaluae(
        apprenant_id SMALLINT,
        Evaluation_id SMALLINT,
        apprenant_evaluationindex SMALLINT NOT NULL,
        PRIMARY KEY(apprenant_id, Evaluation_id),
        FOREIGN KEY(apprenant_id) REFERENCES apprenant(apprenant_id),
        FOREIGN KEY(Evaluation_id) REFERENCES Evaluation(Evaluation_id)
      );

      CREATE TABLE exame(
        Module_id SMALLINT,
        Evaluation_id SMALLINT,
        evaluationmoduleindex SMALLINT NOT NULL,
        PRIMARY KEY(Module_id, Evaluation_id),
        FOREIGN KEY(Module_id) REFERENCES Module_formation(Module_id),
        FOREIGN KEY(Evaluation_id) REFERENCES Evaluation(Evaluation_id)
      );

  
```
  <p align = 'center' ><img src="Img/mpd.png" width="200" alt="merise Logo" /> </P>

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

##  Author

-  Prasanna Balasubramaniyam

 

 