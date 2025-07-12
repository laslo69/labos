# 🖧💻🐧 Lab personnel - Administration Système & Réseau

Bienvenue sur mon lab personnel dédié à l’administration système et réseau. Ce projet me permet d’explorer, tester et documenter différents services et configurations en environnement virtualisé.

## 📌 Objectifs du lab

- Mettre en place des services réseau (DHCP, DNS, Web...)
- Gérer des machines Linux dans un réseau simulé
- Superviser l’activité du réseau
- Automatiser les tâches récurrentes
- Apprendre la sécurisation de base d’un système

## 🛠️ Environnement technique

- **OS** : Ubuntu Server / Debian
- **Hyperviseur** : VirtualBox / Proxmox
- **Outils** : Wireshark, Nmap, Ansible, Bash, Zabbix

---

## 🗂️ Modules détaillés

| 📁 Module       | Description                             | Lien                       |
|----------------|-----------------------------------------|----------------------------|
| DHCP           | Serveur d’attribution IP                | [Voir documentation](./docs/01-dhcp.md) |
| DNS            | Résolution de noms                      | [Voir documentation](./docs/02-dns.md) |
| Serveur Web    | Apache/Nginx pour héberger un site      | [Voir documentation](./docs/03-serveur-web.md) |
| Supervision    | Monitoring via Zabbix ou Prometheus     | [Voir documentation](./docs/04-supervision.md) |
| Sécurité       | Firewall, Fail2Ban, gestion utilisateurs| [Voir documentation](./docs/05-securite.md) |

---

## 📸 Etapes mise en place de la solution

![Dashboard Zabbix](./screenshots/zabbix1.png)
![Configuration DHCP](./screenshots/dhcp1.png)

---

## 🧾 Scripts

Les scripts utilisés sont disponibles dans le dossier [`/scripts`](./scripts/).

---

## 🧠 Ce que j’ai appris

- Automatisation de déploiements système
- Analyse de paquets réseau
- Gestion d’accès et sécurité système
- Supervision d'une architecture réseau complète

## Feedback

Un avis, une question ou une remarque ? Laissez un commentaire !
