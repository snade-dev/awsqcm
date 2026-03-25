Question 1Ignoré  
Si une personne connaissant AWS constate une erreur dans le montant qui lui est facturé, que doit-elle faire pour la corriger ?  
**Bonne réponse**  
Ouvrez un ticket détaillé concernant la facturation et soumettez-le au support AWS pour obtenir de l'aide.  
Procédez à la création d'un nouveau tableau de bord dans Amazon QuickSight.  
Téléversez les données décrivant le problème dans un nouvel objet situé dans un compartiment Amazon S3 privé.  
Question 2Ignoré  
Pour augmenter la disponibilité, un utilisateur souhaite créer deux instances Amazon EC2 supplémentaires. Que doit-il faire ?  
Lancez les instances dans plusieurs régions AWS, mais dans la même zone de disponibilité.  
**Bonne réponse**  
Déployez les instances sur plusieurs zones de disponibilité dans une seule région AWS.  
Lancez des instances EC2 en tant qu'instances Spot dans différentes zones de disponibilité au sein de la même région AWS.  
Question 3Ignoré  
Laquelle des propositions suivantes relève des obligations d'AWS dans le cadre du modèle de responsabilité partagée d'AWS ?  
Gestion des politiques de sécurité AWS IAM  
**Bonne réponse**  
Application des mises à jour à l'hyperviseur  
Activation du chiffrement côté serveur pour les objets stockés dans S3  
Question 4Ignoré  
Comment garantir le fonctionnement ininterrompu des bases de données sans intervention humaine après une seule interruption de service dans une zone de disponibilité ?  
**Bonne réponse**  
Configurez les déploiements Amazon RDS à zones de disponibilité multiples avec basculement automatique vers la zone de secours.  
Ajoutez plusieurs équilibreurs de charge d'application et déployez l'instance de base de données avec AWS Elastic Beanstalk.  
Utilisez plusieurs routes Amazon Route 53 vers le point de terminaison de l'instance de base de données de secours hébergée sur AWS Storage Gateway.  
Question 5Ignoré  
Dans quelles situations utiliserait-on la mise à l'échelle automatique ?  
**Bonne réponse**  
Lorsque la charge de travail ne présente pas de schémas cohérents  
Lorsque la charge de travail présente des schémas réguliers.  
Lors de la mise à disposition de la capacité des compartiments S3  
Question 6Ignoré  
Dans le cadre du modèle de responsabilité partagée, quels sont les domaines qui relèvent de la responsabilité du client ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Correction des systèmes d'exploitation  
Sécurité physique des centres de données  
**Sélection correcte**  
Configuration du groupe de sécurité  
Mises à niveau du micrologiciel de l'infrastructure réseau  
Question 7Ignoré  
Quels services ou fonctionnalités AWS permettent le basculement entre plusieurs régions AWS afin de garantir une haute disponibilité et une faible latence ?  
Équilibreur de charge réseau  
Équilibreur de charge d'application  
**Bonne réponse**  
Route 53 d'Amazonie  
Question 8Ignoré  
Parmi les éléments suivants, lesquels relèvent des obligations du client dans le cadre de la responsabilité partagée d'AWS ?

