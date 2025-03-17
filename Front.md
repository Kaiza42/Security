Sécurisation du Front-End

Le front-end est la section de la plateforme avec laquelle les utilisateurs interagissent directement. Assurer sa sécurité est crucial pour éviter différentes menaces et offrir une expérience utilisateur fiable. Voici un aperçu des différentes vulnérabilités auxquelles le front-end peut être exposé, ainsi que les mesures spécifiques mises en place pour les prévenir et garantir une sécurité optimale.

3.1. Menaces sur le Front-End
Attaques XSS (Cross-Site Scripting)
Les attaques XSS surviennent lorsqu'un attaquant parvient à injecter du code JavaScript malveillant dans une page web. Ce code est ensuite exécuté dans le navigateur de l'utilisateur, ce qui peut permettre le vol de cookies, la manipulation de données, ou encore la redirection vers des sites malveillants.

Attaques CSRF (Cross-Site Request Forgery)
Une attaque CSRF exploite la confiance d'un utilisateur déjà authentifié. L'attaquant incite l'utilisateur à effectuer des actions non souhaitées (par exemple, modifier des informations de compte) en utilisant ses privilèges d'authentification, généralement via une requête HTTP malveillante.

Vol de session et cookies
Le vol de session est une menace courante dans le front-end. Un attaquant peut intercepter ou voler un cookie de session pour usurper l'identité d'un utilisateur authentifié et accéder à ses informations personnelles ou sensibles.

Injection de scripts via formulaires et champs de saisie
Lorsque des formulaires ne sont pas correctement sécurisés, des attaquants peuvent injecter des scripts malveillants dans des champs de saisie, ce qui peut entraîner des violations de données et des exécutions de code non autorisées sur la plateforme.


3.2. Solutions mises en place pour sécuriser le Front-End
Protection contre les attaques XSS (Cross-Site Scripting)

Validation et assainissement des entrées : Toutes les données provenant des utilisateurs sont systématiquement validées et nettoyées afin d'éviter l'injection de code malveillant. Par exemple, les champs de saisie doivent être nettoyés pour éliminer tout code HTML ou JavaScript.
Utilisation de Content Security Policy (CSP) : Cette politique permet de définir les sources autorisées pour les scripts, ce qui réduit considérablement le risque d'exécution de code non fiable.
Échappement des données : Lors de l'affichage des données saisies par les utilisateurs, des techniques d'échappement sont appliquées pour empêcher l'exécution de code JavaScript.
Protection contre les attaques CSRF (Cross-Site Request Forgery)

Tokens CSRF : À chaque action sensible effectuée sur la plateforme, un token unique est inclus dans la requête afin de vérifier que l'action provient bien de l'utilisateur légitime et non d'un site malveillant.
Vérification des méthodes HTTP : Les requêtes sensibles sont limitées à certaines méthodes HTTP (comme POST), empêchant ainsi l'envoi de requêtes via des liens.
Sécurisation des sessions et cookies

Cookies sécurisés et HttpOnly : Les cookies de session sont marqués comme "secure" et "HttpOnly" pour les protéger contre les attaques de type XSS. Cela empêche un script malveillant d'accéder au contenu du cookie.
Expiration des sessions : Des mécanismes de gestion de la durée des sessions sont mis en place pour réduire les risques liés au vol de session. Les sessions sont expirées après un certain délai d'inactivité.
Sécurisation des formulaires et champs de saisie

Validation côté serveur : En plus de la validation côté client, une validation supplémentaire est effectuée côté serveur pour garantir qu'aucune donnée malveillante n'est traitée.
Utilisation de bibliothèques sécurisées : Les bibliothèques utilisées pour le rendu des formulaires ou des champs de saisie sont choisies en fonction de leur niveau de sécurité et de leur résistance aux attaques d'injection.
