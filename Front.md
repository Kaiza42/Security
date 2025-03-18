# Sécurisation du Front-End

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

Validation et assainissement des entrées : Toutes les données provenant des utilisateurs sont systématiquement validées et nettoyées avant d’être traitées ou affichées sur la page. Cela inclut les champs de formulaire, les URL et les autres points d'entrée de données utilisateur.
Échappement des données : Lors de l’affichage de données sur le front-end, des méthodes d’échappement sont utilisées pour transformer les caractères spéciaux en entités HTML sûres. Cela empêche le code malveillant d’être interprété comme du script.
Utilisation de Content Security Policy (CSP) : L'implémentation d'une politique CSP limite les sources de contenu autorisées (scripts, images, etc.), empêchant l'exécution de scripts malveillants provenant de sources non fiables.
Protection contre le Reflected XSS (XSS temporaire)

Validation et filtrage des paramètres d'URL : Tous les paramètres d'URL, ainsi que les données envoyées dans les formulaires, sont validés pour s'assurer qu'ils ne contiennent pas de scripts malveillants.
Filtrage et évasion des données : Les données reçues par le serveur doivent être correctement échappées avant d'être renvoyées dans la réponse HTTP afin d'éviter qu’elles soient interprétées comme des scripts.
Protection contre les attaques CSRF (Cross-Site Request Forgery)

Tokens CSRF : À chaque action sensible sur le site (comme la modification du profil ou l'envoi de données), un token unique est envoyé dans la requête HTTP pour s'assurer que la demande provient bien de l'utilisateur légitime et non d'un site malveillant.
Vérification des méthodes HTTP : Les actions sensibles sont limitées aux méthodes HTTP appropriées (par exemple, POST plutôt que GET), afin d'éviter l'exploitation des requêtes GET pour des actions non sécurisées.
Sécurisation des sessions et cookies

Cookies sécurisés (Secure Cookies) : Les cookies utilisés pour stocker les informations de session sont marqués comme Secure et ne sont envoyés que via des connexions HTTPS.
Cookies HttpOnly : Les cookies de session sont également marqués comme HttpOnly, ce qui empêche l'accès aux cookies via JavaScript et les protège contre les attaques XSS.
Expiration des sessions : Des mécanismes de gestion de la durée des sessions sont mis en place pour expirer les sessions inactives après un certain délai, réduisant ainsi les risques de vol de session.
Sécurisation des formulaires et champs de saisie

Validation côté serveur et côté client : Toutes les données soumises via des formulaires sont validées à la fois côté client (pour l'expérience utilisateur) et côté serveur (pour la sécurité).
Filtrage des caractères spéciaux : Toute donnée saisie dans un formulaire est filtrée pour éliminer les caractères spéciaux qui pourraient être interprétés comme du code malveillant.
