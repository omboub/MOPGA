# mopga_django
Make Our Planet Green Again - Django - Université d'Angers - Master 2 ACDI

## Pré-requis
Il faut avoir sur son poste :
- python 3
- virtualenv

Si les deux paquets ne sont pas installés, vous pouvez les installer en suivant les instructions ci-dessous :
```bash
sudo apt-get install python-virtualenv python-pip python-dev
```

## Lancement en mode développement
```bash
# Se mettre à la racine du projet (là où se trouve le fichier manage.py)
cd mopga_django

# Création d'un virtualenv
virtualenv venv -p python3

# Activation du virtualenv
source venv/bin/activate

# Une fois que l'environnement virtuel est activé, il faut installé Django.
# Dans ce projet nous sommes sur Django 2.2.*
pip install Django

# lancement du serveur se développement
python manage.py runserver
```
## Effectuer des migrations dans la base de données

Pour créer et appliquer les migrations dans une base de données, exécutez les commandes ci-dessous :
```bash
# Il faut être dans le répertoire du projet et s'assurer que
# l'environnement virtuel est bien activé

# Création des migrations (les éventuels changements dans les models des applications)
python manage.py makemigrations

# Appliquer les migrations (s'il y en a) dans la base de données
python manage.py migrate
```