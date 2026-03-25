Question 1Ignoré  
Lequel des services AWS suivants est utilisé pour stocker des données de manière hautement évolutive et durable ?  
Stockage par blocs Amazon  
Amazon EFS  
**Bonne réponse**  
S3  
Question 2Correct  
Qui est responsable de la sécurité et de la conformité dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
AWS et le client partagent la responsabilité  
AWS partage la responsabilité avec l'organisme de réglementation compétent.  
La responsabilité incombe au client.  
C'est AWS qui est responsable.  
Question 3Correct  
Dans quelle mesure le plan de support Business vers lequel votre plan de support AWS a été mis à niveau est-il performant ?  
Assistance avec un délai de réponse inférieur à 24 heures en cas de panne de votre système de production  
**Votre réponse est correcte**  
Assistance avec un délai de réponse inférieur à 1 heure en cas de panne de votre système de production.  
Assistance avec un temps de réponse inférieur à 15 minutes en cas de panne de votre système de production.  
Question 4Correct  
Quel service AWS utilisez-vous pour contrôler qui peut accéder à vos ressources AWS ?  
**Votre réponse est correcte**  
Gestion des identités et des accès AWS  
Politique de ressources AWS  
MFA  
Question 5Correct  
Laquelle des propositions suivantes relève des obligations du client dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
Installation des correctifs de sécurité du système d'exploitation pour les instances de base de données Amazon EC2  
Installation des correctifs du système d'exploitation pour Amazon DynamoDB  
Installation des correctifs de sécurité pour les hyperviseurs Xen et KVM  
Question 6Incorrect  
Quelle option permet de partager publiquement des compartiments entiers, y compris celui hébergeant un site web S3 ?  
**Bonne réponse**  
Politiques de compartimentage   
**Votre réponse est incorrecte**  
Listes de contrôle des compartiments  
Politiques d'accès  
Question 7Ignoré  
Ce qui suit décrit une application qui s'étend sur plusieurs zones de disponibilité.  
possédant une élasticité  
**Bonne réponse**  
étant très disponible  
en utilisant des économies d'échelle  
ayant une portée mondiale  
Question 8Correct  
Laquelle des propositions suivantes décrit l'élasticité dans le cloud AWS ?  
Rapidité de redémarrage d'une instance Amazon EC2  
Le modèle de facturation au paiement à l'utilisation  
**Votre réponse est correcte**  
La capacité d'adapter les ressources à l'évolution de la demande  
Question 9Ignoré  
Quel concept d'architecture cloud est pris en charge par un système capable de s'adapter en termes d'utilisateurs, de trafic ou de quantité de données sans sacrifier les performances ?  
**Bonne réponse**  
Mettre en œuvre l'élasticité  
Pensez parallèle  
Découplez vos composants  
Concevoir pour l'échec  
Question 10Incorrect  
Quel service de stockage AWS est idéal pour stocker des ensembles de données volumineux, non structurés et rarement consultés, tels que les sauvegardes et les fichiers journaux ?  
**Bonne réponse**  
Amazon Glacier  
Elastic Block Store (EBS)  
Service de stockage simple (S3)  
**Votre réponse est incorrecte**  
Système de fichiers élastique Amazon (EFS)  
Question 11Ignoré  
Quelles sont les obligations du client lorsqu'il utilise un service géré AWS dans le cadre du modèle de responsabilité partagée d'AWS ?  
Sécurité physique des centres de données  
**Bonne réponse**  
Données client  
correctifs du système d'exploitation  
Chiffrement côté serveur  
Question 12Incorrect  
Quelle est la responsabilité des clients dans le modèle de responsabilité partagée d'AWS ?  
**Votre réponse est incorrecte**  
Sécurité des centres de données  
**Bonne réponse**  
Données chiffrées au repos  
Application de correctifs au système d'exploitation hôte  
Mise au rebut du vieux matériel  
Question 13Correct  
À quel contrôle AWS Trusted Advisor tous les utilisateurs AWS ont-ils accès ?  
Contrôles d'optimisation des coûts  
**Votre réponse est correcte**  
Contrôles de base  
Tous les contrôles  
Contrôles de tolérance aux pannes  
Explication générale  
Tous les utilisateurs d'AWS ont accès aux cinq vérifications principales d'AWS Trusted Advisor, disponibles pour tous les clients AWS, y compris ceux qui utilisent le niveau gratuit. Ces cinq vérifications principales sont :

1. Limites de service \- Cette vérification permet d'identifier les limites de service AWS qui s'approchent ou sont dépassées, ce qui pourrait potentiellement impacter les performances ou la disponibilité de votre application.  
2. Utilisation d'IAM \- Cette vérification permet d'identifier les utilisateurs et les rôles IAM qui n'ont pas été utilisés au cours des 90 derniers jours, ce qui pourrait indiquer des autorisations IAM inutiles pouvant être supprimées afin de réduire le risque d'accès non autorisé.  
3. Authentification multifacteur sur le compte racine \- Cette vérification permet d'identifier les comptes AWS sur lesquels l'authentification multifacteur (MFA) n'est pas activée sur le compte racine, ce qui constitue une bonne pratique de sécurité pour se protéger contre les accès non autorisés.  
4. Instantanés publics EBS \- Cette vérification permet d'identifier les instantanés Amazon Elastic Block Store (EBS) marqués comme publics, qui pourraient potentiellement exposer des données sensibles à un accès non autorisé.  
5. Groupes de sécurité \- Ports spécifiques non restreints \- Cette vérification permet d'identifier les groupes de sécurité dont les règles entrantes autorisent le trafic provenant de n'importe quelle adresse IP ou plage d'adresses IP sur des ports spécifiques, ce qui pourrait potentiellement exposer votre application à des attaques.