modèle ? (Sélectionnez deux réponses.)  
Calculer la disponibilité de la capacité  
**Sélection correcte**  
Configurations réseau et pare-feu  
**Sélection correcte**  
Configuration du chiffrement côté serveur sur un compartiment Amazon S3  
Mise à jour des instances Amazon RDS  
Question 9Ignoré  
Un client possède plusieurs utilisateurs IAM qui nécessitent les mêmes autorisations d'accès. Comment peut-il leur accorder ces mêmes autorisations rapidement et efficacement ?  
attribuer une stratégie AWS préconfigurée à chaque utilisateur  
**Bonne réponse**  
Attribuer les utilisateurs à un groupe IAM disposant des autorisations nécessaires.  
créer une politique et l'attribuer à chaque utilisateur  
Question 10Ignoré  
Dans quelles deux situations un utilisateur doit-il signaler un problème à l'équipe AWS Abuse ?  
**Sélection correcte**  
En cas d'attaque DDoS  
**Sélection correcte**  
Du contenu illégal ou inapproprié est hébergé à l'aide des ressources AWS.  
Les ressources de l'entreprise sont utilisées d'une manière non conforme à la politique de l'entreprise.  
Une attaque par injection SQL est menée à partir d'une adresse IP.  
Question 11Ignoré  
Quelles sont les utilisations possibles des emplacements périphériques AWS ?  
Applications d'hébergement  
**Bonne réponse**  
Diffuser le contenu au plus près des utilisateurs  
Exécution de services de mise en cache de bases de données NoSQL  
Question 12Ignoré  
Quels éléments peuvent être associés à une instance Amazon EC2 via AWS Identity and Access Management (IAM) pour initier des demandes de service ?  
Politique  
Groupe  
**Bonne réponse**  
Rôle  
Question 13Ignoré  
Quel service AWS peut être utilisé pour découvrir, classer et sécuriser les données sensibles dans S3 ?  
Reconnaissance  
LEX  
**Bonne réponse**  
Tu as  
Polly  
Question 14Ignoré  
Quelle est la responsabilité du client dans le cadre du modèle de responsabilité partagée d'AWS ?  
Application de correctifs aux composants du système d'exploitation pour Amazon Relational Database Server (Amazon RDS)  
**Bonne réponse**  
Configuration des listes de contrôle d'accès réseau (ACL)  
Effacement des disques durs utilisés  
Gestion de la sécurité des centres de données  
Question 15Ignoré  
Selon le modèle de responsabilité partagée d'AWS, laquelle des propositions suivantes relève exclusivement de la responsabilité d'AWS ?  
Application de correctifs au système d'exploitation invité  
Sensibilisation et formation à la sécurité  
**Bonne réponse**  
Contrôles physiques et environnementaux  
Question 16Ignoré  
Selon le modèle de responsabilité partagée d'AWS, lesquelles des propositions suivantes constituent des obligations pour AWS ?  
Application de correctifs au système d'exploitation invité  
Sécurité des données de l'application  
Politiques IAM  
**Bonne réponse**  
sécurité physique du matériel  
Question 17Ignoré  
Qu'est-ce qu'un service d'entrepôt de données entièrement géré à l'échelle du pétaoctet proposé par AWS ?  
Amazon EFS  
**Bonne réponse**  
Amazon Redshift  
Amazon S3  
Question 18Ignoré  
Quel service ou fonctionnalité AWS est utilisé par les applications distribuées pour envoyer des SMS et des e-mails ?  
Amazon Simple Email Service (Amazon SES)  
Amazon Simple Queue Service (Amazon SQS)  
**Bonne réponse**  
Service de notification simple d'Amazon (Amazon SNS)  
alertes Amazon CloudWatch  
Question 19Ignoré  
Comment les clients peuvent-ils minimiser le temps consacré à la mise à jour de leurs systèmes d'exploitation en migrant vers le cloud AWS ?  
**Bonne réponse**  
Les utilisateurs peuvent tirer parti des services gérés sur AWS  
Les utilisateurs ont la possibilité d'utiliser des instances Amazon EC2 incluses dans la licence.  
Les utilisateurs peuvent externaliser la mise à jour des systèmes d'exploitation auprès de l'équipe de support AWS.  
Question 20Ignoré  
Parmi les options suivantes, lesquelles constituent des options de tarification EC2 valides ? (Choisissez 2\)  
Sclable  
Entreprise  
**Sélection correcte**  
Réservé  
**Sélection correcte**  
Sur demande  
Question 21Ignoré  
Quels coûts doivent être pris en compte lors de la comparaison du coût total de possession (TCO) entre AWS Cloud et une infrastructure sur site ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Infrastructure réseau du centre de données  
développement de schémas de base de données  
administration du système d'exploitation  
**Sélection correcte**  
matériel de stockage physique  
Question 22Ignoré  
Un administrateur doit installer et utiliser rapidement un produit informatique courant. Quelles ressources sont mises à sa disposition ?  
Documentation du framework AWS Well-Architected  
**Bonne réponse**  
Déploiements de référence pour le démarrage rapide d'AWS  
Amazon CloudFront  
Question 23Ignoré  
Une entreprise souhaite prévoir ses dépenses et sa consommation futures. Quel outil peut-elle utiliser ?  
**Bonne réponse**  
Explorateur de coûts AWS  
Organisations AWS  
Budget AWS  
Question 24Ignoré  
Quelles actions de gestion des changements, conformément au cadre AWS Well-Architected, doivent être mises en œuvre pour garantir la fiabilité du cloud AWS ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Utilisez AWS Config pour générer un inventaire des ressources AWS.  
Amazon GuardDuty pour valider les modifications de configuration  
**Sélection correcte**  
Utilisez AWS CloudTrail pour enregistrer les appels d'API AWS dans un fichier journal auditable.  
Question 25Ignoré  
Parmi les types d'instances suivants, lequel offre le coût horaire le plus bas ?  
t3.tlarge  
**Bonne réponse**  
t3.micro  
t3.2xlarge  
Question 26Ignoré  
Quels sont les avantages du cloud AWS ?  
accès physique aux centres de données cloud  
coût mensuel fixe  
**Bonne réponse**  
Accélération de la mise sur le marché  
Question 27Ignoré  
Dans le cadre du modèle de responsabilité partagée, quelles sont les tâches qui incombent au client ? (Sélectionnez deux réponses.)  
Remplacement des disques durs défectueux.  
Maintenance du matériel Amazon EC2 sous-jacent.  
**Sélection correcte**  
Gestion des listes de contrôle d'accès au réseau VPC  
**Sélection correcte**  
Chiffrement des données en transit et au repos  
Question 28Ignoré  
Avant de transférer un environnement vers le cloud AWS, un professionnel du cloud doit recevoir les rapports de conformité AWS.

