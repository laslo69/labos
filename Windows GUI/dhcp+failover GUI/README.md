# 🖧 💻 Lab personnel - Administration Système

## 📌 Objectifs du lab

- Mise en place d'un DHCP pour un lan unique sans options
- Création de réservation DHCP
- Mise en place d'un Fail-over pour assurer une disponibilitée

## 🛠️ Environnement technique

- **OS** : Windows server 2022 / Windows 10 pro
- **Hyperviseur** : Proxmox

## 🗂️ Modules détaillés

|📁 Module|Description|
|:-:|:-:|
|Installation du rôle|Installation et configuration du DHCP|
|Création pool|Mise en place du pool HDCP pour le lan|
|Configuration Failover|Configuration de la solution Fail-over sur un deuxième serveur|

## 📸 Etapes mise en place de la solution

### Installation du rôle

Sur le serveur AD1, installation du rôle DHCP

![installation dhcp](./Illustration/dhcp_1.JPG)

### Création Pool DHCP

Création de l'étendu avec un nom et une description qui doit rester facilement compréhensible.

![creation pool](./Illustration/dhcp_2.JPG)

Configuration de la plage IP avec le masque réseau

J'ai choisis volontairement une plage qui permet d'exclure automatiquement, autant les serveurs que la passerelle par défaut pour éviter des potentiels conflits

![plage ip](./Illustration/dhcp_3.JPG)

Exclusion d'adresse IP qui fait parti du pool créer précédement

![exclusion ip](./Illustration/dhcp_4.JPG)

Pas de modification de la durée du bail.

Dans mon environnement de lab je n'en ai pas d'intéret.

![configuration bail](./Illustration/dhcp_5.JPG)

Ajout de la passerelle par défaut distribuer aux hôtes

![configuration gateway](./Illustration/dhcp_6.JPG)

Ajout d'un serveur DNS, ici mon serveur AD1, je n'ai pas ajouté l'AD2 en tant que DNS

![configuration DNS](./Illustration/dhcp_7.JPG)

J'ai laissé la configuration par défaut du/des serveur(s) WINS par défaut.

Je n'ai jamais apprs à utiliser les serveurs WINS, au vu de la vieillesse de cette technologie

![configuration WINS](./Illustration/dhcp_8.JPG)

Une fois finie, on active l'étendue.

Il peut être possible, que l'on doit autoriser le services DHCP sur le domaine

![activer etendue](./Illustration/dhcp_9.JPG)

Dans la console DHCP, on retrouve bien l'étendue créer avec le pool d'adresse autoriser à être distribuer ainsi que, la plage d'adresse exclue du pool

![controle etendue](./Illustration/dhcp_10.JPG)

![controle etendue](./Illustration/dhcp_11.JPG)

Ajout d'une réservation DHCP pour le serveur AD2

![reservation dhcp](./Illustration/dhcp_12.JPG)

![reservation dhcp](./Illustration/dhcp_13.JPG)

### Configuration Fail-over

Sur l'AD1, après avoir fait un click droit et choisis: configurer un basculement, une fenêtre de configuration s'ouvre

Je choisis l'étendue à configurer, ici j'en ai une seule

![choix etendue](./Illustration/dhcp_failover_1.JPG)

Je dois ensuite choisir le serveur DHCP "partenaire",qui est AD2

![ajout serveur](./Illustration/dhcp_failover_2.JPG)

Je lui défini que les 2 serveurs DHCP devront fonctionner en équilibrage de charge avec un ratio de charge équivalent à 50/50

![relation basculement](./Illustration/dhcp_failover_3.JPG)

Un petit récap' de la configuration avant la validation

![recap basculement](./Illustration/dhcp_failover_4.JPG)

Ici, sur l'AD2, on peut constater que l'étendue DHCP est bien remonter et le serveur DHCP disponible.

![dhcp ad2](./Illustration/dhcp_failover_5.JPG)

## 🧠 Ce que j’ai appris

- Installation et configuration du rôle DHCP
- Mise en place d'une étendue et des exclusions
- Création d'un basculement pour permettre une redondance du service DHCP en cas de panne
- Assurer une disponibilité accrue en faisant un doublon du service
