# 💻 TP personnel - Administration Système & Réseau

## 📌 Objectifs du TP

Création d'unitées d'organisation dans le but de gérer plus efficacement les groupes, utilisateurs, pc présent dans l'active directory et dans le futur, mettre en place une gestion des droits via la méthode AGDLP

## 🛠️ Environnement technique

- **OS** : Windows Server 2019
- **Hyperviseur** : Hyper-V

## 🗂️ Modules détaillés

|Module|Description|
|:-:|:-:|
|Création OU|Création des unitées d'organisation|
|Gestion Object AD|Déplacer les ressources existantes dans la bonne OU|
|Ajout utilisateur|Ajout d'utilisateur dans l'OU respective|

## 📸 Etapes mise en place de la solution

Dans la console `utilisateurs et ordinateurs active directory`, je crée 2 nouvelles unitée d'organisation:

- Utilisateurs : Permettera de regrouper tout les utilisateurs créer
- grp_utilisateurs : Permettera de regrouper tout les groupes créer

![creation ou](./Illustration/crea_ou_1.JPG)

Dans mon unitée d'organisation grp_utilisateurs, je vais créer des groupes de sécurité pour pouvoir attribuer des groupes à mes utilisateurs

![creation_groupe](./Illustration/crea_groupe_1.JPG)

Dans mon unité d'organisation utilisateurs, je vais créer quelques utilisateurs

![creation user](./Illustration/crea_user_1.JPG)

On retrouve nos utilisateurs créer

![creation user](./Illustration/crea_user_2.JPG)

## 🧠 Ce que j’ai appris

Comment créer, déplacer, supprimer des unités d'organisation et l'importance des unités d'organisation au sein d'un domaine active directory pour cloisonner les ressources
