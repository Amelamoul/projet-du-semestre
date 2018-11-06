 L'architecture Global:
 
 L'architecture en couches consiste à diviser une application en différents modules, qui constituent autant de couches. L'objectif est de proposer une meilleure répartition des rôles (chaque module a un rôle clairement défini), la séparation des traitements, ainsi qu'une réduction des dépendances entre les services. Chaque module se doit d'être indépendant des autres pour permettre une meilleure maintenabilité.
Une application peut aisément se diviser en trois niveaux distincts : les données, le traitement de ces données, et leur affichage.

![architecture_niveaux](https://user-images.githubusercontent.com/44230045/48089226-39119400-e204-11e8-9ba5-26ee00cbf1bb.png)

La couche de données: regroupe le stockage et les mécanismes d'accès des données de façon à ce qu'elles soient utilisables par l'application au niveau traitement.

La couche de traitement: concerne à la fois les tâches à réaliser par l'application sur les données et les traitements nécessaires suite à une action venant de l'utilisateur : vérification d'authentification, calculs divers, etc.

Enfin, la couche présentation: gère l'affichage des données et les interactions de l'application avec l'utilisateur. La séparation de cette couche permet notamment de proposer plusieurs présentations pour une même application : la même couche de traitement peut alors servir pour une application lourde et pour une application légère.
Les bonnes pratiques de développement logiciel recommandent de développer ces trois niveaux d'une manière la plus indépendante possible. Ainsi, la décision de changer de modèle de données ne devra impacter que la couche Données ; aucune modification ne devrait être nécessaire dans les deux autres couches.
Mais le découpage en couches va plus loin. Imaginons que, lors du développement d'un logiciel, il soit décidé de changer le système de gestion de base de données, sans pour autant que le modèle de données ne soit modifié. Si la couche de Données est elle-même découpée en modules indépendants les uns des autres, cette décision sera plus rapide à mettre en oeuvre et les modifications nécessaires moins fastidieuses.
Pour cette raison, l'architecture d'un logiciel est le plus souvent présentée plus finement que précédemment : 

![architecture_couches](https://user-images.githubusercontent.com/44230045/48089315-7aa23f00-e204-11e8-8cad-5d19a4ec3de1.png)


Dans cette architecture, nous distinguons :

1)le système de gestion de base de données (SGBD), qui stocke les données utilisées par l'application,
2)la couche de persistance, qui gère le mécanisme de sauvegarde et de restauration des données,
3)la couche d'accès aux données, en charge de l'accès aux données et de leur manipulation, indépendamment du SGBD choisi,
4)la couche de services, ou couche métier, gère la logique de l'application et les traitements à effectuer sur les données, 5)indépendamment de la provenance des données et de la façon dont elles seront affichées une fois les traitements effectués,
6)la couche interface utilisateur, qui s'occupe à la fois d'afficher les données reçues par la couche de services et d'envoyer à la 7)couche de services les informations relatives aux actions de l'utilisateur.

L'objectif de ce tutoriel étant de réaliser des applications Web en JEE, l'architecture de nos solutions devra intégrer la notion de client-serveur et suivre le schéma suivant : 