Comment ces rapports sont-ils produits ?  
Contactez l'équipe de conformité AWS  
Ouvrez un ticket auprès du support AWS.  
Générez les rapports avec Amazon Macie  
**Bonne réponse**  
Téléchargez les rapports depuis AWS Artifact  
Question 29Ignoré  
Une entreprise anticipe une augmentation ponctuelle du trafic internet pour son application. Le programme ne doit pas être interrompu pendant ce pic de trafic. De plus, l'entreprise doit réduire ses coûts tout en gagnant en flexibilité. Pour répondre à ces besoins, quel type d'instance Amazon EC2 doit-elle utiliser ?  
Hôtes dévoués  
Instances ponctuelles  
**Bonne réponse**  
Instances à la demande  
Instances réservées  
Question 30Ignoré  
Quelle est la proposition de valeur d'AWS Cloud ?  
Mise en service de nouveaux serveurs en quelques jours  
**Bonne réponse**  
Vous n'avez pas besoin d'un contrat à long terme.  
AWS est responsable de la sécurité dans le cloud AWS.  
Question 31Ignoré  
Selon le modèle de responsabilité partagée d'AWS, quelle tâche incombe au client ?  
Mettre à jour le système d'exploitation des instances Amazon RDS.  
Mettre en œuvre des contrôles physiques et environnementaux.  
**Bonne réponse**  
Configurer les pare-feu et les réseaux  
Maintenir la sécurité du cloud AWS.  
Question 32Ignoré  
Quelles sont les utilisations possibles des emplacements périphériques AWS ?  
**Bonne réponse**  
Diffuser le contenu au plus près des utilisateurs  
Envoi de messages de notification aux utilisateurs finaux  
Applications d'hébergement  
Réduction du trafic sur le serveur par la mise en cache des réponses  
Question 33Ignoré  
Laquelle de ces affirmations concernant les régions AWS est correcte ?  
**Bonne réponse**  
En général, les régions désignent des zones géographiques spécifiques.  
Les régions sont des ensembles d'emplacements Edge  
Les régions sont des constructions définies par l'utilisateur.  
Question 34Ignoré  
Lequel des services AWS suivants vous permet de déployer votre code sans avoir à vous soucier de l'infrastructure sous-jacente ?  
**Bonne réponse**  
AWS Lambda  
AWS Cloud 9  
AWS Fargate  
Question 35Ignoré  
Quels coûts faut-il prendre en compte lors de la comparaison entre AWS Cloud et une infrastructure sur site ? Total

