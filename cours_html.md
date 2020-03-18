# Présentation du langage HTML

## Définition:

- HTML

      HTML (HyperText Markup Language) est un langage de balisage qui permet de structurer le contenu des pages web dans différents éléments (Balise(Marquage / Tags).

- Langage HTML:

      Le langage HTML a beaucoup évolué depuis sa création par Tim Berners‐Lee en 1992. Aujourd'hui on en est à la version 5 (notée HTML 5).

- Page Web HTML:

      La page Web HTML est constitué de : titres, paragraphes, images, tableaux,formulaires, liens hypertext...)
      Après être passé par une version appelé XHTML (qui est réellement une reformulation de HTML en tant qu’application XML).

- L’organisme W3C:

      Un acteur actuellement responsables des évolutions,des recommandations et des spécifications du langage HTML: L’organisme W3C (World Wide Web Consortium : http:// www.w3.org/

## Utilisation du langage Html:

- Pour apprendre le langage HTML, on a besoin :

        1. D'un éditeur de texte tout simple comme par exemple:
        Bloc‐notes de Windows ou Visual Studio Code ou autres

        2. D'un navigateur web comme :
        Microsoft Internet Explorer, Google Chrome ou autres.

- Pour développer des sites web professionnels, on utilise souvent des logiciels de développement spécialisés appelés aussi éditeurs WYSIWYG :What You See Is What You Get (Ce que vous voyez, vous l'obtenez).

## Syntaxe du langage HTML:

- Editeurs de Coding:
  La Programmation des pages web ou le Coding nécessite un éditeur de texte:
  -Visual Studio Code,....

- Notion de balise (élément)

  - document HTML:

    La description d'un document HTML passe par l'utilisation de balises. Une balise est délimitée par les signe "<" et ">".

    ```html
     Exemple:
      <Center> Chaque balise doit être fermé < … > ……. </…> (Exception balises Auto fermeture)
    ```

  - Les attributs:

    Les attributs modifient les propriétés des balises HTML.


      ```html
      Exemple :
      <font size="7" face="‘’Arial’’" color="‘’red‘‘" Align="‘’right’’"></font>
      ```

- Les commentaires:


      Les commentaires débute par <!‐‐ et finit par ‐‐> .

      ```html
      Exemple:
      <!‐‐ Ceci est un commentaire ‐‐>
      ```

- Structure générale d’un document HTML:

  Un document HTML 4.0 comporte 2 parties, encadrées par des balises `<HTML> et </HTML>` :

  - Un en-tête de déclaration (délimité par des balises `<HEAD>`)

  - Le corps du document, dans lequel on placera le contenu de celui-ci (délimité par des balises <BODY>

  - D'autre part, la version HTML utilisée doit être précisée dans la première ligne, en utilisant une balise `<!DOCTYPE ...>`

  ````html
  Exemple:
  <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.0//EN" "http://www.w3.org/TR/REC-html40/strict.dtd">
  <html>
    <head>
      <title>Bienvenue dans l'estuaire de Seine</title>
    </head>
    <body>
      <h1>L'estuaire de Seine</h1>
      <p>
        Lieu magique, rencontre du fleuve et de la mer,un environnement unique,
        l'estuaire de Seine est aussi un lieu de communication important...
      </p>
    </body>
  </html>
  ```
  ````

* Exemple des balises:

  - Formater un texte en GRAS :
    <b> définit un texte gras (b de bold en anglais) puis se termine par </b>
    La balise : <b>Texte en Gras</b>

    Résultat : Texte en Gras

  - Gérer la tailledu texte :
    <font size="+3"> définit la taille du texte puis se termine par </font>
    (valeurs de -3 à +3)
    La balise :<font size="+3">Texte en grand<font>

    Résultat : Texte en grand

  - Formater un texte en italique :
    <i> définit un texte en Italique puis se termine par </i>
    La balise :<i>Texte en Italique</i>

    Résultat : Texte en Italique

  - Formater un texte souligné :
    <u> définit un texte souligné puis se termine par </u>
    La balise : <u>Texte Souligné</u>

    Résultat : Texte Souligné

  - Formater un indice :
    <sub> définit un texte en indice puis se termine par</sub>
    La balise : Texte <sub>en indice </sub>

    Résultat : Texte en indice

  - Le retour à la ligne :
    <br />définit un retour à la ligne (pas besoin d'untag de fermeture)
    Exemple : Texte de la première ligne<br />Texte de la seconde ligne

    Résultat : Texte de la première ligne
    Texte de la seconde ligne

* Les listes:

  ```html
  Les listes HTML sont prévues pour dresser des énumérations. Les structures
  sont :
  <ol>
    Les liste ordonnée (liste numérotée) et
    <ul>
      les listes non ordonnée (liste à puces) au sein desquels chaque élément
      individuel est un
      <li>
        . Lorsqu’il s’agit de rédiger une liste de définitions, l’élément
        <dl>
          peut être utilisé en conjonction avec
          <dt>et</dt>
          <dd>.</dd>
        </dl>
      </li>
    </ul>
  </ol>
  ```

  Exemple:

  ```html
  <dl>
    <dt>HTML</dt>
    <dd>Langage de structuration des contenus des pages web</dd>
    <dt>SQL</dt>
    <dd>Langage d’interrogation des bases de données</dd>
  </dl>
  ```

* Liste ordonnée

  L'élément HTML <ol> représente une liste ordonnée. Les éléments d'une telle liste sont généralement affichés avec un indicateur ordinal pouvant prendre la forme de nombres, de lettres, de chiffres romains ou de points

  Exemple:

  ```html
  <ol type="?" ,start="?" ,reversed="?">
    <li>Mix flour, baking powder, sugar, and salt.</li>
    <li>In another bowl, mix eggs, milk, and oil.</li>
    <li>Stir both mixtures together.</li>
    <li>Fill muffin tray 3/4 full.</li>
    <li>Bake for 20 minutes.</li>
  </ol>
  <!--type: l’attribut type en indique le type : ‘’1’’, ‘’a’’, ‘’A’’
        start: L’attribut start définit l’index du début de la numérotation
        reversed: L’attribut reversed inverse l’ordre de la numérotation
        <li>:Désigne un élément contenu dans une liste.
    -->
  ```

  Résultat:

      1.Mix flour, baking powder, sugar, and salt.
      2.In another bowl, mix eggs, milk, and oil.
      3.Stir both mixtures together.
      4.Fill muffin tray 3/4 full.
      5.Bake for 20 minutes.

* Liste non ordonnée:

  ```html
  <ul type="?">
    <!--l’attribut type en indique le type :Disc ,Square,Square.
      <li>:Désigne un élément contenu dans une liste.
  --></ul>
  ```

* Les Tableaux en HTML:

      En HTML, un tableau se construit ligne par ligne. Dans chaque ligne (<tr>), on indique le contenu des différentes cellules (<td>).

  Exemple:

  ```html
  <table border>
    <tr>
      <td>Mohamed</td>
      <td>33 ans</td>
      <td>Espagne</td>
    </tr>
    <tr>
      <td>Rachid</td>
      <td>26 ans</td>
      <td>États-Unis</td>
    </tr>
  </table>
  ```

  résultat:

  <table border>
  <tr>
  <td>Mohamed</td>
  <td>33 ans</td>
  <td>Espagne</td>
  </tr>
  <tr>
  <td>Rachid</td>
  <td>26 ans</td>
  <td>États-Unis</td>
  </tr>

     </table>

* Les Liens hypertext en HTML:

  Un hyperlien, ou lien hypertexte, ou lien web, ou simplement lien, est une référence dans un système hypertexte permettant de passer automatiquement d'un document consulté à un document lié. Les hyperliens sont notamment utilisés dans le World Wide Web pour permettre le passage d'une page Web à une autre à l'aide d'un clic.

  ```html
  1 – Lien vers une page Web:
    <A href=".../Accueil.html" target="_blank" > Accueil </A>
  2 - Liste vers une adresse mail:
    <A href="mailto:contact@Gmail.com">Contactez moi par email </A>
  3 - Lien vers un site web:
    <A href=http://www.google.fr target="_blank" >Navigateur Google </A>
  4 - Lien interne dans le même document:
    <A id="paragra1">Paragraphe 1</a>Structure Document HTML <a href="#para1">Aller à la structure </a>
  ```

* Les Formulaires:

  ```html
  - <input type="text" name="ident" />
  ```

  ```html
  -
  <select name="menu">
    <option> Orange < option selected> Citron < option> Pêche </option></select
  >
  ```

  ```html
  - <input type="checkbox" name="Act" value="Sport" checked /> Sport
  ```

  ```html
  - <input type="radio" name="SF" value="Cel" />Célibataire
  ```

  ```html
  - <input type="submit" value="Envoi" /> 6.
  <input type="reset" value="Efface" />
  ```

  - <input type=text name="ident">
  - <select name="menu">
         < option> Orange
         < option selected> Citron
         < option> Pêche
     </select>
  - <input type="checkbox" name="Act" value="Sport"
     checked> Sport
  - <input type="radio" name="SF" value="Cel">Célibataire
  - <input type="submit" value="Envoi">
  - <input type="reset" value="Efface">

* Les Menus

      L'élément FRAME permet de définir le contenu de chacune des zones. Pour cela, on utilise deux attributs :

      - src=url pour indiquer le fichier à placer dans la zone

      - name=nomDeZonepermet de nommer la zone afin qu'elle puisse devenir la cible d'un lien (on utilisera alors l'attribut target de la balise <A> pour y accéder.

  Exemple:

  ````html
   <HTML>
   <Head> <Title> filiales et formulaire </Title></Head>
   <FRAMESET ROWS=“20%, 80%">
   <FRAME SRC=“entete.html" Name=“haut”>
   <FRAME SRC="formulaire.html" Name=“Bas”>
   </FRAMESET>
   </HTML>
   ```
  ````

* Les contenu embarqué:

  - les images
    ```ruby
    <img src=‘’NomImage.Ext’’ height=% width=% >
    ```
  - Audio
    ```ruby
    <audio src="musique.mp3" controls></audio>
    ```
    -git Video
    ```ruby
    <video src=" video.mp4" width="200" height="200" controls></video>
    ```