![architecture_client_serveur 1](https://user-images.githubusercontent.com/44230045/48089572-1d5abd80-e205-11e8-8f7a-190352a2a534.png)

La couche appelée précédemment "interface utilisateur" est désormais remplacée par un client Web, lié par Internet (ou un réseau local) aux autres modules présents, eux, sur un serveur :
![architecture_client_serveur_couches](https://user-images.githubusercontent.com/44230045/48089658-4da25c00-e205-11e8-9d80-e80d15b68823.png)
 
 La plate forme JEE:
 
 une application Web suit le principe d'une architecture client-serveur : 

![architecture_client_serveur](https://user-images.githubusercontent.com/44230045/48088533-93115a00-e202-11e8-9470-05dbeba8808d.png)


SERVEUR D'APPLICATIONS:
 Dans le cas d'une application JEE, l'architecture est quelque peu différente et utilise un serveur d'applications, situé entre le serveur Web et la base de données :
 ![architecture_jee](https://user-images.githubusercontent.com/44230045/48088661-d966b900-e202-11e8-8bb6-ecea2d440790.png)

(1) Le client envoie une requête au serveur
(2) Le serveur Web transmet la requête au serveur d'applications
(3) Le serveur d'applications traite la requête en manipulant les données stockées dans la base de données
(4) Le serveur d'applications envoie au serveur Web le résultat de la requête
(5) Le serveur Web transmet le résultat au client Web, qui peut enfin l'afficher
 

Le serveur d'applications est l'environnement d'exécution des applications côté serveur. Il offre un certain nombre de services tels que: 

l'accès aux composants,
la répartition de charge,
la persistance,
la gestion transactionnelle
la sécurité.
Parmi les serveurs d'applications les plus connus, nous trouverons Glassfish, WebLogic, WebSphere, ou encore Tomcat, que nous utiliserons dans ce tutoriel, combiné au serveur Web Apache.

Bien que Tomcat ne supporte pas l'ensemble des vingt-deux composants de JEE (notamment les EJB, que nous définirons dans le chapitre suivant), il offre tous les services que nous comptons utiliser tout au long de ce tutoriel et présente les avantages d'être libre, gratuit et simple à utiliser et à intégrer dans Eclipse.

LES CONTENEURS:
 La partie Serveur JEE se décompose en deux types de conteneurs : le conteneur Web et le conteneur EJB.

Le conteneur Web est un environnement d’exécution pour les pages JSP et les Servlets qui constituent une passerelle entre l’interface utilisateur et les EJB qui implémentent la logique métier.

Le conteneur EJB est un environnement d’exécution pour les EJB : il héberge les composants métiers et leur fournit les services nécessaires.


![architecture_jee_conteneurs](https://user-images.githubusercontent.com/44230045/48088345-0ebed700-e202-11e8-902a-2d94b6448dc2.png)

Nous l'avons abordé plus haut, Tomcat n'est pas à proprement parler un serveur d'applications. En réalité, c'est uniquement un conteneur Web. Ce tutoriel ne portant pas sur les EJB, Tomcat répond tout à fait à nos besoins.

 

Maintenant que nous savons un peu mieux comment s'organise une application JEE, découvrons les composants de la plate-forme JEE.

La plate-forme JEE regroupe un ensemble de composants qui facilitent la mise en oeuvre d'applications Web en Java, dont les plus utilisés sont :

 1)JPA

La persistance des objets en Java a longtemps donné lieu à des manipulations fastidieuses. Aujourd'hui, la Java Persistence API apporte une solution performante et simple à utiliser. S'appuyant sur JDBC (Java DataBase Connectivity), JPA propose une abstraction suffisante pour que le développeur n'ait, dans la majorité des cas, pas à se préoccuper du fonctionnement de JDBC.
Pour plus de détails sur JPA, nous vous proposons un tutoriel sur cette API et le framework Hibernate qui en constitue une implémentation.

 2)Servlets

Les Servlets forment l'un des composants JEE les plus utilisés. Elles permettent de gérer des requêtes HTTP et de fournir au client une réponse HTTP et forment ainsi la base de la programmation Web JEE.
Les Servlets s’exécutent toujours dans un moteur de Servlet ou conteneur de Servlet permettant d’établir le lien entre la Servlet et le serveur Web. Dans ce tutoriel, nous utiliserons Apache Tomcat.

 3)Pages JSP

Les JSP (Java Server Pages) sont des pages HTML qui permettent l'affichage de contenu web dynamique par l'intégration de fragments de code Java et de directives JSP.

 

4) JSF

Java Server Faces est un framework Java basé sur la notion de composants où l'état d'un composant est enregistré lors du rendu de la page, pour être ensuite restauré au retour de la requête. Il utilise JSP par défaut, mais peut être utilisé avec d'autres technologies, comme par exemple Facelets ou XUL.

 

5)EJB 3.0

Les EJB (Enterprise Java Beans) forment l'une des spécifications majeures de JEE et utilisent le principe des annotations Java. Ils se déclinent en :

    entités (Entity Bean)
    sessions (Session Bean
    messages (Message Bean)
 