Ces contrôles de base fournissent aux utilisateurs des recommandations concrètes pour améliorer leur sécurité, leurs performances et leur rentabilité. En plus de ces contrôles de base, AWS Trusted Advisor propose des contrôles supplémentaires dans les domaines de l'optimisation des coûts, des performances, de la sécurité et de la tolérance aux pannes. Cependant, certains de ces contrôles peuvent nécessiter un plan de support Business ou Enterprise pour être accessibles.  
Question 14Ignoré  
Quel est le principe de conception du framework AWS Well-Architected pour l'excellence opérationnelle ?  
N'attribuez que les privilèges minimaux requis.  
**Bonne réponse**  
Déployer des changements plus petits et réversibles  
Privilégiez les architectures sans serveur.  
Question 15Correct  
Ce qui suit décrit une application qui s'étend sur plusieurs zones de disponibilité :  
**Votre réponse est correcte**  
étant très disponible  
en utilisant des économies d'échelle  
ayant une portée mondiale  
Question 16Incorrect  
Quels sont les problèmes rencontrés lorsqu'une entreprise déploie des serveurs web sur plusieurs régions AWS ?  
Disponibilité  
Sécurité  
**Votre réponse est incorrecte**  
Couplage  
**Bonne réponse**  
Durabilité  
Question 17Correct  
De quelles obligations liées à la sécurité AWS est-elle responsable dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
Sécurité physique des infrastructures mondiales  
Chiffrement des volumes Amazon EBS  
Gestion du cycle de vie des identifiants IAM  
Configuration du pare-feu  
Question 18Correct  
Dans le cadre du modèle de responsabilité partagée, lequel des éléments suivants relève d'un contrôle partagé entre un client et AWS ?  
Sécurité de zone  
Audit des centres de données  
**Votre réponse est correcte**  
Gestion des correctifs  
Commandes physiques  
Question 19Correct  
Quelle action, en termes d'architecture AWS Cloud, est compatible avec le concept de moindre privilège ?  
Empêcher les responsables d'accéder au code source important.  
**Votre réponse est correcte**  
Accorder aux utilisateurs l'accès minimal nécessaire à l'exécution d'une tâche  
Utilisez les balises  
Attribuer des autorisations en fonction des intitulés de poste.  
Question 20Incorrect  
Quelle est une technique permettant d'unifier la facturation si chaque département au sein d'une entreprise

possède son propre compte AWS ?  
Utilisez AWS Budgets sur chaque compte pour ne payer que dans les limites du budget.  
**Bonne réponse**  
Créez une organisation AWS à partir du compte payeur et invitez les autres comptes à la rejoindre.  
**Votre réponse est incorrecte**  
Contactez le support AWS pour obtenir une facture mensuelle  
Question 21Ignoré  
Quels services AWS sont gérés par AWS et permettent de déployer des applications sans serveur ?  
**Bonne réponse**  
Lambda  
haricot élastique  
Fargate  
Question 22Ignoré  
Selon le modèle de responsabilité partagée d'AWS, quelle tâche est partagée entre AWS et le client ?  
**Bonne réponse**  
Gestion des correctifs et gestion de la configuration  
Gestion et chiffrement du matériel serveur  
Sécurité des applications  
Contrôles physiques et environnementaux  
Question 23Ignoré  
Comment créer une application pour qu'elle fonctionne sur le cloud AWS conformément aux meilleures pratiques ?  
**Bonne réponse**  
Utilisez des composants faiblement couplés  
Utiliser des composants fréquemment couplés  
Utilisez des composants étroitement couplés.  
Utiliser des composants rarement couplés  
Question 24Ignoré  
Quelles autorisations parmi les suivantes sont gérées par les politiques de contrôle des services ?

(SCP) ?  
Régions AWS  
Emplacements périphériques  
**Bonne réponse**  
Organisations AWS  
Zones de disponibilité  
Question 25Correct  
Quels sont les avantages de l'élasticité du cloud AWS ?  
**Votre réponse est correcte**  
Ajustement automatique de la capacité de calcul requise pour maintenir une cohérence

performance  
Autorisez AWS à sélectionner automatiquement les services les plus rentables.  
Assurez-vous que le trafic web soit automatiquement réparti sur plusieurs régions AWS.  
Réduisez les coûts de stockage en archivant automatiquement les données de journalisation.  
Question 26Ignoré  
Quel est l'un des 6 avantages du cloud computing ?  
Estimer facilement la capacité  
**Sélection correcte**  
vitesse et agilité accrues  
Échangez les dépenses variables contre des dépenses d'investissement.  
Question 27Correct  
Lequel des éléments suivants constitue un inconvénient de l'utilisation d'AWS ElastiCache ?  
Son évolutivité est limitée  
Il peut être difficile de le configurer  
**Votre réponse est correcte**  
Cela peut coûter cher.  
Explication générale  
L'utilisation d'AWS ElastiCache peut engendrer des coûts supplémentaires par rapport à l'exécution de votre propre solution de cache en mémoire, car vous payez pour l'infrastructure sous-jacente et la gestion du service de cache. Ces coûts varient en fonction du type de nœuds de cache, du volume de données mises en cache et du niveau d'utilisation.  
Question 28Ignoré  
Quel est le nom du service AWS qui permet de gérer et d'administrer les bases de données ?  
Amazon DynamoDB  
Amazon S3  
**Bonne réponse**  
Amazon RDS  
Question 29Ignoré  
Quel pilier du cadre AWS Well-Architected est conçu sur l'idée de modifications fréquentes, mineures et réversibles ?  
efficacité de performance  
Fiabilité  
**Bonne réponse**  
Excellence opérationnelle  
optimisation des coûts  
Question 30Ignoré  
Quel pilier du cadre AWS Well-Architected est soutenu par la philosophie de conception de la performance