Coût de possession ?  
Gestion de projet  
**Bonne réponse**  
Matériel de stockage  
Développement logiciel  
Question 36Ignoré  
Laquelle des propositions suivantes est une caractéristique des instances Amazon EC2 ?  
Ils sont conçus pour fonctionner uniquement sous Windows.  
Ils proposent des tarifs mensuels fixes  
Ils ont besoin d'un accès physique pour la gestion  
**Bonne réponse**  
Ils sont évolutifs à la demande  
Question 37Ignoré  
Si votre entreprise souhaite transférer la gestion de son DNS vers le cloud, quel service AWS devriez-vous utiliser ?  
AWS CloudFront  
CloudFormation  
**Bonne réponse**  
Route 53  
Question 38Ignoré  
Quelles tâches nécessitent les identifiants de l'utilisateur racine d'un compte AWS ? (Sélectionnez deux réponses.)  
Suppression d'un utilisateur IAM du groupe des administrateurs  
Création d'une paire de clés Amazon EC2  
**Sélection correcte**  
Accorder à un utilisateur IAM un accès administrateur complet  
**Sélection correcte**  
Modification du plan de support AWS  
Question 39Ignoré  
Quelles sont les obligations du client dans le cadre du modèle de responsabilité partagée d'AWS ? (Sélectionnez deux réponses.)  
**Sélection correcte**  
Configurations réseau et pare-feu  
**Sélection correcte**  
Configuration du chiffrement côté serveur  
Mise à jour des instances Amazon RDS  
Sécurité physique des infrastructures  
Question 40Ignoré  
Que peuvent faire les utilisateurs avec AWS Marketplace ?  
Commander AWS Snowball.  
Vendre les instances Spot Amazon EC2 inutilisées.  
**Bonne réponse**  
Vendre des solutions à d'autres utilisateurs AWS  
Question 41Ignoré  
Quel service AWS peut vous aider à identifier les failles de sécurité de vos instances EC2 ?  
AWS KMS  
AWS WAF  
**Bonne réponse**  
Inspecteur AWS  
Question 42Ignoré  
Quelle fonctionnalité d'EC2 permet aux utilisateurs de stocker des données sur un disque dur virtuel attaché à leur instance ?  
Groupes de sécurité  
**Bonne réponse**  
Elastic Block Store (EBS)  
IP élastique  
Image machine Amazon (AMI)  
Question 43Ignoré  
Quelle fonctionnalité AWS permet à une entreprise de s'adapter aux variations de la demande pour une application web critique utilisant Amazon Elastic Container Service et Amazon DynamoDB ?  
Agilité  
**Bonne réponse**  
Évolutivité  
Sécurité  
Portée mondiale  
Question 44Ignoré  
Lequel des services AWS suivants peut vous aider à surveiller et à gérer votre sécurité et votre conformité sur plusieurs comptes AWS ?  
Gestionnaire de certificats AWS  
AWS GuardDuty  
Conseiller de confiance AWS  
**Bonne réponse**  
AWS Security Hub  
Question 45Ignoré  
Parmi les types d'instances Amazon EC2 suivants, lequel offre l'option la plus économique pour les applications non critiques ?  
instance optimisée en mémoire  
**Bonne réponse**  
instance éclatable  
instance optimisée de calcul  
instance optimisée pour le stockage  
Question 46Ignoré  
Quels services AWS sont pris en charge nativement par AWS Snowball Edge ?  
Amazon S3  
**Bonne réponse**  
Amazon EC2  
Amazon Aurora  
Service de migration de serveurs AWS (AWS SMS)  
Question 47Ignoré  
Laquelle des fonctionnalités Amazon S3 suivantes permet de déplacer automatiquement des objets entre différentes classes de stockage en fonction des modèles d'accès ?  
Verrouillage d'objet S3  
Inventaire S3  
Accélération du transfert S3  
**Bonne réponse**  
Politiques de cycle de vie S3  
Question 48Ignoré  
Dans le cadre du modèle de responsabilité partagée d'AWS, laquelle des actions suivantes relève de la responsabilité du client ?  
mettre hors service le matériel ancien  
**Bonne réponse**  
Chiffrement des données côté client  
Formation du personnel du centre de données  
Maintenance du réseau entre les zones de disponibilité  
Question 49Ignoré  
Quel service de base de données AWS offre la possibilité d'exécuter vos propres scripts et requêtes SQL ?  
Amazon S3  
**Bonne réponse**  
Amazon RDS  
Amazon Neptune  
Base de données de documents  
Question 50Ignoré  
Quelles sont les obligations du client dans le cadre du modèle de responsabilité partagée d'AWS ?  
**Bonne réponse**  
Authentification de l'intégrité des données  
Mise hors service des périphériques de stockage  
Dispositifs de réseau physiques, y compris les pare-feu  
Question 51Ignoré  
Amazon DynamoDB est utilisé par une entreprise dans son architecture cloud AWS.

