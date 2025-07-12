# 💻 Lab personnel - Administration Système

## 📌 Objectifs du lab

Mise en place d'un domaine active directory

## 🛠️ Environnement technique

- **OS** : windows Server 2022
- **Hyperviseur** : Proxmox

## 🗂️ Module détaillé

|📁 Module|Description|
|:-:|:-|
|Installation|Installation de rôle ADDS|
|Création|Création d'une fôret et d'un domaine active directory|
|Connexion|Connexion en tant que administrateur du domaine|

## 📸 Etapes mise en place de la solution

Le premier serveur qui servira de contrôleur de domaine est configuré:

- Renommer
- IP Statique

Pour l'instant, le serveur est en mode `WORKGROUP`

![AD sans contrôleur de domaine](./Illustration/crea_ad_1.JPG)

S'ensuit l'installation du rôle ADDS

![installation ADDS](./Illustration/crea_ad_2.JPG)

Comme je ne possède ni domaine existant, ni forêt existante, je crée une nouvelle forêt et un nouveau domaine que je vais nommer `lab.local`

![nommage de la forêt](./Illustration/crea_ad_3.JPG)

Définition d'un mot de passe DSRM

![definition mdp DSRM](./Illustration/crea_ad_4.JPG)

J'ai choisis de ne pas créer de délégation DNS pour pouvoir la gérer manuellement au fil du temps

![creation deleguation DNS](./Illustration/crea_ad_5.JPG)

Contrôle de la configuration avant d'installer le rôle ADDS

![installation ADDS](./Illustration/crea_ad_6.JPG)

Lors de la fin de l'installation, un reboot est nécessaire

![reboot](./Illustration/crea_ad_7.JPG)

Une fois redémarrer, on peut se connecter en tant que administrateur du domaine

![connexion](./Illustration/crea_ad_8.JPG)

## 🧠 Ce que j’ai appris

- Création d'une fôret et d'un domaine active directory
- Comment mettre en place un serveur qui fait office de contrôleur de domaine

## Feedback

Un avis, une question ou une remarque ? Laissez un commentaire !