opérations sous forme de code ?  
Fiabilité  
**Bonne réponse**  
Excellence opérationnelle  
Sécurité  
efficacité de performance  
Question 31Correct  
Dans le modèle de responsabilité partagée, laquelle des propositions suivantes relève de la responsabilité d'AWS ?  
Chiffrement côté serveur (SSE)

#### Explications

Le chiffrement côté serveur (SSE) relève de la responsabilité du client dans le cadre du modèle de responsabilité partagée d'AWS. Il consiste à chiffrer les données stockées sur les serveurs AWS afin de les protéger contre tout accès non autorisé.  
Configuration du pare-feu

#### Explications

Dans le cadre du modèle de responsabilité partagée d'AWS, la configuration du pare-feu relève de la responsabilité du client. Elle consiste à définir et à gérer les règles de pare-feu afin de contrôler le trafic entrant et sortant vers et depuis les ressources AWS.  
**Votre réponse est correcte**  
Maintenance du matériel physique

#### Explications

La maintenance du matériel physique relève de la responsabilité d'AWS dans le cadre du modèle de responsabilité partagée. AWS est responsable de l'infrastructure physique, notamment des centres de données, des serveurs, des équipements réseau et des périphériques de stockage. Cela inclut la garantie de la sécurité, de la disponibilité et de la maintenance du matériel nécessaire au fonctionnement des services cloud AWS.  
Gestion des identités et des accès (IAM)

#### Explications

La gestion des identités et des accès (IAM) relève de la responsabilité du client dans le cadre du modèle de responsabilité partagée d'AWS. Elle consiste à gérer l'accès, les autorisations et l'authentification des utilisateurs au sein de l'environnement AWS.  
Question 32Correct  
Quel service de stockage AWS offre un stockage haute durabilité pour les objets ?  
stockage par blocs  
RDS  
**Votre réponse est correcte**  
S3  
Question 33Ignoré  
Comment accorder à une instance Amazon EC2 l'accès à un compartiment Amazon S3 conformément aux meilleures pratiques de sécurité ?  
**Bonne réponse**  
Configurez l'instance EC2 pour qu'elle assume un rôle lui permettant d'obtenir les privilèges nécessaires au chargement du fichier.  
Stockez la clé secrète et la clé d'accès de l'utilisateur IAM dans un fichier texte sur l'instance EC2, puis lisez les clés.  
Intégration des informations d'identification de l'utilisateur IAM dans le code de l'application et téléchargement du fichier.  
Modifiez la politique du compartiment S3 afin que n'importe quel service puisse y télécharger des données à tout moment.  
Question 34Correct  
Si vous travaillez sur un projet et que vous devez utiliser un outil pour gérer et déployer vos applications conteneurisées sur AWS, quel service AWS devriez-vous utiliser ?  
**Votre réponse est correcte**  
Amazon ECS  
Amazon Fargate  
Amazon ECR  
Question 35Ignoré  
Parmi les propositions suivantes, laquelle correspond à une plage d'adresses IP utilisables au sein d'un VPC Amazon ?  
10.0.0.0 \- 10.255.255.255  
192.168.0.0 \- 192.168.255.255  
0.0.0.0 \- 255.255.255.255  
**Bonne réponse**  
172.16.0.0 \- 172.31.255.255  
Explication générale  
Amazon VPC vous permet de définir une topologie de réseau virtuel similaire à un réseau traditionnel que vous pourriez exploiter dans votre propre centre de données. Lors de la création d'un VPC, vous devez spécifier une plage d'adresses IP sous la forme d'un bloc CIDR (Classless Inter-Domain Routing). Ce bloc CIDR doit appartenir aux plages d'adresses IP privées spécifiées dans la RFC 1918 : 10.0.0.0/8, 172.16.0.0/12 et 192.168.0.0/16. La réponse C correspond à la plage d'adresses IP privées 172.16.0.0/12, qui autorise jusqu'à 1 048 576 adresses IP.  
Question 36Ignoré  
Quel service AWS permet d'identifier la personne ayant effectué la requête API lorsqu'une instance Amazon EC2 est arrêtée ?  
**Bonne réponse**  
AWS Cloud Trail  
AWS X-Ray  
Amazon CloudWatch  
Gestion des identités et des accès AWS (IAM)  
Explication générale  
Lorsqu'une instance EC2 est arrêtée, AWS CloudTrail enregistre l'événement dans un journal contenant des informations telles que l'heure de l'événement, l'identité de l'utilisateur ou du rôle ayant effectué la requête API, l'adresse IP source de la requête et les détails de celle-ci. Ces informations permettent d'identifier l'auteur de la requête API.  
Question 37Correct  
De quoi AWS est-il responsable dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
Gestion de l'infrastructure réseau  
Maintenir le trafic de l'application  
Configuration d'Amazon VPC  
Question 38Ignoré  
Quel outil ou service fourni par AWS pouvez-vous utiliser pour configurer et contrôler cet environnement de cloud privé ?  
**Bonne réponse**  
VPC  
sous-réseaux  
EC2  
Question 39Incorrect  
Quelles sont les responsabilités du client lors de l'administration des fonctions AWS Lambda dans le cadre du modèle de responsabilité partagée d'AWS ?  
Adaptation des ressources Lambda à la demande  
**Bonne réponse**  
Création de versions des fonctions Lambda  
**Votre réponse est incorrecte**  
Mise à jour de l'environnement d'exécution Lambda  
Maintenance des serveurs et des systèmes d'exploitation  
Question 40Incorrect  
Parmi les options de stockage AWS suivantes, laquelle est la mieux adaptée au stockage et à l'accès à des ensembles de données fréquemment consultés qui nécessitent des performances élevées et une faible latence ?  
**Bonne réponse**  
Système de fichiers élastique Amazon (EFS)  
**Votre réponse est incorrecte**  
Amazon Elastic Block Store (EBS)  
Amazon Simple Storage Service (S3)  
Question 41Ignoré  
Quelle est l'obligation du client dans le cadre du modèle de responsabilité partagée ?  
S'assurer que les disques durs sont effacés après utilisation.  
**Bonne réponse**  
Garantir le chiffrement des données au repos.  
S'assurer que le firmware des périphériques matériels est mis à jour  
Question 42Ignoré  
Quels scénarios un utilisateur doit-il signaler à l'équipe de lutte contre les abus d'AWS ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Les ressources AWS sont utilisées pour héberger du contenu répréhensible ou illégal.  
**Sélection correcte**  
Une attaque DDoS est en cours sur une ressource AWS.  
Une entreprise reçoit des requêtes HTTPS sur un serveur web qui sert du HTTP.  
Question 43Ignoré  
Parmi les contrôles opérationnels suivants, lesquels les utilisateurs héritent-ils intégralement d'AWS dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Bonne réponse**  
Aucune des réponses ci-dessus  
Maintenance des centres de données physiques  
Gestion des correctifs du système d'exploitation sous-jacent  
Gestion de la sécurité du centre de données  
Gestion des utilisateurs et des accès  
Explication générale  
La réponse correcte est que, dans le cadre du modèle de responsabilité partagée d'AWS, les utilisateurs n'héritent absolument d'aucun contrôle opérationnel d'AWS.

