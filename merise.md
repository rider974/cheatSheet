# Merise Concept 


## MCD

MCD est un Modéle conceptuel de données. Il représente les tables d'une partie ou tout une base de données relationnelle.

Appelés aussi Modéle Entités Associations. 

### Clé primaire 

C'est un identifiant qui est unique à chaque ligne. Toutes les tables doivent possèder une clé primaire. 

### CIF ET CIM

Contrainte d'intégrité fonctionnelle fait référence à une association de la forme O,N <-> 1,1 entre deux tables 
Contraintes d'intégrité Multiple. Cas où il y a une association de la forme 0,N <-> 0,N entre deux tables



### association reflexive  

Une association qui relie une table à elle-même. 


### L'intérêt des contraintes d'association est d'avoir des données cohérentes et conformes aux règles de gestion établis. 


## MLD 

Le modèle logique de données traduit le MCD en entités/relations plus précise et plus proche de ce qui va être implémenté en BDD. Les clés étrangères et primaires sont spécifiés et les tables sont reliés entre elles. Les associations CIM deviennent des tables. 

## Intégrité 

Les intégrités fonctionnels relatif au métier. Une commande doit contenir un repas. Ces contrôles peuvent être vérifier à l'aide de trigger (à chaque ajout sur la table/update sur la table/delete sur la table).

Les intégrités physique sont des contraintes directement ajoutées sur des champs ou des tables de la bdd. Exemple: champ not null, nombre de caractères limité, clé primaire, clé étrangère, clé unique, type de données

## MPD 

Le Modèle Physique de données est adapté au SGBD sur lequel va être implémenter les entités/tables/relations.

Il faut ajouter des contraintes qui vont renforcer l'intégrité des données 

### Renforcement de l'intégrité 

- Ajout des contraintes CHECK ==> Verifie qu'une données est conforme. Exemple CHECK (Quantity >0)
- Ajout d'Index qui vont ajouter une rapidité sur certains champs et ralentir d'autres. Exemple: titre d'un livre lors d'une recherche en BDD
- Ajout de contraintes NOT NULL. Exemple : Des champs obligatoires comme le nom, prenom, 
- Ajout de contraintes UNIQUE pour des champs qui doivent avoir une valeur unique. Exemple: des adresses mails, des titres, noms de status

## Dictionnaire de données 

Le dictionnaire de données va lister toutes les données collectées en base de données 

Il peut être décomposer comme suit: 

| Entité | Attribut | Type de données | Longueur | Contraintes | Description | Exemple | 


## La normalisation 

Le but de la normalisation est de réduire les redondances, maximiser l'intégrité et la cohérence des données, optimiser les requêtes. 

### 1NF 

Chaque table doit contenir des valeurs atomiques. Exemple: décomposer les données Nom en Nom et prenom. Adresse en nom rue, numero de rue, code postal, ville, ...

- Chaque colonne doit contenir des valeurs du meme type 
- Chaque ligne est unique 

### 2NF 

Doit être en 1NF + chaque champ doit dépendre de la clé primaire de la table. Exemple: table utilisateur ne peut pas contenir un nom de commande ou de produit. Comme commande ne peut pas contenir l'id et le nom de l'utilisateur car le nom de l'utilisateur dépend de son id. 

Vérifier que la 2NF est respecter en pensant aux redondances de données. Une 2NF élimine les données en trop. 

### 3NF 

Doit être en 2NF + chaque champ doit dépendre de la clé primaire et non d'une clé étrangère sur la table ou sur un autre champ de la table. Tous les champs dans une table doivent dépendre d'une clé primaire et être relié à celle-ci. 


