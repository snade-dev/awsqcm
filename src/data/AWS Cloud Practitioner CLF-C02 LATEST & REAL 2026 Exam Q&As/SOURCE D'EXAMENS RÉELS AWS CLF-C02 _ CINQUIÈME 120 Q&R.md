Question 1Correct  
Une entreprise demande des rapports de conformité à la norme PCI DSS (Payment Card Industry Data Security Standard) attestant de l'efficacité opérationnelle des contrôles de sécurité d'AWS. Comment doit-elle se procurer ces rapports ?  
A. Contactez le support AWS.

#### Explications

Incorrect. Le support AWS fournit une assistance technique et relative aux comptes et peut aider à localiser des ressources, mais il n'héberge ni ne distribue d'attestations d'audit ou de rapports de conformité officiels de tiers qui valident l'efficacité opérationnelle des contrôles AWS.  
**Votre réponse est correcte**  
B. Téléchargez les rapports depuis AWS Artifact.

#### Explications

Exact. AWS Artifact est le portail libre-service qui permet d'accéder à la demande à la documentation de conformité AWS et aux rapports d'audit tiers (par exemple, les attestations PCI DSS et les résumés de responsabilité). Ces documents constituent les preuves officielles utilisées par les clients pour valider la conception et l'efficacité opérationnelle des contrôles de sécurité AWS.  
C. Téléchargez les rapports depuis AWS Security Hub.

#### Explications

Incorrect. AWS Security Hub agrège et normalise les résultats de sécurité et propose des contrôles de conformité automatisés, mais ne fournit pas de rapports d'audit ou d'attestations officiels de tiers. Les rapports de conformité officiels sont distribués via AWS Artifact.  
D. Contactez un responsable de compte technique AWS (TAM).

#### Explications

Incorrect. Un responsable technique de compte (TAM) peut fournir des conseils, aider à interpréter les documents de conformité et coordonner avec les équipes AWS, mais il ne remplace ni ne distribue les attestations d'audit officielles ; celles-ci sont accessibles via AWS Artifact.  
Explication générale  
Cette question vise à déterminer où obtenir la documentation officielle de conformité et d'audit d'AWS. AWS Artifact est la plateforme en libre-service désignée pour les rapports d'audit et les attestations de tiers (y compris PCI DSS) qui documentent l'efficacité opérationnelle des contrôles AWS. D'autres ressources, telles que le support, Security Hub ou un TAM, peuvent fournir des conseils ou des conclusions, mais ne proposent pas les rapports d'audit officiels nécessaires à la validation de la conformité.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 2Correct  
Une instance Amazon EC2 précédemment utilisée pour le développement est inaccessible et n'apparaît plus dans la console de gestion AWS. Quel service AWS faut-il utiliser pour déterminer l'action qui a rendu cette instance EC2 inaccessible ?  
A. Journaux Amazon CloudWatch

#### Explications

CloudWatch Logs permet de collecter, stocker et analyser les flux de journaux provenant d'applications, de systèmes d'exploitation et de certains services AWS. Il ne fournit pas de journal d'audit standardisé des appels à l'API de gestion AWS contenant l'identité de l'appelant, les noms des événements et les modifications de ressources nécessaires pour déterminer qui a effectué des actions sur une instance EC2.  
B. AWS Security Hub

#### Explications

Security Hub agrège et normalise les résultats de sécurité provenant d'autres services AWS et d'outils tiers afin de présenter le niveau de sécurité et les conclusions de conformité. Il n'enregistre pas l'historique brut des appels d'API ni les auteurs des modifications de ressources ; il ne peut donc pas être utilisé pour retracer l'action ayant rendu une instance inaccessible.  
C. Inspecteur Amazon

#### Explications

Amazon Inspector effectue des évaluations de sécurité automatisées (vérifications de vulnérabilité et de configuration) des instances EC2 et des images de conteneurs. Il n'enregistre pas les appels d'API IAM ni les événements liés au cycle de vie des ressources et ne peut donc pas identifier l'auteur d'une action sur une instance EC2.  
**Votre réponse est correcte**  
D. AWS CloudTrail

#### Explications

AWS CloudTrail enregistre l'activité du compte AWS sous forme d'appels d'API (événements de gestion et de données), incluant l'identité de l'appelant (principal/rôle IAM), le nom de l'événement, l'horodatage, l'adresse IP source et les ressources concernées. Utilisez l'historique des événements CloudTrail ou les fichiers journaux fournis (S3/CloudWatch Logs) pour identifier les opérations telles que TerminateInstances ou ModifyInstanceAttribute qui ont rendu l'instance inaccessible.  
Explication générale  
Cette question évalue les capacités d'audit et d'analyse des modifications apportées aux ressources AWS. AWS CloudTrail est le service de référence pour l'audit de l'activité des API de gestion et l'identification des personnes ayant effectué des actions sur les ressources (y compris les instances EC2). Les autres services mentionnés proposent la journalisation, les résultats de sécurité ou l'analyse des vulnérabilités, mais ne fournissent pas l'historique détaillé des appels d'API ni l'identité de l'appelant, contrairement à CloudTrail.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 3Correct  
Une entreprise doit identifier les personnes ayant accédé à un service AWS et les actions effectuées sur une période donnée. Quel service AWS doit-elle utiliser pour répondre à ce besoin ?  
A. Amazon CloudWatch

#### Explications

CloudWatch est un service d'observabilité et de surveillance qui collecte des métriques et des journaux, et génère des alarmes et des tableaux de bord. Il ne fournit pas d'historique des appels d'API effectués par les principaux IAM ni la trace d'audit complète des actions ; cette fonctionnalité est assurée par un service d'audit dédié. CloudWatch peut exploiter les journaux et les métriques (y compris ceux fournis par le service d'audit) et générer des alarmes, mais il ne constitue pas la source principale d'historique des accès utilisateurs ou des actions API.  
**Votre réponse est correcte**  
B. AWS CloudTrail

#### Explications

Ce service génère un historique quasi complet des appels aux API de gestion et de données, enregistrant l'auteur de chaque action, l'API utilisée, la date et l'heure, l'adresse IP source et les paramètres de la requête. Les journaux peuvent être stockés de manière pérenne et intégrés aux systèmes de surveillance, d'analyse et de traçabilité de l'organisation à des fins d'audit, de conformité et d'investigation numérique. Il constitue ainsi la solution idéale pour suivre les accès aux services et les actions effectuées.  
C. AWS Security Hub

#### Explications

Security Hub centralise et normalise les résultats de sécurité provenant de plusieurs services AWS et outils partenaires, et contribue à évaluer la conformité aux normes. Il n'enregistre pas l'activité au niveau des appels d'API et ne constitue pas la source de référence pour identifier les auteurs d'actions spécifiques sur les ressources AWS.  
D. Inspecteur Amazon

#### Explications

Inspector est un service d'évaluation automatisé permettant d'identifier les vulnérabilités de sécurité et les écarts par rapport aux bonnes pratiques dans les ressources de calcul et les images de conteneurs. Il se concentre sur l'évaluation des vulnérabilités et de la configuration, et non sur l'audit de l'activité des utilisateurs ou la journalisation des appels d'API.  
Explication générale  
This question tests auditing and accountability for AWS actions. The correct service provides an event history of API calls and user activity (who did what, when, where). That service captures request metadata and supports delivery to durable storage and integrations for compliance and investigation. The distractors focus on monitoring/observability (CloudWatch), security findings aggregation (Security Hub), and vulnerability assessment (Inspector), which are complementary but do not replace the audit-log capabilities required here.  
Domaine  
Domain 2: Security and Compliance  
Question 4Correct  
A company uses Amazon WorkSpaces. Which task is the responsibility of AWS, according to the AWS shared responsibility model?  
A. Set up multi-factor authentication (MFA) for each WorkSpaces user account.

#### Explications

Incorrect. Responsibility for identity and access management — including creating and administering user accounts, enforcing password policies, and enabling authentication mechanisms — lies with the customer. AWS supplies services (IAM, directory integrations) but does not configure individual customer user accounts.  
**Votre réponse est correcte**  
B. Ensure the environmental safety and security of the AWS infrastructure that hosts WorkSpaces.

#### Explications

Correct. Under the AWS shared responsibility model, AWS is responsible for the security of the cloud: physical data center security, environmental controls, networking hardware, and underlying host infrastructure that run managed services such as Amazon WorkSpaces.  
C. Provide security for WorkSpaces user accounts through AWS Identity and Access Management (IAM).

#### Explications

Incorrect. AWS provides IAM as a service, but configuring user permissions, roles, and account-level security for WorkSpaces is a customer responsibility (security in the cloud). AWS does not manage customers' user account settings or policies.  
D. Configure AWS CloudTrail to log API calls and user activity.

#### Explications

Incorrect. Delivery and configuration of logging and auditing (for example, enabling and managing AWS CloudTrail trails, retention, and analysis) are customer responsibilities. AWS provides CloudTrail but customers must enable and manage it for their accounts and resources.  
Explication générale  
This item tests knowledge of the AWS shared responsibility model. AWS handles 'security of the cloud' — the physical facilities, network, servers, and virtualization infrastructure that host services like WorkSpaces (answer B). Customers are responsible for 'security in the cloud' such as user accounts, authentication, permissions, and enabling monitoring/logging (the other options).  
Domaine  
Domain 2: Security and Compliance  
Question 5Correct  
A systems administrator created a new IAM user for a developer and assigned the user an access key instead of a user name and password. What is the access key used for?  
A. To access the AWS account as the AWS account root user

#### Explications

Incorrect. Les clés d'accès sont des identifiants utilisés pour signer les requêtes API (elles se composent d'un ID de clé d'accès et d'une clé d'accès secrète) et sont liées à une identité IAM. La connexion à l'administrateur de la console utilise l'adresse e-mail et le mot de passe du compte (et l'authentification multifacteur si elle est activée) ; la création d'une clé d'accès IAM n'équivaut pas à l'utilisation des identifiants de connexion à l'administrateur de la console.  
B. Accéder au compte AWS via la console de gestion AWS

#### Explications