Dans le cadre du modèle de responsabilité partagée d'AWS, AWS est responsable de la sécurité du cloud, notamment de la sécurité physique des centres de données, de l'infrastructure matérielle et logicielle, ainsi que des services de base. Cependant, les clients d'AWS sont responsables de la sécurité des charges de travail qu'ils déploient sur AWS, y compris le système d'exploitation, les applications et les données. Cela signifie que les utilisateurs sont responsables de tous les contrôles opérationnels, y compris la gestion de la sécurité du centre de données, la gestion des correctifs, la gestion de la configuration et la gestion des utilisateurs et des accès.  
Question 44Ignoré  
Parmi les options tarifaires suivantes, laquelle permettrait la réduction la plus importante après la réservation d'un hôte dédié Amazon EC2 ?  
Paiement partiel anticipé  
**Bonne réponse**  
Paiement intégral à l'avance  
Paiement horaire à la demande  
Aucun paiement initial  
Question 45Ignoré  
Une entreprise souhaite développer une nouvelle application métier. Quels concepts de conception doivent être appliqués conformément au cadre AWS Well-Architected ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Découpler l'architecture AWS Cloud pour décomposer les déploiements monolithiques  
Déplacez le matériel réseau sur site vers des VPC  
Regroupez plusieurs comptes AWS en un seul compte.  
**Sélection correcte**  
Intégrez l'élasticité dans la conception du cloud AWS.  
Question 46Ignoré  
Quels services ou fonctionnalités AWS Enterprise Support offre-t-il que les autres abonnements AWS Support ne proposent pas ?  
Cas de support AWS  
**Bonne réponse**  
Équipe de conciergerie  
Conseiller de confiance AWS  
Explication générale  
Le support AWS Enterprise propose le service Concierge, une fonctionnalité non disponible dans les autres abonnements de support AWS. L'équipe Concierge offre un accompagnement et des conseils personnalisés pour aider les entreprises à optimiser leur infrastructure AWS.  
Question 47Ignoré  
Selon le modèle de responsabilité partagée d'AWS, qui est responsable de la gestion des accès utilisateurs et des clés secrètes IAM ?  
Les clés d'accès et les clés secrètes IAM sont statiques, il n'est donc pas nécessaire de les renouveler.  
**Bonne réponse**  
Le client est responsable de la rotation des clés  
AWS fera tourner les clés chaque fois que cela sera nécessaire.  
Question 48Incorrect  
Lors de la configuration d'une distribution CloudFront, quelles options peuvent être désignées comme origine ?  
**Votre réponse est incorrecte**  
Emplacement périphérique  
Route 53  
**Bonne réponse**  
compartiment S3  
Question 49Ignoré  
Quel service d'archivage de données est réputé pour être extrêmement abordable, mais peut nécessiter un délai de récupération de plusieurs heures ?  
S3-IA  
**Bonne réponse**  
Glacier  
Norme S3  
Question 50Incorrect  
Quel concept d'architecture cloud est pris en charge par la répartition des charges de travail sur différentes zones de disponibilité ?  
Concevoir pour l'agilité  
**Votre réponse est incorrecte**  
Mettre en œuvre l'élasticité  
**Bonne réponse**  
Concevoir pour l'échec  
Mettre en œuvre l'automatisation  
Question 51Ignoré  
Quel est le nombre maximal d'objets que vous pouvez stocker dans S3 par compte AWS ?  
12456  
**Bonne réponse**  
Illimité  
2444  
53678  
Question 52Ignoré  
Lequel des services AWS suivants est utilisé pour gérer et automatiser les déploiements de conteneurs ?  
Amazon Lambda  
**Bonne réponse**  
Amazon ECS  
Amazon ECR  
Question 53Ignoré  
Parmi les options de stockage AWS suivantes, laquelle est la mieux adaptée à la sauvegarde de données rarement consultées et dont la priorité de récupération est faible ?  
**Bonne réponse**  
Amazon Glacier  
Système de fichiers élastique Amazon (EFS)  
Amazon Elastic Block Store (EBS)  
Amazon Simple Storage Service (S3)  
Question 54Ignoré  
Lequel des services AWS suivants est utilisé pour répartir le trafic entrant sur plusieurs instances EC2 ?  
**Bonne réponse**  
équilibreur de charge  
Mise à l'échelle automatique  
Distribution du front de nuage  
Question 55Ignoré  
Quelles méthodes de sécurité Amazon S3 utilise-t-il pour protéger ses compartiments ?  
Groupe de sécurité  
Clés d'accès  
**Bonne réponse**  
Politique d'accès aux seaux   
Question 56Ignoré  
Dans le cadre de la gestion des identités et des accès (IAM), un client a créé un groupe d'administrateurs composé de 5 utilisateurs. Quelle action le client doit-il entreprendre pour s'assurer que chaque utilisateur du groupe dispose des privilèges d'administrateur nécessaires ?  
Rôle IAM  
Politiques de contrôle des services  
**Bonne réponse**  
Politique IAM  
Question 57Ignoré  
Quelles sont les obligations du client lorsqu'il utilise un service géré AWS dans le cadre du modèle de responsabilité partagée d'AWS ?  
Sécurité physique des centres de données  
**Bonne réponse**  
Données client  
Chiffrement côté serveur  
correctifs du système d'exploitation  
Question 58Correct  
Quelles sont les responsabilités du client lors de l'utilisation d'Amazon RDS ?  
Gestion des sauvegardes automatiques de la base de données  
Mise à jour et maintenance du système d'exploitation sous-jacent  
Remplacement des instances défaillantes en cas de panne matérielle.  
**Votre réponse est correcte**  
Contrôle de l'accès au réseau via des groupes de sécurité  
Question 59Ignoré  
Quelle est la proposition de valeur du cloud AWS ?  
AWS est responsable de la sécurité dans le cloud AWS.  
Mise en service de nouveaux serveurs en quelques jours  
**Bonne réponse**  
Pas de contrat à long terme  
Question 60Ignoré  
Parmi les propositions suivantes, laquelle constitue un concept de conception essentiel pour l'architecture des applications cloud ?  
Capacité de réserve pour la charge de pointe  
Utilisez le processus de développement Scrum  
**Bonne réponse**  
Mettre en œuvre l'élasticité  
Utilisez l'instance la plus grande possible  
Question 61Incorrect  
Quel composant de l'infrastructure mondiale d'AWS est constitué d'un ou plusieurs centres de données distincts ?  
Emplacements périphériques  
Avant-poste d'Aws  
**Bonne réponse**  
Zone de disponibilité  
**Votre réponse est incorrecte**  
Région  
Question 62Ignoré  
Quel service AWS est un système de stockage sans serveur basé sur les objets et peut stocker une quantité illimitée de données ?  
Amazon ECS

