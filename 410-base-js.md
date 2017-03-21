---
layout: page
title: Bases JavaScript
permalink: /js/bases/
---

Quelques bases JavaScript...

Navigateurs et JavaScript
==

Chaque navigateur intègre un interpréteur de JS, plus ou moins performant: 

Permet un niveau d'interactivité plus riche qu'avec de l'HTML simple:


Placer du JavaScript dans un document HTML
==

Comme pour les feuilles de style CSS, vous avez plusieurs options:

**1) Dans un fichier séparé:** 

Vous pouvez enregistrer votre code JavaScript dans un fichier dont le nom se terminera par `.js`. 

Vous devrez les charger ainsi:

```html
<script src="script.js"></script>
```

C'est la méthode recommandée : déplacer le code JavaScript dans un fichier externe et utiliser le moins possible du code inline dans un fichier HTML pour favoriser la maintenabilité et séparer clairement les responsabilités.

On placera ce code soit dans la partie ```<head>``` du document (si on souhaite que le JavaScript s'exécute *avant* le chargement du contenu), ou tout en bas, juste avant la balise fermante ```</body>``` (si on souhaite que le contenu soit chargé en premier, ce qui est souvent le cas).

Il est possible d'influer sur le chargement du JavaScript avec deux attributs, **"async"** et **"defer"**.

```html
<script async src="script.js">
```

Normalement, lorsque le navigateur charge un fichier JavaScript, le rendu visuel de la page est bloqué pendant ce laps de temps. En effet, le chargement d’une ressource JavaScript est bloquante. Avec l'attribut **"async"**, on indique au navigateur que le rendu de la page peut se poursuivre **en parallèle** (de manière **asynchrone**).

```html
<script defer src="script.js">
```

L'attribut **"defer"** indique au navigateur que le rendu de la page peut se poursuivre pendant le chargement du fichier JavaScript, et que l'exécution de celui-ci doit attendre que le rendu intégral de la page soit fini. Cela garantit que le JavaScript ne ralentit pas le chargement. Voir [cet article](https://bitsofco.de/async-vs-defer/) d'Ire Aderinokun pour plus de détails.

**2) Dans le code de la page HTML (inline):**

```html
<script>
```



**3) Directement dans un élément HTML:**

```html
<a href="#" onclick="alert('Vous avez cliqué !'); return false;">Cliquez-moi !</a>
```

**4) Dans la console développeur:**

La console est un outil intégré à votre navigateur. Voici comment l'afficher:

* Dans Chrome: Alt+Cmd+J
* Dans Safari: Alt+Cmd+C

À propos, il semble que Facebook n'apprécie pas que ses utilisateurs ouvrent la console développeur:

![Message d’avertissement de Facebook apparaissant dans la console](/cours-javascript/img/fb-console.jpg)

L'artiste James Bridle a [écrit un article](http://booktwo.org/notebook/welcome-js/) et développé un script  - [welcome.js](https://github.com/stml/welcomejs/) - en résponse à cette pratique.

3 instructions pour démarrer
===

Afficher une boîte avec un message:

```javascript
```

Écrire du texte dans la console (pour débugguer):

```javascript
```

Écrire quelque chose dans le document, dans une balise HTML qui a un certain id:

```javascript
document.getElementById("item").innerHTML = "<p>Mon contenu</p>";
```



Syntaxe JavaScript
==

Chaque instruction est séparée par un ;

Commentaires


```javascript
// Ceci est un commentaire 
```

Par bloc : 

```javascript
/* Ceci est un
```

Conventions

* Noms de variables et fonctions écrits en CamelCase
* Noms de constantes écrits en majuscule

Déclaration et typage
===

* Variables avec le mot clé var 
* Constantes avec le mot clé const
* Une variable peut être déclarée après avoir été utilisée (hoisting)

Types primitifs
===

```javascript

// Entier
var annee = 2014;

// Réel

// Chaîne de caractère
var message="Gangnam style";
var message='Gangnam style';

// Booléen
var estSympa=true;
```

Notion de fonction
===

```javascript
// déclaration de la fonction
```

Une fonction, c'est un ensemble d’instructions prêt à être utilisé après sa déclaration.

* Permet la ré-utilisabilité du code

Structures de contrôle
===

Condition

```javascript
if (expr) { ... } else { ... }
```

Boucle

```javascript
```

Sélection

```javascript
switch(expr) { case n:...}
```

Itération

```javascript
```

Enchaînement

```javascript
```

Opérateurs arithmétiques
===

Opérateurs binaires

Opérateurs unaires

Opérateurs logiques
