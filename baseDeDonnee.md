# 5. Protection de la Base de Données

## 5.1. Menaces sur la Base de Données

### Accès non autorisé à la base de données

 Une des principales menaces pour la sécurité des données stockées dans une base de données est l'accès non autorisé. Si un attaquant parvient à accéder à la base de données via des identifiants compromis, des défauts de configuration du serveur ou une mauvaise gestion des permissions, il peut avoir un contrôle total sur les données. Cela pourrait entraîner la fuite, la modification ou la suppression de données sensibles.

### Vol de données sensibles 

 Les bases de données contiennent souvent des informations sensibles des utilisateurs, telles que des mots de passe, des adresses, des numéros de téléphone, etc. Si ces informations ne sont pas correctement protégées, elles peuvent être compromises en cas d'accès non autorisé à la base de données. Une mauvaise gestion du stockage des mots de passe, par exemple, peut exposer des utilisateurs à des attaques.

 ### Exploitation des privilèges d'administrateur

 Les comptes avec des privilèges d'administration ou des permissions élevées dans la base de données sont des cibles privilégiées pour les attaquants. Si ces comptes ne sont pas correctement sécurisés (par exemple, en utilisant des mots de passe forts et une authentification multi-facteurs), ils peuvent permettre à un attaquant de prendre le contrôle complet de la base de données et de causer des dommages importants.

 Fuite d'informations à travers des requêtes non sécurisées
 Des données sensibles peuvent être exposées si les requêtes vers la base de données ne sont pas correctement sécurisées ou filtrées. Par exemple, un utilisateur malveillant peut tenter d'exploiter des failles dans des requêtes non sécurisées pour accéder à des informations qu'il ne devrait pas voir.

## 5.2. Solutions mises en place pour sécuriser la Base de Données

### Chiffrement des données sensibles

Les informations sensibles, telles que les mots de passe, doivent être chiffrées à la fois lors de leur stockage dans la base de données et lors de leur transmission via des canaux sécurisés. Cela garantit qu’en cas d'accès non autorisé à la base de données, les données volées resteront illisibles sans la clé de déchiffrement.

### Hachage et salage des mots de passe

 Le hachage des mots de passe, accompagné d'un salage unique pour chaque utilisateur, est une méthode essentielle pour sécuriser les informations de connexion. Ce processus rend impossible la récupération du mot de passe original, même si les informations de la base de données sont compromises. 

### Contrôle d'accès : WOW

Les privilèges d'accès à la base de données doivent être strictement contrôlés. Chaque compte utilisateur doit avoir un niveau d'accès minimal correspondant à ses besoins spécifiques, et l'accès aux informations sensibles doit être limité au personnel autorisé uniquement. L’utilisation de rôles d’utilisateur dans la base de données permet de gérer ces permissions.

## Segmentation de la base de données

 Pour limiter l'impact d'un éventuel piratage, il est recommandé de segmenter la base de données, en créant des bases de données ou des tables séparées pour les données sensibles. Cela permet de restreindre l'accès et de réduire la surface d'attaque en cas de compromission d'une partie du système.

 [source segmentation :](https://www.cnil.fr/fr/definition/segmentation-des-donnees)

Utilisation de requêtes préparées : Bravo genie

Pour prévenir les attaques par injection SQL, l'utilisation de requêtes préparées est une pratique incontournable. Cela garantit que les données utilisateur sont correctement échappées, évitant ainsi que des entrées malveillantes ne puissent altérer la structure de la requête.
