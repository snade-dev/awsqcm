Question 1Correct  
Quelle perspective du cadre d'adoption du cloud AWS (AWS CAF) inclut une capacité pour une architecture de données et d'analyse bien conçue ?  
A. Sécurité

#### Explications

La perspective de sécurité vise à protéger les informations et les systèmes (gestion des identités et des accès, chiffrement, gestion des clés, contrôle du réseau, journalisation et détection). Bien qu'elle sécurise les données et les contrôles associés, elle ne prend pas en charge la conception technique des architectures d'ingestion, de stockage, de traitement et d'analyse des données.  
B. Gouvernance

#### Explications

La perspective de gouvernance se concentre sur les politiques, la conformité, la structure des comptes, la gestion des risques et les contrôles organisationnels (par exemple, AWS Organizations, les politiques et les cadres de conformité). Elle définit qui prend les décisions et comment, plutôt que la conception technique au niveau de la plateforme des solutions de données et d'analyse.  
C. Opérations

#### Explications

La perspective Opérations couvre les processus et capacités opérationnels tels que la surveillance, la réponse aux incidents, les procédures d'exploitation et les outils opérationnels (CloudWatch, Systems Manager, automatisation des procédures d'exploitation). Elle garantit la fiabilité des services, mais ne définit pas l'architecture de la plateforme pour les charges de travail de données et d'analyse.  
**Votre réponse est correcte**  
D. Plateforme

#### Explications

La perspective Plateforme englobe la conception et la mise en œuvre de la plateforme cloud et des services fondamentaux nécessaires au développement d'applications, notamment les capacités d'architecture de données et d'analyse. Cela comprend la définition de modèles de stockage et de traitement évolutifs, l'ingestion et le streaming des données, le catalogage et l'ETL des données, ainsi que la sélection et l'assemblage de services managés (par exemple Amazon S3, AWS Glue, Amazon Redshift, Amazon Athena, Amazon EMR, Amazon Kinesis) afin de répondre aux exigences d'évolutivité, de disponibilité, d'intégration et de performance.  
Explication générale  
La perspective Plateforme d'AWS CAF est responsable de l'architecture technique et des services fondamentaux de la plateforme cloud, notamment des architectures de données et d'analyse bien conçues (ingestion, stockage, traitement, analyse et intégration avec les services gérés). Les autres perspectives (Sécurité, Gouvernance et Opérations) concernent la protection, la gouvernance et l'exploitation de cette plateforme, mais ne sont pas principalement responsables de la conception technique des solutions de données et d'analyse.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 2Correct  
Quel composant doit être connecté à un VPC pour permettre l'accès Internet entrant ?  
A. Passerelle NAT

#### Explications

Ce service assure une connectivité Internet sortante uniquement pour les instances situées dans des sous-réseaux privés en traduisant les adresses IP privées en adresses IP publiques. Du fait de la traduction d'adresses réseau (NAT) à la source pour les connexions sortantes, il ne crée pas de chemin routable pour le trafic entrant non sollicité provenant d'Internet.  
B. Point de terminaison VPC

#### Explications

Ce système crée une connectivité privée et interne à AWS pour les services AWS ou les services de points de terminaison pris en charge, évitant ainsi que le trafic ne transite par l'Internet public. Cette architecture maintient le trafic au sein du réseau AWS et, par conséquent, ne connecte pas le VPC à l'Internet public ni n'autorise l'accès à Internet depuis ce réseau.  
C. Connexion VPN

#### Explications

Établit une connexion chiffrée entre un VPC et un réseau externe (par exemple, sur site) pour une communication sécurisée entre sites. Le VPC n'est pas accessible publiquement sur Internet et n'est pas utilisé pour recevoir du trafic Internet entrant.  
**Votre réponse est correcte**  
D. Passerelle Internet

#### Explications

Un composant VPC redondant et à mise à l'échelle horizontale qui fournit une cible dans les tables de routage pour le trafic Internet (par exemple, une route 0.0.0.0/0). Associé à une adresse IP publique, aux entrées appropriées dans les tables de routage et aux contrôles de sécurité (groupes de sécurité/ACL), il permet la communication Internet entrante et sortante des instances.  
Explication générale  
Une passerelle Internet doit être associée à un VPC pour fournir un chemin routable vers Internet. Les instances nécessitent également des adresses IP publiques (ou des adresses IP élastiques), des entrées dans la table de routage pointant vers la passerelle et des règles de groupe de sécurité/ACL permissives pour accepter le trafic entrant. Les autres options répondent à des besoins différents : la solution NAT assure la traduction uniquement pour le trafic sortant, les points de terminaison VPC permettent un accès privé aux services AWS sans passer par Internet et les VPN établissent une connexion sécurisée aux réseaux externes sans exposer le VPC au trafic Internet entrant.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 3Correct  
Une entreprise migre ses environnements de développement et de test vers AWS afin d'accroître son agilité et de réduire ses coûts. Ces environnements n'étant pas destinés à la production et les serveurs n'étant pas utilisés à pleine capacité, une indisponibilité ponctuelle est acceptable. Quel est le modèle tarifaire Amazon EC2 le plus avantageux pour répondre à ces exigences ?  
A. Instances réservées

#### Explications

Les instances réservées (IR) offrent une réduction sur la facturation en échange d'un engagement à long terme et sont optimisées pour les charges de travail prévisibles et stables. Elles sont moins adaptées aux charges de travail intermittentes hors production qui peuvent tolérer des interruptions, car les IR nécessitent une utilisation continue pour bénéficier d'économies maximales.  
B. Instances à la demande

#### Explications

Les instances à la demande sont facturées à l'heure ou à la seconde, sans engagement, et conviennent aux charges de travail imprévisibles ou de courte durée. Elles offrent une grande flexibilité, mais sont plus coûteuses que les alternatives qui exploitent la capacité disponible ou proposent des options moins onéreuses ; elles ne constituent donc pas le choix le plus rentable dans ce cas précis.  
**Votre réponse est correcte**  
C. Exemples ponctuels

#### Explications

Les instances Spot utilisent la capacité EC2 disponible à prix fortement réduits et sont conçues pour les charges de travail tolérant les interruptions. Lorsque AWS a besoin de récupérer cette capacité, les instances Spot peuvent être libérées rapidement, ce qui les rend idéales pour les environnements de développement et de test privilégiant les économies à la disponibilité garantie.  
D. Hôtes dévoués

#### Explications

Les serveurs dédiés allouent un serveur physique entier à un seul client pour répondre à des exigences de licence ou de conformité. Ils engendrent des coûts nettement plus élevés et sont destinés aux charges de travail nécessitant du matériel dédié ou des licences spécifiques, ce qui ne convient pas à un environnement hors production où les coûts sont un facteur déterminant.  
Explication générale  
Cette question évalue la connaissance des modèles de tarification d'EC2 et la capacité à optimiser les coûts en fonction des exigences de disponibilité. Pour les environnements de développement et de test hors production tolérant des interruptions ponctuelles, l'utilisation de capacités disponibles (instances Spot) offre les économies les plus importantes. Les instances réservées et les instances à la demande privilégient la disponibilité ou la flexibilité, au prix d'un coût plus élevé, tandis que les hôtes dédiés privilégient l'isolation matérielle et la conformité plutôt que la réduction des coûts.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 4Correct  
Une entreprise doit effectuer des recherches textuelles dans des documents stockés sur Amazon S3. Quel service AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Amazon Kendra

#### Explications

Fournit une solution de recherche d'entreprise entièrement gérée qui peut explorer et indexer les documents stockés dans Amazon S3 (et d'autres référentiels), prend en charge les requêtes en langage naturel, le réglage de la pertinence, les index chiffrés et le contrôle d'accès précis via AWS IAM — des fonctionnalités qui permettent une recherche de texte efficace dans les collections de documents.  
B. Reconnaissance d'Amazon

#### Explications