#### Explications

Amazon ECS (Elastic Container Service) est un service d'orchestration de conteneurs permettant d'exécuter, d'arrêter et de gérer des conteneurs Docker sur un cluster. Contrairement à Amazon S3, il ne s'agit pas d'un système de stockage sans serveur et sa capacité de stockage est limitée. ECS est conçu pour la gestion d'applications conteneurisées et n'offre pas les mêmes fonctionnalités de stockage qu'Amazon S3.  
Amazon EC2

#### Explications

Amazon EC2 (Elastic Compute Cloud) est un service web qui fournit une capacité de calcul modulable dans le cloud. Contrairement à Amazon S3, il ne s'agit pas d'un système de stockage sans serveur ; il est principalement utilisé pour exécuter des serveurs virtuels (instances) dans le cloud. Bien que les instances EC2 puissent servir au stockage de données, elles ne sont pas conçues comme un système de stockage objet permettant de stocker des volumes illimités de données.  
**Bonne réponse**  
Amazon S3 \- Service de stockage simple

#### Explications

Amazon S3 (Simple Storage Service) est un système de stockage objet sans serveur fourni par AWS. Il permet aux utilisateurs de stocker et de récupérer n'importe quelle quantité de données à tout moment, ce qui en fait une solution idéale pour stocker des volumes de données illimités. Hautement évolutif, robuste et sécurisé, S3 est un choix populaire pour répondre à divers besoins de stockage dans le cloud.  
Question 63Correct  
Quel est le nom du service de base de données gérée d'Amazon Web Services (AWS) qui fonctionne avec MySQL ?  
MariaDB  
**Votre réponse est correcte**  
Aurore  
PostgreSQL  
Question 64Correct  
Quel service de stockage AWS fournit des volumes de stockage au niveau bloc pour une utilisation avec les instances Amazon EC2 et convient aux charges de travail transactionnelles ?  
**Votre réponse est correcte**  
Elastic Block Store (EBS)  
Amazon Glacier  
Aurora DB  
Système de fichiers élastique (EFS)  
Question 65Ignoré  
Quelles sont les utilisations potentielles des emplacements périphériques AWS ?  
Envoi de messages de notification aux utilisateurs finaux  
Exécution de services de mise en cache de bases de données NoSQL  
**Bonne réponse**  
Diffuser le contenu au plus près des utilisateurs  
Question 66Ignoré  
Lequel des services AWS suivants est utilisé pour fournir un système de messagerie aux applications ?  
Amazon S3  
**Bonne réponse**  
Amazon SQS  
Amazon SNS  
Question 67Correct  
Dans laquelle des catégories générales de services AWS VPC est-il inclus ?  
Base de données  
**Votre réponse est correcte**  
Réseau  
Stockage  
Calculer  
Question 68Ignoré  
Selon le modèle de responsabilité partagée d'AWS, lequel des éléments suivants est le

