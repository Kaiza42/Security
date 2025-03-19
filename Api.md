

# 8. Sécurisation des API

Les API (Application Programming Interfaces) sont des points d’entrée permettant à différentes applications, services ou plateformes d’échanger des données et des fonctionnalités. Dans le cadre de Pire2Pire.com, elles jouent un rôle essentiel pour l'interconnexion des services, mais sont également des cibles potentielles d'attaques si elles ne sont pas sécurisées de manière adéquate.

## 8.1. Principales menaces contre les API


### Injection SQL et autres injections 

 Comme pour les applications web, les API peuvent être vulnérables à des attaques d’injection si les entrées ne sont pas correctement validées.

**Attaques par force brute** 

 les identifiants d'API  Les attaquants peuvent essayer de casser les identifiants d'accès API pour compromettre les systèmes.

**Vol d'identifiants API**

 Si les clés ou tokens d’API ne sont pas correctement protégés, ils peuvent être volés et utilisés pour accéder aux ressources protégées.

**Exposition excessive des données** 

 Les API peuvent par erreur exposer plus de données que nécessaire dans leurs réponses, ce qui augmente les risques de fuite de données sensibles.

**Attaques DDoS** 

 Les API peuvent être la cible d'attaques par déni de service, rendant l'application ou le service indisponible.

#### 8.2. Solutions de sécurisation des API

**Validation stricte des entrées** 

 Toutes les données envoyées à l’API doivent être validées pour éviter les injections et autres exploitations. Il est essentiel d’utiliser des bibliothèques fiables pour valider les formats JSON ou XML.

**Limitation du taux**

  Imposer des restrictions sur le nombre de requêtes envoyées à l'API sur une période donnée permet de limiter les abus (notamment contre les attaques par force brute ou DDoS).

**Utilisation de clés API et tokens**

 Chaque utilisateur ou service doit utiliser une clé API unique. Ces clés ne doivent pas être stockées en clair, ni être incluses dans le code client accessible au public. En cas de compromission, les clés doivent être rapidement régénérées.

**Contrôle d'accès basé sur les rôles (RBAC)** 

 Les droits d'accès aux différentes fonctionnalités de l'API doivent être régis par des rôles d'utilisateur. Ce contrôle d'accès basé sur les rôles est essentiel pour limiter les actions disponibles selon les permissions de chaque utilisateur (référence à la section 5.2 controle d'accès).


### 8.3. Intégration des opérations CRUD
Les **API REST** gèrent souvent les opérations **CRUD** qui sont des actions fondamentales sur les ressources. Chaque méthode d’API doit être soigneusement contrôlée pour éviter les abus :

**Create (POST)**

 Restreindre les créations de données aux utilisateurs ou services autorisés.

**Read (GET)** 

 Limiter la lecture de données sensibles aux utilisateurs avec les permissions adéquates.

**Update (PUT/PATCH)** 

 Protéger les mises à jour de données avec des contrôles d'accès renforcés.

**Delete (DELETE)**

 Restreindre cette action critique, surtout pour les données sensibles ou les comptes utilisateurs, afin de prévenir les suppressions abusives.

### 8.4. Limitation de l'exposition des données

Les API doivent toujours être configurées pour ne retourner que les données strictement nécessaires. Il est recommandé de filtrer les réponses API et d'éviter d'exposer des informations sensibles inutiles.

### 8.5. Bonnes pratiques pour le développement des API

**Design RESTful** : Suivre les principes de conception RESTful pour une gestion claire et sécurisée des ressources et des autorisations.

**Documentation de l'API** : Fournir une documentation complète de l’API aide à garantir son utilisation correcte et sécurisée par les développeurs.

**Versioning** : La gestion des versions d'API permet de maintenir la compatibilité tout en introduisant des corrections de sécurité ou des améliorations sans perturber les services en cours.

[api REST par IBM](https://www.ibm.com/fr-fr/topics/rest-apis)