Un service de vision par ordinateur pour l'analyse d'images et de vidéos (détection d'objets/de visages, analyse de scènes et détection de texte dans les images). Il peut détecter le texte dans les images, mais ne propose pas l'indexation de documents, la recherche en langage naturel ni la recherche à l'échelle de l'entreprise pour les fichiers stockés sur S3.  
C. Amazon Polly

#### Explications

Un service de synthèse vocale (TTS) qui convertit un texte en audio. Il n'effectue ni extraction de texte, ni indexation, ni recherche de documents ; il n'est donc pas adapté à la recherche de texte dans les documents S3.  
D. Amazon Lex

#### Explications

Un service de création d'interfaces conversationnelles et de chatbots (reconnaissance d'intention et gestion du dialogue). Il est conçu pour les flux de travail conversationnels, et non pour l'indexation ou la recherche de contenu de documents stockés dans S3.  
Explication générale  
Cette tâche exige un service de recherche et d'indexation adapté aux entreprises, capable d'ingérer des documents depuis S3 et de répondre aux requêtes en langage naturel. La solution idéale propose l'exploration automatisée des documents, l'indexation, l'optimisation de la pertinence et des contrôles d'accès sécurisés. Les autres options sont des services spécialisés (analyse d'images/vidéos, synthèse vocale, interfaces conversationnelles) qui ne prennent pas en charge l'indexation et la recherche de documents sur S3.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 5Incorrect  
Une entreprise souhaite réduire ses coûts en archivant les données qui ne sont plus fréquemment consultées par les utilisateurs finaux. Quelle fonctionnalité d'Amazon S3 répond à ce besoin ?  
**Votre réponse est incorrecte**  
A. Gestion des versions S3

#### Explications

Le versionnage S3 stocke plusieurs versions d'un objet, ce qui permet de récupérer des données après une suppression ou un écrasement accidentel. Il augmente le nombre d'objets stockés (et donc le coût), car chaque version est conservée et ne propose ni transition automatique vers des classes de stockage moins coûteuses, ni expiration automatique en fonction des habitudes d'accès.  
**Bonne réponse**  
B. Cycle de vie S3

#### Explications

Les politiques de cycle de vie S3 permettent de définir des règles qui transfèrent automatiquement les objets vers des classes de stockage moins coûteuses (par exemple, Standard-IA, One Zone-IA, S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval ou S3 Glacier Deep Archive) ou les suppriment en fonction de leur ancienneté, de leur date de création ou de leurs étiquettes. Cette automatisation est le mécanisme prévu par S3 pour l'archivage optimisé des données rarement consultées, à moindre coût.  
C. S3 Verrouillage d'objet

#### Explications

S3 Object Lock enforces WORM (write‑once‑read‑many) retention using governance or compliance modes to prevent object deletion or modification for a defined retention period. It is used for regulatory compliance and data immutability, not for moving objects to lower‑cost tiers or deleting them to reduce storage costs.  
D. S3 Inventory

#### Explications

S3 Inventory produces scheduled reports (CSV/Parquet/ORC) that list objects and metadata (size, encryption, storage class, etc.) to help with auditing and lifecycle planning. It is a reporting tool only and does not perform automatic data movement or deletion.  
Explication générale  
The question targets the S3 capability for automatic cost optimization. S3 Lifecycle policies are the correct choice because they automate transitions between storage classes and object expirations based on rules (age, tags), directly addressing archiving and cost reduction. The other options relate to version management, immutability/compliance, or reporting and do not automate archival transitions.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 6Correct  
A company wants to deploy an application that stores data in a relational database. The company wants database tasks, such as automated backups and database snapshots, to be managed by AWS. Which AWS service will meet these requirements?  
A. Amazon DocumentDB

#### Explications

Incorrect — Amazon DocumentDB is a managed document (NoSQL) database compatible with the MongoDB document model. It is not a relational database engine and therefore does not satisfy a requirement for a managed relational DB with SQL-based schemas and relational engine features.  
**Votre réponse est correcte**  
B. Amazon RDS

#### Explications

Correct — Amazon RDS is AWS’s managed relational database service that supports multiple RDBMS engines (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, and Amazon Aurora). AWS automates daily backups, automated snapshots, point-in-time recovery, automated minor version patching, and offers Multi‑AZ deployments and read replicas for availability and scalability, matching the requirement for AWS-managed database tasks.  
C. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Incorrect — Amazon EBS provides block storage volumes for EC2 instances and supports volume-level snapshots. It is a storage service, not a managed database service, so it does not perform database-engine backups, automated DB snapshots, engine patching, or other DB management tasks.  
D. Amazon S3

#### Explications

Incorrect — Amazon S3 is object storage intended for storing and retrieving files/objects. It can store backup files but does not provide a relational database engine or built-in DB management features such as automated backups, snapshots at the DB engine level, or patching.  
Explication générale  
This question tests knowledge of AWS managed database offerings. The requirement is for a managed relational database where AWS handles database tasks (backups, snapshots, patching). Amazon RDS is the appropriate service because it provides managed RDBMS engines and automates backups, snapshots, point-in-time recovery, patching, and availability features. The distractors are services for different use cases: DocumentDB is a NoSQL/document database, and EBS/S3 are storage services rather than managed relational database services.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 7Correct  
A company needs a content delivery network that provides secure delivery of data, videos, applications, and APIs to users globally with low latency and high transfer speeds. Which AWS service meets these requirements?  
**Votre réponse est correcte**  
A. Amazon CloudFront

#### Explications

CloudFront uses a global network of edge locations (points of presence) to cache and serve content close to end users, reducing latency and improving throughput. It provides built-in security and delivery features such as TLS support, AWS Shield for DDoS protection, AWS WAF integration for application-layer protection, signed URLs/cookies for private content, HTTP/2 and HTTP/3 support, and compute-at-edge options (CloudFront Functions and Lambda@Edge) for request/response customization. CloudFront can originate content from S3 buckets, ALBs, EC2, or custom origins, making it the appropriate AWS service for secure, low-latency global delivery of data, video, applications, and APIs.  
B. Elastic Load Balancing

#### Explications

Elastic Load Balancing (ALB/NLB/CLB) distributes incoming traffic across targets within one or more Availability Zones in a region to provide high availability and fault tolerance for applications. It is a regional load-distribution service, not a global edge caching/distribution network, so it does not by itself provide the global low-latency content delivery expected from a CDN.  
C. Amazon S3

#### Explications

Amazon S3 is durable object storage used to store and retrieve data and can host static website assets. S3 does not provide edge caching or a global points-of-presence network; to achieve low-latency global distribution of S3-hosted content you pair S3 with CloudFront. (S3 Transfer Acceleration is a separate feature that uses edge locations to accelerate transfers but is distinct from a full CDN solution.)  
D. Amazon Elastic Transcoder

#### Explications

Amazon Elastic Transcoder (and related media-conversion services) is used to convert or transcode media files into different formats for playback on various devices. It handles format conversion and bitrate/resolution changes, not global content distribution or edge delivery, so it does not meet the CDN requirement.  
Explication générale  
The requirement is for a global, secure, low-latency content delivery capability. The correct service provides edge caching, a worldwide points-of-presence network, integration with AWS security features (Shield, WAF, TLS), and the ability to serve static and dynamic content and APIs—capabilities provided by CloudFront. The other options are regional or specialized services (ELB for regional load distribution, S3 for storage only, Elastic Transcoder for media conversion) and therefore do not satisfy the full CDN requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 8Incorrect  
A company wants to migrate unstructured data to AWS. The data needs to be securely moved with inflight encryption and end-to-end data validation. Which AWS service will meet these requirements?  
**Votre réponse est incorrecte**  
A. AWS Application Migration Service

#### Explications

AWS Application Migration Service (MGN) is designed for lift-and-shift migrations of servers by replicating entire server volumes and orchestrating cutover. It is not a file-level transfer service that provides built-in in-transit TLS encryption plus per-object end-to-end validation for unstructured file datasets, so it does not meet the stated requirements.  
B. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed, POSIX-compliant file storage service for use by EC2 and on-prem clients. While it provides storage-level features (including encryption at rest and optional encryption in transit for mounts), it is not a tool for migrating data with automated transfer workflows, transfer-specific in-flight encryption and checksum-based validation between sources and targets.  
**Bonne réponse**  
C. AWS DataSync

#### Explications

AWS DataSync is purpose-built for automated, high-performance transfers of file and object data between on-premises storage and AWS (and between AWS storage services). It encrypts data in transit (TLS), can use AWS KMS/SSE for encryption at rest, uses checksums to verify data integrity during transfer, supports NFS/SMB/S3/EFS/FSx endpoints, and provides agents, scheduling, and bandwidth controls—matching the requirements for in-flight encryption and end-to-end validation.  
D. AWS Migration Hub

#### Explications

AWS Migration Hub provides a central view to track progress of migrations and integrations with migration tools; it does not perform data movement or provide transfer-level encryption and integrity verification features, so it cannot fulfill the secure data transfer and validation requirement.  
Explication générale  
The task requires a service that securely transfers unstructured data with in-transit encryption and end-to-end integrity verification. AWS DataSync is the correct choice because it is engineered for file/object transfers, uses TLS for in-flight encryption, performs checksum-based validation, and integrates with AWS storage targets. The other choices are either storage services (EFS), server/VM migration tools (Application Migration Service), or a migration tracking dashboard (Migration Hub), none of which provide the full set of transfer, encryption, and validation capabilities required.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 9Correct  
A developer needs to use a standardized template to create copies of a company's AWS architecture for development, test, and production environments. Which AWS service should the developer use to meet this requirement?  
A. AWS Cloud Map

#### Explications

Provides service discovery (name-to-resource mapping) so applications can locate endpoints; it does not provide infrastructure-as-code, templating, or automated provisioning for entire architectures.  
**Votre réponse est correcte**  
B. AWS CloudFormation

#### Explications

Implements infrastructure as code using JSON/YAML templates to define resources as stacks. Supports parameters, outputs, nested stacks, change sets, drift detection, and StackSets for consistent, repeatable deployments across environments and accounts — making it the correct solution for templated environment creation.  
C. Amazon Cloud Front

#### Explications

A global content delivery service that caches and delivers content at edge locations; its purpose is low-latency content distribution, not defining or provisioning AWS infrastructure templates.  
D. AWS CloudTrail

#### Explications

A logging and auditing service that records API calls and user activity for governance and compliance; it tracks changes rather than provisioning resources, so it cannot be used to create standardized environment templates.  
Explication générale  
This question tests knowledge of infrastructure-as-code and templating for repeatable environment deployments. CloudFormation is the appropriate service because it defines AWS resources in templates that can be versioned and deployed consistently (including across accounts/regions via StackSets). The other options provide service discovery, content delivery, or auditing capabilities and do not offer templated infrastructure provisioning.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 10Correct  
A company needs to provide customer service by using voice calls and web chat features. Which AWS service should the company use to meet these requirements?  
A. Amazon Aurora

#### Explications

Incorrect. Aurora is a managed relational database (MySQL/PostgreSQL-compatible) optimized for transactional and analytical workloads. It supplies storage and query capabilities, not contact-center features like IVR, call routing, or web chat.  
**Votre réponse est correcte**  
B. Amazon Connect

#### Explications

Correct. Amazon Connect is a fully managed cloud contact-center service that provides omnichannel engagement (voice and web chat), contact flows, automatic call distribution, integration with Amazon Lex for conversational bots and AWS Lambda for backend integrations, plus real-time and historical metrics—all required for customer service interactions.  
C. Amazon WorkSpaces

#### Explications

Incorrect. WorkSpaces is a Desktop-as-a-Service (virtual desktop) that provides users with a managed desktop environment. Although agents could use it to access applications, it does not include built-in contact-center capabilities such as voice routing or web chat.  
D. AWS Organizations

#### Explications

Incorrect. AWS Organizations is used for centralized account management, consolidated billing, and policy controls (SCPs). It does not offer any customer communication or contact-center functionality.  
Explication générale  
This item tests service selection for customer engagement. Amazon Connect is the AWS service purpose-built for contact centers, supporting both voice and web chat along with integrations (Lex, Lambda) and analytics. The other choices are unrelated infrastructure or management services (database, virtual desktops, account management) and therefore do not meet the stated requirements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 11Incorrect  
A user needs to quickly deploy a nonrelational database on AWS. The user does not want to manage the underlying hardware or the database software. Which AWS service can be used to accomplish this?  
**Votre réponse est incorrecte**  
A. Amazon RDS

#### Explications

Incorrect. Amazon RDS is a managed relational (SQL) database service for engines such as MySQL, PostgreSQL, Oracle, and SQL Server. It requires choosing instance classes and a relational schema and is not a NoSQL/key‑value or document database, so it does not meet the requirement for a nonrelational, serverless-style deployment.  
**Bonne réponse**  
B. Amazon DynamoDB

#### Explications

Correct. Amazon DynamoDB is a fully managed, serverless NoSQL database that provides key‑value and document data models, automatic scaling and multi‑AZ durability, and eliminates the need to provision or manage underlying servers, operating systems, or database software—matching the requirement to quickly deploy a nonrelational database without managing hardware or DB software.  
C. Amazon Aurora

#### Explications

Incorrect. Amazon Aurora is a high-performance, managed relational database engine compatible with MySQL and PostgreSQL. It is designed for relational workloads and not intended as a NoSQL/nonrelational solution, so it does not satisfy the question’s requirement.  
D. Amazon Redshift

#### Explications

Incorrect. Amazon Redshift is a managed, petabyte‑scale, columnar MPP data warehouse optimized for analytical queries and OLAP workloads. It is not a general-purpose nonrelational operational database and therefore is not appropriate for this use case.  
Explication générale  
This question tests recognition of the appropriate managed AWS service for nonrelational (NoSQL) workloads without server management. The best fit is the fully managed, serverless NoSQL service that removes hardware and database software administration (DynamoDB). The other options are managed services for relational databases (RDS, Aurora) or for analytics/data warehousing (Redshift) and therefore do not meet the nonrelational, no‑server‑management requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 12Correct  
Which AWS service or component allows inbound traffic from the internet to access a VPC?  
**Votre réponse est correcte**  
A. Internet gateway

#### Explications

This VPC-attached, horizontally scaled and redundant gateway is the route target that enables two‑way IPv4/IPv6 connectivity between a VPC and the public internet. For inbound traffic to reach instances, the subnet’s route table must send internet-bound traffic (0.0.0.0/0 or ::/0) to this gateway, and the target resources must have public IPs (or public IPv6) and permissive security groups/NACLs. Without this gateway and the appropriate routing and addressing, internet clients cannot reach VPC resources.  
B. NAT gateway

#### Explications

Provides network address translation so instances in private subnets can initiate outbound connections to the internet and receive responses. It does not accept unsolicited inbound connections from internet hosts and therefore cannot be used to enable inbound internet access to resources in a VPC.  
C. AWS WAF

#### Explications

A managed web application firewall that inspects and filters HTTP/HTTPS requests (often integrated with CloudFront, ALB, or API Gateway). It enforces application-layer protections but does not create routing or a network path between the internet and a VPC.  
D. VPC peering

#### Explications

Creates private, point‑to‑point connectivity between two VPCs so resources can communicate internally. It does not provide internet routing, cannot be used as a transit gateway for internet traffic, and therefore does not enable inbound internet access.  
Explication générale  
This item tests basic VPC networking: which component creates a routable path between a VPC and the public internet. The correct choice is the VPC internet gateway because it is the route-table target that allows two‑way internet traffic when combined with public IP addressing and appropriate security rules. The distractors are incorrect: NAT gateways only support outbound-initiated traffic for private subnets, AWS WAF is an application-layer filter (not a routing component), and VPC peering provides private inter‑VPC connectivity rather than internet access.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 13Correct  
A company runs an application on AWS that performs batch jobs. The application is fault-tolerant and can handle interruptions. The company wants to optimize the cost to run the application. Which AWS offering will meet these requirements?  
A. Amazon Macie

#### Explications

Amazon Macie is a data security and privacy service that uses machine learning to discover, classify, and protect sensitive data in Amazon S3. It does not provide compute capacity or pricing models for running batch workloads and therefore does not address cost optimization for interruption-tolerant compute jobs.  
B. Amazon Neptune

#### Explications

Amazon Neptune is a managed graph database service for highly connected datasets and graph queries. It is a data store, not a compute pricing option or runtime environment for batch jobs, so it is not applicable for reducing compute costs for fault-tolerant batch processing.  
**Votre réponse est correcte**  
C. Amazon EC2 Spot Instances

#### Explications

EC2 Spot Instances let you run workloads on spare EC2 capacity at substantial discounts compared to On‑Demand pricing by accepting potential interruptions when AWS reclaims capacity. They integrate with AWS Batch, EC2 Auto Scaling, Spot Fleet, and provide interruption notices, making them the appropriate cost-optimized choice for fault-tolerant, interruption-tolerant batch jobs.  
D. Amazon EC2 On-Demand Instances

#### Explications

On‑Demand Instances provide dedicated compute capacity billed at fixed rates and are not subject to Spot interruptions. They are useful when you need guaranteed capacity or cannot tolerate interruptions, but they are typically more expensive than Spot for batch workloads that can handle interruptions.  
Explication générale  
This question tests knowledge of AWS compute pricing and when to use Spot capacity. For batch workloads that are fault-tolerant and can tolerate interruptions, EC2 Spot Instances provide the best cost optimization because they use spare capacity at deep discounts and integrate with AWS Batch and Auto Scaling. The On‑Demand model is more costly but avoids interruptions, while Macie and Neptune are unrelated services (data protection and graph database, respectively).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 14Correct  
Which AWS service uses edge locations to cache content?  
A. Amazon Kinesis

#### Explications

Incorrect. Kinesis is a platform for real-time data ingestion and streaming (Kinesis Data Streams, Data Firehose, Data Analytics) used for processing and analytics pipelines; it does not provide a global content-delivery cache at edge locations.  
B. Amazon Simple Queue Service (Amazon SQS)

#### Explications

Incorrect. Amazon SQS is a fully managed message queuing service that decouples components and ensures reliable message delivery; it is not a CDN and does not cache user-facing content at edge locations.  
**Votre réponse est correcte**  
C. Amazon CloudFront

#### Explications

Correct. The AWS content-delivery service uses a global network of edge locations and regional edge caches to store and serve cached copies of web content close to end users; it supports distributions with configurable cache behaviors, TTLs, origin configurations (S3, EC2, ALB), cache invalidation, and edge computing features (Lambda@Edge, CloudFront Functions) to reduce latency and improve performance.  
D. Amazon Route 53

#### Explications

Incorrect. Route 53 is a scalable DNS and domain registration service that uses a global network of authoritative DNS servers (anycast) for query resolution and health checks; it does not function as a CDN that caches and serves website content from edge locations.  
Explication générale  
This item tests recognition of AWS’s CDN and its use of edge locations for caching. The correct choice is the AWS content-delivery service, which caches static and dynamic content at edge locations and provides features such as configurable TTLs, origins, invalidation, and edge computing. The distractors are services for streaming (Kinesis), messaging (SQS), and DNS (Route 53), none of which provide edge-location content caching.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 15Correct  
Which of the following are benefits of using AWS Trusted Advisor? (Choose two.)  
A. Providing high-performance container orchestration

#### Explications

Incorrect. Trusted Advisor does not provide container orchestration functionality. Container orchestration and scheduling are provided by services such as Amazon ECS, Amazon EKS, and AWS Fargate, which manage container placement, scaling, and lifecycle.  
B. Creating and rotating encryption keys

#### Explications

Incorrect. Management of cryptographic keys (creation, storage, rotation, and lifecycle) is handled by AWS Key Management Service (KMS) or AWS CloudHSM. Trusted Advisor does not create or rotate encryption keys; it provides configuration and best-practice checks instead.  
**Votre sélection est correcte**  
C. Detecting underutilized resources to save costs

#### Explications

Correct. Trusted Advisor performs cost-optimization checks that analyze resource utilization (for example, low-usage EC2 instances and idle load balancers) and surfaces actionable recommendations such as rightsizing or terminating underused resources to reduce spend.  
**Votre sélection est correcte**  
D. Improving security by proactively monitoring the AWS environment

#### Explications

Correct. Trusted Advisor runs multiple security checks (for example, MFA on the root account, exposed S3 buckets, overly permissive security group rules, and unused IAM credentials) and provides prioritized recommendations to remediate those issues and improve the account security posture.  
Explication générale  
AWS Trusted Advisor is a discovery and recommendation service that runs automated checks across five categories (cost optimization, security, fault tolerance, performance, and service limits). The best answers identify its role in cost optimization (identifying low-utilization resources) and security posture improvement (providing security checks and remediation guidance). The distractors describe capabilities provided by other AWS services—container orchestration by ECS/EKS/Fargate and key management by KMS—so they do not apply to Trusted Advisor.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 16Incorrect  
For which use case are Amazon EC2 On-Demand Instances MOST cost-effective?  
A. Compute-intensive video transcoding that can be restarted if necessary

#### Explications

Incorrect. Workloads that can be restarted or tolerate interruption are best served by EC2 Spot Instances, which offer steep discounts compared with On-Demand but can be reclaimed by AWS. On-Demand provides stable, non‑interruptible capacity but is more expensive than Spot for interruptible, fault‑tolerant tasks.  
**Bonne réponse**  
B. An instance in continual use for 1 month to conduct quality assurance tests

#### Explications

Correct. On‑Demand Instances are optimal for short‑term, unpredictable, or temporary workloads where you need immediate capacity without a 1- or 3‑year commitment. They bill per second (with a minimum), avoid up‑front commitments required by Reserved Instances or Savings Plans, and therefore are most cost‑effective for a one‑month QA run.  
C. An instance that runs a web server that will run for 1 year

#### Explications

Incorrect. A web server running continuously for a year is a steady, predictable workload. Compute Savings Plans or 1‑year Reserved Instances (or Savings Plans) typically provide substantial discounts versus On‑Demand for sustained, long‑term use.  
**Votre réponse est incorrecte**  
D. An instance that runs a database that will run for 3 years

#### Explications

Incorrect. Multi‑year steady workloads (such as a database for 3 years) are best optimized with 1‑ or 3‑year Reserved Instances or Savings Plans, which reduce hourly costs in exchange for a term commitment. On‑Demand would be the most expensive option over that period.  
Explication générale  
Cette question porte sur le choix du modèle d'achat d'instances EC2. Le modèle à la demande est idéal lorsque vous avez besoin de capacité à court terme, imprévisible ou immédiate, sans engagement de durée ; il est donc particulièrement rentable pour une instance de test d'un mois. Les instances Spot, qui permettent des calculs interruptibles ou redémarrables, sont moins chères, tandis que les charges de travail prévisibles à long terme sont mieux adaptées aux instances réservées ou aux plans d'économies.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 17Correct  
Une entreprise souhaite utiliser des instances Amazon EC2 pour une charge de travail de production stable qui fonctionnera pendant un an. Quelle option d'achat d'instance répond le mieux à ces exigences en termes de coût ?  
A. Hôtes dévoués

#### Explications

Les hôtes dédiés sont des serveurs EC2 physiques dédiés à un seul compte AWS et sont principalement utilisés pour répondre à des exigences spécifiques de conformité, de licences (BYOL) ou de visibilité au niveau de l'hôte. Ils engendrent des coûts d'exploitation et des frais supplémentaires par rapport aux options d'achat au niveau de l'instance ; ils ne constituent donc pas le choix le plus rentable pour une charge de travail de production prévisible sur un an.  
**Votre réponse est correcte**  
B. Cas réservés

#### Explications

Les instances réservées (IR) offrent un engagement tarifaire pour une durée de 1 ou 3 ans, avec une réduction récurrente sur la facturation par rapport aux tarifs à la demande. Pour des besoins de calcul prévisibles et stables, une IR d'un an garantit un tarif horaire plus avantageux et (pour les IR zonales) permet de réserver de la capacité, ce qui en fait l'option la plus rentable parmi les choix proposés pour une charge de travail de production d'un an.  
C. Instances à la demande

#### Explications

Les instances à la demande n'entraînent aucun engagement à long terme et sont facturées à l'heure/seconde, ce qui offre une flexibilité maximale mais se traduit généralement par un coût total plus élevé pour les charges de travail soutenues et prévisibles sur une année par rapport aux modèles de tarification avec engagement.  
D. Exemples ponctuels

#### Explications

Les instances Spot offrent des remises importantes en utilisant de la capacité inutilisée, mais elles peuvent être interrompues lorsque AWS a besoin de cette capacité. Comme elles ne garantissent pas une disponibilité continue, elles ne conviennent pas aux charges de travail de production stables qui nécessitent une puissance de calcul prévisible et ininterrompue pendant un an.  
Explication générale  
Cette question évalue vos connaissances des options d'achat d'instances EC2 pour les charges de travail prévisibles et à long terme. La réservation d'une instance pour un an permet de bénéficier d'un tarif préférentiel (et d'une réservation de capacité potentielle), ce qui en fait l'option la plus rentable parmi celles proposées. Les options alternatives sont : les hôtes dédiés (cas d'utilisation spécialisés et plus coûteux, comme la conformité ou le BYOL), les instances à la demande (flexibles mais plus chères pour une utilisation stable) et les instances Spot (susceptibles d'être interrompues et non adaptées à une disponibilité garantie en production).  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 18Correct  
Une entreprise doit migrer une base de données PostgreSQL de son infrastructure locale vers Amazon RDS. Quel service ou outil AWS doit-elle utiliser pour répondre à ce besoin ?  
A. Outil de préparation à l'adoption du cloud

#### Explications

Solution d'évaluation et de planification permettant d'analyser la préparation des organisations et de formuler des recommandations pour l'adoption du cloud. Elle ne prend pas en charge la réplication des données, la capture des modifications ni l'exécution des migrations nécessaires au transfert d'une base de données PostgreSQL en production vers Amazon RDS.  
B. AWS Migration Hub

#### Explications

A centralized tracking and visibility service that aggregates migration progress across tools and partners. It provides project-level tracking and insights but does not perform data migration or replication itself.  
**Votre réponse est correcte**  
C. AWS Database Migration Service (AWS DMS)

#### Explications

A fully managed service purpose-built for migrating databases to AWS. It supports initial full-load migrations and ongoing change data capture (CDC) to minimize downtime, works with PostgreSQL sources and RDS targets, and integrates with the Schema Conversion Tool when schema transformation is needed.  
D. AWS Application Migration Service

#### Explications

A lift-and-shift service that replicates entire servers (block-level volumes and system state) for application/server migrations. It is not designed for logical database migration or continuous database replication required to migrate a PostgreSQL database to RDS.  
Explication générale  
The correct choice is the managed database migration service because it is specifically designed to move databases to AWS with support for full load and ongoing replication (CDC), enabling minimal downtime and compatibility with Amazon RDS for PostgreSQL. The other options address assessment, tracking, or server-level lift-and-shift tasks and do not provide the database-specific replication and migration features required for this scenario.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 19Correct  
A company has 5 TB of data stored in Amazon S3. The company plans to occasionally run queries on the data for analysis. Which AWS service should the company use to run these queries in the MOST cost-effective manner?  
A. Amazon Redshift

#### Explications

Redshift is a provisioned, petabyte-scale data warehousing service that requires compute nodes (clusters) to be running for queries. Even though Redshift can query S3 via Redshift Spectrum, you still incur cluster costs when provisioned. For occasional, ad-hoc queries against S3 data, the ongoing provisioning and compute charges make it less cost-effective than a serverless, pay-per-scan service.  
**Votre réponse est correcte**  
B. Amazon Athena

#### Explications

Athena is a serverless, interactive query service that uses a SQL engine (Presto) to read data directly from S3. Billing is based on the amount of data scanned per query, and costs can be reduced via partitioning, compression, and columnar formats (e.g., Parquet/ORC). No clusters or infrastructure management are required, making it the most cost-effective choice for infrequent analysis of a 5 TB S3 dataset.  
C. Amazon Kinesis

#### Explications

Kinesis family services are focused on ingesting, processing, and analyzing streaming data in real time. They are not designed for running ad-hoc SQL queries against static datasets stored in S3. While Kinesis Data Analytics can query streaming records, it does not provide the serverless, pay-per-query facility for S3-based analytics that Athena offers.  
D. Amazon RDS

#### Explications

RDS is a managed relational database service optimized for transactional (OLTP) workloads and persistent database instances. It requires provisioning of compute and storage and is not intended to run large-scale, ad-hoc queries directly against S3 data. Using RDS for this purpose would be operationally and cost-wise inefficient compared with serverless S3-query options.  
Explication générale  
The question tests knowledge of cost-effective options for ad-hoc analysis of data stored in S3. A serverless, pay-per-query service that reads data directly from S3 is the best fit because it avoids cluster provisioning and ongoing compute costs. Athena fits this pattern (serverless, billed by data scanned, integrates with the Glue Data Catalog and benefits from partitioning/columnar formats). The other options—provisioned data warehouse (Redshift), streaming services (Kinesis), and transactional databases (RDS)—are not as cost-effective or purpose-built for occasional S3-based SQL queries.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 20Correct  
A company needs to purchase Amazon EC2 instances to support an application that will run continuously for more than 1 year. Which EC2 instance purchasing option meets these requirements MOST cost-effectively?  
A. Dedicated Instances

#### Explications

Incorrect. Dedicated Instances (single-tenant tenancy) exist to meet isolation or licensing requirements, but they do not provide the long-term, commitment-based discounts needed for the most cost-effective solution for steady, multi-year compute — they typically result in higher costs than shared-tenancy commitment options.  
B. Spot Instances

#### Explications

Incorrect. Spot Instances offer deep discounts on unused capacity but are interruptible by AWS with little notice; they are appropriate for fault-tolerant or flexible batch workloads, not for an application that must run continuously for more than a year.  
**Votre réponse est correcte**  
C. Reserved Instances

#### Explications

Correct. Reserved Instances (RIs) provide significant hourly cost savings in exchange for a 1- or 3-year commitment. RIs (Standard or Convertible) and regional RIs with instance-size flexibility are designed for steady-state, continuously running instances and therefore are the most cost-effective choice among the listed options for \>1 year workloads. (Note: AWS Savings Plans are a newer, more flexible alternative, but RIs are the best answer given the provided choices.)  
D. On-Demand Instances

#### Explications

Incorrect. On-Demand Instances provide maximum flexibility with no long-term commitment and are billed at the standard rate; this makes them suitable for short-lived or unpredictable usage patterns but generally the most expensive choice for continuous, long-term workloads.  
Explication générale  
For a continuously running application with a multi-year horizon, a commitment-based pricing option is required to achieve the best cost savings. Reserved Instances deliver that commitment (1- or 3-year terms) and corresponding discounts tailored to steady-state EC2 usage. Spot is interruptible and unsuitable for continuous availability; Dedicated tenancy increases cost for isolation needs but does not provide term discounts; On-Demand lacks long-term savings. Thus Reserved Instances are the most cost-effective among the provided options.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 21Correct  
Why are AWS CloudFormation templates used?  
**Votre réponse est correcte**  
A. To reduce provisioning time by using automation.

#### Explications

AWS CloudFormation implements Infrastructure as Code: you declare resources in JSON/YAML templates which CloudFormation uses to create, update, and delete stacks reliably and repeatedly. Features such as parameters, change sets, nested stacks, stack sets, and drift detection enable automated, auditable, and consistent provisioning and lifecycle management of AWS resources.  
B. To transfer existing infrastructure to another company.

#### Explications

Incorrect. CloudFormation is not a mechanism for transferring ownership of infrastructure to another organization. It defines and manages resources within an AWS account/region. While CloudFormation can import existing resources into a stack for management, it does not move resources between companies or accounts by itself.  
C. To reuse on-premises infrastructure in the AWS Cloud.

#### Explications

Incorrect. CloudFormation manages AWS resources (and some hybrid resources) via templates; it does not directly ‘reuse’ on-premises hardware. Migrating on-premises resources to AWS typically uses migration services (e.g., AWS Application Migration Service, Migration Hub) and then you can use CloudFormation to provision AWS-side resources.  
D. To deploy large infrastructure with no cost implications.

#### Explications

Incorrect. CloudFormation automates deployment but does not remove the cost of the underlying resources. The CloudFormation service itself has no additional charge for most uses, but any AWS resources created by templates (EC2, RDS, S3, etc.) incur the usual service costs.  
Explication générale  
The question tests understanding of CloudFormation as AWS’s Infrastructure as Code service. The correct answer is that templates automate and standardize provisioning and management of AWS resources. Distractors confuse ownership transfer, on-premises reuse, or imply cost elimination; CloudFormation automates provisioning but does not transfer infrastructure ownership, directly reuse on-prem hardware, or eliminate resource costs.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 22Correct  
A company runs MySQL database workloads on self-managed servers in an on-premises data center. The company wants to migrate the database workloads to an AWS managed service. Which migration strategy should the company use?  
A. Rehost

#### Explications

Moving the existing database servers to Amazon EC2 with no significant changes preserves the need for the customer to manage backups, patching, scaling, and high availability. That approach does not deliver an AWS-managed database service and therefore does not meet the requirement to migrate to a managed DB offering.  
B. Repurchase

#### Explications

Replacing the current database with a third-party SaaS product (a 'buy' or subscription replacement) is a different strategy intended for swapping entire applications with hosted services. It does not describe migrating self-managed MySQL to an AWS managed database service such as Amazon RDS and is only appropriate when adopting a new software provider.  
C. Refactor

#### Explications

Redesigning the application and database to be cloud-native or changing architectures (which may include re-architecting queries, schema, or switching engines) is often high-effort. While it can produce long-term benefits, it is more invasive than necessary when the goal is to move on-premises MySQL to an AWS managed DB with minimal disruption.  
**Votre réponse est correcte**  
D. Replatform

#### Explications

Migrating the on-premises MySQL to Amazon RDS (or Aurora) while making only small, necessary adjustments best fulfills the goal of using an AWS-managed database. This path lets you leverage automated backups, Multi-AZ deployments, automated minor version patching, snapshots, and CloudWatch monitoring. Tools such as AWS Database Migration Service (AWS DMS) (and AWS SCT when schema conversion is required) can perform continuous replication to minimize downtime during cutover.  
Explication générale  
The question asks which migration strategy moves self-managed MySQL workloads to an AWS-managed database. The correct approach is to migrate to a managed DB service with minimal adjustments so you gain managed features (backups, patching, HA) without a full redesign. Alternatives either keep databases self-managed on EC2, replace them with unrelated SaaS, or require a costly redesign—none of which match the stated goal as well as migrating to Amazon RDS/Aurora using AWS DMS.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 23Correct  
A company has a set of ecommerce applications. The applications need to be able to send messages to each other. Which AWS service meets this requirement?  
A. AWS Auto Scaling

#### Explications

AWS Auto Scaling manages compute capacity by increasing or decreasing EC2 (and other resources) based on policies and metrics. It does not provide messaging or queueing functionality for inter-application communication.  
B. Elastic Load Balancing

#### Explications

Elastic Load Balancing distributes incoming network traffic across targets (EC2, containers, IPs) to improve availability and fault tolerance. It is a traffic distribution mechanism, not a message-passing or queue service for asynchronous app-to-app communication.  
**Votre réponse est correcte**  
C. Amazon Simple Queue Service (Amazon SQS)

#### Explications

Amazon SQS is a fully managed message queuing service designed for decoupling distributed applications. It provides durable message storage, at-least-once delivery (standard queues), FIFO ordering (FIFO queues), visibility timeouts, and long polling—features that enable reliable asynchronous message exchange between producers and consumers.  
D. Amazon Kinesis Data Streams

#### Explications

Amazon Kinesis Data Streams is built for high-throughput, real-time streaming ingestion and processing (analytics, monitoring, event streaming). While it can transport event data, it is not a purpose-built message queue for typical asynchronous application-to-application messaging patterns and lacks the queue semantics and delivery guarantees provided by SQS.  
Explication générale  
The question tests knowledge of AWS services for inter-application messaging. Amazon SQS is the appropriate choice because it is explicitly a managed message queue that enables asynchronous, decoupled communication with delivery and visibility controls. Auto Scaling and Elastic Load Balancing handle capacity and traffic distribution, not messaging, and Kinesis is focused on streaming data and real-time processing rather than queue semantics.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 24Correct  
According to the AWS shared responsibility model, the customer is responsible for applying the latest security updates and patches for which of the following?  
A. Amazon DynamoDB

#### Explications

Incorrect — this is a fully managed NoSQL service where AWS operates and patches the underlying infrastructure and service software. The customer's responsibilities are data protection, access controls, and configuration, not applying OS or service-level security patches.  
**Votre réponse est correcte**  
B. Amazon EC2 instances

#### Explications

Correct — with virtual servers you manage the guest operating system, middleware, and applications, so you are responsible for applying OS and software security updates and patches. AWS is responsible for the physical hosts, hypervisor, and foundational infrastructure.  
C. Amazon RDS instances

#### Explications

Incorrect — this is a managed relational database service where AWS typically performs patching of the database engine and underlying OS as part of service maintenance (you can control maintenance windows and enable automatic minor version upgrades). Customers remain responsible for database configuration, data, and access. For self-managed databases on EC2 or RDS Custom, patching responsibility may differ.  
D. Amazon S3

#### Explications

Incorrect — object storage is provided as a managed service and AWS patches the storage infrastructure and service components. Customers are responsible for securing their objects and access (bucket policies, encryption, IAM), not for applying infrastructure patches.  
Explication générale  
This tests the AWS shared responsibility model. AWS manages and patches the infrastructure and managed-service components (e.g., S3, DynamoDB, RDS), while customers are responsible for security of what they control — notably the guest OS, applications, and data on virtual servers. Therefore only the virtual server option requires the customer to apply security updates directly; managed services offload patching to AWS (with some configuration/maintenance controls exposed to the customer).  
Domaine  
Domain 2: Security and Compliance  
Question 25Correct  
Which AWS service supports a hybrid architecture that gives users the ability to extend AWS infrastructure, AWS services, APIs, and tools to data centers, co-location environments, or on-premises facilities?  
A. AWS Snowmobile

#### Explications

This offering is a physical data-transport solution for moving very large datasets (petabytes to exabytes) using secure shipping containers. It is intended for offline bulk data migration and does not provide AWS-managed hardware, APIs, or services deployed inside customer data centers to enable hybrid operations.  
B. AWS Local Zones

#### Explications

Local Zones are AWS-managed extensions of a Region that place compute and storage closer to end users to reduce latency. They are still AWS-operated infrastructure near metropolitan areas and do not install AWS hardware or provide the Region control plane inside a customer’s on-premises facility for hybrid integration.  
**Votre réponse est correcte**  
C. AWS Outposts

#### Explications

Outposts delivers AWS-managed, rack-level hardware and software installed at a customer site or co-location, and it exposes the same AWS APIs, services, tools, and management model as the Region. It extends VPCs and integrates with the Region control plane to enable consistent hybrid deployments, low-latency on-premises workloads, and unified operational procedures — which is why it is the correct choice.  
D. AWS Fargate

#### Explications

This is a serverless container compute engine that runs within AWS Regions (ECS/EKS integration) and abstracts server management. It is not a physical, on-premises AWS hardware offering and therefore does not extend AWS infrastructure or the AWS control plane into customer data centers.  
Explication générale  
The question targets AWS hybrid infrastructure capabilities. AWS Outposts is the correct answer because it installs AWS-managed hardware on-premises and exposes the same APIs, services, and management model as the AWS Region, enabling a true hybrid architecture. The other options are distractors: one is for bulk data transport, one provides low-latency AWS infrastructure near users (but not inside customer facilities), and one is a serverless container runtime that runs in the cloud.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 26Correct  
A company with multiple accounts and teams wants to set up a new multi-account AWS environment. Which AWS service supports this requirement?  
A. AWS CloudFormation

#### Explications

CloudFormation is an infrastructure-as-code service used to provision and manage AWS resources via templates and stacks. While CloudFormation (and StackSets) can deploy resources across accounts, it does not provide automated multi-account account provisioning, built-in governance, or the opinionated landing-zone guardrails that are required to set up and govern a multi-account environment.  
**Votre réponse est correcte**  
B. AWS Control Tower

#### Explications

Control Tower automates the creation of a secure multi-account landing zone by orchestrating AWS Organizations, Account Factory for account provisioning, centralized logging, and pre-configured preventive and detective guardrails. Those built-in governance, security, and lifecycle features make it the appropriate service for establishing and governing a multi-account environment.  
C. AWS Config

#### Explications

AWS Config records and evaluates resource configurations and compliance over time and can aggregate data across accounts and regions. It is useful for continuous compliance monitoring but does not handle account provisioning or provide the automated landing-zone and governance orchestration required to initially set up a multi-account environment.  
D. Amazon Virtual Private Cloud (Amazon VPC)

#### Explications

Amazon VPC provides isolated virtual networks for resources within a single account and region and is a networking construct. It does not manage account creation, governance, or multi-account organizational structure (though VPC connectivity across accounts can be enabled via peering or Transit Gateway).  
Explication générale  
The question tests knowledge of AWS services for establishing and governing a multi-account environment. AWS Control Tower is designed to create an opinionated landing zone by integrating AWS Organizations, automated account provisioning (Account Factory), centralized logging, and guardrails for security and compliance. The other options describe useful AWS capabilities—infrastructure provisioning (CloudFormation), configuration monitoring (AWS Config), and networking (VPC)—but none provide the end-to-end, governed multi-account setup that Control Tower does.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 27Correct  
Which tasks are the customer’s responsibility, according to the AWS shared responsibility model? (Choose two.)  
A. Establish the global infrastructure.

#### Explications

Provisioning and maintaining the physical pieces of the cloud (Regions, Availability Zones, data centers, and the global network backbone) is performed by AWS. Customers consume this infrastructure rather than build or operate it.  
**Votre sélection est correcte**  
B. Perform client-side data encryption.

#### Explications

Customers are responsible for encrypting sensitive data before it leaves their environment if they require end-to-end control of plaintext and key material. This includes implementing client-side encryption in applications, managing keys (or choosing to integrate with AWS KMS customer-managed keys), and ensuring encryption during transmission and at rest where appropriate.  
**Votre sélection est correcte**  
C. Configure IAM credentials.

#### Explications

Identity and access management within an account is a customer responsibility: creating and rotating IAM users/roles, defining and attaching IAM policies, configuring access keys and MFA, and applying least-privilege controls to govern who and what can access resources.  
D. Secure edge locations.

#### Explications

AWS designs, operates, and secures edge locations (the CDN and edge compute infrastructure such as Amazon CloudFront and Lambda@Edge). Customers can configure CDN behaviors and cache settings, but not the physical or operational security of those edge sites.  
E. Patch Amazon RDS DB instances.

#### Explications

Amazon RDS is a managed database service where AWS applies operating system and engine patches for the managed instances. Customers remain responsible for database-level configuration, schema, data, and for patching when they run database software on self-managed EC2 instances.  
Explication générale  
The AWS shared responsibility model splits duties: AWS is responsible for the security 'of' the cloud (physical infrastructure, Regions/Availability Zones, edge locations, and managed service maintenance), while customers are responsible for security 'in' the cloud (data protection, identity and access management, and client-side controls). Options B and C map to customer responsibilities (data encryption performed client-side and managing IAM). The other options describe AWS-managed responsibilities or scenarios where AWS handles the operational tasks.  
Domaine  
Domain 2: Security and Compliance  
Question 28Incorrect  
Which actions are best practices for an AWS account root user? (Choose two.)  
A. Share root user credentials with team members.

#### Explications

Incorrect. Distributing root credentials increases the blast radius of a compromise, prevents individual accountability, and violates the principle of least privilege. AWS recommends never sharing the root account credentials.  
B. Create multiple root users for the account, separated by environment.

#### Explications

Incorrect. There is only one AWS account root user per account. For environment separation, AWS recommends using separate accounts (AWS Organizations) or IAM roles/users — not multiple root users.  
**Votre sélection est correcte**  
C. Enable multi-factor authentication (MFA) on the root user.

#### Explications

Correct. Enabling MFA on the root account adds a strong second authentication factor for the single, highly privileged identity that has unrestricted access to the account, which is an AWS security best practice.  
**Sélection correcte**  
D. Create an IAM user with administrator privileges for daily administrative tasks, instead of using the root user.

#### Explications

Correct. Creating IAM users or roles with administrative privileges for daily tasks follows least-privilege and identity-management best practices, avoids routine use of the root account, and enables individual credentialing and auditing.  
**Votre sélection est incorrecte**  
E. Use programmatic access instead of the root user and password.

#### Explications

Incorrect. While programmatic access should be used for automation, you should not use root account access keys for that purpose. Instead create IAM users or roles with the specific programmatic permissions required. Root credentials should be kept disabled/unused and protected with MFA.  
Explication générale  
Secure the single AWS root user by protecting it (enable MFA) and minimizing its use. Delegate routine administrative work to IAM users or roles with appropriate privileges to enable least-privilege, individual auditing, and safer programmatic access. Distractors (sharing credentials, multiple roots, or using root access keys for automation) increase risk or are not possible; use separate accounts or IAM constructs instead.  
Domaine  
Domain 2: Security and Compliance  
Question 29Correct  
A company wants to use AWS Managed Services (AMS) for operational support and wants to understand the scope of AMS. Which AMS feature will meet these requirements?  
**Votre réponse est correcte**  
A. Landing zone and network management

#### Explications

AWS Managed Services (AMS) operates and automates the baseline infrastructure and environment setup for customers — including account provisioning, network/VPC configuration, connectivity, and enforcement of operational guardrails. AMS provides lifecycle operations such as patching, change management, monitoring, backup, and security baseline enforcement for the landing zone and networking components, which is why this capability aligns with the request for operational support and scope definition.  
B. Customer application development

#### Explications

Building or writing customer application code is not part of AMS’s remit. AMS focuses on operational management of the AWS environment and infrastructure; application development and feature work are the responsibility of the customer or application teams (or can be provided by separate AWS Professional Services or third-party partners).  
C. DevSecOps pipeline configuration

#### Explications

Setting up CI/CD or DevSecOps pipelines is an application delivery activity that typically resides with development or platform teams. While AMS can integrate with or operate parts of the environment used by pipelines, full pipeline design and configuration (including build/test/deploy workflows) are not core AMS deliverables.  
D. Application log monitoring

#### Explications

Collecting and analyzing application-level logs is an application monitoring concern. AMS provides infrastructure and platform monitoring, incident management, and can help with centralized logging for supported resources, but detailed application log instrumentation and application-level diagnostics are primarily the responsibility of the application owners or monitoring tools configured by the customer.  
Explication générale  
The question tests knowledge of AWS Managed Services’ scope: AMS is intended to operate and manage the foundational AWS environment (accounts, landing zone, network, baseline security and operational processes). Therefore the option describing environment/landing-zone and network operations is correct. Other options (application development, pipeline configuration, and detailed app log diagnostics) describe application- or delivery-focused activities that fall outside AMS’s primary operational scope.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 30Correct  
A company is assessing its AWS Business Support plan to determine if the plan still meets the company’s needs. The company is considering switching to AWS Enterprise Support. Which additional benefit will the company receive with AWS Enterprise Support?  
A. A full set of AWS Trusted Advisor checks

#### Explications

Incorrect. Access to the full set of AWS Trusted Advisor checks is available with Business and Enterprise Support (not exclusive to Enterprise). Trusted Advisor provides best-practice checks across cost optimization, security, fault tolerance, performance, and service limits; Business customers already receive the core/full checks, so this is not the unique differentiator.  
B. Phone, email, and chat access to cloud support engineers 24 hours a day, 7 days a week

#### Explications

Incorrect. 24x7 phone, email, and chat access to AWS Cloud Support Engineers for production issues is provided by the Business Support plan as well. Enterprise Support does provide additional proactive and high-touch services and faster critical-issue SLAs, but round-the-clock basic access is not unique to Enterprise.  
**Votre réponse est correcte**  
C. A designated technical account manager (TAM) to assist in monitoring and optimization

#### Explications

Correct. Enterprise Support includes a named Technical Account Manager (TAM) who serves as a dedicated technical point of contact to provide ongoing, proactive guidance — coordinating architecture reviews, operational best practices, incident management escalation, and access to AWS specialists and resources to help optimize reliability, performance, and cost. The TAM role is a signature, Enterprise-only offering.  
D. A consultative review and architecture guidance for the company’s applications

#### Explications

Incorrect as stated. Architecture guidance and consultative reviews are delivered as part of Enterprise engagements, but they are typically provided through the Enterprise support program via the assigned TAM and other Enterprise services (for example, infrastructure event management and Well-Architected engagements). The option describes a capability of Enterprise but is not the single distinguishing benefit separate from the TAM.  
Explication générale  
The main distinction between Business and Enterprise Support is the high-touch, proactive services provided by Enterprise, most notably a named Technical Account Manager who offers ongoing, consultative assistance, coordinates escalations, and arranges advanced engagements. Other features listed (Trusted Advisor checks, and 24/7 access to support engineers) are available with Business Support as well; architecture guidance exists in Enterprise but is typically delivered via the TAM and related Enterprise programs.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 31Correct  
Which of the following is a customer responsibility according to the AWS shared responsibility model?  
A. Apply security patches for Amazon S3 infrastructure devices.

#### Explications

Patching of the underlying hardware, storage, and network infrastructure that run Amazon S3 is performed by AWS as part of their responsibility for the security of the cloud. Customers are responsible for protecting their data, configuring access controls, and managing resources they deploy, not applying OS or firmware patches to AWS-managed infrastructure.  
B. Provide physical security for AWS datacenters.

#### Explications

Physical protection of AWS data centers (facility access controls, guards, cameras, and environmental controls) is managed by AWS. Physical security is part of the cloud provider’s responsibilities; customers must secure their accounts, data, and access but do not provide on-site physical security for AWS facilities.  
C. Install operating system updates on Lambda@Edge.

#### Explications

For serverless offerings like Lambda@Edge, AWS operates and updates the underlying runtime and host environment. Customers are responsible for their application code, dependencies, and permission policies, but not for installing or maintaining the operating system or host-level updates for the managed runtime.  
**Votre réponse est correcte**  
D. Implement multi-factor authentication (MFA) for IAM user accounts.

#### Explications

Managing identity and access for an AWS account is a customer responsibility. Implementing multi-factor authentication for IAM identities (and the root user) is a customer-controlled security configuration that reduces credential compromise risk and is explicitly part of ‘security in the cloud’ under the shared responsibility model.  
Explication générale  
This question tests understanding of the AWS shared responsibility model: AWS handles ‘security of the cloud’ (physical facilities, hardware, network, and managed service runtimes), while customers handle ‘security in the cloud’ (data protection, identity and access management, and configuration of their resources). The correct choice is the customer-managed identity control, whereas the other options describe protections that AWS provides for its infrastructure and managed runtimes.  
Domaine  
Domain 2: Security and Compliance  
Question 32Correct  
Which recommendation can AWS Cost Explorer provide to help reduce cost?  
A. Use a specific database engine.

#### Explications

AWS Cost Explorer analyzes cost and usage patterns and does not recommend application-level technology choices. Selecting a database engine involves performance, compatibility and licensing trade-offs (for which you would use service-specific guidance and the AWS Pricing Calculator), not a Cost Explorer cost-reduction suggestion.  
B. Change the programming language for an application.

#### Explications

Changing a programming language is a development decision that may affect runtime efficiency, but it is outside the scope of AWS Cost Explorer. Cost Explorer provides usage, rightsizing and reservation recommendations; it does not propose software-language changes.  
C. Deploy a specific operating system.

#### Explications

While operating system choice can influence licensing costs (for example, Windows vs. Linux), Cost Explorer does not issue OS selection recommendations. It focuses on resource utilization, cost trends, rightsizing and reservation analysis rather than prescribing a specific OS.  
**Votre réponse est correcte**  
D. Terminate an idle instance.

#### Explications

Correct — Cost Explorer’s rightsizing and cost-usage reports identify underutilized or idle compute resources and surface actions to reduce spend (for example, stop/terminate unused instances or change instance sizes). Note: related services such as AWS Compute Optimizer and Trusted Advisor also provide complementary instance-sizing and idle-resource recommendations.  
Explication générale  
The question tests knowledge of what AWS Cost Explorer provides for cost optimization. Cost Explorer analyzes cost and usage data to produce rightsizing and reservation recommendations (identifying underutilized or idle resources and suggesting termination or resizing). It does not make application-architecture decisions such as which database engine, programming language, or operating system to use.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 33Correct  
Which option is a shared control between AWS and the customer, according to the AWS shared responsibility model?  
**Votre réponse est correcte**  
A. Configuration management

#### Explications

Configuration-related responsibilities are split: AWS secures and maintains the underlying infrastructure (physical hosts, hypervisor, networking, and managed service configurations), while the customer is responsible for configuring and patching guest operating systems, applications, and enforcing secure baselines. AWS provides monitoring and remediation tools (for example AWS Config and Systems Manager) to help customers detect and manage configuration drift, which illustrates the shared nature of these controls.  
B. Physical and environmental controls

#### Explications

Physical and environmental controls (data‑center access, power, cooling, hardware maintenance, and physical security) are owned and operated by AWS. Customers have no responsibility for on‑site physical safeguards; their responsibilities are limited to logical controls for their resources running within AWS.  
C. Data integrity authentication

#### Explications

L'intégrité et l'authentification des données client au niveau applicatif et des données relèvent principalement de la responsabilité du client. AWS propose des services et des fonctionnalités (AWS KMS, sommes de contrôle, versionnage S3, TLS) qui prennent en charge l'intégrité et l'authentification, mais la mise en œuvre de la signature, du chiffrement et de la vérification au niveau applicatif reste à la charge du client.  
D. Gestion des identités et des accès

#### Explications

AWS fournit et exploite le service IAM et en assure la sécurité, mais il incombe aux clients de créer et de gérer les identités, les rôles, les politiques et les autorisations d'accès de leurs comptes et ressources. La configuration et l'application des politiques d'identité relèvent donc de la responsabilité du client et ne constituent pas un contrôle partagé dans ce modèle.  
Explication générale  
Le modèle de responsabilité partagée d'AWS répartit la sécurité entre AWS (sécurité du cloud : infrastructure physique, hébergement et exploitation des services gérés) et le client (sécurité dans le cloud : données, système d'exploitation invité, applications et contrôles d'accès). Les responsabilités de configuration sont partagées : AWS configure et maintient l'infrastructure sous-jacente, tandis que les clients configurent et maintiennent leurs systèmes d'exploitation, applications et paramètres de ressources. La gestion de la configuration constitue donc le contrôle partagé approprié. Les autres options relèvent principalement de la responsabilité d'AWS (contrôles physiques) ou, au contraire, de celle du client (intégrité des données/authentification et configuration des identités et des accès).  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 34Correct  
Une entreprise a une charge de travail qui s'exécutera en continu pendant un an. Cette charge de travail ne tolère aucune interruption de service. Quelle option d'achat Amazon EC2 sera la plus rentable ?  
**Votre réponse est correcte**  
A. Toutes les instances réservées à l'avance

#### Explications

Le paiement intégral de la réservation annuelle en une seule fois permet de bénéficier de la remise maximale sur les instances réservées, ce qui se traduit par un coût horaire effectif minimal et une facturation prévisible pour les charges de travail stables et continues. Cette option est particulièrement avantageuse car les instances réservées (contrairement aux instances Spot) ne sont pas interrompues pour la récupération de capacité, et un paiement anticipé couvrant l'intégralité du contrat maximise les économies réalisées sur les 12 mois.  
B. Instances partiellement réservées à l'avance

#### Explications

Les réservations partielles à l'avance combinent un paiement initial avec des frais continus et offrent des réductions par rapport à la réservation à la demande, mais les économies totales sur une période d'un an sont inférieures à celles réalisées en payant la totalité de la période à l'avance ; elles sont donc moins rentables lorsqu'une réduction maximale est souhaitée pour des charges de travail continues.  
C. Instances dédiées

#### Explications

Les instances dédiées s'exécutent sur du matériel mono-utilisateur et sont principalement utilisées pour l'isolation ou la conformité réglementaire. Elles engendrent des coûts supplémentaires par rapport à une infrastructure partagée et n'offrent pas le même niveau de réduction tarifaire à long terme que les instances réservées pour une optimisation des coûts en régime permanent.  
D. Instances à la demande

#### Explications

Les instances à la demande offrent une flexibilité maximale sans engagement à long terme et sont facturées à l'heure/à la seconde, mais pour une charge de travail exécutée en continu pendant un an, elles entraînent généralement un coût total plus élevé que les instances réservées ou les plans d'économies et ne constituent donc pas le choix le plus rentable pour les charges de travail stables et non interruptibles.  
Explication générale  
This item tests knowledge of EC2 purchasing options for steady, mission‑critical workloads. For a continuous, non‑interruptible 1‑year workload, committing to the full term with an upfront reservation maximizes discounts and billing predictability, making it the most cost‑effective choice. The distractors are either less discounted (partial upfront), targeted at isolation rather than cost reduction (dedicated tenancy), or designed for flexibility rather than long‑term savings (On‑Demand).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 35Correct  
Which AWS service gives users the ability to deploy highly repeatable infrastructure configurations?  
**Votre réponse est correcte**  
A. AWS CloudFormation

#### Explications

CloudFormation is AWS's declarative infrastructure-as-code service: you define resources in JSON/YAML templates and CloudFormation provisions them as stacks. It provides idempotent stack creation/updates, change sets for controlled modifications, drift detection to identify manual changes, and StackSets for consistent multi-account and multi-region deployment — all features that enable highly repeatable infrastructure provisioning.  
B. AWS CodeDeploy

#### Explications

CodeDeploy is an application deployment service that automates delivering application revisions to compute targets (EC2, Lambda, ECS). It orchestrates code rollout strategies (blue/green, rolling) but does not provide declarative templates or primary mechanisms for provisioning full infrastructure stacks.  
C. AWS CodeBuild

#### Explications

CodeBuild is a fully managed build service that compiles source code, runs tests, and produces build artifacts. It is part of CI/CD pipelines for building software, not a tool for declaring or provisioning infrastructure configurations.  
D. AWS Systems Manager

#### Explications

AWS Systems Manager offers operational capabilities (Run Command, State Manager, Automation, Parameter Store) to manage and configure existing resources and OS/application settings. While it can automate configuration tasks, it does not serve as the primary declarative IaC engine for provisioning entire AWS infrastructure stacks.  
Explication générale  
The question tests knowledge of AWS infrastructure-as-code. The correct choice is the service designed to declare and provision resources reproducibly using templates, with features such as idempotent stack operations, change sets, drift detection, and StackSets for multi-account/region deployment. The other options focus on application deployment, build services, or operational management and do not provide the same declarative, template-driven infrastructure provisioning capabilities.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 36Correct  
A company needs to store infrequently used data for data archives and long-term backups. Which AWS service or storage class will meet these requirements MOST cost-effectively?  
A. Amazon FSx for Lustre

#### Explications

A managed high‑performance file system built for low‑latency, high‑throughput compute workloads (HPC, ML, media processing). Its design and pricing target performance rather than low-cost, long‑term retention, so it is not cost‑effective for archival backups.  
B. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Block storage for EC2 instances intended for boot and transactional volumes with low latency. While snapshots provide backup capabilities, block volumes and their snapshots are not optimized for the lowest‑cost, long‑term archival storage compared with object storage archival tiers.  
C. Amazon Elastic File System (Amazon EFS)

#### Explications

A scalable NFS file system for shared file access that supports an infrequent access tier, but its pricing and access semantics are geared toward active file workloads. For long‑term archives and backups, object storage archival classes typically offer lower storage costs.  
**Votre réponse est correcte**  
D. Amazon S3 Glacier Flexible Retrieval

#### Explications

An S3 archival storage class designed for long‑term retention of infrequently accessed data with very low storage costs and multiple retrieval options (Expedited/Standard/Bulk). It integrates with S3 lifecycle policies to transition objects from hotter tiers and is purpose‑built for cost‑effective archives and backups (for even lower cost with longer retrieval times, Glacier Deep Archive is available).  
Explication générale  
This item tests selecting the most cost‑effective AWS storage for infrequently accessed, long‑term backups. The S3 Glacier archival tier provides the lowest storage cost and appropriate retrieval options and lifecycle integration for archives. The other choices are optimized for performance or active file/block storage and therefore are not the best fit for long‑term archival cost optimization.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 37Correct  
A team of researchers is going to collect data at remote locations around the world. Many locations do not have internet connectivity. The team needs to capture the data in the field, and transfer it to the AWS Cloud later. Which AWS service will support these requirements?  
A. AWS Outposts

#### Explications

Outposts extends AWS infrastructure, services, and APIs to on-premises locations for low-latency and local processing, but it is a permanently provisioned rack-level solution that assumes continuous connectivity and is not intended for collecting data offline in disconnected field locations or for physical shipment to AWS.  
B. AWS Transfer Family

#### Explications

Transfer Family provides managed SFTP/FTPS/FTP endpoints to move files directly into Amazon S3 or EFS over a network. It requires network connectivity at the transfer point and does not provide offline, physical appliances for disconnected data collection.  
**Votre réponse est correcte**  
C. AWS Snow Family

#### Explications

The Snow Family (Snowball, Snowball Edge, Snowmobile) provides rugged, tamper-evident appliances and edge-capable devices for local data collection and processing when network connectivity is limited. Data is encrypted (integrated with AWS KMS), stored locally on the device, and the device is physically shipped to AWS for secure ingestion into S3—making it the appropriate solution for disconnected field data capture and later transfer to the cloud.  
D. AWS Migration Hub

#### Explications

Migration Hub offers visibility and tracking for application migration projects (status and progress) but does not provide mechanisms for physical data collection, offline storage appliances, or transport of collected data to AWS.  
Explication générale  
This scenario requires secure offline data capture and physical transport to AWS. The Snow Family supplies encrypted, rugged devices and edge capabilities for collecting and storing data without network connectivity and then physically shipping the devices for ingestion—unlike Outposts (on-premises AWS infra requiring provisioning and connectivity), Transfer Family (network-based file transfer), or Migration Hub (migration tracking only).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 38Correct  
Which task is the responsibility of a company that is using Amazon RDS?  
A. Provision the underlying infrastructure.

#### Explications

Amazon RDS is a managed database service; AWS is responsible for provisioning and operating the underlying physical and virtual infrastructure (hosts, storage, networking, hypervisor). Customers choose DB instance classes, storage size, and configuration settings, but they do not provision physical hardware or the underlying infrastructure stack.  
**Votre réponse est correcte**  
B. Create IAM policies to control administrative access to the service.

#### Explications

Managing identities and access is the customer's responsibility under the AWS Shared Responsibility Model. Customers must create IAM users, groups, roles, and policies to control who can perform RDS API/console actions and to enforce least-privilege access. RDS can integrate with IAM (including IAM database authentication for supported engines) and IAM roles for resource access, but policy creation and access governance remain with the customer.  
C. Install the cables to connect the hardware for compute and storage.

#### Explications

Physical data center tasks (cabling, rack hardware installation, physical maintenance) are performed by AWS. Customers do not have access to or responsibility for the physical layer of AWS data centers; AWS handles facilities management and physical security.  
D. Install and patch the RDS operating system.

#### Explications

For standard Amazon RDS DB instances, AWS manages the operating system and database engine patching and maintenance as part of the managed service. (Note: specialized offerings such as RDS Custom provide more OS-level control to customers, but the typical RDS service offloads OS installation and patching to AWS.)  
Explication générale  
This question tests understanding of the AWS Shared Responsibility Model for a managed service. Amazon RDS offloads infrastructure, physical hardware, and OS-level management to AWS, while customers retain responsibility for identity and access management, database configuration, and data-level security. Therefore, creating and managing IAM policies to control administrative access is the customer's responsibility, whereas the other tasks are handled by AWS.  
Domaine  
Domain 2: Security and Compliance  
Question 39Correct  
A solutions architect needs to maintain a fleet of Amazon EC2 instances so that any impaired instances are replaced with new ones. Which AWS service should the solutions architect use?  
A. Amazon Elastic Container Service (Amazon ECS)

#### Explications

ECS is a container orchestration service for running and scaling containerized workloads (on EC2 or Fargate). It manages tasks and services, not the lifecycle replacement of underlying EC2 instances; replacing impaired EC2 instances is handled by Auto Scaling groups or EC2 Auto Scaling, not by ECS itself.  
B. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat-detection service that analyzes account and workload activity to surface security findings. It does not perform instance lifecycle management or automatically replace unhealthy EC2 instances.  
C. AWS Shield

#### Explications

AWS Shield provides DDoS protection and mitigation for network and application-layer attacks. It is focused on availability under attack, not on monitoring EC2 instance health or replacing impaired instances.  
**Votre réponse est correcte**  
D. AWS Auto Scaling

#### Explications

Auto Scaling (via EC2 Auto Scaling groups) maintains a desired capacity by performing health checks and automatically terminating and launching instances to replace unhealthy ones. It integrates with ELB health checks, CloudWatch alarms, lifecycle hooks, and scaling policies to ensure fleet health and availability.  
Explication générale  
The question tests knowledge of which AWS feature maintains an EC2 fleet and replaces impaired instances. Auto Scaling (EC2 Auto Scaling groups) is designed to preserve desired capacity by detecting unhealthy instances (via EC2/ELB health checks) and launching replacements. The distractors (ECS, GuardDuty, Shield) are real AWS services but address container orchestration, threat detection, and DDoS protection respectively, not automatic EC2 instance replacement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 40Correct  
A company wants an Amazon S3 solution that provides access to object storage within single-digit milliseconds. Which solution will meet these requirements?  
**Votre réponse est correcte**  
A. S3 Express One Zone

#### Explications

This storage class is purpose-built to deliver single-digit millisecond access by keeping objects immediately available in S3 storage while optimizing for cost and latency. It is a one-Availability-Zone storage class, so it trades multi-AZ resilience for lower cost and the targeted low-latency access required by the scenario.  
B. S3 Standard

#### Explications

S3 Standard provides high durability and low, millisecond-level latency across multiple Availability Zones and is suitable for frequently accessed data, but it is not specifically optimized or marketed to guarantee single-digit millisecond access or the lower-cost, one-zone latency profile provided by the specialized Express One Zone class.  
C. S3 Glacier Flexible Retrieval

#### Explications

S3 Glacier Flexible Retrieval is an archival storage class with retrieval times measured in minutes to hours for most retrieval options. It is intended for long-term archive and infrequent access, so it cannot meet single-digit millisecond access requirements.  
D. S3 Glacier Instant Retrieval

#### Explications

S3 Glacier Instant Retrieval offers archive-class storage with immediate (millisecond) retrieval for cold data, but it is designed for archival use cases and cost/retention trade-offs rather than being optimized specifically to deliver guaranteed single-digit millisecond latency like the Express One Zone class.  
Explication générale  
AWS S3 provides multiple storage classes that balance cost, durability, and access latency. The Express One Zone class is the best fit when the requirement is explicit single-digit millisecond access because it is engineered for very low-latency, one-AZ object access at reduced cost. S3 Standard offers low-latency, multi-AZ access but is not optimized specifically for guaranteed single-digit millisecond access; Glacier classes are archival and either have slower retrieval (Flexible Retrieval) or are archival-focused despite instant retrieval capability (Glacier Instant Retrieval).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 41Correct  
A company runs Amazon EC2 instances in a research lab. The instances run for 3 hours each week and cannot be interrupted. What is the MOST cost-effective instance purchasing option to meet these requirements?  
A. Compute Savings Plan

#### Explications

Compute Savings Plans require a monetary commitment (a $/hour discount applied across compute usage) over a 1- or 3-year term. They provide value when you have sustained, predictable compute spend to amortize the commitment. For a workload that runs only  
**Votre réponse est correcte**  
B. On-Demand Instances

#### Explications

Using pay-as-you-go EC2 capacity with no long-term commitment is the most appropriate choice for very low, infrequent runtime and for workloads that must not be interrupted. At  
C. Convertible Reserved Instances

#### Explications

Convertible Reserved Instances (or standard RIs) provide significant hourly discounts in exchange for a 1- or 3-year commitment and are intended for steady, predictable usage. Although convertible RIs allow instance family/type changes, the required long-term commitment makes them poor value for a few hours of weekly usage.  
D. Spot Instances

#### Explications

Spot capacity delivers the deepest discounts but is interruptible: EC2 can reclaim Spot instances with a short warning. Because the lab instances cannot be interrupted, Spot’s termination risk makes it unsuitable despite the lower price.  
Explication générale  
This item tests understanding of EC2 purchasing models and the trade-offs between cost, commitment, and interruption tolerance. For very small, infrequent, non-interruptible runs, the pay-as-you-go model avoids multi-year commitments that would not be utilized and prevents interruption risks inherent in Spot. Long-term commitments (Savings Plans, Reserved Instances) only become cost-effective when usage is sustained enough to amortize the discount.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 42Correct  
Which AWS services or features provide high availability and low latency by enabling failover across different AWS Regions? (Choose two.)  
**Votre sélection est correcte**  
A. Amazon Route 53

#### Explications

Uses DNS-based routing (latency-based, geolocation, failover) together with health checks to direct clients to healthy endpoints in other AWS Regions. This enables automated DNS failover and selection of the lowest-latency regional endpoint for users.  
B. Network Load Balancer

#### Explications

Operates at the regional level across Availability Zones. It provides high throughput and low latency within a region but has no built-in cross-region failover capability, so it cannot be used alone to fail over traffic between Regions.  
C. Amazon S3 Transfer Acceleration

#### Explications

Optimizes client-to-bucket transfer performance by using the Amazon edge network for faster uploads to a single bucket/region. It does not provide cross-region failover or multi-region availability (S3 Cross-Region Replication is a separate feature).  
**Votre sélection est correcte**  
D. AWS Global Accelerator

#### Explications

Provides static anycast IPs and routes traffic over the AWS global network to optimal regional endpoints, with endpoint groups and health checks for automatic failover between Regions, improving both availability and latency for global users.  
E. Application Load Balancer

#### Explications

Is a Layer 7, regional load balancer that balances HTTP/HTTPS traffic across targets in Availability Zones. It supports routing features within a region but does not provide cross-region failover.  
Explication générale  
The correct choices are the DNS-level and global-network services that can route and fail over traffic across Regions: DNS routing with health checks (Route 53\) and Global Accelerator’s anycast endpoints and regional endpoint groups. Regional load balancers (ALB, NLB) and S3 Transfer Acceleration address regional traffic distribution or faster uploads, not automated cross-region failover.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 43Correct  
A company has a test AWS environment. A company is planning on testing an application within AWS. The application testing can be interrupted and does not need to run continuously. Which Amazon EC2 purchasing option will meet these requirements MOST cost-effectively?  
A. On-Demand Instances

#### Explications

On-Demand provides immediate, pay-as-you-go compute with no long-term commitment. It is appropriate for unpredictable or short-lived tasks that require guaranteed capacity, but it is more expensive per hour than options that use spare capacity, so it is not the most cost-effective for interruptible test workloads.  
B. Dedicated Instances

#### Explications

Dedicated Instances run on single-tenant hardware to meet isolation or compliance needs. They incur a higher cost and do not provide cost savings for transient, interruptible testing, making them unsuitable for this scenario.  
**Votre réponse est correcte**  
C. Spot Instances

#### Explications

Spot Instances leverage spare EC2 capacity at significant discounts, making them the best fit for workloads that can tolerate interruptions. AWS can reclaim Spot capacity (with a two-minute interruption notice), so use checkpointing, job retries, Spot Fleets, or Auto Scaling mixed-instance policies to maintain reliability while minimizing cost.  
D. Reserved Instances

#### Explications

Reserved Instances (and Savings Plans) reduce hourly costs in exchange for a long-term commitment and are intended for predictable, steady-state usage. They are not the best choice for intermittent, interruptible testing that lacks consistent runtime.  
Explication générale  
This question tests EC2 purchasing models and cost optimization. For testing that can be interrupted and does not require continuous operation, the most cost-effective choice is to run on spare capacity with discounted instances and handle interruptions (Spot Instances). On-Demand is flexible but costlier; Reserved or Dedicated options are designed for steady-state commitments or single-tenant isolation and are inappropriate for transient, interruptible tests.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 44Correct  
Which AWS service or feature identifies whether an Amazon S3 bucket or an IAM role has been shared with an external entity?  
A. AWS Service Catalog

#### Explications

Incorrect. AWS Service Catalog is focused on provisioning and governing a curated set of approved products (templates) for self-service deployment; it does not analyze resource-based policies or inspect S3 bucket or IAM role trust policies to detect external sharing.  
B. AWS Systems Manager

#### Explications

Incorrect. AWS Systems Manager provides operational management (run commands, patching, inventory, Session Manager, Parameter Store) for instances and resources; it does not perform policy analysis to identify resources that are shared with external principals.  
**Votre réponse est correcte**  
C. AWS IAM Access Analyzer

#### Explications

Correct. IAM Access Analyzer analyzes resource-based policies and IAM trust policies (for example, S3 bucket policies and IAM role trust policies) and uses policy analysis to generate findings when a resource is accessible by principals outside the account or outside the AWS Organization. It surfaces external-sharing findings so you can review and remediate unintended access.  
D. AWS Organizations

#### Explications

Incorrect. AWS Organizations manages and governs multiple AWS accounts (billing, consolidated management, and service control policies) but does not inspect individual resource policies to detect whether an S3 bucket or an IAM role has been shared with external principals.  
Explication générale  
This question tests knowledge of which AWS feature performs policy analysis to detect external sharing of resources. IAM Access Analyzer inspects resource-based and trust policies and produces findings when access is granted to principals outside your account or organization. The other services (Service Catalog, Systems Manager, Organizations) address provisioning, operational management, or account governance but do not perform the resource-policy analysis required to detect external sharing.  
Domaine  
Domain 2: Security and Compliance  
Question 45Incorrect  
Which AWS service provides a single location to track the progress of application migrations?  
**Votre réponse est incorrecte**  
A. AWS Application Discovery Service

#### Explications

AWS Application Discovery Service is an on‑premises discovery and data‑collection tool that inventories servers, collects configuration and performance data, and helps plan migrations. It does not provide a centralized, ongoing dashboard to track migration progress across multiple migration tools.  
B. AWS Application Migration Service

#### Explications

AWS Application Migration Service (MGN) focuses on automating lift‑and‑shift migrations by replicating servers, orchestrating cutover, and executing migration tasks for specific workloads. It is an execution tool and does not serve as a single aggregated tracking location for migrations performed with multiple tools.  
C. AWS Service Catalog

#### Explications

AWS Service Catalog enables organizations to create, manage, and govern catalogs of approved IT products and deployments for users. Its purpose is governance and standardized provisioning, not migration tracking or reporting of migration status.  
**Bonne réponse**  
D. AWS Migration Hub

#### Explications

AWS Migration Hub provides a central dashboard that aggregates migration status from multiple AWS migration services and partner tools, presenting application‑centric and server‑level progress, tracking of migration waves, and metrics across the migration lifecycle. Because it consolidates status from discovery and execution tools, it is the appropriate service for single‑location tracking of migration progress.  
Explication générale  
The question tests knowledge of AWS services used during migrations. AWS Migration Hub is the centralized tracking service that aggregates status information from discovery and migration tools, giving application‑level visibility into progress. The other options represent complementary capabilities (discovery, execution, or service catalog/governance) but do not provide a single, consolidated migration progress dashboard.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 46Incorrect  
A company wants to use automated video analysis to identify employees that are accessing its offices. Which AWS service will meet this requirement?  
**Bonne réponse**  
A. Amazon Rekognition

#### Explications

Rekognition provides managed image and video analysis, including Rekognition Video for asynchronous analysis, face detection, face comparison, and face search against indexed collections. It can ingest video (S3 or Kinesis Video Streams), index known employee faces into collections, and perform face-matching to identify employees in footage.  
B. Amazon Polly

#### Explications

Amazon Polly is a text-to-speech service that synthesizes spoken audio from text. It does not provide any computer-vision or video-analysis capabilities and therefore cannot be used to identify people in video.  
**Votre réponse est incorrecte**  
C. Amazon Cognito

#### Explications

Amazon Cognito manages user sign-up, sign-in, authentication, and user directories for applications (user pools and identity pools). It is not a computer-vision or video-processing service and cannot analyze or recognize faces in video.  
D. AWS Lambda

#### Explications

AWS Lambda is serverless compute for running code in response to events; it can orchestrate workflows and invoke Rekognition but does not include built-in machine‑vision models for analyzing video. Lambda is useful as glue code, not as the face-recognition engine.  
Explication générale  
The question tests knowledge of which AWS service offers managed computer-vision capabilities for video-based identification. Amazon Rekognition is the appropriate choice because it provides face detection, face search, and video-analysis APIs (including integration with S3 and Kinesis Video Streams) to identify people. The other options are unrelated: Polly is text-to-speech, Cognito handles user identity for applications, and Lambda is compute for running code and orchestration but not a vision service.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 47Incorrect  
A company wants to run CPU-intensive workload across multiple Amazon EC2 instances. Which EC2 instance type should the company use to meet this requirement?  
A. General purpose instances

#### Explications

General purpose instances (for example, M and T families) provide a balanced mix of compute, memory, and networking to support a wide range of workloads. They are not tuned to maximize raw CPU throughput or provide the highest vCPU-to-memory ratio, so they are less efficient than compute-optimized instances for sustained, CPU-bound workloads.  
**Bonne réponse**  
B. Compute optimized instances

#### Explications

Compute-optimized instance families (C series) offer a high vCPU-to-memory ratio, high clock-speed processors (Intel/AMD or AWS Graviton options), and network/Nitro-performance features designed for sustained, CPU-bound workloads such as scientific modeling, batch processing, and high-performance compute. These characteristics make them the appropriate choice for CPU-intensive tasks that will run across multiple EC2 instances.  
**Votre réponse est incorrecte**  
C. Memory optimized instances

#### Explications

Memory-optimized instances (R, X families) provide large amounts of RAM relative to vCPU and are intended for in-memory databases, real-time big data analytics, and other memory-bound applications. Their configuration favors memory capacity over raw CPU throughput, so they are not the best fit for primarily CPU-bound workloads.  
D. Storage optimized instances

#### Explications

Storage-optimized instances (I, D families) are designed to deliver high, low-latency local storage I/O (NVMe instance store or high-throughput EBS configurations) for workloads like data warehousing or log processing. Their optimizations focus on disk I/O and throughput rather than maximizing CPU compute performance.  
Explication générale  
The question tests instance family selection for CPU-bound workloads. Compute-optimized (C) EC2 instance families are tailored for high CPU performance with a high vCPU-to-memory ratio, high clock speeds, and platform features (Nitro, enhanced networking) that improve sustained compute throughput across multiple instances. Other families—general purpose, memory-optimized, and storage-optimized—optimize different resource balances (balanced, memory capacity, or I/O throughput) and therefore are less suitable for sustained CPU-intensive tasks.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 48Correct  
A company is launching a mobile app in the AWS Cloud. The company wants the app's users to sign in through social media identity providers (IdPs). Which AWS service will meet this requirement?  
A. AWS Lambda

#### Explications

Serverless compute used to run code in response to events; it can host custom authentication logic or backend endpoints but is not a managed identity or federation service and does not provide built-in social sign-in flows, token issuance, or SDK integrations for mobile authentication.  
**Votre réponse est correcte**  
B. Amazon Cognito

#### Explications

Managed identity service that provides user pools (authentication), federation with social IdPs (Google, Facebook, Apple, Login with Amazon) through OAuth2/OIDC, issues JWT tokens, and integrates with AWS SDKs for mobile apps; it’s designed specifically to enable social sign-in and to exchange federated identities for AWS credentials when needed.  
C. AWS Secrets Manager

#### Explications

Service for storing, retrieving, and rotating secrets such as database credentials and API keys; it secures backend secrets but does not provide end-user authentication, social identity federation, or token-based sign-in flows.  
D. Amazon CloudFront

#### Explications

Global content delivery network for caching and delivering content with low latency; it can accelerate app content delivery but does not handle user authentication, identity federation, or provide social sign-in capabilities.  
Explication générale  
The question tests recognition of the AWS service that supports mobile app social sign-in. The correct service is the managed identity solution that offers user pools, social IdP federation, OAuth/OIDC token issuance, and mobile SDK integration. The other options are core AWS services (compute, secret management, CDN) that serve different purposes and do not provide built-in social identity federation for end users.  
Domaine  
Domain 2: Security and Compliance  
Question 49Correct  
Which AWS service or feature can a company use to apply security rules to specific Amazon EC2 instances?  
A. Network ACLs

#### Explications

Network ACLs are stateless packet filters applied at the subnet boundary in a VPC. They affect all resources in a subnet and require separate inbound and outbound rules, so they cannot be targeted to a single EC2 instance or its network interface.  
**Votre réponse est correcte**  
B. Security groups

#### Explications

Security groups are stateful virtual firewalls applied at the Elastic Network Interface (ENI) level and can be attached to specific EC2 instances. They allow you to define inbound and outbound allow rules (return traffic is automatically permitted) and support referencing other security groups for granular, instance-level access control.  
C. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor provides best-practice checks and recommendations across cost, performance, security, fault tolerance, and service limits. It is an advisory tool and does not deploy or enforce instance-level network/firewall rules.  
D. AWS WAF

#### Explications

AWS WAF is a web application firewall that inspects and filters HTTP/HTTPS requests for resources such as CloudFront, Application Load Balancer, and API Gateway. It operates at the application layer and is not used to apply network-level security directly to EC2 instances.  
Explication générale  
The key distinction is between instance-level and subnet/application-level controls. Security groups provide stateful, instance-level network access control and can be attached to individual EC2 network interfaces, making them the correct choice. Network ACLs are subnet-scoped and stateless, AWS WAF protects web application traffic at layer 7, and Trusted Advisor only offers recommendations rather than enforcing rules.  
Domaine  
Domain 2: Security and Compliance  
Question 50Correct  
Which AWS services make use of global edge locations? (Choose two.)  
A. AWS Fargate

#### Explications

Incorrect — AWS Fargate is a serverless container compute engine (ECS/EKS launch type) that runs tasks within AWS Regions and Availability Zones. It is a regional compute service and does not leverage AWS global edge locations (Points of Presence) for content delivery or traffic acceleration.  
**Votre sélection est correcte**  
B. Amazon CloudFront

#### Explications

Correct — Amazon CloudFront is AWS’s content delivery network that caches objects at a global network of edge locations (Points of Presence) and regional edge caches to reduce latency for end users and offload origin servers.  
**Votre sélection est correcte**  
C. AWS Global Accelerator

#### Explications

Correct — AWS Global Accelerator uses the AWS global network and edge locations (PoPs) to accept client traffic via static anycast IPs and route it to the optimal regional endpoints, improving latency, availability, and failover behavior.  
D. AWS Wavelength

#### Explications

Incorrect — AWS Wavelength places compute capacity in telecom operator locations (Wavelength Zones) at the 5G network edge for ultra-low-latency mobile workloads. These Wavelength Zones are distinct from CloudFront/Global Accelerator global edge locations and are not the same PoP network used for CDN/accelerator functions.  
E. Amazon VPC

#### Explications

Incorrect — Amazon VPC (Virtual Private Cloud) is a regional virtual network construct that provides isolated subnets, routing, and security controls within a region; it does not use global edge locations for delivering or accelerating user traffic.  
Explication générale  
This question tests knowledge of AWS services that use global edge locations (Points of Presence). Services that push traffic into AWS’s PoP network—specifically CloudFront (a CDN that caches content at edge locations) and Global Accelerator (which accepts client traffic at PoPs and routes it over the AWS global network)—are correct. The other options are regional or specialized-edge constructs (Fargate and VPC are regional; Wavelength is a telecom-edge solution distinct from the global PoP network) and therefore do not use the global edge location network for CDN/acceleration.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 51Correct  
A company wants to block SQL injection attacks. Which AWS service or feature should the company use to meet this requirement?  
**Votre réponse est correcte**  
A. AWS WAF

#### Explications

Provides application‑layer (HTTP/S) inspection and rule engines that can detect and block SQL injection patterns. Use built‑in managed rule groups (e.g., SQLi rules) or custom rule statements and deploy WAF in front of CloudFront, API Gateway, or an ALB so malicious payloads are stopped before they reach the application.  
B. Network ACLs

#### Explications

Stateless, subnet-level packet filters that allow/deny traffic by IP, protocol, and port. They do not inspect HTTP request bodies or application-layer content, so they cannot detect or block SQL injection payloads.  
C. Security groups

#### Explications

Instance/resource-level, stateful virtual firewalls controlling IP/port/protocol. They do not perform deep payload inspection of HTTP requests and therefore cannot mitigate SQL injection attacks.  
D. AWS Certificate Manager (ACM)

#### Explications

Manages issuance and lifecycle of TLS/SSL certificates to encrypt data in transit. Certificate management provides encryption but does not inspect or filter application-layer requests and cannot prevent SQL injection.  
Explication générale  
Blocking SQL injection requires application-layer request inspection and pattern/rule-based blocking. An application firewall that can analyze HTTP/S payloads and apply SQLi-specific rules is the correct solution; WAF supplies managed and custom SQLi protections. Network ACLs and security groups operate at network/transport layers and lack payload inspection, while ACM only handles TLS certificates.  
Domaine  
Domain 2: Security and Compliance  
Question 52Incorrect  
Which AWS service helps users plan and track their server and application inventory migration data to AWS?  
A. Amazon CloudWatch

#### Explications

Incorrect — This service is AWS’s monitoring and observability platform that collects metrics, logs, and events and provides alarms and dashboards. It is used to monitor resource and application health, not to plan or maintain a migration inventory or provide a centralized migration progress dashboard.  
B. AWS DataSync

#### Explications

Incorrect — This is a managed data-transfer service that automates and accelerates movement of files between on‑premises storage and AWS storage services (S3, EFS, FSx). It handles data transfer operations but does not provide migration inventory planning or a centralized migration tracking dashboard.  
**Bonne réponse**  
C. AWS Migration Hub

#### Explications

Correct — This service provides a central place to discover, group, and track migrations across AWS and partner migration tools. It aggregates migration status from multiple tools, offers migration groups and per‑application/server progress, and is intended specifically for planning and tracking server and application migration inventories.  
**Votre réponse est incorrecte**  
D. AWS Application Migration Service

#### Explications

Incorrect — This service automates replication and orchestration for lift‑and‑shift migrations (server replication, testing, and cutover). It executes migrations and can report status to a central tracker, but it is not the primary tool for planning or maintaining a centralized migration inventory and progress dashboard.  
Explication générale  
The question tests knowledge of AWS migration tracking tools. The central, purpose‑built service for planning and tracking server and application migration inventories and consolidating status across migration tools is the migration tracking service (Migration Hub). The other options are focused on monitoring (CloudWatch), data transfer (DataSync), or executing migrations (Application Migration Service) and therefore do not serve as the centralized inventory/planning dashboard.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 53Correct  
When designing AWS workloads to be operational even when there are component failures, what is an AWS best practice?  
A. Perform quarterly disaster recovery tests.

#### Explications

Incorrect. Performing disaster recovery tests exercises recovery procedures and validates runbooks, but the testing schedule itself does not make an architecture resilient. Achieving operational resilience requires designing redundancy, fault isolation, and automated recovery mechanisms (as described in the AWS Well‑Architected Reliability pillar), not just periodic tests.  
B. Place the main component on the us-east-1 Region.

#### Explications

Incorrect. Concentrating primary resources in a single AWS Region creates a regional single point of failure. Resilient architectures use multiple Availability Zones and, when needed, cross‑region replication or failover (for example, Route 53 failover routing, S3 replication, or cross‑region RDS strategies) to tolerate zone- or region-level outages.  
**Votre réponse est correcte**  
C. Design for automatic failover to healthy resources.

#### Explications

Correct. Architectures that automatically shift traffic or workloads to healthy resources reduce recovery time and remove manual intervention. AWS implementations include ALB/NLB with health checks and Auto Scaling, Route 53 health checks and failover routing, RDS Multi‑AZ and Aurora automatic failover, and multi‑region active/active or active/passive deployments — all aligned with the Reliability pillar.  
D. Design workloads to fit on a single Amazon EC2 instance.

#### Explications

Incorrect. Relying on a single EC2 instance introduces a single point of failure: if that instance fails, the service is unavailable. Use Auto Scaling groups across multiple AZs, managed services, and distributed designs to provide redundancy and fault isolation.  
Explication générale  
The question targets architectural resilience: the recommended practice is to build automatic failover and redundancy so healthy resources take over during component failures. This is achieved via AWS features such as Elastic Load Balancing, Auto Scaling, Route 53 failover, and RDS Multi‑AZ/Aurora failover. Options that focus only on test cadence or concentrate resources in a single instance or region do not provide the same level of continuous availability.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 54Correct  
Which of the following are ways to improve security on AWS? (Choose two.)  
A. Using AWS Artifact

#### Explications

AWS Artifact provides access to compliance reports, certifications, and contractual agreements (for example, SOC, ISO, and PCI reports) to support audits and regulatory requirements. It does not change configurations or enforce controls in your account, so it does not directly harden the environment.  
B. Granting the broadest permissions to all IAM roles

#### Explications

Granting overly broad permissions violates the principle of least privilege, increases attack surface, and enables privilege escalation. Secure AWS deployments use narrowly scoped IAM policies, role assumptions, permissions boundaries, and monitoring—not blanket permissions.  
C. Running application code with AWS Cloud

#### Explications

Merely running workloads on AWS does not automatically improve security. Actual security improvements require applying controls such as network segmentation (VPC, security groups), encryption, patch management, IAM best practices, and managed security services when deploying applications.  
**Votre sélection est correcte**  
D. Enabling multi-factor authentication (MFA) with Amazon Cognito

#### Explications

Requiring a second authentication factor for user sign-in greatly reduces the impact of compromised credentials. Amazon Cognito supports MFA and adaptive authentication for user pools, enabling administrators to enforce second-factor verification (TOTP or SMS) and strengthen identity protection.  
**Votre sélection est correcte**  
E. Using AWS Trusted Advisor security checks

#### Explications

AWS Trusted Advisor performs automated checks across an account and identifies security-related misconfigurations (for example, exposed S3 objects, unused IAM credentials, and missing MFA) and provides prioritized, actionable recommendations to remediate risks and improve security posture.  
Explication générale  
This question tests AWS security best practices. The correct choices are implementing stronger identity protection (MFA via the identity service) and using AWS tooling that discovers and recommends fixes for misconfigurations (Trusted Advisor). The other options either do not enforce controls (Artifact, simply running workloads on AWS) or actively reduce security (broad IAM permissions).  
Domaine  
Domain 2: Security and Compliance  
Question 55Incorrect  
A company wants a cost-effective option when running its applications in an Amazon EC2 instance for short time periods. The applications can be interrupted. Which EC2 instance type will meet these requirements?  
**Bonne réponse**  
A. Spot Instances

#### Explications

EC2 Spot Instances use spare EC2 capacity offered at steep discounts and are intended for fault-tolerant, stateless, short-duration workloads. They can be reclaimed by AWS with a short (approximately two-minute) warning, making them ideal when interruptions are acceptable and minimizing compute cost is the primary goal.  
**Votre réponse est incorrecte**  
B. On-Demand Instances

#### Explications

On-Demand Instances provide per-second billing and no long-term commitment, so they are flexible for short runs, but their pricing is regular (higher) compared with spare-capacity offerings. They are not reclaimed by AWS and therefore do not provide the same level of cost savings for interruptible workloads.  
C. Reserved Instances

#### Explications

Reserved Instances (and similar billing constructs like Savings Plans) provide lower rates in exchange for 1- or 3-year commitments and are designed for predictable, steady-state usage. They are not cost-effective for short-lived, intermittent workloads that can be frequently interrupted.  
D. Dedicated Instances

#### Explications

Dedicated Instances run on single-tenant hardware to provide isolation for compliance or licensing reasons; this increases cost and is not appropriate when the priority is short-term, interruptible, cost-optimized compute.  
Explication générale  
The question tests knowledge of EC2 purchasing options for workloads that tolerate interruptions. The spare-capacity option that offers the largest cost savings for short, interruptible jobs is Spot (EC2 Spot) because AWS can reclaim those instances with short notice. On-Demand avoids interruptions but costs more; Reserved/Savings Plans require long commitments for discounts; Dedicated Instances increase isolation and cost—none match the interruptible+cost-optimized requirement as well as Spot.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 56Correct  
A company needs to connect its on-premises data center to the AWS Cloud. The company needs a dedicated, low-latency connection with consistent network performance. Which AWS service will meet these requirements?  
A. AWS Global Accelerator

#### Explications

AWS Global Accelerator provides static anycast IPs and routes user traffic to optimal AWS endpoints at edge locations to improve global application availability and performance. It optimizes client-to-edge routing but does not create a private, dedicated network link from an on-premises data center into AWS, so it cannot guarantee the dedicated, consistent, low-latency connectivity required here.  
B. Amazon CloudFront

#### Explications

Amazon CloudFront is a content delivery network that caches and serves content from edge locations to reduce latency for end users. It is not a mechanism for establishing a private, dedicated connection between an on-premises data center and AWS and therefore does not meet the requirement for a dedicated low-latency link.  
**Votre réponse est correcte**  
C. AWS Direct Connect

#### Explications

AWS Direct Connect provisions a physical or hosted dedicated network connection between your on-premises network and AWS. It provides predictable, lower-latency and higher-throughput connectivity than internet-based links, supports private Virtual Interfaces to access VPCs (and public VIFs for AWS public endpoints), can be combined with Direct Connect Gateway and Link Aggregation Groups, and is the appropriate choice when dedicated, consistent network performance is required.  
D. AWS Managed VPN

#### Explications

AWS Managed VPN creates IPsec-encrypted tunnels over the public internet to connect on-premises networks to AWS. While secure and commonly used for connectivity or as a backup to Direct Connect, it relies on internet routing and can exhibit variable latency and throughput, so it does not provide the guaranteed, dedicated performance described in the question.  
Explication générale  
The requirement is for a dedicated, low-latency connection with consistent performance between an on-premises data center and AWS. AWS Direct Connect is specifically designed to provide a private, dedicated network connection with predictable latency and higher bandwidth compared with internet-based options. The other choices (Global Accelerator, CloudFront, Managed VPN) either optimize client-to-AWS edge performance, provide CDN caching, or rely on the internet and therefore do not provide the dedicated, consistent link required.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 57Correct  
A company needs to use Amazon S3 to store audio files that are each 5 megabytes in size. The company will rarely access the files, but the company must be able to retrieve the files immediately. Which S3 storage class will meet these requirements MOST cost-effectively?  
A. S3 Standard

#### Explications

Incorrect — S3 Standard provides the highest availability and low-latency access for frequently accessed objects, but its storage price is higher than the infrequent-access classes, making it less cost-effective for data that is rarely accessed.  
**Votre réponse est correcte**  
B. S3 Standard-Infrequent Access (S3 Standard-IA)

#### Explications

Correct — S3 Standard-Infrequent Access is designed for long-lived objects that are accessed infrequently but require millisecond (immediate) retrieval when needed. It offers lower storage cost than S3 Standard while applying higher retrieval and request charges, which makes it the most cost-effective choice for 5 MB audio files that are rarely accessed but must be available immediately.  
C. S3 Glacier Flexible Retrieval

#### Explications

Incorrect — S3 Glacier Flexible Retrieval (formerly Glacier) is an archival class intended for long-term storage where retrievals can take minutes to hours depending on the retrieval option. Because the question requires immediate access, Glacier Flexible Retrieval is not appropriate despite its lower storage cost for archival data.  
D. S3 Glacier Deep Archive

#### Explications

Incorrect — S3 Glacier Deep Archive is optimized for the lowest-cost, long-term archival storage and typically requires hours for retrieval. It does not meet the immediate-retrieval requirement and therefore is not suitable for this scenario.  
Explication générale  
Choose S3 Standard-Infrequent Access when objects are rarely accessed but must be retrieved immediately: it balances lower storage pricing with instant availability, while trading off higher retrieval/request fees. S3 Standard would be more expensive for infrequently accessed objects, and the Glacier classes are cheaper for storage but impose retrieval delays (minutes to hours) that violate the immediate-access requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 58Correct  
Which AWS service or feature improves network performance by sending traffic through the AWS worldwide network infrastructure?  
A. Route table

#### Explications

Defines routing rules inside a single VPC to direct traffic between subnets, gateways, and VPC endpoints. This is a local VPC construct and does not steer client traffic onto the AWS global network to reduce Internet latency.  
B. AWS Transit Gateway

#### Explications

Acts as a hub to connect multiple VPCs, VPNs, and Direct Connect attachments at scale and supports inter‑region peering for VPC connectivity. It centralizes routing but is not an edge‑based service that advertises Anycast IPs or optimizes end‑user traffic across the AWS global backbone for lower latency.  
**Votre réponse est correcte**  
C. AWS Global Accelerator

#### Explications

Uses static Anycast IP addresses announced from AWS edge locations and steers user connections onto the AWS global network backbone to reach the optimal regional endpoint (ALB/NLB/EC2). Provides health checks and automatic failover, reduces latency and jitter compared with public‑internet routing, and is specifically designed to accelerate global client traffic.  
D. Amazon VPC

#### Explications

Provides a logically isolated virtual network for launching AWS resources with control over IP ranges, subnets, and security controls. It governs network topology and access within AWS but does not itself route public client traffic over the AWS worldwide backbone to accelerate global performance.  
Explication générale  
The question tests knowledge of services that improve global network performance by leveraging AWS's private backbone. The correct choice provides Anycast static IPs, edge admission into the AWS global network, health checks and failover to reduce latency for end users. The other options (VPC route tables, Transit Gateway, and VPC) are networking constructs or connectivity services that manage routing or connectivity within/between VPCs and on‑premises networks but are not designed to accelerate public client traffic across the AWS global network.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 59Incorrect  
A developer who has no AWS Cloud experience wants to use AWS technology to build a web application. Which AWS service should the developer use to start building the application?  
**Votre réponse est incorrecte**  
A. Amazon SageMaker

#### Explications

Incorrect. This service is a managed machine learning platform (not a general web-hosting solution). It provides notebooks, model training, and hosting endpoints for ML workloads, so it is not the appropriate, beginner-oriented choice for building a standard web application.  
B. AWS Lambda

#### Explications

Incorrect. This is a serverless function service suited to running event-driven code and back-end logic (often paired with API Gateway). It requires understanding of function packaging, invocation patterns, IAM, and limits (execution time, ephemeral storage), making it less straightforward as a single first step for a developer with no cloud experience.  
**Bonne réponse**  
C. Amazon Lightsail

#### Explications

Correct. This offering is purpose-built for users new to AWS: it provides simplified virtual private server instances, one‑click application blueprints (WordPress, LAMP, Node.js, etc.), easy static IP and DNS setup, optional managed databases, and predictable flat-rate pricing. It abstracts lower-level services (EC2, VPC, storage, DNS) so a beginner can deploy a working web app quickly without learning complex AWS infrastructure details.  
D. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Incorrect. This is a container orchestration service for running Docker containers at scale. Using it effectively requires knowledge of containers, task definitions, clusters, networking, and deployment strategies, which makes it more complex than the beginner-friendly option.  
Explication générale  
This question tests recognition of the most beginner-friendly AWS hosting option. The correct choice is the service that abstracts underlying infrastructure and provides preconfigured application stacks, simple networking and DNS, and predictable pricing so a novice can deploy a web app quickly. The other options are focused on specialized use cases (machine learning, serverless functions, container orchestration) that require more cloud knowledge and are therefore less suitable as the first starting point.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 60Correct  
A food delivery company needs to block users in certain countries from accessing its website. Which AWS service should the company use to meet this requirement?  
**Votre réponse est correcte**  
A. AWS WAF

#### Explications

AWS WAF is a web application firewall that can inspect HTTP/S requests and enforce Web ACL rules. It supports a GeoMatch condition that allows you to block or allow requests based on the requester's country. WAF rules can be applied to Amazon CloudFront distributions, Application Load Balancers, and API Gateway endpoints, making it the appropriate service to restrict website access from specific countries.  
B. AWS Control Tower

#### Explications

AWS Control Tower provides automated setup and governance for multi-account AWS environments (landing zones) and policy guardrails for accounts. It does not inspect or filter inbound web requests and therefore cannot be used to block user traffic by geographic location.  
C. Amazon Fraud Detector

#### Explications

Amazon Fraud Detector is a managed ML service for identifying potentially fraudulent activity in events (for example, online transactions). It evaluates event data and returns fraud predictions, but it is not a front-door request-filtering service and does not provide built-in geographic request blocking for website traffic.  
D. Amazon Pinpoint

#### Explications

Amazon Pinpoint is a customer engagement and messaging service used for targeted campaigns, analytics, and sending messages (email/SMS/push). It is not designed to filter or block inbound web traffic and does not offer geo-based request blocking for a website.  
Explication générale  
The requirement is to block users from certain countries at the web request level. AWS WAF is designed for that use case: it inspects HTTP/S traffic and can enforce Web ACLs with GeoMatch conditions, and it integrates with CloudFront, ALB, and API Gateway. The other options (Control Tower, Fraud Detector, Pinpoint) provide governance, fraud-scoring, and messaging capabilities respectively and do not perform geo-based web request filtering.  
Domaine  
Domain 2: Security and Compliance  
Question 61Correct  
How does AWS Cloud computing help businesses reduce costs? (Choose two.)  
A. AWS charges the same prices for services in every AWS Region.

#### Explications

AWS pricing is published on a per-region basis and can differ because of factors like local infrastructure costs, taxes, and market conditions. Assuming uniform pricing across regions is inaccurate and not a mechanism for lowering costs.  
**Votre sélection est correcte**  
B. AWS enables capacity to be adjusted on demand.

#### Explications

AWS provides elasticity and a pay-as-you-go model (examples: Auto Scaling, on‑demand instances, and serverless services) so capacity can be increased or decreased to match demand. This alignment of resources to actual use prevents over‑provisioning and reduces wasted spend.  
C. AWS offers discounts for Amazon EC2 instances that remain idle for more than 1 week.

#### Explications

AWS does not grant discounts based on an instance being idle. Cost reductions are achieved through commitment-based pricing (Reserved Instances, Savings Plans), Spot Instances for spare capacity, or by stopping/terminating unused resources—not by idle-time discounts.  
D. AWS does not charge for data sent from the AWS Cloud to the internet.

#### Explications

Data ingress is typically free, but egress (data transfer out to the internet) is generally billed and can be a material cost. Reducing egress costs requires architectural choices (e.g., caching, CloudFront, Direct Connect), so free outbound transfer is not a reliable cost-saving guarantee.  
**Votre sélection est correcte**  
E. AWS eliminates many of the costs of building and maintaining on-premises data centers.

#### Explications

Moving to AWS converts many capital expenditures (servers, racks, physical facilities, power, and hands‑on maintenance) into managed, operational expenses. This reduces upfront investment, lowers maintenance overhead, and leverages AWS economies of scale to reduce total cost.  
Explication générale  
The primary AWS cost advantages are elasticity (scale resources up/down to pay only for what you use) and the elimination of on‑premises capital and operational costs through managed services. Other statements in the distractors are incorrect because regional pricing varies, AWS does not offer idle‑time discounts, and outbound internet data transfer is typically charged.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 62Correct  
A company wants to build graph queries for real-time fraud pattern detection. Which AWS service will meet this requirement?  
**Votre réponse est correcte**  
A. Amazon Neptune

#### Explications

Neptune is a purpose-built, fully managed graph database that supports both property graph (Apache TinkerPop Gremlin) and RDF (SPARQL) models. It is optimized for low-latency, multi-hop traversals and complex relationship queries, which are core requirements for real-time fraud pattern detection. Neptune also provides high availability, read replicas, and security integrations suitable for production graph workloads.  
B. Amazon DynamoDB

#### Explications

DynamoDB is a high-performance NoSQL key-value and document store designed for predictable single-digit millisecond lookups at scale. It does not provide native graph traversal/query languages, so implementing multi-hop relationship analysis requires complex data modeling, denormalization, or additional compute (e.g., Lambda), making it inefficient for real-time graph queries.  
C. Amazon Timestream

#### Explications

Timestream is a time-series database optimized for storing, querying, and downsampling time-stamped metrics and events. Its query primitives focus on time-series aggregation and interpolation rather than relationship traversals, so it is not suitable for graph-based pattern detection.  
D. Amazon Forecast

#### Explications

Forecast is a managed machine-learning service for producing time-series forecasts. It is designed to predict future values from historical time-series data, not to store or perform graph traversals or relationship analysis required for fraud pattern detection.  
Explication générale  
Real-time fraud detection that relies on identifying patterns across connected entities requires efficient graph traversals and relationship-aware queries. Neptune provides native graph engines (Gremlin and SPARQL) and optimizations for multi-hop queries, making it the appropriate choice. The other services are optimized for different workloads—key-value/document lookups, time-series analytics, or forecasting—and do not offer native graph query capabilities.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 63Correct  
Which AWS service can be used to retrieve compliance reports on demand?  
A. AWS Secrets Manager

#### Explications

Secrets Manager is a secrets management service used to securely store, manage, and rotate credentials and API keys. It does not provide audit-ready compliance or certification reports for regulators or auditors.  
**Votre réponse est correcte**  
B. AWS Artifact

#### Explications

Artifact is the centralized AWS portal for downloading AWS compliance reports and security and compliance documentation (for example, SOC, ISO, and PCI reports) and for accessing customer-specific agreements. It is the service designed to deliver on-demand compliance artifacts to customers and auditors.  
C. AWS Security Hub

#### Explications

Security Hub aggregates and normalizes security findings from multiple AWS services and third-party tools and evaluates resources against security standards and best practices. It provides posture and findings, not the official downloadable compliance certification reports required for audits.  
D. AWS Certificate Manager

#### Explications

Certificate Manager issues and manages SSL/TLS certificates and automates renewals for AWS resources. It is focused on cryptographic certificate lifecycle management, not on producing compliance or audit reports.  
Explication générale  
AWS Artifact is the correct service because it provides on-demand access to AWS compliance reports and contractual agreements that customers and auditors use for regulatory verification (SOC, ISO, PCI, etc.). The other services listed address different needs: Secrets Manager handles credentials, Security Hub consolidates security findings and posture checks (not official audit reports), and Certificate Manager handles TLS certificates.  
Domaine  
Domain 2: Security and Compliance  
Question 64Correct  
Which of the following are pillars of the AWS Well-Architected Framework? (Choose two.)  
A. Resource scalability

#### Explications

Incorrect — Scalability is an important design goal in cloud architectures but it is not listed as one of the six AWS Well-Architected pillars. The concept of scaling resources is addressed within other pillars (notably Performance Efficiency and Reliability) rather than being a standalone pillar.  
**Votre sélection est correcte**  
B. Performance efficiency

#### Explications

Correct — This pillar concerns selecting the right resource types and sizes, monitoring performance, and adapting infrastructure to meet changing demands. It covers practices such as right‑sizing, using managed services and serverless architectures, caching and CDN use, benchmarking, and telemetry (for example, Amazon CloudWatch) to maintain efficient performance.  
C. System elasticity

#### Explications

Incorrect — Elasticity (automatic adjustment of capacity) is a design capability that supports cloud architectures, but it is not one of the named Well‑Architected pillars. Elasticity is a behavior typically implemented under Performance Efficiency and Reliability using features like Auto Scaling and AWS Lambda.  
D. Agile development

#### Explications

Incorrect — Agile development is a software delivery methodology and organizational practice. The Well‑Architected Framework includes Operational Excellence to address processes and continual improvement, but ‘agile development’ itself is not a pillar.  
**Votre sélection est correcte**  
E. Operational excellence

#### Explications

Correct — This pillar focuses on running and monitoring systems to deliver business value and continually improve processes. It emphasizes operational procedures, change and incident management, automation, CI/CD and infrastructure as code (for example, AWS CloudFormation, CI/CD pipelines, runbooks and monitoring with CloudWatch) to improve and automate operations.  
Explication générale  
The AWS Well‑Architected Framework defines six pillars (Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization and Sustainability). The best answers are the pillars that appear in that list: Performance Efficiency and Operational Excellence. The other options describe desirable practices or behaviors (scalability, elasticity, agile) but are not named pillars.  
Domaine  
Domain 1: Cloud Concepts  
Question 65Correct  
A company plans to perform a one-time migration of a large dataset with millions of files from its on-premises data center to the AWS Cloud. Which AWS service should the company use for the migration?  
A. AWS Database Migration Service (AWS DMS)

#### Explications

Incorrect. AWS Database Migration Service is specialized for migrating and replicating relational and NoSQL databases (schema conversion, continuous change-data-capture, homogeneous and heterogeneous DB engines). It does not operate on file shares (NFS/SMB) and is not intended for bulk file-based transfers of millions of files.  
**Votre réponse est correcte**  
B. AWS DataSync

#### Explications

Correct. AWS DataSync is a managed service built for efficient, secure file-based transfers between on-premises storage and AWS (supports NFS and SMB to S3/EFS/FSx). It uses an on‑premises agent, parallelizes data movement, performs integrity verification, and supports encryption in transit—making it well suited for one-time migrations of large numbers of files.  
C. AWS Migration Hub

#### Explications

Incorrect. AWS Migration Hub provides visibility and tracking for migration projects across multiple AWS migration tools; it does not perform data movement itself and therefore cannot be used to transfer large datasets.  
D. AWS Application Migration Service

#### Explications

Incorrect. AWS Application Migration Service (MGN) focuses on lift-and-shift server migrations by replicating whole server instances (block-level replication of OS and applications). It is not designed as a file-transfer service for migrating large collections of standalone files.  
Explication générale  
This question tests knowledge of AWS services for data transfer. For migrating large numbers of files from on‑premises storage to AWS, DataSync is the appropriate service because it is purpose-built for file-based transfers (NFS/SMB to S3/EFS/FSx), optimizes throughput with parallelism, and verifies data integrity. The other options are focused on databases (DMS), migration tracking (Migration Hub), or server/instance lift-and-shift (Application Migration Service), so they are not the best fit. For extremely large datasets where network transfer is impractical, physical appliance options (AWS Snowball) can be considered as an alternative.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 66Incorrect  
A global company wants to migrate its third-party applications to the AWS Cloud. The company wants help from a global team of experts to complete the migration faster and more reliably in accordance with AWS internal best practices. Which AWS service or resource will meet these requirements?  
A. AWS Support

#### Explications

This is a paid support offering with tiered plans (Basic, Developer, Business, Enterprise) that provides technical guidance, account-level recommendations, and tools such as Trusted Advisor and, for Enterprise, a Technical Account Manager. It is advisory and reactive—helpful for troubleshooting and best-practice guidance—but it does not function as a hands-on, project-focused migration delivery team that executes migrations on the customer’s behalf.  
**Bonne réponse**  
B. AWS Professional Services

#### Explications

An internal, global professional services organization that performs hands-on migration engagements: assessment, target-state architecture, migration execution, runbook and automation development, and knowledge transfer. They follow the AWS Well-Architected Framework and programs such as the Migration Acceleration Program (MAP), and they coordinate with APN partners when needed—making them the appropriate choice for fast, reliable migrations aligned with AWS best practices.  
C. AWS Launch Wizard

#### Explications

A guided deployment tool that walks users through sizing and provisioning for specific supported application patterns by generating CloudFormation templates and recommended configurations. It automates deployments for certain workloads but is not a dedicated migration delivery team and does not provide the global, hands-on expert project services required for complex third‑party application migrations.  
**Votre réponse est incorrecte**  
D. AWS Managed Services (AMS)

#### Explications

A service that provides ongoing operational management, governance, incident response, patching, and security operations for AWS environments. It is focused on run‑time operations and long‑term management of workloads rather than on delivering the initial migration project or acting as a global migration services team.  
Explication générale  
The requirement is for a global, hands‑on team that can plan and execute third‑party application migrations according to AWS internal best practices. The AWS Professional Services organization is built to deliver those migration engagements (assess, design, execute, and transfer knowledge) and leverages programs like MAP and the Well‑Architected Framework. The other options provide valuable capabilities—technical support and tooling or ongoing managed operations—but they are advisory, deployment helpers, or operations‑focused rather than project migration delivery teams.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 67Incorrect  
A company has teams that have different job roles and responsibilities. The company’s employees often change teams. The company needs to manage permissions for the employees so that the permissions are appropriate for the job responsibilities. Which IAM resource should the company use to meet this requirement with the LEAST operational overhead?  
**Bonne réponse**  
A. IAM user groups

#### Explications

Attaching IAM policies to groups centralizes permission management so that membership changes (adding/removing a user from a group) immediately change the user's effective permissions without editing policies or user credentials. This approach scales for many users, is auditable, and minimizes operational work when employees move between teams.  
**Votre réponse est incorrecte**  
B. IAM roles

#### Explications

IAM roles provide temporary security credentials for delegation, cross-account access, or service identities (users/services call STS AssumeRole). They are not intended as the primary mechanism for persistent, membership-based permissions for human users and introduce extra steps to assume the role, increasing operational complexity for routine team changes.  
C. IAM instance profiles

#### Explications

An instance profile is a container that associates an IAM role with an EC2 instance so applications on that instance can access AWS APIs. Instance profiles are for compute resources, not for granting human users permissions when changing teams.  
D. IAM policies for individual users

#### Explications

Attaching policies directly to individual users is supported but does not scale: every team change requires editing user-specific permissions, increasing administrative overhead, risk of inconsistent access, and difficulty in auditing compared to group-based policy management.  
Explication générale  
This item tests IAM identity-management best practices. Using IAM groups lets administrators manage permissions centrally (policies attached to groups) so moving users between teams is just a change of group membership, minimizing operational overhead. Roles and instance profiles serve different purposes (temporary credentials, cross-account access, or granting permissions to EC2), and per-user policies scale poorly for organizations with frequent team changes.  
Domaine  
Domain 2: Security and Compliance  
Question 68Incorrect  
A company needs a bridge between technology and business to help evolve to a culture of continuous growth and learning. Which perspective in the AWS Cloud Adoption Framework (AWS CAF) serves as this bridge?  
**Bonne réponse**  
A. People

#### Explications

Addresses organizational change management, skills and role definition, leadership alignment, training and workforce enablement—activities that connect business strategy with technology adoption and cultivate continuous learning and capability growth across the organization.  
B. Governance

#### Explications

Focuses on decision-making frameworks, policies, compliance, risk and accountabilities (e.g., control objectives and governance models). Important for alignment and risk management but not primarily responsible for workforce development or cultural transformation.  
**Votre réponse est incorrecte**  
C. Operations

#### Explications

Covers runbook procedures, operational processes, incident and service management, and automation to operate cloud environments. It improves operational excellence but does not drive organizational culture or people development.  
D. Security

#### Explications

Concerns confidentiality, integrity and availability through identity and access management, threat detection, encryption and compliance controls. Critical for risk mitigation, but it does not serve as the primary bridge between business strategy and workforce transformation.  
Explication générale  
The AWS CAF People perspective is centered on organizational change, skills, roles and leadership—making it the primary mechanism to bridge technology and business and to build a culture of continuous growth and learning. Other CAF perspectives (Governance, Operations, Security) address decision rights, run-time operations, and risk controls respectively, and while complementary, they do not primarily focus on workforce enablement and cultural transformation.  
Domaine  
Domain 1: Cloud Concepts  
Question 69Incorrect  
Which of the following best describes the benefit of using AWS Cloud for a business migration? (Choose two.)  
**Sélection correcte**  
A. It reduces capital expenses by enabling pay-as-you-go pricing models.

#### Explications

Moving to AWS shifts costs from capital expenditure (CAPEX) to operating expenditure (OPEX). AWS’s on‑demand and flexible pricing models let organizations provision compute, storage, and networking without large upfront hardware purchases, paying for resources as they are consumed — a primary financial benefit when migrating to the cloud.  
B. It guarantees 100% uptime for all applications without the need for additional configurations.

#### Explications

Incorrect. AWS fournit des composants et des bonnes pratiques pour la haute disponibilité (déploiements multi-AZ, équilibrage de charge, Auto Scaling) et publie des SLA de service, mais ne garantit pas une disponibilité à 100 %. Pour atteindre une haute disponibilité, il est nécessaire que les clients conçoivent des architectures résilientes et appliquent les configurations appropriées.  
C. Grâce aux fonctionnalités de sécurité intégrées d'AWS, il n'est plus nécessaire de prendre des mesures de sécurité.

#### Explications

Incorrect. La sécurité sur AWS repose sur le modèle de responsabilité partagée : AWS gère la sécurité du cloud (matériel, hyperviseur, réseau), tandis que les clients sont responsables de la sécurité dans le cloud (mises à jour du système d'exploitation, gestion des identités et des accès, protection des données, configuration des groupes de sécurité, chiffrement). La migration ne dispense pas de la mise en œuvre de mesures de sécurité.  
**Votre sélection est incorrecte**  
D. Il simplifie la migration en fournissant un outil unique qui automatise tous les aspects du processus de migration.

#### Explications

Incorrect. AWS propose une suite d'outils et de services de migration (Migration Hub, Application Migration Service, Database Migration Service, Snow Family, etc.) pour faciliter différentes tâches de migration, mais aucun outil n'automatise entièrement tous les aspects. Une migration réussie nécessite une planification, des tests et souvent le recours à plusieurs services.  
**Votre sélection est correcte**  
E. Elle permet aux organisations de faire évoluer leur infrastructure de manière dynamique, soutenant ainsi la croissance sans investissements initiaux.

#### Explications

AWS offre élasticité et évolutivité grâce à des services tels que Auto Scaling, Elastic Load Balancing, les plateformes sans serveur (Lambda) et les bases de données gérées (RDS, DynamoDB). Ces fonctionnalités permettent aux entreprises d'ajuster dynamiquement leur capacité en fonction de la demande, favorisant ainsi leur croissance sans investissements initiaux importants dans l'infrastructure.  
Explication générale  
Cette question évalue les principaux avantages du cloud en matière de migration. Ces avantages sont économiques (réduction des dépenses d'investissement initiales grâce au paiement à l'usage) et opérationnels (évolutivité dynamique pour accompagner la croissance). Il s'agit de concepts fondamentaux du cloud ; les autres options surestiment les capacités d'AWS (disponibilité à 100 %), ignorent la responsabilité partagée en matière de sécurité ou laissent entendre, à tort, l'existence d'un outil de migration unique et complet.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 70Incorrect  
Une entreprise doit exécuter une application sur des instances Amazon EC2 sans interruption. Quelle option d'achat d'instances EC2 répond le mieux à cette exigence en termes de coût ?  
**Bonne réponse**  
A. Instances réservées standard

#### Explications

Pour les charges de travail continues et stables, un engagement sur une période de facturation de 1 ou 3 ans offre la plus forte réduction horaire par rapport à la facturation à la demande et constitue donc l'option la plus rentable pour un fonctionnement continu. Les réservations zonales permettent également de réserver de la capacité dans une zone de disponibilité spécifique afin de garantir le lancement des instances en cas de besoin.  
B. Instances réservées convertibles

#### Explications

Cette option permet d'effectuer des échanges entre familles d'instances, types de systèmes d'exploitation et locations afin d'offrir une flexibilité pendant la durée du contrat. Cette flexibilité s'accompagne généralement d'une réduction des coûts, ce qui la rend moins avantageuse qu'un engagement à long terme fixe pour une charge de travail garantie et ininterrompue.  
**Votre réponse est incorrecte**  
C. Instances à la demande

#### Explications

No long‑term commitment is required and instances can run continuously, but On‑Demand per‑hour pricing is higher than reserved options for sustained use, making it a more expensive choice for workloads that must run without interruption.  
D. Spot Instances

#### Explications

Offered at steep discounts but subject to termination when AWS reclaims capacity (with a short warning), this purchasing model is inherently interruptible and therefore unsuitable for applications that require uninterrupted operation.  
Explication générale  
The key concept is selecting a purchasing option that minimizes cost for a long‑running, always‑on EC2 workload. A long‑term reserved billing commitment delivers the largest sustained discount (and can include zonal capacity reservation), making it the best fit for uninterrupted, cost‑effective operation. Alternatives either cost more over time (On‑Demand), trade maximum savings for flexibility (Convertible), or are interruptible (Spot).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 71Incorrect  
A company wants to migrate its on-premises SQL Server database to the AWS Cloud. The company wants AWS to handle the day-to-day administration of the database. Which AWS service will meet the company's requirements?  
A. Amazon EC2 for Microsoft SQL Server

#### Explications

Incorrect — Deploying SQL Server on Amazon EC2 is an IaaS approach: you (the customer) must manage the operating system and the database instance, including installation, OS and DB patching, backups, recovery, and HA configuration. It does not offload day-to-day database administration to AWS.  
**Votre réponse est incorrecte**  
B. Amazon DynamoDB

#### Explications

Incorrect — Amazon DynamoDB is a fully managed NoSQL key-value and document database. It is not compatible with Microsoft SQL Server or T-SQL and does not provide relational features (joins, native relational transactions) required for a straightforward SQL Server migration without application redesign.  
**Bonne réponse**  
C. Amazon RDS

#### Explications

Correct — Amazon RDS for SQL Server is a managed relational database service that automates routine DBA tasks (automated backups and snapshots, automated patching, monitoring, point-in-time recovery) and offers features like Multi-AZ for high availability. These managed operations allow AWS to handle day-to-day administration while you focus on the database schema and data.  
D. Amazon Aurora

#### Explications

Incorrect — Amazon Aurora is a managed relational engine compatible with MySQL and PostgreSQL. It does not support Microsoft SQL Server compatibility, so it cannot host a native SQL Server database for a lift-and-shift migration.  
Explication générale  
The question tests knowledge of AWS managed database options for migrating an on-premises Microsoft SQL Server when the customer wants AWS to handle routine administration. The appropriate choice is the managed relational option that supports SQL Server (RDS for SQL Server), because it automates backups, patching, monitoring, and offers managed HA. The other choices either require customer-managed administration (EC2), are incompatible engines (Aurora), or are a different database model (DynamoDB).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 72Correct  
A company wants to quickly implement a continuous integration/continuous delivery (CI/CD) pipeline. Which AWS service will meet this requirement?  
A. AWS Config

#### Explications

Incorrect — AWS Config provides continuous monitoring of resource configurations, change history, and compliance evaluation (rules and conformance packs). It is an auditing and governance service, not a tool for source control, automated builds, tests, or deployments required by CI/CD pipelines.  
B. Amazon Cognito

#### Explications

Incorrect — Amazon Cognito handles user authentication, authorization, and identity federation (user pools and identity pools) for applications. It is an identity management service and does not provide CI/CD pipeline capabilities like build or deployment orchestration.  
C. AWS DataSync

#### Explications

Incorrect — AWS DataSync is a managed data-transfer service for moving files and objects between on-premises storage and AWS or between AWS storage services. It addresses data migration and replication, not software build/test/deploy automation.  
**Votre réponse est correcte**  
D. AWS CodeStar

#### Explications

Correct — CodeStar provides preconfigured project templates, a unified project dashboard, and built-in integrations with developer tools (such as CodeCommit, CodeBuild, CodePipeline, CodeDeploy, and CloudFormation) to provision an end-to-end CI/CD toolchain rapidly, minimizing setup effort.  
Explication générale  
The question assesses knowledge of AWS developer tools for implementing CI/CD. CodeStar is the best fit because it accelerates project and pipeline setup by provisioning an integrated toolchain and templates; the other options focus on configuration auditing (Config), identity management (Cognito), or data transfer (DataSync), and therefore do not meet the requirement for quickly implementing a CI/CD pipeline.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 73Correct  
A company needs to run a pre-installed third-party firewall on an Amazon EC2 instance. Which AWS service or feature can provide this solution?  
A. Network ACLs

#### Explications

Network ACLs are stateless, subnet-level access control lists that allow or deny IP traffic based on rules. They are network controls, not deployable software or virtual appliances, so they cannot provide a pre-installed third-party firewall on an EC2 instance.  
B. Security groups

#### Explications

Security groups are stateful, instance-level virtual firewalls that control inbound and outbound traffic by protocol, port, and source/destination. They are configuration-based controls managed by AWS and do not provide installable third-party firewall software or vendor-supplied appliance images.  
**Votre réponse est correcte**  
C. AWS Marketplace

#### Explications

AWS Marketplace provides vendor-supplied Amazon Machine Images (AMIs) and virtual appliance listings that come pre-configured with third-party firewall software. Customers can subscribe to a Marketplace listing and launch the vendor AMI as an EC2 instance (including supported licensing options such as hourly billing or BYOL), giving a ready-to-run third-party firewall.  
D. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor is a best-practices recommendation service that inspects your AWS resources for cost optimization, security, performance, and fault tolerance. It offers guidance and checks but does not supply software images or deployable firewall appliances.  
Explication générale  
To run a pre-installed third-party firewall on EC2 you need a vendor-supplied AMI or virtual appliance that contains the firewall software. AWS Marketplace is the appropriate source for such pre-configured images and licensing options. Network ACLs and security groups are AWS-managed network controls (stateless and stateful respectively) and are not installable software, while Trusted Advisor only provides recommendations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 74Correct  
Which cloud concept is demonstrated by using AWS Cost Explorer?  
**Votre réponse est correcte**  
A. Rightsizing

#### Explications

AWS Cost Explorer provides cost and usage visibility and includes built-in recommendations that analyze historical usage to identify underutilized compute and database resources and recommend downsizing or termination. These recommendations enable optimization of instance sizes and counts and help reduce spend by aligning capacity with actual demand (e.g., advising instance family/size changes and identifying candidates for Savings Plans or Reserved Instances).  
B. Reliability

#### Explications

This option describes system availability and fault-tolerance (designs that reduce outages and recover from failures). Those concerns are addressed by architecture choices and services such as Auto Scaling, Elastic Load Balancing, multi‑AZ deployments, and health checks; Cost Explorer focuses on cost/usage analysis rather than improving availability.  
C. Resilience

#### Explications

This option refers to the ability of an application to absorb and recover from failures (design patterns like multi‑AZ/multi‑Region, backups, and disaster recovery). Cost Explorer does not assess or implement these architectural resiliency measures; it only reports and analyzes cost and usage data.  
D. Modernization

#### Explications

This option concerns migrating or refactoring applications to newer architectures (for example, using AWS Migration Hub, Application Migration Service, or moving to serverless/container platforms). Cost Explorer can inform cost implications of modernization but does not perform migration or modernization activities itself.  
Explication générale  
AWS Cost Explorer is a cost-management tool that analyzes historical AWS cost and usage and provides actionable recommendations to right‑size resources (identify underutilized instances and suggest downsizing or termination). The correct concept tested is cost-driven resource optimization. The other options describe availability, architectural resilience, and application modernization—important cloud concepts but not what Cost Explorer directly implements.  
Domaine  
Domain 1: Cloud Concepts  
Question 75Correct  
A company needs an event history of which AWS resources the company has created. Which AWS service will provide this information?  
A. Amazon CloudWatch

#### Explications

CloudWatch provides metrics, logs, alarms and operational telemetry for resources and applications. It is focused on performance and operational monitoring and does not serve as the authoritative audit trail of AWS management API calls that show who created or changed resources.  
**Votre réponse est correcte**  
B. AWS CloudTrail

#### Explications

CloudTrail records AWS API activity and management/data events across accounts and services, delivers logs to S3/CloudWatch Logs/EventBridge, and exposes an Event history in the console (short-term) and configurable trails for long-term retention and auditing—making it the correct service for resource creation history.  
C. Amazon Aurora

#### Explications

Aurora is a managed relational database service for storing application data. It does not provide cross-service API logging or an audit history of AWS resource lifecycle events.  
D. Amazon EventBridge

#### Explications

EventBridge is an event bus and routing service for near-real-time integration and event-driven architectures. It routes events but is not the primary source of audited API call history; CloudTrail produces the API audit events that can be forwarded to EventBridge if needed.  
Explication générale  
This question tests auditing and governance knowledge. AWS CloudTrail is the service designed to capture, store, and provide searchable records of API calls and resource lifecycle events, which is required to obtain an event history of created resources. Other services mentioned (CloudWatch, EventBridge, Aurora) serve monitoring, event routing, and database roles and do not replace CloudTrail's API-level audit capabilities.  
Domaine  
Domain 2: Security and Compliance  
Question 76Incorrect  
A company needs to manage multiple logins across AWS accounts within the same organization in AWS Organizations. Which AWS service should the company use to meet this requirement?  
A. Amazon VPC

#### Explications

Amazon VPC provides logically isolated virtual networks for AWS resources (subnets, route tables, security groups, etc.). It is a networking construct and does not provide identity, authentication, or centralized access management across AWS accounts.  
B. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat detection service that analyzes AWS CloudTrail, VPC Flow Logs, and DNS logs to identify suspicious activity. It focuses on threat detection and monitoring, not on user authentication or single sign-on across accounts.  
**Votre réponse est incorrecte**  
C. Amazon Cognito

#### Explications

Amazon Cognito manages authentication and user pools for web and mobile applications (including federated sign-in and identity pools for AWS credentials). It is designed for application-level user identities, not for centrally managing AWS account access or SSO across multiple AWS accounts in an organization.  
**Bonne réponse**  
D. AWS IAM Identity Center

#### Explications

AWS IAM Identity Center (formerly AWS Single Sign-On) provides centralized user and permissions management across multiple AWS accounts. It integrates with AWS Organizations, uses permission sets to provision IAM roles in member accounts, supports SAML/OIDC identity providers and SCIM provisioning, and enables single sign-on to the AWS Management Console and supported applications — making it the correct service for managing multiple logins across accounts.  
Explication générale  
The question tests centralized identity and access management across AWS accounts. AWS IAM Identity Center is the appropriate service because it integrates with AWS Organizations to provide SSO, permission sets that map to IAM roles in member accounts, and support for external identity providers. The other options are unrelated: VPC is networking, GuardDuty is threat detection, and Cognito is for application user identities rather than account-level access across AWS accounts.  
Domaine  
Domain 2: Security and Compliance  
Question 77Correct  
A company is planning to migrate to the AWS Cloud. The company is conducting organizational transformation and wants to become more responsive to customer inquiries and feedback. Which task should the company perform to meet these requirements, according to the AWS Cloud Adoption Framework (AWS CAF)?  
**Votre réponse est correcte**  
A. Realign teams to focus on products and value streams.

#### Explications

This option reflects the AWS Cloud Adoption Framework’s People perspective: reorganizing staff into cross-functional, product-focused teams that own end-to-end value streams reduces handoffs, shortens feedback loops, and creates clear ownership and accountability. Those organizational changes enable faster response to customer inquiries and continuous improvement through DevOps and agile practices.  
B. Create new value propositions with new products and services.

#### Explications

Creating new value propositions is a business-level initiative (aligning with the Business perspective) that affects what the company offers, but it does not by itself change team structure, ownership, or day-to-day processes needed to improve responsiveness to customer feedback.  
C. Use a new data and analytics platform to create actionable insights.

#### Explications

Deploying a new data and analytics platform improves insights and decision-making, but it targets information capabilities rather than organizational design. Analytics can support better decisions, yet responsiveness requires organizational changes (roles, processes, team boundaries) emphasized by the People perspective.  
D. Migrate and modernize legacy infrastructure.

#### Explications

Migrating and modernizing legacy infrastructure improves scalability, reliability, and operational efficiency (Platform/Operations focus), but technical modernization alone does not reorganize people or processes to shorten feedback cycles or improve how teams handle customer inquiries.  
Explication générale  
The AWS CAF expects organizations to address people, processes, and organizational structure to become more responsive. The most direct action is reorganizing teams into cross-functional units that own product value streams—this creates ownership and faster feedback loops. Other options (new offerings, analytics platforms, or infrastructure modernization) are valuable but address business, data, or technical capabilities rather than the organizational changes required for faster customer responsiveness.  
Domaine  
Domain 1: Cloud Concepts  
Question 78Correct  
Which of the following best describes the benefit of using AWS Cloud services for a business looking to improve scalability and reduce infrastructure costs?  
A. AWS Cloud services require significant upfront investment in physical hardware.

#### Explications

Incorrect. AWS removes the need for customers to buy and maintain physical servers by offering on-demand compute, storage, and networking — converting capital expenditures into operational expenditures. Customers still manage in-cloud configuration and consumption, but they do not need the significant upfront hardware purchases implied here.  
**Votre réponse est correcte**  
B. AWS Cloud services allow businesses to scale their resources dynamically based on demand, which can reduce costs and improve performance.

#### Explications

Correct. AWS provides elasticity and on-demand provisioning (for example, Auto Scaling with EC2, AWS Lambda for serverless, and Elastic Load Balancing) combined with a pay-as-you-go pricing model and cost-optimization features (Savings Plans, Reserved Instances, right-sizing). Together these enable resources to scale with demand, improving performance while reducing wasted spend.  
C. Using AWS Cloud services guarantees enhanced security without any additional security measures required.

#### Explications

Incorrect. AWS operates under a shared responsibility model: AWS secures the underlying cloud infrastructure, but customers are responsible for securing their data and configurations in the cloud. AWS offers security services (IAM, KMS, Security Hub, etc.), yet customers must implement identity management, encryption, patching, and secure configurations.  
D. AWS Cloud services are only suitable for large enterprises with complex infrastructure needs.

#### Explications

Incorrect. AWS is designed to serve organizations of all sizes. Its pricing models and managed services (serverless, managed databases, pay-per-use compute) make it accessible to startups and small businesses as well as large enterprises; complexity is optional and can scale with organizational needs.  
Explication générale  
This question tests the core cloud concept of elasticity and cost efficiency. The correct choice highlights AWS capability to provision and scale resources dynamically and bill based on consumption, which reduces idle capacity and lowers infrastructure costs. The distractors confuse cloud economics (capital vs. operational costs), misstate security responsibilities (shared responsibility model), or incorrectly limit AWS applicability to only large enterprises.  
Domaine  
Domain 1: Cloud Concepts  
Question 79Incorrect  
Which of the following are benefits of migrating existing applications to the AWS Cloud? (Choose three)  
**Votre sélection est correcte**  
A. Lower capital expenditure with pay-as-you-go pricing

#### Explications

Shifts spending away from large upfront hardware purchases toward ongoing operational costs by paying only for compute, storage, and other services consumed; this reduces capital exposure and the need to provision for peak capacity.  
B. Increased management complexity due to cloud migration

#### Explications

This is not a benefit. While some migrations can introduce short-term operational complexity, AWS offers managed services, automation, and orchestration tools that typically simplify ongoing management rather than increase it permanently.  
**Sélection correcte**  
C. Enhanced scalability and flexibility of applications

#### Explications

Enables on-demand provisioning and elasticity so applications can scale up or down to match workload changes (examples: Auto Scaling, Elastic Load Balancing, serverless services), improving responsiveness and resource efficiency.  
D. Reduced security and compliance controls

#### Explications

Incorrect as stated. AWS provides numerous security, identity, and compliance features and customers can use these to maintain or strengthen controls; migration does not inherently reduce security under the shared responsibility model.  
**Votre sélection est correcte**  
E. Faster deployment of new features and capabilities

#### Explications

Cloud-native services, automation, and developer tooling (for example CI/CD, Infrastructure as Code, managed platforms and serverless) reduce provisioning and release cycles, enabling faster time-to-market for new features.  
Explication générale  
Key benefits of migrating to AWS include converting large capital expenditures into pay-for-what-you-use operational costs, gaining elastic scalability to handle variable demand, and accelerating feature delivery through managed services and automation. The distractors are incorrect because increased management complexity and reduced security are not inherent benefits of migration; in fact, AWS provides tools to simplify operations and support strong security and compliance.  
Domaine  
Domain 1: Cloud Concepts  
Question 80Correct  
A cloud practitioner needs to obtain AWS compliance reports before migrating an environment to the AWS Cloud. How can these reports be generated?  
A. Contact the AWS Compliance team.

#### Explications

Standard AWS compliance and audit reports are provided through a self-service portal; reaching out to AWS account or compliance contacts is reserved for specific legal or account-level inquiries and is not the normal method to obtain the standard audit documents.  
**Votre réponse est correcte**  
B. Download the reports from AWS Artifact.

#### Explications

AWS Artifact is the AWS Management Console service that delivers on-demand access to AWS compliance and audit documents (for example, SOC, ISO, PCI DSS, and related certifications and attestations) and certain AWS agreements. Customers can retrieve and download these reports directly from Artifact without needing to file support requests.  
C. Open a case with AWS Support.

#### Explications

AWS Support can assist with account or access issues but is not the primary channel for retrieving published compliance reports. The reports are published for self-service access in AWS Artifact; Support would be used only if there is a problem accessing those reports or for account-specific assistance.  
D. Generate the reports with Amazon Macie.

#### Explications

Amazon Macie is a data security service that discovers, classifies, and helps protect sensitive data in AWS. It does not produce AWS-wide compliance or audit reports (such as SOC/ISO/PCI reports) for customers.  
Explication générale  
AWS Artifact is the official, self-service portal in the AWS Management Console for obtaining AWS compliance and audit reports (SOC, ISO, PCI, etc.) and certain agreements. Other routes—contacting AWS compliance staff or opening a support case—are for special or account-specific needs and are not the routine method; Amazon Macie is unrelated, as it focuses on data discovery and protection rather than providing AWS compliance audit documents.  
Domaine  
Domain 2: Security and Compliance  
Question 81Correct  
Which Amazon EC2 instance pricing model can provide discounts of up to 90%?  
A. Reserved Instances

#### Explications

Incorrect. Reserved Instances (RIs) provide lower hourly rates in exchange for a 1‑ or 3‑year commitment and can offer substantial savings (commonly up to  
B. On-Demand

#### Explications

Incorrect. On‑Demand instances are billed at published rates with no long‑term commitment and therefore do not provide large percentage discounts; they represent the baseline (no‑discount) pricing model.  
C. Dedicated Hosts

#### Explications

Incorrect. Dedicated Hosts provide physical server isolation for compliance or licensing requirements by allocating entire EC2 servers to a single account. They are not intended to produce very large discounts and are typically not cheaper than other instance purchasing options.  
**Votre réponse est correcte**  
D. Spot Instances

#### Explications

Correct. Spot Instances run on unused EC2 capacity and can offer very deep discounts (commonly up to  
Explication générale  
Spot Instances yield the largest cost reductions by leveraging spare EC2 capacity and are therefore the only option among the choices that can approach discounts of up to 90%. Reserved Instances offer meaningful but smaller discounts through long‑term commitments; On‑Demand provides no discount; Dedicated Hosts provide physical isolation for compliance rather than deep cost savings. For highly flexible, interruptible workloads, Spot is the appropriate choice.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 82Correct  
Which AWS service is designed to help users handle large amounts of data in a data warehouse environment?  
A. Amazon RDS

#### Explications

Incorrect. Amazon RDS is a managed relational database service optimized for transactional (OLTP) workloads. It uses row-based storage and does not provide the massively parallel processing (MPP), columnar storage, or built-in analytic optimizations required for petabyte-scale data warehousing and complex analytical queries.  
B. Amazon DynamoDB

#### Explications

Incorrect. Amazon DynamoDB is a fully managed NoSQL key-value and document database built for low-latency, high-throughput transactional access. It is not designed for OLAP-style analytics or complex, large-scale data warehouse queries (although data can be exported from DynamoDB for analytics elsewhere).  
**Votre réponse est correcte**  
C. Amazon Redshift

#### Explications

Correct. Amazon Redshift is a fully managed, petabyte-scale data warehouse service that uses columnar storage, data compression, and a massively parallel processing (MPP) architecture to accelerate complex analytical queries. It also integrates with Redshift Spectrum and other AWS analytics services to query data in S3 and support large-scale analytics workloads.  
D. Amazon Aurora

#### Explications

Incorrect. Amazon Aurora is a high-performance, MySQL- and PostgreSQL-compatible relational database engine intended for transactional applications. While fast for OLTP use cases and scalable for read replicas, it lacks the MPP columnar architecture and analytic optimizations of a purpose-built data warehouse.  
Explication générale  
This question tests recognition of the AWS service purpose-built for data warehousing. Amazon Redshift is designed for OLAP workloads using columnar storage and MPP to handle very large datasets and complex analytical queries. The other choices are transactional or NoSQL databases (RDS and Aurora for OLTP; DynamoDB for low-latency NoSQL) and therefore are not the optimal managed service for large-scale data warehouse analytics.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 83Correct  
Which action should a company take to improve security in its AWS account?  
**Votre réponse est correcte**  
A. Require multi-factor authentication (MFA) for privileged users.

#### Explications

Enabling MFA forces a second authentication factor (for example, a time-based one-time password from a virtual or hardware MFA device) in addition to a password. AWS IAM best practices call for MFA on the root account and on privileged IAM principals. MFA mitigates the risk from compromised credentials and can be enforced via IAM policies or AWS Organizations controls, making it the most effective single action to raise account security.  
B. Remove the root user account.

#### Explications

The AWS account root user cannot be deleted. Best practice is to secure it (enable MFA on the root user, remove any root access keys, and use the root user only for a small set of account-level tasks) and instead create and use IAM principals with least privilege for daily operations.  
C. Create an access key for the AWS account root user.

#### Explications

Creating long-term access keys for the root user greatly increases risk because those credentials have full account privileges. AWS recommends deleting any root access keys, using IAM users or roles with least privilege, and using temporary credentials (AWS STS) for programmatic access instead.  
D. Create an access key for each privileged user.

#### Explications

Les clés d'accès fournissent des informations d'identification programmatiques et peuvent être nécessaires pour certaines charges de travail, mais l'attribution de clés permanentes à chaque utilisateur privilégié représente un risque. Il est préférable d'utiliser les rôles IAM, les informations d'identification STS temporaires, la rotation des clés et l'application du principe du moindre privilège et de l'authentification multifacteur (MFA). La simple création de clés n'améliore pas la sécurité en soi et peut même l'aggraver si elles ne sont pas gérées.  
Explication générale  
Cette question teste les bonnes pratiques de sécurité de base des comptes AWS. Exiger l'authentification multifacteur pour les utilisateurs privilégiés est la meilleure action immédiate, car elle ajoute un deuxième facteur qui réduit considérablement l'impact des mots de passe compromis et est recommandée par AWS pour le compte racine et les principaux IAM à privilèges élevés. Les autres options sont soit impossibles (suppression du compte racine), soit activement non sécurisées (création de clés d'accès racine), soit incomplètes (attribution de clés d'accès aux utilisateurs sans utilisation de rôles, d'informations d'identification temporaires, de rotation et d'authentification multifacteur).  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 84Correct  
Quel service AWS utilise une combinaison d'éditeurs et d'abonnés ?  
A. AWS Lambda

#### Explications

Incorrect — Lambda est le service de calcul sans serveur d'AWS qui exécute du code en réponse à des déclencheurs et peut servir de cible d'abonnement, mais ce n'est pas un service de messagerie de publication/abonnement géré qui fournit des sujets, une diffusion et une gestion des abonnements.  
**Votre réponse est correcte**  
B. Service de notification simple d'Amazon (Amazon SNS)

#### Explications

Exact — Amazon SNS est un service de messagerie de type publication/abonnement entièrement géré. Il utilise des sujets pour dissocier les éditeurs des abonnés, prend en charge plusieurs protocoles d'abonnement (par exemple : SQS, HTTP/S, Lambda, e-mail, SMS) et assure la diffusion par fan et le filtrage optionnel des messages — le comportement de publication/abonnement par excellence.  
C. Amazon CloudWatch

#### Explications

Incorrect — CloudWatch se concentre sur l'observabilité (métriques, journaux, alarmes) et le routage des événements ; bien que CloudWatch Events/EventBridge gère le routage piloté par les événements, il ne s'agit pas du service de messagerie de type publication/abonnement canonique basé sur les sujets, conçu pour une large diffusion vers de multiples points de terminaison d'abonnés.  
D. AWS CloudFormation

#### Explications

Incorrect — CloudFormation est un service d'infrastructure en tant que code permettant de provisionner et de gérer des ressources AWS via des modèles ; il ne fournit pas de fonctionnalités de messagerie ou de publication/abonnement.  
Explication générale  
La question porte sur la reconnaissance du système de messagerie de type publication/abonnement d'AWS. Amazon SNS implémente le modèle éditeur → sujet → abonné, permettant la diffusion des messages vers plusieurs points de terminaison et offrant la gestion et le filtrage des abonnements. Les autres options correspondent à différents types de services : calcul sans serveur (Lambda), surveillance/routage d'événements (CloudWatch/EventBridge) et provisionnement d'infrastructure (CloudFormation). Aucun de ces services n'est un service de messagerie de type publication/abonnement géré.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 85Correct  
Une entreprise met en place une architecture AWS pour acheminer des flux de données en temps réel depuis un centre de données sur site vers une application exécutée sur AWS. L'entreprise a besoin d'une connexion réseau stable avec une latence minimale. Quelle solution doit-elle utiliser pour connecter l'application et le centre de données afin de répondre à ces exigences ?  
**Votre réponse est correcte**  
A. AWS Direct Connect

#### Explications

Direct Connect établit une liaison réseau privée et dédiée entre le routeur local du client et un point de présence AWS. En contournant l'Internet public, il offre un débit prévisible à faible latence et une gigue réduite, prend en charge les interfaces virtuelles privées pour une connexion directe aux VPC et peut être intégré à une passerelle Direct Connect pour accéder à plusieurs VPC — autant d'atouts adaptés aux flux de données en temps réel.  
B. Internet public

#### Explications

Le trafic transitant par l'Internet public est acheminé au mieux via plusieurs systèmes autonomes ; la latence et la perte de paquets sont donc variables et non couvertes par un SLA d'AWS. Cette imprévisibilité en fait un choix inadapté aux exigences strictes de latence en temps réel.  
C. VPN AWS

#### Explications

Le VPN site à site d'AWS établit des tunnels chiffrés sur Internet. Bien qu'il garantisse la confidentialité, il reste soumis aux aléas d'Internet (latence/gigue) et ne peut généralement pas égaler la faible latence constante d'une connexion Direct Connect dédiée ; le VPN est souvent utilisé comme solution de secours ou pour les charges de travail tolérant une latence plus élevée.  
D. Amazon Connect

#### Explications

Amazon Connect est un service de centre de contact cloud géré pour l'engagement client. Il ne s'agit pas d'un service de réseau et il n'assure pas la connectivité entre les centres de données sur site et AWS.  
Explication générale  
Cette question évalue les options de connectivité hybride pour le transfert de données en temps réel à faible latence. Une liaison privée dédiée (AWS Direct Connect) offre une connectivité prévisible à faible latence et l'intégration VPC requise pour les flux en temps réel. L'Internet public et les VPN de site à site dépendent des chemins Internet et présentent donc une latence variable ; Amazon Connect est indépendant du transport réseau.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 86Incorrect  
Une entreprise dispose d'une politique IAM gérée qui n'accorde pas aux utilisateurs les autorisations nécessaires pour accomplir les tâches requises. Comment résoudre ce problème ?  
A. Activez AWS Shield Advanced.

#### Explications

Incorrect. AWS Shield Advanced fournit une protection et des mesures d'atténuation contre les attaques DDoS afin d'améliorer la disponibilité des applications ; il ne modifie pas les contrôles d'accès basés sur l'identité et n'accorde pas d'autorisations aux principaux IAM.  
**Bonne réponse**  
B. Créez une stratégie IAM personnalisée.

#### Explications

Exact. La création d'une stratégie IAM gérée par le client (JSON) permet de spécifier précisément les actions AWS et les ARN de ressources requis, puis d'associer cette stratégie à des utilisateurs, des groupes ou des rôles. Ceci offre un contrôle d'accès précis, basé sur le principe du moindre privilège, et comble les lacunes des stratégies immuables gérées par AWS. Utilisez le simulateur de stratégie IAM pour valider les autorisations et CloudTrail pour auditer les modifications.  
C. Utilisez une règle gérée par un pare-feu d'application Web (WAF) tiers provenant de l'AWS Marketplace.

#### Explications

Incorrect. Les règles AWS WAF et Marketplace WAF protègent les applications web en filtrant les requêtes HTTP/S ; elles opèrent au niveau de la couche application et ne modifient ni les politiques IAM ni les autorisations des utilisateurs.  
**Votre réponse est incorrecte**  
D. Utilisez AWS Key Management Service (AWS KMS) pour créer une clé gérée par le client.

#### Explications

Incorrect. AWS KMS gère les clés de chiffrement et les politiques régissant leur utilisation. La création d'une clé gérée par le client affecte les contrôles de chiffrement, et non les autorisations IAM plus générales requises pour les tâches des utilisateurs.  
Explication générale  
The issue is missing identity-based permissions. The correct solution is to create and apply a customer-managed (or inline) IAM policy that grants the precise actions and resources required, following least-privilege and validating with the IAM Policy Simulator. The other options (DDoS protection, WAF rules, KMS keys) address security domains unrelated to granting or modifying IAM permissions.  
Domaine  
Domain 2: Security and Compliance  
Question 87Incorrect  
A company has decided to adopt Amazon EC2 infrastructure and wants to scale various stateless services for short-term usage. Which EC2 pricing model is MOST cost-efficient to meet these requirements?  
**Bonne réponse**  
A. Spot Instances

#### Explications

Uses spare EC2 capacity offered at steep discounts compared with standard pricing. Ideal for ephemeral, fault‑tolerant, stateless workloads because capacity can be reclaimed with a short (two‑minute) interruption notice; design patterns such as checkpointing, diversified instance types, Spot Fleet/Spot Instance pools, and EC2 Auto Scaling (with mixed instances and capacity‑optimized allocation) are used to maximize availability and cost savings.  
**Votre réponse est incorrecte**  
B. On-Demand Instances

#### Explications

Provides pay‑as‑you‑go capacity with no long‑term commitment and no interruption risk, so it’s appropriate when immediate, reliable capacity is required. However, its hourly/second billing rates are higher than spare‑capacity options, making it less cost‑efficient for large‑scale, short‑lived, interruption‑tolerant workloads.  
C. Reserved Instances

#### Explications

Requires a time commitment (e.g., 1‑ or 3‑year Reserved Instances or Savings Plans) to obtain lower effective rates. These offerings are optimized for predictable, steady‑state usage and do not suit short‑term, highly variable scaling needs.  
D. Dedicated Hosts

#### Explications

Allocates physical servers dedicated to a single customer to meet compliance or licensing requirements (visibility into sockets/cores and host IDs). This model incurs higher cost and reduced elasticity, so it is not appropriate for short‑term, rapidly scaled stateless services.  
Explication générale  
This item assesses EC2 pricing model selection. For short‑term, stateless workloads that can tolerate interruptions, the spare‑capacity pricing model delivers the greatest cost savings by leveraging unused EC2 capacity and AWS features (Spot Fleet, mixed instance Auto Scaling, interruption‑handling strategies). Other models (On‑Demand, Reserved, Dedicated Hosts) trade lower interruption risk, long‑term discounts, or physical isolation for higher cost or reduced flexibility, and therefore are less suitable here.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 88Correct  
A company wants a fully managed service that centralizes and automates data protection across AWS services and hybrid workloads. Which AWS service will meet these requirements?  
A. AWS Artifact

#### Explications

AWS Artifact is a portal for on-demand access to AWS compliance reports and security and compliance documentation (for example, SOC, PCI, and ISO reports). It does not provide backup orchestration, snapshot management, restore capabilities, or lifecycle policies required for centralized data protection.  
**Votre réponse est correcte**  
B. AWS Backup

#### Explications

Provides a fully managed, centralized backup service with backup plans, backup vaults, lifecycle/retention policies, and cross‑region / cross‑account copy. Integrates with AWS resources (EBS, RDS, DynamoDB, EFS, FSx, etc.) and with on‑premises environments via AWS Backup Gateway to automate backups and restores across cloud and hybrid workloads.  
C. AWS Batch

#### Explications

AWS Batch is a job scheduling and compute orchestration service for running batch processing workloads on AWS. It manages compute environments and job queues but does not manage data backups, snapshots, or automated data protection.  
D. AWS Shield

#### Explications

AWS Shield is a managed service that provides DDoS protection (network and transport layer defenses). Its focus is availability and attack mitigation, not data backup, retention, or restore functionality.  
Explication générale  
This question asks which managed AWS service centralizes and automates data protection across AWS and hybrid environments. AWS Backup is the dedicated service for centralized backup management (backup plans, vaults, lifecycle, cross‑region/cross‑account copy) and integrates with on‑premises via Backup Gateway. The other options address compliance reporting (Artifact), batch compute (Batch), or DDoS protection (Shield), so they do not meet the data protection/backup requirements.  
Domaine  
Domain 2: Security and Compliance  
Question 89Incorrect  
A company wants to design its cloud architecture so that it can support development innovations, and continuously improve processes and procedures. This is an example of which pillar of the AWS Well-Architected Framework?  
A. Security

#### Explications

This pillar addresses protecting data, systems, and assets through controls such as IAM, encryption, logging, and auditing (for example AWS IAM, KMS, CloudTrail, AWS Config). Those controls focus on confidentiality, integrity, and accountability rather than on instituting processes and practices to drive continuous operational improvement or foster development innovation.  
B. Performance efficiency

#### Explications

This pillar is about making optimal use of IT resources and selecting the right compute, storage, and networking options (for example Auto Scaling, serverless architectures, Amazon CloudFront) to meet system requirements. It emphasizes resource selection and monitoring for performance, not the organizational processes and automation practices used to continuously improve operations and enable innovation.  
**Bonne réponse**  
C. Operational excellence

#### Explications

This pillar is about how an organization runs and evolves systems and processes: automating operations, defining operations-as-code, instrumenting, learning from operations, and iterating procedures to enable rapid, safe innovation (examples include using CloudFormation/Infrastructure as Code, CI/CD pipelines, Systems Manager, CloudWatch for automation and feedback). Those practices directly support continuous improvement and development innovation.  
**Votre réponse est incorrecte**  
D. Reliability

#### Explications

This pillar focuses on designing systems to withstand and recover from failures—availability, fault tolerance, and recovery planning (for example multi‑AZ/multi‑Region deployments, Auto Scaling, Route 53 failover). While critical to reliable operation, it does not primarily describe the cultural and procedural continuous-improvement practices that enable ongoing innovation.  
Explication générale  
The scenario describes enabling development innovations and continuously improving processes and procedures, which maps to the Operational Excellence pillar. Operational Excellence emphasizes organizational practices (operations-as-code, automation, measurement, and iterative improvement) that enable agility and learning. The other pillars address distinct concerns: Security (protecting assets), Performance Efficiency (resource selection and optimization), and Reliability (availability and fault tolerance).  
Domaine  
Domain 1: Cloud Concepts  
Question 90Correct  
A company operates a petabyte-scale data warehouse to analyze its data. The company wants a solution that will not require manual hardware and software management. Which AWS service will meet these requirements?  
A. Amazon DocumentDB (with MongoDB compatibility)

#### Explications

Amazon DocumentDB is a managed document (JSON) database compatible with MongoDB workloads. It is optimized for transactional/document queries and operational workloads, not for columnar, massively parallel analytics or petabyte-scale data warehousing, so it does not meet the requirement.  
**Votre réponse est correcte**  
B. Amazon Redshift

#### Explications

Amazon Redshift is a purpose-built, fully managed data warehouse that supports petabyte-scale analytics using a columnar storage format and a Massively Parallel Processing (MPP) architecture. Management tasks such as provisioning, software patching, backups, and scaling are handled by the service (including options like RA3 nodes and managed storage), making it the appropriate no-heavy-ops solution for the scenario.  
C. Amazon Neptune

#### Explications

Amazon Neptune is a managed graph database for property graph and RDF workloads (graph queries, traversals). Its design, query models, and scaling characteristics are oriented to graph use cases rather than large-scale, SQL-based analytical data warehousing.  
D. Amazon ElastiCache

#### Explications

Amazon ElastiCache provides in-memory caching (Redis or Memcached) to reduce application latency. It is not a durable, columnar, or MPP analytics store and is not intended for petabyte-scale data warehousing or complex analytical queries.  
Explication générale  
The requirement is for a fully managed, petabyte-scale data warehouse that minimizes manual hardware and software management. Amazon Redshift is designed for that purpose (columnar storage, MPP, managed operations and scaling). The other services listed are managed databases or caches for different workload types (document, graph, in-memory cache) and are not suitable replacements for a large-scale analytical data warehouse.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 91Incorrect  
Which AWS service or resource provides answers to the most frequently asked security-related questions that AWS receives from its users?  
A. AWS Artifact

#### Explications

Ce service offre un accès à la demande aux rapports de conformité AWS, aux documents d'audit et à la documentation relative à la sécurité et à la conformité (par exemple, les rapports SOC, PCI et ISO). Il s'agit d'un référentiel de documents de conformité et non d'une base de questions-réponses structurée ; par conséquent, il ne constitue pas le principal lieu de publication des réponses d'AWS aux questions de sécurité fréquemment posées.  
B. Amazon Connect

#### Explications

Un service de centre de contact cloud géré pour la gestion des appels entrants et sortants des clients. Il est axé sur la téléphonie et les flux de travail de contact, et non sur la publication ou la maintenance de la FAQ ou des articles de la base de connaissances AWS relatifs à la sécurité.  
**Votre réponse est incorrecte**  
C. Chatbot AWS

#### Explications

Cette intégration permet d'envoyer des alertes AWS et d'exécuter des commandes simples depuis des plateformes de messagerie instantanée (Slack, Chime). Il s'agit d'un outil opérationnel/de notification, et non d'une base de connaissances ou d'une FAQ sur la sécurité.  
**Bonne réponse**  
D. Centre de connaissances AWS

#### Explications

Une ressource officielle du support AWS qui publie des articles concis sous forme de questions-réponses abordant les questions fréquemment posées, notamment en matière de sécurité. Il s'agit d'une collection organisée et consultable, maintenue par AWS, qui propose des réponses éprouvées et des solutions aux problèmes courants rencontrés par les utilisateurs ; c'est pourquoi elle convient à ce cas d'utilisation.  
Explication générale  
Cette question teste la connaissance des ressources officielles AWS pour trouver des réponses aux questions fréquentes en matière de sécurité. Le Centre de connaissances AWS est le référentiel de questions-réponses (FAQ) organisé et consultable qu'AWS utilise pour publier des conseils de sécurité et des procédures de dépannage courants. Les autres options correspondent à différents types de services : un référentiel de documents de conformité (Artifact), un outil de centre de contact (Connect) et une intégration de chat/notifications (Chatbot). Aucun de ces services ne constitue la base de connaissances principale pour les FAQ.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 92Correct  
Une entreprise doit transférer des données entre un compartiment Amazon S3 et une application sur site. Qui est responsable de la sécurité de ces données, selon le modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
A. L'entreprise

#### Explications

Conformément au modèle de responsabilité partagée d'AWS, les clients sont responsables de la sécurité dans le cloud. Cela inclut la protection des données en transit et au niveau applicatif lors des transferts de données entre S3 et les systèmes sur site. Parmi les mesures pratiques que le client doit configurer, citons l'application du protocole TLS/HTTPS, l'utilisation d'un VPN ou d'une connexion Direct Connect chiffrée, l'application de politiques de compartiment S3 et d'autorisations IAM appropriées, ainsi que l'activation du chiffrement lorsque cela est nécessaire.  
B. AWS

#### Explications

AWS est responsable de la sécurité du cloud, c'est-à-dire des infrastructures physiques, du matériel, du réseau, de la virtualisation et des services gérés. AWS n'assume aucune responsabilité quant à la protection des données du client lors de leur transfert entre S3 et les systèmes sur site ; la configuration du chiffrement, des contrôles d'accès et des mécanismes de transfert reste à la charge du client.  
C. Fournisseur de pare-feu

#### Explications

A firewall vendor supplies products that can help control and inspect network traffic, but using their tools does not shift the customer’s responsibility under the shared responsibility model. Unless the vendor is engaged under a managed‑service contract, the customer must deploy and configure network security controls and encryption for data transfers.  
D. AWS Marketplace partner

#### Explications

An AWS Marketplace partner may provide software or managed services that assist with secure transfer, but a Marketplace listing alone does not transfer responsibility for the customer’s data. The customer remains responsible for configuring encryption, IAM, and policies unless a partner is explicitly contracted to manage those controls.  
Explication générale  
This item tests understanding of the AWS shared responsibility model: AWS secures the underlying cloud infrastructure (‘security of the cloud’), while customers are responsible for protecting their data and applications in the cloud (‘security in the cloud’). Because data transfers between S3 and on‑premises systems involve customer data and configuration, the customer must implement encryption, proper transfer channels (TLS/VPN/Direct Connect), and access controls. The distractors describe parties that either secure infrastructure (AWS) or provide tools/services (third‑party vendors/partners) but do not replace the customer’s responsibility unless explicitly contracted.  
Domaine  
Domain 2: Security and Compliance  
Question 93Incorrect  
A company wants to migrate its server-based applications to the AWS Cloud. The company wants to determine the total cost of ownership for its compute resources that will be hosted on the AWS Cloud. Which combination of AWS services or tools will meet these requirements? (Choose two.)  
**Votre sélection est correcte**  
A. AWS Pricing Calculator

#### Explications

The AWS service that provides a web-based cost estimator for EC2, ECS, Lambda, storage and networking lets you model On-Demand, Reserved Instances and Savings Plans and produce a detailed cost breakdown. This output is used to quantify expected monthly and annual cloud compute costs, which is a required input when calculating TCO for migrated servers.  
**Sélection correcte**  
B. Migration Evaluator

#### Explications

The assessment tool that discovers on-premises server inventory and collects utilization metrics produces right‑sizing recommendations and migration readiness and TCO reports. It analyzes current resource usage and maps it to equivalent AWS compute offerings so you can estimate infrastructure reductions and projected AWS costs for an accurate TCO.  
C. AWS Support Center

#### Explications

The support portal and case-management service is used to open technical or billing cases and manage support plans; it does not perform cost modeling, workload discovery, or generate TCO estimates.  
**Votre sélection est incorrecte**  
D. AWS Application Discovery Service

#### Explications

The discovery agent/service collects on-premises inventory, process and dependency data and utilization metrics that are useful inputs to cost-assessment tools, but by itself it does not produce comprehensive cost estimates or TCO reports.  
E. AWS Database Migration Service (AWS DMS)

#### Explications

The database migration service facilitates homogeneous and heterogeneous database migrations and continuous replication; it helps move data but does not provide cost-estimation or TCO calculation features for compute.  
Explication générale  
To determine TCO for migrating server-based applications you need both a cost-modeling estimator and an assessment tool that collects on‑premises usage and recommends right‑sizing. The cost estimator produces detailed pricing for AWS compute, storage and networking (including pricing options such as Reserved Instances and Savings Plans), while the migration assessment tool analyzes existing servers, utilization and dependencies and produces TCO and right‑sizing recommendations. Support portals, discovery-only agents, and migration-execution services are useful for other parts of a migration but do not alone produce the combined cost and sizing analysis required for TCO.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 94Correct  
Which AWS service or feature allows users to securely store encrypted credentials and retrieve these credentials when required?  
A. AWS Encryption SDK

#### Explications

Incorrect. The AWS Encryption SDK is a client-side library for performing encryption and decryption (including envelope encryption) and integrates with AWS KMS for key management. It does not provide a centralized secrets storage, rotation, or retrieval API needed for credential lifecycle management.  
B. AWS Security Hub

#### Explications

Incorrect. AWS Security Hub aggregates, normalizes, and prioritizes security findings from multiple AWS services and third-party tools to help with security posture management; it does not store or serve application credentials or secrets.  
**Votre réponse est correcte**  
C. AWS Secrets Manager

#### Explications

Correct. This service offers centralized secret lifecycle features: secrets are encrypted at rest using AWS KMS, can be retrieved programmatically via APIs/SDKs, support automatic rotation for many managed resources (for example, RDS credentials), and access is controlled with fine-grained IAM policies and resource-based permissions.  
D. AWS Artifact

#### Explications

Incorrect. AWS Artifact provides on-demand access to AWS compliance reports and security and compliance documentation (agreements, certifications, audit artifacts). It is not a secrets management or credential storage service.  
Explication générale  
The question tests knowledge of AWS secret-management capabilities. The correct service provides centralized lifecycle management for credentials with encryption, access control, rotation, and programmatic retrieval — features provided by AWS Secrets Manager. The other options are unrelated: the Encryption SDK is a client-side crypto library, Security Hub is a findings/monitoring service, and Artifact provides compliance documents.  
Domaine  
Domain 2: Security and Compliance  
Question 95Correct  
Which task can a company perform by using security groups in the AWS Cloud?  
**Votre réponse est correcte**  
A. Allow access to an Amazon EC2 instance through only a specific port.

#### Explications

Verified correct. Security groups are instance-level, stateful virtual firewalls attached to network interfaces (ENIs). You define inbound and outbound allow rules that specify protocol, port ranges and source/destination (CIDR blocks or other security groups), which enables precise control over which ports are reachable on an EC2 instance. Security groups are allow-only and automatically permit return traffic because they are stateful.  
B. Deny access to malicious IP addresses at a subnet level.

#### Explications

Incorrect. Security groups operate at the instance/ENI level and do not apply at the subnet level. To implement subnet-level, stateless allow/deny rules (including explicit denies), use network ACLs (NACLs), which are applied to subnets and are stateless.  
C. Protect data that is cached by Amazon CloudFront.

#### Explications

Incorrect. Security groups do not control content cached by Amazon CloudFront. CloudFront access and protection are managed at the distribution level using mechanisms such as origin access control/identity, signed URLs or cookies, TLS, and AWS WAF.  
D. Apply a stateless firewall to an Amazon EC2 instance.

#### Explications

Incorrect. Security groups are stateful firewalls: return traffic for an established connection is automatically allowed. If a stateless firewall is required (no automatic return-traffic handling) at the subnet level, network ACLs are the appropriate AWS feature.  
Explication générale  
This question tests understanding of AWS security groups. The correct choice is A because security groups provide instance-level, stateful control over inbound and outbound traffic by protocol and port. The other options are distractors: subnet-level denials and stateless behavior are handled by network ACLs, and CloudFront cached content is protected using distribution-level controls (signed URLs, origin access, TLS, AWS WAF), not security groups.  
Domaine  
Domain 2: Security and Compliance  
Question 96Correct  
A company has developed a new In-house application. The company does not have a way to determine or predict the usage demand that the application will create. Which AWS Cloud computing benefit is the company seeking?  
A. Easy to use

#### Explications

Describes usability and administrative simplicity, which does not ensure the infrastructure can handle unpredictable traffic. The ability to cope with variable demand requires automatic adjustment of compute and networking resources, not just an easy-to-use system.  
B. Cost-effective

#### Explications

Refers to reducing costs through pricing models like pay-as-you-go and reserved capacity. While cost optimization is a cloud benefit, it does not by itself provide the capability to automatically match resource capacity to unknown or spiking usage patterns.  
C. Secure

#### Explications

Concerns protecting data, identities, and system availability (confidentiality, integrity, availability). Security features do not address automatic resource scaling to meet variable demand.  
**Votre réponse est correcte**  
D. Scalable and high performance

#### Explications

This option corresponds to the cloud principle of automatically adjusting resource capacity to meet changing load. AWS services that deliver this capability include Amazon EC2 Auto Scaling and Elastic Load Balancing for compute, AWS Lambda for serverless automatic scaling, and Amazon S3 for virtually unlimited storage—together they prevent over‑ or under‑provisioning and maintain performance during demand spikes.  
Explication générale  
The question tests understanding of cloud elasticity: the ability to automatically adjust resources to match unpredictable application demand. AWS provides this through features and services that scale capacity up and down (for example EC2 Auto Scaling, ELB, Lambda, and S3), avoiding manual provisioning and ensuring performance. The other choices describe real benefits (usability, cost control, security) but do not solve the core problem of unpredictable usage patterns.  
Domaine  
Domain 1: Cloud Concepts  
Question 97Correct  
A company needs to check for IAM access keys that have not been rotated recently. Which AWS service should the company use to meet this requirement?  
A. AWS WAF

#### Explications

A web application firewall that filters and blocks malicious HTTP(S) requests (e.g., SQL injection, XSS). It operates at the application request layer and does not provide IAM credential auditing or reports on access key rotation.  
B. AWS Shield

#### Explications

A managed DDoS protection service focused on mitigating network- and transport-layer attacks. Its capabilities are for attack protection and do not include auditing or flagging IAM access keys that need rotation.  
C. Amazon Cognito

#### Explications

An identity/authentication service for application users (user pools, identity pools, federation) that issues tokens and temporary credentials for apps. It manages end-user authentication, not IAM user access key lifecycle or rotation reporting.  
**Votre réponse est correcte**  
D. AWS Trusted Advisor

#### Explications

A service that runs automated best-practice checks across cost, performance, security, fault tolerance, and service limits. Its security checks include identifying long-standing IAM access keys and recommending rotation (flagging keys that haven’t been rotated within the recommended timeframe), which directly meets the requirement.  
Explication générale  
This question tests knowledge of AWS tools for credential hygiene. The appropriate tool among the options is the service that performs automated security checks and will flag IAM access keys that need rotation. The other choices address web application protection, DDoS mitigation, or application user authentication, and therefore do not provide IAM access key rotation auditing. (Note: for more detailed auditing you can also use the IAM credential report or AWS Config, but among the provided options the automated security check service is the correct choice.)  
Domaine  
Domain 2: Security and Compliance  
Question 98Correct  
A company wants to implement detailed tracking of its cloud costs by department and project. Which AWS feature or service should the company use?  
A. Consolidated billing

#### Explications

Incorrect — AWS Organizations consolidated billing (a payer/management account model) centralizes invoicing and can simplify payment collection across accounts, but it does not provide resource- or project-level cost attribution. Detailed breakdowns still require tagging, separate accounts per cost center, Cost Categories, or Cost and Usage Reports to allocate costs to departments or projects.  
**Votre réponse est correcte**  
B. Cost allocation tags

#### Explications

Correct — Cost allocation tags are user-defined labels that, once applied to resources and activated for cost allocation in the Billing console, appear in Cost Explorer and the AWS Cost and Usage Report (CUR). They enable grouping, filtering, and allocation of costs by department or project. To use them effectively, apply consistent tag keys/values, activate the tag keys for cost allocation, and allow propagation time for reporting.  
C. AWS Marketplace

#### Explications

Incorrect — AWS Marketplace is a catalog for purchasing third-party software and services. Marketplace listings and charges appear on the AWS bill, but the Marketplace does not provide native features to create department- or project-level cost allocation or tagging schemes.  
D. AWS Budgets

#### Explications

Incorrect (related but not sufficient) — AWS Budgets lets you set cost/usage thresholds and receive alerts and can be scoped by tags or linked accounts. However, Budgets does not itself produce the allocation taxonomy; it depends on tags or account structure to define how costs are attributed and tracked.  
Explication générale  
The question tests how to create resource- and project-level cost attribution. Cost allocation tags are the AWS feature designed for labeling resources so costs can be grouped and reported by department or project in Cost Explorer and the Cost and Usage Report. Consolidated billing centralizes invoices but doesn’t provide resource-level allocation; AWS Budgets provides monitoring/alerts and can use tags for scoping but does not create the allocation metadata; Marketplace is for software purchases, not cost allocation.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 99Correct  
A user wants to securely automate the management and rotation of credentials that are shared between applications, while spending the least amount of time on managing tasks. Which AWS service or feature can be used to accomplish this?  
A. AWS CloudHSM

#### Explications

CloudHSM provides dedicated hardware security modules for generating and protecting cryptographic keys (FIPS 140-2 Level 3\) and is intended for customers requiring HSM-backed key operations and compliance. It requires provisioning and operational management of HSMs and does not include built-in secret lifecycle features such as automated credential rotation and distributed secret retrieval for applications.  
B. AWS Key Management Service (AWS KMS)

#### Explications

AWS KMS manages and protects cryptographic keys and can rotate customer master keys, and it is commonly used to encrypt secrets. However, it does not act as a secrets store or provide automated credential rotation workflows, versioning, or secret distribution for application credentials — a separate secrets-management layer is required.  
**Votre réponse est correcte**  
C. AWS Secrets Manager

#### Explications

A managed secrets service that stores secrets encrypted (using KMS), offers automatic rotation (via Lambda or native integrations such as RDS), secret versioning/staging, and fine-grained IAM access controls. These capabilities provide centralized, automated secret lifecycle management and minimize operational overhead for rotating and distributing credentials.  
D. Server-side encryption

#### Explications

Server-side encryption is a data-at-rest protection mechanism (for example SSE-S3 or SSE-KMS) that encrypts stored objects. It protects storage but does not provide secret storage semantics, rotation workflows, versioning, or secret distribution for application credentials.  
Explication générale  
This tests knowledge of AWS services for centralized secret lifecycle management. The correct solution is the managed secrets service because it combines encrypted storage, automated rotation, access control, and service integrations to automate credential rotation and distribution. KMS and CloudHSM address key protection and management but lack secret rotation and lifecycle features; server-side encryption only protects data at rest and does not manage credentials.  
Domaine  
Domain 2: Security and Compliance  
Question 100Incorrect  
A company wants to verify if multi-factor authentication (MFA) is enabled for all users within its AWS accounts. Which AWS service or resource will meet this requirement?  
**Votre réponse est incorrecte**  
A. AWS Cost and Usage Report

#### Explications

The Cost and Usage Report is a billing/usage data export; it provides detailed cost and usage metrics and resource-level billing information, but it does not contain IAM credential or MFA state for users.  
**Bonne réponse**  
B. IAM credential reports

#### Explications

The IAM credential report is a downloadable CSV that provides a snapshot of credential status for IAM users, including the mfa\_active column (true/false). It can be generated via the IAM console or the AWS CLI (iam generate-credential-report / iam get-credential-report) and is the appropriate tool to audit MFA enablement for IAM users. Note: federated identities and some external SSO providers are not represented in the IAM credential report, so those should be checked in their identity provider or AWS SSO configuration.  
C. AWS Artifact

#### Explications

AWS Artifact provides on-demand access to AWS compliance reports and legal agreements (e.g., SOC, ISO), and does not expose per-user credential or MFA status for account users.  
D. Amazon CloudFront reports

#### Explications

CloudFront reporting and logs relate to CDN distributions, request/edge metrics, and content delivery behavior. They do not provide any information about IAM user credentials or MFA settings.  
Explication générale  
Pour vérifier l'activation de l'authentification multifacteur (MFA) pour les utilisateurs IAM, le rapport d'informations d'identification IAM est la ressource appropriée car il répertorie explicitement l'état des informations d'identification (y compris le champ mfa\_active) pour chaque utilisateur IAM. Les rapports de facturation, les portails de documents de conformité et les rapports CDN ne contiennent pas les détails des informations d'identification des utilisateurs. Pour les identités gérées en dehors d'IAM (utilisateurs fédérés ou SSO externe), il convient d'auditer séparément le fournisseur d'identité externe ou le service SSO AWS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 101Incorrect  
Quelle fonctionnalité AWS offre une plateforme gratuite permettant aux utilisateurs AWS de rejoindre des groupes communautaires, de poser des questions, de trouver des réponses et de lire des articles rédigés par la communauté sur les meilleures pratiques ?  
**Votre réponse est incorrecte**  
A. Centre de connaissances AWS

#### Explications

Cette ressource contient des articles pratiques et des conseils de dépannage officiels, rédigés par AWS et sélectionnés par AWS ; il ne s’agit pas d’un forum communautaire avec des questions posées par les utilisateurs, des votes ou des réponses générées par la communauté, elle ne répond donc pas aux exigences d’une plateforme de questions-réponses gratuite et gérée par la communauté.  
**Bonne réponse**  
B. AWS re:Post

#### Explications

Il s'agit d'une plateforme de questions-réponses gratuite et collaborative où clients et experts AWS publient des questions et des réponses, votent pour les réponses utiles, marquent les solutions acceptées et publient des articles et des bonnes pratiques rédigés par la communauté. Ses fonctionnalités (tags par service, système de vote, réponses acceptées et contenu participatif) en font le forum communautaire gratuit idéal pour poser des questions et trouver des conseils partagés par la communauté.  
C. AWS IQ

#### Explications

Ce service met en relation les clients avec des professionnels certifiés AWS et rigoureusement sélectionnés pour des missions rémunérées et du conseil d'experts. Il facilite le recrutement et la facturation de services professionnels, contrairement à un service gratuit de questions-réponses ou de rédaction d'articles géré par la communauté.  
D. Support AWS pour entreprises

#### Explications

Il s'agit d'une offre de support payante comprenant la gestion technique de votre compte, des SLA de réponse rapide et une assistance directe des ingénieurs AWS. C'est un niveau de support commercial, et non un forum public, gratuit et collaboratif d'échange de questions-réponses et de publications entre utilisateurs.  
Explication générale  
Cette question évalue la connaissance des ressources communautaires AWS par rapport à la documentation officielle et aux services d'assistance payants. La bonne réponse est la plateforme de questions-réponses gratuite et communautaire qui propose des questions, des réponses, un système de vote et des articles rédigés par les utilisateurs. Les réponses incorrectes décrivent la documentation officielle AWS, le recours à des consultants payants et les différents niveaux d'assistance payants, qui n'offrent pas les mêmes fonctionnalités de forum communautaire gratuit.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 102Incorrect  
Quelles options correspondent aux perspectives du cadre d'adoption du cloud AWS (AWS CAF) ? (Choisissez deux réponses.)  
A. Maîtrise du cloud

#### Explications

Il ne s'agit pas d'une perspective officielle du CAF d'AWS. Ce terme décrit les initiatives en matière de compétences organisationnelles et de formation que le CAF aborde dans le cadre de la perspective « Personnel » (rôles, effectifs, apprentissage), mais ce n'est pas une perspective nommée du CAF.  
**Sélection correcte**  
B. Sécurité

#### Explications

L'une des six perspectives du CAF AWS. Elle se concentre sur la protection des informations et des systèmes en matière de confidentialité, d'intégrité et de disponibilité ; elle couvre la gestion des identités et des accès, les contrôles et la surveillance, la gestion des risques et l'alignement sur la conformité lors de l'adoption du cloud.  
**Votre sélection est incorrecte**  
C. Accélération de changement

#### Explications

Ce terme décrit les activités de gestion du changement organisationnel (accélération des transformations culturelles et procédurales). Ces responsabilités sont prises en charge dans le cadre des perspectives « Personnes » et « Gouvernance » du CAF, mais il n’existe pas de perspective CAF distincte et nommée ainsi.  
**Votre sélection est incorrecte**  
D. Architecture

#### Explications

Cela concerne la conception technique et la structure du système, que le CAF aborde principalement sous l'angle de la plateforme et des opérations. Il s'agit d'une préoccupation technique plutôt que d'une perspective distincte et nommée du CAF.  
**Sélection correcte**  
E. Business

#### Explications

L'une des six perspectives du CAF d'AWS. Elle vise à aligner les initiatives cloud sur la stratégie organisationnelle et les besoins des parties prenantes, à définir les résultats commerciaux, à mesurer la création de valeur et à soutenir l'analyse de rentabilité et la priorisation des investissements.  
Explication générale  
Le cadre d'adoption du cloud AWS (AWS Cloud Adoption Framework) définit six perspectives officielles — Métier, Personnel, Gouvernance, Plateforme, Sécurité et Opérations — pour guider les différentes dimensions de l'adoption du cloud. Les choix pertinents correspondent aux perspectives Métier et Sécurité, car elles traitent explicitement de l'alignement sur les objectifs métier et des contrôles des risques et de la sécurité. Les autres options décrivent des concepts connexes (compétences, gestion du changement, architecture technique) abordés dans d'autres perspectives du cadre d'adoption du cloud, mais qui ne sont pas désignées comme telles.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 103Incorrect  
Une entreprise prévoit d'utiliser un appareil Amazon Snowball Edge pour transférer des fichiers vers le cloud AWS. Quelles sont les activités liées à un appareil Snowball Edge qui sont disponibles gratuitement pour l'entreprise ?  
**Votre réponse est incorrecte**  
A. Utilisation de l'appareil Snowball Edge pendant une période de 10 jours

#### Explications

Incorrect. Les tâches AWS Snowball nécessitent des frais (qui couvrent une période d'utilisation limitée) et les jours inclus font partie intégrante de cette tâche payante ; il n'existe pas de période d'utilisation « gratuite » de 10 jours distincte. Tout jour supplémentaire au-delà de la période incluse entraîne des frais journaliers par appareil.  
B. Le transfert des données d'Amazon S3 vers l'appliance Snowball Edge

#### Explications

Incorrect. L'exportation de données d'Amazon S3 vers un périphérique Snowball (ou le déplacement de données hors de S3) n'est pas considérée comme une opération d'entrée gratuite ; les tâches Snowball et les activités d'exportation associées sont soumises à des frais de traitement/expédition et à d'éventuels frais de déplacement de données, il ne s'agit donc pas d'une opération gratuite.  
**Bonne réponse**  
C. Le transfert des données de l'appliance Snowball Edge vers Amazon S3

#### Explications

Exactement. AWS ne facture pas de frais de transfert de données pour l'importation de données depuis un appareil Snowball vers Amazon S3 : l'ingestion de données depuis Snowball vers S3 est donc totalement gratuite. Veuillez noter que les frais liés à la tâche Snowball elle-même (frais d'exécution, frais d'expédition et frais journaliers supplémentaires) restent applicables.  
D. Utilisation quotidienne de l'appareil Snowball Edge après 10 jours

#### Explications

Incorrect. Toute utilisation prolongée de l'appareil au-delà de la période incluse entraîne des frais journaliers. L'utilisation gratuite n'est pas illimitée après cette période ; toute utilisation prolongée est facturée.  
Explication générale  
Cette question teste la compréhension de la tarification d'AWS Snowball : l'importation de données depuis un périphérique Snowball vers Amazon S3 est gratuite, ce qui rend cette opération gratuite en termes d'entrée de données. Cependant, les tâches Snowball entraînent des frais (frais de tâche/d'expédition et frais journaliers après la période incluse). Les réponses incorrectes confondent l'entrée de données gratuite avec les frais de tâche/d'utilisation ou décrivent des opérations d'exportation/sortie qui ne sont pas gratuites.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 104Correct  
Selon le modèle de responsabilité partagée d'AWS, quelle tâche incombe au client ?  
A. Corriger le système d'exploitation Amazon DynamoDB.

#### Explications

Incorrect — Pour les services entièrement gérés comme Amazon DynamoDB, AWS est responsable de l'infrastructure sous-jacente et de l'environnement d'exploitation, y compris des correctifs et de la maintenance. Les clients sont responsables de leurs données, de la configuration et des contrôles d'accès au service, et non du système d'exploitation hôte.  
B. Sécurisez les emplacements périphériques d'Amazon CloudFront en autorisant l'accès physique selon le principe du moindre privilège.

#### Explications

Incorrect — La sécurité physique des emplacements AWS (y compris les sites périphériques CloudFront) est gérée par AWS. Les clients ne peuvent pas contrôler l'accès physique aux infrastructures AWS ; leurs responsabilités portent sur la sécurité logique, notamment la configuration de la distribution et les politiques d'accès.  
C. Protéger le matériel qui exécute les services AWS.

#### Explications

Incorrect — La protection des serveurs, du matériel réseau et des contrôles d'accès aux installations relève de la responsabilité d'AWS. Il incombe aux clients de sécuriser leurs comptes, leurs données et la configuration de leurs ressources au sein de l'environnement AWS.  
**Votre réponse est correcte**  
D. Utilisez AWS Identity and Access Management (IAM) selon le principe du moindre privilège.

#### Explications

C’est exact — Il incombe aux clients de gérer les identités et les accès (sécurité dans le cloud). Cela comprend la création et l’attribution d’utilisateurs, de groupes, de rôles et de politiques IAM, l’application du principe du moindre privilège, l’activation de l’authentification multifacteur et l’audit des accès — des tâches qui protègent les comptes et les ressources des clients.  
Explication générale  
Ce test illustre le modèle de responsabilité partagée d'AWS. AWS assure la sécurité du cloud (matériel, infrastructures et services managés). Les clients sont responsables de la sécurité dans le cloud, notamment de la gestion des identités et des accès, de la protection des données et de la configuration des ressources. Par conséquent, la configuration et l'application des principes de gestion des identités et des accès (IAM) et du moindre privilège relèvent de la responsabilité du client, tandis que les correctifs du système d'exploitation pour les services managés, la protection du matériel et la sécurité physique des sites sont du ressort d'AWS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 105Incorrect  
Parmi les services suivants, lesquels permettent de bloquer le trafic réseau vers une instance ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Groupes de sécurité

#### Explications

Les groupes de sécurité sont des pare-feu virtuels avec état, associés aux interfaces réseau d'une instance. Ils évaluent l'état de la connexion et appliquent des règles d'autorisation au trafic entrant et sortant ; étant donné qu'ils conservent leur état, le trafic de retour est automatiquement autorisé. Bien que les groupes de sécurité ne prennent pas en charge les règles de refus explicites, vous pouvez restreindre ou bloquer le trafic vers une instance en renforçant ou en supprimant des règles d'autorisation.  
**Votre sélection est incorrecte**  
B. Journaux de flux Amazon Virtual Private Cloud (Amazon VPC)

#### Explications

Les journaux de flux Amazon VPC capturent les métadonnées relatives au trafic IP entrant et sortant des interfaces réseau à des fins de surveillance et de dépannage (ces données sont transmises à CloudWatch Logs ou à S3). Il s'agit d'une fonctionnalité d'observabilité passive qui n'impose ni ne bloque le trafic réseau.  
**Sélection correcte**  
C. Listes de contrôle d'accès réseau

#### Explications

Les listes de contrôle d'accès réseau (NACL) sont des listes de contrôle d'accès sans état appliquées au niveau du sous-réseau. Elles évaluent les règles entrantes et sortantes séparément, par ordre numérique, et prennent en charge les entrées d'autorisation et de refus explicites. Elles peuvent donc être utilisées pour bloquer des plages d'adresses IP ou des ports spécifiques pour toutes les instances d'un sous-réseau.  
D. Amazon CloudWatch

#### Explications

Amazon CloudWatch fournit des métriques, des journaux et des alarmes pour la surveillance et l'observabilité. CloudWatch ne bloque pas le trafic ; bien que les alarmes puissent déclencher des actions automatisées (par exemple, une fonction Lambda modifiant les contrôles de sécurité), CloudWatch n'est pas un plan de contrôle réseau.  
E. AWS CloudTrail

#### Explications

AWS CloudTrail enregistre les appels d'API et l'activité des utilisateurs à des fins d'audit et de conformité. Il s'agit d'un service d'audit et de journalisation qui ne contrôle ni ne bloque le trafic réseau.  
Explication générale  
La question porte sur les fonctionnalités AWS permettant d'appliquer des restrictions d'accès au niveau du réseau. Les groupes de sécurité (avec état, associés aux interfaces réseau des instances et comportant des règles d'autorisation) et les listes de contrôle d'accès réseau (sans état, au niveau du sous-réseau et comportant des règles d'autorisation/de refus) sont les mécanismes utilisés pour restreindre ou bloquer le trafic. Les journaux de flux VPC, CloudWatch et CloudTrail offrent des fonctionnalités de journalisation, de surveillance et d'audit, mais n'appliquent pas directement le blocage du réseau.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 106Correct  
Quelle est la responsabilité d'AWS lors de l'utilisation des services AWS ?  
A. Gestion des autorisations des utilisateurs IAM

#### Explications

Incorrect — La configuration des identités, des clés d’accès, des utilisateurs, des groupes, des rôles et des stratégies IAM au sein de votre compte AWS est effectuée par le client. IAM est un service contrôlé par le client pour la gestion des autorisations ; AWS ne configure pas les paramètres IAM des comptes individuels.  
B. Création de règles de groupe de sécurité pour l'accès sortant

#### Explications

Incorrect — Les groupes de sécurité sont des pare-feu virtuels fournis par AWS, mais configurés et gérés par le client pour contrôler le trafic entrant et sortant au niveau de l'instance. AWS fournit la fonctionnalité ; les clients définissent les règles spécifiques.  
**Votre réponse est correcte**  
C. Maintien des contrôles physiques et environnementaux

#### Explications

Exact — AWS est responsable de la sécurité physique et des contrôles environnementaux (contrôles d'accès au centre de données, alimentation électrique, refroidissement, maintenance du matériel physique) dans le cadre de la « sécurité du cloud » du modèle de responsabilité partagée.  
D. Application des correctifs du système d'exploitation Amazon EC2

#### Explications

Incorrect — Le système d'exploitation invité et les applications sur les instances EC2 sont gérés par le client. L'application des correctifs du système d'exploitation et des applications est à la charge du client, sauf s'il utilise un service géré incluant explicitement la gestion du système d'exploitation.  
Explication générale  
Cette question teste le modèle de responsabilité partagée d'AWS. AWS gère la sécurité du cloud (infrastructure physique, contrôles environnementaux des centres de données et matériel). Les clients sont responsables de la sécurité dans le cloud : gestion des identités et des accès, règles réseau et application des systèmes d'exploitation et des applications sur les ressources de calcul. Par conséquent, la maintenance des contrôles physiques et environnementaux incombe à AWS (option C) ; les autres options relèvent de la responsabilité du client.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 107Correct  
Quelle équipe ou offre AWS aide les utilisateurs à accélérer leur adoption du cloud grâce à des engagements payants dans divers domaines de spécialisation ?  
A. Support AWS pour entreprises

#### Explications

Cette offre est un plan de support qui fournit une assistance technique 24h/24 et 7j/7, des conseils et un gestionnaire de compte technique (TAM) pour les escalades et les meilleures pratiques opérationnelles ; elle ne prend pas en charge les missions de conseil spécialisées basées sur des projets pour assurer et accélérer l'adoption du cloud.  
B. Architectes de solutions AWS

#### Explications

Les architectes de solutions fournissent des conseils en matière d'architecture, des modèles de référence et des bonnes pratiques pour aider à concevoir des solutions, mais ils constituent des ressources consultatives plutôt qu'une organisation formelle et rémunérée de réalisation de projets qui exécute des missions d'adoption spécialisées.  
**Votre réponse est correcte**  
C. Services professionnels AWS

#### Explications

Une équipe AWS dédiée qui propose des missions de conseil payantes et axées sur les projets dans divers domaines de spécialisation (par exemple, la migration, l'analyse de données, la sécurité et l'apprentissage automatique), travaillant avec les clients pour planifier, mettre en œuvre et accélérer l'adoption du cloud à l'aide de méthodologies prescriptives et de consultants seniors.  
D. Gestionnaires de comptes AWS

#### Explications

Les gestionnaires de comptes se concentrent sur la relation commerciale, la gestion des contrats et des comptes, ainsi que sur la défense des intérêts des clients ; ils n’effectuent généralement pas la mise en œuvre technique spécialisée et concrète qui accélère l’adoption du cloud par le biais de projets de mise en œuvre payants.  
Explication générale  
La question établit une distinction entre les rôles de conseil, d'assistance et de vente, et l'organisation qui réalise les projets d'adoption payants. La bonne réponse est l'organisation AWS qui propose des missions de conseil structurées et spécialisées pour la mise en œuvre de solutions cloud. Les autres options décrivent des plans d'assistance, des conseils en architecture ou la gestion de compte, qui sont complémentaires mais ne constituent pas l'équipe principale chargée de la réalisation des projets d'adoption.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 108Correct  
Une entreprise souhaite déployer plusieurs charges de travail sur AWS. Chaque charge de travail est associée à une unité commerciale différente. L'entreprise souhaite séparer et suivre les coûts de chaque unité commerciale. Quelle solution répondra à ces exigences avec le moins de frais d'exploitation ?  
**Votre réponse est correcte**  
A. Utilisez AWS Organizations et créez un compte pour chaque unité commerciale.

#### Explications

AWS Organizations, avec ses comptes distincts, permet de définir des limites de coûts naturelles et utilise une facturation consolidée : les frais sont facturés par compte tandis que les factures sont centralisées. Cette approche nécessite un minimum d'interventions continues par rapport aux systèmes d'étiquetage et s'intègre directement à Cost Explorer, aux rapports de coûts et d'utilisation AWS, à AWS Budgets et aux politiques de contrôle des services/IAM pour une gouvernance basée sur des règles.  
B. Use a spreadsheet to control the owners and cost of each resource.

#### Explications

A spreadsheet is manual, prone to errors, and does not integrate with AWS billing APIs; it requires continuous updates and reconciliation and therefore increases operational overhead and risk for multi-account or multi-team environments.  
C. Use an Amazon DynamoDB table to record costs for each business unit.

#### Explications

Storing cost data in Amazon DynamoDB would require building custom data collection, ETL, and reporting pipelines against AWS billing APIs or CUR, increasing development and maintenance work compared with using AWS-native cost management features.  
D. Use the AWS Billing console to assign owners to resources and track costs.

#### Explications

The AWS Billing console displays costs but cannot by itself assign owners or split costs by business unit; meaningful separation requires either separate accounts or consistently applied cost-allocation tags/cost categories, which introduce governance overhead.  
Explication générale  
Creating one AWS account per business unit under AWS Organizations gives clear, enforced cost boundaries with consolidated billing and minimal operational effort. Built-in tools (Cost Explorer, CUR, Budgets) can report per-account costs directly. Alternatives such as spreadsheets or custom databases require manual work and maintenance, while relying solely on the Billing console requires additional tagging or governance to achieve the same separation.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 109Correct  
Which of the following is a benefit of using the AWS Cloud?  
**Votre réponse est correcte**  
A. On-demand self-service

#### Explications

On-demand self-service allows customers to provision compute, storage, and networking resources immediately through the AWS Management Console, APIs, or CLI without requiring interaction with a human service provider. This capability supports rapid deployment, elasticity, and operational agility—core cloud characteristics that reduce time-to-market and enable scalable, on‑demand workloads.  
B. Limited scalability

#### Explications

‘Limited scalability’ is incorrect. AWS is designed to provide virtually unlimited scalability using features such as Auto Scaling, Elastic Load Balancing, and serverless services (for example, AWS Lambda), which let capacity grow or shrink to match demand.  
C. High upfront hardware costs

#### Explications

‘High upfront hardware costs’ is incorrect. AWS follows a pay-as-you-go model that reduces capital expenditures by eliminating the need to purchase and maintain on‑premises hardware; customers pay for resources they consume and can opt for pricing models (e.g., Savings Plans, Reserved Instances) to lower long‑term costs.  
D. Manual resource management

#### Explications

‘Manual resource management’ is incorrect. AWS promotes automation and managed services to reduce manual operations—examples include AWS CloudFormation, AWS Systems Manager, Elastic Beanstalk, and many managed AWS services—improving operational efficiency and consistency.  
Explication générale  
The question targets a fundamental cloud concept: on‑demand self‑service. AWS enables users to provision resources instantly via console/APIs/CLI without human intervention, delivering elasticity and faster deployments. The other choices describe drawbacks of traditional on‑premises models (limited scalability, high upfront costs, manual management) and therefore are not benefits of using the AWS Cloud.  
Domaine  
Domain 1: Cloud Concepts  
Question 110Correct  
A company needs to block SQL injection attacks. Which AWS service or feature provides this functionality?  
**Votre réponse est correcte**  
A. AWS WAF

#### Explications

Provides Layer‑7 (HTTP/S) inspection via web ACLs and rule statements (including SQLi match statements). AWS Managed Rule groups include SQL injection protections and you can attach the WAF to CloudFront, an Application Load Balancer, or API Gateway to block malicious requests before they reach the application.  
B. Network ACLs

#### Explications

Stateless, subnet‑level filters that allow/deny traffic based on IP, port, and protocol only. They do not inspect application‑layer payloads or HTTP content, so they cannot detect or block SQL injection.  
C. Security groups

#### Explications

Stateful VPC instance‑level firewall that controls allowed ports and protocols on ENIs. It does not parse HTTP requests or inspect application payloads and therefore cannot identify SQL injection attempts.  
D. AWS Trusted Advisor

#### Explications

A best‑practice advisory service that runs checks and gives recommendations; it does not perform runtime traffic inspection or block web attacks, so it cannot stop SQL injection in real time.  
Explication générale  
Blocking SQL injection requires application‑layer (Layer‑7) inspection and rule logic that can identify malicious patterns in HTTP requests. The AWS Web Application Firewall offers web ACLs, SQLi match statements and managed rule groups to detect and block SQL injection at the edge or at the application endpoint. Network ACLs and security groups operate at lower network layers and only enforce IP/port/protocol rules; Trusted Advisor provides guidance but does not block traffic.  
Domaine  
Domain 2: Security and Compliance  
Question 111Correct  
Which of the following best describes the shared responsibility model in AWS cloud security?  
**Votre réponse est correcte**  
A. AWS manages security \*of\* the cloud infrastructure, while the customer manages security \*in\* the cloud.

#### Explications

AWS is responsible for securing the cloud infrastructure itself — the physical facilities, hardware, network, and foundational services — while customers are responsible for their data, applications, guest operating systems, identity and access management, and configuration of security controls. This distinction is central to the AWS "security of the cloud" vs "security in the cloud" model and varies by service type (IaaS vs managed services).  
B. AWS handles all security responsibilities for the customer, including data encryption and user access management.

#### Explications

Cela surestime la responsabilité d'AWS. AWS fournit des fonctionnalités de sécurité (primitives de chiffrement, IAM, services de clés gérés), mais ne configure ni ne gère les données, les politiques d'accès ou le chiffrement au niveau applicatif de ses clients ; il incombe à ces derniers de mettre en œuvre et de gérer ces contrôles.  
C. Les clients sont responsables de toutes les mesures de sécurité, y compris la sécurité physique des centres de données.

#### Explications

La sécurité physique des centres de données (installations, contrôles d'accès physiques, infrastructure réseau et d'hébergement) est gérée par AWS. Les clients n'ont aucun contrôle sur la sécurité physique et doivent se concentrer sur les contrôles logiques tels que le renforcement de la sécurité du système d'exploitation, l'application de correctifs et la sécurité des applications.  
D. Les responsabilités en matière de sécurité sont partagées à parts égales entre AWS et le client pour tous les aspects de la sécurité du cloud.

#### Explications

Les responsabilités ne sont pas réparties à parts égales (50/50) pour chaque contrôle. Le modèle définit quelle partie gère quels contrôles et cette répartition peut varier selon le modèle de service (par exemple, les services gérés réduisent les responsabilités du client). Affirmer qu'elles sont partagées de manière égale est inexact et trompeur.  
Explication générale  
Le modèle de responsabilité partagée distingue les obligations d'AWS en matière de protection de l'infrastructure cloud sous-jacente de celles du client en matière de sécurité de ses charges de travail exécutées sur cette infrastructure. AWS gère les hôtes physiques, le réseau et les services fondamentaux ; les clients gèrent la protection des données, la gestion des identités et des accès (IAM), la configuration et la sécurité des applications et du système d'exploitation. Les autres options sont incorrectes car elles attribuent soit toutes les responsabilités à AWS, soit imposent aux clients des tâches physiques impossibles à réaliser, soit présentent une répartition erronée des responsabilités entre les différents types de services.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 112Correct  
Quelle perspective du cadre d'adoption du cloud AWS (AWS CAF) aborde la capacité de gestion stratégique ?  
**Votre réponse est correcte**  
A. Perspective commerciale

#### Explications

Cette perspective CAF est responsable de la capacité de gestion stratégique : elle définit les moteurs et les objectifs commerciaux de l’adoption du cloud, crée des analyses de rentabilité, priorise les investissements et établit des indicateurs/KPI pour mesurer la création de valeur et l’alignement avec les objectifs organisationnels.  
B. Perspective des personnes

#### Explications

Elle se concentre sur la transformation organisationnelle, les rôles, les compétences, les modèles de dotation en personnel et la formation pour faciliter l'adoption du cloud. Elle aborde le développement des personnes, de la culture et des compétences plutôt que la définition de la stratégie d'entreprise ou des priorités d'investissement.  
C. Perspective de gouvernance

#### Explications

Elle se concentre sur les politiques, les pouvoirs de décision, la gestion des risques, la conformité et les cadres de contrôle afin de garantir une utilisation cohérente et auditable des ressources cloud. La gouvernance soutient la supervision et les contrôles, mais ne relève pas de la formulation de la stratégie ni de la priorisation des analyses de rentabilité.  
D. Perspective des opérations

#### Explications

Ce document décrit les processus opérationnels nécessaires au fonctionnement et à la maintenance des environnements cloud : gestion des services, réponse aux incidents, surveillance et procédures opérationnelles. Il traite de l’exécution quotidienne et non de la gestion stratégique de haut niveau.  
Explication générale  
The AWS Cloud Adoption Framework maps business- and technical-focused capabilities to perspectives. The strategy-management capability belongs to the Business perspective because it defines business drivers, builds business cases, prioritizes cloud investments, and sets success metrics. The People, Governance, and Operations perspectives address organizational change, policy/control, and run‑time operations respectively, so they are not the primary owners of strategy management.  
Domaine  
Domain 1: Cloud Concepts  
Question 113Correct  
Which AWS service is used to track, record, and audit configuration changes made to AWS resources?  
A. AWS Shield

#### Explications

AWS Shield is a service focused on protecting applications from Distributed Denial of Service (DDoS) attacks (Standard and Advanced offerings). It provides network-layer and application-layer DDoS mitigation and reporting, but it does not provide a resource inventory, configuration snapshots, or a continuous audit trail of configuration changes.  
**Votre réponse est correcte**  
B. AWS Config

#### Explications

AWS Config continuously records configuration items and changes for supported AWS resources, stores configuration snapshots and a history of configuration items (typically in S3), and enables compliance evaluation via AWS Config Rules and conformance packs. It is specifically designed to provide a timeline of resource configuration states for auditing, troubleshooting, and compliance.  
C. AWS IAM

#### Explications

AWS Identity and Access Management (IAM) handles authentication, authorization, users, groups, roles, and policies. It controls who can do what in an account but does not capture full resource configuration histories or provide configuration auditing (CloudTrail logs IAM API calls but is not a configuration-state recorder).  
D. Amazon Inspector

#### Explications

Amazon Inspector is an automated security assessment service that analyzes the configuration and behavior of compute resources to find vulnerabilities and deviations from best practices. It produces findings about security posture but does not record or maintain a timeline of resource configuration changes for auditing purposes.  
Explication générale  
The question assesses which AWS service is intended for tracking and auditing resource configuration changes. AWS Config is the purpose-built service that records configuration items, maintains change histories, supports compliance checks (Config Rules), and stores configuration snapshots for audit and troubleshooting. Other services mentioned perform different roles—Shield for DDoS protection, IAM for access control, Inspector for vulnerability assessment, and CloudTrail for API activity logging—but none provide the continuous configuration-state recording and compliance evaluation that AWS Config offers.  
Domaine  
Domain 2: Security and Compliance  
Question 114Correct  
Which of the following best describes the benefit of using AWS Well-Architected Framework when designing cloud solutions?  
A. It provides a set of best practices for cost management only.

#### Explications

Incorrect. Le cadre AWS Well-Architected ne se limite pas à un seul sujet ; il définit un large ensemble de principes de conception et de bonnes pratiques organisés en cinq piliers (excellence opérationnelle, sécurité, fiabilité, efficacité des performances et optimisation des coûts) utilisés pour évaluer et améliorer les architectures.  
**Votre réponse est correcte**  
B. Elle propose une approche structurée pour évaluer et améliorer les architectures cloud en s'appuyant sur les meilleures pratiques réparties en cinq piliers.

#### Explications

Exact. Le cadre fournit une méthodologie d'examen structurée (et des outils via l'outil AWS Well-Architected et ses lentilles) pour identifier les risques, prioriser les mesures correctives et guider les améliorations itératives à travers les cinq piliers, aidant ainsi les équipes à concevoir des systèmes résilients, sécurisés, efficaces et soucieux des coûts.  
C. C'est un outil qui optimise automatiquement vos ressources AWS pour réaliser des économies.

#### Explications

Incorrect. Le Framework est un guide et un processus d'évaluation, et non un optimiseur automatisé. AWS propose d'autres services de recommandations automatisées et de dimensionnement adapté (par exemple, AWS Compute Optimizer, Trusted Advisor et Cost Explorer), qui effectuent des analyses et suggèrent des actions, mais le Framework d'architecture bien conçue fournit des principes et des flux de travail d'évaluation plutôt qu'une optimisation automatique des ressources.  
D. Elle garantit que votre solution cloud sera exempte de failles de sécurité.

#### Explications

Incorrect. Le cadre de référence prescrit les meilleures pratiques de sécurité et aide à identifier les risques, mais il ne garantit pas l'absence de vulnérabilités. Les résultats en matière de sécurité dépendent de la mise en œuvre des contrôles et du modèle de responsabilité partagée entre AWS et le client.  
Explication générale  
Le cadre AWS Well-Architected propose une approche structurée et fondée sur des principes pour évaluer et améliorer les architectures cloud selon cinq piliers : excellence opérationnelle, sécurité, fiabilité, performance et optimisation des coûts. Il s'agit d'un processus d'analyse et d'amélioration (assisté par l'outil Well-Architected et ses outils d'analyse), et non d'un optimiseur automatisé ni d'une garantie de sécurité. Le choix judicieux de ce cadre met l'accent sur son rôle dans l'évaluation structurée et l'amélioration continue.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 115Correct  
Quels sont les avantages de l'adoption du cloud AWS ? (Choisissez deux réponses.)  
A. Augmentation des dépenses d'investissement

#### Explications

Incorrect. AWS permet de passer des dépenses d'investissement aux dépenses d'exploitation grâce à une tarification à l'usage et à un provisionnement à la demande, évitant ainsi d'importants achats initiaux de serveurs et de matériel de centre de données.  
**Votre sélection est correcte**  
B. Évolutivité et flexibilité

#### Explications

Exact. AWS fournit des ressources de calcul et de stockage élastiques à la demande (EC2 Auto Scaling, AWS Lambda, ELB, S3/EBS) et une infrastructure mondiale (régions et zones de disponibilité), permettant une mise à l'échelle rapide et une flexibilité architecturale pour répondre à l'évolution de la demande.  
C. Options de déploiement limitées

#### Explications

Incorrect. AWS offre un large éventail de choix de déploiement à travers les régions, les zones de disponibilité, les options hybrides (AWS Outposts, zones locales) et les dispositifs edge/Snow ; les options de déploiement sont donc vastes et non limitées.  
**Votre sélection est correcte**  
D. Complexité opérationnelle réduite

#### Explications

Correct. AWS reduces operational complexity by managing physical infrastructure and offering managed services (RDS, DynamoDB, ECS/EKS/Fargate), automated scaling, patching, and monitoring (CloudWatch), allowing customers to focus on applications.  
E. Higher upfront costs

#### Explications

Incorrect. The AWS pay-as-you-go model minimizes upfront costs; while Savings Plans or Reserved Instances require commitments to obtain lower rates, they are cost-optimization tools rather than evidence of inherently higher upfront costs.  
Explication générale  
The primary cloud benefits tested here are scalability/flexibility and reduced operational complexity: AWS delivers on-demand, elastic resources and managed services that let organizations scale quickly and offload infrastructure management. The incorrect options confuse cloud economics and deployment breadth—AWS emphasizes OPEX-based pricing, broad global and hybrid deployment options, and cost-optimization features rather than increased capital or upfront costs.  
Domaine  
Domain 1: Cloud Concepts  
Question 116Correct  
Which option is an AWS Cloud Adoption Framework (AWS CAF) platform perspective capability?  
**Votre réponse est correcte**  
A. Data architecture

#### Explications

Designing how data is stored, ingested, processed, and exposed as platform services — including choices for object and block storage, data lakes, ETL, schemas, and integration with AWS services (Amazon S3, AWS Glue, Amazon Redshift, Amazon RDS) — is a Platform-perspective capability because it defines platform-level architectures and services that enable application workloads to operate at scale and be managed consistently.  
B. Data protection

#### Explications

Incorrect — this capability belongs to the Security perspective. It focuses on protecting data through encryption, key management, access controls, backup and recovery, and monitoring (e.g., AWS KMS, IAM policies, AWS Backup), rather than on designing platform-level data architectures.  
C. Data governance

#### Explications

Incorrect — this is a Governance-perspective capability. It covers policies, ownership, compliance, data lifecycle management, and stewardship (using tools like AWS Organizations, AWS Config, and tagging strategies) rather than the technical design of the platform.  
D. Data science

#### Explications

Incorrect — this describes analytics and ML activities (insight generation and model development) that align with business and people/organizational goals, using services like Amazon SageMaker, rather than platform engineering responsibilities.  
Explication générale  
The AWS CAF Platform perspective addresses the technical components required to build and operate a cloud platform that supports workloads. The correct choice is the capability that concerns designing platform-level data systems and integrations (storage, processing, ETL, and managed data services). The other options map to different CAF perspectives: data protection to Security, governance to Governance, and analytics/ML activities to Business/People-focused perspectives.  
Domaine  
Domain 1: Cloud Concepts  
Question 117Incorrect  
A company's application is running on Amazon EC2 instances. The company is planning a partial migration to a serverless architecture in the next year and wants to pay for resources up front. Which AWS purchasing option will optimize the company's costs?  
A. Convertible Reserved Instances

#### Explications

These are a form of Reserved Instance that let you alter instance attributes (family, OS, tenancy) during the term and provide discounted EC2 capacity for 1–3 year commitments. They only apply to EC2 instances and therefore do not provide cost coverage for serverless compute (Lambda, Fargate) during a partial migration.  
**Votre réponse est incorrecte**  
B. Spot Instances

#### Explications

This purchasing model provides access to spare EC2 capacity at steep discounts but with possible interruption and no guarantee of continuity. It is intended for fault‑tolerant or batch workloads and is not suitable for predictable, upfront-paid commitments or for ensuring cost coverage during a staged move to serverless.  
C. EC2 Instance Savings Plans

#### Explications

This commitment-based discount applies only to EC2 instance usage and offers lower rates when you commit to a usage amount. Because it does not apply to Lambda or Fargate, it cannot protect or optimize costs for serverless resources as the company migrates away from EC2.  
**Bonne réponse**  
D. Compute Savings Plan

#### Explications

A Savings Plan that lets you commit to a consistent hourly spend (1- or 3-year terms, with All Upfront/Partial/No Upfront payment options) and automatically applies discounted rates across multiple compute services (EC2, AWS Lambda, and Fargate). This multi-service coverage plus upfront payment ability makes it the best fit for optimizing costs during a partial migration to serverless.  
Explication générale  
The question tests knowledge of AWS compute purchasing options and which provide multi-service coverage. The Compute Savings Plan is the best choice because it allows an upfront commitment and delivers discounts across EC2, Lambda, and Fargate, aligning with a phased migration from EC2 to serverless. The other options either only cover EC2, are interruptible, or lack cross-service applicability.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 118Correct  
Which of the following best describes the benefit of adopting a pay-as-you-go pricing model for AWS services?  
A. It allows organizations to predict their costs accurately over a fixed period.

#### Explications

Incorrect — pay-as-you-go pricing bills based on actual consumption, so costs vary with usage and are not inherently fixed or precisely predictable over a set period. Organizations that need predictable, lower-cost commitments use Reserved Instances or Savings Plans, and rely on tools like AWS Cost Explorer and AWS Budgets for forecasting and control.  
**Votre réponse est correcte**  
B. It enables organizations to pay only for the resources they consume, which can lead to cost savings and flexibility.

#### Explications

Tout à fait exact : le modèle de paiement à l’usage (à la demande) facture la consommation réelle de ressources sans engagement à long terme, ce qui permet une mise à l’échelle flexible et des dépenses d’investissement réduites. Amazon EC2 On-Demand, AWS Lambda (facturé par invocation et par durée) et S3 (facturé par Go et par mois) en sont des exemples, ce qui rend ce modèle rentable pour les charges de travail variables ou imprévisibles.  
C. Cela nécessite un investissement initial important, ce qui réduit les coûts globaux à long terme.

#### Explications

Incorrect — cette description décrit une approche tarifaire nécessitant d'importants investissements initiaux. Le paiement à l'utilisation ne requiert aucun investissement initial conséquent ; en revanche, les instances réservées et les plans d'épargne exigent des engagements ou des paiements initiaux pour obtenir des prix unitaires inférieurs.  
D. Elle garantit les prix les plus bas possibles, quelle que soit l'utilisation.

#### Explications

Incorrect — le paiement à l'utilisation ne garantit pas le prix le plus bas dans tous les cas. Des coûts effectifs inférieurs peuvent être obtenus avec les instances réservées, les plans d'épargne ou les instances ponctuelles (moins chères mais interrompables). Le paiement à l'utilisation privilégie la flexibilité aux réductions les plus importantes.  
Explication générale  
La facturation à l'usage (à la demande) permet aux clients de ne payer que ce qu'ils consomment, offrant ainsi évolutivité, flexibilité opérationnelle et réduction des dépenses d'investissement initiales ; elle est donc idéale pour les charges de travail variables. Pour des coûts prévisibles ou des prix unitaires plus bas, AWS propose d'autres modèles de tarification (instances réservées, plans d'économies, Spot) et des outils de prévision (Cost Explorer, Budgets).  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 119Incorrect  
Une entreprise exécute sa charge de travail de production sur le cloud AWS. Elle doit choisir un plan de support AWS. Lequel répondra à ses exigences au coût le plus bas ?  
A. Développeur

#### Explications

L'assistance aux développeurs est l'offre la plus économique, mais elle est conçue pour les environnements de développement et de test. Elle propose une assistance au mieux pendant les heures ouvrables et des vérifications limitées par un conseiller de confiance. Elle ne donne pas accès à une assistance 24 h/24 et 7 j/7 aux ingénieurs du support cloud ni aux fonctionnalités de production nécessaires aux charges de travail de production prises en charge.  
B. Rampe d'accès aux entreprises

#### Explications

L'offre Enterprise On-Ramp est conçue pour permettre aux organisations d'accéder à certaines fonctionnalités de support de type entreprise pendant leur croissance, mais elle se positionne au-dessus de l'offre Business en termes de capacités et de coût. Ce n'est pas l'option la plus économique qui réponde aux exigences de support pour les charges de travail de production.  
**Votre réponse est incorrecte**  
C. Entreprise

#### Explications

L'assistance aux entreprises offre l'ensemble de services le plus complet (y compris un gestionnaire de compte technique et un support consultatif de niveau entreprise) et est destinée aux charges de travail critiques ; comme il s'agit du niveau le plus coûteux, il ne répond pas à l'exigence d'être le plan le moins cher pour les charges de travail de production.  
**Bonne réponse**  
D. Affaires

#### Explications

Le support Business est le niveau de support AWS minimum recommandé pour les charges de travail de production : il offre un accès 24 h/24 et 7 j/7 aux ingénieurs du support cloud (téléphone/chat/e-mail), des temps de réponse plus rapides et l’ensemble des vérifications Trusted Advisor, ainsi qu’une prise en charge des logiciels tiers, fournissant un support de niveau production à un coût inférieur aux offres destinées aux entreprises.  
Explication générale  
Pour vos charges de travail en production, vous avez besoin d'un plan de support offrant un accès 24h/24 et 7j/7 à des ingénieurs de support cloud, des délais de réponse adaptés à la production et des contrôles complets Trusted Advisor. Le support Business est le plan le plus économique répondant à ces exigences. Le support Developer est moins cher, mais destiné à un usage hors production ; les plans Enterprise et Enterprise On-Ramp offrent davantage de fonctionnalités pour les entreprises, à un coût plus élevé.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 120Incorrect  
Quelles actions illustrent les efforts déployés par une entreprise pour adapter ses ressources AWS afin de maîtriser ses coûts cloud ? (Choisissez deux réponses.)  
A. Passez d'Amazon RDS à Amazon DynamoDB pour prendre en charge les ensembles de données NoSQL.

#### Explications

Cela décrit la migration vers un paradigme de base de données différent. Passer à un modèle de données différent peut parfois réduire les coûts si le nouveau service correspond mieux aux caractéristiques de la charge de travail, mais il s'agit d'une migration architecturale plutôt que d'une simple optimisation des ressources, ce qui peut engendrer de nouveaux coûts d'exploitation ou de développement.  
**Sélection correcte**  
B. Basez la sélection des types d'instances Amazon EC2 sur les modèles d'utilisation antérieurs.

#### Explications

Le choix des types d'instances en fonction de l'historique d'utilisation s'appuie sur des métriques (CloudWatch) et des recommandations (AWS Compute Optimizer, Cost Explorer) pour adapter la capacité du processeur, de la mémoire et des E/S à la demande. Cela permet de réduire le surdimensionnement et de diminuer directement les dépenses EC2 en optant pour des familles d'instances ou des tailles plus petites ou plus adaptées.  
**Votre sélection est correcte**  
C. Utilisez les politiques de cycle de vie Amazon S3 pour déplacer les objets auxquels les utilisateurs accèdent rarement vers des niveaux de stockage moins coûteux.

#### Explications

La migration des objets vers des classes de stockage S3 moins coûteuses via des politiques de cycle de vie (par exemple, Standard → Standard-IA → Glacier) permet de réduire les frais de stockage récurrents pour les données rarement consultées. Les transitions de cycle de vie automatisées constituent une technique courante d'optimisation des coûts de stockage.  
D. Utilisez des déploiements multi-AZ pour Amazon RDS.

#### Explications

Le déploiement de ressources pour une haute disponibilité (Multi-AZ) accroît la redondance et la résilience en créant des copies supplémentaires ou des instances de basculement. Cela améliore la tolérance aux pannes, mais augmente généralement les coûts ; il ne s’agit donc pas d’une mesure d’optimisation visant à réduire les dépenses.  
**Votre sélection est incorrecte**  
E. Remplacez les instances Amazon EC2 existantes par AWS Elastic Beanstalk.

#### Explications

L'adoption d'une plateforme de services peut simplifier le déploiement et la gestion, mais ne réduit pas automatiquement la taille des ressources ni les coûts. Les choix sous-jacents en matière de calcul et de mise à l'échelle déterminent toujours les dépenses ; il ne s'agit donc pas d'un exemple direct d'optimisation des ressources.  
Explication générale  
Le dimensionnement optimal consiste à adapter la capacité des ressources et les niveaux de service aux besoins réels en matière de charge de travail afin d'éviter le surdimensionnement et de réduire les coûts. L'utilisation des données d'utilisation et des outils d'optimisation AWS pour choisir les types d'instances EC2 appropriés (B) et le déplacement des données rarement consultées vers des classes de stockage S3 moins coûteuses, avec des politiques de cycle de vie (C), sont des mesures directes de dimensionnement optimal. Les autres options décrivent des migrations architecturales ou des améliorations de la disponibilité qui ne visent pas principalement à réduire la capacité allouée ou les coûts de stockage.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
