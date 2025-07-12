# 💻 Lab personnel - Administration Système

## 📌 Objectifs du lab

- Création de groupes et d'utilisateurs
- Organisation des ressources en unitées d'organisation

## 🛠️ Environnement technique

- **OS** : Windows Server 2022
- **Hyperviseur** : Proxmox

## 🗂️ Module détaillé

|📁 Module|Détail|
|:-:|:-:|
|ADDS|Utilisateurs et ordinateurs Active Directory|

## 📸 Etapes mise en place de la solution

Dans la console `utilisateurs et ordinateurs active directory`, je crée 2 nouvelles unitée d'organisation:

- Utilisateurs : Permettera de regrouper tout les utilisateurs créer
- grp_utilisateurs : Permettera de regrouper tout les groupes créer

![creation ou](./Illustration/crea_ou_1.JPG)

Dans mon unitée d'organisation `grp_utilisateurs`, je vais créer des groupes de sécurité pour pouvoir attribuer des groupes aux utilisateurs

![creation_groupe](./Illustration/crea_groupe_1.JPG)

Dans mon unitée d'organisation `utilisateurs`, je vais créer quelques utilisateurs

![creation user](./Illustration/crea_user_1.JPG)

On retrouve les 3 utilisateurs créer

![creation user](./Illustration/crea_user_2.JPG)

## 🧠 Ce que j’ai appris

- Création basique d'utilisateurs et groupes
- Importance de créer des unitées d'organisation pour gérer plus efficacement les ressources

## Feedback

Un avis, une question ou une remarque ? Laissez un commentaire !
