# principe Defense en profondeur 

L'idée derrière la défense en profondeur est de sécuriser chaque couche du système indépendamment des autres. Cela signifie que, même si le front-end venait à être compromis, le back-end et la base de données continueraient à protéger leur partie respective, empêchant ainsi un accès non autorisé ou une compromission complète du système.

- **Isoler les composant** : chaque composant doit être isoleé afin de si un élément est compromis le saitre continuent de fonctionner en toute sécurité. dans l'idée si le **front-end** est attaqué, le back-end est la base de données resteront sécurisés cela inclut : 
    

- **Reduire la surface d'attaque** : Minimiser l'exposition des service et des points d'entrée est essetiel pour rendre l'attaque plus difficile. cela passe par : 

    - **Restriction des accès** : en ne rendant disponibles que les fonctionnalités strictement nécessaires, le sustèmme reduit le nombre de point d'entrée vulnérables.

    - **utilisation de mécanisme de sécurité par défaut** : cela inclut l'application des meilleures partiques de sécurité, telles que l'utilisation de protocoles sécurisés tel que HTTPS et SSH la désactivation de service non utilisés et le verrouillage des paramètres par defaut 
       - **désactivation des service non utilisés** si un service n'est plus nécessaire il doit etre désactivé pour éviter une entré possible pour les attaquant.

## 2.2. Confidentialité, Intégrité et Disponibilité

La sécurité des informations repose sur tois principe clés : Confidentialité, Intégrité et Disponibilité.
Ces Principes sont essentiles pour protéger les données des utilisateurs et garantir le bon fonctionnement de la plateforme Pire2Pire.com

**Integrité**

L'intégrité garantit que les données restent exactes et ne sont pas modifié de manière non autorisée.
Des Techniques telles que le **hashing des mots de passes** et l'utilisatio de **signature numérique** sont utilisées pour protéger l'exactitude des données.

**Disponibilité**

La **Disponibilité** assure que la plateforme reste accessible aux utilisateur à tout moment.
Cela inclut la mise en place de **sauvegarde régulières**, de **serveur redondants**, et des protections contre les attaques par déni de service (DDoS) pour garantir le accès aux services.

**maintien de l'équilibre** 

Il est important de maintenir un équilibre entre ces trois principes, car un déséquilibre pourrait entraîner des problèmes tels que des ralentissements ou une inaccessibilité des informations pour l'utilisateur. Par exemple, si l'accent est trop mis sur la confidentialité, cela pourrait ralentir l'accès aux données ou compliquer l'expérience utilisateur.

