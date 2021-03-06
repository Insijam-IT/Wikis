# Resume Git et Github

## Git

- C'est quoi Git

Git est un logiciel de gestion de versions décentralisé. C'est un logiciel libre créé par Linus Torvalds, auteur du noyau Linux, il s’agit du logiciel de gestion de versions le plus populaire qui est utilisé par plus de douze millions de personnes,il permet également, comme beaucoup de ses congénères, de travailler à plusieurs sur un même projet.

- Installer et configurer Git

1. Installation

   - Installer Git sous Mac OS X

     Il y a plusieurs façons d’installer Git sous Mac OS X. Le plus simple est de se baser sur ce lien https://code.google.com/archive/p/git-osx-installer/.
     Vous allez télécharger une archive .dmg. Il suffit de l’ouvrir pour la monter, ce qui vous donnera accès à plusieurs fichiers.
     Ouvrez tout simplement l’archive .pkg qui se trouve à l’intérieur, ce qui aura pour effet d’exécuter le programme d’installation
     Suivez les étapes en laissant les valeurs par défaut (c’est suffisant), et vous aurez installé Git !
     Il vous suffit ensuite d’ouvrir un terminal et vous aurez alors accès aux commandes de Git.

2. Configurer Git

   - Dans la console, commencez par envoyer ces trois lignes :

     ```
     git config --global color.diff auto
     git config --global color.status auto
     git config --global color.branch auto
     ```

     De même, il faut configurer votre nom (ou pseudo) :

     ```
     git config --global user.name "votre_pseudo"
     ```

     Puis votre e-mail :

     ```
     git config --global user.email moi@email.com
     ```

   - Créer un nouveau dépôt ou cloner un dépôt existant

     1. Créer un nouveau dépôt
        Commencez par créer un dossier du nom de votre projet sur votre disque.
        Par exemple, je vais créer/home/Insijam-IT

        ```
         cd /home/Insijam-IT
         mkdir Wikis
         cd Wikis
        ```

     2. Ensuite, initialisez un dépôt Git tout neuf dans
        ce dossier avec la commande :
        ```
        git init
        ```
     3. Cloner un dépôt existant
        Cloner un dépôt existant consiste à récupérer tout l’historique et tous
        les codes source d’un projet avec Git.
        Pour trouver un dépôt Git, rien de plus facile ! Comme je vous le disais,
        GitHub est une formidable fourmilière de dépôts Git.
        Utliser la forme SSH qui est plus sécurisé.
        ```
        git clone git@github.com:Insijam-IT/Wikis.git
        ```
        Les messages suivants devraient apparaître dans la console :
        ```
        $ git clone http://git@github.com:Insijam-IT/Wikis.git
        Initialized empty Git repository in /home/Insijam-IT/Wikis/.git/
        remote: Counting objects: 7820, done.
        remote: Compressing objects: 100% (2490/2490), done.
        remote: Total 7820 (delta 4610), reused 7711 (delta 4528)
        Receiving objects: 100% (7820/7820), 1.40 MiB | 479 KiB/s, done.
        Resolving deltas: 100% (4610/4610), done.
        Checking out files: 100% (565/565), done.
        ```
        Le seul dossier un peu particulier créé par Git est un dossier .git
        (c’est un dossier caché situé à la racine du projet).Il contient l’historique
        des modifications des fichiers et la configuration de Git pour ce projet.

   - Modifier le code et effectuer des commits

     1. Placez-vous dans le répertoire de base du code, par exemple :
        ```
        cd /home/Insijam-IT/Wikis
        ```
        La commande git status vous indique les fichiers que vous
        avez modifiés récemment :
        ```
        $ git status
        # On branch master
        nothing to commit (working directory clean)
        ```
        Ce message nous informe que rien n’a été modifié (nothing to commit).
     2. Méthode de travail

        - modifier le code source
        - tester votre programme pour vérifier si cela fonctionne
        - faire un commit pour « enregistrer » les changements et les faire connaître à Git
        - recommencer à partir de l’étape 1 pour une autre modification.

     3. Effectuer un commit des changements

        faire git add nomfichier1 nomfichier2 pour ajouter les fichiers à la
        liste de ceux devant faire l’objet d’un commit, puis faire un git commit


     * Travailler avec des branches

         C’est un moyen de travailler en parallèle sur d’autres fonctionnalités.
         C’est comme si vous aviez quelque part une « copie » du code source du site
         qui vous permet de tester vos idées les plus folles et de vérifier si elles
         fonctionnent avant de les intégrer au véritable code source de votre projet.

       1. Les branches locales
          ```
          git branch
          ```
          Vous verrez normalement uniquement « master » :
          ```
          git branch
          master
          ```
       2. Créer une branche et changer de branche
          ```
          git branch branch1
          ```
          Une fois la branche créée, vous devriez la voir quand vous tapez simplement
          ```
          $ git branch
          * master
          branch1
          ```
          Comme vous pouvez le voir, vous êtes toujours sur la branche « master ».
          Pour aller sur la branche « branch1 », tapez ceci :
          ```
          git checkout branch1
          ```
       3. Fusionner les changements
          Lorsque vous avez fini de travailler sur une branche et que celle-ci est concluante, il faut « fusionner »
          cette branche vers « master » avec la commande  git merge
          ```
          git merge branch1
          ```
          Votre branche « branch1 » ne servant plus à rien, vous pouvez la supprimer :
          ```
          git branch -d branch1
          ```

