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

