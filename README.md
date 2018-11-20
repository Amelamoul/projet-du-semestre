
 1)Indroduction:
 
 
 
 
 Les systèmes d’information ont besoin de supporter les changements dans la gestion de l’entreprise de façon rapide et efficace, et de s’adapter au développement rapide des technologies. La majorité des systèmes d’information d’entreprise sont hétérogènes, contiennent une gamme de différents systèmes, d’applications, de technologies, et d’architectures .
Pour gérer les problèmes liés aux changements des besoins, au développement technologique, et à l’intégration, différentes solutions ont été proposées et utilisées a travers le temps mais ces solutions ont plus ou moins échoué .




2)l'application Cloud-native :







Cloud-native est une approche pour construire et exécuter des applications qui exploitent pleinement les avantages du modèle de livraison du cloud computing. L'approche Cloud-native est la façon dont les applications sont créées et déployées, non pas où elles sont exécutées. Bien que le cloud public actuel nuise à la réflexion sur l'investissement dans les infrastructures pour pratiquement toutes les industries, un modèle de livraison sans cloud n'est pas exclusif pour les environnements publics. Il convient aux cloud publics et privés. Le plus important est la capacité d'offrir des ressources informatiques presque illimitées, à la demande, ainsi que des services modernes de données et d'applications pour les développeurs. Lorsque les entreprises créent et exploitent des applications de manière native sur le cloud, elles apportent de nouvelles idées au marché plus rapidement et répondent plus rapidement aux demandes des clients.



1)les microservice:



les microservices sont un style d'architecture logicielle à partir duquel un ensemble complexe d'applications est décomposé en plusieurs processus indépendants et faiblement couplés, souvent spécialisés dans une seule tâche. Les processus indépendants communiquent les uns avec les autres en utilisant des API langage-agnostiques.





2)MVC:
L'architecture Modèle/Vue/Contrôleur (MVC) est une façon d'organiser une interface graphique d'un programme. Elle consiste à distinguer trois entités distinctes qui sont, le modèle, la vue et le contrôleur ayant chacun un rôle précis dans l'interface.






3) Monolithique:


est un bloc de pierre de grande dimension, constitué d’un seul élément, naturel ou taillé voire déplacé par l’Homme.




Dans notre application on a choisis L'architecture MVC




MVC:


Le modèle MVC décrit une manière d’architecturer une application informatique en la décomposant en trois sous-parties :

la partie Modèle ;
la partie Vue ;
la partie Contrôleur.
Ce modèle de conception a été imaginé à la fin des années 1970 pour le langage Smalltalk afin de bien séparer le code de l’interface graphique de la logique applicative. Il est utilisé dans de très nombreux langages : bibliothèques Swing et Model 2 (JSP) de Java, frameworks PHP, ASP.NET MVC, etc.


3)L'architecture Global:


modèle:





contient les données manipulées par le programme. Il assure la gestion de ces données et garantit leur intégrité. Dans le cas typique d'une base de données, c'est le modèle qui la contient.

Le modèle offre des méthodes pour mettre à jour ces données (insertion suppression, changement de valeur). Il offre aussi des méthodes pour récupérer ses données. Dans le cas de données importantes, le modèle peut autoriser plusieurs vues partielles des données. 







 la vue:
 
 
 
 
 
 
 fait l'interface avec l'utilisateur. Sa première tâche est d'afficher les données qu'elle a récupérées auprès du modèle. Sa seconde tâche est de recevoir tous les actions de l'utilisateur (clic de souris, sélection d'une entrées, boutons, …). Ses différents événements sont envoyés au contrôleur.
La vue peut aussi donner plusieurs vues, partielles ou non, des mêmes données. Par exemple, l'application de conversion de bases a un entier comme unique donnée. Ce même entier est affiché de multiples façons (en texte dans différentes bases, bit par bit avec des boutons à cocher, avec des curseurs). La vue peut aussi offrir la possibilité à l'utilisateur de changer de vue.






 contrôleur:
 
 
 
 
 
Le contrôleur est chargé de la synchronisation du modèle et de la vue. Il reçoit tous les événements de l'utilisateur et enclenche les actions à effectuer. Si une action nécessite un changement des données, le contrôleur demande la modification des données au modèle et ensuite avertit la vue que les données ont changé pour que celle-ci se mette à jour. Certains événements de l'utilisateur ne concerne pas les données mais la vue. Dans ce cas, le contrôleur demande à la vue de se modifier.



![mvc](https://user-images.githubusercontent.com/44230045/48795502-6890c800-ecfd-11e8-8b80-57b006b5eefc.png)





![370px-modelemvc](https://user-images.githubusercontent.com/44230045/48795774-19976280-ecfe-11e8-991c-1388859ddd2b.png)




L'architecture de la couche des donnée:




![mvc bd](https://user-images.githubusercontent.com/44230045/48798814-c1fcf500-ed05-11e8-9ea6-e22bdcf4c4e4.png)



une application constituée de plusieurs contrôleurs, chaque contrôleur étant lui-même constitué d’un ensemble d’actions. La première caractéristique de cette organisation est donc de structurer hiérarchiquement une application. Dans les cas simples, un seul contrôleur suffit, contenant l’ensemble des actions qui constituent l’application Web.

Chaque requête HTTP est analysée par le framework qui détermine alors quel sont le contrôleur et l’action concernés. Il existe un contrôleur frontal (intégré au framework et donc transparent pour le programmeur), chargé de recevoir les requêtes HTTP, qui exécute l’action en lui passant les paramètres HTTP. Il se base notamment sur les mappings qui associent des URLs à des servlets


La maniére de gestion des demandes des clients:



le visiteur demandera la page au contrôleur et c'est la vue qui lui sera retournée. Bien entendu, tout cela est transparent pour lui, il ne voit pas tout ce qui se passe sur le serveur. C'est un schéma plus complexe que ce à quoi vous avez été habitués, bien évidemment : c'est pourtant sur ce type d'architecture que repose un grand nombre de sites professionnels .



![382129mvv](https://user-images.githubusercontent.com/44230045/48800083-18b7fe00-ed09-11e8-9362-aa414cf87a8c.png)



pourquoi on a choisis le MVC:



Une conception claire et efficace grâce à la séparation des données de la vue et du contrôleur
Un gain de temps de maintenance et d’évolution du site
Une plus grande souplesse pour organiser le développement du site entre différents développeurs (indépendance des données, de l’affichage (webdesign) et des actions)
