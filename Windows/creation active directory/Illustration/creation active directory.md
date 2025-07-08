# Creation d'un domaine active directory

## Sujet du lab

Dans ce lab, le 

Le premier serveur qui servira de contrôleur de domaine est configuré:

- Renommer
- IP Statique

Pour l'instant, le serveur est en mode `WORKGROUP`

![AD sans contrôleur de domaine](./crea_ad_1.JPG)

S'ensuit l'installation du rôle ADDS

![installation ADDS](./crea_ad_2.JPG)

Comme je ne possède ni domaine existant, ni forêt existante, je crée une nouvelle forêt que je nomme `lab.local`

![nommage de la forêt](./crea_ad_3.JPG)

Définition du mot de passe DSRM

![definition mdp DSRM](./crea_ad_4.JPG)

Je choisis de ne pas créer de délégation DNS pour pouvoir la gérer manuellement plus tard

![creation deleguation DNS](./crea_ad_5.JPG)

Contrôle de la configuration avant d'installer le rôle ADDS

![installation ADDS](./crea_ad_6.JPG)

Lors de la fin de l'installation, un reboot est nécessaire

![reboot](./crea_ad_7.JPG)

Une fois redémarrer, ont peux se connecter en tant que administrateur du domaine

![](./crea_ad_8.JPG)