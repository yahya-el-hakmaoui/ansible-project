# GESTION DES UTILISATEURS AVEC ANSIBLE

## Description

Ce projet permet d’automatiser la gestion des utilisateurs (ajout, suppression, configuration SSH) sur des serveurs distants grâce à Ansible. Il facilite l’administration système en centralisant les opérations courantes liées aux comptes utilisateurs.

---

## Objectifs

- Automatiser la création, suppression et mise à jour des utilisateurs.
- Assurer un accès SSH sécurisé avec des clés publiques.
- Faciliter la maintenance des utilisateurs via un playbook Ansible réutilisable.

---

## Fonctionnalités

- Ajout automatique de comptes utilisateurs.
- Suppression ou désactivation des comptes existants.
- Déploiement des clés SSH sans mot de passe.
- Support de plusieurs serveurs (webserver, dbserver).
- Gestion simple via des fichiers YAML.
- Personnalisation des groupes, shell, et répertoires home.

---

## Prérequis

- Ansible installé sur la machine de gestion :

  ```bash
  sudo apt install ansible
Accès SSH fonctionnel vers les serveurs cibles (avec clé privée configurée).

Python installé sur les hôtes distants (prérequis d’Ansible).

## Arborescence du Projet
bash
Copy
Edit
.

├── ansible-users/

│   ├── dbserver_users.yml         # Utilisateurs pour le serveur de base de données

│   ├── webserver_users.yml        # Utilisateurs pour le serveur web

│   ├── manage_users.yml           # Playbook général de gestion des utilisateurs

│   └── inventory                  # Fichier d'inventaire listant les hôtes cibles

├── README.md                      # Documentation du projet

## Exécuter le Playbook
bash
Copy
Edit
ansible-playbook ansible-users/manage_users.yml -i ansible-users/inventory -e role_users_file=webserver_users.yml
## Auteur
Nom : yahya-el-hakmaoui

Email : yahyaelhakm@gmail.com

## Contributions
Les contributions sont les bienvenues !
N'hésitez pas à forker le projet, créer des issues ou proposer des pull requests.
