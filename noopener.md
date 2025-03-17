# noopener

### Sécurisation des liens vers des sites externes : Attaques via window.opener
Contexte
Lorsque vous ouvrez un lien avec l'attribut target="_blank" dans un nouvel onglet, une nouvelle fenêtre ou un nouvel onglet est ouvert. Cependant, si ce lien pointe vers un site externe et que la page externe contient du JavaScript non fiable, elle peut potentiellement accéder et manipuler la page parent via l'objet window.opener. Ce mécanisme peut être exploité pour injecter du contenu malveillant, manipuler l'interface utilisateur, ou rediriger les utilisateurs vers des sites de phishing.

### Problématique
L'objet window.opener fait référence à la fenêtre d'origine qui a ouvert la nouvelle fenêtre ou le nouvel onglet. Cela permet à la page ouverte d'interagir avec et de modifier la page parente. Si cette fenêtre ouverte est malveillante, elle pourrait avoir un accès total à la page d'origine, ce qui constitue une vulnérabilité potentielle.

Exemple d'utilisation malveillante de window.opener :

```js
if (window.opener) {
    window.opener.document.body.innerHTML = "<h1>Page A modifiée par Page B!</h1>";
}
```
Ce code permet à Page B de manipuler Page A en accédant directement à son DOM et en modifiant son contenu.

### Exemple détaillé de risque
#### 1. Page A (votre site d'origine) :
```html
<!DOCTYPE html>
<html>
<head>
    <title>Page A - Site d'origine</title>
</head>
<body>
    <h1>Bienvenue sur la Page A</h1>
    <p>Cliquez sur le lien ci-dessous pour ouvrir la Page B dans un nouvel onglet.</p>

    <!-- Lien vers la Page B -->
    <a href="pageB.html" target="_blank">Visiter la Page B</a>
</body>
</html>
```
#### 2. Page B (site externe malveillant) :
```html
<!DOCTYPE html>
<html>
<head>
    <title>Page B - Site externe</title>
</head>
<body>
    <h1>Ceci est la Page B</h1>
    <script>
        // La page B accède à la page A et modifie son contenu
        if (window.opener) {
            window.opener.document.body.innerHTML = "<h1>Page A modifiée par Page B!</h1>";
        }
    </script>
</body>
</html>
```
### Mécanisme d'attaque
Page A contient un lien vers Page B avec l'attribut target="_blank", ce qui ouvre Page B dans un nouvel onglet.
Page B, par l'intermédiaire de l'objet window.opener, accède à la page parente (Page A) et modifie son contenu.
Page A voit son contenu remplacé par le texte "Page A modifiée par Page B!", ce qui peut être étendu pour exécuter des attaques plus complexes, comme des redirections, des injections de contenu malveillant (ex. publicités), ou encore l'exfiltration de données sensibles.

### Solution : Sécurisation avec rel="noopener"
1. Comportement attendu sans rel="noopener"
Lorsqu'aucun attribut rel="noopener" n'est ajouté, Page B a la possibilité de manipuler Page A via l'objet window.opener, comme illustré précédemment. Cette interaction constitue un vecteur d'attaque potentiellement grave, notamment dans des scénarios où Page B pourrait être contrôlée par un attaquant.

2. Solution sécurisée : Ajout de rel="noopener"
Pour éliminer ce risque, il est impératif d'empêcher Page B d'accéder à l'objet window.opener. Cela peut être réalisé en ajoutant l'attribut rel="noopener" au lien ouvrant Page B.

Code sécurisé de la Page A (avec rel="noopener") :

```html
<!DOCTYPE html>
<html>
<head>
    <title>Page A - Site d'origine</title>
</head>
<body>
    <h1>Bienvenue sur la Page A</h1>
    <p>Cliquez sur le lien ci-dessous pour ouvrir la Page B dans un nouvel onglet.</p>

    <!-- Lien sécurisé avec rel="noopener" -->
    <a href="pageB.html" target="_blank" rel="noopener">Visiter la Page B</a>
</body>
</html>
```
### Explication du mécanisme de rel="noopener"
L'attribut rel="noopener" empêche l'objet window.opener d'être défini, ce qui bloque toute tentative d'interaction entre Page A et Page B. Cela a pour effet de rendre Page B isolée de la page parente. Autrement dit, Page B n'a plus accès à la propriété window.opener et ne peut donc pas manipuler la page d'origine.

- Sécurité : L'attribut rel="noopener" empêche toute tentative de manipulation de la page par des fenêtres externes ouvertes dans un nouvel onglet.


- Comportement attendu : Lorsqu'un utilisateur clique sur le lien, Page B s'ouvre dans un nouvel onglet, mais elle n'a plus aucun accès à la page d'origine via window.opener.


### Avantages de l'utilisation de rel="noopener"
1. Protection contre les attaques : Empêche l'exploitation de window.opener pour manipuler la page parent.


2. Prévention des redirections malveillantes : Préserve l'intégrité de votre site en empêchant les redirections ou les manipulations malveillantes.


3. Contrôle renforcé sur l'interface utilisateur : Empêche toute modification indésirable de l'interface de votre site par des pages externes.
### Conclusion
L'ajout de rel="noopener" est une mesure de sécurité indispensable pour protéger vos utilisateurs contre les attaques liées à window.opener. En utilisant cette approche, vous vous assurez qu'aucune page externe ne puisse interagir de manière malveillante avec votre site lorsqu'elle est ouverte dans un nouvel onglet ou une nouvelle fenêtre.

