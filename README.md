# README

Ce script Python récupère les données des bars à Toulouse à partir du site [schlouk-map.com](https://www.schlouk-map.com/fr/cities/toulouse/happy-hour), extrait diverses informations telles que le nom du bar, les heures d'ouverture, les services proposés et les tarifs des boissons en happy hour. Ensuite, il crée une carte interactive avec les emplacements des bars, leurs noms, adresses, prix en happy hour et heures d'ouverture.

## Utilisation

1. Assurez-vous d'avoir Python 3.x installé sur votre système.
2. Installez les dépendances requises en exécutant `pip install -r requirements.txt`.
3. Exécutez le script principal `main.py`.

## Structure du Code

Le code est divisé en plusieurs parties :

### Partie 1 : Extraction des Données des Bars

Cette section utilise BeautifulSoup pour extraire les informations sur les bars à partir du site web. Il récupère les liens des bars, puis parcourt chaque lien pour extraire les détails tels que le nom, les heures d'ouverture, les services disponibles et les tarifs des boissons.

### Partie 2 : Analyse des Prix des Boissons

Dans cette partie, le script analyse les prix des boissons en happy hour. Il extrait les prix à partir des pages HTML des bars et les stocke dans un DataFrame. Ensuite, il calcule le prix moyen des boissons en happy hour, trouve les bars avec les prix les moins chers, et identifie le bar offrant le prix maximum et le prix minimum.

### Partie 3 : Génération d'un Rapport HTML et Envoi par Email

Cette section utilise Jinja2 pour générer un rapport HTML avec les meilleurs deals en happy hour. Ensuite, il envoie ce rapport par email à l'aide de SMTP.

### Partie Carte : Création d'une Carte Interactive

Cette partie crée une carte interactive avec les emplacements des bars, leurs noms, adresses, prix en happy hour et heures d'ouverture. La carte est générée à l'aide de Folium et sauvegardée au format HTML.

## Résultats

Les résultats sont sauvegardés dans plusieurs fichiers :
- Un fichier CSV contenant toutes les informations des bars.
- Un fichier HTML avec un rapport des meilleurs deals en happy hour.
- Une carte interactive au format HTML avec les emplacements des bars.

## Remarque

Assurez-vous d'avoir une connexion Internet active pour exécuter le script, car il récupère les données en temps réel à partir du site web.
