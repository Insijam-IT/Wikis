## Gestion du banque

- Classe Compte

  ```ruby
    class Compte

      attr_accessor :numeroCompte,:nomCompte,:dateCreation,:solde

      def initialize(numeroCompte,nomCompte,dateCréation)
        @numeroCompte=numeroCompte
        @nomCompte=nomCompte
        @dateCréation=dateCréation
        @solde=0
      end

      def affichierCompte
        puts "Le nom de compte est: #{nomCompte} ,crée en: #{dateCréation} ,solde: #{solde}DH"
      end

      def debiterCompte(somme)
        @solde += somme
        puts "le compte a été debité de #{somme}"
      end

      def créditerCompte(somme)
        @solde -= somme
        puts "le compte a été crédité de #{somme}"
      end

    end
  ```

* Classe Personne

  ```ruby
    class Personne

      attr_accessor :comptes,:nom,:prenom

      def initialize(nom,prenom,cin)
        @nom = nom
        @prenom = prenom
        @cin = cin
        @comptes=[]
      end

      def afficherComptes
        puts "Voici les comptes de #{@nom} #{@prenom}: "
        comptes.each do|compte|
          puts compte.nomCompte
        end
      end
    end

  ```

* Classe Banque

  ```ruby
    class Banque
      attr_accessor :nomBanque,:adresse,:comptes,:personnes

      def initialize(nomBanque,adresse)
        @nomBanque=nomBanque
        @adresse=adresse
        @comptes=[]
        @personnes=[]
      end

      def afficherClients
        puts "voici les clients existe dans la #{@nomBanque}"
        personnes.each do |personne|
          puts "#{personne.nom} #{personne.prenom}"
        end
      end

      def afficherParBanque
        puts "voici les comptes existe dans la #{@nomBanque}"
        comptes.each do |compte|
          puts compte.nomCompte
        end
      end

    end
  ```

* Test

  ```ruby
    #creation des banques
    banque1=Banque.new("banque1","Casa Ain chok Rue14 N 41")
    banque2=Banque.new("banque2","Casa Derb sultan Rue 33 N 54")

    #creation des comptes
    compte1=Compte.new(1,"compte1","09/03/2020")
    compte2=Compte.new(2,"compte2","09/03/2020")
    compte3=Compte.new(1,"compte3","09/04/2020")

    #creation des personnes
    amine = Personne.new("Reda","Amine","Bk342564")
    rachid=Personne.new("Reda","Rachid","Bk657876")

    #ajouter les comptes aux banques
    banque1.comptes << compte1
    banque1.comptes << compte2
    banque2.comptes << compte3

    #ajouter les comptes aux personnes
    amine.comptes << compte1
    amine.comptes << compte2
    rachid.comptes << compte3

    #ajouter les personnes aux banques
    banque1.personnes << amine
    banque2.personnes << rachid

    #afficher les comptes pour chaque personne
    amine.afficherComptes
    #=>Voici les comptes de Reda Amine:
    #=>compte1
    #=>compte2
    rachid.afficherComptes
    #=>Voici les comptes de Reda Rachid:
    #=>compte3

    #faire l'opération debiter
    compte1.debiterCompte(2000)
    puts compte1.affichierCompte
    #=>le compte a été debité de 2000
    #=>Le nom de compte est: compte1 ,crée en: 09/03/2020 ,solde: 2000DH

    #faire l'opération créditer
    compte1.créditerCompte(3000)
    puts compte1.affichierCompte
    #=>le compte a été debité de 3000
    #=>Le nom de compte est: compte1 ,crée en: 09/03/2020 ,solde: -1000DH

    #afficher les clients de la banque
    banque1.afficherClients
    banque2.afficherClients
    #=>voici les clients existe dans la banque1
    #=>Reda Amine
    #=>voici les clients existe dans la banque2
    #=>Reda Rachid

    #afficher les comptes existe dans une banque
    banque1.afficherParBanque
    banque2.afficherParBanque
    #=>voici les comptes existe dans la banque1
    #=>compte1
    #=>compte2
    #=>voici les comptes existe dans la banque2
    #=>compte3
  ```
