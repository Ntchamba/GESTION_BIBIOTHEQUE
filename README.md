
# GESTION_BIBIOTHEQUE
Application en console(CLI) de gestion d'une biblitheque .afin de remedier aux difficultes dans la gestion
des emprunts ,de l'ajout ,de la suppression de nouveaux livres , des recherches de livre , la location des espaces de travail tout cela  dans une bibliotheque.

## Membres et participation
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membres             |      role                         | nom
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre1             |la classe salle                    |  Lapobe Zacharie
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre2             |la class emprunt et location_salle |  Nembe Denise
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre3             |la class Catalogue                 | Oumate Alim 
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre4             |la classe Bibliotheque et livre    | umarou hamid
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre5             |la classe Client                   | steve jorel
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
membre6             |la class Main                      | ntchamba alan
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++


## Acknowledgements
  A l'attention des membres :
  -<List> : fait juste reference au type ArrayList
   
 modelisation UML:
 Diagramme des classes

 class Client {
   -id_ client : String
   -nom_client : String
   -numero_de_CNI : String
   -date_emprunt:Date
   -duree_emprunt:int
   <List> locations_salle : LocationSalle
   <List> emprunts : Emprunt
   +emprunter(livre : Livre):void
   +afficher():void
   +supprimerCompte(id_utilisateur:String):void
   +modifierCompte(id_utilisateur:String):void
    
    }



 class Salle {
    -id_espace_travail: String
    -cote_salle: String
    -Etat_location:boolean
 }   



 class Livre {
    -id_livre:String
    -nom_livre:String
    -nom_auteur:String
    -cote:String
    +supprimerLivre(id_livre: String)
    +modifier(id_livre:String)
    
 }



 class Catalogue{
    -id_catalogue : String
    -cote:String
    <List> livre: Livre 
    +ajouterLivre(livre: Livre): void
    +afficher():Livre
    +rechercheLivre(id_Livre: String):String
    +filtreNom(nom:String):void
    +filtreAuteur(nom:String):void
    +supprimerLivre(id_livre: String):void
    +modifierLivre(id_livre: Livre):void
 }




 
 class Emprunt extends Location{
    -id_livre :String 
    <List>bibliothecaires : Bibliothecaires
    <List>livres : Livre
    -date_emprunt: Date
    -duree_emprunt: int
    -id_client: String
    -penalites: int 
    +ajouterPenalite():void
 }


<<Abstrack>> class Location{
-dureeLocation : int
-dateLocation : Date
}

class LocationSalle extends Location{

    <List> salles : Salle
    <List> clients : Client
    
}







 class Bibliothecaire   {
    code_bibliothecaire: String
    nom_bibliothecaire: String
    heure_de_services: String

 }
    -


                

## Tech 

**language:** java



## Documentation

### lancement du CLI
les commandes neccessaires pour lancer le projet sont: javac Main.java et
 java Main  .
### premiere interface

### seconde interface

### troisieme interface
## Contributions

des contributions sont la bienvenu!


adherez au projet .Merci beaucoup.