Selon la charte AWS, laquelle des propositions suivantes relève des obligations de l'organisation ?

modèle de responsabilité ?  
**Bonne réponse**  
Application des autorisations appropriées avec les outils IAM  
Approvisionnement et maintenance de l'infrastructure  
Mise à jour et correctifs du système d'exploitation  
Question 52Ignoré  
Qu'est-ce qu'un rôle IAM ?  
**Bonne réponse**  
Une entité IAM qui définit un ensemble d'autorisations pour effectuer des requêtes de service AWS.  
Un service AWS permettant de créer et de gérer des comptes utilisateurs.  
Un outil pour configurer le routage réseau dans AWS.  
Question 53Ignoré  
Quel service AWS prend en charge MySQL et PostgreSQL comme bases de données relationnelles ?  
Amazon Redshift  
**Bonne réponse**  
Amazon Aurora  
Amazon Neptune  
Question 54Ignoré  
Une copie du rapport AWS SOC 2 est requise lors d'un contrôle de conformité effectué par un auditeur. Par quel service cette demande doit-elle être envoyée ?  
Amazon S3  
Tableau de bord de santé personnelle AWS  
**Bonne réponse**  
Artefact AWS  
Conseiller de confiance AWS  
Question 55Ignoré  
Quelles sont les deux choses que les clients AWS doivent faire dans le cadre du modèle de responsabilité partagée ?  
**Sélection correcte**  
Garantir que les données de l'application sont chiffrées au repos  
**Sélection correcte**  
S'assurer que les utilisateurs savent utiliser AWS en toute sécurité en leur dispensant une formation à la sécurité.  
Garantir que l'accès aux centres de données soit restreint  
Provisionner des serveurs dans les centres de données AWS  
Question 56Ignoré  
Comment les services AWS peuvent-ils contribuer à garantir la conformité aux politiques de l'entreprise pour tous les comptes de son environnement ?  
Conseiller en confiance  
**Bonne réponse**  
Tour de contrôle  
Organisation AWS  
Artefacts AWS  
Question 57Ignoré  
Quelles fonctionnalités peuvent être utilisées pour empêcher l'écrasement ou la suppression accidentelle de compartiments Amazon S3 ?  
**Bonne réponse**  
versionnage d'objets  
ACL du compartiment  
Chiffrement côté serveur  
Politique de cycle de vie  
Question 58Ignoré  
Quel service AWS propose un service de protection DDoS (déni de service distribué) entièrement géré ?  
**Bonne réponse**  
Bouclier AWS  
Gestionnaire de pare-feu AWS  
AWS Security Hub  
Question 59Ignoré  
Quelle est l'obligation d'AWS dans le cadre du modèle de responsabilité partagée d'AWS ?  
Application de correctifs au système d'exploitation sur les instances Amazon EC2  
**Bonne réponse**  
Mises à jour du firmware sur le matériel  
Cryptage des données au repos  
Cryptage des données en transit  
Question 60Ignoré  
Lequel des services AWS suivants est utilisé pour automatiser vos déploiements d'infrastructure ?  
Surveillance des nuages  
**Bonne réponse**  
Formation des nuages  
front nuageux  
Question 61Ignoré  
Quels outils AWS peuvent être utilisés pour éviter les interruptions de service et les retards en basculant vers des serveurs de secours situés dans différentes parties du monde ?  
Front de nuage  
**Bonne réponse**  
Route 53 d'Amazonie  
Accélération du transfert S3  
Équilibreur de charge d'application  
Question 62Ignoré  
Quels frais sont inclus dans la comparaison du coût total de possession (TCO) entre AWS et une infrastructure sur site ?  
Gestion de projet  
**Bonne réponse**  
Sécurité des centres de données  
administration du système d'exploitation  
Question 63Ignoré  
Sur Amazon EC2, une entreprise héberge une application web dans un conteneur Docker. De quelles tâches AWS s'occupe-t-elle ?  
Mise à l'échelle de l'application web et des services développés avec Docker  
**Bonne réponse**  
Effectuer la maintenance du matériel dans les infrastructures AWS qui hébergent le cloud AWS.  
Gestion du système d'exploitation invité, y compris les mises à jour et les correctifs de sécurité  
Question 64Ignoré  
Quels services ou fonctionnalités AWS facilitent le basculement entre plusieurs régions AWS pour garantir une faible latence et une haute disponibilité ?  
**Bonne réponse**  
Accélérateur mondial AWS  
Amazon CloudFront  
Accélération des transferts Amazon S3  
Question 65Ignoré  
Dans le cadre du modèle de responsabilité partagée d'AWS, laquelle des actions suivantes relève de la responsabilité du client ?  
Formation du personnel du centre de données  
Maintenir les contrôles environnementaux au sein d'un centre de données  
**Bonne réponse**  
Chiffrement des données côté client  
Question 66Ignoré  
Quels produits AWS anticipent automatiquement les dépenses AWS futures ?  
Calculateur du coût total de possession (TCO) AWS  
Centre de support AWS  
**Bonne réponse**  
Explorateur de coûts  
Calculateur mensuel simple AWS  
Question 67Ignoré  
Quel type d'assistance est offert à tous les utilisateurs avec le niveau de base du support AWS ?  
Assistance 24h/24 et 7j/7 par téléphone et chat  
**Bonne réponse**  
Assistance à la facturation  
Soutien architectural  
Question 68Ignoré  
Qu'est-ce qu'Amazon Rekognition et à quoi sert-il ?  
Service AWS pour le traitement et l'analyse en temps réel de grands volumes de données en flux continu.  
**Bonne réponse**  
Service AWS permettant de reconnaître et d'analyser des images et des vidéos à l'aide de technologies d'apprentissage profond.  
Service AWS d'analyse de texte et d'extraction de sens à partir du langage naturel  
Question 69Ignoré  
Qu'est-ce qu'AWS ne prend pas en charge dans le cadre du modèle de responsabilité partagée ?  
Hyperviseur  
Réseautage  
**Bonne réponse**  
Données client  
Question 70Ignoré  
Quelles sont les actions que le client doit entreprendre selon le modèle de responsabilité partagée d'AWS ?  
Mise à jour de l'infrastructure hôte  
Sécurité des infrastructures  
**Bonne réponse**  
Application de correctifs aux instances Amazon EC2  
Question 71Ignoré  
Comment décrire au mieux Amazon Polly ?  
**Bonne réponse**  
Service AWS de conversion de texte en parole naturelle  
Service AWS pour l'analyse et la visualisation des données en temps réel.  
Service AWS permettant de créer et de gérer des serveurs virtuels dans le cloud.  
Question 72Ignoré  
Laquelle des fonctionnalités de sécurité suivantes peut vous aider à protéger vos ressources AWS contre les accès non autorisés ?  
AWS Lambda  
Équilibreur de charge élastique AWS  
**Bonne réponse**  
Gestion des identités et des accès AWS (IAM)  
AWS Glue  
Question 73Ignoré  
Quelle est la taille maximale des fichiers pouvant être téléchargés sur Amazon S3 ?  
10 Go  
50 Go  
**Bonne réponse**  
5 To  
100  
Question 74Ignoré  
Lequel des services de base de données suivants est un service de base de données NoSQL géré ?  
Amazon RDS  
**Bonne réponse**  
Amazon DynamoDB  
Amazon Aurora  
S3  
Question 75Ignoré  
Parmi les propositions suivantes, lesquelles décrivent l'élasticité dans le cloud AWS ? (Sélectionnez deux réponses.)  
La quantité maximale de RAM qu'une instance Amazon EC2 peut utiliser  
Rapidité de redémarrage d'une instance Amazon EC2  
**Sélection correcte**  
La capacité d'adapter les ressources en fonction de l'évolution de la demande  
**Sélection correcte**  
Avec quelle facilité les ressources peuvent être produites lorsqu'elles sont nécessaires  
Explication générale  
Dans AWS, le processus consiste à obtenir les ressources de manière dynamique lorsque vous en avez réellement besoin.