## Github

Lorsque vous travaillez sur un projet sur votre machine, il est important d'avoir un backup de
votre code sur une autre machine, au cas où la vôtre tombe en panne par exemple. Une fois que
vous avez travaillé sur votre code et effectué vos commits, vous allez donc les envoyer sur
un remote, c'est-à-dire une autre machine qui peut être :
interne (si vous avez la chance d'avoir plusieurs ordinateurs )
ou externe (grâce à des services comme GitHub ou BitBucket)

- C'est quoi github
  GitHub est un outil gratuit pour héberger du code open source, et propose également des plans
  payants pour les projets de code privés. C'est le numéro 1 mondial et il héberge plus d'une dizaine
  de millions de repositories! .Le site est aussi un espace collaboratif. Chaque utilisateur peut
  contribuer aux projets mis en ligne publiquement sur GitHub, en proposant des modifications.
  Le succès de GitHub repose notamment sur la façon dont le site a facilité ce processus.

- Les etape d'utilisation github

  1.  créer un compte github sur https://github.com/
  2.  connectez-vous à votre compte GitHub. Cliquez sur le bouton "Create new" symbolisé
      par un signe "+" en haut à droite de votre écran, puis "New repository".
      GitHub vous demandera alors de préciser quelques détails sur votre repository:

      - son nom
      - sa description
      - son statut public ou privé. Ici, nous partageons du code open-source, c'est donc public et gratuit :).

      Et voilà, vous avez créé votre premier repository sur GitHub

  3.  Configuration du Clé SSh.
      Nous devons générer des clés SSH qui seront utilisées par GitHub et Heroku pour vous authentifier.
      Ouvrez un terminal et saisissez-le en remplaçant l'e-mail par le vôtre (le même que vous avez utilisé pour créer votre compte GitHub). Il vous demandera des informations. Appuyez simplement sur Entrée jusqu'à ce qu'il demande une phrase secrète.

      ```
      mkdir -p ~/.ssh && ssh-keygen -t ed25519 -o -a 100 -f ~/.ssh/id_ed25519 -C "TYPE_YOUR_EMAIL@HERE.com"
      ```

      Ensuite, vous devez donner votre clé publique à GitHub. Courir:

      ```
      cat ~/.ssh/id_ed25519.pub
      ```

      Il affichera à l'écran le contenu du fichier id_ed25519.pub.
      Copy that text, then go to github.com/settings/ssh. Click on Add SSH key
      remplissez le titre avec le nom de votre ordinateur et collez la clé. Terminez en cliquant sur le bouton vert Ajouter une clé.
      Pour vérifier que cette étape est terminée:

      ```
      ssh -T git@github.com
      ```

      Si vous voyez quelque chose comme ça, vous avez terminé!

      ```
      # Hi --------! You've successfully authenticated, but GitHub does not provide shell access
      ```

      Si cela ne fonctionne pas, essayez d'exécuter ceci avant de réessayer la commande ssh -T:

      ```
      ssh-add ~/.ssh/id_ed25519
      ```

  4.  synchroniser les modifications dans votre repo sur votre machine avec votre repo sur GitHub ?

      ```
      git push origin master
      ```

  5.  Pour récupérer en local les dernières
      modifications du repo GitHub

      ```
      git pull origin master
      ```
