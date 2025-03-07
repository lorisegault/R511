Ce projet Ansible automatise l'installation de Apache, MariaDB et PyMySQL sur des machines distantes.
Il utilise un fichier d'inventaire (hosts.ini) pour définir les hôtes et exécute un playbook (global_role.yaml) pour déployer les modules.
Les tâches pour l’installation sont gérées via le rôle installation_logiciel.
