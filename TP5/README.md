# TP5 : Utilisation des Rôles Ansible

## Objectif
Structurer un projet Ansible en utilisant des rôles pour faciliter la réutilisation et l’organisation des playbooks.

## Étapes principales
1. Créer un rôle Nginx :

ansible-galaxy init roles/nginx

Définir les variables dans roles/nginx/vars/main.yml :


nginx_package: nginx
nginx_service: nginx

Définir les tâches dans roles/nginx/tasks/main.yml :

Installer Nginx

Copier la configuration via template

Démarrer et activer Nginx

Créer le template roles/nginx/templates/nginx.conf.j2 pour configurer Nginx.

Ajouter les handlers dans roles/nginx/handlers/main.yml pour redémarrer Nginx.

Créer le playbook site.yml :


- name: Déploiement de Nginx
  hosts: webservers
  become: yes
  roles:
    - nginx
Exécuter le playbook :

ansible-playbook site.yml

Vérification
Ouvrir un navigateur sur l’IP du serveur :
La page par défaut de Nginx devrait s’afficher.