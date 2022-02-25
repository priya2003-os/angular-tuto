# angular-tuto
Construction d'une application à partir de ces 4 composants

- \<app-root> : composant qui englobe les 3 autres 
- \<app-top-bar> : composant qui defini la barre de navigation principale
- \<app-product-list> : composant qui affiche le contenu des "articles"
- \<app-product-alerts> : composants qui affiche la fenêtre des messages d'alerte


<img src="https://angular.io/generated/images/guide/start/app-components.png">
 
 ## Création de la liste de produits 

A partir des données contenu dans le fichier "product.ts" et de la méthode de la "class ProductListComponent" nous allons pouvoir afficher les produits
à partir du fichier "product-list.component.html". La directive structurelle "ngFor" permet de boucler sur un array et d'injecter les éléments dans le DOM. Ici "ngFor" qui se trouve dans la balise ouvrante de la \<div> va nous permettre de boucler les produits afin d'afficher la liste des produits à l'aide des expression introduit par {{}} et "product.name" = {{product.name}} (objet product avec la propriéte name et sa valeur en string ici "Phone XL, Phone Mini, Phone Standar).

Ainsi d'autre éléments peuvent être rajouter comme des lien \<a>

"ngIf" est une directive structurelle qui permet de faire une condition ici dans la balise ouvrante \<p> afin d'afficher une description si celle-ci est "true".

Ajout d'un bouton auquelle on lie un evenement "click" qui appelle la méthode "share()" de la "class ProductListComponent" dont l'instruction est d'afficher une fenetre d'alerte contenant le message : 'The product has been shared!' (window.alert('The product has been shared!');)

## Création d'un nouveau composant

utilisation de la ligne de commande via le terminal :
- ng generate component "nom du composant"
  
ici le nom du nouveau composant : "product-alerts"
- > ng generate component product-alerts

un nouveau composany est crée avec dans "src/app/product-alerts/product-alerts.component.ts" avec tout les éléménts par défaut :
- importation des interfaces
- class 
- les constructeurs vides
