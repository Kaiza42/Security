CSP = Content Security Policy

mission principal : 

 1 : prevenir les attaque XSS : bloque les chargement de script malveillants ou non autorisé Et empeche les injection de code JavaScript

 2 : limite les ressource non autorisées : Permet de spécifié quelles ressource sont autorisées pour autorisées pour changer des ressource ex : img, scripts, style, empeche les ressource externe 

 3 : reduire les attaque de type injection : peut limiter d'autre vertions d'injection comme styless css ou les iframes non sécurisées

 limite : 
          1 : complexe a configuré : mal configurée sa peut bloquer les script et casser des feature 
          2 : compatibilité avec du contenue dynamique :      Certains sites utilisent du contenu dynamique généré à la volée, ce qui rend plus difficile la définition d'une politique CSP stricte.
          3 : Usage du unsafe-inline : Pour des raisons de compatibilité avec des scripts inline (par exemple du code JavaScript ou CSS écrit directement dans une page HTML), certains développeurs utilisent l'option unsafe-inline dans CSP, ce qui affaiblit la protection globale contre les attaques XSS.