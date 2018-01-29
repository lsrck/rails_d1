#Explications des concepts principaux de rails#


*Un **site statique** est un site qui présente les mêmes informations a tous les utilisateurs sans distinction.
...*Exemple:* un site vitrine pour présenter son entreprise.
...A l'inverse un **site dynamique** va présenter les informations différement en fonction de l'utilisateur et de ses interactions avec le site internet.
...*Exemple:* réseaux sociaux

Le **Modele View Controler** est un "patron de conception" composé de trois types de modules ayant trois responsabilités différentes : les modèles, les vues et les contrôleurs.
⋅⋅*Le **_Modele_** contient les données à afficher.
⋅⋅*La **_View_** contient la présentation de l'interface graphique.
⋅⋅*Le **_Controler_** pour finir contient la logique concernant les actions effectuées par l'utilisateur.
Il permet de bien se repérer dans l'architecture du site internet et permet de bien comprendre les intéractions entre l'utilisateur et le site internet.

*Les Routes permettent d’interpréter les URL et d’orienter vers les bonnes actions des controlleurs. Ce sont elles qui permettent la creation des chemins du site internet et de connaitre l'architecture du site. 

*Les Bases de Données permettent de stocker un ensemble d'informations. Le prinicpal intéret est ensuite de pouvoir manipuler ses données en choisissant les plus pertinantes. Les bases de données sont dans notre cas gérés en utilisant le langage SQL. Les bases de données sont organisées avec des tables reliées les unes aux autres.

*La méthode get permet de récupérer une ressource, à l'inverse la méthode post permet la création d'une nouvelle ressource. On utilise ainsi la méthpode get pour consulter un article du blog alors qu'on utilisera la methode post pour créer un nouvel article.


*La migration permet de modifier la base de données au fil du temps. Chaque migration correspond à une nouvelle version de la base de données et permet d'ajouter et de retirer des tables, colonnes et entrées.

	ex:
	class CreateArticles < ActiveRecord::Migration[5.1]
	  def change
	    create_table :articles do |t|
	    	t.string :title
	    	t.text :text
	      	t.timestamps
	    end
	  end
	end

*Cette migration permet d'ajouter la table articles avec une colonne nommée titles et une colonne appelée text. En plus de ces deux colonnes, une colonne avec un identifiant unique est implictement ajoutée  ainsi que deux colonnes qui contiennent la date et l'heure de creation et d'update.


*Les relations entre les models des BDD permet de définir les relations entre les différentes informations d'une base de données. Dans le cas du blog, il est défini qu'un article peut avoir plusieurs commentaires qu'il est impossible pour un commentaire d'être relié à plusieurs articles.

*Les fonctions du CRUD (Create Read Update Delete) correspondent aux quatre types d'opérations qu'il est possible d'effectuer sur les bases de données. Dans le cadre de notre blog, la fonction create permet la creation d'un nouvel élément dans la base de données: un article. La fonction read permet de récupérer les données liées à cet article. La fonction update permet une mise à jour des données de l'article (contenu, titre...). Enfin la fonction delete permet la suppression des données dans la base de données et donc de l'article en question.

[Mon GitHub](https://github.com/lsrck)
