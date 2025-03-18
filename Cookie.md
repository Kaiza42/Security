# Cookie

## Domain 
determine le domaine sur le quel le cookie seras envoyer par defaut il s'applique uniquement au domaine a partir duquel le cookie a été émis, peut etre étendu aux sous domaines si spécifié 

## path 
Spécifie les chemins URL pour les quel le cookie seras envoyé Par dafaut il est associé à ``/```, ce qui signifie que le cookie sera envoyé avec toutes les requete de ce domaine.

## Max-Age / Expires 

Max-Age definit la durée de validité du cookie en seconde a partir de sa création si ce champ est absent, le cookie est un **cookie de session**, ce qui signifie qu'il disparait lorsque l'utilisateur ferme son navigateur 

## HttpOnly 
lorsque que cet attribue est spécifié, le cookie ne seras pas accecible par JavaScript via document.cookie 

## Secure Si l'attribue Secure est défini, le cookie seras transmis uniquelent via HTTPS cela empêche les cookies d'etre envoyer sur des connexion http non sécurisées limitant les risque man-in-the-midle

## SameSite 

la propriété SameSite Sa indique au navigateur si les cookie sont restreint au requete du meme site (Same-Site)
Ou peut etre envoyer a d'autre site (Cross-Site)

### les mode de SameSite

#### Same-Site = lax (par défaut)
1. les cookie ne sont pas envoyer lors de requete Cross-site comme les image iframes ou formulaire POST 
2. des cookie pourrais etre envoyer dans une requete GET Cross-Site comme line clické d'un autre site web vers notre site 
3. permet d'eviter les attaque CSRF

#### Same-Site = strict 
1. En mode Strict, le cookie n’est envoyé que pour les requêtes provenant du même site (Same-Site). Cela signifie que même lorsqu'un utilisateur suit un lien depuis un autre site, le cookie ne sera pas envoyé.

2. Ce mode offre le niveau de sécurité le plus élevé, car il empêche totalement toute interaction entre les cookies et des requêtes provenant d’autres sites.

3. Cas d’usage : Idéal pour les cookies sensibles, comme ceux de session utilisateur ou d'authentification, où vous ne voulez absolument pas que les cookies soient exposés à des requêtes provenant d’autres sites.

#### Same-Site = None 

1. En mode None, le cookie peut être envoyé lors de requêtes cross-site. Cela signifie que le cookie sera envoyé dans tous les contextes, y compris les requêtes provenant d'autres sites.

2. Important : Si vous définissez SameSite=None, il est obligatoire que le cookie soit marqué comme Secure (ce qui signifie qu'il ne sera envoyé que via des connexions HTTPS).

3. Cas d’usage : Ce mode est nécessaire lorsque vous devez partager des cookies entre différents sites, comme dans le cas d’un site principal et d’un sous-domaine tiers, ou dans des applications de tiers intégrées (widgets, services de paiement, etc.).


[Utiliser les cookies HTTP par MDN](https://developer.mozilla.org/fr/docs/Web/HTTP/Guides/Cookies)


