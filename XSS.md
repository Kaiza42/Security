
# Les attaques XSS (Cross-site scripting)

Les XSS sont des attaques dans lesquelles un attaquant parvient à insérer un script JavaScript malveillant dans une page web. Ce script est ensuite exécuté dans le navigateur de la victime, ce qui peut permettre à l'attaquant de voler des informations sensibles (comme les cookies ou les identifiants), d'effectuer des actions en son nom, ou de modifier l'apparence d'une page.

Il existe plusieurs types d'attaques XSS, telles que les Stored XSS et les Reflected XSS que nous détaillerons dans la section suivante.

 **Stored XSS** : Dans ce type d'attaque, le code malveillant est stocké sur le serveur (dans une base de données, par exemple). Il est ensuite renvoyé dans les pages web que l'utilisateur consulte. Cette attaque peut avoir des conséquences graves, notamment l'injection de scripts sur toutes les pages où l'attaque a été enregistrée.

**Reflected XSS**  : Contrairement à l’attaque Stored XSS, le Reflected XSS n'implique pas de stockage sur le serveur. L'attaquant insère du code malveillant dans l'URL ou dans un champ de saisie. Ce code est immédiatement renvoyé par le serveur dans la réponse HTTP sans être validé, et est exécuté dans le navigateur de l'utilisateur. Cette attaque peut survenir lorsque des données non vérifiées sont affichées sur une page, comme dans un formulaire de recherche ou des paramètres d'URL.

<!-- Ils en existe d'autre toute les documenter serait une perte de temp mais en prendre connaissance est une bonne choses. -->
[lien Wikipédia sur les attaque XSS](https://en.wikipedia.org/wiki/Cross-site_scripting)

[lien MDN sur les attaque XSS](https://developer.mozilla.org/en-US/docs/Web/Security/Attacks/XSS)