Obligation du client ?  
Mise à jour de l'infrastructure réseau  
Correction de l'infrastructure sous-jacente  
**Bonne réponse**  
Application de correctifs aux instances Amazon EC2  
sécurité physique  
Question 69Incorrect  
Quels services et/ou fonctionnalités AWS améliorent la disponibilité et atténuent l'impact des pannes lors de la construction d'une application web trois-tiers classique ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
AWS Auto Scaling pour les instances Amazon EC2  
Listes de contrôle d'accès (ACL) de sous-réseau Amazon VPC pour vérifier l'état d'un service  
**Votre sélection est incorrecte**  
Ressources distribuées sur plusieurs points de présence AWS  
**Votre sélection est correcte**  
Ressources distribuées sur plusieurs zones de disponibilité  
Question 70Ignoré  
Quels sont les services de plateforme sans serveur proposés par AWS ?  
Amazon EC2, Amazon S3, Amazon Athena  
Amazon Athéna, Amazon Cognito, Amazon EC2  
**Bonne réponse**  
Amazon DynamoDB, Amazon SNS, AWS Step Functions,  
Question 71Correct  
Quel est le nombre maximal de VPC pouvant être créés par défaut par région AWS ?  
10  
**Votre réponse est correcte**  
5  
1  
20  
Explication générale  
Par défaut, chaque compte AWS peut créer jusqu'à 5 VPC par région AWS. Si vous avez besoin de davantage de VPC, vous pouvez contacter le support AWS pour augmenter cette limite.  
Question 72Correct  
Quel modèle d'hébergement informatique doit être pris en compte dans le coût total de possession (TCO) lors d'une analyse de coûts permettant l'isolation physique de la charge de travail d'un client ?  
Instances à la demande

#### Explications

Les instances à la demande sont facturées à l'heure ou à la seconde, sans engagement à long terme. Bien qu'elles puissent contribuer au coût total de possession (TCO) d'un déploiement cloud, elles n'offrent pas l'isolation physique de la charge de travail du client, contrairement aux serveurs dédiés.  
**Votre réponse est correcte**  
Hôtes dévoués

#### Explications

Il convient de prendre en compte les serveurs dédiés dans le calcul du coût total de possession (CTP) lorsqu'on envisage un modèle d'hébergement permettant l'isolation physique de la charge de travail d'un client. Les serveurs dédiés fournissent des serveurs physiques exclusivement réservés à un seul client, offrant ainsi un contrôle et une sécurité accrus. Ce modèle d'hébergement engendre généralement des coûts plus élevés en raison de l'utilisation exclusive des ressources matérielles.  
Aucune instance réservée à l'avance

#### Explications

Les instances réservées sans paiement initial sont une option de paiement qui ne requiert aucun acompte. Bien qu'elles puissent réduire le coût total de possession (TCO) en offrant des économies par rapport aux instances à la demande, elles ne répondent pas à l'exigence d'isolation physique de la charge de travail du client, un point essentiel dans ce contexte.  
Instances réservées

#### Explications

