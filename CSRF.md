CSRF = cross-site request Forgery ou falsification de requete intersite 
Permet d'usurper l'identiter d'un utilisateur grace au cookies 
1. L'utilisateur est authentifié sur un site web (par exemple, sur un site bancaire). Cela signifie que le site a enregistré un cookie d'authentification dans le navigateur de l'utilisateur.

2.Le pirate incite l'utilisateur à visiter un autre site malveillant. Ce site malveillant contient du code qui envoie une requête HTTP au site web authentifié (par exemple, une requête pour transférer de l'argent à un autre compte).

3.Le site authentifié reçoit la requête et l'accepte : puisque l'utilisateur est déjà authentifié (grâce aux cookies envoyés automatiquement avec la requête), le site croit que l'utilisateur légitime souhaite réellement effectuer cette action. Le site n'a aucune idée que l'utilisateur a été piégé pour envoyer cette requête.