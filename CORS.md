# CORS => cross-origin ressource Sharing 

CORS sert de validation de lien donc de 2e origin ?

Oui, CORS sert à valider si une deuxième origine (un autre site ou domaine) a le droit d'accéder à une ressource (données, API, etc.) sur un serveur. Par exemple, si un site A (exemple.com) veut accéder à une ressource sur un site B (api.exemple2.com), CORS valide si le serveur du site B autorise cette requête venant du site A.

CORS contourne Same Origin Policy SOP ? 
Oui, CORS permet de contourner la Same-Origin Policy (SOP) de manière sécurisée. Par défaut, SOP bloque toute requête entre des sites de différentes origines (différents domaines). Grâce à CORS, le serveur de l'origine cible (le second site) peut dire : "J'autorise cette autre origine à faire des requêtes chez moi". CORS ne désactive pas SOP, mais il permet des exceptions sécurisées.

Sans CORS pas de requete a d'autre site car bloquer par defaut ?
Oui. Sans CORS, le navigateur bloque par défaut toutes les requêtes provenant d'un site vers un autre domaine, pour des raisons de sécurité. Les sites web ne peuvent interagir qu’avec des ressources du même domaine, à moins que le serveur distant n’autorise explicitement l'accès via CORS.

le CSRF token c'est quoi ? 

un token unique entre serveur et utilisateur  ce token est envoyer a l'utilisateur 

Attaque basé sur les vulnérabilité dans la gestion du CSRF Token 

1. absence de verification du token CSRF si 