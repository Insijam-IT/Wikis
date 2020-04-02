# Présentation du langage JavaScript

## Définition:

1. Pour aborder JavaScript, il faut déjà connaître:
  - Le langage HTML
  - Les feuilles de styles (CSS

2. JavaScript est un langage interprété par le navigateur.

3. Le JavaScript est un langage « client »
Il est exécuté chez l'utilisateur lorsque la page Web est chargée.

4. JavaScript est un langage « objet »
chaque objet possède des méthodes (ou fonctions ) et des propriétés

5. Il a pour but de dynamiser les sites Internet.

6. Liste non exhaustive des navigateurs:

   - Linux/UNIX: Firefox,Netscape,Mozilla,Konqueror
   - Windows: Internet Explorer,Firefox,Netscape,Opéra,Chrome.
   - Mac OS: Internet Explorer,Konqueror,Opéra,Safari

## Utilisation du langage JavaScript:

1. Les conditions:
    ```javascript
       if(var == var2)
         {
            ...............
         }
       Else
         {
            ...............
         }
    ```
    Syntaxe des conditions:
    ```
    • égalité : ==
    • différent de: !=
    • inférieur ou égal à : =<
    • supérieur ou égal à : =>
    • inférieur à : <
    • supérieur à : >
    • et logique : &&
    • ou logique : ||
    • identique à : ===
    • non identique à : !==
    ```
2. Les boucles:

      - La boucle for
      ```javascript
         for(i=0,i<5,i++)
           {
              ...............
           }
      ```
      - La boucle while
      ```javascript
        while(a<b)
          {
            ...............
          }
      ```
      - La boucle do while
      ```javascript
        do{
        ...............
        }
        while(a<b)
      ```
3. Structure de programme script interne:

      ```html
      <html >
      <head >
        <title Titre title >
        <script type="text/ javascript ">
        <!----////---->
        </script>
      </head>
      <body >
        <………Contenu de la page programme…………..>
      </body >
      </html>
      ```

4. Structure de programme script externe:
      ```html
      <html>
      <head>
          <title></title>
          <script type ==" javascript src =="MonFichier. </script>
      </head>
        <body>
          ……………………………
          ……………………………
        </body>
      </html>
      ```
5. Les fonction:

      ```javascript
      function maFonction()
         {
            ...............
            ...............
            ...............
         }
      ```
      Exemple 1:
      ```javascript
      function maFonctionIf
         {
          if(test1)
          {
            .................
            .................
          }
          Else
          {
            .................
            .................
          }
         for(i=0,i<n,i++)
          {
            .................
            .................
          }
         }
      ```
      Exemple 2:
      ```javascript
      function maFonctionSwitch
         {
          var nb = prompt("…............");
         switch(nb)
           {
            case 0: alert ("...........");
              break;
            case 1: alert («...........");
              break;
            case 2:
            case 3: alert («...........");
              break;
            Default: alert («...........");
              break;
         }
      ```

3. Les tableaux:
     ```javascript
     //On crée le tableau, contenant les lignes
         var grille = new Array()
     //On crée les lignes les unes après les autres
          for(var i=0; i<9; i++)
          grille[i] = new Array()
     // on parcourt les lignes...
          for(var i=0; i<9; i++)
     //Dans chaque ligne, on parcourt les cellules
          for(var j=0; j<9; j++)
          grille[i][j] = 0;
      ```
4. Les commentaire:

      ```javascript
        // Ceci est un commentaire JavaVascript sur une ligne

        /* Ceci est un commentaire JavaScriptsur plusieurs lignes */
      ```

## Exercices d'application

1. Programme de base entrée/sortie:
   - Version 1:
      ```javascript
      <html>
        <Head> <Title > Programmes Entrées et Sorties de Title > </Head>

        <body>
         <script type="text/javascript">
          var Np , Age;
          Np= prompt(" Saisissez votre Nom et Prènom SVP ");
          //Np += n";
          alert("Vous êtes " + Np + n" + " Est ce Exacte !!??);
         </script>
        </body>
      </html>
      ```
   - Version 2:

      ```javascript
      <html>
        <Head> <Title > Programmes Entrées et Sorties de Title > </Head>
        <body>
          <script type="text/javascript>
           var Np ,Age;
           Np= prompt(" Saisissez votre Nom et Prènom SVP ");
           alert("Vous êtes " + Np + n" + " Est ce Exacte !!??);
           age = prompt("Saisissez votre age SVP ");
           alert("Vous avez : " + age + " ans " + " Est vous êtes : " + Np );
          </script>
          <h1> Bon Travail .. Continuons avec le Coding JavaScript </h1>
        </body>
      </html>
      ```
2. Programme instructions conditionelles:


   - Version 1:

     ```html
     <html>
      <head>
            <Title>
            Programmes Table Multiplication avec Boucle
            </Title>
      </head>
      <body>
         <script type="text/javascript">
          var a, i;
          do {
          a=prompt("Saisissez un nomre entier SVP ");
             }
          while(isNaN (a) || a%1!==0);
          document.write("<h2>La table de multiplication du nombre : "+a+"</h2>")
          for(var i =1; i <=10; i ++)
           {
             document.write(" "+a+" x i +" = "
             document.write(" "+ i +" ", n","< br
           }
         </script>
           <p><H1>Bravo !!!!Opération Table de Multiplication en JavaScript Réussie avec succés </H1</p>
      </body>
    </html>
    ```
3. Les outils JavaScript boites de dialogues:


      ```html
          <html>
            <head>
              <title>
                Boites de dialogue
              </title>
            </head>
            <body>
              <center>
              <button onclick ="alert('Bonjour Les étudiants AMEUR ... Veuillez vous Identifiez SVP ')">
              Click Ici .... Surprise </button> <br> <br> <br>
              <button onclick= 'saisir_nom()'> Identifiez vous par votre Nom </button>
            </body>
                <script type="text/javascript ">
                  function saisir_nom()
                  {
                  var nom=prompt(" Quel est votre nom ? ");
                  var conf=confirm(" Vous vous appelez vraiment"+nom + "
                  If(conf){
                  alert("Soyez la Bienvenue "+nom);
                  alert("A la prochaine séance "+nom);
                          }
                  }
              </script>
        </html>
        ```