Les utiliser, puis libérer les ressources une fois que vous avez terminé et que vous n'en avez plus besoin.  
Question 76Ignoré  
Comment appliquer le principe du moindre privilège dans l'architecture du cloud AWS ?  
Empêcher les responsables d'accéder au code source important.  
Attribuer des autorisations en fonction des intitulés de poste.  
**Bonne réponse**  
Donnez aux utilisateurs juste assez d'accès pour leur permettre d'accomplir leur travail.  
Question 77Ignoré  
Quel est l'outil AWS permettant de connecter votre cloud AWS à un centre de données sur site ?  
Passerelle privée virtuelle  
**Bonne réponse**  
Connexion directe  
Passerelle Internet  
Interconnexion VPC  
Question 78Ignoré  
Quel service AWS est le plus adapté au stockage des données de vente et à la réalisation d'analyses mensuelles avec des outils de visualisation ?  
**Bonne réponse**  
Amazon Redshift  
Amazon Lambda  
Amazon CloudWatch  
Amazon S3  
Question 79Ignoré  
Une instance de base de données Amazon RDS est déployée sur plusieurs zones de disponibilité. Quel pilier du cadre AWS Well-Architected est inclus dans cette stratégie ?  
optimisation des coûts  
Sécurité  
**Bonne réponse**  
Fiabilité  
efficacité de performance  
Question 80Ignoré  
Selon quelle directive de conception du cloud AWS les systèmes doivent-ils minimiser leur interdépendance ?  
Supprimer les points de défaillance uniques  
**Bonne réponse**  
Accouplement lâche  
Évolutivité  
Des services, pas des serveurs  
Question 81Ignoré  
Parmi les propositions suivantes, laquelle constitue une bonne pratique de sécurité lors de l'utilisation d'AWS ?  
**Bonne réponse**  
Accorder l'accès aux privilèges minimaux  
Utilisez le même mot de passe pour tous vos comptes AWS  
Partagez vos identifiants AWS avec les membres de votre équipe.  
Désactiver l'authentification multifacteurs (MFA)  
Question 82Ignoré  
Amazon EC2, un équilibreur de charge élastique et Amazon RDS sont tous des composants d'une architecture. Quelle est la meilleure méthode pour estimer le coût mensuel de cette architecture ?  
Utilisez le calculateur de coût total de possession (TCO) d'AWS pour estimer le coût mensuel.  
Demandez une estimation des coûts mensuels pour une proposition d'architecture en ouvrant un ticket de support AWS.  
**Bonne réponse**  
Estimez le coût mensuel à l'aide du calculateur mensuel simple d'AWS.  
Question 83Ignoré  
Pour garantir une haute disponibilité, combien de zones de disponibilité faut-il répartir les ressources de calcul ?  
Un minimum de trois  
Un minimum d'un  
**Bonne réponse**  
Un minimum de deux  
Question 84Ignoré  
Pendant 3 heures, 5 minutes et 6 secondes, un client utilise une instance Amazon Linux EC2 à la demande. Combien de temps le client sera-t-il facturé ?  
**Bonne réponse**  
3 heures, 5 minutes et 6 secondes  
3 heures et 6 minutes  
3 heures et 5 minutes  
Question 85Ignoré  
Quelles sont les deux options qui décrivent les caractéristiques des listes de contrôle d'accès réseau (ACL) dans le cloud AWS ?  
Ils opèrent au niveau de l'instance.  
**Sélection correcte**  
Ils traitent les règles dans l'ordre, en commençant par celles dont le numéro est le plus bas.  
**Sélection correcte**  
Ils sont apatrides.  
Ils sont étatiques.  
Question 86Ignoré  
AWS peut proposer des prix plus avantageux en mutualisant l'utilisation des ressources de nombreux utilisateurs. C'est un des atouts du cloud AWS.  
Lancement mondial en quelques minutes  
**Bonne réponse**  
économies d'échelle  
Augmenter la vitesse et l'agilité  
Question 87Ignoré  
Quel service AWS propose un service de protection contre les attaques par déni de service distribué (DDoS) évolutif et entièrement géré ?  
**Bonne réponse**  
Bouclier AWS  
AWS CloudTrail  
AWS CloudHSM  
Amazon GuardDuty  
Question 88Ignoré  
Que doit faire le client dans le modèle de responsabilité partagée ?  
**Bonne réponse**  
Données chiffrées au repos  
Veillez à effacer toutes les données des disques durs lorsqu'elles ne sont plus nécessaires.  
Mise à jour du firmware sur les périphériques matériels  
Question 89Ignoré  
Quels éléments peuvent être associés à une instance Amazon EC2 via AWS Identity and Access Management (IAM) pour initier des demandes de service ?  
**Bonne réponse**  
Rôle  
Politique  
Clé d'accès  
Groupe  
Question 90Ignoré  
Les développeurs ont créé une nouvelle application qui doit répartir le trafic HTTP et HTTPS. Quel est le meilleur équilibreur de charge à utiliser ?  
Équilibreur de charge classique  
**Bonne réponse**  
Équilibreur de charge d'application  
Équilibreur de charge de passerelle  
Équilibreur de charge réseau  
Question 91Ignoré  
Laquelle des pratiques suivantes ne constitue PAS une bonne pratique de sécurité sur AWS ?  
Utiliser le chiffrement pour protéger les données sensibles  
Rotation régulière des clés d'accès et des clés secrètes  
Accorder l'accès au moindre privilège  
**Bonne réponse**  
Désactivation de l'authentification multifacteurs (MFA)  
Question 92Ignoré  
Selon le modèle de responsabilité partagée d'AWS, lesquelles des propositions suivantes relèvent des obligations d'AWS ?  
MFA  
Configurer les équilibreurs de charge  
**Bonne réponse**  
Infrastructure réseau et virtualisation de l'infrastructure  
Configuration du VPC  
Question 93Ignoré  
Quels contrôles de responsabilité partagée AWS sont partagés ? (Sélectionnez deux réponses.)  
Contrôles physiques et environnementaux  
**Sélection correcte**  
Gestion de la configuration  
Mise à jour d'Amazon RDS  
**Sélection correcte**  
Sensibilisation et formation  
Question 94Ignoré  
En cas de perturbation environnementale, une entreprise doit s'assurer que son infrastructure est conçue pour la tolérance aux pannes et la continuité de ses activités. Quelles parties de l'architecture AWS l'organisation doit-elle répliquer ?  
Emplacements périphériques  
**Bonne réponse**  
Régions  
Zones de disponibilité  
Question 95Ignoré  
Quelle solution permet aux utilisateurs de différentes régions AWS de bénéficier des temps de réponse les plus rapides pour les données fréquemment demandées ?  
Une passerelle privée virtuelle via AWS Direct Connect  
AWS CloudTrail sur plusieurs zones de disponibilité  
**Bonne réponse**  
Amazon CloudFront vers les emplacements périphériques  
Question 96Ignoré  
Quelles sont les qualités qui rendent le cloud computing AWS avantageux ?  
Disponibilité du support AWS pour le développement de code  
Un accord de niveau de service (SLA) à 100 % pour tous les services AWS  
**Bonne réponse**  
Capacité de calcul ajustée à la demande  
Question 97Ignoré  
Quels sont les services sans serveur proposés par AWS ?  
Amazon Kinesis, Amazon SQS, Amazon EMR  
Amazon EC2, Amazon S3, Amazon Athena  
**Bonne réponse**  
Amazon DynamoDB, Amazon SNS, AWS Step Functions  
Amazon Athéna, Amazon Cognito, Amazon EC2  
Question 98Ignoré  
Parmi les tâches suivantes, laquelle incombe au client AWS dans le cadre du contrat partagé ?

