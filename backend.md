## 4. *Sécurisation du Back-End*

### **introduction Back-end**

Le back-end représente la colonne vertébrale de la plateforme Pire2Pire.com, orchestrant les fonctionnalités critiques invisibles aux utilisateurs mais essentielles au bon fonctionnement du service. Cette infrastructure centrale gère l'authentification, les sessions utilisateurs, le traitement des données et les interactions avec la base de données.

La sécurisation de cet environnement constitue un enjeu majeur, car toute compromission à ce niveau pourrait avoir des répercussions catastrophiques sur l'ensemble de l'écosystème. Les attaquants ciblent fréquemment cette couche applicative en raison de son accès privilégié aux données sensibles et aux ressources système.

Cette section présente notre approche globale pour protéger le back-end contre les menaces potentielles. Nous y détaillons les vulnérabilités identifiées ainsi que les mécanismes et bonnes pratiques implémentés pour garantir la confidentialité, l'intégrité et la disponibilité des données et services de la plateforme Pire2Pire.com.

## 4.1 **Menaces sur le Back-End**

### 1. **Injection SQL** 

L'attaque par injection SQL survient lorsqu'un attaquant parvient à insérer du code malveillant dans une requête SQL via des champs de saisie non sécurisés. Cela permet à l'attaquant d'exécuter des commandes SQL arbitraires sur la base de données, compromettant ainsi la confidentialité et l'intégrité des données.

[doc Cnil a propos de l'injection SQL](https://www.cnil.fr/fr/definition/injection-sql)

[doc wikipedia a porpos de l'injection SQL](https://fr.wikipedia.org/wiki/Injection_SQL)

### 2. **Weak Authentication** <!-- => logique  -->

 Une authentification faible se produit lorsque des mécanismes de validation des utilisateurs sont insuffisants, tels que des mots de passe simples ou des méthodes d'authentification obsolètes. Cela permet aux attaquants de contourner facilement les mesures de sécurité et d'accéder aux ressources protégées.

 [anssi](https://cyber.gouv.fr/sites/default/files/2021/10/anssi-guide-authentification_multifacteur_et_mots_de_passe.pdf)

 ### 3. **Insufficient Access Control** <!--=> logique  -->

 Si les contrôles d'accès ne sont pas correctement implémentés, les utilisateurs peuvent accéder à des données ou des fonctionnalités qu'ils ne devraient pas pouvoir utiliser. Cela peut être dû à une mauvaise gestion des rôles et des permissions.