Les instances réservées ne sont pas directement liées à l'isolation physique de la charge de travail d'un client. Il s'agit d'une option d'achat pour les instances Amazon EC2 offrant des remises importantes en échange d'un engagement sur une configuration d'instance spécifique pendant une période donnée. Bien qu'elles puissent avoir un impact sur le coût total de possession (TCO), elles ne répondent pas spécifiquement à l'exigence d'isolation physique.  
Explication générale  
Le modèle d'hébergement informatique qui doit être pris en compte dans le coût total de possession (TCO) lors de la réalisation d'une analyse des coûts permettant l'isolation physique d'une charge de travail client est A. Hôtes dédiés.  
Question 73Correct  
Quels attributs d'un compte AWS AWS Trusted Advisor peut-il surveiller et sur lesquels il peut fournir des conseils ? (Sélectionnez 2\)  
**Votre sélection est correcte**  
Respect des meilleures pratiques de sécurité  
**Votre sélection est correcte**  
optimisation des coûts  
Performances de l'application  
Utilisation du réseau  
Question 74Ignoré  
Parmi les services AWS suivants, lequel un client doit-il utiliser pour auditer la gestion des changements des ressources AWS ?  
**Bonne réponse**  
Configuration AWS  
Conseiller de confiance AWS  
Amazon CloudWatch  
Inspecteur Amazon  
Question 75Ignoré  
Parmi les tâches suivantes, lesquelles peuvent être utilisées pour améliorer les coûts d'Amazon EC2 ? (Sélectionnez deux réponses.)  
Création d'une stratégie pour empêcher les utilisateurs IAM de créer de nouvelles instances  
Ajout d'instances EC2 à une deuxième région AWS géographiquement proche des utilisateurs finaux.  
**Sélection correcte**  
Mise en place de groupes de mise à l'échelle automatique pour ajouter et supprimer des instances en fonction de la demande  
**Sélection correcte**  
Achat d'instances réservées  
Question 76Ignoré  
Parmi les propositions suivantes, laquelle ne constitue pas une obligation du client dans le cadre du modèle de responsabilité partagée d'AWS ? (Sélectionnez 2 réponses)  
configuration des groupes de sécurité et des listes de contrôle d'accès (ACL)  
**Sélection correcte**  
Contrôler l'accès physique aux centres de données  
**Sélection correcte**  
Mise hors service des dispositifs de stockage physique  
Question 77Correct  
Quel pilier du cadre AWS Well-Architected est conçu sur l'idée de modifications fréquentes, mineures et réversibles ?  
efficacité de performance  
optimisation des coûts  
Fiabilité  
**Votre réponse est correcte**  
Excellence opérationnelle  
Explication générale  
Le pilier « Excellence opérationnelle » du cadre AWS Well-Architected est conçu sur l'idée de modifications fréquentes, mineures et réversibles, car cette approche aide les organisations à atteindre un haut niveau d'agilité et de réactivité face à l'évolution des besoins commerciaux, tout en minimisant les risques et les perturbations de leurs systèmes et opérations.  
Question 78Ignoré  
Quel concept d'architecture cloud repose sur la distribution des charges de travail sur différentes zones de disponibilité ?  
Concevoir un système qui favorise l'agilité.  
**Bonne réponse**  
Concevoir pour la résilience.  
Exploitez l'élasticité.  
Mettre en œuvre l'automatisation.  
Question 79Correct  
Quel service AWS peut protéger vos applications et vos informations contre les attaques web classiques ?  
Amazon LEX  
Amazon Macie  
**Votre réponse est correcte**  
Amazon Shield  
Question 80Ignoré  
Pour installer une charge de travail conforme à la norme PCI sur AWS, laquelle des tâches suivantes est requise ?  
**Bonne réponse**  
Utilisez un service AWS conforme à la norme PCI et appliquez les contrôles PCI au niveau de la couche application.  
Utilisez un service AWS conforme à la norme PCI et ouvrez un ticket de support AWS pour activer la conformité PCI au niveau de l'application.  
Utilisez n'importe quel service AWS et mettez en œuvre des contrôles PCI au niveau de la couche application.  
Question 81Incorrect  
Quelle solution permet aux utilisateurs de suivre l'évolution de la configuration logicielle sur leurs serveurs locaux au fil du temps ?  
**Bonne réponse**  
Configuration AWS  
**Votre réponse est incorrecte**  
Service de garde AWS  
Inspecteur AWS  
Question 82Correct  
Quel service AWS propose des bases de données relationnelles gérées ?  
Amazon MariaDB  
**Votre réponse est correcte**  
Amazon RDS  
Amazon DynamoDB  
Question 83Ignoré  
Quels services relèvent de la catégorie migration ?  
**Bonne réponse**  
Service de découverte d'applications AWS  
Configuration AWS  
AWS OpsWorks  
Question 84Ignoré  
Après avoir analysé le rapport « Coûts et utilisation » d'AWS dans la console de gestion AWS, un expert cloud détecte un problème de facturation. Quelle action doit-il entreprendre pour le résoudre ?  
Contactez le gestionnaire de compte AWS  
**Bonne réponse**  
Veuillez soumettre un dossier de facturation détaillé et l'envoyer au support AWS pour obtenir de l'aide.  
Procédez à la création d'un nouveau tableau de bord dans Amazon QuickSight.  
Utilisez CloudTrail pour identifier le problème.  
Question 85Ignoré  
Parmi ces migrations de bases de données, lesquelles peuvent être classées comme migrations hétérogènes ?  
Oracle vers Amazon RDS pour Oracle  
MySQL vers Amazon Aurora MySQL  
**Bonne réponse**  
Oracle vers Amazon Aurora PostgreSQL  
Explication générale  
La migration de bases de données hétérogènes désigne le processus de migration de données d'un type de base de données vers un autre. Dans ce cas précis, la migration implique le transfert de données d'Oracle ou de Microsoft SQL Server, qui sont des bases de données propriétaires, vers Amazon Aurora PostgreSQL, qui est une base de données différente, dotée d'une structure et de fonctionnalités différentes.  
Question 86Ignoré  
Dans le cadre de la configuration, vous devez vous assurer de disposer d'un service permettant de surveiller et d'analyser vos ressources et applications AWS. Quel service AWS choisiriez-vous à cet effet ?  
**Bonne réponse**  
Amazon CloudWatch  
Essai gratuit d'Amazon Cloud  
Amazon Cloud Inspect  
Question 87Ignoré  
Lequel des moteurs suivants est classé comme base de données relationnelle ?  
DynamoDB  
**Bonne réponse**  
Aurore  
Décalage vers le rouge  
Question 88Ignoré  
Quels éléments de coût doivent être pris en compte lors de l'élaboration d'un modèle de coût total de possession (TCO) pour les charges de travail AWS ? (Sélectionnez trois réponses.)  
**Sélection correcte**  
coûts d'infrastructure réseau  
**Sélection correcte**  
Calculer les coûts  
**Sélection correcte**  
Frais de stockage  
coûts des installations  
Question 89Ignoré  
Quel service AWS permet d'utiliser le cloud AWS pour héberger une base de données NoSQL ?  
**Bonne réponse**  
Amazon DynamoDB  
Amazon RDS  
Amazon Aurora  
Question 90Ignoré  
Quelle est l'obligation du client dans le cadre du modèle de responsabilité partagée d'AWS ?  
Correction et résolution des défauts de l'infrastructure  
Contrôles physiques et environnementaux  
**Bonne réponse**  
Mise à jour du système d'exploitation invité et des applications  
Question 91Incorrect  
Lesquels des éléments suivants sont inclus dans les vérifications d'AWS Trusted Advisor ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
L'authentification multifacteurs est activée pour l'utilisateur racine du compte AWS.  
**Votre sélection est correcte**  
Informations sur les autorisations des compartiments Amazon S3  
**Votre sélection est incorrecte**  
Pannes de service AWS  
Nombre d'utilisateurs du compte  
Question 92Ignoré  
Quels services AWS sont utilisés pour distribuer du contenu aux utilisateurs du monde entier ?  
Formation des nuages  
Nuage 9  
**Bonne réponse**  
Front de nuage  
Question 93Correct  
Quel service AWS est utilisé pour le stockage de fichiers dans le cloud ?  
**Votre réponse est correcte**  
S3  
stockage par blocs  
EC2  
Explication générale  
Amazon S3 (Simple Storage Service) est le service AWS utilisé pour le stockage de fichiers dans le cloud. Ce service de stockage d'objets offre une évolutivité, une disponibilité des données, une sécurité et des performances de pointe. Avec Amazon S3, les utilisateurs peuvent stocker et récupérer n'importe quelle quantité de données depuis n'importe où sur le web, ce qui en fait un choix populaire pour de nombreux cas d'utilisation, tels que la sauvegarde et la restauration, le stockage et la diffusion de contenu, l'archivage et l'analyse de données massives. Amazon S3 propose également différentes classes de stockage permettant aux utilisateurs de choisir l'option la plus économique pour leurs besoins, comme Standard, Intelligent-Tiering, Glacier, etc.  
Question 94Correct  
Lequel des éléments suivants illustre la sécurité dans le cloud AWS sous AWS ?

