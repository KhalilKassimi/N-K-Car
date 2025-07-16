# NK CAR - Système de Location de Voitures

NK CAR est une application web professionnelle de gestion de location de voitures. Elle permet aux utilisateurs de parcourir une flotte de véhicules, effectuer des réservations, et gérer leur compte client.

## Fonctionnalités

- 🚗 Catalogue de véhicules avec filtres avancés
- 👤 Système d'authentification complet
- 📅 Gestion des réservations
- ⭐ Système d'avis et notations
- 💳 Suivi des paiements
- 📱 Interface responsive
- 🔒 Sécurité renforcée

## Prérequis

- PHP 7.4 ou supérieur
- MySQL 5.7 ou supérieur
- Serveur web (Apache/Nginx)
- Composer (optionnel)

## Installation

1. Clonez le dépôt dans votre répertoire web :
```bash
git clone https://github.com/votre-username/nk-car.git
```

2. Importez la base de données :
```bash
mysql -u root -p < database.sql
```

3. Configurez la connexion à la base de données :
   - Ouvrez `config/database.php`
   - Modifiez les constantes selon votre configuration :
     ```php
     define('DB_HOST', 'localhost');
     define('DB_USER', 'votre_utilisateur');
     define('DB_PASS', 'votre_mot_de_passe');
     define('DB_NAME', 'nk_car');
     ```

4. Créez le dossier pour les images de véhicules :
```bash
mkdir -p assets/images/vehicles
chmod 755 assets/images/vehicles
```

5. Assurez-vous que le serveur web a les permissions d'écriture nécessaires :
```bash
chmod -R 755 .
chmod -R 777 assets/images/vehicles
```

## Structure du Projet

```
nk-car/
├── admin/              # Interface d'administration
├── assets/
│   ├── css/           # Fichiers CSS
│   ├── js/            # Scripts JavaScript
│   └── images/        # Images du site
├── config/            # Configuration
├── includes/          # Fichiers inclus (header, footer)
├── pages/            # Pages du site
└── index.php         # Point d'entrée
```

## Utilisation

### Interface Client

1. Création de compte :
   - Accédez à la page d'inscription
   - Remplissez le formulaire avec vos informations
   - Validez votre compte via l'email reçu

2. Réservation de véhicule :
   - Parcourez le catalogue
   - Utilisez les filtres pour affiner votre recherche
   - Sélectionnez un véhicule
   - Choisissez vos dates
   - Confirmez la réservation

3. Gestion des réservations :
   - Consultez vos réservations en cours
   - Annulez une réservation si nécessaire
   - Laissez un avis après utilisation

### Interface Administrateur

1. Accès :
   - URL : `/admin`
   - Identifiants par défaut :
     - Email : admin@nk-car.fr
     - Mot de passe : admin123

2. Fonctionnalités :
   - Gestion des véhicules
   - Gestion des réservations
   - Gestion des utilisateurs
   - Statistiques et rapports

## Sécurité

- Toutes les entrées utilisateur sont validées et nettoyées
- Protection contre les injections SQL via PDO
- Mots de passe hashés avec bcrypt
- Protection CSRF sur les formulaires
- Sessions sécurisées

## Maintenance

Pour maintenir le site à jour :

1. Sauvegardez régulièrement la base de données
2. Mettez à jour les images des véhicules
3. Surveillez les logs d'erreur
4. Effectuez des tests de sécurité réguliers

## Support

Pour toute question ou assistance :
- Email : contact@nk-car.fr
- Téléphone : +33 1 23 45 67 89

## Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## Auteurs

- NK CAR Team
- Contact : dev@nk-car.fr 
