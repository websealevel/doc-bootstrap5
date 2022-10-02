# Doc Bootstrap 5

Installer et utiliser Bootstrap 5 en version Sass pour en tirer le meilleur profit, et le customiser à notre guise.

- [Doc Bootstrap 5](#doc-bootstrap-5)
  - [Installation](#installation)
  - [Utilisation](#utilisation)
    - [Boilerplate](#boilerplate)
    - [Utiliser Bootstrap dans notre projet](#utiliser-bootstrap-dans-notre-projet)
      - [Feuilles de style](#feuilles-de-style)
      - [Javascript](#javascript)
  - [Maintenance](#maintenance)
  - [Ressources utiles](#ressources-utiles)

>Si vous cloner ce dépot, [pensez à installer Bootstrap 5](#installation).

## Installation

- télécharger [les Sources Bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/download/#source-files)
- installer un compilateur [Sass](https://fr.wikipedia.org/wiki/Sass_(langage)), comme [Dart Sass](https://sass-lang.com/dart-sass)
- extraire le contenu de l'archive des sources de Bootstrap 5
- supprimer l'archive

## Utilisation

Nous allons utiliser les fichiers [sass](https://fr.wikipedia.org/wiki/Sass_(langage)) de Bootstrap. On ne veut pas des sources précompilées (ni en local ni en CDN): on veut pouvoir recompiler les sources afin d'utiliser le framework et toutes ses capacités de personnalisation.

### Boilerplate

- créer vos fichiers `index.html`, `style.scss` et `script.js`
- link votre feuille de style `style.css` (qui n'existe pas encore!) à votre fichier HTML
- link votre fichier source javascript `script.js` à votre fichier HTML dans une balise script

Votre projet devrait ressember à ça

~~~bash
bootstrap-5.0.2/
index.html
style.scss
script.js
~~~

>A l'écriture de cette doc, la version de Bootstrap est la 5.0.2, ce qui peut être amené à changer si vous lisez cette doc plus tard.

On laisse le projet comme ça, quand Bootstrap sortira une nouvelle version, vous n'aurez qu'à la télécharger, à l'extraire et à redéfinir le PATH vers les sources. Et c'est tout ! Ainsi, le projet est facile à maintenir. 

### Utiliser Bootstrap dans notre projet

#### Feuilles de style

Le point d'entrée de l'import de Bootstrap est le fichier `style.scss`. *Vous ne devez et n'avez pas à modifier directement les sources de Bootstrap*.

Nous allons utiliser les sources Sass de Bootstrap, non compilées. Et nous allons utiliser seulement celles qui sont nécessaires au bon fonctionnement de Bootstrap et celles qui nous intéressent (que nous allons utiliser). Cela nous permettra d'avoir un contrôle fin des sources (et donc de la taille des assets envoyés au navigateur) et de personnaliser Bootstrap *comme nous l'entendons*.

Voici à quoi devrait ressembler notre fichier source `style.scss`

>Attention, l'ordre des import doit être respecté !
~~~scss
~~~

Compilez votre fichier style.scss en fichier css interprétable par votre navigateur

~~~bash
sass style.scss style.css
~~~

#### Javascript

## Maintenance

Vous n'avez pas besoin de versionner les sources de Bootstrap, seulement votre fichier `style.scss`. Vous pouvez télécharger Bootstrap à votre guise sur n'importe quelle machine afin de le brancher à votre projet.

Comme nous ne touchons pas directement aux sources, nous pouvons maintenir facilement notre projet et mettre à jour Bootstrap en cas de besoin.

## Ressources utiles

- [Documentation officielle de Bootstrap 5](https://getbootstrap.com/docs/5.0/getting-started/introduction/)
- [Dart Sass](https://sass-lang.com/dart-sass)
- [The Missing Bootstrap 5 Guide, de Jeppe Schaumburg Jensen, éditions Packt Publishing](https://www.packtpub.com/product/the-missing-bootstrap-5-guide/9781801076432), un très bon livre qui vous explique comment tirer le maximum de Bootstrap et comment le personnaliser. Pour cela, on a un bref aperçu du fonctionnement du core de Bootstrap et comment utiliser l'[utility API](https://getbootstrap.com/docs/5.0/utilities/api/) pour ajouter nos propres systèmes de design.