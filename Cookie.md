## SameSite 

la propriété SameSite Sa indique au navigateur si les cookie sont restreint au requete du meme site (Same-Site)
Ou peut etre envoyer a d'autre site (Cross-Site)

### les mode de SameSite
#### Same-Site = lax (par défaut)
1. les cookie ne sont pas envoyer lors de requete Cross-site comme les image iframes ou formulaire POST 
2. des cookie pourrais etre envoyer dans une requete GET Cross-Site comme line clické d'un autre site web vers notre site 
3. permet d'eviter les attaque CSRF 


