# Présentation cours Css

## Définition:

Les feuilles de style est un langage informatique qui sert à décrire la présentation des documents HTML et XML. Il définit dans un fichier spécial,le style de certaines balises.Grâce aux feuilles de style, il suffit de modifier la définition des feuilles de style en un seul endroit pour changer l'apparence du site tout entier.
A l'aide de la balise <link> on peut créer un lien vers une feuille de style à dans un fichier HTML.

```html
Exemple: <link href="style.css" rel="stylesheet" type="text/css" />
```

La définition d'un style se fait à l'aide de règles en texte simple permettant de décrire l'aspect des éléments de la page. Une règle CSS est caractérisée par deux principaux éléments : un sélecteur de balises, des attributs et les valeurs correspondantes.

# La syntaxe de base:

La syntaxe est composée de 3 éléments :

- Le sélecteur est l’élément sur lequel on applique les
  propriétés (balise HTML, id, classe, etc.)

- La propriété est l’effet que l’on va vouloir donner (ex
  couleur de texte,positionnement, couleur de fond, etc.)

- La valeur de la propriété CSS (rouge, 10px, etc.)

Exemple:

```css
selecteur {
  propriete: valeur ...;
}
```

- Les commentaires CSS
  Pour créer un commentaire CSS, on utilise /\* commentaire \*/
  Le commentaire n’est pas visible dans le navigateur.

## Exemples des attributs possédant des valeurs différentes:

- Modification du fond d'écran:

Exemple:

```css
body {
  background-image: url(fleurrose.gif);
}
```

- Modification du style du texte:

Exemple:

```css
h3 {
  font-family: verdana, sans-serif;
  color: #e24ba0;
  text-decoration: underline;
}
```

## Le sélecteur usuel d'élément HTML:

On peut sélectionner n’importe quel élément HTML et lui appliquer un style.! Une propriété appliquée sur un élément HTML, s’applique par défaut à tous les éléments présents dans le document HTML.

Exemple:

```css
p {
 color : blue;
}
#=> Tous les paragraphes auront une couleur de texte bleu
```

## Notion d’enfant et de descendance:

- h1, p, h2, p sont enfants de div.

- a, strong et em sont enfant du p dans lequel ils sont
  contenus (mais pas de l’autre p)

- a, strong et em (et h1, p, h2 et p) sont descendants de div

## Sélecteur de hiérarchie:

Pour sélectionner le a descendant de p, nous allons pouvoir écrire :

```css
p a { … }
```

(notez l’espace entre le p et le a)

## Sélecteur de groupe:

Pour sélectionner plusieurs éléments et leur appliquer la même valeur, on les sépare par une virgule.

```css
h1,
h2 {
  color: red;
}
=> Va donner la couleur rouge à tous les h1 ou h2
```

## Les sélecteurs de classe:

class=" " est un attribut qui peut se mettre sur n’importe quelle balise

Il permet de cibler de manière plus « spécifique » certains éléments

```html
<p class="important">Un paragraphe spécifique qui est mis en avant</p>
```

## Cibler une classe indépendamment de la balise:

Si on veut cibler une classe, sans se préoccuper de la
balise on utilise le « point ».

```css
.nomdeclasse {
}
```

## L’id(identifiant):

Il a le même rôle qu’une classe, mais doit être unique sur la page(donc on va moins l’utiliser)

- Un seul attribut id par balise est possible
- On le note <element id="monid">
- On le cible en CSS avec #monid { }

## Bordures et arrières plans:

- La propriété border permet d'ajouter une bordure à un élément
- Elle a 3 « sous propriétés » possibles : style, color et
  width.
- On regroupe souvent comme ceci :border: width style color;

Exemple:

```css
h2 {
  border: 2px solid #009860;
}
```

## La notion Background-color:

- background-color : valeur permet de donner une couleur de
  fond.
- Valeurs : n’importe quelle couleur CSS
- Sur un élément bloc (prend toute la largeur) ou inline (prend la largeur du contenu)

## Dimensions, margin et padding:

1. Margin:

- La propriété margin détermine l’espace entre le bord de
  l’élément,et l’élément suivant.
- Par défaut margin: valeur applique la même valeur aux 4 cotés
- Valeur possible : auto, valeur en unité de mesure, positive
  ou négative.

  On peut la décomposer individuellement en

- margin-top : marge extérieure haute
- margin-right : marge extérieure droite
- margin-bottom : marge extérieure basse
- margin-left : marge extérieure gauche
- Ou rassembler les 4 valeurs : margin: 10px 5px 8px 15px; (dans
  l’ordre : haut, droite, bas, gauche)

2. Padding

La propriété padding détermine un espacement entre le bord de
la boite et son contenu

- Par défaut padding : valeur applique la même valeur aux côtés
- Valeur possible : valeur en unité de mesure.

On peut la décomposer individuellement en

- padding-top : marge intérieure haute
- padding-right : marge intérieure droite
- padding-bottom : marge intérieure basse
- padding-left : marge intérieure gauche

- Ou rassembler les 4 valeurs : padding: 10px 5px 8px 15px;
  (dans l’ordre : haut, droite, bas, gauche)