Modèle de responsabilité ? (Sélectionnez deux réponses.)  
S'assurer que les serveurs NTP d'AWS sont configurés sur l'heure correcte  
S'assurer que le matériel est éliminé correctement  
**Sélection correcte**  
Garantir que les données de l'application sont chiffrées au repos  
**Sélection correcte**  
S'assurer que les utilisateurs ont reçu une formation à la sécurité concernant l'utilisation des services AWS  
Question 99Ignoré  
Pour migrer un environnement vers le cloud AWS, il est nécessaire d'obtenir des rapports d'AWS afin de garantir la conformité. Comment obtenir ces rapports ?  
Générez les rapports avec Amazon Macie  
**Bonne réponse**  
Téléchargez les rapports depuis AWS Artifact  
Contactez l'équipe de conformité AWS  
Question 100Ignoré  
Si un client utilise une instance Amazon Linux EC2 réservée pendant 3 heures, 5 minutes et 6 secondes, quelle sera la durée totale de facturation pour cette utilisation ?  
3 heures, 5 minutes et 6 secondes  
**Bonne réponse**  
4 heures  
3 heures et 5 minutes  
Explication générale  
Si un client utilise une instance Amazon Linux EC2 réservée pendant 3 heures, 5 minutes et 6 secondes, il sera facturé pour 4 heures complètes, car l'unité facturable minimale pour les instances Amazon EC2 est d'une heure.

