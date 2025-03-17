# XMLHttpRequest ou XHR

API Javascript 

cet methode permet de recevoir et d'envoyer des requete sans recharger la page 

### InnerHTML

**innerHTML** n'est pas très fiable en matière de sécurité. Dans le cadre de l'utilisation avec XHR, il peut ouvrir une faille de sécurité, permettant à des personnes malveillantes d'injecter du code dans votre site web. 

### textContent 
1. textContent n'exécute pas le code JavaScript et traite tout le contenu comme du texte brut. Cela signifie que le JavaScript et le HTML malveillant ne peuvent pas être exécutés, évitant ainsi les attaques XSS (Cross-Site Scripting).

2. textContent est plus rapide que **innerHTML** lorsque vous manipulez du texte, car il ne nécessite pas d'analyser ou de construire des éléments HTML dans le DOM. Cela réduit les coûts de traitement supplémentaires associés à la manipulation des balises HTML.