Incorrect. La console de gestion AWS requiert une authentification interactive (nom d'utilisateur et mot de passe pour les utilisateurs IAM, ou fédération). Les clés d'accès sont destinées à un usage programmatique (API/CLI/SDK) et ne servent pas à l'authentification auprès de la console web.  
**Votre réponse est correcte**  
C. Accéder au compte AWS via une interface de ligne de commande (CLI)

#### Explications

Exact. Les clés d'accès (ID de clé d'accès \+ clé d'accès secrète) sont des identifiants permanents utilisés pour signer les requêtes effectuées par l'interface de ligne de commande AWS (AWS CLI), les kits de développement logiciel (SDK) ou les appels d'API directs. Elles permettent d'identifier et d'authentifier le principal IAM à l'origine de la requête. Il est recommandé d'utiliser des rôles IAM et des identifiants STS temporaires lorsque cela est possible, de renouveler régulièrement les clés et d'éviter d'intégrer des clés permanentes dans le code.  
D. Accéder à tous les comptes AWS d'une entreprise

#### Explications

Incorrect. Les clés d'accès sont liées à l'identité et au compte qui les possèdent. Accorder un accès multi-comptes nécessite une relation de confiance explicite entre comptes et une prise en charge des rôles (STS) ; les clés d'accès seules ne permettent pas un accès multi-comptes automatique.  
Explication générale  
Cette question évalue la compréhension des types d'identifiants IAM. Les clés d'accès (ID de clé d'accès et clé d'accès secrète) sont destinées à l'accès par programmation (CLI/SDK/API) et se distinguent des identifiants de console (mots de passe) et des mécanismes d'accès inter-comptes (rôles/STS). La bonne réponse identifie l'utilisation par programmation/API ; les autres options peuvent prêter à confusion avec la connexion à la console/l'accès root ou l'accès inter-comptes.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 6Incorrect  
Quelle solution AWS permet aux entreprises d'utiliser des protocoles tels que NFS pour stocker et récupérer des objets dans Amazon S3 ?  
A. Amazon FSx pour Lustre

#### Explications

FSx for Lustre est un système de fichiers haute performance conforme à la norme POSIX, conçu pour les charges de travail de calcul haute performance et de traitement de données. Il utilise le protocole Lustre (et non NFS) et, bien qu'il puisse s'intégrer à S3 pour l'importation/exportation de données, il ne propose pas d'interface NFS/SMB permettant le stockage direct d'objets dans S3 pour les clients NFS.  
B. Passerelle de volume AWS Storage Gateway

#### Explications

La passerelle de volumes Storage Gateway fournit des volumes iSCSI au niveau bloc aux applications sur site et stocke des instantanés dans AWS, mais elle expose un stockage par blocs (et non des protocoles de fichiers). Elle ne permet pas aux clients NFS/SMB de lire et d'écrire directement des objets dans S3.  
**Bonne réponse**  
C. Passerelle de fichiers AWS Storage Gateway

#### Explications

File Gateway expose une interface de fichiers (NFS et SMB) aux applications tout en stockant les fichiers sous forme d'objets dans Amazon S3. Il gère le mappage des objets et les métadonnées, fournit une mise en cache locale pour optimiser les performances et est explicitement conçu pour permettre l'accès basé sur NFS/SMB au stockage S3.  
**Votre réponse est incorrecte**  
D. Système de fichiers élastique Amazon (Amazon EFS)

#### Explications

Amazon EFS est un système de fichiers NFS géré, utilisé par les instances EC2 et les instances locales via le réseau. Il offre la sémantique POSIX et un stockage de fichiers évolutif. EFS n'est pas une passerelle vers S3 et ne stocke pas les fichiers en tant qu'objets S3.  
Explication générale  
Cette question teste vos connaissances sur les options de stockage hybride AWS permettant aux clients sur site ou en réseau d'utiliser des protocoles de fichiers tout en exploitant Amazon S3 comme système de stockage sous-jacent. AWS Storage Gateway (File Gateway) est la solution adéquate car il présente NFS/SMB aux clients et stocke les fichiers sous forme d'objets S3 avec mise en cache locale et mappage des métadonnées. Les autres services proposent soit un stockage par blocs (Volume Gateway), soit un système de fichiers Lustre haute performance (FSx for Lustre), soit un service NFS natif au sein d'AWS (EFS), mais aucun ne fait office de passerelle entre NFS/SMB et les objets S3.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 7Correct  
Un développeur a été embauché par une grande entreprise et a besoin d'identifiants AWS. Quelles sont les bonnes pratiques de sécurité à suivre ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Accorder au développeur l'accès uniquement aux ressources AWS nécessaires à l'exécution de sa tâche.

#### Explications

Correct. Appliquez le principe du moindre privilège à l'aide d'IAM : créez une identité individuelle, associez des politiques précises ou des appartenances à des groupes qui n'autorisent que les actions requises, et privilégiez les rôles ou les informations d'identification STS temporaires lorsque cela est approprié afin de minimiser l'impact.  
B. Partagez les identifiants de l'utilisateur racine du compte AWS avec le développeur.

#### Explications

Incorrect. L'utilisateur racine du compte AWS dispose d'un accès illimité et doit être protégé (activer l'authentification multifacteur, éviter toute utilisation régulière). Le partage des identifiants racine crée un point de vulnérabilité unique ; il est préférable de créer des identités IAM individuelles avec des autorisations limitées.  
C. Ajoutez le développeur au groupe d'administrateurs dans AWS IAM.

#### Explications

Incorrect. Accorder des privilèges d'administrateur complets à un développeur contrevient au principe du moindre privilège et accroît les risques. Utilisez des politiques IAM, des rôles et des limites d'autorisation précis afin que l'accès corresponde aux responsabilités du poste.  
D. Configurez une politique de mot de passe qui garantit que le mot de passe du développeur ne peut pas être modifié.

#### Explications

Incorrect. Empêcher la modification des mots de passe réduit la sécurité opérationnelle. Il est recommandé d'imposer des mots de passe robustes et modifiables et de permettre aux utilisateurs de les renouveler ou de les réinitialiser ; les politiques de mots de passe IAM peuvent exiger complexité et expiration, mais ne doivent pas rendre les identifiants immuables.  
**Votre sélection est correcte**  
E. Assurez-vous que la politique relative aux mots de passe des comptes exige une longueur minimale.

#### Explications

Exact. L'application d'une longueur minimale de mot de passe (et d'autres règles de complexité/expiration) via la stratégie de mot de passe du compte IAM renforce l'authentification. Combinée à l'authentification multifacteur (MFA), elle offre une protection des identifiants nettement supérieure.  
Explication générale  
Ce test évalue les bonnes pratiques de gestion des identifiants et des accès IAM. Les contrôles appropriés sont le principe du moindre privilège (attribution d'identités avec uniquement les autorisations nécessaires) et une politique de mots de passe robustes (longueur et complexité minimales). Les pratiques déviantes sont dangereuses : ne jamais partager ni utiliser régulièrement le compte racine, éviter d'octroyer des droits d'administrateur généraux et ne pas empêcher la rotation des mots de passe ; privilégiez plutôt des politiques IAM ciblées, des politiques de mots de passe et l'authentification multifacteur (MFA).  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 8Correct  
Une entreprise souhaite moderniser et convertir une application monolithique en microservices. Elle souhaite migrer cette application vers AWS. Quelle stratégie de migration doit-elle adopter ?  
A. Réhéberger

#### Explications

Cette approche consiste à migrer l'application vers le cloud avec des modifications de code minimales, voire nulles (on parle alors de migration « lift-and-shift »). Elle préserve l'architecture monolithique et ne décompose donc pas l'application en services déployables indépendamment, ne permettant ainsi pas d'atteindre l'objectif de modernisation par microservices.  
B. Replatform

#### Explications

Cette stratégie applique des modifications ciblées pour tirer parti des services gérés (par exemple, la migration d'une base de données vers Amazon RDS ou l'utilisation d'un service de conteneurs géré) tout en préservant l'architecture de base. N'exigeant pas de repenser l'application en composants déployables indépendamment, elle ne constitue pas une migration complète vers les microservices.  
C. Rachat

#### Explications

Cette option remplace la solution existante par un SaaS commercial ou un autre progiciel. Elle évite la refonte du code existant au lieu de convertir l'architecture monolithique en microservices ; elle n'est donc pas adaptée si l'objectif est de moderniser l'application existante en une architecture de microservices.  
**Votre réponse est correcte**  
D. Refactor

#### Explications

Cette stratégie consiste à repenser et à réarchitecturer l'application afin de la décomposer en services plus petits et déployables indépendamment. Sur AWS, cela implique généralement l'utilisation de conteneurs (ECS, EKS ou Fargate) et/ou de composants sans serveur (Lambda \+ API Gateway), le découplage avec la messagerie (SQS, SNS) et la migration vers des bases de données managées (RDS/Aurora, DynamoDB). La refactorisation permet une mise à l'échelle indépendante, des déploiements plus rapides et une meilleure isolation des pannes — autant de caractéristiques essentielles à la modernisation d'une architecture de microservices.  
Explication générale  
La question porte sur la stratégie de migration permettant de convertir une application monolithique en microservices. La stratégie appropriée consiste à refactoriser/réarchitecturer l'application, car cela implique de repenser ses composants en services plus petits et déployables indépendamment, et d'adopter des modèles natifs du cloud (conteneurs, architecture sans serveur, messagerie, services de données gérés). Les autres stratégies – migration à l'identique, modifications minimales de la plateforme ou remplacement par une solution SaaS – ne restructurent pas le monolithe en microservices et ne répondent donc pas à l'objectif de modernisation énoncé.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 9Correct  
Laquelle des propositions suivantes décrit certaines des fonctionnalités de base d'Amazon S3 ?  
A. Amazon S3 est un service de stockage par blocs haute performance conçu pour être utilisé avec Amazon EC2.

#### Explications

Incorrect : cette description fait référence au stockage par blocs pouvant être associé à une instance EC2. Le stockage par blocs AWS est fourni par Amazon EBS ; S3 utilise un modèle de stockage objet accessible via des API et n’est pas monté comme un périphérique de stockage par blocs.  
**Votre réponse est correcte**  
B. Amazon S3 est un service de stockage d'objets qui offre des performances, une sécurité, une évolutivité et une disponibilité des données de haut niveau.

#### Explications

Exact — S3 implémente une architecture de stockage objet avec un espace de noms plat et est conçu pour une scalabilité massive, une haute durabilité (99,9 ...  
C. Amazon S3 est un système de stockage de fichiers entièrement géré, hautement fiable et évolutif, accessible via le protocole SMB standard du secteur.

#### Explications

Incorrect — SMB est un protocole de partage de fichiers utilisé par les systèmes de fichiers Windows. AWS fournit un stockage de fichiers conforme à la norme POSIX/SMB via Amazon EFS (NFS) ou Amazon FSx (Windows/SMB). S3 n'est pas un système de fichiers conforme à POSIX et est accessible via des API REST et des kits de développement logiciel (SDK) plutôt que par SMB.  
D. Amazon S3 est un système de fichiers NFS élastique, évolutif et entièrement géré, utilisable avec les services cloud AWS et les ressources sur site.

#### Explications

Incorrect — Les systèmes de fichiers partagés de type NFS, conformes à la norme POSIX, sont proposés par Amazon EFS ou FSx pour Lustre. S3 est un stockage objet exposé via des API et ne fournit pas les fonctionnalités natives de NFS ni ne se comporte comme un serveur NFS géré.  
Explication générale  
Cette question teste votre connaissance de S3 en tant que service de stockage d'objets d'AWS. La bonne réponse est celle qui décrit le modèle objet de S3, son extrême durabilité, sa scalabilité, ses fonctionnalités de sécurité et son accès via API. Les réponses incorrectes décrivent d'autres catégories de stockage (stockage par blocs ou services de fichiers/NFS/SMB) fournies par EBS, EFS ou FSx et qui, par conséquent, ne s'appliquent pas à S3.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 10Correct  
Parmi les éléments suivants, lesquels constituent les piliers du cadre AWS Well-Architected ? (Choisissez deux réponses.)  
A. Haute disponibilité

#### Explications

Ce choix décrit un objectif de conception (améliorer la disponibilité) plutôt qu'un pilier spécifique de l'architecture. La disponibilité et la tolérance aux pannes sont traitées par le pilier Fiabilité, qui fournit les recommandations et les bonnes pratiques pour atteindre une haute disponibilité.  
**Votre sélection est correcte**  
B. Efficacité de la performance

#### Explications

Il s'agit de l'un des piliers officiels de Well-Architected. Il couvre le choix des types et des tailles de ressources appropriés, la surveillance des performances, l'analyse comparative et l'adaptation des architectures (par exemple, l'utilisation de services gérés, de modèles sans serveur, de la mise en cache et de la mise à l'échelle automatique) afin que les charges de travail répondent efficacement aux exigences.  
**Votre sélection est correcte**  
C. Optimisation des coûts

#### Explications

Il s'agit de l'un des piliers officiels de l'architecture bien conçue. Elle vise à contrôler et à réduire les coûts grâce à des pratiques telles que l'élimination du gaspillage, le dimensionnement approprié, l'utilisation d'instances Spot/réservées ou de plans d'économies, et le suivi des dépenses avec des outils comme AWS Cost Explorer, Budgets et Trusted Advisor.  
D. Devenir mondial en quelques minutes

#### Explications

Le déploiement mondial rapide est une capacité de l'infrastructure AWS (régions, zones de disponibilité, CloudFront, Route 53), mais il s'agit d'un avantage de la plateforme plutôt que d'un des piliers de Well-Architected et donc pas d'un pilier en soi.  
E. Développement continu

#### Explications

Continuous development (CI/CD) is a delivery practice and set of processes (supported by services like AWS CodePipeline/CodeBuild) that maps to Operational Excellence practices, but it is not one of the six named Well‑Architected pillars.  
Explication générale  
The AWS Well‑Architected Framework defines six pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. The question asks to identify two pillars from the options; Performance Efficiency and Cost Optimization are both named pillars and therefore correct. The other options describe design goals or practices (availability, CI/CD) or AWS capabilities (global reach) that are important but are not listed as separate pillars.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 11Correct  
A company wants to provision and manage its AWS infrastructure by using the common programming languages Typescript, Python, Java, and .NET. Which AWS service will meet this requirement?  
A. AWS CodeBuild

#### Explications

Used to run build and test jobs as part of CI/CD pipelines; it is not an infrastructure-as-code framework that lets you author and synthesize cloud resources using general-purpose languages like TypeScript, Python, Java, or .NET.  
B. AWS CloudFormation

#### Explications

Provides declarative provisioning using JSON or YAML CloudFormation templates. It does not natively let you write infrastructure directly in TypeScript, Python, Java, or .NET (although tools such as the AWS CDK can generate CloudFormation templates from code written in those languages).  
C. AWS CLI

#### Explications

A command-line tool for calling AWS APIs and scripting operations. While it can create and manage resources, it is not a framework for defining infrastructure using the listed programming languages and does not provide language-specific constructs or synthesis to CloudFormation.  
**Votre réponse est correcte**  
D. AWS Cloud Development Kit (AWS CDK)

#### Explications

An open-source framework that provides language bindings for TypeScript, Python, Java, and .NET to define cloud infrastructure using high-level constructs. Code is synthesized into CloudFormation templates and provisioned via CloudFormation, enabling infrastructure-as-code in those programming languages.  
Explication générale  
This item tests infrastructure-as-code options on AWS. The AWS CDK is the correct choice because it is specifically designed to let developers define AWS infrastructure using general-purpose languages (TypeScript, Python, Java, .NET) and then synthesize those definitions into CloudFormation templates for provisioning. CloudFormation itself uses JSON/YAML templates, and tools like the AWS CLI or CodeBuild serve operational or CI/CD roles rather than providing multi-language IaC abstractions.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 12Correct  
A developer needs to maintain a development environment infrastructure and a production environment infrastructure in a repeatable fashion. Which AWS service should the developer use to meet these requirements?  
A. AWS Ground Station

#### Explications

This option describes a managed ground station service for satellite communications (satellite downlink, scheduling, and data processing). It is not an infrastructure-as-code or provisioning tool and therefore cannot be used to repeatably define and deploy development and production environments.  
B. AWS Shield

#### Explications

This option is a managed DDoS protection service (Shield Standard and Shield Advanced) focused on network-layer security. It protects resources from distributed denial-of-service attacks but does not provide capabilities to define or provision AWS infrastructure in a repeatable way.  
C. AWS IoT Device Defender

#### Explications

This option is a security management service for IoT fleets (audit, detect, and remediate IoT device security issues). It is unrelated to provisioning or templating AWS infrastructure for development and production environments.  
**Votre réponse est correcte**  
D. AWS CloudFormation

#### Explications

CloudFormation is the AWS declarative infrastructure-as-code service that uses JSON/YAML templates to define resources as stacks. It enables repeatable, versionable provisioning, supports parameters, change sets, drift detection, and StackSets for multi-account/multi-region deployments—making it the appropriate choice to maintain consistent development and production infrastructures.  
Explication générale  
The question tests knowledge of infrastructure-as-code. AWS CloudFormation is the service that lets you declare and provision AWS resources from templates to reproduce environments reliably. The other options are specialized services (satellite ground station, DDoS protection, IoT security) that do not provide templated infrastructure provisioning, so they are not suitable for maintaining repeatable dev and prod environments.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 13Correct  
A company wants to connect its supported AWS services and VPCs. The company does not want to expose its internal traffic to the public internet. Which AWS service will meet these requirements?  
A. Amazon Inspector

#### Explications

Amazon Inspector is an automated security assessment service that analyzes EC2 instances and container images for vulnerabilities and deviations from best practices. It does not provide network connectivity or VPC endpoints and therefore cannot be used to create private links between VPCs and AWS services.  
**Votre réponse est correcte**  
B. AWS PrivateLink

#### Explications

AWS PrivateLink provides private connectivity to supported AWS services and endpoint services using interface VPC endpoints (Elastic Network Interfaces with private IPs in your subnets). Traffic using PrivateLink remains on the AWS network and does not traverse the public internet, making it the appropriate solution for connecting VPCs and services without exposing internal traffic.  
C. Amazon Connect

#### Explications

Amazon Connect is a managed cloud contact-center service for customer interactions. It is unrelated to VPC networking or private service endpoints and does not provide the private connectivity required by this scenario.  
D. AWS Internet Gateway

#### Explications

An Internet Gateway attaches a VPC to the public internet and enables routing to/from internet addresses. Because it enables public internet access, it would expose internal traffic and therefore does not meet the requirement to keep traffic off the public internet.  
Explication générale  
The requirement is private connectivity between VPCs and supported AWS services without routing traffic over the public internet. AWS PrivateLink (interface VPC endpoints) achieves this by creating ENI-based endpoints that keep traffic on the AWS network. The other choices either provide public internet access (Internet Gateway) or are unrelated services (Inspector, Connect) and do not fulfill the private connectivity requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 14Correct  
A company needs to run some of its workloads on premises to comply with regulatory guidelines. The company wants to use the AWS Cloud to run workloads that are not required to be on premises. The company also wants to be able to use the same API calls for the on-premises workloads and the cloud workloads. Which AWS service or feature should the company use to meet these requirements?  
A. Dedicated Hosts

#### Explications

Incorrect. Dedicated Hosts reserve an EC2 physical server for a single AWS account to help with software licensing and compliance, but they do not extend AWS infrastructure, control plane, or service APIs into a customer’s on‑premises data center and therefore cannot provide a unified API surface for hybrid workloads.  
**Votre réponse est correcte**  
B. AWS Outposts

#### Explications

Correct. AWS Outposts delivers AWS-managed hardware and software to a customer’s premises and exposes the same AWS control plane and supported service APIs (for example, EC2, EBS, ECS/EKS, RDS where supported) and management tools, enabling workloads on‑premises to use the same API calls and operational workflows as workloads running in AWS Regions.  
C. Availability Zones

#### Explications

Incorrect. Availability Zones are isolated locations within an AWS Region that provide redundancy and high availability for cloud deployments; they are not an on‑premises offering and do not provide a mechanism to run AWS services or the AWS API surface inside a customer data center.  
D. AWS Wavelength

#### Explications

Incorrect. AWS Wavelength places compute at the edge of telecom networks to reduce latency for mobile and 5G applications; it is designed for edge/telecom scenarios and does not extend AWS infrastructure or APIs into a customer’s on‑premises environment for hybrid management.  
Explication générale  
This question tests knowledge of AWS hybrid deployment options. The requirement is to run some workloads on‑premises for regulatory reasons while using identical AWS APIs for both on‑premises and cloud workloads. Outposts is the AWS solution that extends the AWS control plane, supported service APIs, and management tools to customer premises, enabling consistent API usage and operations. The other choices (Dedicated Hosts, Availability Zones, Wavelength) address tenancy, regional availability, or edge latency use cases and do not provide a managed, API-consistent on‑premises AWS environment.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 15Correct  
A company uses Amazon RDS for a product database. The company wants to ensure the database is highly available. Which feature of Amazon RDS will meet this requirement?  
A. Read replicas

#### Explications

Incorrect. Read replicas use asynchronous replication to offload read traffic and improve read scalability. Because replication is asynchronous, they do not provide automatic, synchronous failover of the primary instance and therefore do not guarantee high availability.  
B. Blue/green deployment

#### Explications

Incorrect. Blue/green deployment is a release/deployment strategy that reduces risk and downtime during updates by switching traffic between environments; it does not provide automatic cross‑Availability Zone redundancy or failover for an RDS primary instance.  
**Votre réponse est correcte**  
C. Multi-AZ deployment

#### Explications

Correct. Multi‑AZ deployment provisions a synchronous standby in a different Availability Zone and configures automatic failover. This architecture provides high availability and minimizes downtime when the primary instance, underlying hardware, or AZ fails. The standby is maintained for failover rather than for read scaling.  
D. Reserved Instances

#### Explications

Incorrect. Reserved Instances are a pricing/commitment option that reduces cost for long‑term usage; they change billing, not replication, redundancy, or failover behavior.  
Explication générale  
The key concept tested is Amazon RDS high availability. Multi‑AZ deployments provide synchronous standby replicas in a different Availability Zone and automatic failover, which directly addresses availability and resilience. The other options are distractors: read replicas are for read scaling (asynchronous), blue/green is a deployment strategy, and reserved instances affect pricing only.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 16Correct  
A company is developing an application that uses multiple AWS services. The application needs to use temporary, limited-privilege credentials for authentication with other AWS APIs. Which AWS service or feature should the company use to meet these authentication requirements?  
A. Amazon API Gateway

#### Explications

Incorrect. API Gateway is a managed service for creating, securing, and monitoring APIs and can validate or front requests, but it does not issue AWS credentials or create temporary AWS security tokens for authenticating to other AWS APIs.  
B. IAM users

#### Explications

Incorrect. IAM users represent long-term credentials (persistent access keys or console passwords). They are not designed for short-lived, limited-privilege access and are discouraged for application authentication where temporary credentials are required.  
**Votre réponse est correcte**  
C. AWS Security Token Service (AWS STS)

#### Explications

Correct. AWS STS issues short-lived security credentials (access key ID, secret access key, and session token) via operations such as AssumeRole and AssumeRoleWithWebIdentity. These credentials are time-limited and scoped by IAM roles and policies, enabling least-privilege, cross-account access, and federated or mobile scenarios without exposing long-term keys.  
D. IAM instance profiles

#### Explications

Incorrect. An instance profile is a mechanism to attach an IAM role to an EC2 instance so the instance can obtain temporary credentials from the instance metadata service. It’s EC2-specific and a way to deliver role-based temporary credentials to that instance, not a general-purpose credential-issuing service for arbitrary application authentication flows.  
Explication générale  
The question tests knowledge of how to obtain temporary, limited-privilege AWS credentials. AWS STS is the dedicated service that issues time-limited credentials tied to IAM roles or federation flows, enabling secure, short-lived access. The distractors either provide API management (API Gateway), long-term credentials (IAM users), or an EC2-specific role attachment mechanism (instance profiles), none of which serve as the general credential-issuing service STS provides.  
Domaine  
Domain 2: Security and Compliance  
Question 17Correct  
A company wants to provide managed Windows virtual desktops and applications to its remote employees over secure network connections. Which AWS services can the company use to meet these requirements? (Choose two.)  
A. Amazon Connect

#### Explications

This is a cloud contact-center service for managing customer voice, chat, and omnichannel interactions. It does not provide virtual desktops or application streaming functionality and therefore does not meet the requirement.  
**Votre sélection est correcte**  
B. Amazon AppStream 2.0

#### Explications

A managed application streaming service that delivers Windows applications to users through secure streaming sessions. It centralizes application management (image builder, fleets), integrates with directory/authentication, and encrypts application traffic so users get Windows apps without managing full desktop infrastructure.  
**Votre sélection est correcte**  
C. Amazon WorkSpaces

#### Explications

A managed Desktop-as-a-Service (DaaS) offering that provides persistent or non-persistent Windows desktops managed by AWS. It integrates with AWS Directory Service/AD Connector, supports encryption of data in transit and at rest, and is designed specifically to deliver full virtual Windows desktops to remote users.  
D. AWS Site-to-Site VPN

#### Explications

A network connectivity service that creates encrypted IPSec tunnels between on-premises networks and AWS VPCs. It provides secure connectivity but does not itself deliver managed desktops or application streaming — it can complement desktop services but is not a desktop/application service.  
E. Amazon Elastic Container Service (Amazon ECS)

#### Explications

A container orchestration service for running containerized applications on EC2 or AWS Fargate. It is intended for deploying backend and application containers, not for providing interactive Windows virtual desktops or streaming Windows GUI applications to end users.  
Explication générale  
Amazon AppStream 2.0 and Amazon WorkSpaces are the appropriate services: AppStream 2.0 streams Windows applications securely without full desktop management, and WorkSpaces provides managed Windows virtual desktops. The other choices are for contact-center functionality (Connect), network connectivity only (Site-to-Site VPN), or containerized application hosting (ECS), none of which directly provide managed Windows desktops or application streaming.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 18Correct  
Which AWS service provides users with AWS issued reports, certifications, accreditations, and third-party attestations?  
**Votre réponse est correcte**  
A. AWS Artifact

#### Explications

AWS Artifact is the centralized on-demand repository for AWS-issued compliance documentation (Reports) and customer-specific agreements (Agreements). It provides access to AWS compliance reports and third-party attestations such as SOC, ISO, PCI, and other audit artifacts that customers download or reference to support audits and regulatory compliance obligations.  
B. AWS Trusted Advisor

#### Explications

Trusted Advisor provides automated best-practice checks and actionable recommendations across cost optimization, security, fault tolerance, performance, and service limits. It does not serve as a repository for AWS-issued compliance reports or third-party attestations.  
C. AWS Health Dashboard

#### Explications

AWS Health Dashboard (and the Personal Health Dashboard) delivers alerts and detailed information about service events and account-level health that affect you. It reports service status and notifications, not AWS compliance reports or certifications.  
D. AWS Config

#### Explications

AWS Config records and evaluates resource configurations over time and can assess compliance against custom or managed rules. It helps demonstrate configuration compliance but does not issue AWS-authored certification documents or third-party attestations.  
Explication générale  
The question tests where to obtain official AWS compliance documentation. AWS Artifact is the service designed to provide AWS-issued reports and third-party attestations used for audits and regulatory compliance. The other services listed (Trusted Advisor, Health Dashboard, AWS Config) provide operational guidance, service-event information, or configuration compliance data, but they do not publish AWS compliance reports or formal attestations.  
Domaine  
Domain 2: Security and Compliance  
Question 19Correct  
A company needs to block SQL injection attacks. Which AWS service or feature can meet this requirement?  
**Votre réponse est correcte**  
A. AWS WAF

#### Explications

This service inspects HTTP(S) requests at the application (Layer 7\) and provides managed and custom rule types (including SQLi match statements) that detect and block SQL injection patterns in request components such as the query string, headers, and body. It integrates with CloudFront, Application Load Balancer, and API Gateway and can be centrally managed across accounts with Firewall Manager for consistent SQLi protection.  
B. AWS Shield

#### Explications

This offering provides DDoS protection focused on volumetric and protocol-layer attacks and, with Advanced, enhanced detection/response for DDoS events. It does not perform deep inspection of HTTP request payloads to identify SQL injection patterns, so it cannot be relied upon to block SQLi.  
C. Network ACLs

#### Explications

Network ACLs are stateless, subnet-level access controls that allow or deny traffic based on IP addresses and ports (network/transport layers). They do not analyze application-layer content and therefore cannot detect or block SQL injection attempts.  
D. Security groups

#### Explications

Les groupes de sécurité sont des pare-feu avec état, au niveau de l'instance, qui filtrent le trafic par adresse IP et port. Ils fonctionnent au niveau des couches réseau/transport et n'inspectent pas les charges utiles HTTP ni n'appliquent les signatures de la couche application nécessaires pour empêcher les injections SQL.  
Explication générale  
Bloquer les injections SQL nécessite une inspection au niveau de la couche application (couche 7\) et une logique de règles qui recherche les schémas d'injection SQL dans les requêtes HTTP. Le pare-feu applicatif web offre ces fonctionnalités (règles gérées, instructions de correspondance SQLi, intégration avec CDN/ALB/API Gateway). Les autres solutions se concentrent sur le filtrage au niveau du réseau ou la protection contre les attaques DDoS et ne proposent pas l'inspection de la charge utile au niveau de la couche application nécessaire pour stopper les injections SQL.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 20Correct  
Quel service ou outil AWS permet de surveiller les ressources et les applications AWS en temps réel ?  
A. Conseiller de confiance AWS

#### Explications

Ce service propose des analyses et des recommandations de bonnes pratiques en matière de coûts, de sécurité, de tolérance aux pannes et de performances. Il génère des analyses et des rapports consultatifs périodiques (certaines analyses sont actualisées automatiquement et la pleine fonctionnalité dépend du niveau de support), et non une collecte continue de métriques, de journaux, d'alarmes ou de tableaux de bord pour une surveillance opérationnelle en temps réel.  
**Votre réponse est correcte**  
B. Amazon CloudWatch

#### Explications

Collecte et stocke les données opérationnelles sous forme de métriques, de journaux et d'événements provenant des ressources et applications AWS. Prend en charge les tableaux de bord en temps réel, les alarmes configurables, la recherche et l'agrégation des journaux (CloudWatch Logs), les réponses automatisées via Alarms and Events/EventBridge, ainsi que les fonctionnalités de surveillance (par exemple, Container Insights et Synthetics) pour une observabilité et des alertes actives et quasi temps réel.  
C. AWS CloudTrail

#### Explications

Enregistre l'activité et les événements de gestion des API AWS à des fins d'audit, de gouvernance et de conformité. Transmet les journaux d'audit (généralement vers S3 et, en option, vers CloudWatch Logs) et est destiné à des fins d'analyse et de conformité, et non à la surveillance continue des performances ou des applications.  
D. AWS Cost Explorer

#### Explications

Cet outil fournit des analyses de coûts et d'utilisation, des prévisions, des budgets et des recommandations d'optimisation des ressources à des fins de facturation. Il s'agit d'un outil d'analyse financière et d'utilisation qui ne collecte ni ne présente de données opérationnelles en temps réel ni de journaux d'application.  
Explication générale  
Cette question évalue vos connaissances sur les fonctionnalités de surveillance d'AWS. La bonne réponse est le service conçu pour collecter les métriques, les journaux et les événements, et fournir des tableaux de bord, des alarmes et des réponses automatisées pour une meilleure observabilité opérationnelle. Les autres options abordent des problématiques différentes (recommandations de bonnes pratiques, journalisation des API/audits et analyse des coûts) et ne constituent donc pas l'outil principal de surveillance en temps réel.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 21Correct  
Quel service permet aux clients d'auditer les appels d'API dans leurs comptes AWS ?  
**Votre réponse est correcte**  
A. AWS CloudTrail

#### Explications

CloudTrail est le service AWS qui enregistre et fournit un historique des appels d'API et des événements associés au sein d'un compte AWS. Il capture les événements de gestion (console, SDK, CLI et appels de service à service) et, en option, les événements de données. Il écrit les fichiers journaux dans un compartiment S3, prend en charge les journaux multirégionaux, l'intégration avec CloudWatch Logs et la validation de l'intégrité des fichiers journaux, ce qui en fait l'outil idéal pour l'audit, la conformité et les investigations numériques.  
B. Conseiller de confiance AWS

#### Explications

Trusted Advisor provides best-practice checks and actionable recommendations for cost optimization, performance, security, and fault tolerance as part of AWS Support; it does not capture a continuous record of account API calls or produce an auditable event history.  
C. Amazon Inspector

#### Explications

Amazon Inspector performs automated security assessments (vulnerability and CIS-type checks) on compute resources and container images to find exposures and deviations from security standards; it is not designed to log or audit account-level API call activity.  
D. AWS X-Ray

#### Explications

AWS X-Ray is a distributed tracing service that instruments applications to trace requests and diagnose performance or latency issues across services; it captures traces and segments for application debugging, not an account-wide audit trail of API calls.  
Explication générale  
The question tests knowledge of AWS auditing capabilities. CloudTrail is the correct choice because it is the dedicated service that records API activity and delivers auditable logs (management and optional data events) for security, compliance, and troubleshooting. The other services listed provide recommendations (Trusted Advisor), vulnerability assessments (Inspector), or application tracing (X-Ray), none of which produce the account-wide API call audit logs CloudTrail provides.  
Domaine  
Domain 2: Security and Compliance  
Question 22Correct  
Which feature of Amazon RDS provides the ability to automatically create a primary database instance and to synchronously replicate data to an instance in another Availability Zone?  
A. Read replicas

#### Explications

Incorrect. Read replicas provide read scalability by creating asynchronous copies of a DB instance. Because replication is asynchronous, they do not guarantee zero data loss or automatic failover for high availability; replicas can be promoted manually to become a primary but are not the RDS mechanism for synchronous cross‑AZ failover.  
B. Blue/green deployment

#### Explications

Incorrect. Blue/green deployment is an application deployment strategy for switching between two environments to reduce downtime and risk. It is not an Amazon RDS feature that performs synchronous replication or automatic failover between Availability Zones.  
**Votre réponse est correcte**  
C. Multi-AZ deployment

#### Explications

Correct. The RDS Multi‑AZ feature provisions a standby instance in a different Availability Zone and keeps data synchronously replicated to that standby. Amazon RDS manages automatic failover to the standby to provide high availability and durability. Note that the standby is not used for read traffic.  
D. Reserved Instances

#### Explications

Incorrect. Reserved Instances are a billing/discount mechanism that reduce the cost of long‑running database instances. They do not affect replication behavior, availability, or failover capabilities.  
Explication générale  
This question assesses knowledge of Amazon RDS high‑availability and replication options. The correct answer is the RDS Multi‑AZ feature because it creates a standby in a different Availability Zone and uses synchronous replication with automatic failover. Read replicas are asynchronous and intended for read scaling, blue/green deployment is a deployment strategy (not an RDS replication feature), and Reserved Instances relate only to pricing.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 23Correct  
Which AWS service can a company use to manage encryption keys in the cloud?  
A. AWS License Manager

#### Explications

Manages software licenses across AWS and on-premises environments; it does not provide cryptographic key lifecycle features (generation, secure hardware storage, rotation, or usage controls) needed for encryption key management.  
B. AWS Certificate Manager (ACM)

#### Explications

Focused on provisioning and managing TLS/SSL certificates (and private CAs via ACM Private CA). It handles certificate lifecycle for TLS but is not a general-purpose key management service and does not provide HSM-backed key custody for application data encryption.  
**Votre réponse est correcte**  
C. AWS CloudHSM

#### Explications

Provides dedicated, single-tenant Hardware Security Modules (HSMs) that let customers generate, store, and use cryptographic keys under their control. CloudHSM is FIPS 140-2 Level 3 validated, can be accessed via HSM APIs, and can integrate with AWS KMS custom key stores — making it appropriate for HSM-backed key management and strict compliance requirements.  
D. AWS Directory Service

#### Explications

Delivers managed directory services (for example, AWS Managed Microsoft AD) to support identity, authentication, and directory-aware applications. It does not perform cryptographic key generation, secure key storage, or key lifecycle management.  
Explication générale  
The question assesses knowledge of AWS services used for cryptographic key custody. AWS CloudHSM is the correct choice because it supplies dedicated HSM appliances for generating and storing keys with strong compliance (FIPS 140-2 Level 3\) and can be used directly or integrated with KMS. The other options address separate needs: License Manager handles software licensing, ACM manages TLS certificates, and Directory Service provides identity/directory features — none offer dedicated HSM-backed key management for encrypting data.  
Domaine  
Domain 2: Security and Compliance  
Question 24Incorrect  
A company wants to manage access and permissions for its third-party software as a service (SaaS) applications. The company wants to use a portal where end users can access assigned AWS accounts and AWS Cloud applications. Which AWS service should the company use to meet these requirements?  
**Votre réponse est incorrecte**  
A. Amazon Cognito

#### Explications

Amazon Cognito provides user sign-up, sign-in, and token-based authentication for web and mobile applications (via user pools) and temporary AWS credentials for app resources (via identity pools). It is an application-level identity service and does not provide a centralized portal, built-in multi-account AWS access management, or native SaaS provisioning for end users across multiple AWS accounts.  
**Bonne réponse**  
B. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

AWS IAM Identity Center centralizes identity and access management across AWS accounts and cloud applications. It uses permission sets that map to IAM roles for account access, offers a user-facing portal (My Applications) for assigned AWS accounts and SaaS apps, and supports SAML/OIDC federation and SCIM provisioning to many third-party SaaS providers — matching the requirements described.  
C. AWS Identity and Access Management (IAM)

#### Explications

AWS Identity and Access Management (IAM) manages identities, policies, and roles within an AWS account (and enables role-based cross-account access), but it is not a user portal or a SaaS application SSO/provisioning service and lacks the centralized multi-account application-assignment workflows provided by IAM Identity Center.  
D. AWS Directory Service for Microsoft Active Directory

#### Explications

AWS Directory Service for Microsoft Active Directory provides a managed Microsoft AD for domain join, Windows authentication (Kerberos/LDAP), and on-prem AD integration. It is intended for directory-aware workloads and Windows environments and does not provide an end-user portal or native SaaS application SSO and multi-account assignment features.  
Explication générale  
The question tests identity and access management for end users across multiple AWS accounts and third-party SaaS apps with a single portal. AWS IAM Identity Center is designed for that use case: it centralizes access, exposes a user portal for assigned AWS accounts and cloud applications, and supports SAML/SCIM federation and permission-set → IAM role mappings. The other services (Cognito, IAM, Directory Service) provide authentication or directory features for specific contexts (application auth, account-level IAM, or AD integration) but do not deliver the centralized multi-account SaaS portal and provisioning workflow required here.  
Domaine  
Domain 2: Security and Compliance  
Question 25Correct  
A company is storing sensitive customer data in an Amazon S3 bucket. The company wants to protect the data from accidental deletion or overwriting. Which S3 feature should the company use to meet these requirements?  
A. S3 Lifecycle rules

#### Explications

Lifecycle rules automate transitions between storage classes and object expiration for cost management. They do not provide recoverability or prevent accidental deletion/overwrites; in fact, a misconfigured lifecycle rule can delete objects permanently. Lifecycle rules can interact with versioning (e.g., expire previous versions), but they are not a recovery mechanism.  
**Votre réponse est correcte**  
B. S3 Versioning

#### Explications

Versioning stores multiple immutable versions of each object in a bucket so that overwrites create new versions and deletes create delete markers while previous versions remain retrievable. This enables recovery of prior object states after accidental overwrite or deletion. For additional protection against permanent removal, versioning can be combined with MFA Delete or S3 Object Lock for retention/immutability.  
C. S3 bucket policies

#### Explications

Bucket policies control which principals can perform actions (Allow/Deny) on a bucket or objects. While they can be used to restrict who can delete objects, policies are an access-control mechanism and do not themselves preserve prior object data or provide automatic recovery from accidental deletes/overwrites.  
D. S3 server-side encryption

#### Explications

Server-side encryption (SSE-S3, SSE-KMS, SSE-C) protects object data at rest by encrypting it, but it does not affect object lifecycle, versioning, or deletion semantics and therefore does not prevent accidental deletion or overwriting.  
Explication générale  
The question tests knowledge of S3 data protection features. Enabling S3 Versioning is the appropriate choice because it preserves every object version and allows restoration after accidental overwrites or deletions. The other options address different concerns: lifecycle rules manage cost and retention, bucket policies control access, and server-side encryption protects data at rest—none provide the same recoverability that versioning does. For stronger prevention of deletion, consider combining versioning with MFA Delete or S3 Object Lock.  
Domaine  
Domain 2: Security and Compliance  
Question 26Correct  
Which of the following is a fully managed graph database service on AWS?  
A. Amazon Aurora

#### Explications

Aurora is a fully managed relational database (MySQL/PostgreSQL-compatible) optimized for OLTP and SQL workloads. It is not designed to provide native graph models or graph query engines (Gremlin/SPARQL), so it does not meet the requirement for a managed graph database service.  
B. Amazon FSx

#### Explications

Amazon FSx provides managed file systems (Windows, Lustre, etc.) for shared file storage. It is a storage service, not a database, and therefore does not offer graph data models or graph query capabilities.  
C. Amazon DynamoDB

#### Explications

DynamoDB is a fully managed NoSQL key-value and document database with single-digit millisecond latency. While you can model relationships in DynamoDB at the application level, it does not natively support graph data models or graph query languages (property graph/RDF, Gremlin/SPARQL), so it is not a purpose-built graph database service.  
**Votre réponse est correcte**  
D. Amazon Neptune

#### Explications

Amazon Neptune is a purpose-built, fully managed graph database that supports both property graph (Apache TinkerPop/Gremlin) and RDF (SPARQL) models. It provides ACID transactions, high availability across AZs, read replicas, and integrates with AWS security and encryption features — all characteristics required for a managed graph database service.  
Explication générale  
The question tests recognition of AWS services specialized for graph workloads. Amazon Neptune is the correct choice because it is explicitly designed and managed to store and query graph data using Gremlin or SPARQL. The other options are managed services for relational databases (Aurora), file storage (FSx), or key-value/document NoSQL (DynamoDB) and do not provide native graph database features.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 27Correct  
Une entreprise de vente au détail en ligne souhaite migrer ses charges de travail locales vers AWS. Elle doit gérer automatiquement et à moindre coût les pics saisonniers de charge de travail. Quelles fonctionnalités du cloud AWS lui permettront de répondre à ce besoin ? (Choisissez deux réponses.)  
A. Déploiement de charges de travail interrégionales

#### Explications

Le déploiement interrégional des charges de travail répartit les ressources entre différentes régions géographiques afin d'améliorer la disponibilité, la latence et la reprise après sinistre. Toutefois, il ne permet pas, à lui seul, une mise à l'échelle élastique automatique en fonction des pics de demande et peut engendrer des coûts supplémentaires de transfert et de réplication des données ; il ne constitue donc pas la solution principale pour une mise à l'échelle saisonnière rentable.  
**Votre sélection est correcte**  
B. Tarification à l'utilisation

#### Explications

La facturation à l'usage d'AWS signifie que vous êtes facturé uniquement pour votre consommation réelle de ressources (heures de calcul, stockage utilisé, appels d'API, etc.). Pour les charges de travail saisonnières, cela évite de payer pour une capacité inutilisée ; combiné à la mise à l'échelle automatique et aux options d'achat appropriées (On-Demand, Spot, Savings Plans), ce modèle permet une gestion rentable de la demande variable.  
C. Fonctionnalités d'audit intégrées d'AWS CloudTrail

#### Explications

AWS CloudTrail enregistre l'activité des API des comptes et sert à l'audit, aux enquêtes de sécurité et à la conformité. Bien qu'important pour la gouvernance, CloudTrail n'effectue pas de mise à l'échelle des ressources et n'influence pas les ajustements de capacité en cours d'exécution ; la surveillance et la mise à l'échelle sont assurées par des services tels qu'Amazon CloudWatch et Auto Scaling.  
**Votre sélection est correcte**  
D. Politiques de mise à l'échelle automatique

#### Explications

La mise à l'échelle automatique (groupes EC2 Auto Scaling, mise à l'échelle automatique des applications) ajuste dynamiquement la capacité des ressources en fonction de politiques définies, de métriques CloudWatch ou de planifications. Elle permet une augmentation ou une diminution automatique de la capacité pour répondre à la demande, minimisant ainsi le surdimensionnement et réduisant les coûts en période de faible demande, tout en répondant aux besoins de capacité lors des pics saisonniers.  
E. Enregistrement centralisé

#### Explications

La journalisation centralisée (par exemple, Amazon CloudWatch Logs, Amazon OpenSearch Service ou les journaux S3 agrégés) consolide les données opérationnelles à des fins d'analyse et de dépannage. Elle assure l'observabilité, mais ne provisionne ni ne supprime automatiquement les ressources de calcul en fonction des variations de charge de travail.  
Explication générale  
Les fonctionnalités les plus pertinentes sont la mise à l'échelle automatique et la facturation à l'usage. La mise à l'échelle automatique ajuste automatiquement la capacité (augmentation/diminution) en fonction de la demande, et la facturation à l'usage vous garantit de ne payer que les ressources consommées. Les autres options mentionnées (déploiement multirégional, CloudTrail, journalisation centralisée) concernent la disponibilité, l'audit et l'observabilité, mais pas l'élasticité automatique et économique face aux pics de charge saisonniers.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 28Correct  
Quel service de sécurité AWS protège les applications contre les attaques par déni de service distribué grâce à une détection permanente et à des mesures d'atténuation automatiques intégrées ?  
A. Inspecteur Amazon

#### Explications

Amazon Inspector est un service d'évaluation de sécurité automatisé qui analyse les applications et les instances EC2 afin de détecter les vulnérabilités et les écarts par rapport aux bonnes pratiques ; il ne fournit pas de détection des attaques DDoS au niveau du réseau ou du transport ni d'atténuation automatique en temps réel.  
B. Pare-feu d'applications Web AWS (AWS WAF)

#### Explications

AWS WAF est un pare-feu d'applications web de couche 7 qui filtre les requêtes HTTP/S à l'aide de règles et peut contribuer à atténuer certains types d'attaques par déni de service (DoS) lorsqu'il est configuré. Cependant, il ne s'agit pas du service de protection DDoS réseau/transport automatisé et permanent décrit dans la question. WAF est souvent utilisé conjointement avec AWS Shield pour une protection plus étendue.  
C. Équilibrage élastique de la charge (ELB)

#### Explications

L'équilibrage de charge élastique améliore la disponibilité et répartit le trafic entre les cibles, ce qui peut aider à absorber la charge, mais ELB n'est pas un service de protection contre les attaques DDoS et ne fournit pas la détection permanente et les mesures d'atténuation automatiques en ligne des attaques DDoS que propose Shield.  
**Votre réponse est correcte**  
D. Bouclier AWS

#### Explications

AWS Shield fournit une protection DDoS gérée avec une surveillance du trafic permanente et des mesures d'atténuation automatiques en ligne aux niveaux réseau et transport (Shield Standard pour les protections de base ; Shield Advanced pour une détection, une atténuation, une protection contre les coûts DDoS et un accès DRT améliorés), correspondant aux fonctionnalités mentionnées dans la question.  
Explication générale  
La question porte spécifiquement sur la détection permanente et l'atténuation automatique en temps réel des attaques DDoS. AWS Shield est le service managé conçu à cet effet (Shield Standard offre une protection permanente et automatique en périphérie du réseau ; Shield Advanced ajoute des fonctionnalités d'atténuation étendues, des rapports et l'assistance d'une équipe de réponse aux attaques DDoS). Les autres options sont des outils de sécurité ou de disponibilité (Inspector pour l'évaluation des vulnérabilités, WAF pour le filtrage de couche 7 et ELB pour la distribution du trafic), mais ils ne fournissent pas à eux seuls l'atténuation permanente et automatique des attaques DDoS décrite.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 29Correct  
Qui est responsable de la gestion des accès utilisateurs et des clés secrètes IAM conformément au modèle de responsabilité partagée d'AWS ?  
A. Les clés d'accès et les clés secrètes IAM sont statiques, il n'est donc pas nécessaire de les renouveler.

#### Explications

Incorrect. Les clés d'accès sont des identifiants client qui doivent être gérés activement ; les bonnes pratiques incluent une rotation régulière, la suppression des clés inutilisées et la préférence pour les identifiants à courte durée de vie (rôles IAM/STS) plutôt que de s'appuyer sur des secrets statiques à longue durée de vie.  
**Votre réponse est correcte**  
B. Le client est responsable de la rotation des clés.

#### Explications

Exactement. Dans le cadre du modèle de responsabilité partagée d'AWS, les clients gèrent les identités et les accès à leurs comptes. Cela inclut la création, le renouvellement, la désactivation et la suppression des clés d'accès utilisateur IAM, ainsi que la mise en œuvre de contrôles (principe du moindre privilège, authentification multifacteur, renouvellement automatique ou Secrets Manager) pour protéger ces informations d'identification.  
C. AWS fera tourner les clés chaque fois que cela sera nécessaire.

#### Explications

Incorrect. AWS n'effectue pas la rotation des clés d'accès IAM gérées par le client. AWS est responsable de la sécurité de l'infrastructure cloud, tandis que les clients sont responsables de la gestion de leurs propres identifiants et de l'automatisation de leur rotation, s'ils le souhaitent.  
D. L'équipe de support AWS effectuera une rotation des clés à la demande du client.

#### Explications

Incorrect. Le support AWS peut fournir des conseils, mais ne gère ni ne renouvelle les informations d'identification IAM d'un client ; la gestion de ces informations doit être effectuée par le propriétaire du compte ou automatisée par les outils du client.  
Explication générale  
This question tests understanding of the AWS shared responsibility model as it applies to identity and access management. AWS secures the infrastructure; customers are responsible for security in the cloud, which includes managing IAM users and their access keys (creation, rotation, deletion, and use of safer alternatives like IAM roles). The correct choice identifies the customer as responsible; the distractors incorrectly assign key rotation to AWS or imply keys are static.  
Domaine  
Domain 2: Security and Compliance  
Question 30Correct  
Which of the following is an AWS value proposition that describes a user’s ability to scale infrastructure based on demand?  
A. Speed of innovation

#### Explications

Incorrect. This option describes faster delivery of features and reduced time-to-market enabled by managed services and developer tooling (for example, AWS CodePipeline, AWS CodeDeploy, and managed databases). It does not specifically describe automatic adjustment of infrastructure capacity in response to demand.  
**Votre réponse est correcte**  
B. Resource elasticity

#### Explications

Correct. AWS provides the capability to automatically increase and decrease capacity to match workload demand (examples: Amazon EC2 Auto Scaling, Application Load Balancer, AWS Lambda concurrency scaling). This behavior lets customers optimize cost and performance by provisioning resources on-demand and releasing them when no longer needed.  
C. Decoupled architecture

#### Explications

Incorrect. This describes an architectural pattern that decouples components to improve resiliency and allow components to be developed and scaled independently (services such as Amazon SQS, SNS, and EventBridge). While decoupling can enable easier scaling of parts of a system, the term itself does not denote the automatic up/down adjustment of capacity based on demand.  
D. Global deployment

#### Explications

Incorrect. This option refers to deploying applications across multiple geographic locations (Regions and Availability Zones) to reduce latency and improve fault tolerance (examples: Amazon CloudFront, Route 53). Geographic distribution addresses latency and redundancy, but it does not, by itself, describe dynamic scaling of resources with demand.  
Explication générale  
The key concept tested is the cloud capability to automatically adjust infrastructure capacity to match workload demand. The correct choice describes that automatic up/down capacity adjustment (implemented in AWS via services like EC2 Auto Scaling, load balancers, and serverless autoscaling), which enables cost optimization and consistent performance. The distractors describe related but different benefits: faster innovation velocity, architectural decoupling, and global deployment — none of which specifically define automatic, demand-driven scaling.  
Domaine  
Domain 1: Cloud Concepts  
Question 31Correct  
A company has an uninterruptible application that runs on Amazon EC2 instances. The application constantly processes a backlog of files in an Amazon Simple Queue Service (Amazon SQS) queue. This usage is expected to continue to grow for years. What is the MOST cost-effective EC2 instance purchasing model to meet these requirements?  
A. Spot Instances

#### Explications

Les instances Spot offrent les remises les plus importantes en utilisant la capacité EC2 inutilisée, mais AWS peut les récupérer avec un préavis d'interruption court (généralement deux minutes). Ce comportement les rend inadaptées à une application conçue pour être non interruptible, à moins qu'une architecture supplémentaire (points de contrôle, réplication d'état) ne soit mise en place pour tolérer les arrêts.  
B. Instances à la demande

#### Explications

Les instances à la demande offrent une flexibilité totale sans engagement à long terme et sont facturées au tarif horaire/seconde le plus élevé. Elles conviennent aux charges de travail ponctuelles, imprévisibles ou sans engagement, mais sur plusieurs années d'utilisation stable et croissante, elles ne constituent pas l'option la plus rentable par rapport à une tarification avec engagement.  
**Votre réponse est correcte**  
C. Plans d'épargne

#### Explications

La tarification par engagement, qui permet de bénéficier de tarifs réduits en échange d'un engagement d'utilisation de 1 ou 3 ans, est la solution idéale pour une charge de travail pérenne et ininterrompue. Les plans d'économies (plans d'économies pour les instances de calcul et EC2) offrent des remises importantes par rapport à la facturation à la demande, tout en garantissant une grande flexibilité quant à la taille des instances, le système d'exploitation et (pour les plans d'économies pour les instances de calcul) les familles d'instances et les régions. Ils sont ainsi parfaitement adaptés à une consommation EC2 croissante et prévisible, sans risque d'interruption.  
D. Hôtes dévoués

#### Explications

Les serveurs dédiés sont destinés à répondre à des besoins spécifiques en matière de licences et de conformité et ne constituent pas la solution générale la plus rentable.  
Explication générale  
Pour une charge de travail EC2 ininterrompue avec une croissance prévisible à long terme, un modèle de tarification basé sur l'engagement offre le meilleur rapport coût-efficacité sans risque de résiliation d'instance. Les plans d'économies proposent des remises importantes en échange d'un engagement de 1 ou 3 ans, tout en conservant la flexibilité des attributs d'instance. Le modèle Spot est inadapté car il peut être interrompu ; le modèle à la demande est trop coûteux pour une utilisation soutenue sur plusieurs années ; les hôtes dédiés répondent à des besoins spécifiques en matière de licences et de conformité et ne constituent pas la solution générale la plus rentable.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 32Correct  
Une entreprise doit pouvoir développer, tester et déployer rapidement une application sur le cloud AWS. Quel avantage du cloud computing répond à ces exigences ?  
A. Cessez de deviner la capacité

#### Explications

Cet avantage réside dans la réduction de l'incertitude quant à la capacité requise grâce à l'utilisation d'une infrastructure évolutive et à la demande (par exemple, la mise à l'échelle automatique et l'équilibrage de charge élastique). Il améliore la rentabilité et la planification des performances, mais ne raccourcit pas directement les cycles de développement, de test ou de mise en production.  
B. Échanger les charges fixes contre des charges variables

#### Explications

Cela décrit le passage d'un modèle de dépenses d'investissement à un modèle de dépenses d'exploitation à la demande (modèles de tarification AWS tels que les plans à la demande, réservés et d'économies). Ce modèle accroît la flexibilité financière, mais n'est pas le principal facteur d'accélération du développement ou du déploiement d'applications.  
C. Réaliser des économies d'échelle

#### Explications

Cela fait référence aux réductions de coûts obtenues grâce à l'utilisation de l'infrastructure partagée d'un grand fournisseur de cloud et aux remises sur volume. Les économies d'échelle diminuent les coûts unitaires, mais ne permettent pas, à elles seules, d'assurer le provisionnement rapide, l'automatisation et les outils de développement nécessaires pour accélérer les processus de compilation, de test et de mise en production.  
**Votre réponse est correcte**  
D. Augmenter la vitesse et l'agilité

#### Explications

Cloud platforms provide on-demand provisioning, elasticity, managed platform services, and DevOps automation that directly reduce lead time for features. Examples include quickly provisioning compute and storage (Amazon EC2, Amazon S3), using managed runtimes and orchestration (AWS Elastic Beanstalk, Amazon RDS, Amazon EKS), serverless options (AWS Lambda), and CI/CD and infrastructure-as-code tools (AWS CodePipeline/CodeBuild, AWS CloudFormation, AWS CDK). These capabilities enable fast environment creation, automated testing, and rapid deployment.  
Explication générale  
The question targets cloud agility: the ability to rapidly provision resources and automate delivery pipelines so teams can develop, test, and launch applications faster. While cost-related benefits (capacity planning, pay-as-you-go, economies of scale) are real advantages, the core benefit that meets the requirement is the increased speed and agility enabled by on-demand services, managed platforms, serverless options, and DevOps automation.  
Domaine  
Domain 1: Cloud Concepts  
Question 33Correct  
Which AWS service or feature gives users the ability to connect VPCs and on-premises networks to a central hub?  
A. Virtual private gateway

#### Explications

A virtual private gateway is the AWS side of a Site-to-Site VPN connection and attaches to a single VPC to terminate VPN tunnels. It is not designed to act as a scalable central routing hub for multiple VPCs and on-premises networks; connecting many VPCs with virtual private gateways would require multiple point-to-point VPNs and complex routing.  
**Votre réponse est correcte**  
B. AWS Transit Gateway

#### Explications

AWS Transit Gateway provides a regional hub-and-spoke connectivity model that supports VPC attachments, Site-to-Site VPN connections, and integration with Direct Connect gateways. It centralizes routing through TGW route tables, scales to thousands of attachments, and simplifies management by replacing many point-to-point links—making it the appropriate service for a central hub.  
C. Internet gateway

#### Explications

An internet gateway enables instances in a VPC to communicate with the public internet (and vice versa). It does not provide connectivity to on-premises networks or inter-VPC hub functionality, so it cannot serve as a central hub for VPCs and on-premises networks.  
D. Customer gateway

#### Explications

A customer gateway is a representation of the customer’s on-premises VPN device (or its static IP) within AWS and is used as an endpoint for VPN connections. It functions as the customer-side endpoint for a VPN but does not provide hub-style routing or inter-VPC connectivity.  
Explication générale  
The question tests knowledge of AWS networking services for centralizing connectivity. The Transit Gateway is the correct choice because it provides a scalable, managed hub that connects multiple VPCs and on-premises networks (via VPN or Direct Connect) and centralizes routing via TGW route tables. The other options are endpoint or internet-focused components: virtual private and customer gateways are used for VPN endpoints for specific VPCs or on-prem devices, and an internet gateway only enables internet access.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 34Correct  
Quel service AWS est conçu pour les utilisateurs exécutant des charges de travail incluant une base de données NoSQL ?  
A. Amazon RDS

#### Explications

Amazon RDS est un service de base de données relationnelle gérée qui impose des schémas, des transactions et des modèles d'accès basés sur SQL (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB). Ces caractéristiques relationnelles le rendent mal adapté aux charges de travail sans schéma, à haut débit et de type clé-valeur ou document, pour lesquelles les bases de données NoSQL sont conçues.  
B. Amazon S3

#### Explications

Amazon S3 est un service de stockage d'objets pour les fichiers et les objets binaires/textuels volumineux, optimisé pour la durabilité et l'évolutivité. Il ne propose pas les fonctionnalités de lecture/écriture indexée à faible latence, d'index secondaires ni de requêtes/mises à jour attendues d'une base de données NoSQL utilisée pour les charges de travail opérationnelles.  
C. Amazon Redshift

#### Explications

Amazon Redshift est un entrepôt de données en colonnes, à l'échelle du pétaoctet, conçu pour les requêtes analytiques (OLAP) et la génération de rapports. Sa conception optimise l'analyse à grande échelle plutôt que les opérations de lecture/écriture à faible latence et haute concurrence typiques des bases de données opérationnelles NoSQL.  
**Votre réponse est correcte**  
D. Amazon DynamoDB

#### Explications

Amazon DynamoDB est une base de données NoSQL entièrement gérée et conçue à cet effet, qui prend en charge les modèles de données clé-valeur et document, une latence de quelques millisecondes, une mise à l'échelle automatique (capacité à la demande ou provisionnée), des tables globales et des fonctionnalités telles que DAX, les transactions, le chiffrement et la restauration à un point précis dans le temps, ce qui en fait le choix idéal pour les charges de travail NoSQL.  
Explication générale  
Cette question vise à évaluer la correspondance entre les types de charges de travail et le service de données AWS approprié. Pour les charges de travail opérationnelles sans schéma, à haut débit et à faible latence, un service NoSQL managé est nécessaire ; Amazon DynamoDB répond à ces besoins. Les autres services ciblent des problématiques différentes : RDS pour les bases de données relationnelles (SQL) transactionnelles, S3 pour le stockage d'objets et Redshift pour l'entreposage de données analytiques. Ils ne constituent donc pas des alternatives adéquates à une base de données NoSQL.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 35Correct  
Une entreprise prévoit de migrer ses sauvegardes de données vers le cloud AWS. Elle doit remplacer son stockage sur site par un stockage cloud avec cache local. Quel service AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Passerelle de stockage AWS

#### Explications

Fournit une interface de stockage hybride, basée sur le cloud et dotée d'un cache local. Storage Gateway propose plusieurs types de passerelles (volume mis en cache, fichier et bande) qui conservent les données fréquemment consultées sur site pour une faible latence, tout en stockant l'ensemble de données principal dans AWS (snapshots S3/Glacier ou EBS). Les modes de passerelle volume mis en cache et bande sont couramment utilisés pour remplacer le stockage de sauvegarde sur site par un stockage cloud qui maintient un cache local.  
B. AWS Snowcone

#### Explications

Snowcone est un petit appareil robuste de la gamme AWS Snow dédié au calcul en périphérie et au transfert de données hors ligne. Il est conçu pour la collecte et le transport physique de données déconnectées ou distantes, et non pour fournir un cache local synchronisé en continu et basé sur le cloud, remplaçant le stockage sur site pour les flux de travail de sauvegarde continus.  
C. Sauvegarde AWS

#### Explications

AWS Backup centralizes and automates backups across AWS services and manages backup policies, lifecycle, and retention. It does not present a local on-premises cache or act as a hybrid storage gateway — it orchestrates backups into AWS storage services rather than exposing a cached local storage interface.  
D. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a fully managed, scalable NFS file system accessible by EC2 (and other compute) in the cloud. It does not provide an on-premises local caching appliance or hybrid cached volumes; using EFS from on-prem requires other networking/transfer solutions and does not fulfill the local-cache replacement requirement.  
Explication générale  
The requirement is for cloud-backed storage that keeps a local cache so on-premises systems can continue low-latency access while the primary dataset is stored in AWS. Storage Gateway is purpose-built for that hybrid scenario (Cached Volume/File/Tape modes integrating with S3/Glacier and snapshots). The other options either manage backups (AWS Backup), provide physical data transfer/edge compute (Snowcone), or are cloud-only file systems without an on-premises cache (EFS).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 36Correct  
How does the AWS Cloud help companies build agility into their processes and cloud infrastructure?  
A. Companies can avoid provisioning too much capacity when they do not know how much capacity is required.

#### Explications

Incorrect — this option describes capacity and cost-management capabilities. AWS features such as Amazon EC2 Auto Scaling and on‑demand instances help match capacity to demand and reduce waste, but these are mechanisms for scalability and cost control rather than the primary enabler of organizational agility (rapid experimentation and process iteration).  
B. Companies can expand into new geographic regions.

#### Explications

Incorrect — this refers to AWS’s global infrastructure (Regions and Availability Zones), which supports lower latency, data locality, and geographic expansion. Those capabilities enable reach and resiliency but do not directly drive faster innovation or iterative development practices that define agility.  
**Votre réponse est correcte**  
C. Companies can access a range of technologies to experiment and innovate quickly.

#### Explications

Correct — AWS provides a broad catalog of managed services (compute, storage, databases, analytics, AI/ML, serverless, CI/CD and developer tools) plus infrastructure-as-code (AWS CloudFormation, AWS CDK) and self-service provisioning. Together these reduce setup and operational overhead, enable ephemeral test environments, and let teams prototype and iterate rapidly — the core elements of agility.  
D. Companies can pay for IT resources only when they use the resources.

#### Explications

Incorrect — pay-as-you-go pricing (on-demand billing) increases financial flexibility and lowers capital expense, which supports scalability and cost efficiency. However, pricing model alone does not create faster development cycles, rapid experimentation, or the tooling/process changes associated with agility.  
Explication générale  
Cette question évalue la compréhension du fait que l'agilité dans le cloud repose sur un accès rapide à un large éventail de services gérés et d'outils de développement permettant un prototypage rapide, l'itération et l'automatisation. Bien que d'autres avantages d'AWS (capacité dynamique, facturation à l'usage et régions mondiales) favorisent l'évolutivité, la maîtrise des coûts et la couverture géographique, le principal facteur d'agilité organisationnelle est la capacité d'expérimenter et de déployer rapidement grâce au vaste catalogue de services AWS et aux fonctionnalités d'infrastructure en libre-service.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 37Correct  
Une entreprise a besoin d'un pare-feu pour contrôler les connexions réseau entrantes et sortantes d'une instance Amazon EC2 spécifique. Ce pare-feu ne doit pas contrôler les connexions réseau sortantes et entrantes d'autres instances situées dans le même sous-réseau. Quel service ou fonctionnalité AWS l'entreprise peut-elle utiliser pour répondre à ces exigences ?  
A. ACL réseau

#### Explications

Les listes de contrôle d'accès réseau (ACL) sont des listes de contrôle d'accès sans état qui s'appliquent au niveau du sous-réseau. Elles évaluent le trafic selon l'ordre des règles et exigent des règles explicites pour le trafic de retour ; elles affectent donc toutes les instances du sous-réseau et ne peuvent pas fournir de pare-feu dynamique par instance.  
B. AWS WAF

#### Explications

AWS WAF est un pare-feu applicatif web (HTTP/HTTPS) intégré à des services tels que CloudFront, ALB et API Gateway. Il inspecte les requêtes web afin de détecter les menaces au niveau applicatif (par exemple, les injections SQL et les attaques XSS) et ne contrôle pas les connexions réseau au niveau IP/port vers une instance EC2 individuelle.  
C. Tableau de routage

#### Explications

Les tables de routage déterminent le routage IP pour un sous-réseau (quelle passerelle ou cible reçoit le trafic) et n'effectuent pas de contrôle d'accès ni de filtrage des connexions entrantes/sortantes vers des instances individuelles ; elles concernent la destination des paquets, et non les règles du pare-feu.  
**Votre réponse est correcte**  
D. Groupe de sécurité

#### Explications

Les groupes de sécurité sont des pare-feu virtuels avec état, appliqués aux interfaces réseau (ENI) et gérés au niveau de l'instance. Ils permettent de définir des règles de trafic entrant et sortant (protocole, port, source/destination) pour une instance spécifique sans affecter les autres instances du même sous-réseau ; le trafic de retour est automatiquement autorisé grâce à la gestion de l'état.  
Explication générale  
Il est nécessaire de disposer d'un pare-feu par instance qui contrôle le trafic vers une seule instance EC2 sans impacter les autres instances du même sous-réseau. Les groupes de sécurité offrent un contrôle d'accès dynamique au niveau de l'instance (associé à l'interface réseau de l'instance) et prennent en charge des règles d'autorisation granulaires pour les ports, les protocoles et les plages d'adresses IP. À l'inverse, les listes de contrôle d'accès réseau (ACL) et les tables de routage fonctionnent au niveau du sous-réseau/routage et affectent tous les membres du sous-réseau, tandis que le pare-feu applicatif AWS (AWS WAF) est conçu pour la protection HTTP/HTTPS au niveau applicatif et non pour le contrôle d'accès général au niveau du réseau.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 38Correct  
Quelle action permettra d'améliorer la sécurité dans le cloud AWS ?  
A. Activer l'accès programmatique pour tous les utilisateurs IAM.

#### Explications

L'accès programmatique aux API/CLI s'effectue par l'émission de clés d'accès permanentes. Son activation généralisée augmente considérablement le nombre d'identifiants à gérer et la surface d'attaque ; il est donc recommandé d'appliquer le principe du moindre privilège, d'exiger l'authentification multifacteur (MFA) lorsque cela est pertinent et de privilégier les identifiants temporaires (rôles) plutôt que l'émission de clés d'accès permanentes pour chaque utilisateur.  
B. Use IAM users instead of IAM roles to delegate permissions.

#### Explications

IAM roles provide temporary, short-lived credentials (via STS) and are the recommended mechanism for delegation, cross-account access, and granting permissions to AWS resources (including EC2 instance profiles). Creating many IAM users with long-term credentials increases risk and operational overhead.  
**Votre réponse est correcte**  
C. Rotate access keys on a reoccurring basis.

#### Explications

Regularly rotating access keys reduces the time window during which a compromised key can be used and is an AWS security best practice when long-term keys must exist. Rotation should be automated, accompanied by credential inventories, and combined with using temporary credentials (IAM roles) and least-privilege policies.  
D. Use inline policies instead of customer managed policies.

#### Explications

Inline policies are embedded for a single principal and are harder to manage, reuse, and audit compared with customer-managed policies. They do not inherently increase security and can lead to inconsistent or hard-to-track permissions; customer-managed or AWS-managed policies are preferred for maintainability and clearer access control.  
Explication générale  
This question tests credential management and least-privilege principles. The best actionable step among the choices is to rotate access keys to reduce exposure if keys are compromised. However, the broader AWS best practice is to avoid long-term access keys when possible by using IAM roles and temporary credentials; the incorrect options either increase credential exposure or reduce manageability.  
Domaine  
Domain 2: Security and Compliance  
Question 39Correct  
Which tool should a developer use to integrate AWS service features directly into an application?  
**Votre réponse est correcte**  
A. AWS Software Development Kit

#### Explications

The AWS SDK provides language-specific libraries and APIs (for Java, Python, JavaScript/Node.js, .NET, Go, Ruby, PHP, etc.) that abstract direct HTTP calls to AWS services. It handles request signing with credentials, retries, error handling, pagination, and exposes high-level service clients and data models so application code can call and consume AWS service features directly.  
B. AWS CodeDeploy

#### Explications

AWS CodeDeploy is a deployment automation service for rolling out application revisions to compute resources (EC2, on‑premises servers, Lambda). It orchestrates deployments and rollbacks but does not provide client libraries or in‑process APIs for embedding AWS service features inside application code.  
C. AWS Lambda

#### Explications

AWS Lambda is a serverless compute service that runs code in response to events (triggers from S3, API Gateway, etc.). While Lambda functions can call AWS services (typically using an SDK), Lambda itself is a compute/runtime environment, not the library/tool used to integrate AWS service features directly into application source code.  
D. AWS Batch

#### Explications

AWS Batch manages, schedules, and runs batch computing jobs on managed compute resources and is intended for large-scale, compute‑intensive workloads. It is not a client library or API surface for integrating AWS service features into application code.  
Explication générale  
Cette question évalue comment les développeurs intègrent les fonctionnalités AWS dans leurs applications. Les kits de développement logiciel (SDK) spécifiques au langage sont l'outil approprié, car ils fournissent des API, la signature des requêtes, la gestion des nouvelles tentatives et des abstractions client permettant au code applicatif d'appeler directement les services AWS. Les autres options sont les services de plateforme ou d'orchestration (déploiement ou calcul) et ne fonctionnent pas comme des bibliothèques intégrées pour l'intégration des fonctionnalités des services AWS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 40Correct  
Une entreprise souhaite protéger ses informations, ses systèmes et ses actifs sur le cloud AWS tout en réalisant des évaluations et des mesures d'atténuation des risques. Quel pilier du cadre AWS Well-Architected est pris en charge par ces objectifs ?  
A. Fiabilité

#### Explications

Ce pilier traite de la disponibilité du système, de la tolérance aux pannes, de la capacité de récupération et de la résilience des charges de travail (par exemple : déploiements multi-AZ, récupération automatisée, contrôles d’intégrité et gestion des capacités). Ces aspects contribuent à la disponibilité et à la reprise après incident, mais ne concernent pas principalement la protection des données, l’évaluation des risques ni la mise en œuvre de mesures de sécurité.  
**Votre réponse est correcte**  
B. Sécurité

#### Explications

Ce pilier vise à protéger la confidentialité, l'intégrité et la disponibilité des informations et des systèmes grâce à la gestion des identités et des accès, aux contrôles de détection et de prévention, à la protection de l'infrastructure, à la protection des données et à la réponse aux incidents. Les contrôles AWS généralement utilisés pour atteindre ces objectifs comprennent IAM, KMS, CloudTrail, AWS Config, AWS Shield/WAF, la journalisation et la surveillance, le chiffrement et la réponse automatisée aux incidents ; autant d'éléments qui contribuent à l'évaluation et à l'atténuation des risques.  
C. Excellence opérationnelle

#### Explications

Ce pilier est axé sur les processus opérationnels : procédures, manuels d’exploitation, gestion des changements et des incidents, amélioration continue et mesure des indicateurs de performance. Il aide les équipes à exploiter et à faire évoluer les systèmes de manière fiable, mais son principal objectif est la santé des processus et des opérations plutôt que l’évaluation des risques et les contrôles de sécurité.  
D. Efficacité de la performance

#### Explications

Ce pilier concerne la sélection et l'utilisation efficace des ressources de calcul, de stockage et de réseau (exemples de techniques : dimensionnement optimal des instances, mise en cache, utilisation d'architectures sans serveur et choix de moteurs de base de données appropriés). Son objectif est d'optimiser les performances et les coûts, et non d'identifier et d'atténuer les risques de sécurité ou de protéger les actifs.  
Explication générale  
Le scénario décrit la protection des informations, des systèmes et des ressources du cloud, ainsi que l'évaluation et la réduction des risques – des responsabilités essentielles du pilier Sécurité. Ce pilier définit les objectifs de sécurité (confidentialité, intégrité, disponibilité) et prescrit les contrôles d'identité et d'accès, la journalisation et la surveillance, la protection des données, la protection de l'infrastructure et la réponse aux incidents. Les autres piliers (fiabilité, excellence opérationnelle, efficacité des performances) traitent respectivement de la disponibilité, des processus opérationnels et de l'optimisation des ressources, mais ne sont pas axés principalement sur la sécurité et la gestion des risques.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 41Correct  
Quel service ou fonctionnalité AWS permet aux utilisateurs de provisionner une infrastructure AWS par programmation ?  
**Votre réponse est correcte**  
A. Kit de développement cloud AWS (AWS CDK)

#### Explications

AWS CDK is an infrastructure-as-code framework that lets developers author infrastructure using familiar programming languages, synthesizes those definitions into AWS CloudFormation templates, and uses CloudFormation to deploy and manage the resources. This enables repeatable, programmatic provisioning, integration with CI/CD, and use of higher-level constructs to model infrastructure.  
B. Amazon CodeGuru

#### Explications

Amazon CodeGuru is a developer tool for automated code reviews and runtime application profiling. It provides recommendations to improve code quality and performance but does not create, deploy, or manage AWS infrastructure resources.  
C. AWS Config

#### Explications

AWS Config is a resource inventory, configuration tracking, and compliance auditing service. It records and evaluates resource configurations over time for compliance and troubleshooting; it does not provision resources or define infrastructure.  
D. AWS CodeCommit

#### Explications

AWS CodeCommit is a managed, secure Git-based source control service for storing and versioning source code. It can host IaC code repositories used by provisioning tools, but it does not itself provision or deploy infrastructure.  
Explication générale  
This question tests knowledge of infrastructure-as-code and programmatic provisioning. The AWS CDK is the correct choice because it enables developers to define infrastructure in code, synthesize CloudFormation templates, and deploy resources programmatically. The other options are developer tooling or configuration/audit services (CodeGuru, CodeCommit, AWS Config) that assist with code quality, source control, or compliance but do not perform provisioning.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 42Correct  
Which AWS service uses AWS Compute Optimizer to provide sizing recommendations based on workload metrics?  
**Votre réponse est correcte**  
A. Amazon EC2

#### Explications

Compute Optimizer ingests historical Amazon CloudWatch metrics and applies machine-learning models to produce right-sizing recommendations for compute resources. For instance-level workloads it evaluates CPU, network, and storage utilization and recommends optimal instance families and sizes to improve performance and reduce cost, along with projected savings and confidence levels.  
B. Amazon RDS

#### Explications

Incorrect. RDS does not rely on Compute Optimizer for automated instance-sizing recommendations. Amazon RDS provides its own monitoring and diagnostic tools (CloudWatch, Enhanced Monitoring, Performance Insights) and RDS console recommendations for tuning database instances and storage.  
C. Amazon Lightsail

#### Explications

Incorrect. Lightsail is a simplified VPS-style offering with fixed plans and does not integrate with Compute Optimizer’s ML-based right-sizing; it is intended for straightforward deployments rather than detailed instance-family optimization.  
D. AWS Step Functions

#### Explications

Incorrect. Step Functions is a serverless orchestration service that coordinates other services; it does not represent an EC2-like compute resource and therefore is not a target for Compute Optimizer sizing recommendations.  
Explication générale  
AWS Compute Optimizer analyse les données d'utilisation de CloudWatch et utilise l'apprentissage automatique pour générer des recommandations de dimensionnement optimales pour les ressources de calcul et de stockage. Ce service est particulièrement adapté à cette problématique en ce qui concerne le dimensionnement au niveau de l'instance ; les recommandations relatives à la famille et à la taille des instances EC2 constituent donc le choix idéal. Les autres options disposent soit de leurs propres mécanismes de surveillance et de recommandation (RDS), soit sont des offres simplifiées sans dimensionnement précis (Lightsail), soit sont des services d'orchestration qui ne sont pas ciblés par Compute Optimizer (Step Functions).  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 43Correct  
Une entreprise de commerce électronique prévoit de migrer les données de son centre de données vers le cloud AWS afin de prendre en charge des modèles d'utilisation très dynamiques. Quels avantages rendent le cloud AWS rentable pour la migration de ce type de données ? (Choisissez deux réponses.)  
A. Fiabilité

#### Explications

Ce document décrit la conception d'AWS pour la tolérance aux pannes et la disponibilité continue (par exemple, grâce à l'utilisation de plusieurs zones et régions de disponibilité). Cet avantage améliore la disponibilité et la résilience, mais ne réduit pas à lui seul les coûts des charges de travail variables dans le temps, car il privilégie la continuité plutôt que la capacité dynamique ou les modèles de facturation.  
B. Sécurité

#### Explications

Cela concerne les mécanismes de protection tels que la gestion des identités et des accès (IAM), le chiffrement et les contrôles réseau. La sécurité est essentielle au bon fonctionnement et à la conformité, mais elle ne permet pas de réaliser directement des économies pour les charges de travail très variables.  
**Votre sélection est correcte**  
C. Élasticité

#### Explications

Ce concept décrit la capacité d'ajuster automatiquement la capacité en fonction de la demande (par exemple, à l'aide des groupes Auto Scaling, de la mise à l'échelle automatique d'AWS Lambda et des équilibreurs de charge). L'adaptation de la capacité à la charge de travail en temps réel évite le surdimensionnement et réduit les dépenses inutiles en cas de baisse de la demande, ce qui en fait un mécanisme d'optimisation des coûts essentiel pour les charges de travail dynamiques.  
**Votre sélection est correcte**  
D. Ressource à paiement à l'utilisation

#### Explications

Cela fait référence à la facturation à la consommation d'AWS (par exemple, la tarification à la demande et à la seconde pour le calcul, et la facturation par requête pour les services sans serveur). Le fait de ne payer que les ressources réellement consommées permet d'éviter les coûts fixes liés à la capacité inutilisée et d'aligner les dépenses sur les fluctuations de la charge de travail.  
E. Haute disponibilité

#### Explications

Il s'agit de concevoir des systèmes pour qu'ils restent disponibles en cas de défaillance de composants (par exemple, les déploiements multi-AZ). La haute disponibilité accroît la résilience, mais peut augmenter la consommation de ressources (et les coûts) et ne constitue pas le principal mécanisme de réduction des coûts pour les charges de travail variables.  
Explication générale  
Cette question évalue la compréhension des facteurs de coût du cloud pour les charges de travail variables. L'association de la mise à l'échelle automatique pour adapter la capacité à la demande et de la facturation à l'usage rend AWS rentable pour les charges de travail très dynamiques : la mise à l'échelle réduit le gaspillage d'infrastructure et la facturation à l'usage évite de payer pour des ressources inactives. Les autres avantages mentionnés (fiabilité, sécurité, haute disponibilité) sont importants pour l'exploitation et la conformité, mais n'expliquent pas directement les principaux avantages de coût liés à une demande fluctuante.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 44Correct  
Une entreprise envisage de migrer vers le cloud AWS. Elle doit comprendre l'utilisation et la configuration de son infrastructure sur site actuelle. Elle ne souhaite pas encore répliquer ses charges de travail sur AWS. Quel service ou outil AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Service de découverte d'applications AWS

#### Explications

Collecte des données détaillées d'inventaire et de configuration sur site (avec ou sans agent), capture l'utilisation des serveurs et les cartographies des dépendances applicatives, et exporte les résultats vers AWS Migration Hub pour la planification. Conçu pour l'évaluation et l'analyse de préparation à la migration sans réplication.  
B. Service de migration d'applications AWS

#### Explications

Ce service (Application Migration Service / MGN) est axé sur les migrations lift-and-shift : il effectue une réplication continue au niveau bloc et orchestre la bascule vers EC2. Son objectif principal est la réplication/migration, et non une simple évaluation de découverte.  
C. Usine de migration vers le cloud

#### Explications

Il ne s'agit pas d'un service géré par AWS. « Cloud Migration Factory » désigne un programme/une méthodologie de migration (un ensemble de processus, d'outils et de pratiques) plutôt qu'un outil de découverte AWS spécifique ; par conséquent, il ne fournit pas les données automatisées d'inventaire et de dépendances ciblées requises ici.  
D. Famille de transfert AWS

#### Explications

Fournit un transfert de fichiers entièrement géré (SFTP/FTPS/FTP) vers les points de terminaison de stockage AWS (S3/EFS) et n'effectue pas la découverte de l'environnement, la collecte d'inventaire ou la cartographie des dépendances nécessaires à l'évaluation de la migration.  
Explication générale  
Cette question vise à distinguer les outils de découverte/d'évaluation des services de migration/transfert. La bonne réponse est le service qui effectue la collecte d'inventaire et la cartographie des dépendances pour la planification de la migration sans répliquer les charges de travail. Les autres options effectuent soit une réplication/migration proprement dite, soit sont des services de transfert de fichiers gérés sans lien avec la question, soit relèvent de méthodologies de migration non AWS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 45Correct  
Une entreprise a créé une instance Amazon EC2. Elle souhaite contrôler le trafic réseau entrant et sortant au niveau de cette instance. Quelle ressource ou quel service AWS répond à ce besoin ?  
A. Bouclier AWS

#### Explications

AWS Shield est un service de protection DDoS géré (Shield Standard et Shield Advanced) qui atténue les attaques par déni de service distribué au niveau du réseau et des applications. Il ne propose pas de pare-feu par instance ni de règles d'autorisation/de blocage du trafic entrant/sortant sur les instances EC2 individuelles.  
**Votre réponse est correcte**  
B. Groupes de sécurité

#### Explications

Les groupes de sécurité constituent le mécanisme de contrôle d'accès réseau au niveau de l'instance pour EC2. Ce sont des pare-feu virtuels avec état, associés aux interfaces réseau (ENI), qui appliquent des règles d'autorisation uniquement pour le trafic entrant et sortant ; le trafic de retour des connexions autorisées est automatiquement autorisé. Cela permet un contrôle précis du trafic vers et depuis des instances spécifiques.  
C. Analyseur d'accès réseau

#### Explications

L'Analyseur d'accès réseau (VPC Reachability/Network Access Analyzer) est un outil de diagnostic et de vérification qui analyse les configurations réseau et l'accessibilité entre les ressources. Il permet d'identifier les chemins d'accès potentiels et les erreurs de configuration, mais ne contrôle ni n'applique de contrôle au trafic réseau en temps réel sur les instances.  
D. Points de terminaison VPC

#### Explications

Les points de terminaison VPC (passerelle et interface) assurent une connectivité privée entre un VPC et les services AWS compatibles, sans transiter par Internet. Ils gèrent le routage vers les services, et non le filtrage du trafic ou les règles de pare-feu par instance ; ils ne répondent donc pas aux exigences de contrôle du trafic au niveau de l’instance.  
Explication générale  
Cette question évalue votre connaissance des méthodes de contrôle au niveau du réseau pour une instance EC2. Les groupes de sécurité constituent la bonne réponse, car il s'agit du mécanisme AWS qui applique des règles d'autorisation/de refus dynamiques au niveau de l'instance et de l'interface réseau. Les autres options concernent la protection contre les attaques DDoS (Shield), la connectivité et les diagnostics (points de terminaison VPC, Network Access Analyzer) et ne permettent pas l'application d'un pare-feu par instance.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 46Correct  
Un ingénieur réseau doit concevoir une architecture de cloud hybride connectant des réseaux sur site au cloud AWS via AWS Direct Connect. L'entreprise dispose de quelques VPC dans une seule région AWS et prévoit d'en déployer plusieurs centaines à terme. Quel service ou fonctionnalité AWS l'ingénieur doit-il utiliser pour simplifier et faire évoluer cette connectivité à mesure que le nombre de VPC augmente ?  
A. Points de terminaison VPC

#### Explications

Les points de terminaison VPC (passerelle et interface) offrent un accès privé et spécifique à un service depuis un seul VPC vers les services AWS pris en charge, sans routage Internet. Ils ne permettent pas la connectivité entre VPC ni le transit sur site et ne résolvent donc pas le problème de mise à l'échelle lié à la connexion de centaines de VPC à un réseau sur site.  
**Votre réponse est correcte**  
B. Passerelle de transit AWS

#### Explications

Transit Gateway centralise le routage entre de nombreux VPC et réseaux sur site. Il prend en charge des milliers de connexions VPC, des tables de routage centralisées et l'intégration avec AWS Direct Connect (via une passerelle Direct Connect ou Transit Gateway Connect) afin de simplifier et de faire évoluer la connectivité hybride tout en évitant les configurations d'appairage complexes de type « plusieurs à plusieurs ».  
C. Route 53 d'Amazonie

#### Explications

Amazon Route 53 est un service DNS et de routage du trafic permettant la résolution de noms de domaine, les contrôles d'intégrité et les politiques de routage globales. Il ne fournit pas de connectivité réseau de couche 3 entre les VPC ni entre les réseaux sur site et les VPC.  
D. AWS Secrets Manager

#### Explications

AWS Secrets Manager est un service de gestion des secrets permettant de stocker et de renouveler les informations d'identification et les clés API. Il n'intervient pas dans la connectivité réseau ni dans la connexion des VPC aux réseaux sur site.  
Explication générale  
Ce scénario nécessite une plateforme évolutive pour interconnecter de nombreux VPC à des réseaux sur site via Direct Connect. AWS Transit Gateway est conçu à cet effet : routage centralisé, capacité de connexion élevée et intégration Direct Connect. C'est donc le choix idéal. Les autres options sont indépendantes : les points de terminaison VPC servent à l'accès privé aux services depuis un seul VPC, Route 53 assure la gestion DNS et Secrets Manager gère les informations d'identification.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 47Correct  
Une entreprise souhaite surveiller et bloquer les requêtes HTTP et HTTPS malveillantes reçues par ses distributions Amazon CloudFront. Quel service AWS doit-elle utiliser pour répondre à ces exigences ?  
A. Amazon GuardDuty

#### Explications

GuardDuty analyse les journaux AWS (CloudTrail, journaux de flux VPC, DNS) pour identifier les menaces et prend en charge les alertes et les réponses automatisées, mais il ne s'insère pas dans le chemin de la requête et ne fournit pas de filtrage au niveau de la requête pour bloquer le trafic HTTP/HTTPS sur une distribution CloudFront.  
B. Inspecteur Amazon

#### Explications

Inspector effectue des évaluations de sécurité automatisées des instances EC2, des images de conteneurs et des applications qui y sont exécutées afin de détecter les vulnérabilités et les écarts par rapport aux bonnes pratiques ; il ne s’agit pas d’un service d’inspection ou de blocage du trafic Web et il ne peut pas être connecté à CloudFront pour filtrer les requêtes.  
**Votre réponse est correcte**  
C. AWS WAF

#### Explications

AWS WAF est un pare-feu d'applications Web qui peut être associé directement aux distributions CloudFront pour inspecter les requêtes HTTP/HTTPS à l'aide de groupes de règles gérés, de règles personnalisées et de règles basées sur le débit ; il prend en charge le blocage, l'autorisation ou le comptage des requêtes et s'intègre à la journalisation et à AWS Firewall Manager pour une gestion centralisée, ce qui en fait le service idéal pour surveiller et bloquer les requêtes Web malveillantes.  
D. Détective Amazonien

#### Explications

Amazon Detective collecte et visualise les données de sécurité pour aider à enquêter sur les problèmes de sécurité et à en déterminer la cause profonde ; il s’agit d’un outil d’investigation/d’analyse qui n’applique pas de contrôles de trafic ni ne bloque les requêtes au niveau de la distribution.  
Explication générale  
Pour surveiller et bloquer les requêtes HTTP/HTTPS malveillantes sur CloudFront, un service de contrôle au niveau des requêtes est nécessaire. AWS WAF est spécifiquement conçu pour s'intégrer à CloudFront et appliquer une inspection et un blocage des requêtes web basés sur des règles. Les autres options (GuardDuty, Inspector, Detective) offrent des fonctionnalités de détection, d'évaluation ou d'investigation, mais ne prennent pas en charge le filtrage ou le blocage des requêtes en temps réel pour CloudFront.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 48Correct  
Une entreprise dispose d'un plan AWS Business Support. Elle a besoin d'accéder à l'équipe de réponse aux attaques DDoS (DRT) d'AWS pour atténuer les risques liés aux attaques DDoS. Quel service ou ressource AWS doit-elle utiliser pour répondre à ce besoin ?  
A. Norme AWS Shield

#### Explications

Shield Standard offre une protection DDoS automatique de base au niveau réseau et transport sans frais supplémentaires, mais n'inclut pas de fonctionnalités d'atténuation avancées, de diagnostics d'attaque détaillés, de protection des coûts ni la possibilité de solliciter l'équipe de réponse DDoS (DRT) d'AWS. Par conséquent, elle ne répond pas aux exigences.  
B. Support AWS pour entreprises

#### Explications

Le plan de support Entreprise offre une assistance technique renforcée, un gestionnaire de compte technique (TAM) et des délais de réponse plus courts. Toutefois, un plan de support seul ne garantit pas la protection contre les attaques DDoS ni l'accès direct à l'équipe de réponse aux incidents (DRT). L'interaction directe avec la DRT est une fonctionnalité proposée par l'abonnement AWS Shield Advanced (les plans de support sont complémentaires, mais ne constituent pas le principal moyen d'accès à la DRT).  
C. AWS WAF

#### Explications

AWS WAF est un pare-feu de couche application (HTTP/S) qui applique des règles personnalisées pour bloquer les requêtes malveillantes et réduire les attaques de couche application. Il n'offre pas de protection DDoS de couche réseau à grande échelle et ne donne pas accès à l'équipe de réponse DDoS d'AWS ; il ne répond donc pas à la question.  
**Votre réponse est correcte**  
D. AWS Shield Advanced

#### Explications

A subscription to AWS Shield Advanced includes enhanced DDoS protections (additional detection and mitigation, attack diagnostics, and cost protection) and provides the ability to engage the AWS DDoS Response Team (DRT) for incident assistance and mitigation. This is why Shield Advanced is the correct choice for obtaining DRT support.  
Explication générale  
Access to the AWS DDoS Response Team is provided as part of the AWS Shield Advanced offering, which adds advanced detection, mitigation controls, attack diagnostics, and DRT engagement. Other options are either basic protection (Shield Standard), an application-layer firewall (WAF), or a support plan (Enterprise), none of which by themselves grant the DRT engagement capability required in the scenario.  
Domaine  
Domain 2: Security and Compliance  
Question 49Correct  
A company wants to grant users in one AWS account access to resources in another AWS account. The users do not currently have permission to access the resources. Which AWS service will meet this requirement?  
A. IAM group

#### Explications

Groups are collections of IAM users used to assign the same set of permissions to multiple users inside a single AWS account. They are not IAM principals and cannot be assumed by identities from another account, so they cannot be used to delegate cross-account access.  
**Votre réponse est correcte**  
B. IAM role

#### Explications

Create a role in the account that owns the resources, give that role a permissions policy for the actions/resources required, and configure its trust policy to allow principals (an account, specific IAM role, or user) from the other AWS account to assume it. AWS STS AssumeRole issues temporary credentials when the role is assumed, enabling secure, auditable cross-account access without creating long‑term credentials in the resource account.  
C. IAM tag

#### Explications

Tags are metadata (key–value pairs) applied to AWS and IAM resources to aid organization and to use in policy conditions. They are not identities and do not themselves grant or delegate permissions, so tagging cannot be used to grant cross-account access on its own.  
D. IAM Access Analyzer

#### Explications

Access Analyzer inspects resource-based policies and identifies resources that are shared with external principals or are publicly accessible. It is a monitoring and analysis tool and does not create trust relationships or grant permissions to enable cross-account access.  
Explication générale  
The correct approach is to create an IAM role in the account that owns the resources and allow principals from the other account to assume that role. This uses IAM trust policies and AWS STS AssumeRole to provide temporary, least‑privilege credentials for cross-account access. Other options — grouping users, tags, or running an analyzer — either operate only within a single account, are metadata, or only analyze access rather than establish it.  
Domaine  
Domain 2: Security and Compliance  
Question 50Correct  
Which architecture concept describes the ability to deploy resources on demand and release resources when they are no longer needed?  
A. High availability

#### Explications

La haute disponibilité vise à concevoir des systèmes et des architectures qui restent opérationnels et accessibles en cas de défaillance de composants (par exemple, grâce à l'utilisation de plusieurs zones de disponibilité, de l'équilibrage de charge élastique, du routage de basculement Route 53 et de la redondance). Elle garantit la disponibilité et un basculement rapide, mais ne décrit pas à elle seule le provisionnement et la libération automatiques des ressources de calcul ou autres en fonction de l'évolution de la demande.  
B. Architecture découplée

#### Explications

L'architecture découplée consiste à séparer les composants afin qu'ils communiquent de manière asynchrone (par exemple via Amazon SQS, SNS ou des modèles événementiels). Cela améliore l'évolutivité et l'isolation des pannes, mais le découplage est un modèle de conception axé sur la modularité et la résilience, et non sur l'allocation et la libération automatiques à la demande de la capacité de l'infrastructure.  
C. Résilience

#### Explications

La résilience est la capacité d'un système à résister aux pannes et à s'en remettre (par le biais de tentatives de redémarrage, de redondance, de sauvegardes et de stratégies de reprise après sinistre). Elle prend en compte la continuité et la reprise (RTO/RPO), mais ne décrit pas spécifiquement l'ajout ou la suppression dynamique de ressources en fonction de la charge en temps réel.  
**Votre réponse est correcte**  
D. Élasticité

#### Explications

Ce concept désigne l'ajustement automatique de la capacité des ressources en fonction de la demande de charge de travail. Sur AWS, il est rendu possible par des fonctionnalités telles que EC2 Auto Scaling, Application Auto Scaling (pour ECS/EKS et DynamoDB), Elastic Load Balancing et les services sans serveur comme AWS Lambda. Il permet une optimisation des coûts grâce à une facturation à l'usage et à un provisionnement/libération rapide des ressources en fonction de métriques ou de planifications, ce qui le distingue de la scalabilité générale.  
Explication générale  
Cette question évalue le concept d'ajustement dynamique des ressources dans le cloud computing. La bonne réponse correspond au concept qui décrit l'ajout et la suppression automatiques de capacité en fonction de la demande, implémenté dans AWS via Auto Scaling, les équilibreurs de charge et les services sans serveur. Les autres réponses (haute disponibilité, architecture découplée, résilience) traitent de la disponibilité, de la conception modulaire ou de la reprise après incident, mais ne mentionnent pas spécifiquement le provisionnement et la libération automatiques des ressources à la demande.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 51Correct  
Quelle fonctionnalité du framework d'adoption du cloud AWS (AWS CAF) relève de la perspective humaine ?  
A. Architecture des données

#### Explications

Cette capacité s'inscrit dans la perspective de la plateforme, responsable de la conception et de la mise en œuvre de l'infrastructure cloud et des systèmes de données (stockage, bases de données, pipelines de données). Les tâches de la plateforme comprennent la sélection des services gérés (par exemple, Amazon S3, Amazon RDS, Amazon Redshift), la définition du cycle de vie des données et des modèles d'intégration — des responsabilités qui diffèrent des activités axées sur les personnes.  
B. Gestion d'événements

#### Explications

Cela correspond à la perspective des opérations. Elle englobe la surveillance, la détection, la réponse aux incidents et la gestion des événements à l'aide d'outils et de processus (par exemple, Amazon CloudWatch, AWS CloudTrail, les procédures d'exécution automatisées). Il s'agit de responsabilités opérationnelles axées sur la fiabilité du service plutôt que sur le développement des compétences des équipes.  
**Votre réponse est correcte**  
C. Maîtrise du cloud

#### Explications

Il s'agit d'une capacité axée sur les personnes : elle vise à développer les capacités organisationnelles en matière d'adoption du cloud grâce à la planification des effectifs, la définition des rôles, les programmes de formation et de certification, la requalification, le changement de culture et les parcours d'apprentissage continu, afin que le personnel possède les compétences et les responsabilités nécessaires pour réussir dans le cloud.  
D. Partenariat stratégique

#### Explications

Cela relève de la perspective commerciale, qui se concentre sur l'alignement des initiatives cloud avec la stratégie organisationnelle, les relations avec les parties prenantes, l'engagement des fournisseurs et des partenaires, et l'élaboration d'analyses de rentabilité — des préoccupations stratégiques et de gouvernance plutôt que le développement des compétences de la main-d'œuvre.  
Explication générale  
Le cadre d'adoption du cloud AWS (AWS Cloud Adoption Framework) regroupe les capacités selon six perspectives. La perspective « Personnel » concerne la préparation des effectifs : définition des rôles, formation, certifications, recrutement et évolution culturelle pour faciliter l'adoption du cloud. Le choix optimal est donc celui qui privilégie le développement des compétences et de l'expertise du personnel. Les éléments perturbateurs correspondent aux autres perspectives du cadre d'adoption du cloud : l'un concerne la plateforme et l'infrastructure, un autre les opérations et la gestion des incidents, et le dernier la stratégie et les enjeux commerciaux.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 52Correct  
Quel service AWS utilise la conversion de la parole en texte pour aider les utilisateurs à prendre des notes de réunion ?  
A. Amazon Polly

#### Explications

Incorrect — Ce service propose la synthèse vocale (TTS) pour générer du son à partir de texte. Il n'effectue pas de reconnaissance vocale automatique (ASR) et ne peut pas transcrire l'audio des réunions en texte.  
B. Extrait de texte Amazon

#### Explications

Incorrect — Ce service effectue la reconnaissance optique de caractères (OCR) et l'extraction de données structurées à partir de documents et d'images numérisés (formulaires, tableaux, paires clé-valeur). Il ne traite pas l'audio et ne convertit pas le langage parlé en texte.  
C. Reconnaissance Amazon

#### Explications

Incorrect — Ce service analyse les images et les vidéos à la recherche d'objets, de visages et d'activités, et peut détecter le texte dans les images. Il ne propose pas de transcription vocale des flux audio.  
**Votre réponse est correcte**  
D. Transcription Amazon

#### Explications

Exact — Ce service est la solution de reconnaissance vocale automatique (ASR) d'AWS, offrant la transcription en temps réel et par lots, la diarisation des locuteurs, les horodatages, l'identification des canaux et les vocabulaires personnalisés, ce qui le rend adapté à la génération de notes de réunion précises à partir de l'audio.  
Explication générale  
La question porte sur les services AWS utilisés pour convertir la parole en texte. Le service ASR est la bonne réponse, car il est spécifiquement conçu pour la transcription vocale et offre des fonctionnalités (transcription en temps réel/par lots, identification du locuteur, horodatage, vocabulaires personnalisés) nécessaires à la prise de notes en réunion. Les autres options relèvent de domaines différents : synthèse vocale, reconnaissance optique de caractères (OCR) de documents ou analyse d’images/vidéos, et ne répondent donc pas aux exigences de transcription.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 53Incorrect  
Une entreprise souhaite établir une connexion réseau sécurisée entre son infrastructure sur site et le cloud AWS en une semaine. Quelle solution répondra à ces exigences ?  
**Votre réponse est incorrecte**  
A. AWS Direct Connect

#### Explications

Incorrect. AWS Direct Connect fournit une liaison réseau privée et dédiée à AWS, mais nécessite un provisionnement physique, la commande de connexions croisées auprès d'un centre de données Direct Connect et une coordination avec un fournisseur. La configuration prend généralement plus d'une semaine et ne répond donc pas aux exigences de déploiement rapide.  
B. Amazon VPC

#### Explications

Incorrect. Un VPC Amazon est un réseau virtuel isolé au sein d'AWS, utilisé pour héberger des ressources ; il ne crée pas, à lui seul, de connectivité entre l'infrastructure sur site et AWS. La connexion d'un VPC à l'infrastructure sur site nécessite un service supplémentaire tel qu'un VPN de site à site ou Direct Connect.  
**Bonne réponse**  
C. VPN site à site AWS

#### Explications

Exact. Le VPN site à site AWS établit des tunnels chiffrés IPSec sur Internet entre votre passerelle locale et une passerelle privée virtuelle ou une passerelle de transit AWS. Il peut être configuré immédiatement via la console AWS ou les API, prend en charge le protocole BGP pour le routage dynamique et est conçu pour une connectivité rapide et sécurisée sans attendre le provisionnement physique.  
D. Emplacement du bord

#### Explications

Incorrect. Les emplacements Edge font partie du réseau de distribution de contenu Amazon CloudFront utilisé pour la mise en cache et la distribution de contenu aux utilisateurs finaux ; ils ne fournissent pas de connectivité réseau privée ni de fonctionnalité VPN/Direct Connect pour les réseaux sur site.  
Explication générale  
La méthode la plus rapide et pratique pour établir une connexion sécurisée entre votre infrastructure locale et AWS en moins d'une semaine est le VPN de site à site AWS. Ce service utilise des tunnels IPSec via Internet et peut être provisionné immédiatement via la console ou les API. Direct Connect est une option privée plus performante, mais elle nécessite un provisionnement physique et est généralement plus longue à mettre en œuvre. Un VPC est le réseau de destination au sein d'AWS, mais ne fournit pas lui-même de connectivité. Les points de présence (Edge Location) sont des points de terminaison CDN indépendants des connexions réseau privées.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 54Correct  
Quel service ou outil AWS permet aux utilisateurs de se connecter à AWS et de déployer des ressources par programmation ?  
A. Amazon QuickSight

#### Explications

Amazon QuickSight est un service de veille stratégique géré permettant de créer des tableaux de bord et des visualisations à partir de sources de données. Axé sur l'analyse et le reporting, il ne fournit ni API ni bibliothèques de développement pour le provisionnement ou la gestion de l'infrastructure AWS.  
B. Lien privé AWS

#### Explications

AWS PrivateLink est une fonctionnalité réseau qui permet une connectivité privée aux services du réseau Amazon, sans exposition à Internet. Elle concerne la connectivité sécurisée des services, et non la création ou la gestion programmatique des ressources AWS.  
C. AWS Direct Connect

#### Explications

AWS Direct Connect fournit des connexions réseau physiques dédiées entre les environnements sur site et AWS pour une connectivité prévisible et à haut débit. Il s'agit d'un service de connectivité réseau qui n'offre pas de fonctionnalités de provisionnement de ressources par programmation.  
**Votre réponse est correcte**  
D. Kits de développement logiciel AWS

#### Explications

Les kits de développement logiciel (SDK) AWS sont des bibliothèques spécifiques à chaque langage qui encapsulent les API des services AWS, gèrent la signature des requêtes (Sigv4), les nouvelles tentatives et l'analyse des réponses, et s'intègrent aux informations d'identification IAM. Ils permettent aux applications et aux scripts d'appeler les API des services AWS pour créer, mettre à jour et supprimer des ressources par programmation, ce qui en fait le mécanisme idéal pour les déploiements automatisés.  
Explication générale  
Cette question vise à déterminer quelle option offre une interface de programmation avec AWS. Les kits de développement logiciel (SDK) AWS exposent les API des services AWS via des bibliothèques de langage et gèrent l'authentification et les mécanismes de requête, permettant ainsi la création et la gestion de ressources par le biais du code. Les autres options sont des services d'analyse ou de mise en réseau (QuickSight, PrivateLink, Direct Connect) et ne constituent pas des API de développement pour le déploiement d'infrastructures.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 55Incorrect  
Quel service AWS peut être utilisé sans frais supplémentaires ?  
**Votre réponse est incorrecte**  
A. Amazon SageMaker

#### Explications

Incorrect — Amazon SageMaker est un service de machine learning géré, facturé en fonction des ressources utilisées : instances d’entraînement, hébergement des points de terminaison, instances de notebooks, stockage et traitement des données. Bien qu’il puisse exister des versions d’essai gratuites limitées, l’utilisation classique de SageMaker est payante (heures d’instance, stockage, transfert de données).  
B. Configuration AWS

#### Explications

Incorrect — AWS Config est un service de suivi et d'évaluation de la configuration qui facture les éléments de configuration enregistrés, les évaluations de règles et les fonctionnalités avancées (packs de conformité, agrégateurs). Son utilisation continue n'est pas gratuite.  
**Bonne réponse**  
C. Organisations AWS

#### Explications

Exact — AWS Organizations est proposé sans frais supplémentaires. Il offre une facturation consolidée, une gestion centralisée des comptes et des contrôles basés sur des politiques (politiques de contrôle des services) sans frais de niveau de service. Les comptes membres continuent de payer pour les ressources et services AWS qu’ils utilisent.  
D. Amazon CloudWatch

#### Explications

Incorrect — Amazon CloudWatch propose une offre gratuite limitée pour les métriques, les journaux et les alarmes de base, mais la plupart des fonctionnalités en production (métriques personnalisées, alarmes et tableaux de bord supplémentaires, ingestion et conservation des journaux, stockage des métriques et requêtes API) sont facturées. Le service n'est donc pas entièrement gratuit.  
Explication générale  
Ce test évalue vos connaissances sur la tarification des services AWS. AWS Organizations est la seule option gratuite : elle offre le regroupement de comptes, la facturation consolidée et la gestion des politiques sans frais. Les autres services (SageMaker, AWS Config, CloudWatch) peuvent proposer une utilisation gratuite limitée, mais la plupart des activités de production importantes (calcul, stockage, enregistrement, évaluation, métriques et journaux) sont facturées.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 56Correct  
Une entreprise souhaite stocker et récupérer des fichiers dans Amazon S3 pour ses applications sur site existantes en utilisant des protocoles de système de fichiers standard. Quel service AWS répond à ces exigences ?  
A. AWS DataSync

#### Explications

AWS DataSync est un service géré permettant des transferts de données automatisés et performants entre le stockage local et AWS (S3, EFS, FSx). Il est conçu pour la migration, la réplication et les synchronisations périodiques, et non pour la mise à disposition d'un partage de fichiers NFS/SMB persistant que les applications locales peuvent monter pour un accès aux fichiers en temps réel.  
B. AWS Snowball Edge

#### Explications

AWS Snowball Edge is a physical, portable device for large-scale data transfer and edge compute; it enables offline data import/export and local processing. It does not provide a continuously mounted, protocol-compatible file gateway to Amazon S3 for production on‑premises applications.  
**Votre réponse est correcte**  
C. Amazon S3 File Gateway

#### Explications

AWS Storage Gateway — File Gateway exposes industry-standard file protocols (NFS and SMB) to on‑premises applications and maps files to Amazon S3 objects. It provides a local cache for low-latency access, persists data as S3 objects (so you can use S3 lifecycle, versioning, encryption, etc.), and is intended specifically for seamless file-based access to S3.  
D. AWS Transfer Family

#### Explications

AWS Transfer Family offers managed endpoints for SFTP, FTPS, and FTP to move files into and out of S3 (or EFS). It facilitates file transfers over those protocols but does not act as a mountable NFS/SMB file system for existing on‑premises applications.  
Explication générale  
The question tests knowledge of services that enable on‑premises applications to access Amazon S3 using standard file system protocols. AWS Storage Gateway (File Gateway) is the appropriate service because it exposes NFS/SMB file shares backed by S3 and provides a local cache and object mapping. The other options are transfer or data-migration/edge solutions (DataSync, Snowball Edge) or managed transfer endpoints (Transfer Family) and do not provide a mountable file system backed by S3.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 57Correct  
Which task is a customer’s responsibility, according to the AWS shared responsibility model?  
**Votre réponse est correcte**  
A. Management of the guest operating systems

#### Explications

Customers are responsible for securing and maintaining the operating system they run on their compute resources (for example, EC2 instances). This includes applying OS patches and updates, configuring OS-level security controls (user accounts, host-based firewalls), and hardening the system. AWS operates and patches the underlying physical hosts, hypervisor, and control plane, but not the software you install inside your virtual machines.  
B. Maintenance of the configuration of infrastructure devices

#### Explications

Incorrect — AWS is responsible for the physical network devices and the configuration and maintenance of the underlying infrastructure. Customers manage their virtual network configuration (VPCs, subnets, route tables, security group rules), but not the physical infrastructure devices that AWS owns and operates.  
C. Management of the host operating systems and virtualization

#### Explications

Incorrect — The host operating systems that run the hypervisor and the virtualization layer are managed by AWS as part of the AWS-managed infrastructure. Customers do not manage the physical hosts or the hypervisor for managed services like EC2; they manage only the guest OS and software they deploy on instances.  
D. Maintenance of the software that powers Availability Zones

#### Explications

Incorrect — Software and control systems that operate Availability Zones (facility operations, host software, zoning, and related control-plane components) are the responsibility of AWS. Customers do not maintain the software that runs AWS’s Availability Zone infrastructure.  
Explication générale  
This question tests the AWS shared responsibility model: AWS is responsible for security and maintenance of the cloud infrastructure (hardware, host OS, virtualization, network, and facilities), while customers are responsible for security in the cloud (data, applications, and the software they run on provisioned resources). The correct choice identifies the customer responsibility for the operating system running inside their compute instances; the other options describe AWS-managed infrastructure and control-plane responsibilities.  
Domaine  
Domain 2: Security and Compliance  
Question 58Correct  
Which AWS service should users use to learn about AWS service availability and operations?  
A. Amazon EventBridge

#### Explications

EventBridge is an event bus and routing service that connects AWS services and SaaS sources for event-driven architectures. It does not provide service-status dashboards, account-specific operational alerts, or scheduled-maintenance information about AWS services.  
B. AWS Service Catalog

#### Explications

AWS Service Catalog is for centrally managing and provisioning approved IT products (templates, configurations) within an organization for governance and self-service. It does not publish AWS service availability or operational status.  
C. AWS Control Tower

#### Explications

Control Tower automates the setup and governance of multi-account AWS environments (landing zones and guardrails). Its purpose is account governance and compliance, not publishing service health or availability information.  
**Votre réponse est correcte**  
D. AWS Health Dashboard

#### Explications

The AWS Health Dashboard (including the Personal Health Dashboard) delivers account-specific, real-time alerts, scheduled-maintenance notifications, and operational guidance for AWS services that affect your resources. It also exposes the AWS Health API and integrates with EventBridge for automated notifications, making it the appropriate tool for learning about service availability and operations.  
Explication générale  
This question checks which AWS offering provides service availability and operational status information. The Health Dashboard is the correct choice because it presents both public and personalized health information, real-time and scheduled-event notifications, and integration points for alerting. The other options focus on event routing (EventBridge), cataloged product provisioning (Service Catalog), or multi-account governance (Control Tower) and therefore do not serve as service-status dashboards.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 59Correct  
Which AWS service provides the ability to manage infrastructure as code?  
A. AWS CodePipeline

#### Explications

This service orchestrates CI/CD pipelines (build, test, and deploy stages) and is designed for automating application release workflows, not for declaring and provisioning AWS resources via templates or stacks.  
B. AWS CodeDeploy

#### Explications

Ce service automatise le déploiement d'applications sur des cibles de calcul (par exemple EC2, ECS, Lambda) mais ne fournit pas de modélisation des ressources pilotée par des modèles, de création de piles ou de gestion du cycle de vie de l'infrastructure.  
C. AWS Direct Connect

#### Explications

Il s'agit d'un service réseau qui fournit une connexion dédiée entre les environnements sur site et AWS ; il n'offre pas de fonctionnalités permettant de définir, de provisionner ou de gérer les ressources AWS sous forme de code.  
**Votre réponse est correcte**  
D. AWS CloudFormation

#### Explications

Ce service fournit une infrastructure sous forme de code basée sur des modèles utilisant des modèles JSON ou YAML déclaratifs, prend en charge les piles et les ensembles de modifications, permet un provisionnement automatisé et reproductible ainsi qu'une détection des dérives, et s'intègre à d'autres services AWS pour une gestion complète du cycle de vie, ce qui en fait le choix idéal pour gérer l'infrastructure sous forme de code.  
Explication générale  
La gestion de l'infrastructure en tant que code requiert un service qui modélise, provisionne et gère les ressources AWS à l'aide de modèles déclaratifs et d'opérations de pile. Le service validé utilise des modèles JSON/YAML, des piles, des ensembles de modifications et la détection des écarts pour automatiser le cycle de vie de l'infrastructure. Les autres options sont axées sur l'orchestration CI/CD, l'automatisation du déploiement ou la mise en réseau et ne proposent donc pas de provisionnement d'infrastructure basé sur des modèles.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 60Correct  
Quel service AWS Cloud peut envoyer des alertes aux clients en cas de dépassement des seuils de dépenses personnalisés ?  
**Votre réponse est correcte**  
A. Budgets AWS

#### Explications

Offre des fonctionnalités budgétaires dédiées : vous pouvez créer des budgets de coûts, d’utilisation et de réservation avec des seuils en pourcentage ou en montant et recevoir des notifications lorsque ces seuils sont dépassés. Les notifications sont envoyées par e-mail et peuvent être acheminées via Amazon SNS. Budgets prend également en charge les budgets au niveau de l’organisation et les actions budgétaires automatisées pour faciliter le contrôle des coûts.  
B. AWS Cost Explorer

#### Explications

Il s'agit principalement d'un outil de reporting et de visualisation permettant d'analyser les données historiques et prévisionnelles de coûts et d'utilisation. Il aide à explorer les tendances de dépenses et à générer des rapports, mais ne propose pas d'alertes personnalisables basées sur des seuils (utilisez les alertes budgétaires ou la détection d'anomalies dédiée pour les alertes).  
C. Balises d'allocation des coûts AWS

#### Explications

Les balises sont des métadonnées appliquées aux ressources pour attribuer et répartir les coûts entre les projets, les équipes ou les environnements. Elles permettent le filtrage et le regroupement dans les rapports de coûts, mais ne génèrent pas d'alertes de dépenses.  
D. Organisations AWS

#### Explications

Ce service permet de gérer de manière centralisée plusieurs comptes AWS, d'appliquer des politiques et de consolider la facturation. Il assure la facturation consolidée et la gestion de la hiérarchie, mais ne sert pas de mécanisme d'envoi d'alertes personnalisées en cas de dépassement de seuil de dépenses (les budgets sont intégrés à AWS Organizations pour la budgétisation inter-comptes).  
Explication générale  
Cette question évalue vos connaissances des outils de gestion des coûts AWS. La fonctionnalité Budgets permet de suivre les dépenses et l'utilisation et d'informer les parties prenantes lorsque des seuils définis sont dépassés (par e-mail/réseaux sociaux et via des actions budgétaires optionnelles). Les autres outils mentionnés servent à l'analyse, au balisage ou à la gestion de compte et ne proposent pas le système d'alertes configurable basé sur des seuils offert par Budgets.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 61Correct  
Quel service ou fonctionnalité AWS nécessite un fournisseur d'accès Internet (FAI) et un centre de colocation pour être mis en œuvre ?  
A. VPN AWS

#### Explications

Incorrect. Le VPN site à site AWS crée un tunnel chiffré IPsec entre une passerelle client et une passerelle privée virtuelle ou une passerelle de transit, et achemine le trafic via l'Internet public. Bien que le client ait besoin d'une connexion Internet sur site, le VPN ne nécessite ni colocation physique dans un emplacement AWS Direct Connect, ni interconnexions dédiées dans un centre de colocation.  
B. Amazon Connect

#### Explications

Incorrect. Amazon Connect est un service de centre de contact entièrement géré et hébergé dans le cloud, accessible via Internet ou la téléphonie gérée par AWS. Il s'agit d'un service logiciel qui ne nécessite aucun déploiement d'équipement dans un centre de colocation ni l'établissement d'une interconnexion FAI dédiée à AWS.  
**Votre réponse est correcte**  
C. AWS Direct Connect

#### Explications

Exact. AWS Direct Connect établit une connexion réseau privée et dédiée entre le réseau sur site d'un client (ou d'un locataire en colocation) et les emplacements AWS Direct Connect. Sa mise en œuvre nécessite généralement une présence physique dans un centre de colocation ou le recours à un partenaire AWS Direct Connect, ainsi qu'une coordination avec un fournisseur de réseau/FAI pour la mise en place de connexions fibre optique et de VLAN, offrant ainsi un accès à AWS sans passer par Internet.  
D. Passerelle Internet

#### Explications

Incorrect. Une passerelle Internet est un composant VPC virtuel géré par AWS qui permet aux instances dotées d'adresses IP publiques de communiquer avec Internet. Il ne s'agit pas d'un dispositif physique et son déploiement ne nécessite aucun centre de colocation ni interconnexion spécifique à un FAI.  
Explication générale  
Cette question distingue les services nécessitant une infrastructure réseau physique de ceux fonctionnant sur l'Internet public ou en tant que composants virtuels gérés par AWS. AWS Direct Connect est la seule option exigeant des interconnexions physiques et une présence dans un centre de colocation (ainsi qu'une coordination avec un fournisseur de réseau/FAI) pour établir une connexion dédiée à AWS. Les autres options (VPN, Amazon Connect, passerelle Internet) utilisent l'Internet public ou sont des services virtuels et ne requièrent donc ni colocation ni interconnexions dédiées auprès d'un FAI.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 62Correct  
Une entreprise souhaite améliorer la productivité de ses employés en leur offrant la possibilité de rechercher des questions et d'obtenir des réponses précises. Elle souhaite utiliser une interface de recherche unique et intelligente. Quel service AWS répond à ces exigences ?  
A. Amazon Connect

#### Explications

Incorrect. Amazon Connect est une solution de centre de contact cloud (CCaaS) pour les interactions vocales et par chat, les flux de contacts et le routage des agents. Elle ne propose pas l'indexation de documents, la recherche d'entreprise en langage naturel ni la récupération intégrée de questions-réponses dans les bases de connaissances.  
**Votre réponse est correcte**  
B. Amazon Kendra

#### Explications

Exact. Amazon Kendra est un service de recherche d'entreprise entièrement géré et basé sur l'apprentissage automatique, qui indexe les documents et les sources de connaissances, prend en charge les requêtes en langage naturel et le réglage de la pertinence, fournit des connecteurs (S3, SharePoint, bases de données, FAQ) et renvoie des passages et des réponses précis, ce qui le rend idéal pour une interface de recherche intelligente unique pour les employés.  
C. Amazon Lex

#### Explications

Incorrect. Amazon Lex fournit des interfaces conversationnelles (chatbots) utilisant des intentions et des emplacements pour l'interaction vocale et textuelle. Bien qu'il puisse alimenter une interface conversationnelle, il n'indexe pas les documents d'entreprise et ne propose pas de recherche et d'extraction basées sur l'apprentissage automatique dans plusieurs sources de données sans service de recherche sous-jacent.  
D. Amazon Comprendre

#### Explications

Incorrect. Amazon Comprehend effectue des tâches de traitement automatique du langage naturel (extraction d'entités, analyse des sentiments, identification des mots-clés, modélisation thématique) pour analyser du texte. Il peut enrichir la recherche en produisant des métadonnées, mais n'offre pas d'interface de recherche d'entreprise gérée ni de récupération directe de questions-réponses dans les référentiels de documents.  
Explication générale  
Cette question évalue vos connaissances des services AWS dédiés à la recherche d'entreprise et à l'extraction de connaissances. Amazon Kendra est le choix idéal, car il s'agit d'un service de recherche géré, basé sur l'apprentissage automatique, qui indexe de multiples sources de données et prend en charge la réponse aux questions en langage naturel. Les autres services (Connect, Lex et Comprehend) s'adressent respectivement aux centres de contact, aux interfaces conversationnelles et à l'analyse de texte, mais ne fournissent pas les fonctionnalités complètes de recherche et d'extraction de données d'entreprise requises ici.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 63Correct  
Une entreprise prévoit de migrer vers le cloud AWS. Dans le cadre d'une transformation organisationnelle, elle souhaite être plus réactive aux demandes et aux commentaires de ses clients. Quelles actions doit-elle entreprendre pour répondre à ces exigences, conformément au cadre d'adoption du cloud AWS (AWS CAF) ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Réorganiser les équipes pour qu'elles se concentrent sur les produits et les flux de valeur.

#### Explications

La réorganisation autour des produits et des flux de valeur permet aux équipes de maîtriser l'intégralité du processus, des fonctionnalités aux interactions clients, réduisant ainsi les transferts de responsabilité et raccourcissant les cycles de rétroaction. Ce changement structurel constitue une pratique organisationnelle fondamentale d'AWS CAF visant à accroître la réactivité et à aligner la prestation sur la valeur client.  
B. Créer de nouvelles propositions de valeur avec de nouveaux produits et services.

#### Explications

Définir de nouvelles propositions de valeur est une activité de stratégie commerciale/produit qui peut créer de la valeur pour le client, mais elle ne modifie pas en soi la structure de l'équipe ni les pratiques de livraison nécessaires pour mieux répondre aux demandes et aux commentaires.  
**Votre sélection est correcte**  
C. Utiliser des méthodes agiles pour itérer et évoluer rapidement.

#### Explications

L'adoption de méthodes agiles et de pratiques connexes (itérations courtes, livraison continue, boucles de rétroaction rapides) permet une expérimentation rapide et une intégration plus rapide des commentaires des clients, ce que l'AWS CAF identifie comme essentiel à la réactivité organisationnelle.  
D. Utilisez une nouvelle plateforme de données et d'analyse pour générer des informations exploitables.

#### Explications

La mise en place d'une plateforme de données et d'analyse peut améliorer la connaissance des clients, mais il s'agit d'une capacité technique (du point de vue de la plateforme) et elle ne modifiera pas automatiquement les processus organisationnels ni les responsabilités des équipes nécessaires à une réponse plus rapide.  
E. Migrer et moderniser l'infrastructure existante.

#### Explications

La migration et la modernisation de l'infrastructure permettent de moderniser les aspects techniques et d'assurer l'évolutivité opérationnelle, mais elles n'impliquent pas directement les changements organisationnels ou de processus (alignement des équipes, pratiques agiles) qui favorisent la réactivité aux besoins des clients.  
Explication générale  
Le cadre d'adoption du cloud AWS met l'accent sur les changements organisationnels et de processus — tels que la réorganisation des équipes autour des flux de valeur et l'adoption de pratiques agiles — afin d'améliorer la réactivité aux besoins des clients. Les investissements techniques (plateformes analytiques, modernisation de l'infrastructure) et les nouvelles offres de produits peuvent contribuer à cet objectif, mais ne remplacent pas les changements structurels et culturels qui raccourcissent directement les cycles de rétroaction et améliorent la réactivité.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 64Correct  
Quel service ou outil AWS permet de visualiser les tendances historiques des dépenses AWS et les projections des coûts futurs d'AWS ?  
A. Rapport sur les coûts et l'utilisation d'AWS

#### Explications

Incorrect — Le rapport AWS Cost and Usage Report (CUR) génère des fichiers de facturation et d'utilisation bruts et détaillés, stockés sur Amazon S3 (CSV/Parquet). Il est destiné au traitement et à l'analyse en aval (Athena, Redshift, QuickSight ou pipelines ETL) et non à la visualisation interactive intégrée ou à la prévision.  
B. Budgets AWS

#### Explications

Incorrect — AWS Budgets est conçu pour définir des seuils de coûts/d'utilisation, envoyer des alertes et suivre les dépenses budgétées par rapport aux dépenses réelles. Il peut fournir des prévisions budgétaires de base par rapport à un budget défini, mais il ne constitue pas l'outil principal pour l'exploration multidimensionnelle des coûts historiques et les prévisions détaillées par service, balise et compte.  
**Votre réponse est correcte**  
C. Explorateur de coûts

#### Explications

Tout à fait exact — AWS Cost Explorer fournit des rapports interactifs et multidimensionnels sur les coûts et l'utilisation, avec des graphiques intégrés, des filtres (service, région, étiquette, compte associé, type d'utilisation) et une fonction de prévision qui projette les coûts futurs à partir des tendances historiques. Il propose également des recommandations de plans d'inventaire réservé (RI) et d'économies, et s'intègre aux fonctionnalités de gestion des coûts pour l'analyse et la prévision quotidiennes.  
D. Amazon Cloud Watch

#### Explications

Incorrect — Amazon CloudWatch est un service de surveillance et d'observabilité des métriques, des journaux et des alarmes liés aux ressources et aux applications. Bien qu'il soit possible d'activer les métriques de facturation pour CloudWatch, ce service n'offre pas les fonctionnalités avancées d'analyse des coûts, de visualisation interactive de l'historique des coûts ni de prévision proposées par Cost Explorer.  
Explication générale  
Cette question évalue vos connaissances des outils de gestion des coûts AWS. AWS Cost Explorer est le service dédié à la visualisation interactive de l'historique des coûts et à la prévision. Le rapport « Coûts et utilisation » fournit des données brutes à exporter, nécessitant une analyse plus approfondie. AWS Budgets permet de définir des seuils et des alertes (avec des prévisions budgétaires limitées). Enfin, CloudWatch est destiné aux indicateurs opérationnels et à la journalisation, plutôt qu'à une analyse complète des coûts.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 65Incorrect  
Une entreprise a migré ses systèmes vers le cloud AWS. Les systèmes sont correctement dimensionnés et un audit de sécurité n'a révélé aucun problème. L'entreprise doit s'assurer que les développements, intégrations, modifications et la croissance de l'utilisation du système ne compromettent pas cette infrastructure AWS optimisée. Quel service AWS l'entreprise doit-elle utiliser pour suivre l'optimisation et la sécurité en continu ?  
**Bonne réponse**  
A. Conseiller de confiance AWS

#### Explications

Trusted Advisor évalue en continu un compte en fonction d'un ensemble complet de critères répartis en cinq catégories (optimisation des coûts, performances, sécurité, tolérance aux pannes et limites de service) et génère des recommandations priorisées et exploitables. Accessible via la console ou l'API, il fournit un accompagnement automatisé et continu pour prévenir les dérives de configuration susceptibles de dégrader la sécurité ou l'efficacité. (Remarque : certains critères nécessitent un support Business/Enterprise.)  
**Votre réponse est incorrecte**  
B. Tableau de bord de santé AWS

#### Explications

Le tableau de bord AWS Health fournit des informations sur l'état opérationnel et les événements des services AWS susceptibles d'affecter votre compte (interruptions de service, maintenance planifiée et problèmes spécifiques au compte). Il ne propose pas d'optimisation proactive ni de recommandations de configuration personnalisées pour améliorer les coûts, les performances ou la sécurité.  
C. Amazon Connect

#### Explications

Amazon Connect est un service de centre de contact cloud destiné aux interactions clients. Il est indépendant de l'optimisation de l'infrastructure et de la gestion de la sécurité, et ne propose pas les contrôles continus de l'environnement ni les recommandations nécessaires dans ce contexte.  
D. Responsable des systèmes AWS

#### Explications

AWS Systems Manager est une suite de gestion des opérations qui fournit des services d'inventaire, de mise à jour, d'automatisation, d'exécution de commandes et de rapports de conformité pour les instances gérées. Bien qu'elle contribue à automatiser les tâches opérationnelles et à garantir l'application de la configuration, elle ne propose pas les recommandations d'optimisation et de sécurité globales et transversales (analyses des coûts, des performances et de la sécurité) offertes par Trusted Advisor.  
Explication générale  
L'objectif est de fournir des recommandations continues et transversales aux différents services afin de préserver un environnement AWS optimisé et sécurisé, même en cas d'évolution. Trusted Advisor est conçu pour effectuer des contrôles continus et priorisés, et proposer des recommandations concrètes concernant les coûts, les performances, la sécurité, la tolérance aux pannes et les limites de service. Les autres options, qu'elles se limitent à l'évaluation de l'état du service (AWS Health), à la gestion opérationnelle des instances (Systems Manager) ou qu'elles soient sans rapport avec ces aspects (Amazon Connect), ne répondent donc pas pleinement aux exigences en matière d'optimisation continue et de rapports de sécurité.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 66Correct  
Quel service AWS permet à une entreprise de traiter son infrastructure comme du code ?  
A. AWS CodeDeploy

#### Explications

Ce service automatise le déploiement des mises à jour d'applications sur les cibles de calcul (EC2, Lambda, sur site) et gère les stratégies de déploiement (sur place, bleu/vert). Il ne propose pas de méthode déclarative pour définir ou versionner les ressources d'infrastructure sous-jacentes ; il ne s'agit donc pas de l'outil IaC testé par la question.  
B. AWS Elastic Beanstalk

#### Explications

This platform-as-a-service automates provisioning and lifecycle management of application environments (capacity, load balancing, scaling, health). Although it simplifies deployments and can generate underlying resources, it is not the primary declarative IaC mechanism for modeling and versioning infrastructure across AWS accounts and regions.  
C. Amazon API Gateway

#### Explications

This fully managed service is used to create, publish, secure and monitor APIs. It is unrelated to defining or provisioning AWS infrastructure as code and therefore does not satisfy the IaC requirement.  
**Votre réponse est correcte**  
D. AWS CloudFormation

#### Explications

Provides a declarative, template-based mechanism (JSON/YAML) to define AWS resources as stacks, enabling repeatable provisioning, version control, change sets, stack updates, and drift detection. These capabilities are the foundation for treating infrastructure as code on AWS and integrating with CI/CD pipelines.  
Explication générale  
The question asks which service enables infrastructure-as-code. The correct choice is the service that offers declarative templates and stack management so infrastructure can be defined, versioned, and provisioned automatically. Other options focus on application deployment or API management and do not provide the comprehensive template-driven IaC features (stack creation, change sets, drift detection, cross-account/region provisioning) required for treating infrastructure as code.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 67Incorrect  
A company needs a central user portal so that users can log in to third-party business applications that support Security Assertion Markup Language (SAML) 2.0. Which AWS service will meet this requirement?  
A. AWS Identity and Access Management (IAM)

#### Explications

Incorrect — AWS Identity and Access Management (IAM) is focused on managing identities, roles, policies, and permissions for AWS resources and can enable federation for AWS console access, but it does not provide a user-facing centralized SSO portal for third-party SAML 2.0 applications.  
**Votre réponse est incorrecte**  
B. Amazon Cognito

#### Explications

Incorrect — Amazon Cognito provides user pools and identity pools to authenticate end users of web and mobile applications and can federate with SAML IdPs, but it is designed for application-level authentication and developer integration, not as an enterprise-wide SAML SSO portal for multiple third‑party business applications.  
**Bonne réponse**  
C. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

Correct — AWS IAM Identity Center (AWS Single Sign‑On) delivers a centralized user portal and single sign‑on capabilities, supports SAML 2.0 integration with third‑party cloud applications, allows administrators to assign application access centrally (and optionally provision users via SCIM), and integrates with external identity providers and AWS Organizations for enterprise access management.  
D. AWS CLI

#### Explications

Incorrect — The AWS Command Line Interface (CLI) is a tool for programmatic interaction with AWS APIs and services; it is not an identity provider or a user portal and cannot serve as a SAML 2.0 single sign‑on solution for third‑party applications.  
Explication générale  
Cette question vise à déterminer quel service AWS fournit un portail d'authentification unique (SSO) d'entreprise pour les applications tierces utilisant SAML 2.0. AWS IAM Identity Center est conçu spécifiquement pour l'authentification unique centralisée et l'attribution d'applications via SAML 2.0. IAM gère les autorisations des ressources AWS, Cognito est dédié à l'authentification des utilisateurs au niveau de l'application et l'interface de ligne de commande AWS (AWS CLI) est un outil de développement ; aucun de ces services ne propose de portail SSO SAML centralisé.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 68Correct  
Une entreprise souhaite établir une connexion réseau privée entre AWS et son réseau d'entreprise. Quel service ou fonctionnalité AWS répond à ce besoin ?  
A. Amazon Connect

#### Explications

Amazon Connect est un centre de contact cloud (CCaaS) pour les interactions clients et les flux de travail téléphoniques. Il ne fournit pas de connectivité réseau de couche 2/3 ni la possibilité d'établir un circuit privé dédié entre l'infrastructure sur site et AWS.  
B. Route 53 d'Amazonie

#### Explications

Amazon Route 53 est un service DNS et de gestion du trafic (zones hébergées publiques et privées) utilisé pour la résolution de noms et les politiques de routage. Il ne crée pas de liaisons réseau physiques ou dédiées entre un centre de données d'entreprise et AWS.  
**Votre réponse est correcte**  
C. AWS Direct Connect

#### Explications

AWS Direct Connect fournit une connexion réseau dédiée entre votre infrastructure locale et AWS. Il établit des interfaces virtuelles privées pour se connecter directement à un VPC (via une passerelle privée virtuelle ou une passerelle de transit) ou aux services publics AWS, offrant ainsi une latence plus stable, un débit plus élevé et une dépendance réduite à l'Internet public. Direct Connect peut être associé à un chiffrement (par exemple, en exécutant un VPN sur la connexion Direct Connect) si nécessaire.  
D. Interconnexion VPC

#### Explications

Le peering VPC permet une connectivité IP privée entre deux VPC au sein d'AWS, mais est exclusivement réservé à la communication entre VPC et ne crée pas de circuit vers un réseau d'entreprise sur site. Il ne remplace pas Direct Connect et n'est pas transitif (il ne peut pas être utilisé pour acheminer le trafic sur site entre plusieurs VPC).  
Explication générale  
Le choix optimal est AWS Direct Connect, car ce service AWS est conçu pour créer une connexion réseau privée et dédiée entre un centre de données sur site et AWS, garantissant des performances constantes et une exposition réduite à Internet. Les autres options correspondent à différents types de services : Amazon Connect est un service de centre de contact, Route 53 est un service de gestion DNS et de trafic, et le peering VPC ne relie que les VPC au sein d’AWS et ne permet pas de connecter un réseau d’entreprise à AWS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 69Correct  
Quelles sont les responsabilités du client lors de l'utilisation d'AWS Lambda selon le modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
A. Gestion du code au sein de la fonction Lambda

#### Explications

Les clients sont responsables de la logique de leurs applications et de ce qu'ils déploient sur Lambda : création, packaging et mise à jour du code des fonctions et des bibliothèques ou couches incluses ; configuration des paramètres des fonctions (mémoire, délai d'expiration, variables d'environnement) ; et sécurisation de l'accès au niveau de l'application (rôles et stratégies IAM, validation des entrées et gestion des secrets). Il s'agit de responsabilités de la couche application dans le modèle de responsabilité partagée.  
B. Confirmer que le matériel fonctionne dans le centre de données

#### Explications

AWS is responsible for the physical infrastructure and facility operations (servers, power, networking, and data‑center security). Confirming hardware health and repair is an AWS operational responsibility, not something customers perform for managed services like Lambda.  
C. Patching the operating system

#### Explications

Operating-system patching for the underlying hosts and the managed runtime environment is handled by AWS for Lambda’s managed runtimes. If you bring your own container image or custom runtime, you remain responsible for the contents of that image (OS packages and libraries inside it), but not the host OS that AWS manages.  
D. Shutting down Lambda functions when they are no longer in use

#### Explications

Lambda is a serverless, event-driven service that automatically provisions and scales execution environments and terminates them as needed. Manually shutting down functions is not required; however, customers should delete or disable unused functions to reduce attack surface and accidental invocation.  
Explication générale  
This question tests the shared-responsibility model for a serverless service. AWS manages the physical infrastructure, host OS, and managed runtimes for Lambda, while customers are responsible for application code, dependencies, function configuration, and application-level security. The correct option focuses on the customer’s duty for their code and configuration; the incorrect options describe responsibilities that belong to AWS or misconstrue how Lambda lifecycle is managed.  
Domaine  
Domain 2: Security and Compliance  
Question 70Correct  
Which AWS service can migrate Amazon EC2 instances from one AWS Region to another?  
**Votre réponse est correcte**  
A. AWS Application Migration Service

#### Explications

Provides continuous, block-level replication of source servers, automated conversion of replicated machines into Amazon EC2 instances, and orchestration of test cutovers and final cutover — enabling a lift-and-shift migration of running servers between Regions with minimal downtime.  
B. AWS Database Migration Service (AWS DMS)

#### Explications

Designed to migrate and replicate database engines (homogeneous or heterogeneous) and their data; it operates at the database level and does not replicate OS-level state, applications, or entire EC2 instances.  
C. AWS DataSync

#### Explications

A managed service for high-performance data transfers between file/object storage locations (on-premises and AWS or between AWS storage services); it moves files and objects, not running server images or VM instances.  
D. AWS Migration Hub

#### Explications

A centralized tracking and progress-reporting service for migration projects; it aggregates status from migration tools but does not perform replication, conversion, or the actual movement of EC2 instances.  
Explication générale  
This question tests which AWS service performs lift-and-shift migrations of servers. The correct service performs block-level replication, automated conversion to EC2, and cutover orchestration to migrate entire server instances across Regions. The other options focus on database migration, data transfer, or migration tracking and therefore do not perform full EC2 instance migrations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 71Correct  
Quel principe de conception AWS met l'accent sur la réduction des interdépendances entre les composants d'une application ?  
A. Évolutivité

#### Explications

La scalabilité concerne la capacité d'un système à gérer une charge accrue en ajoutant des ressources ou en utilisant des services élastiques (par exemple, Auto Scaling, Amazon EC2, AWS Lambda). Elle ne traite pas spécifiquement de la réduction des dépendances entre les composants ni de l'amélioration de leur isolation.  
**Votre réponse est correcte**  
B. Accouplement lâche

#### Explications

Le couplage faible est un principe architectural qui minimise les dépendances entre les composants afin qu'ils puissent évoluer, s'adapter et tomber en panne indépendamment. Dans les architectures AWS, ce principe est mis en œuvre grâce à des limites de service clairement définies, des modèles asynchrones et des services de découplage gérés (par exemple, Amazon SQS, Amazon SNS, les architectures événementielles, API Gateway ou des API de service bien définies) pour améliorer la résilience et la maintenabilité.  
C. Automatisation

#### Explications

L'automatisation vise à garantir la reproductibilité et à réduire les interventions manuelles grâce à des outils tels qu'AWS CloudFormation, AWS CDK et AWS Systems Manager. Bien qu'elle améliore la cohérence des déploiements et l'efficacité opérationnelle, elle ne réduit pas à elle seule les interdépendances entre les composants.  
D. Mise en cache

#### Explications

La mise en cache améliore les performances et réduit la latence en stockant les données fréquemment consultées (par exemple, Amazon ElastiCache ou Amazon CloudFront). Elle améliore les performances de lecture et réduit la charge, mais ne corrige pas le couplage architectural entre les composants.  
Explication générale  
Cette question évalue la connaissance des principes architecturaux d'AWS. Le couplage faible est la bonne réponse car il vise explicitement à réduire les interdépendances afin que les composants puissent fonctionner, évoluer et tomber en panne indépendamment ; AWS encourage cette approche grâce aux limites de service et aux mécanismes de découplage (SQS, SNS, événements, API). Les autres options — évolutivité, automatisation et mise en cache — sont des considérations de conception pertinentes, mais elles concernent la gestion de la charge, les opérations répétitives et l'optimisation des performances plutôt que la réduction de l'interdépendance des composants.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 72Correct  
Une entreprise souhaite suivre les étiquettes, les compartiments et les préfixes de ses objets Amazon S3. Quelle fonctionnalité S3 répond à ce besoin ?  
**Votre réponse est correcte**  
A. Rapport d'inventaire S3

#### Explications

L'inventaire S3 est une fonctionnalité de reporting permettant de générer des listes CSV ou ORC planifiées, contenant des métadonnées sélectionnables. Vous pouvez configurer l'inventaire pour inclure les étiquettes, les clés (qui indiquent la structure compartiment/préfixe), la classe de stockage, l'état du chiffrement, etc. Les rapports sont envoyés vers un compartiment S3 et peuvent être interrogés (par exemple avec Amazon Athena) pour suivre les étiquettes, les préfixes et les objets dans différents compartiments.  
B. Cycle de vie S3

#### Explications

Les règles de cycle de vie automatisent les transitions entre les classes de stockage et l'expiration/le nettoyage des objets. Elles ne génèrent pas de listes consolidées ni de rapports planifiés sur les métadonnées ou les étiquettes des objets ; elles ne peuvent donc pas être utilisées pour suivre les étiquettes, les compartiments ou les préfixes.  
C. Versionnage S3

#### Explications

Le versionnage conserve plusieurs versions historiques d'un objet afin de permettre sa récupération et de le protéger contre les suppressions ou écrasements accidentels. Il ne fournit cependant pas de mécanisme de génération de rapports listant les étiquettes d'objets ou les inventaires de préfixes dans les différents compartiments.  
D. S3 ACL

#### Explications

Access Control Lists (ACLs) define permissions at the bucket or object level to grant/read/write access. ACLs are an access control mechanism, not a reporting or inventory tool, and therefore do not provide tag or prefix tracking.  
Explication générale  
The question distinguishes S3 reporting capabilities from management and access features. The inventory feature is designed to produce scheduled, queryable reports of objects and selected metadata—including tags and object keys (prefixes)—making it the appropriate choice for tracking tags, buckets, and prefixes. Lifecycle rules, versioning, and ACLs serve different operational or security purposes and do not create consolidated object metadata reports.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 73Correct  
A company that uses AWS needs to transfer 2 TB of data. Which type of transfer of that data would result in no cost for the company?  
**Votre réponse est correcte**  
A. Inbound data transfer from the internet

#### Explications

AWS does not charge for data ingress from the public internet into AWS (commonly described as “Data Transfer IN”). For an upload of 2 TB into AWS, there is no per‑GB data transfer fee charged by AWS, so this option results in no transfer cost.  
B. Outbound data transfer to the internet

#### Explications

Data egress from AWS to the public internet (Data Transfer OUT) is billed per GB and is one of the primary sources of data transfer charges; transferring 2 TB out to the internet would incur significant cost.  
C. Data transfer between AWS Regions

#### Explications

Inter‑region transfer (data moved between AWS Regions) is charged per GB. Traffic that crosses regional boundaries leaves the region and is billed as inter‑region data transfer, so it is not free.  
D. Data transfer between Availability Zones

#### Explications

Data transferred between Availability Zones in the same Region is normally billed (cross‑AZ data transfer rates apply for resources communicating across AZs). This traffic is not free in general, so it would incur charges for a 2 TB transfer.  
Explication générale  
The question tests knowledge of AWS data transfer billing. AWS does not charge for ingress (data transferred in from the internet), so importing 2 TB into AWS would have no transfer fee. By contrast, outbound internet transfer, inter‑region transfer, and most cross‑AZ transfers incur per‑GB charges and would produce costs.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 74Correct  
A company wants an AWS service to collect and process 10 TB of data locally and transfer the data to AWS. The company has intermittent connectivity. Which AWS service will meet these requirements?  
A. AWS Database Migration Service (AWS DMS)

#### Explications

Incorrect — AWS Database Migration Service (DMS) is focused on migrating and replicating databases (including ongoing change data capture) over network connections. It is not a physical appliance and is not intended for bulk offline data collection or shipping when network connectivity is intermittent.  
B. AWS DataSync

#### Explications

Incorrect — AWS DataSync transfère efficacement les données de fichiers entre le stockage local et AWS grâce à un agent réseau et un protocole optimisé. Il nécessite une connectivité réseau (stable ou avec reprise possible) et n'est pas conçu comme une solution d'expédition physique hors ligne pour les environnements à connectivité intermittente ou inexistante.  
C. Sauvegarde AWS

#### Explications

Incorrect — AWS Backup centralise la gestion des sauvegardes et la protection automatisée des ressources AWS (et des cibles sur site prises en charge), mais ne fournit pas d'appliance physique ni de mécanisme de transfert en masse hors ligne pour collecter et expédier des téraoctets de données locales vers AWS.  
**Votre réponse est correcte**  
D. AWS Snowball Edge

#### Explications

Exact — AWS Snowball Edge est un dispositif physique sécurisé conçu pour la collecte de données en périphérie, leur traitement local (avec prise en charge des fonctions de calcul et Lambda) et leur transfert hors ligne vers AWS. Il prend en charge le stockage chiffré et la gestion inviolable des données et est spécifiquement destiné aux grands ensembles de données et aux environnements à connectivité réseau intermittente ou limitée ; les dispositifs sont renvoyés à AWS pour être intégrés à S3.  
Explication générale  
Cette question évalue vos connaissances des options de transfert de données AWS pour les grands ensembles de données avec une connectivité intermittente. La solution appropriée consiste en un dispositif physique prenant en charge la collecte locale et l'envoi hors ligne vers AWS. AWS Snowball Edge répond à ces exigences en fournissant un stockage sécurisé à haute capacité et une puissance de calcul locale optionnelle pour le traitement en périphérie avant que le dispositif ne soit renvoyé à AWS pour ingestion. Les autres options (DMS, DataSync, AWS Backup) sont des services réseau ou des outils d'orchestration de sauvegarde et ne proposent pas la capacité de transfert physique hors ligne requise ici.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 75Correct  
Une plateforme d'apprentissage en ligne doit exécuter une application pendant deux mois chaque année. Cette application sera déployée sur des instances Amazon EC2. Toute interruption de service est impérativement évitée durant ces deux mois. Quelle option d'achat EC2 répond le mieux à ces exigences en termes de coût ?  
A. Instances réservées

#### Explications

Ce modèle d'achat exige un engagement d'un ou trois ans en échange d'une tarification horaire plus avantageuse. Étant donné que la charge de travail ne s'étend que sur deux mois par an, l'engagement à long terme et la planification préalable nécessaires rendent ce modèle peu susceptible d'être rentable dans ce cas précis.  
B. Hôtes dévoués

#### Explications

Cette option propose des serveurs physiques entièrement dédiés à un seul client afin de répondre aux exigences de licences ou de conformité. Elle engendre des coûts et des frais d'exploitation plus élevés, inutiles pour une charge de travail critique en termes de disponibilité et à court terme.  
C. Exemples ponctuels

#### Explications

Cette approche utilise la capacité EC2 disponible à des prix très réduits, mais les instances peuvent être récupérées rapidement (interruptions ponctuelles avec un  
**Votre réponse est correcte**  
D. Instances à la demande

#### Explications

L'utilisation de la capacité EC2 à la demande, sans engagement à long terme, garantit la disponibilité de la capacité pendant exactement deux mois et vous ne payez que ce que vous consommez. Cela assure une disponibilité prévisible (sans interruption forcée par AWS) et constitue généralement le choix le plus rentable pour les charges de travail de courte durée qui ne doivent en aucun cas être interrompues.  
Explication générale  
For a workload that runs only two months per year and cannot tolerate downtime, the best purchasing choice is a pay-as-you-go EC2 option: it provides guaranteed, uninterrupted capacity for the required period without a long-term commitment. Long-term commitment options or single-tenant physical servers are not cost-effective for this short window, and spot pricing introduces interruption risk that violates the zero-downtime requirement.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 76Incorrect  
Which of the following are features of network ACLs as they are used in the AWS Cloud? (Choose two.)  
**Votre sélection est correcte**  
A. They are stateless.

#### Explications

Network ACLs do not maintain connection state. Each packet is evaluated independently against the ACL rules (both ingress and egress), so return traffic requires explicit rules in the opposite direction. NACLs support explicit allow and deny entries and are applied at the subnet boundary.  
B. They are stateful.

#### Explications

Incorrect — stateful behavior applies to security groups, not network ACLs. With stateful security groups, response traffic is automatically allowed without an explicit rule; network ACLs require matching rules for both directions because they are stateless.  
**Votre sélection est incorrecte**  
C. They evaluate all rules before allowing traffic.

#### Explications

Incorrect — network ACLs do not evaluate all rules before making a decision. Rules are checked in ascending rule-number order and evaluation stops at the first rule that matches the traffic; that rule's action (allow or deny) is applied.  
**Sélection correcte**  
D. They process rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic.

#### Explications

Network ACLs use ordered rule evaluation: rules are processed starting with the lowest rule number and stop when a match is found. This ordering (and the presence of both allow and deny entries) determines whether a packet is permitted at the subnet boundary.  
E. They operate at the instance level.

#### Explications

Incorrect — network ACLs are associated with subnets, not individual instances. Instance-level access control is provided by security groups, which are attached to network interfaces (ENIs) and operate differently (statefully).  
Explication générale  
This item tests the distinguishing characteristics of network ACLs: they are stateless and use ordered (lowest-number-first) rule evaluation that stops at the first match. Those two behaviors (statelessness and ordered processing) contrast with security groups, which are stateful and applied at the instance/network-interface level.  
Domaine  
Domain 2: Security and Compliance  
Question 77Incorrect  
A company has migrated its workloads to AWS. The company wants to adopt AWS at scale and operate more efficiently and securely. Which AWS service or framework should the company use for operational support?  
A. AWS Support

#### Explications

AWS Support est un service d'assistance technique payant qui fournit une aide personnalisée, des conseils et un accès à des outils de diagnostic (par exemple, les vérifications Trusted Advisor et la gestion technique du compte avec les forfaits supérieurs). Ce service n'assure pas la gestion opérationnelle continue des environnements clients ni la prise en charge des opérations quotidiennes pour le compte du client ; il ne répond donc pas aux besoins d'une assistance opérationnelle gérée à grande échelle.  
B. Cadre d'adoption du cloud AWS (AWS CAF)

#### Explications

Le cadre d'adoption du cloud AWS (AWS CAF) est un ensemble de recommandations, de bonnes pratiques et de perspectives organisationnelles visant à planifier et à aligner les ressources humaines, les processus et les technologies en vue de l'adoption du cloud. Il contribue à définir la stratégie et la gouvernance, mais constitue un cadre de planification plutôt qu'un service opérationnel de gestion et d'exploitation de l'infrastructure AWS.  
**Bonne réponse**  
C. Services gérés AWS (AMS)

#### Explications

AWS Managed Services (AMS) assure la gestion opérationnelle des environnements AWS grâce à des procédures d'exploitation standardisées, l'automatisation, la surveillance, la gestion des incidents et des changements, l'application de correctifs, les sauvegardes et le renforcement de la sécurité. Spécifiquement conçu pour exploiter l'infrastructure AWS pour le compte des clients, il permet d'assurer l'évolutivité, la cohérence opérationnelle et une sécurité renforcée, répondant ainsi au besoin de support opérationnel à grande échelle.  
**Votre réponse est incorrecte**  
D. Cadre d'architecture AWS

#### Explications

Le cadre d'architecture bien conçu (Well-Architected Framework) formalise les meilleures pratiques autour de piliers tels que l'excellence opérationnelle, la sécurité, la fiabilité, l'efficacité des performances et l'optimisation des coûts. L'outil Well-Architected Tool facilite l'évaluation des charges de travail et fournit des recommandations pour la conception et la revue. Il ne s'agit cependant pas d'un service géré assurant l'exploitation continue des charges de travail des clients.  
Explication générale  
La question porte sur une offre permettant de fournir un support opérationnel pour adopter et exploiter AWS à grande échelle. AWS Managed Services est l'offre d'opérations gérées qui exécute et automatise les tâches opérationnelles quotidiennes (surveillance, gestion des incidents, des changements et des correctifs, contrôles de sécurité) pour le compte des clients. Les autres options sont des ressources ou des cadres de référence : le support AWS propose une assistance technique et des outils, le CAF guide la planification de l'adoption et le cadre Well-Architected propose des bonnes pratiques de conception ; aucun ne fournit le service opérationnel géré offert par AMS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 78Correct  
Une entreprise de commerce électronique souhaite répartir le trafic entre les instances Amazon EC2 qui hébergent son site web. Quel service ou ressource AWS répond à ces besoins ?  
**Votre réponse est correcte**  
A. Équilibreur de charge d'application

#### Explications

Un service d'équilibrage de charge AWS de couche 7 conçu pour le trafic HTTP/HTTPS, qui répartit les requêtes entre les instances EC2 enregistrées à l'aide de contrôles d'intégrité, de groupes cibles, d'un routage basé sur le chemin et l'hôte, et d'une terminaison TLS. Il s'intègre à Auto Scaling et offre une haute disponibilité et une tolérance aux pannes pour les applications web, répondant ainsi aux exigences de répartition du trafic web entre les instances EC2.  
B. AWS WAF

#### Explications

A managed web application firewall that protects applications from common exploits (for example, SQL injection and cross‑site scripting) and can be associated with CDN or load‑balancing endpoints. It provides security filtering, not request distribution or traffic balancing across EC2 instances, so it does not satisfy the load‑distribution requirement.  
C. AWS CloudHSM

#### Explications

A managed hardware security module service that provides dedicated HSMs for generating and storing cryptographic keys and performing cryptographic operations (FIPS‑level HSMs). Its purpose is key management and cryptography, not network traffic routing or load balancing.  
D. AWS Direct Connect

#### Explications

A dedicated network connection between an on‑premises data center and AWS that can reduce latency and increase bandwidth predictability. It establishes private connectivity to AWS, but it does not perform load balancing or distribute incoming web traffic across EC2 instances.  
Explication générale  
The question tests knowledge of AWS services used to distribute incoming web traffic across EC2 instances. The correct solution is the Layer‑7 load‑balancing service that provides health checks, target groups, path/host routing and TLS termination and integrates with Auto Scaling to ensure availability. The other options are specialized services (web application firewall, hardware security module, dedicated network connection) that provide security, cryptography, or connectivity benefits but do not perform request distribution across EC2 targets.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 79Correct  
Which design principle is related to the reliability pillar according to the AWS Well-Architected Framework?  
**Votre réponse est correcte**  
A. Test recovery procedures

#### Explications

Aligns with the Reliability pillar because it emphasizes validating system recovery through regular recovery drills, automated failover testing, and disaster recovery exercises. These activities prove that recovery mechanisms work under real conditions, reduce recovery time objectives (RTO) and recovery point objectives (RPO), and increase system fault tolerance and availability.  
B. Experiment more often

#### Explications

This option focuses on rapid experimentation and iterative change, supporting learning and operational agility (Operational Excellence pillar). While valuable for innovation and process improvement, it does not directly validate recovery capabilities or improve availability.  
C. Go global in minutes

#### Explications

This option emphasizes rapid geographic deployment and low‑latency access, mapping primarily to Performance Efficiency and global scalability. It helps with latency and regional redundancy but is not the core practice for validating recovery or resilience.  
D. Analyze and attribute to expenditure

#### Explications

This option concerns cost tracking and allocation, which belongs to the Cost Optimization pillar. Monitoring and attributing expenditure helps control spend but does not directly ensure system recovery, fault tolerance, or availability.  
Explication générale  
Le pilier « Fiabilité » du cadre d'architecture performante concerne la capacité à prévenir les pannes et à s'en remettre. Le choix judicieux consiste à valider les mécanismes de reprise par des tests et des exercices afin de réduire les délais de reprise (RTO/RPO) et d'améliorer la tolérance aux pannes. Les autres options sont, à juste titre, associées à d'autres piliers (Excellence opérationnelle, Efficacité des performances et Optimisation des coûts) et, de ce fait, détournent l'attention de cette question axée sur la fiabilité.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 80Correct  
Un utilisateur a reçu l'autorisation de modifier son mot de passe IAM. Quels services AWS peut-il utiliser pour effectuer cette modification ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Interface de ligne de commande AWS (AWS CLI)

#### Explications

L'action d'API IAM ChangePassword peut être invoquée depuis l'interface de ligne de commande ; avec l'autorisation iam:ChangePassword, un utilisateur peut exécuter la commande AWS CLI (aws iam change-password) pour mettre à jour son mot de passe. L'utilisation de l'interface de ligne de commande ou du SDK est une méthode authentifiée et prise en charge pour la modification autonome des mots de passe.  
B. Service de gestion des clés AWS (AWS KMS)

#### Explications

AWS Key Management Service est un service de gestion des clés de chiffrement pour les opérations cryptographiques (chiffrement/déchiffrement, rotation des clés, signature). Il ne propose pas d'API ni d'interface utilisateur pour modifier le mot de passe d'un utilisateur IAM d'un compte AWS ; il n'est donc pas adapté à cette tâche.  
**Votre sélection est correcte**  
C. Console de gestion AWS

#### Explications

La console de gestion AWS propose une procédure de modification de mot de passe en libre-service (par exemple via Mes informations d'identification de sécurité) qui utilise l'action IAM ChangePassword. Un utilisateur disposant de l'autorisation iam:ChangePassword peut ainsi mettre à jour son mot de passe de console via cette interface web.  
D. AWS Resource Access Manager (AWS RAM)

#### Explications

AWS Resource Access Manager permet de partager des ressources entre comptes AWS et unités organisationnelles. Il est indépendant de l'authentification des utilisateurs et de la gestion des mots de passe IAM et ne propose aucun mécanisme pour modifier le mot de passe d'un utilisateur IAM.  
E. AWS Secrets Manager

#### Explications

AWS Secrets Manager stocke et peut renouveler les secrets tels que les identifiants de base de données, mais ne gère ni ne renouvelle nativement les mots de passe des utilisateurs IAM pour le compte AWS. Bien qu'il soit possible de créer une automatisation personnalisée, Secrets Manager n'est pas le mécanisme pris en charge pour modifier le mot de passe de connexion AWS d'un utilisateur IAM.  
Explication générale  
La modification du mot de passe d'un utilisateur IAM requiert l'autorisation \`iam:ChangePassword\` et peut être effectuée via les interfaces AWS compatibles qui appellent cette API : la console de gestion (pages de modification de mot de passe en libre-service) ou les méthodes en ligne de commande/SDK (l'interface de ligne de commande invoquant \`aws iam change-password\`). Les autres services mentionnés (KMS, RAM, Secrets Manager) ont des fonctions différentes (clés de chiffrement, partage de ressources et stockage/rotation des secrets, respectivement) et ne fournissent pas de mécanisme intégré permettant à un utilisateur IAM de modifier son mot de passe de connexion AWS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 81Correct  
Une entreprise doit pouvoir acquérir des ressources lorsqu'elle en a besoin. Elle doit également pouvoir les libérer lorsqu'elles ne sont plus nécessaires. Quel concept AWS correspond aux objectifs de l'entreprise ?  
A. Évolutivité

#### Explications

La scalabilité décrit la capacité d'augmenter ou de diminuer la capacité d'un système pour répondre aux exigences de charge de travail (verticale ou horizontale). Elle indique qu'un système peut gérer la croissance, mais n'implique pas nécessairement un provisionnement et une suppression automatiques et en temps réel des ressources ; les actions de mise à l'échelle peuvent être manuelles, planifiées ou nécessiter des modifications architecturales.  
B. Durabilité

#### Explications

Cela concerne les considérations environnementales et d'efficacité énergétique (par exemple, la réduction de l'empreinte carbone et l'optimisation de l'utilisation des ressources pour une utilisation durable). Il s'agit d'un objectif de gouvernance/conception qui ne répond pas à l'exigence d'acquérir et de libérer automatiquement des ressources à la demande.  
**Votre réponse est correcte**  
C. Élasticité

#### Explications

Répond à l'exigence de provisionnement et de suppression automatiques de ressources en fonction de l'évolution de la demande. Sur AWS, ce comportement est mis en œuvre par des fonctionnalités et des services tels que les groupes Auto Scaling EC2, les politiques de suivi des applications et des cibles, la mise à l'échelle automatique sans serveur pour AWS Lambda et les services gérés qui ajustent automatiquement la capacité ; autant d'éléments qui permettent l'acquisition et la libération de ressources à la demande afin d'optimiser les coûts et les performances.  
D. Excellence opérationnelle

#### Explications

Ce concept se concentre sur les pratiques organisationnelles, l'automatisation des processus, la surveillance et l'amélioration continue des systèmes d'exploitation et des charges de travail. L'excellence opérationnelle améliore le fonctionnement et la surveillance des systèmes, mais ne décrit pas spécifiquement la mise à l'échelle automatisée du cycle de vie de l'infrastructure pour répondre à la demande.  
Explication générale  
Ce scénario exige l'acquisition et la libération automatiques de ressources en fonction de la demande, ce que décrit au mieux le concept d'élasticité du cloud. L'élasticité met l'accent sur le provisionnement et le déprovisionnement à la demande, souvent automatisés (implémentés dans AWS via Auto Scaling, la mise à l'échelle sans serveur et la mise à l'échelle automatique des services managés). Les autres options décrivent des concepts connexes mais distincts : la scalabilité (capacité à croître, pas nécessairement automatiquement), la durabilité (objectifs environnementaux et d'efficacité) et l'excellence opérationnelle (processus et opérations).  
Domaine  
Domaine 1 : Concepts du cloud  
Question 82Correct  
Un client utilise une instance Amazon Linux EC2 à la demande pendant 3 heures, 5 minutes et 6 secondes. Pour quelle durée sera-t-il facturé ?  
A. 3 heures, 5 minutes

#### Explications

Incorrect. Pour les instances EC2 Linux/Unix, AWS utilise une facturation à la seconde (avec un minimum de 60 secondes) ; les secondes supplémentaires sont donc facturées au lieu d’être supprimées ; tronquer les secondes sous-estimerait le temps facturé.  
**Votre réponse est correcte**  
B. 3 heures, 5 minutes et 6 secondes

#### Explications

Exact. Les instances Amazon EC2 On-Demand Linux/Unix sont facturées à la seconde (avec un minimum de 60 secondes), donc c'est le temps d'exécution réel, mesuré en secondes, qui est utilisé pour calculer le coût.  
C. 3 heures, 6 minutes

#### Explications

Incorrect. La facturation à la seconde signifie que les secondes restantes sont facturées en secondes, et non arrondies à la minute supérieure ; l’arrondi à la minute n’est pas le comportement de facturation pour les instances Linux/Unix.  
D. 4 heures

#### Explications

Incorrect. AWS n'arrondit pas la consommation typique des instances EC2 à la demande Linux/Unix à l'heure supérieure ; une facturation à l'heure entraînerait une surfacturation importante par rapport à une facturation à la seconde.  
Explication générale  
Cette question teste la granularité de la facturation EC2. Les instances EC2 Linux/Unix à la demande sont facturées à la seconde, avec un minimum de 60 secondes ; les frais reflètent donc la durée d'exécution exacte en secondes. Les réponses qui supposent une troncature à la minute ou un arrondi à l'heure supérieure ne sont pas conformes à la facturation à la seconde d'AWS.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 83Correct  
Quel service AWS offre des capacités d'apprentissage automatique pour détecter et analyser le contenu des images et des vidéos ?  
A. Amazon Connect

#### Explications

Ce service est l'offre de centre de contact d'AWS pour les interactions vocales et par chat, avec des fonctionnalités de routage, d'analyse et d'expérience client. Il ne s'agit pas d'un service géré de vision par ordinateur ou d'analyse d'images/vidéos, bien que les flux de contact puissent faire appel à des services d'apprentissage automatique via Lambda si nécessaire.  
B. Voile lumineuse Amazon

#### Explications

Ce produit fournit des serveurs virtuels simples, du stockage et une connectivité réseau pour les petites applications et les sites web. Il ne s'agit pas d'un service géré d'apprentissage automatique ou de vision par ordinateur et il ne propose pas d'API intégrées d'analyse de contenu image/vidéo.  
C. Amazon Personnaliser

#### Explications

Il s'agit d'un service de personnalisation/recommandation géré permettant de proposer des recommandations de produits ou de contenus adaptées à chaque utilisateur. Il privilégie le filtrage collaboratif et contextuel plutôt que l'analyse des médias visuels.  
**Votre réponse est correcte**  
D. Reconnaissance d'Amazon

#### Explications

Il s'agit du service de vision par ordinateur géré d'AWS offrant des API pré-entraînées et des opérations vidéo asynchrones pour la détection d'étiquettes/d'objets, la détection et la reconnaissance de visages, le texte (OCR), la détection de célébrités et de contenus dangereux, le suivi de personnes et l'analyse d'activité/de scène — exactement les capacités requises pour détecter et analyser le contenu des images et des vidéos.  
Explication générale  
La question porte sur le service AWS permettant la détection et l'analyse d'images et de vidéos par apprentissage automatique. Le service de vision par ordinateur managé offre des API prêtes à l'emploi pour la détection d'objets, de scènes et de visages, la reconnaissance optique de caractères (OCR), la détection de contenu inapproprié et l'analyse vidéo, ce qui en fait le choix idéal. Les autres options concernent les fonctionnalités de centre de contact, l'hébergement de ressources de calcul simples ou la personnalisation/les recommandations et ne proposent pas d'API intégrées d'analyse d'images/vidéos.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 84Correct  
Une entreprise a déployé une application dans plusieurs régions AWS à travers le monde. Elle souhaite améliorer les performances et la disponibilité de cette application. Quel service AWS répondra à ces exigences ?  
**Votre réponse est correcte**  
A. Accélérateur mondial AWS

#### Explications

Utilise le réseau mondial AWS et les adresses IP statiques Anycast pour acheminer les clients vers le point de terminaison régional optimal et sain ; assure l’optimisation de la latence au niveau du réseau et le basculement automatique entre les régions et s’intègre aux points de terminaison ALB/NLB/EC2 pour améliorer les performances et la disponibilité globales.  
B. Amazon DataZone

#### Explications

Un service de gouvernance et de catalogage des données permettant de découvrir et de gérer les actifs de données ; il ne fournit pas de routage du trafic réseau, d’optimisation de la latence ni de basculement interrégional, il ne peut donc pas améliorer les performances ou la disponibilité des applications globales.  
C. Carte du cloud AWS

#### Explications

Solution de découverte de services qui enregistre et résout les instances de service (DNS/API) pour les microservices. Elle facilite la localisation des services, mais ne prend pas en charge le routage global du trafic, l'adressage Anycast ni l'optimisation de la latence réseau entre les régions.  
D. Mise à l'échelle automatique AWS

#### Explications

Automatically adjusts compute capacity (EC2, ECS, etc.) to meet demand within a Region or across Availability Zones, improving resilience and cost-efficiency locally, but it does not route end-user traffic between Regions or optimize global network paths for latency/failover.  
Explication générale  
The question tests global traffic-routing and performance optimization. The correct choice provides network-level routing that steers users to the nearest healthy regional endpoint (reducing latency and enabling cross-Region failover). The distractors focus on data governance (DataZone), service discovery (Cloud Map), or regional capacity scaling (Auto Scaling), none of which offer global traffic routing or network-layer performance improvements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 85Correct  
How does the AWS Enterprise Support Concierge team help users?  
A. Supporting application development

#### Explications

This is incorrect because application development (writing code, building features) is not a service provided by the Enterprise Support Concierge. Customers seeking development work use AWS Professional Services, the AWS Partner Network, or developer tools and support engineers for code-level help.  
B. Providing architecture guidance

#### Explications

This is incorrect because architecture and design guidance are provided by Technical Account Managers (TAMs) and AWS Solutions Architects. The Concierge does not perform solution architecture reviews or design guidance at the technical level.  
**Votre réponse est correcte**  
C. Answering billing and account inquiries

#### Explications

Correct. The Concierge is a team of enterprise-level specialists focused on account- and billing-related matters: they assist with invoices, payments, account setup and management, cost allocation and billing inquiries, and they can open or escalate billing-related cases on behalf of the customer.  
D. Answering questions regarding technical support cases

#### Explications

This is incorrect because resolution of technical troubleshooting and case diagnostics is handled by AWS support engineers and technical teams. The Concierge may help route or open cases related to billing or account issues but does not provide deep technical case resolution.  
Explication générale  
The question targets AWS support roles for enterprise customers. The Enterprise Support Concierge is a specialist group that handles account and billing matters (invoicing, payments, account setup and billing cases). Technical architecture advice and application development support are provided by TAMs, Solutions Architects, Professional Services, or support engineers, which makes the billing/account-focused option the best choice.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 86Correct  
A company needs to host an application in a specific geographic area to comply with regulations. Which feature of the AWS global infrastructure will help the company meet this requirement?  
A. Scalability

#### Explications

Ce concept décrit la capacité à augmenter ou à diminuer la capacité (exemples : mise à l’échelle automatique, mise à l’échelle des instances Amazon EC2, mise à l’échelle sans serveur). Il concerne la gestion de la charge variable, et non l’emplacement physique ou légal des ressources hébergées ; les fonctionnalités de mise à l’échelle n’imposent aucune contrainte géographique.  
**Votre réponse est correcte**  
B. Présence mondiale

#### Explications

AWS propose des régions géographiquement isolées, composées de zones de disponibilité, ainsi que des options telles que les zones locales, AWS Outposts et GovCloud. Le choix d'une région spécifique (ou d'une option de déploiement spécifique à une région) permet aux clients de garantir que leurs données et leurs ressources de calcul restent dans la zone géographique requise afin de respecter les exigences réglementaires et de résidence des données.  
C. Disponibilité

#### Explications

Il s'agit de concevoir des systèmes garantissant une haute disponibilité et une grande résilience (par exemple, en répartissant les ressources sur plusieurs zones de disponibilité et en utilisant des services gérés avec des SLA). Bien que la disponibilité améliore la fiabilité, elle ne permet pas, à elle seule, de contrôler l'emplacement géographique des données hébergées ou des charges de travail.  
D. Performance

#### Explications

Cela concerne la latence, le débit et la réactivité, et est pris en charge par des services tels qu'Amazon CloudFront, AWS Global Accelerator et les points de présence en périphérie de réseau. L'optimisation des performances améliore l'expérience utilisateur, mais ne garantit pas le respect des limites légales ou géographiques.  
Explication générale  
Le concept testé décrit comment AWS permet de se conformer aux exigences géographiques ou de résidence des données. Le mécanisme approprié consiste à choisir la région AWS adéquate (et les options de placement régional associées), ce qui garantit que les ressources et les données résident dans la zone géographique requise. D'autres options (évolutivité, disponibilité, performances) sont des caractéristiques importantes du cloud, mais n'offrent pas le contrôle du placement géographique nécessaire à la conformité réglementaire.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 87Correct  
Quel service ou outil AWS complémentaire permet de créer des analyses de rentabilité basées sur les données pour la planification du cloud ?  
**Votre réponse est correcte**  
A. Évaluateur des migrations

#### Explications

AWS Migration Evaluator collecte les données de performance et d'utilisation des charges de travail sur site, produit des profils d'utilisation au niveau du serveur, recommande le dimensionnement approprié et les mappages de services AWS, et génère des rapports sur le coût total de possession (TCO) et les estimations de coûts qui prennent en charge des analyses de rentabilité et une planification de migration quantifiées et basées sur les données.  
B. AWS Billing Conductor

#### Explications

AWS Billing Conductor est un outil permettant d'organiser et de personnaliser la présentation des frais AWS sur l'ensemble des comptes et des groupes de facturation (refacturation/affichage) ; il n'ingère pas de données de télémétrie sur site et ne produit pas d'analyse des coûts de migration ni de résultats TCO nécessaires à l'élaboration d'une analyse de rentabilité pour la migration vers le cloud.  
C. Console de facturation AWS

#### Explications

La console de facturation AWS (et les outils de gestion des coûts associés) offre une visibilité sur les factures AWS, les rapports de coûts, les budgets et les analyses Cost Explorer des dépenses cloud, mais elle ne permet pas de découvrir les ressources sur site ni de générer les recommandations de coûts et de dimensionnement spécifiques à la migration nécessaires à une analyse de rentabilité.  
D. Prévisions Amazon

#### Explications

Amazon Forecast is an ML service for time‑series forecasting (demand, inventory, financial metrics). It produces predictive forecasts from historical data and is unrelated to workload discovery, cost estimation, or migration planning.  
Explication générale  
The question tests recognition of the AWS tool designed specifically for migration planning and business-case creation. The correct tool ingests on‑premises telemetry and outputs server‑level usage profiles, right‑sizing recommendations, and TCO/cost estimates to support migration decisions. The other options relate to billing presentation, cost visibility, or forecasting and do not perform workload discovery or migration cost analysis.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 88Correct  
A company wants to provide access to Windows file shares in AWS from its on-premises workloads. The company does not want to provision any additional infrastructure or applications in its data center. Which AWS service will meet these requirements?  
**Votre réponse est correcte**  
A. Amazon FSx File Gateway

#### Explications

Provides a Storage Gateway that proxies SMB traffic to a fully managed Windows file system in AWS, enabling on‑premises Windows clients to mount and use SMB shares hosted in the cloud without maintaining a Windows file server locally. It integrates with Active Directory and offers caching/low‑latency access patterns appropriate for file share use cases.  
B. AWS DataSync

#### Explications

A managed data transfer service designed to copy files and objects between on‑premises storage and AWS. It performs efficient, scheduled or one‑time transfers and replication, but does not present a live SMB/Windows file share interface that on‑premises workloads can mount for continuous access.  
C. Amazon S3

#### Explications

An object storage service accessed via APIs (and S3 semantics), not a native SMB/Windows file‑share protocol implementation. It does not provide a mountable Windows file share (SMB) interface required for standard on‑premises Windows file share access.  
D. AWS Snow Family

#### Explications

A set of physical, rugged edge devices intended for large-scale data transfer and edge computing in disconnected or limited‑connectivity scenarios. These devices are for importing/exporting data and are not intended to provide persistent, mountable SMB file shares for ongoing on‑premises access.  
Explication générale  
The requirement is to let on‑premises Windows workloads mount and use Windows (SMB) file shares hosted in AWS without running or managing a Windows file server locally. The Storage Gateway option that proxies SMB to Amazon FSx for Windows File Server meets this need by exposing mountable SMB shares backed by a managed FSx file system. The other choices are transfer tools, object storage, or data‑migration hardware and do not provide a live SMB mountable file share for continuous on‑premises access.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 89Correct  
Which maintenance task is the customer’s responsibility, according to the AWS shared responsibility model?  
A. Physical connectivity among Availability Zones

#### Explications

This responsibility falls under AWS’s management of the physical infrastructure and networking fabric. AWS owns and maintains the data centers and the physical network links between Availability Zones; customers work with virtual networking constructs (VPCs, subnets, route tables) rather than the physical layer.  
B. Network switch maintenance

#### Explications

Maintenance and replacement of physical switching hardware are part of AWS’s infrastructure operations. Customers are responsible for configuring virtual networking (security groups, NACLs, VPC routing) but do not perform maintenance on AWS-owned switch hardware.  
C. Hardware updates and firmware patches

#### Explications

Firmware upgrades and hardware patching for servers, storage, and network devices are performed by AWS as part of their infrastructure upkeep. Customers are not responsible for physical server or firmware maintenance under the shared responsibility model.  
**Votre réponse est correcte**  
D. Amazon EC2 updates and security patches

#### Explications

For Amazon EC2 (an IaaS offering), customers control the guest operating system, middleware, and applications; that includes applying OS updates and security patches, configuring patch management, and remediating vulnerabilities. This is an example of the customer’s "security in the cloud" responsibilities (contrast with AWS’s "security of the cloud").  
Explication générale  
Under the AWS shared responsibility model AWS is responsible for the security and maintenance of the underlying cloud infrastructure (physical facilities, hardware, networking). Customers are responsible for what they run in the cloud — for EC2 instances that includes the guest OS, installed software, and security/patching of that software. Therefore the task that correctly maps to customer responsibility is managing EC2 updates and security patches; the other options describe AWS-managed infrastructure responsibilities.  
Domaine  
Domain 2: Security and Compliance  
Question 90Correct  
Which AWS Support plan provides the full set of AWS Trusted Advisor checks at the LOWEST cost?  
A. AWS Developer Support

#### Explications

Incorrect — AWS Developer Support includes only a limited (core) subset of Trusted Advisor checks intended for early development and troubleshooting. The full set of checks (across cost optimization, performance, security, fault tolerance, and service limits) is not included in Developer.  
**Votre réponse est correcte**  
B. AWS Business Support

#### Explications

Correct — AWS Business Support provides access to the complete set of Trusted Advisor checks across all categories. It is the lowest-cost AWS support tier that grants full Trusted Advisor access; Enterprise also provides the full set but at a higher price and with additional enterprise services.  
C. AWS Enterprise On-Ramp Support

#### Explications

Incorrect — 'Enterprise On-Ramp' is not one of the four standard AWS Support tiers (Basic, Developer, Business, Enterprise) that define Trusted Advisor access. The full Trusted Advisor checkset is associated with Business and Enterprise plans.  
D. AWS Enterprise Support

#### Explications

Incorrect — Le support AWS Enterprise inclut bien les vérifications complètes de Trusted Advisor et des services supplémentaires de niveau entreprise (par exemple, un gestionnaire de compte technique et un service de conciergerie), mais il s'agit du niveau le plus cher, ce n'est donc pas l'option la moins coûteuse pour un accès complet à Trusted Advisor.  
Explication générale  
Ce test évalue vos connaissances sur les niveaux de support AWS et l'accès à Trusted Advisor. Seuls les supports Business et Enterprise proposent l'ensemble des vérifications Trusted Advisor ; le support Business est l'offre la plus économique incluant ces vérifications. Les supports Developer (et Basic) offrent un accès limité, voire inexistant, à l'ensemble des vérifications Trusted Advisor, tandis que le support Enterprise inclut toutes les vérifications ainsi que des services Enterprise supplémentaires, moyennant un coût plus élevé.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 91Correct  
Quel service AWS une entreprise peut-elle utiliser pour stocker et chiffrer en toute sécurité les mots de passe d'une base de données ?  
A. Bouclier AWS

#### Explications

AWS Shield est un service de protection contre les attaques par déni de service distribué (DDoS) géré, qui protège les applications au niveau du réseau et du transport. Il ne propose pas d'API de stockage, de rotation ou de récupération des secrets, ni de chiffrement des secrets basé sur un système de gestion de clés (KMS), et n'est donc pas adapté au stockage des mots de passe de bases de données.  
**Votre réponse est correcte**  
B. Gestionnaire de secrets AWS

#### Explications

AWS Secrets Manager assure le stockage sécurisé et la gestion du cycle de vie des informations d'identification et autres secrets. Il chiffre les secrets à l'aide d'AWS KMS, prend en charge la récupération par programmation via des API/SDK et peut effectuer une rotation automatisée des secrets (souvent via Lambda) ainsi qu'un contrôle d'accès précis avec IAM — des fonctionnalités qui le rendent particulièrement adapté à la gestion des mots de passe de bases de données.  
C. Gestion des identités et des accès AWS (IAM)

#### Explications

AWS Identity and Access Management (IAM) gère les identités, les rôles et les autorisations des ressources AWS. IAM permet d'accorder ou de refuser l'accès aux services (y compris Secrets Manager), mais ne constitue pas un service de stockage de secrets et n'offre aucun mécanisme de rotation ou de récupération des informations d'identification des applications.  
Monsieur Amazon Cognito

#### Explications

Amazon Cognito gère l'inscription, la connexion, les groupes d'utilisateurs et la fédération d'identités pour les applications, et émet des jetons d'authentification. Il est axé sur l'authentification de l'utilisateur final et la gestion des sessions, et non sur le stockage sécurisé ou le renouvellement des identifiants d'application ou de base de données.  
Explication générale  
AWS Secrets Manager est la solution idéale, car elle est conçue pour stocker, chiffrer (avec KMS), faire tourner les secrets et fournir un accès programmatique contrôlé aux mots de passe de bases de données. Les autres services répondent à des besoins différents : Shield protège contre les attaques DDoS, IAM gère les identités et les autorisations (mais pas le stockage des secrets) et Cognito assure l’authentification des utilisateurs pour les applications.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 92Correct  
Quel service AWS permet aux entreprises de déployer une application au plus près des utilisateurs finaux ?  
**Votre réponse est correcte**  
A. Amazon CloudFront

#### Explications

CloudFront place des copies en cache du contenu sur un réseau mondial de points de présence et traite les requêtes depuis le point de présence le plus proche afin de réduire la latence. Il prend en charge la diffusion de contenu statique et dynamique, s'intègre aux serveurs d'origine (S3, EC2, ALB) et à des fonctionnalités telles que Lambda@Edge pour l'exécution de la logique en périphérie, permettant ainsi de déployer efficacement les applications au plus près des utilisateurs finaux.  
B. Mise à l'échelle automatique AWS

#### Explications

AWS Auto Scaling manages the number of compute resources (for example EC2 instances) to match demand within a region or across availability zones. It addresses capacity and cost optimization, not geographic proximity or edge delivery, so it does not by itself place an application closer to end users.  
C. AWS AppSync

#### Explications

AWS AppSync is a managed GraphQL service that simplifies connecting clients to data sources and supports real-time and offline capabilities. It solves API/data access patterns, not content distribution or edge deployment, so it does not provide the geographic edge presence needed to deliver an application close to users.  
D. Amazon Route 53

#### Explications

Amazon Route 53 is a DNS service that can route users to endpoints using policies (latency-based, geolocation, failover), but it only directs traffic — it does not host or cache application content at edge locations. To reduce user-perceived latency via proximity, Route 53 is used in combination with geographically distributed endpoints or a CDN like CloudFront.  
Explication générale  
The question tests knowledge of services that reduce latency by bringing application content closer to users. A CDN with global edge locations and caching is the correct mechanism; CloudFront provides that capability. The other options manage compute scaling (Auto Scaling), API access (AppSync), or DNS routing (Route 53), which support availability and routing but do not by themselves provide edge hosting/caching.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 93Correct  
Which AWS service provides DNS resolution?  
A. Amazon CloudFront

#### Explications

CloudFront is a global content delivery network that caches and serves content from edge locations to reduce latency. It relies on DNS to route users but does not provide authoritative or recursive DNS services for domain management or resolution.  
B. Amazon VPC

#### Explications

A VPC is an isolated virtual network. It includes an internal DNS resolver (the Amazon-provided DNS in each VPC) for resolving instance hostnames and private records, but it is not the AWS service for managing public DNS zones or global DNS routing.  
**Votre réponse est correcte**  
C. Amazon Route 53

#### Explications

Route 53 is AWS’s managed DNS service that provides authoritative DNS resolution for public and private hosted zones, domain registration, multiple routing policies (simple, weighted, latency, failover), health checks, and integration with VPCs and hybrid environments. This is the service used to manage and resolve domain names in AWS.  
D. AWS Direct Connect

#### Explications

Direct Connect creates dedicated network connections between on-premises networks and AWS for private network traffic. It improves connectivity and bandwidth/latency characteristics but does not perform DNS resolution or host DNS services.  
Explication générale  
La question porte sur le service AWS qui effectue la résolution DNS. Amazon Route 53 est la bonne réponse, car il s'agit du service DNS faisant autorité d'AWS et de gestion des domaines pour les zones hébergées publiques et privées. Les autres options sont des services de réseau et de distribution : CloudFront est un CDN qui utilise le DNS pour le routage, mais n'est pas un fournisseur DNS ; un VPC offre un résolveur interne pour les noms d'hôtes des instances, mais pas pour la gestion DNS publique ; Direct Connect fournit uniquement une connectivité dédiée.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 94Correct  
Quel service ou outil AWS aide les utilisateurs à visualiser, comprendre et gérer leurs dépenses et leur utilisation au fil du temps ?  
A. Organisations AWS

#### Explications

Il offre une gestion centralisée des comptes, un contrôle des politiques et une facturation consolidée sur plusieurs comptes AWS (unités organisationnelles, politiques de contrôle des services et facturation consolidée), mais il n'inclut pas la visualisation interactive des coûts, l'analyse des coûts historiques ou les tableaux de bord de prévision nécessaires pour analyser les dépenses au fil du temps.  
B. Calculateur de prix AWS

#### Explications

Il s'agit d'un outil de prévision et de planification permettant d'estimer les coûts des architectures et configurations proposées ; il n'intègre pas l'historique d'utilisation ni ne produit de rapports interactifs sur les dépenses historiques ou de visualisations de coûts en séries chronologiques.  
**Votre réponse est correcte**  
C. AWS Cost Explorer

#### Explications

Il propose des graphiques et des rapports interactifs et filtrables pour les données historiques de coûts et d'utilisation, prend en charge le regroupement par service, compte lié, étiquette et type d'utilisation, et inclut des recommandations de prévision et de réservation, ce qui en fait le service AWS conçu pour analyser et gérer les dépenses au fil du temps.  
D. Catalogue de services AWS

#### Explications

Gère les portefeuilles de produits approuvés et applique les normes d'approvisionnement des ressources (catalogues, portefeuilles, contraintes), mais ne fournit pas d'analyses historiques des coûts ni de rapports de dépenses chronologiques.  
Explication générale  
Cette question évalue vos connaissances des outils de gestion des coûts AWS. La bonne réponse est Cost Explorer, car ce service propose des tableaux de bord interactifs, des filtres, des fonctions de regroupement, des rapports historiques sur les coûts et l'utilisation, ainsi que des prévisions permettant de visualiser et de gérer les dépenses dans le temps. Les autres options offrent la gestion de compte (Organizations), l'estimation des coûts pour les architectures planifiées (Pricing Calculator) ou la gouvernance du provisionnement (Service Catalog), mais aucune ne propose l'analyse des coûts en séries temporelles offerte par Cost Explorer.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 95Correct  
Une entreprise souhaite s'engager dès le départ à utiliser ses instances Amazon EC2 de production de manière continue en échange d'une réduction de ses coûts globaux. Quelles options tarifaires répondent à ces exigences au coût le plus bas ? (Choisissez deux réponses.)  
A. Exemples ponctuels

#### Explications

Il s'agit d'instances interruptibles offrant de la capacité EC2 disponible à prix fortement réduits, mais pouvant être résiliées par AWS avec un préavis très court. N'offrant aucun engagement de réservation ou de facturation à long terme, elles ne permettent pas de garantir la continuité de la capacité de production ni la réduction des coûts prévisible et garantie dès le départ dont nous avons besoin.  
B. Instances à la demande

#### Explications

Ce modèle de tarification est horaire/à la seconde, sans engagement à long terme. Il offre une flexibilité maximale pour les charges de travail variables ou de courte durée, mais affiche le prix par utilisation le plus élevé et ne propose pas les remises pour engagement initial mentionnées dans la question.  
**Votre sélection est correcte**  
C. Instances réservées

#### Explications

A multi-year commitment that reduces EC2 hourly rates by applying a reservation to matching usage. Options include term lengths (1 or 3 years), payment choices (no/partial/all upfront) and different RI types (Standard vs Convertible). RIs yield predictable, substantial discounts for steady, production workloads by committing to instance usage attributes or a reservation applied to matching usage.  
**Votre sélection est correcte**  
D. Savings Plans

#### Explications

A commitment to a consistent dollar-per-hour amount of compute usage for 1 or 3 years that automatically applies discounted rates across eligible compute services. Savings Plans (Compute and EC2 Instance Savings Plans) provide similar or greater discounts than RIs while offering greater flexibility across instance families, sizes and regions, making them ideal for lowering long-term compute costs through a usage commitment.  
E. Dedicated Hosts

#### Explications

A physical, single-tenant server that provides placement and licensing control. It addresses compliance and licensing requirements rather than being a primary mechanism for the lowest-cost, committed pricing for typical EC2 production workloads; it can be more expensive and is not the standard option for upfront cost reduction requests.  
Explication générale  
The question tests knowledge of AWS pricing models that lower EC2 costs through an upfront or term commitment. Reserved Instances and Savings Plans are the correct choices because both require a defined, multi-year commitment and apply significant discounts to steady EC2 usage. The distractors either offer no long-term commitment (On‑Demand), are interruptible spare capacity (Spot), or serve a different purpose such as dedicated physical tenancy (Dedicated Hosts).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 96Correct  
Which AWS Well-Architected Framework pillar focuses on structured and streamlined allocation of computing resources?  
A. Reliability

#### Explications

This pillar addresses designing systems to perform reliably under expected and unexpected conditions. It emphasizes availability, fault tolerance, recovery planning, and detecting and responding to failures — concerns about resiliency rather than optimizing how compute resources are allocated or sized.  
B. Operational excellence

#### Explications

This pillar covers operational processes, procedures, monitoring, runbooks, and continuous improvement of operational practices (how you operate and evolve systems). It focuses on procedures and organization-level practices instead of techniques for selecting or right‑sizing compute resources.  
**Votre réponse est correcte**  
C. Performance efficiency

#### Explications

This pillar concerns selecting optimal resource types and sizes, using elasticity and scaling, right‑sizing instances, and adopting serverless or managed services to meet performance requirements efficiently. Typical AWS practices include instance type selection, Auto Scaling, caching, Amazon CloudFront, and CloudWatch metrics to monitor and adapt resource allocation to workload demand.  
D. Sustainability

#### Explications

Ce pilier vise à réduire l'impact environnemental grâce à une utilisation efficace des ressources et à des choix de conception qui diminuent la consommation d'énergie et l'empreinte carbone. Bien qu'il recoupe les objectifs d'efficacité, son but premier est la durabilité environnementale plutôt que l'allocation et le dimensionnement structurés des ressources de calcul pour atteindre des objectifs de performance.  
Explication générale  
Cette question évalue votre connaissance des piliers du cadre AWS Well-Architected. La bonne réponse est le pilier relatif au choix et à l'utilisation efficace des ressources de calcul, de stockage et de réseau (dimensionnement, mise à l'échelle et choix d'architecture). Les autres piliers portent sur la disponibilité/résilience, les pratiques opérationnelles ou l'impact environnemental et n'abordent donc pas principalement l'allocation structurée des ressources de calcul.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 97Correct  
Une entreprise doit configurer et gérer de manière centralisée les groupes de sécurité Amazon VPC sur plusieurs comptes AWS au sein d'une organisation AWS Organizations. Quel service AWS doit-elle utiliser pour répondre à ces besoins ?  
**Votre réponse est correcte**  
A. Gestionnaire de pare-feu AWS

#### Explications

Firewall Manager s'intègre à AWS Organizations pour créer et appliquer des stratégies de groupe de sécurité aux comptes membres et aux VPC. Il évalue en continu la conformité, détecte les groupes de sécurité non conformes et, une fois configuré, applique ou corrige automatiquement les règles de manière centralisée. Il constitue ainsi le service idéal pour la configuration et l'application des stratégies de groupe de sécurité VPC à l'échelle de l'organisation.  
B. Amazon GuardDuty

#### Explications

Amazon GuardDuty est un service de détection des menaces géré qui analyse les journaux de flux VPC, les journaux d'événements AWS CloudTrail et les journaux DNS afin de générer des rapports de sécurité. Il assure la détection et l'émission d'alertes, mais ne propose pas de configuration centralisée ni d'application des règles de groupes de sécurité entre les comptes.  
C. Détective Amazon

#### Explications

Amazon Detective facilite la visualisation et l'analyse des anomalies de sécurité en examinant et en représentant graphiquement les relations entre les activités et les journaux des comptes. Cet outil d'investigation permet d'identifier les causes profondes des problèmes ; il ne gère ni ne déploie de modifications de configuration auprès des groupes de sécurité.  
D. AWS WAF

#### Explications

AWS WAF est un pare-feu d'applications web qui protège les points de terminaison HTTP/S (par exemple, via CloudFront, Application Load Balancer ou API Gateway) à l'aide de règles appliquées au trafic de la couche application. Il ne gère pas les groupes de sécurité VPC ni la configuration des groupes de sécurité entre comptes.  
Explication générale  
Cette question évalue vos connaissances des services AWS pour la gestion centralisée des politiques de sécurité au sein d'AWS Organizations. La solution appropriée est le service permettant de créer, d'appliquer et de corriger les politiques de groupe de sécurité VPC sur plusieurs comptes. Les services de détection et d'investigation (GuardDuty, Detective) et la protection de la couche application (WAF) ne prennent pas en charge la configuration et l'application centralisées des groupes de sécurité VPC et ne conviennent donc pas à ce besoin.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 98Correct  
Une entreprise connecte plusieurs VPC et réseaux sur site. Elle souhaite utiliser un service AWS comme routeur cloud afin de simplifier les relations de peering. Quel service AWS peut-elle utiliser pour répondre à ce besoin ?  
A. AWS Direct Connect

#### Explications

Incorrect. AWS Direct Connect provides private, dedicated network connectivity between on-premises datacenters and AWS. It is a connectivity method (and can be associated with Direct Connect Gateway), but it does not function as a centralized cloud router that provides transitive routing and hub-and-spoke connectivity across multiple VPCs on its own.  
**Votre réponse est correcte**  
B. AWS Transit Gateway

#### Explications

Correct. AWS Transit Gateway provides a centralized, regional hub for connecting VPCs, VPNs, and on-premises networks. It supports attachments, centralized route tables and route propagation, and transitive routing so you avoid a full-mesh of VPC peering connections; it also integrates with Direct Connect and supports inter-region peering for multi-region architectures.  
C. Amazon Connect

#### Explications

Incorrect. Amazon Connect is a cloud contact-center service for customer engagement and telephony; it has no role in L3 network routing or connecting multiple VPCs and on-premises networks.  
D. Amazon Route 53

#### Explications

Incorrect. Amazon Route 53 is a DNS and domain name management service (including private hosted zones for name resolution). It resolves domain names but does not perform inter-VPC L3 routing or act as a cloud router.  
Explication générale  
This question tests AWS networking fundamentals: the correct choice is the managed hub service that provides centralized routing and simplifies multi-VPC and on-premises connectivity. AWS Transit Gateway is designed for hub-and-spoke connectivity, centralized route tables, and transitive routing, which removes the need for complex full-mesh peering. The other options are either connectivity methods (Direct Connect), DNS (Route 53), or unrelated application services (Amazon Connect), and therefore do not fulfill the requirement to act as a cloud router.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 99Correct  
What does Amazon CloudFront provide?  
A. Automatic scaling for all resources to power an application from a single unified interface

#### Explications

Incorrect. Automatic scaling of compute and other resources is provided by AWS Auto Scaling and related services (for example, Application Auto Scaling, Amazon EC2 Auto Scaling). CloudFront is not a scaling/orchestration service; it is a content distribution layer that caches and serves content from edge locations.  
**Votre réponse est correcte**  
B. Secure delivery of data, videos, applications, and APIs to users globally with low latency

#### Explications

Correct. Amazon CloudFront is AWS's global content delivery network (CDN) that uses a worldwide network of edge locations to cache and deliver content closer to users. It supports secure delivery (HTTPS), integrates with AWS Shield and AWS WAF for DDoS and web-application protection, and works with origins such as Amazon S3, ALBs, API Gateway, and custom origins to reduce latency and improve transfer performance.  
C. Ability to directly manage traffic globally through a variety of routing types, including latency-based routing, geo DNS, geoproximity, and weighted round robin

#### Explications

Incorrect. The features described (latency-based routing, geolocation-based routing, geoproximity, weighted routing) are DNS routing policies provided by Amazon Route 53\. CloudFront does not perform DNS-level traffic routing or provide those Route 53 routing policies.  
D. Automatic distribution of incoming application traffic across multiple targets, such as Amazon EC2 instances, containers, IP addresses, and AWS Lambda functions

#### Explications

Incorrect. Distributing incoming application traffic across targets (EC2 instances, containers, IP addresses, Lambda, etc.) is the responsibility of Elastic Load Balancing (Application Load Balancer, Network Load Balancer). CloudFront focuses on caching and delivering content at edge locations rather than balancing live application traffic across backend targets.  
Explication générale  
The question tests recognition of Amazon CloudFront as AWS's CDN. CloudFront improves performance and security by caching and delivering static and dynamic content from a global edge network and integrates with services like S3, ALB, API Gateway, AWS Shield, and WAF. The other choices describe separate AWS services: Auto Scaling (scaling resources), Route 53 (DNS routing policies), and Elastic Load Balancing (distributing application traffic).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 100Correct  
A company wants to rightsize its Amazon EC2 instances. Which configuration change will meet this requirement with the LEAST operational overhead?  
A. Add EC2 instances in another Availability Zone.

#### Explications

Distributing instances across Availability Zones improves fault tolerance and availability by reducing the blast radius of an AZ failure, but it does not change instance size or address over‑ or under‑provisioning. Adding AZs can increase cost and management without achieving right‑sizing.  
**Votre réponse est correcte**  
B. Change the size and type of the EC2 instances based on utilization.

#### Explications

Using utilization‑based instance sizing leverages CloudWatch metrics and AWS Compute Optimizer recommendations and can be automated with Auto Scaling or deployment pipelines to select appropriate instance families and sizes. This targets actual CPU/memory/network usage to reduce over‑provisioning while minimizing manual operational work.  
C. Convert the payment method from On-Demand to Savings Plans.

#### Explications

Changing the payment model to Savings Plans reduces costs for sustained usage by committing to spend, but it does not alter instance types or resource allocation and therefore does not perform right‑sizing or reduce the operational effort required to adjust capacities.  
D. Reprovision the EC2 instances with a larger instance type.

#### Explications

Manually reprovisioning instances to a larger type requires stopping/modifying/replacing instances (or rebuilding AMIs), can cause downtime, increases management overhead, and risks over‑provisioning; it is more operationally intensive than using measurement and automated adjustment tools.  
Explication générale  
The core concept is right‑sizing EC2 instances with minimal operational overhead. The best approach is to base instance type and size decisions on observed utilization and use AWS tools (CloudWatch, Compute Optimizer, Auto Scaling) to automate or guide adjustments. Options that focus on availability (AZ distribution), cost commitment (Savings Plans), or manual scale‑up increase complexity or do not address sizing directly and are therefore inferior for this goal.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 101Incorrect  
A company needs access to checks and recommendations that help the company follow AWS best practices for cost optimization, security, fault tolerance, performance, and service quotas. Which combination of an AWS service and AWS Support plan on the AWS account will meet these requirements?  
**Votre réponse est incorrecte**  
A. AWS Trusted Advisor with AWS Developer Support

#### Explications

Incorrect. The Developer Support plan provides only a limited subset of AWS Trusted Advisor checks. Full access to all Trusted Advisor checks (including comprehensive cost-optimization, security, fault-tolerance, performance, and service-quota checks) requires Business or Enterprise Support. Developer is intended for non-production or early development use and does not meet the requirement for complete best-practice recommendations.  
B. AWS Health Dashboard with AWS Enterprise Support

#### Explications

Incorrect. AWS Health Dashboard reports service and account-level events and ongoing AWS service issues; it does not perform best-practice checks across cost, security, performance, fault tolerance, or quotas. Although Enterprise Support customers do receive full Trusted Advisor checks, selecting the Health Dashboard as the service does not provide the required checks and recommendations.  
**Bonne réponse**  
C. AWS Trusted Advisor with AWS Business Support

#### Explications

Correct. The Business Support plan includes full access to all AWS Trusted Advisor checks and recommendations across the primary categories (cost optimization, security, fault tolerance, performance, and service limits/quotas). Trusted Advisor provides actionable best-practice guidance and can be accessed via the console and APIs; Business (and Enterprise) customers receive the complete set of checks needed to meet the company’s requirements.  
D. AWS Health Dashboard with AWS Enterprise On-Ramp Support

#### Explications

Incorrect. Pairing the AWS Health Dashboard with an Enterprise On‑Ramp style support offering does not deliver Trusted Advisor’s full best-practice checks. The Health Dashboard focuses on service health events, and On‑Ramp or limited enterprise variants do not change the fact that Trusted Advisor (with full checks) is the tool required for proactive recommendations across the requested domains.  
Explication générale  
This question tests knowledge of AWS support plans and the Trusted Advisor service. Trusted Advisor provides best-practice checks and recommendations across cost optimization, security, fault tolerance, performance, and service quotas, but full access to all checks is only included with Business and Enterprise Support. Options that choose the Health Dashboard or the Developer plan are incorrect because they either provide service health information (not best-practice checks) or only a limited subset of Trusted Advisor checks. Therefore, Trusted Advisor combined with Business Support best satisfies the requirement.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 102Correct  
Which AWS service could an administrator use to provide desktop environments for several employees?  
A. AWS Organizations

#### Explications

Incorrect — AWS Organizations is used for centrally managing multiple AWS accounts, billing, organizational units, and applying Service Control Policies. It does not provide any capability to deliver or host end-user desktop sessions.  
B. AWS Fargate

#### Explications

Incorrect — AWS Fargate is a serverless compute engine for running containerized workloads (ECS/EKS) without managing servers or clusters. It’s for application compute, not for provisioning virtual desktops for users.  
C. AWS WAF

#### Explications

Incorrect — AWS WAF is a web application firewall that protects HTTP/HTTPS applications from common web exploits and bots. It is a security control for web traffic and does not provide desktop provisioning or user desktop access.  
**Votre réponse est correcte**  
D. AWS WorkSpaces

#### Explications

Correct — This service is AWS’s Desktop-as-a-Service offering: it delivers persistent virtual Windows or Linux desktops from the cloud, integrates with Active Directory, provides client access (desktop/web/mobile), and supports centralized provisioning, security controls, and per-user or hourly billing, making it the appropriate choice for supplying desktops to employees.  
Explication générale  
The question tests recognition of the AWS service used to deliver cloud-based desktop environments. The correct choice is the AWS DaaS offering, which enables administrators to provision, manage, and secure persistent virtual desktops integrated with enterprise identity. The distractors are account management (Organizations), container compute (Fargate), and a web firewall (WAF), none of which supply end-user desktop sessions.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 103Correct  
A company wants to query its server logs to gain insights about its customers’ experiences. Which AWS service will store this data MOST cost-effectively?  
A. Amazon Aurora

#### Explications

Designed as a managed relational database engine for OLTP workloads, this service uses a relational schema and transactional optimizations. Storing large volumes of semi-structured or unstructured logs in a relational database is costly and operationally unnecessary compared with object storage and does not provide the best cost-per-GB for archival or bulk log retention.  
B. Amazon Elastic File System (Amazon EFS)

#### Explications

This is a managed, POSIX-compliant network file system for EC2 instances, optimized for shared file access and low-latency workloads. Its billing model and performance characteristics make it more expensive than object storage for long-term, high-volume log retention, and it lacks the native integration with serverless query tools used for large-scale log analysis.  
C. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Block storage volumes attach to individual EC2 instances and are intended for instance-backed file systems and databases with provisioned performance. They are not optimized for scalable, low-cost archival of large log datasets because capacity is tied to attached instances and typical pricing is higher than object storage for bulk data.  
**Votre réponse est correcte**  
D. Amazon S3

#### Explications

Object storage with high durability and flexible, low-cost storage classes plus lifecycle policies for automatic tiering and archival. It integrates with analytics and querying services (for example, Athena, S3 Select) and offers storage classes (Standard, Intelligent‑Tiering, Infrequent Access, Glacier) that minimize long-term costs for large volumes of logs while preserving queryability and durability.  
Explication générale  
The question tests understanding of AWS storage types and cost-effectiveness for large-volume log retention and analysis. Object storage is the best fit because it provides low cost per GB, lifecycle transition to archival classes, strong durability, and native integration with query and analytics services. File systems and block volumes are intended for active file or instance storage and transactional workloads and are generally more expensive and less scalable for long-term log storage; relational databases are optimized for structured transactional data, not bulk log archival.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 104Correct  
Which of the following are pillars of the AWS Well-Architected Framework? (Choose two.)  
A. Availability

#### Explications

This concept is not listed as a separate pillar in the Well‑Architected Framework. Elements commonly associated with availability (for example, fault isolation, redundancy, and failover) are addressed within the Reliability pillar rather than as an independent pillar.  
**Votre sélection est correcte**  
B. Reliability

#### Explications

Correct. The Reliability pillar focuses on designing systems that recover from infrastructure or service disruptions, scale to meet demand, and automatically mitigate failures. Relevant AWS concepts include fault isolation, backups, multi‑AZ/multi‑Region deployment patterns, health checks, Amazon CloudWatch monitoring, Auto Scaling, and resilient managed services.  
C. Scalability

#### Explications

Scalability is an important design goal but is covered under the Performance Efficiency pillar (which addresses using computing resources efficiently and scaling to meet business needs) rather than being a separate Well‑Architected pillar.  
D. Responsive design

#### Explications

This term refers to UI/web design that adapts to different screen sizes and is not one of the Well‑Architected pillars. It’s not relevant to the framework’s focus on operational, security, reliability, performance, cost, and sustainability practices.  
**Votre sélection est correcte**  
E. Operational excellence

#### Explications

Correct. The Operational Excellence pillar covers processes and procedures for running and evolving systems, including automation, change management, operations as code, monitoring and incident response, runbooks, and continuous improvement. AWS tooling commonly used to support this pillar includes CloudFormation, AWS Config, Systems Manager, and CI/CD pipelines.  
Explication générale  
The AWS Well‑Architected Framework defines six pillars: Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability. The best answers are the pillars that exactly match the framework: Reliability (designing for fault tolerance, recovery, and availability) and Operational Excellence (processes, automation, and continuous improvement). The other choices describe important cloud concepts (availability and scalability) or unrelated topics (responsive design) but are not named pillars in the framework.  
Domaine  
Domain 1: Cloud Concepts  
Question 105Correct  
A company wants to migrate its on-premises NoSQL workload to Amazon DynamoDB. Which AWS service will meet this requirement?  
A. AWS Migration Hub

#### Explications

Incorrect. AWS Migration Hub provides a central dashboard to track migration progress across multiple tools and projects; it does not perform data replication, transformation, or database-level migrations into targets such as Amazon DynamoDB.  
**Votre réponse est correcte**  
B. AWS Database Migration Service (AWS DMS)

#### Explications

Correct. AWS Database Migration Service (DMS) performs data migrations and continuous replication to supported targets, including Amazon DynamoDB. DMS supports full-load and change-data-capture (CDC) flows from supported NoSQL sources (for example MongoDB), allows basic data mapping/transformation during migration, and is designed to minimize downtime during cutover.  
C. Migration Evaluator

#### Explications

Incorrect. Migration Evaluator (formerly TSO Logic) is a discovery and cost‑estimation service used for migration planning and TCO analysis; it does not migrate or replicate database contents to AWS targets.  
D. AWS Application Migration Service

#### Explications

Incorrect. AWS Application Migration Service automates lift‑and‑shift rehosting of servers (VMs/physical machines) into Amazon EC2 and migrates system images and applications, but it is not intended for migrating database records into a managed NoSQL service like DynamoDB.  
Explication générale  
This question assesses knowledge of AWS migration tools for database workloads. AWS DMS is the correct choice because it is purpose‑built to migrate and replicate data (including from some NoSQL sources) into Amazon DynamoDB with support for full-load and CDC and basic data mapping. The other options are migration planning/tracking (Migration Hub, Migration Evaluator) or server rehosting (Application Migration Service), none of which perform database content migration into DynamoDB.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 106Correct  
Which Amazon EC2 pricing model is the MOST cost efficient for an uninterruptible workload that runs once a year for 24 hours?  
**Votre réponse est correcte**  
A. On-Demand Instances

#### Explications

C’est la solution idéale car le modèle de tarification ne facture que l’utilisation réelle, sans engagement à long terme et avec une facturation à la seconde, ce qui rend une exécution unique de 24 heures, sans interruption, la moins chère par rapport aux options qui nécessitent des engagements pluriannuels ou comportent un risque d’interruption.  
B. Cas réservés

#### Explications

Les instances réservées nécessitent un engagement d'un ou trois ans (instances réservées standard ou convertibles) et sont optimisées pour une utilisation stable, prévisible et à long terme ; leur engagement initial/à long terme les rend inefficaces pour une seule tâche de 24 heures une fois par an.  
C. Exemples ponctuels

#### Explications

Les instances Spot offrent le prix le plus bas, mais elles sont interruptibles (AWS peut récupérer de la capacité avec peu de préavis), elles ne conviennent donc pas aux charges de travail qui doivent s'exécuter sans interruption, malgré leur avantage en termes de coûts pour les tâches tolérantes aux pannes.  
D. Instances dédiées

#### Explications

Les instances dédiées (matériel mono-locataire) existent pour répondre aux besoins de conformité ou de licences et ont des coûts plus élevés que la location partagée ; elles ne sont pas rentables pour un travail occasionnel et de courte durée, sauf si un hôte dédié est spécifiquement requis.  
Explication générale  
Choisissez le modèle de tarification adapté à la fréquence et à la tolérance aux interruptions. Pour une charge de travail ponctuelle de 24 heures ne devant pas être interrompue, la facturation à la demande (sans engagement à long terme) est la plus économique. Les modèles réservés sont moins chers uniquement pour une utilisation continue à long terme, le modèle ponctuel est moins cher mais sujet aux interruptions, et la location dédiée est plus coûteuse et sert à des fins de conformité et de gestion des licences plutôt qu'à réaliser des économies à court terme.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 107Incorrect  
Quelles fonctionnalités d'AWS Cloud Adoption Framework (AWS CAF) relèvent de la perspective de gouvernance ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Gestion de programmes et de projets

#### Explications

La gestion de programmes et de projets assure la supervision, la gouvernance, la coordination des parties prenantes et le contrôle des livrables nécessaires à la gestion des initiatives d'adoption du cloud. Dans AWS CAF, cette fonctionnalité garantit que les programmes cloud sont exécutés selon une gouvernance, des échéanciers, des rapports et un alignement sur les objectifs de l'entreprise clairement définis.  
B. Gestion des produits

#### Explications

La gestion de produits vise à définir les feuilles de route, les fonctionnalités et la valeur client des produits. Il s'agit d'une discipline métier/produit (axée sur les personnes et les domaines d'activité) plutôt que d'une capacité de gouvernance établissant des contrôles organisationnels, des politiques et une supervision pour l'adoption du cloud.  
**Sélection correcte**  
C. Gestion de portefeuille

#### Explications

La gestion de portefeuille encadre la collecte, la priorisation et le financement des projets et programmes afin que les investissements soient alignés sur la stratégie de l'entreprise. Dans le cadre de la gouvernance AWS CAF, elle garantit que les initiatives cloud sont évaluées, priorisées et gérées comme un portefeuille cohérent, sous contrôle de gouvernance.  
**Votre sélection est incorrecte**  
D. Gestion des risques

#### Explications

La gestion des risques vise à identifier et à atténuer les risques au sein de l'organisation. Bien que les considérations relatives aux risques influencent la gouvernance, l'ensemble de capacités de gouvernance AWS CAF met généralement l'accent sur la gestion de portefeuille et de programme comme principaux contrôles de gouvernance testés ici ; la gestion des risques est souvent traitée comme une préoccupation transversale ou mise en avant dans le cadre des activités de sécurité et de conformité plutôt que comme les deux éléments de gouvernance attendus par la question.  
E. Gestion d'événements

#### Explications

La gestion des événements est une capacité opérationnelle liée à la surveillance, aux incidents et à la réponse opérationnelle. Elle s'inscrit dans une perspective opérationnelle et de sécurité (détection des événements et réponse à ceux-ci) plutôt que dans une perspective de gouvernance axée sur la supervision, les politiques et le contrôle des investissements.  
Explication générale  
Le cadre d'adoption du cloud AWS, dans sa perspective de gouvernance, est axé sur la supervision et le contrôle des initiatives cloud, notamment la gestion des portefeuilles et le pilotage des programmes et projets afin que les investissements et leur exécution soient alignés sur la stratégie de l'entreprise. La gestion des programmes et des projets, ainsi que la gestion de portefeuille, constituent les principales capacités de gouvernance parmi les options proposées ; les autres options concernent les produits, les opérations ou les risques/sécurité transversaux, et non les contrôles de gouvernance mis en avant ici.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 108Correct  
Quel service AWS permet de créer une connexion réseau privée entre l'infrastructure sur site et le cloud AWS ?  
A. Configuration AWS

#### Explications

AWS Config est un service de suivi de la configuration des ressources et d'audit de conformité. Il enregistre les modifications de configuration, évalue les règles de conformité et fournit un historique des configurations de ressources ; il ne provisionne ni ne gère la connectivité réseau entre les environnements sur site et AWS.  
B. Cloud privé virtuel (Amazon VPC)

#### Explications

Amazon VPC fournit un réseau virtuel logiquement isolé dans AWS (sous-réseaux, tables de routage, groupes de sécurité). Il définit l'environnement réseau des ressources AWS, mais ne crée pas par lui-même de connexion physique ou privée à l'infrastructure locale ; vous devez utiliser AWS Direct Connect ou un VPN de site à site et vous connecter via une passerelle privée virtuelle ou une passerelle de transit pour relier un réseau local à un VPC.  
**Votre réponse est correcte**  
C. AWS Direct Connect

#### Explications

Fournit une connexion réseau privée et dédiée entre vos locaux et AWS. Direct Connect offre des interfaces virtuelles privées qui peuvent se connecter directement à un VPC (via une passerelle privée virtuelle ou une passerelle de transit), contourne l'Internet public pour une latence réduite et des performances réseau plus stables, et est proposé sous forme de connexions dédiées ou hébergées via les emplacements AWS et ses partenaires.  
D. Amazon Route 53

#### Explications

Amazon Route 53 est un service DNS et de routage de noms de domaine évolutif (incluant des contrôles d'intégrité et des politiques de trafic). Il résout les noms de domaine et dirige le trafic, mais n'établit pas de connexions privées au niveau du réseau entre les sites sur site et AWS.  
Explication générale  
Ce test évalue vos connaissances en matière de connectivité hybride. AWS Direct Connect est la solution idéale car elle établit une connexion privée et dédiée entre votre réseau local et AWS et permet de présenter des interfaces virtuelles privées aux VPC. D'autres options existent, mais elles ont des finalités différentes : un VPC définit le réseau virtuel côté AWS, mais nécessite Direct Connect ou un VPN pour les liaisons locales ; AWS Config sert à l'audit de la configuration ; Route 53 est un service DNS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 109Incorrect  
Quel service ou fonctionnalité AWS permet de rechercher et d'identifier les ressources AWS partagées en externe ?  
**Votre réponse est incorrecte**  
A. Service Amazon OpenSearch

#### Explications

Recherche et analyse gérées pour l'indexation et l'interrogation de grands ensembles de données (compatible Elasticsearch). Ce module est utilisé pour la recherche dans les journaux et les applications, et non pour l'inspection des politiques basées sur les ressources ou l'identité afin de déterminer si des ressources sont partagées avec des acteurs externes.  
B. Tour de contrôle AWS

#### Explications

Un service de gouvernance et de configuration de comptes qui automatise la mise en place des zones d'atterrissage, des politiques et des garde-fous sur l'ensemble des comptes AWS. Son champ d'application concerne la gouvernance et le provisionnement des comptes, et non l'analyse des politiques ou la détection des ressources partagées en externe.  
**Bonne réponse**  
C. Analyseur d'accès IAM AWS

#### Explications

Ce service d'analyse des politiques évalue les politiques basées sur les ressources et les politiques de confiance afin de déterminer si les ressources sont accessibles aux comptes AWS externes ou au public. Il génère des résultats identifiant les compartiments S3 partagés en externe, les relations de confiance des rôles IAM, les clés KMS et autres ressources prises en charge, et assure une surveillance continue des accès externes et la génération d'alertes.  
D. AWS Fargate

#### Explications

Un moteur de calcul sans serveur pour l'exécution de conteneurs (ECS/EKS) sans gestion de serveurs. Sa fonctionnalité principale est l'exécution et l'orchestration de conteneurs, et non l'inspection des politiques d'accès ou l'identification des ressources AWS partagées en externe.  
Explication générale  
La réponse correcte est le service qui analyse les politiques de ressources et de confiance pour détecter les accès externes. IAM Access Analyzer effectue une analyse logique des politiques et génère des résultats lorsque des ressources sont partagées en dehors de votre compte ou de votre organisation. Les autres options sont axées sur la recherche et l'analyse (OpenSearch), la gouvernance des comptes (Control Tower) ou le calcul conteneurisé (Fargate) et ne permettent donc pas de détecter les partages externes.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 110Correct  
Que peut faire un utilisateur avec AWS CloudTrail ?  
A. Générer un rapport d'informations d'identification des utilisateurs IAM.

#### Explications

Incorrect — IAM fournit un rapport d’identification distinct (GenerateCredentialReport) qui répertorie le mot de passe, la clé d’accès et l’état de l’authentification multifacteur (MFA) pour tous les utilisateurs IAM. CloudTrail ne génère pas de rapports d’identification IAM ; il enregistre l’activité de l’API.  
**Votre réponse est correcte**  
B. Enregistrer les appels API effectués vers les services AWS.

#### Explications

Correct — CloudTrail capture et enregistre l'activité et les événements de l'API du compte (événements de gestion et, en option, événements de données), y compris l'identité de l'appelant, les horodatages, l'adresse IP source, les éléments de requête/réponse, et transmet les journaux à S3, CloudWatch Logs ou CloudTrail Lake à des fins d'audit, d'analyse de sécurité et de dépannage.  
C. Évaluer la conformité des configurations de ressources AWS avec les politiques et les directives.

#### Explications

Incorrect — L’évaluation de la conformité de la configuration des ressources est gérée par AWS Config (instantanés de configuration, historique, règles et packs de conformité). CloudTrail fournit des journaux d’événements des appels d’API, mais n’évalue pas la conformité de la configuration des ressources aux règles de conformité.  
D. Assurez-vous que les instances Amazon EC2 sont mises à jour avec les dernières mises à jour de sécurité.

#### Explications

Incorrect — La gestion des correctifs pour les instances Amazon EC2 est assurée par AWS Systems Manager (Patch Manager et SSM Agent). CloudTrail se contente d’enregistrer les appels d’API liés aux opérations de correctifs ; il n’effectue ni ne garantit l’application des correctifs.  
Explication générale  
AWS CloudTrail is an audit and logging service that records API calls and related events for your AWS account, supporting governance, security analysis, and operational troubleshooting. The correct choice is the option describing API-call recording. The other options describe features provided by other services: IAM’s credential report, AWS Config’s compliance assessments, and Systems Manager’s patching capabilities.  
Domaine  
Domain 2: Security and Compliance  
Question 111Correct  
A company is moving some of its on-premises IT services to the AWS Cloud. The finance department wants to see the entire bill so it can forecast spending limits. Which AWS service can the company use to set spending limits and receive notifications if those limits are exceeded?  
A. AWS Cost and Usage Reports

#### Explications

AWS Cost and Usage Reports (CUR) deliver detailed, granular cost and usage data to an S3 bucket for downstream analysis (e.g., Athena, Redshift, billing pipelines). CUR is a reporting and data-delivery service; it does not provide budget threshold enforcement or alerting functionality.  
**Votre réponse est correcte**  
B. AWS Budgets

#### Explications

AWS Budgets lets you define cost, usage, reservation and Savings Plans budgets and configure threshold-based alerts. Alerts can be sent by email or published to Amazon SNS, and Budgets can trigger automated Budget Actions when thresholds are breached, so it is the service used to set spending limits and receive notifications.  
C. AWS Organizations consolidated billing

#### Explications

AWS Organizations (consolidated billing) centralizes billing and cost aggregation across accounts, enabling consolidated invoices and shared discounts. It does not itself provide budget alerts or limit enforcement—use AWS Budgets to create alerts across member accounts.  
D. Cost Explorer

#### Explications

Cost Explorer provides interactive visualizations, trend analysis and forecasting of AWS costs and usage to help you understand spend patterns. It is an analysis and visualization tool and does not provide threshold-based alerting or spending-limit notifications.  
Explication générale  
The requirement is to set spending limits and receive notifications when those limits are exceeded. AWS Budgets is designed for this purpose—creating budgets, setting thresholds, and sending alerts (email or SNS) or triggering actions. The other services listed provide reporting (Cost and Usage Reports), account-level billing consolidation (Organizations), or visualization and forecasting (Cost Explorer), but they do not provide threshold-based alerting and enforcement the way AWS Budgets does.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 112Correct  
A company wants to assess its operational readiness. It also wants to identify and mitigate any operational risks ahead of a new product launch. Which AWS Support plan offers guidance and support for this kind of event at no additional charge?  
**Votre réponse est correcte**  
A. AWS Business Support

#### Explications

This plan includes 24x7 access to Cloud Support Engineers, the full set of Trusted Advisor checks, and architectural and operational guidance to help prepare for launches and mitigate operational risks. Those features enable readiness assessments and runbook/best-practice guidance without requiring an additional event-specific purchase.  
B. AWS Basic Support

#### Explications

The free tier provides only self-service resources (documentation, whitepapers, forums) and does not include technical support, Trusted Advisor full checks, or proactive operational guidance needed for an event readiness assessment.  
C. AWS Developer Support

#### Explications

This plan targets development and test environments: it offers business-hours access and limited support features but lacks 24x7 support, the full Trusted Advisor checks, and the proactive operational readiness services required for a production launch.  
D. AWS Enterprise Support

#### Explications

This top-tier plan delivers the most comprehensive support (including a Technical Account Manager and higher-touch engagement). However, some event-specific services such as Infrastructure Event Management are tied to Enterprise customers and may incur additional fees, so it is not guaranteed to provide the stated guidance at no extra charge.  
Explication générale  
The question tests knowledge of AWS Support plan capabilities. The Business-level plan provides the operational guidance, Trusted Advisor checks, and 24x7 access needed to assess readiness and identify risks for a launch without requiring an extra paid event service. Basic and Developer lack the needed technical and proactive support, while Enterprise offers broader, higher-touch services but can involve paid add-ons for specific event management.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 113Correct  
Which AWS service allows for file sharing between multiple Amazon EC2 instances?  
A. AWS Direct Connect

#### Explications

Incorrect — AWS Direct Connect is a dedicated network connection service that provides private connectivity between on‑premises environments and AWS. It is not a storage or file‑sharing solution and does not provide a concurrently mountable file system for EC2 instances.  
B. AWS Snowball Edge

#### Explications

Incorrect — AWS Snowball Edge is a physical appliance used to transfer large amounts of data offline and to run edge compute workloads. It is intended for data migration and edge processing, not for providing a managed, network‑mounted file system across EC2 instances.  
C. AWS Backup

#### Explications

Incorrect — AWS Backup centralizes and automates backups for supported AWS services to protect and restore data. It performs backups and restores, but it does not expose a live, concurrently mountable file system for direct file sharing between running EC2 instances.  
**Votre réponse est correcte**  
D. Amazon Elastic File System (Amazon EFS)

#### Explications

Correct — Amazon EFS is a fully managed, POSIX‑compliant network file system (NFS) that multiple EC2 instances can mount concurrently. It provides elastic, shared file storage with consistent file semantics, mount targets in subnets across Availability Zones, and configurable performance/throughput modes suitable for workloads that require shared access.  
Explication générale  
Cette question porte sur la connaissance des services AWS permettant l'accès à des fichiers partagés pour les instances EC2. Le choix approprié est le système de fichiers réseau géré prenant en charge les montages simultanés et la sémantique POSIX (Amazon EFS). Les autres options répondent à des besoins différents : Direct Connect pour les liaisons réseau privées, Snowball Edge pour le transfert de données hors ligne et le calcul en périphérie, et AWS Backup pour la sauvegarde et la restauration ; aucune ne propose un système de fichiers géré et montable simultanément.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 114Correct  
Une entreprise souhaite exploiter ses données et créer des tableaux de bord interactifs de visualisation. Quel service AWS répond à ces besoins ?  
A. Amazon SageMaker

#### Explications

Ce service est dédié à la création, à l'entraînement et au déploiement de modèles d'apprentissage automatique (et non à la gestion de solutions de BI ou de tableaux de bord). Il propose des notebooks, des tâches d'entraînement, l'hébergement de modèles et des fonctionnalités d'apprentissage automatique associées — utiles pour générer des prédictions, mais non pour créer des tableaux de bord de veille stratégique interactifs.  
B. Reconnaissance d'Amazon

#### Explications

Il s'agit d'un service de vision par ordinateur pour l'analyse d'images et de vidéos (détection de visages, d'objets et de textes, modération). Il analyse les médias visuels, mais ne propose pas d'outils pour l'agrégation de données commerciales tabulaires ni pour la création de tableaux de bord visuels interactifs.  
**Votre réponse est correcte**  
C. Amazon QuickSight

#### Explications

Il s'agit du service de business intelligence sans serveur et géré d'AWS, conçu pour les tableaux de bord et les visualisations interactifs. Il offre des connecteurs natifs aux sources de données, un moteur d'accélération en mémoire (SPICE) pour des requêtes rapides, des visualisations intégrables, des analyses basées sur le machine learning (détection d'anomalies, prévisions) et une intégration avec IAM pour le contrôle d'accès, répondant ainsi aux besoins d'analyse et de création de tableaux de bord interactifs.  
D. Amazon Kinesis

#### Explications

Cette suite gère l'ingestion et le traitement en temps réel des données (flux, Firehose, analyses) pour capturer et traiter les données d'événements. Elle convient à l'alimentation des pipelines d'analyse, mais ne constitue pas un service de visualisation décisionnelle ou de tableaux de bord dédié ; des outils supplémentaires sont nécessaires pour visualiser les données traitées.  
Explication générale  
Le besoin porte sur un service de business intelligence/tableaux de bord géré. Le service AWS BI, qui propose des tableaux de bord interactifs, évolutifs et sans serveur, des requêtes rapides (SPICE), des connecteurs de données natifs et des analyses basées sur le machine learning, s'avère être la solution idéale. Les autres options, axées sur le cycle de vie des modèles de machine learning, l'analyse d'images/vidéos ou l'ingestion de données en flux continu, ne répondent pas directement au besoin en matière de tableaux de bord/BI.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 115Correct  
Quel service AWS est toujours disponible gratuitement pour les utilisateurs ?  
A. Amazone Athéna

#### Explications

Athena est un service de requêtes interactives sans serveur pour les données stockées sur Amazon S3. La facturation est basée sur le volume de données analysées (par téraoctet analysé) et sur les coûts S3 associés. Il s'agit d'un service à l'usage, non systématiquement gratuit.  
**Votre réponse est correcte**  
B. Gestion des identités et des accès AWS (IAM)

#### Explications

La gestion des identités et des accès (IAM) est incluse sans frais supplémentaires avec un compte AWS. La création d'utilisateurs, de groupes, de rôles ou de stratégies est gratuite. (Remarque : des frais peuvent s'appliquer pour les services ou fonctionnalités connexes tels que AWS Directory Service, les intégrations AWS Identity Center, le stockage des journaux CloudTrail ou d'autres ressources AWS.)  
C. AWS Secrets Manager

#### Explications

Secrets Manager is a managed secrets storage and rotation service that charges per secret (monthly) and for API usage; it is a paid service and not always free.  
D. Amazon ElastiCache

#### Explications

ElastiCache is a managed in‑memory caching service; pricing is based on node type and hours, data transfer, and optional backup/replication—therefore it incurs usage charges and is not free.  
Explication générale  
This question tests knowledge of which core AWS services are provided without additional charge. IAM is a foundational identity and access management capability included free with an AWS account, while Athena, Secrets Manager, and ElastiCache are managed services billed based on usage (queries/data scanned, secrets per month/API calls, and cache node hours respectively). Hence IAM is the correct choice.  
Domaine  
Domain 1: Cloud Concepts  
Question 116Correct  
Which AWS services or features give users the ability to create a network connection between two VPCs? (Choose two.)  
A. VPC endpoints

#### Explications

Provides private connectivity from a VPC to supported AWS services (gateway endpoints for S3/DynamoDB) or to service consumers via AWS PrivateLink (interface endpoints). These mechanisms do not create a general-purpose VPC-to-VPC network connection and cannot be used as a substitute for VPC-level routing between two arbitrary VPCs.  
B. Amazon Route 53

#### Explications

A scalable DNS and domain registration service used for name resolution, routing policies, and private hosted zones. It can help resolve names across VPCs (with shared/private hosted zones), but it does not establish or carry network traffic between VPCs — it only provides DNS functionality.  
**Votre sélection est correcte**  
C. VPC peering

#### Explications

Establishes a private, routable network link between two VPCs by adding route-table entries so instances can communicate directly. Supports intra- and inter-region peering, requires non-overlapping CIDR ranges, and does not provide transitive routing through a third VPC.  
D. AWS Direct Connect

#### Explications

Provides dedicated network connectivity between on-premises networks and AWS locations. While it can be combined with gateways (Direct Connect Gateway, Virtual Private Gateway) to reach VPCs, Direct Connect by itself does not create a VPC-to-VPC connection and is intended for on-premises-to-AWS connectivity.  
**Votre sélection est correcte**  
E. AWS Transit Gateway

#### Explications

Acts as a central hub for connecting many VPCs and on-premises networks, using attachments and Transit Gateway route tables to enable scalable, transitive routing among connected networks. Designed for large-scale VPC interconnection and simplifies management compared to many point-to-point links.  
Explication générale  
Cette question teste la connaissance des primitives réseau AWS pour la connectivité inter-VPC. Les deux mécanismes corrects sont la liaison de peering point à point (adaptée aux connexions directes sans routage transitif) et Transit Gateway (un service en étoile permettant une connectivité transitive et évolutive entre de nombreux VPC et réseaux sur site). Les autres options remplissent des rôles différents : les points de terminaison et PrivateLink offrent un accès privé aux services, Route 53 gère le DNS et Direct Connect assure la connectivité sur site plutôt que de relier directement deux VPC.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 117Correct  
Une entreprise souhaite exécuter efficacement ses charges de travail dans le cloud AWS, réduire les coûts de gestion et améliorer ses processus. Quel pilier du framework AWS Well-Architected correspond à ces exigences ?  
A. Fiabilité

#### Explications

Incorrect. Le pilier Fiabilité vise à concevoir des systèmes disponibles, tolérants aux pannes, capables de reprendre leurs activités et résilients, afin que les charges de travail remplissent leur fonction prévue dans le temps. Il se concentre sur la robustesse et la reprise du système, et non sur la réduction des coûts opérationnels ou l'amélioration des processus d'exploitation.  
**Votre réponse est correcte**  
B. Excellence opérationnelle

#### Explications

Exact. Le pilier « Excellence opérationnelle » du cadre AWS Well-Architected couvre l'exécution et la surveillance des systèmes pour fournir de la valeur commerciale, l'automatisation des procédures opérationnelles (opérations en tant que code), l'établissement de manuels d'exploitation et de scénarios, et l'amélioration continue des processus — autant d'éléments qui réduisent la gestion manuelle et améliorent les opérations.  
C. Efficacité de la performance

#### Explications

Incorrect. Le pilier « Efficacité des performances » concerne le choix des types et des tailles de ressources appropriés, la surveillance des performances et une architecture évolutive pour répondre aux exigences du système. Il vise une utilisation efficace du calcul, du stockage et du réseau plutôt que l'amélioration des processus et de la gestion opérationnelle.  
D. Optimisation des coûts

#### Explications

Incorrect. Le pilier « Optimisation des coûts » se concentre sur la conception axée sur les coûts, le dimensionnement approprié, les options d'achat et le suivi des coûts afin de minimiser les dépenses. Bien que l'automatisation puisse réduire certaines tâches, ce pilier ne traite pas principalement des procédures opérationnelles ni de l'amélioration des processus.  
Explication générale  
Cette question évalue la compréhension des piliers du cadre AWS Well-Architected. L'excellence opérationnelle est le pilier approprié car elle cible explicitement la manière dont les charges de travail sont exploitées et améliorées, notamment la surveillance, l'automatisation et l'amélioration continue des processus afin de réduire les coûts de gestion. Les autres piliers (fiabilité, efficacité des performances et optimisation des coûts) traitent respectivement de la disponibilité/résilience, de l'efficacité/mise à l'échelle des ressources et du contrôle des coûts ; ils ne correspondent donc pas au scénario.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 118Correct  
Une entreprise souhaite améliorer en continu ses processus et procédures afin de générer de la valeur ajoutée. À quel pilier du cadre AWS Well-Architected correspond cet objectif ?  
A. Efficacité de la performance

#### Explications

L'objectif est de sélectionner et d'optimiser les ressources de calcul, de stockage et de réseau (par exemple, dimensionnement adéquat des instances, mise à l'échelle automatique, mise en cache et choix de services gérés) afin d'atteindre les objectifs de performance et de coût. Il s'agit de choix de ressources et d'architecture visant à améliorer le débit et la latence, et non d'améliorer en continu les processus et procédures opérationnels.  
**Votre réponse est correcte**  
B. Excellence opérationnelle

#### Explications

L'approche est axée sur les processus et les pratiques opérationnelles : considérer les opérations comme du code, apporter fréquemment de petites modifications, automatiser les tâches répétitives, maintenir des manuels d'exploitation, instrumenter les systèmes pour l'observabilité et utiliser les outils AWS (CloudFormation, Systems Manager, CloudWatch, AWS Config, etc.) pour mesurer, apprendre et itérer. Ces capacités permettent directement l'amélioration continue des processus et la création de valeur pour l'entreprise.  
C. Fiabilité

#### Explications

Ce document traite de la conception de systèmes garantissant la disponibilité, la tolérance aux pannes et la capacité de récupération (par exemple, les déploiements multi-AZ, le basculement automatique, les sauvegardes et les procédures de restauration). Il assure la fiabilité des charges de travail dans le temps, mais ne se concentre pas principalement sur l'amélioration continue des procédures.  
D. Durabilité

#### Explications

L’objectif est de réduire l’impact environnemental grâce à une utilisation efficace des ressources et à des choix architecturaux durables (par exemple, un dimensionnement adapté, le recours à des services gérés et un traitement efficace des données). Cette approche vise des résultats en matière de développement durable plutôt que l’amélioration des processus et procédures opérationnels.  
Explication générale  
La question porte sur le pilier « Well-Architected » qui vise l'amélioration continue des processus et des procédures pour générer de la valeur ajoutée pour l'entreprise. Le pilier pertinent met l'accent sur les pratiques opérationnelles telles que l'automatisation, le développement logiciel, l'observabilité et l'apprentissage itératif afin d'optimiser l'exécution et la gestion des charges de travail. Les autres piliers se concentrent sur l'optimisation des performances, la résilience du système ou l'impact environnemental et ne décrivent donc pas principalement l'amélioration continue des processus.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 119Correct  
Quel est l'avantage d'utiliser AWS pour le cloud computing ?  
A. Échanger les charges variables contre des charges fixes

#### Explications

Incorrect. Cette affirmation inverse le modèle économique habituel de l'adoption du cloud. AWS et le cloud computing transforment généralement d'importantes dépenses d'investissement initiales (coûts fixes liés aux centres de données sur site) en dépenses d'exploitation variables (paiement à l'usage).  
**Votre réponse est correcte**  
B. Tarification à l'utilisation

#### Explications

Exact. Les modèles de tarification d'AWS permettent aux clients de ne payer que pour les ressources qu'ils provisionnent et consomment (par exemple, facturation à la seconde pour les instances EC2 Linux, par requête/invocation pour Lambda et tarification du stockage par paliers pour S3), ce qui permet une flexibilité des coûts et la possibilité d'adapter les coûts à l'utilisation.  
C. Diminution de la vitesse et de l'agilité

#### Explications

Incorrect. AWS améliore la vitesse et l'agilité en fournissant des ressources de calcul à la demande, des services gérés, l'automatisation (CloudFormation, Elastic Beanstalk, Lambda) et une infrastructure mondiale, ce qui accélère le déploiement et l'itération au lieu de les ralentir.  
D. Dépenses liées à l'exploitation et à la maintenance des centres de données

#### Explications

Incorrect. Consacrer du temps et de l'argent à l'exploitation de centres de données physiques est une caractéristique des infrastructures sur site. Avec AWS, AWS gère l'infrastructure physique sous-jacente (modèle de responsabilité partagée), réduisant ainsi la charge opérationnelle du client.  
Explication générale  
L'avantage principal testé est la tarification à l'usage d'AWS, qui transforme les dépenses informatiques, passant d'investissements initiaux importants à des coûts variables alignés sur l'utilisation réelle, ce qui améliore l'efficacité et l'évolutivité. Les autres options sont trompeuses : l'une inverse l'avantage économique, une autre décrit un résultat contraire aux avantages du cloud, et la dernière décrit un inconvénient de l'infrastructure sur site plutôt qu'un avantage du cloud.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 120Correct  
Quel avantage du cloud AWS permet aux entreprises de réduire leurs coûts d'utilisation grâce à l'utilisation agrégée de tous les utilisateurs AWS ?  
A. Inutile de deviner la capacité

#### Explications

Cette option décrit l'élasticité et la capacité d'adapter la capacité à la demande (par exemple, Auto Scaling et les instances à la demande). Cette capacité réduit les dépenses inutiles liées au surdimensionnement, mais n'explique pas pourquoi AWS peut proposer des prix unitaires inférieurs grâce à la consommation combinée de nombreux clients.  
B. Capacité à se déployer à l'international en quelques minutes

#### Explications

Cela fait référence à la présence mondiale d'AWS (régions, zones de disponibilité et services comme Amazon CloudFront) qui permet un déploiement géographique rapide et une latence réduite. Il s'agit de couverture et de disponibilité, et non du mécanisme qui réduit les coûts unitaires grâce à la mutualisation de la demande client.  
**Votre réponse est correcte**  
C. Économies d'échelle

#### Explications

L'infrastructure mutualisée et de grande envergure d'AWS, ainsi que la demande partagée des clients, permettent de réaliser des économies d'échelle, d'optimiser l'utilisation des ressources et d'accroître l'efficacité opérationnelle. Ces facteurs réduisent le coût unitaire du fournisseur (et ont permis à AWS de baisser ses prix au fil du temps) et lui permettent de répercuter les économies sur ses clients ; c'est cet avantage concurrentiel fondamental qui est mis à l'épreuve.  
D. Vitesse et agilité accrues

#### Explications

Cette option permet un provisionnement et un développement plus rapides (services gérés, infrastructure en tant que code), ce qui réduit les délais de mise sur le marché. Bien qu'elle puisse diminuer les coûts indirects, elle n'est pas la principale raison pour laquelle AWS peut proposer des tarifs d'utilisation plus bas grâce à la taille de sa clientèle.  
Explication générale  
Cette question teste l'hypothèse selon laquelle l'avantage concurrentiel d'AWS en matière de coûts provient de la mutualisation de la demande entre de nombreux clients, ce qui permet de réaliser des économies d'échelle, d'optimiser l'utilisation des ressources et d'améliorer l'efficacité opérationnelle, réduisant ainsi les coûts unitaires. D'autres avantages mentionnés (mise à l'échelle élastique, déploiement mondial et agilité accrue) constituent des atouts importants d'AWS, mais n'expliquent pas à eux seuls la baisse des prix résultant de l'utilisation agrégée.  
Domaine  
Domaine 1 : Concepts du cloud

