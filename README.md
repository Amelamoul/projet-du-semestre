
 1)Indroduction:
 Les systèmes d’information ont besoin de supporter les changements dans la gestion de l’entreprise de façon rapide et efficace, et de s’adapter au développement rapide des technologies. La majorité des systèmes d’information d’entreprise sont hétérogènes, contiennent une gamme de différents systèmes, d’applications, de technologies, et d’architectures .
Pour gérer les problèmes liés aux changements des besoins, au développement technologique, et à l’intégration, différentes solutions ont été proposées et utilisées a travers le temps mais ces solutions ont plus ou moins échoué . 
l'application Cloud-native :
Cloud-native est une approche pour construire et exécuter des applications qui exploitent pleinement les avantages du modèle de livraison du cloud computing. L'approche Cloud-native est la façon dont les applications sont créées et déployées, non pas où elles sont exécutées. Bien que le cloud public actuel nuise à la réflexion sur l'investissement dans les infrastructures pour pratiquement toutes les industries, un modèle de livraison sans cloud n'est pas exclusif pour les environnements publics. Il convient aux cloud publics et privés. Le plus important est la capacité d'offrir des ressources informatiques presque illimitées, à la demande, ainsi que des services modernes de données et d'applications pour les développeurs. Lorsque les entreprises créent et exploitent des applications de manière native sur le cloud, elles apportent de nouvelles idées au marché plus rapidement et répondent plus rapidement aux demandes des clients.
1)Web services:
     * L'architecture Global:
     Les services Web reprennent la plupart des idées et des principes du Web (HTTP, XML), et les appliquent à des interactions entre machines. Comme pour le World Wide Web, les services Web communiquent via un ensemble de technologies fondamentales qui partagent une architecture commune. Ils ont été conçus pour être réalisés sur de nombreux systèmes développés et déployés de façon indépendante. Les technologies utilisées par les services Web sont HTTP, WSDL, REST, XML-RPC, SOAP et UDDI.

REST
REST (Representational State Transfer) est une architecture de services Web. Élaborée en l'an 2000 par Roy Fiedling, l'un des créateurs du protocole HTTP, du serveur Apache HTTPd et d'autres travaux fondamentaux, REST est une manière de construire une application pour les systèmes distribués comme le World Wide Web.

XML-RPC
XML-RPC est un protocole simple utilisant XML pour effectuer des messages RPC. Les requêtes sont écrites en XML et envoyées via HTTP POST. Les requêtes sont intégrées dans le corps de la réponse HTTP. XML-RPC est indépendant de la plate-forme, ce qui lui permet de communiquer avec diverses applications. Par exemple, un client Java peut parler de XML-RPC à un PerlServer ! o_O

SOAP
SOAP (Simple object Access Protocol) est un protocole standard de communication. C'est l'épine dorsale du système d'interopérabilité. SOAP est un protocole décrit en XML et standardisé par le W3C. Il se présente comme une enveloppe pouvant être signée et pouvant contenir des données ou des pièces jointes.
Il circule sur le protocole HTTP et permet d'effectuer des appels de méthodes à distance.

WSDL
WSDL (Web Services Description Language) est un langage de description standard. C'est l'interface présentée aux utilisateurs. Il indique comment utiliser le service Web et comment interagir avec lui. WSDL est basé sur XML et permet de décrire de façon précise les détails concernant le service Web tels que les protocoles, les ports utilisés, les opérations pouvant être effectuées, les formats des messages d'entrée et de sortie et les exceptions pouvant être envoyées.

UDDI
UDDI (Universal Description, Discovery and Integration) est un annuaire de services. Il fournit l'infrastructure de base pour la publication et la découverte des services Web. UDDI permet aux fournisseurs de présenter leurs services Web aux clients.

![whatisaservicewebprojet](https://user-images.githubusercontent.com/44230045/48788483-35453d80-eceb-11e8-8989-1a5aef4d0ade.png)
   
   * l'architecture de la base de donné:
    L’application consiste dans les composantes suivantes:
       . un ensemble des bases de donnees Web e.g. LibraryThing, ISBNdb (au moins 2 sites Web);
       . une base de donnees BD relationelle qui integre les donnees provenant des bases de donnees sur le Web; 
       . un client de la base de donnees BD.
       
![202688serw](https://user-images.githubusercontent.com/44230045/48789814-29a74600-ecee-11e8-9e3b-2a8fb02d881e.png)
  
  
  MySQL:
  
  
  est un système de gestion de bases de données relationnelles (SGBDR). Il est distribué sous une double licence GPL et propriétaire. Il fait partie des logiciels de gestion de base de données les plus utilisés au monde3, autant par le grand public (applications web principalement) que par des professionnels, en concurrence avec Oracle, PostgreSQL et Microsoft SQL Server.

![489px-mysql svg](https://user-images.githubusercontent.com/44230045/48791586-52313f00-ecf2-11e8-8028-0df7de86a84f.png)


Pourquoi on a choisis les Services Web:


Un service Web permet de mettre les données de votre SIG à la disposition d'utilisateurs qui n'ont pas forcément un accès direct aux données de votre organisation. Lorsque vous présentez votre SIG en tant que services Web, vous le rendez accessible via une multitude d'applications exécutées sur des ordinateurs de bureau, des tablettes PC et des smartphones. Vous pouvez choisir de restreindre la diffusion de vos services web à votre bureau physique, mais vous avez également la possibilité de les diffuser sur n'importe quel appareil capable de se connecter à Internet.
