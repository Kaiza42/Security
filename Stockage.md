# Stratégie de stockage des données pour la cybersécurité
## 1. Sauvegardes régulières et redondance

Les sauvegardes sont essentielles pour garantir la récupération des données en cas de panne, cyberattaque ou suppression accidentelle.

- Automatisation des sauvegardes : planification régulière (quotidienne, hebdomadaire) pour éviter toute perte de données.
- Types de sauvegardes 

        Complètes : copie intégrale de la base.

        Incrémentales : enregistrement uniquement des modifications depuis la dernière sauvegarde.
- Stockage sécurisé et géographiquement distribué 

        Conservation des sauvegardes sur plusieurs serveurs sécurisés, situés à différents emplacements pour prévenir tout risque de perte totale.

        Chiffrement des sauvegardes pour éviter tout accès non autorisé.

# 2. Réplication et haute disponibilité
Afin d’assurer la continuité du service et d’éviter les interruptions, une réplication des bases de données est mise en place :

- Réplication Master-Slave : une base principale (Master) reçoit les écritures tandis que les bases secondaires (Slaves) maintiennent des copies synchronisées.

- Réplication Master-Master : plusieurs bases principales partagent la charge et garantissent une tolérance aux pannes accrue.

- Avantages 

         Basculement rapide en cas de panne.

         Répartition des requêtes pour optimiser la charge.
         
         Amélioration des performances pour un accès fluide aux données.