modèle de responsabilité partagée ?  
**Votre réponse est correcte**  
Configuration du pare-feu  
Gestion des emplacements périphériques  
sécurité physique  
Infrastructure mondiale  
Question 95Ignoré  
Laquelle des suggestions suivantes provient d'un conseiller de confiance AWS ?  
**Sélection correcte**  
optimisation des coûts   
**Sélection correcte**  
Performance  
Audit  
Évolutivité  
Question 96Incorrect  
Quel est l'avantage unique dont bénéficient les clients du support aux entreprises ?  
Accès à un chef de projet technique  
Accès à un ingénieur de support cloud  
**Bonne réponse**  
Accès à un gestionnaire de compte technique  
**Votre réponse est incorrecte**  
Accès à un architecte de solutions  
Question 97Correct  
Quelle fonctionnalité permet aux instances Amazon EC2 d'être plus élastiques pour répondre à l'évolution de la demande de charge de travail ?  
**Votre réponse est correcte**  
Gestion de la virtualisation  
Gestion du matériel  
Gestion des installations  
Gestion du chiffrement  
Question 98Ignoré  
Quel service AWS permet d'identifier la personne ayant effectué la requête API lorsqu'une instance Amazon EC2 est arrêtée ?  
Gestion des identités et des accès AWS (IAM)  
AWS X-Ray  
**Bonne réponse**  
AWS Cloud Trail  
Amazon CloudWatch  
Question 99Ignoré  
Quelles sont les fonctionnalités des outils de gestion des coûts AWS ? (Sélectionnez deux réponses.)  
Mettre fin automatiquement à toutes les ressources AWS si les seuils budgétaires sont dépassés.  
**Sélection correcte**  
Créez des budgets et recevez des notifications si l'utilisation actuelle ou prévue dépasse les budgets.  
Basculez automatiquement vers les instances réservées ou les instances Spot, selon la solution la plus rentable.  
**Sélection correcte**  
Détaillez les coûts AWS par jour, service et compte AWS associé.  
Question 100Correct  
Qui est le principal interlocuteur pour les questions de facturation ou de compte si un utilisateur possède un compte AWS ?

avec un plan de support AWS de niveau entreprise ?  
Partenaire du réseau de partenaires AWS (APN)  
Vendeur sur AWS Marketplace  
Architecte de solutions  
**Votre réponse est correcte**  
Équipe de support AWS Concierge

