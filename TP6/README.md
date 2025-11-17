## TP6 : Déploiement d'une Application Web avec Templates Jinja2

## Objectif

Personnaliser la configuration de Nginx et déployer une application web en utilisant des templates Jinja2.

## Étapes principales

1. Création du template Nginx

Créer un fichier template pour définir la configuration du serveur web avec des variables dynamiques pour le nom du serveur et le répertoire racine des fichiers web.

2. Définition des variables

Définir le nom du serveur et le répertoire racine dans le rôle Nginx pour rendre le déploiement configurable.

3. Modification des tâches pour utiliser le template
Mettre à jour les tâches du rôle pour copier la configuration depuis le template et redémarrer le service Nginx si nécessaire.

4. Déploiement d’une page web
Créer et copier une page web sur le serveur pour qu’elle reflète les variables définies dans le template.

5. Exécution du playbook
Lancer le playbook Ansible pour appliquer les modifications sur la machine distante.
![ansible](docs/screenshots/tp66.png)

Vérification

Accéder à l’IP du serveur depuis un navigateur.Vous devriez voir la page affichant "Bienvenue sur monapplication.local".
![ansible](docs/screenshots/tp6.png)