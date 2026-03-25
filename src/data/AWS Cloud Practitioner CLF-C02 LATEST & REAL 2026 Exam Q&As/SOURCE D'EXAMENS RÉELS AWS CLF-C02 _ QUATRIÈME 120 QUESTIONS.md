Question 1Correct  
Une entreprise migre son centre de données sur site vers le cloud AWS. Elle doit transférer 50 pétaoctets de données de stockage de fichiers vers AWS en minimisant les coûts opérationnels. Quel service ou ressource AWS doit-elle utiliser pour répondre à ces exigences ?  
**Votre réponse est correcte**  
A. Motoneige AWS

#### Explications

AWS Snowmobile est un service de transport physique de données à grande échelle spécialement conçu pour déplacer de très grands ensembles de données directement vers Amazon S3. Il minimise les coûts opérationnels du client en fournissant un conteneur et un camion sécurisés, avec une logistique gérée par AWS, un chiffrement de bout en bout, une chaîne de traçabilité et une ingestion directe dans S3 — évitant ainsi la nécessité de coordonner des centaines de petits appareils ou des transferts réseau prolongés pour les migrations de plusieurs pétaoctets.  
B. AWS Snowball Edge

#### Explications

AWS Snowball Edge sont des appliances périphériques portables pour le transfert de données hors ligne et le calcul en périphérie. Chaque appareil a une capacité de l'ordre de plusieurs dizaines de téraoctets ; migrer 50 Po nécessiterait donc d'orchestrer et de gérer de nombreux appareils sur une période prolongée, ce qui augmenterait la complexité opérationnelle par rapport à une seule livraison de Snowmobile.  
C. Échange de données AWS

#### Explications

AWS Data Exchange est une plateforme permettant de découvrir, de s'abonner et de distribuer des produits de données tiers au sein d'AWS. Il ne s'agit pas d'un mécanisme de migration physique du stockage de fichiers sur site d'une organisation vers AWS.  
D. Service de migration de bases de données AWS (AWS DMS)

#### Explications

AWS Database Migration Service est conçu pour migrer et répliquer des bases de données (relationnelles, NoSQL et entrepôts de données). Il n'est pas destiné à la migration en masse de volumes importants de données de systèmes de fichiers à usage général.  
Explication générale  
Pour migrer 50 pétaoctets de données avec un minimum de surcharge opérationnelle, un transfert physique géré par AWS est nécessaire. Snowmobile est spécifiquement conçu pour déplacer des dizaines, voire des centaines de pétaoctets, vers Amazon S3, tandis qu'AWS prend en charge la logistique, la sécurité et l'ingestion. Les autres solutions fonctionnent soit à des échelles beaucoup plus réduites (Snowball Edge), soit ciblent la réplication de bases de données (DMS), soit sont destinées à la distribution de données par des tiers (Data Exchange), ce qui les rend inadaptées à cette échelle et à ce cas d'utilisation.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 2Correct  
Une entreprise souhaite migrer vers AWS et utiliser le même logiciel de sécurité qu'elle utilise sur site. L'éditeur du logiciel de sécurité propose son logiciel en tant que service (SaaS) sur AWS. Où l'entreprise peut-elle acquérir cette solution de sécurité ?  
A. Recherche de solutions partenaires AWS

#### Explications

Ce service est un outil de découverte répertoriant les partenaires du réseau AWS Partner Network (APN) et leurs solutions pour évaluation et prise de contact ; il ne s'agit pas du canal de commerce/catalogue AWS utilisé pour s'abonner et acheter des logiciels SaaS tiers.  
B. Centre de support AWS

#### Explications

Cette zone est destinée à la gestion des plans de support AWS et à la création de demandes de support (facturation, technique, support de compte) et ne fonctionne pas comme une place de marché ou une plateforme d'achat de logiciels tiers.  
C. Console de gestion AWS

#### Explications

L'interface web permettant de gérer les ressources AWS et d'accéder aux services peut être utilisée pour accéder à d'autres services (y compris Marketplace), mais ne constitue pas en elle-même le catalogue/service de commerce permettant d'acheter des abonnements SaaS.  
**Votre réponse est correcte**  
D. Place de marché AWS

#### Explications

Il s'agit du catalogue de commerce AWS qui permet aux clients de découvrir, de s'abonner et d'acquérir des logiciels tiers et des solutions SaaS intégrées à AWS ; il prend en charge les options d'abonnement/de licence, la facturation consolidée sur votre compte AWS et les flux de travail automatisés de provisionnement ou de déploiement lorsqu'ils sont proposés, ce qui en fait le canal d'approvisionnement approprié.  
Explication générale  
Cette question évalue vos connaissances des canaux d'approvisionnement AWS pour les logiciels de sécurité tiers proposés en mode SaaS sur AWS. Le service d'approvisionnement/catalogue approprié assure le référencement, la gestion des abonnements et l'intégration de la facturation avec votre compte AWS ; les répertoires de découverte, les outils de gestion des demandes d'assistance et la console d'administration générale ne proposent pas ces fonctionnalités d'achat et d'abonnement.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 3Correct  
Une entreprise possède une flotte de cargos. Ces navires sont équipés de capteurs qui collectent des données en mer, où la connexion internet est intermittente ou inexistante. L'entreprise doit collecter, formater et traiter ces données directement en mer, puis les transférer vers AWS. Quel service AWS l'entreprise doit-elle utiliser pour répondre à ces exigences ?  
A. AWS IoT Core

#### Explications

AWS IoT Core est un service cloud géré permettant de connecter et d'ingérer en toute sécurité les données de télémétrie des appareils vers le cloud AWS. Il suppose une connectivité réseau pour l'envoi des messages vers le cloud et ne fournit ni appliance physique robuste et autonome, ni flux de travail de transfert de données hors ligne en masse requis pour les périodes prolongées sans connexion Internet.  
B. Voile lumineuse Amazon

#### Explications

Amazon Lightsail est un service d'hébergement cloud simplifié (serveurs virtuels, conteneurs, bases de données) permettant d'exécuter des applications de petite taille sur AWS. Il ne propose ni matériel physique sur site, ni stockage renforcé, ni fonctionnalités intégrées d'import/export de données hors ligne nécessaires à la collecte et au transport de données de capteurs embarqués sur des navires en mer.  
C. Passerelle de stockage AWS

#### Explications

AWS Storage Gateway fournit des appliances virtuelles et une mise en cache permettant d'intégrer le stockage sur site à AWS (interfaces de fichiers, de volumes ou de bandes) et de transférer des données vers AWS de manière asynchrone. Conçu pour les sites sur site connectés au réseau et s'appuyant sur cette connectivité pour la synchronisation des données, il n'est pas destiné à être utilisé comme dispositif physique de collecte de données hors ligne pour les navires distants.  
**Votre réponse est correcte**  
D. AWS Snowball Edge

#### Explications

AWS Snowball Edge est un appareil physique robuste (famille Snow) doté d'un important espace de stockage local chiffré et d'une capacité de calcul locale (compatible avec les instances EC2 et Lambda). Il permet la collecte de données sur site, le traitement en périphérie et le transport hors ligne sécurisé des données, ou leur transfert ultérieur vers AWS, ce qui le rend idéal pour les environnements où la connectivité Internet est intermittente ou inexistante.  
Explication générale  
Il est nécessaire de disposer d'une solution permettant la collecte, le formatage et le traitement locaux des données de capteurs dans un environnement à connectivité intermittente ou inexistante, ainsi que leur transfert ultérieur vers AWS. Snowball Edge propose un dispositif physique robuste doté d'un stockage local chiffré et d'une puissance de calcul en périphérie pour le traitement et le transfert hors ligne sécurisé — des fonctionnalités que les autres options (IoT Core, Lightsail, Storage Gateway) ne proposent pas en tant que solutions autonomes dans les environnements maritimes déconnectés.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 4Correct  
A company is running a critical workload on an Amazon RDS DB instance. The company needs the DB instance to be highly available with a recovery time of less than 5 minutes. Which solution will meet these requirements?  
A. Create a read replica of the DB instance.

#### Explications

Incorrect. Read replicas provide read scalability and can be promoted to a standalone DB, but they are not automatically maintained as synchronous failover targets by Amazon RDS. Promotion is a manual or orchestrated process and does not provide the automatic, low-RTO failover required for high availability.  
B. Create a template of the DB instance by using AWS CloudFormation.

#### Explications

Incorrect. AWS CloudFormation templates automate provisioning and deployment, but creating a template of an existing DB does not provide automatic failover or a standby replica. Infrastructure-as-code helps reproducibility and recovery automation, but it does not by itself meet an RTO under 5 minutes for a running production DB instance.  
C. Take frequent snapshots of the DB instance. Store the snapshots in Amazon S3.

#### Explications

Incorrect. Snapshots (manual or automated backups) protect data and enable point-in-time restores, but restoring from a snapshot involves creating a new DB instance and data rehydration, which typically takes longer than a few minutes and does not provide automatic failover.  
**Votre réponse est correcte**  
D. Modify the DB instance to be a Multi-AZ deployment.

#### Explications

Correct. Multi‑AZ RDS configures a synchronous standby in a different Availability Zone and is managed by Amazon RDS. In the event of a failure, RDS automatically fails over to the standby endpoint, preserving the same DB endpoint and minimizing application downtime (failover typically completes within minutes), which meets the \<5 minute recovery objective.  
Explication générale  
The requirement is automatic high availability with very low recovery time. Amazon RDS Multi‑AZ deployments provide synchronous replication to a managed standby in another AZ and automatic failover to that standby, delivering the fast recovery behavior required. Read replicas, CloudFormation templates, and snapshots are useful for scaling, automation, and backup/recovery, but they do not offer the automated, low-RTO failover that Multi‑AZ does.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 5Incorrect  
A company wants to migrate its NFS on-premises workload to AWS. Which AWS Storage Gateway type should the company use to meet this requirement?  
A. Tape Gateway

#### Explications

Provides a virtual tape library for backup software and archives virtual tapes to Amazon S3 and Glacier. This gateway is intended for backup/archival workflows, not for exposing file-level NFS mounts or migrating active file shares.  
B. Volume Gateway

#### Explications

Exposes iSCSI block volumes (cached or stored) to on-premises hosts for block-level storage and snapshot/DR use cases. Because it provides block storage rather than a file protocol, it does not serve NFS file shares and is therefore not appropriate for migrating NFS workloads.  
**Votre réponse est incorrecte**  
C. Amazon FSx File Gateway

#### Explications

Il permet de connecter les clients locaux aux systèmes de fichiers gérés par Amazon FSx et s'utilise lorsque vous avez besoin des fonctionnalités offertes par les variantes de FSx (par exemple, les fonctionnalités de Windows Server ou de Lustre). Il est axé sur l'accès aux services FSx plutôt que sur l'interface NFS générale basée sur S3 utilisée pour les migrations simples de NFS vers des objets.  
**Bonne réponse**  
D. Passerelle de fichiers Amazon S3

#### Explications

Offre une interface de fichiers NFS (et SMB) aux applications sur site tout en conservant les fichiers sous forme d'objets dans Amazon S3. La mise en cache locale améliore les performances et les objets stockés héritent de la durabilité, des politiques de cycle de vie et des intégrations de S3, faisant de cette passerelle le choix idéal pour migrer les charges de travail de fichiers NFS vers AWS.  
Explication générale  
Ce test évalue vos connaissances sur les différents types de passerelles de stockage AWS et leurs cas d'utilisation. La passerelle de fichiers basée sur S3 expose une interface NFS native et stocke les données de fichiers sur Amazon S3, ce qui en fait la solution idéale pour migrer les charges de travail NFS sur site. Les autres passerelles répondent à des besoins différents : la passerelle de bande virtuelle pour les sauvegardes et l'archivage, la passerelle de volume pour le stockage au niveau bloc et les passerelles FSx pour l'accès à des systèmes de fichiers gérés spécifiques.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 6Correct  
Quelle directive constitue un principe de conception bien architecturé pour la création d'applications cloud ?  
A. Conservez les données statiques au plus près des ressources de calcul.

#### Explications

Cela décrit une optimisation des performances ou de la localité des données (prise en charge par des services comme Amazon CloudFront, la réplication S3, les zones locales), mais ce n'est pas l'un des principes de conception fondamentaux d'AWS Well-Architected qui mettent l'accent sur la résilience, l'automatisation et le couplage faible.  
B. Prévoir des ressources pour la capacité de pointe.

#### Explications

Le provisionnement pour une capacité maximale entraîne un surdimensionnement et des coûts plus élevés. Les bonnes pratiques AWS privilégient l'élasticité et la mise à l'échelle à la demande (par exemple, Auto Scaling, les architectures sans serveur et la tarification à l'usage) afin que les ressources correspondent à la demande plutôt que d'être dimensionnées pour les pics en permanence.  
**Votre réponse est correcte**  
C. Conception pour la récupération automatisée après une panne.

#### Explications

La conception de systèmes capables de se rétablir automatiquement après une panne est un principe fondamental du pilier Fiabilité du cadre AWS Well-Architected. Ce principe met l'accent sur l'automatisation et les modèles résilients (par exemple, les déploiements multi-AZ, la mise à l'échelle automatique, les contrôles d'intégrité, le basculement automatique et l'infrastructure en tant que code) afin que la reprise soit prévisible, reproductible et ne nécessite aucune intervention manuelle.  
D. Utilisez des composants étroitement couplés.

#### Explications

Un couplage fort accroît la fragilité et réduit la capacité d'évolution et de mise à l'échelle. AWS recommande un couplage faible et des modèles d'intégration asynchrones (par exemple, l'utilisation d'Amazon SQS, SNS, EventBridge ou de microservices) afin d'améliorer l'isolation des pannes et la scalabilité.  
Explication générale  
The question tests knowledge of AWS Well‑Architected design principles. The correct choice emphasizes automated recovery, which maps to the Reliability pillar and the practice of using automation and resilient architectures (Multi‑AZ, Auto Scaling, health checks, IaC) to minimize manual recovery. The other options describe performance optimizations, anti‑patterns (over‑provisioning), or coupling patterns that reduce resilience and are therefore not the recommended Well‑Architected guideline.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 7Correct  
A company wants to add a conversational chatbot to its website. Which AWS service can the company use to meet this requirement?  
A. Amazon Textract

#### Explications

Incorrect — Amazon Textract is an OCR and document-analysis service that extracts text, forms, and tables from scanned documents and returns structured data for downstream processing. It does not provide natural language understanding, intent detection, or dialog management required to implement a conversational chatbot.  
**Votre réponse est correcte**  
B. Amazon Lex

#### Explications

Correct — Amazon Lex provides automatic speech recognition (ASR) and natural language understanding (NLU) along with constructs for intents, utterances, slot filling, and dialog management. It can invoke AWS Lambda for fulfillment and is designed to be embedded into web and mobile applications, making it the appropriate service for building a website chatbot.  
C. AWS Glue

#### Explications

Incorrect — AWS Glue is a serverless extract-transform-load (ETL) and data catalog service used to prepare and move data for analytics. It does not offer conversational AI features such as intent recognition, dialog orchestration, or runtime user interaction handling.  
D. Amazon Rekognition

#### Explications

Incorrect — Amazon Rekognition provides image and video analysis (object, scene, facial detection/analysis) and related APIs. It does not include NLU, ASR, or dialog-management capabilities needed to create conversational chatbots.  
Explication générale  
The question assesses knowledge of AWS services for building conversational interfaces. Amazon Lex is the correct choice because it supplies ASR, NLU, intent/slot models, dialog management, and integration points (SDKs, Lambda) for embedding chatbots into websites. The other listed services focus on document processing (Textract), ETL/data preparation (Glue), or image/video analysis (Rekognition) and therefore lack the conversational primitives required for a chatbot.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 8Correct  
Which of the following is a fully managed MySQL-compatible database?  
A. Amazon S3

#### Explications

Object storage for storing and retrieving files and objects; it is not a database engine and does not provide SQL interfaces, relational features, or MySQL wire-protocol compatibility.  
B. Amazon DynamoDB

#### Explications

A fully managed NoSQL key-value and document database that scales horizontally and offers low-latency single-digit millisecond responses. It does not implement the MySQL protocol or provide a MySQL-compatible relational engine.  
C. Amazon Redshift

#### Explications

A managed, columnar, MPP data warehouse service optimized for analytics (OLAP). Its architecture and query engine are designed for large-scale analytics, not for MySQL-compatible transactional OLTP workloads.  
**Votre réponse est correcte**  
D. Amazon Aurora

#### Explications

A managed relational database engine that is wire-compatible with MySQL (and also offers a PostgreSQL-compatible edition). It provides automated backups, storage auto-scaling, high availability options, and MySQL protocol compatibility, making it the appropriate choice for a fully managed MySQL-compatible database.  
Explication générale  
The question assesses knowledge of AWS managed data services and which one provides MySQL compatibility. The correct service is the managed relational engine that offers MySQL wire-protocol compatibility, automated management features, and high availability. The other options are different service categories: object storage, NoSQL key-value/document database, and an analytic data warehouse, none of which provide a MySQL-compatible managed relational engine.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 9Correct  
A company is running big data analytics and massive parallel computations on its AWS test and development servers. The company can tolerate occasional downtime. What is the MOST cost-effective Amazon EC2 purchasing option for the company to use?  
A. On-Demand Instances

#### Explications

On-Demand Instances provide flexible, pay-as-you-go compute with no long-term commitment, making them appropriate for unpredictable or short-term workloads. They are not the most cost-effective choice for large, fault-tolerant parallel workloads because their per-hour/second price is higher than Spot pricing.  
**Votre réponse est correcte**  
B. Spot Instances

#### Explications

Spot Instances use spare EC2 capacity offered at steep discounts (often up to  
C. Reserved Instances

#### Explications

Reserved Instances (and RIs’ modern equivalents like capacity reservations) require a 1- or 3-year commitment in exchange for lower hourly rates. They are optimal for steady-state, predictable workloads where long-term capacity and cost savings are desired, not for highly interruptible, batch-style analytics that benefit most from ephemeral discounted capacity.  
D. Savings Plans

#### Explications

Savings Plans reduce cost by committing to a consistent $/hour spend for 1 or 3 years and are more flexible than classic Reserved Instances across instance families and regions. They target predictable compute spend and are not inherently suited to maximizing cost savings for workloads that intentionally accept interruptions — Spot pricing remains cheaper for those use cases.  
Explication générale  
For large-scale, parallel analytics that can tolerate occasional interruptions, the lowest-cost EC2 option is to use spare capacity rather than committed or on-demand capacity. Spot Instances provide deeply discounted compute suited to distributed, checkpointable jobs (with a two-minute interruption notice). On-Demand is more expensive, while Reserved Instances and Savings Plans require commitments and serve predictable, steady-state usage rather than interruptible batch processing.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 10Correct  
A company wants to store data in Amazon S3. The company rarely access the data, and the data can be regenerated if necessary. The company wants to store the data in the most cost-effective storage class. Which S3 storage class will meet this requirement?  
A. S3 Standard

#### Explications

Incorrect. S3 Standard is optimized for frequently accessed data and provides multi‑AZ redundancy and low latency; its higher per‑GB storage cost makes it a poor choice for rarely accessed, regenerable data where minimizing storage cost is the priority.  
B. S3 Intelligent-Tiering

#### Explications

Incorrect. S3 Intelligent‑Tiering automatically moves objects between access tiers to optimize cost for unpredictable access patterns, but it incurs a small monitoring/automation charge. For a predictable, infrequently accessed dataset that can be regenerated, a simpler, lower‑cost storage class (One Zone‑IA) is more economical.  
C. S3 Standard-Infrequent Access (S3 Standard-IA)

#### Explications

Incorrect. S3 Standard‑IA reduces storage cost compared with Standard while maintaining multi‑AZ resiliency, but that redundancy increases cost relative to One Zone‑IA. If cross‑AZ durability is not required and data can be recreated, the single‑AZ IA class is cheaper.  
**Votre réponse est correcte**  
D. S3 One Zone-Infrequent Access (S3 One Zone-IA)

#### Explications

Correct. S3 One Zone‑IA reduces storage costs by storing objects in a single Availability Zone, trading multi‑AZ redundancy for lower per‑GB pricing. This tradeoff is appropriate when data is infrequently accessed and can be regenerated if an AZ outage occurs. Be aware of retrieval charges and minimum storage duration requirements that still apply.  
Explication générale  
The question tests choosing the lowest‑cost S3 storage class for infrequently accessed data that can be regenerated. S3 One Zone‑IA is the best fit because it lowers storage cost by storing data in a single Availability Zone and is intended for infrequently accessed, non‑critical data. Other options are either designed for frequent access (Standard), for predictable infrequent access with cross‑AZ resilience (Standard‑IA), or for optimizing unknown access patterns (Intelligent‑Tiering), and therefore are more costly or unnecessary given the scenario.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 11Correct  
Which AWS Cloud benefit is shown by an architecture’s ability to withstand failures with minimal downtime?  
A. Agility

#### Explications

Refers to rapid provisioning, faster deployment cycles, and the ability to experiment and iterate (DevOps practices, Infrastructure as Code). That capability speeds delivery and adaptation but does not by itself provide mechanisms for surviving component failures or reducing downtime.  
B. Elasticity

#### Explications

Describes on-demand automatic scaling of resources (Auto Scaling, elastic load balancing) to match workload changes. Elasticity addresses capacity flexibility and cost efficiency, but it does not guarantee continuity when individual components or AZs fail unless combined with redundancy and failover design.  
C. Scalability

#### Explications

Concerns the ability to increase capacity (vertical or horizontal scaling) to handle larger workloads. Scalability ensures performance under growth but does not inherently provide redundancy, automatic failover, or multi‑AZ/regional continuity required to withstand failures with minimal downtime.  
**Votre réponse est correcte**  
D. High availability

#### Explications

Describes the architecture property that provides continuous service despite component or infrastructure failures by using redundancy, fault tolerance, and automated failover. In AWS this is achieved with patterns and services such as multi‑AZ/multi‑Region deployments, Elastic Load Balancers with health checks, Auto Scaling across AZs, RDS Multi‑AZ/failover replicas, Route 53 health checks/DNS failover, and designing for failure at every layer to meet availability SLAs.  
Explication générale  
The question tests recognition of the cloud benefit that emphasizes continuity of service in the face of failures. The correct choice is the property focused on minimizing downtime via redundancy and automatic failover (implemented in AWS using multi‑AZ/Region deployments, ELB/ALB, Auto Scaling, RDS Multi‑AZ, Route 53, etc.). The other choices describe related but different benefits: agility (faster change and deployment), elasticity (automatic scaling to match demand), and scalability (ability to grow capacity)—none of which alone guarantee resilience to failures.  
Domaine  
Domain 1: Cloud Concepts  
Question 12Correct  
Which AWS Cloud Adoption Framework (AWS CAF) perspective focuses on managing identities and permissions at scale?  
A. Operations

#### Explications

Focuses on running and operating deployed services: incident management, monitoring, runbooks, automation for resilience and availability (examples: CloudWatch, Systems Manager). This perspective addresses operational procedures and service management rather than centralized identity, authentication, or permission controls.  
B. Platform

#### Explications

Concerns the design and standardization of the technology stack, provisioning, and platform automation (examples: VPC design, compute and storage choices, infrastructure as code). Identity and access control are implementation details that sit with security practices rather than the platform strategy itself.  
C. Governance

#### Explications

Covers policy, risk, compliance, and decision-making frameworks (example: policies, organizational controls, audit and compliance requirements). It defines access policy objectives and governance requirements, but the technical implementation and day-to-day management of identities and permissions are handled under the security perspective and IAM services.  
**Votre réponse est correcte**  
D. Security

#### Explications

Responsible for identity, authentication, authorization, and access control at scale. This includes use of AWS Identity and Access Management (IAM), AWS Organizations, IAM Identity Center (SSO), roles, policies, permission boundaries, identity federation, key management, and audit logging (CloudTrail). The perspective defines controls, processes, and tooling to enforce least privilege, credential management, and access monitoring across the cloud environment.  
Explication générale  
AWS CAF organizes cloud adoption into perspectives. The question targets which perspective owns identity and permission management. The Security perspective is the correct choice because it defines and implements authentication, authorization, identity federation, and access controls using AWS IAM, Organizations, and related services. The other perspectives focus on operations (service management), platform (technology stack), or governance (policy and compliance), but do not own the technical controls for managing identities at scale.  
Domaine  
Domain 2: Security and Compliance  
Question 13Correct  
A company hosts a web application on AWS. The company has improved the availability of its application by provisioning multiple Amazon EC2 instances. The company wants to distribute its traffic across the EC2 instances while providing a single point of contact to the web clients. Which AWS service can distribute the traffic to multiple EC2 instances as targets?  
A. VPC endpoints

#### Explications

VPC endpoints provide private, direct connectivity between a VPC and supported AWS services (or endpoint services) without using the internet. They are a connectivity mechanism and do not perform request routing or distribute inbound client traffic across multiple EC2 instances.  
**Votre réponse est correcte**  
B. Application Load Balancer

#### Explications

This service functions as a front-end for HTTP/HTTPS traffic and distributes requests to groups of EC2 instances (targets). It includes health checks, supports path- and host-based routing, SSL termination, and evenly directs traffic only to healthy targets, making it the appropriate load-distribution solution for the scenario.  
C. NAT gateway

#### Explications

A NAT gateway performs source network address translation to allow instances in private subnets to initiate outbound internet connections. It is for outbound access only and does not accept or load-balance inbound web traffic to EC2 instances.  
D. Internet gateway

#### Explications

An internet gateway enables internet connectivity for a VPC by acting as a gateway for traffic between the VPC and the internet. It is not a load balancing service and does not distribute incoming requests among multiple EC2 instances.  
Explication générale  
The question tests knowledge of AWS services that provide a single entry point and distribute incoming client traffic to multiple EC2 instances. The correct choice is the application-layer load balancing service because it routes HTTP/HTTPS requests to target groups of EC2 instances, performs health checks, and provides advanced routing features. The other options (VPC endpoints, NAT gateway, internet gateway) are connectivity or address-translation components and do not provide load-balancing functionality.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 14Correct  
A company is setting up AWS Identity and Access Management (IAM) on an AWS account. Which recommendation complies with IAM security best practices?  
A. Use the account root user access keys for administrative tasks.

#### Explications

Incorrect — the AWS account root principal has unrestricted, account-level privileges. Best practice is to avoid using long-term root credentials for everyday administration: enable MFA on the root account, remove or disable root access keys if present, and create IAM users or IAM roles with narrowly scoped administrative permissions for daily tasks.  
B. Grant broad permissions so that all company employees can access the resources they need.

#### Explications

Incorrect — granting broad, overly permissive access violates the principle of least privilege. Use IAM policies, groups, roles, permission boundaries, and AWS Organizations service control policies to grant only the permissions required for each job function and reduce blast radius.  
**Votre réponse est correcte**  
C. Turn on multi-factor authentication (MFA) for added security during the login process.

#### Explications

Correct — requiring a second authentication factor significantly reduces the risk of unauthorized access. AWS recommends enabling MFA for the root account and for privileged IAM principals; supported options include virtual MFA apps and hardware/FIDO2 authenticators. MFA protection works with the AWS Management Console and with temporary credentials obtained via AWS STS.  
D. Avoid rotating credentials to prevent issues in production applications.

#### Explications

Incorrect — avoiding credential rotation increases exposure to compromised credentials. AWS best practices are to use IAM roles and temporary credentials (AWS STS) instead of long-term access keys, rotate any necessary long-term keys regularly, and use services such as AWS Secrets Manager or AWS Systems Manager for automated secret rotation.  
Explication générale  
This item tests IAM security best practices. The strongest single control among the choices is adding a second authentication factor for privileged principals because it mitigates risk from stolen credentials. The distractors recommend insecure practices (using root credentials, granting blanket permissions, or skipping credential rotation) that violate AWS guidance such as least privilege, root-account minimization, and use of temporary credentials.  
Domaine  
Domain 2: Security and Compliance  
Question 15Correct  
A company needs a managed NFS file system that the company can use with its AWS compute resources. Which AWS service or feature will meet these requirements?  
A. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Incorrect — Amazon EBS is block-level storage designed to be attached to an EC2 instance as a volume. It is not a network (NFS) file system and does not provide POSIX-compliant, concurrently mounted file shares across multiple instances (multi-attach is limited and not a replacement for a shared NFS service).  
B. AWS Storage Gateway Tape Gateway

#### Explications

Incorrect — Tape Gateway is a virtual tape library interface used for backup and archival workflows that write tapes to Amazon S3/Glacier. It does not provide a managed NFS file system. (Note: Storage Gateway also offers a File Gateway mode for NFS/SMB to S3, but the Tape Gateway option is specifically for VTL/backups.)  
C. Amazon S3 Glacier Flexible Retrieval

#### Explications

Incorrect — Amazon S3 Glacier Flexible Retrieval est un stockage d'objets archivé accessible via l'API S3, avec des caractéristiques de récupération et de coût de récupération. Le stockage d'objets n'est pas un système de fichiers NFS POSIX et ne peut pas être monté comme un partage NFS pour les ressources de calcul.  
**Votre réponse est correcte**  
D. Système de fichiers élastique Amazon (Amazon EFS)

#### Explications

Correct — Ce service fournit un système de fichiers NFSv4 entièrement géré et conforme à la norme POSIX, pouvant être monté simultanément par plusieurs instances EC2 (et intégré à d'autres services de calcul AWS). Il ajuste automatiquement la capacité, prend en charge les cibles de montage multi-AZ, propose des modes de débit et de performance, et prend en charge le chiffrement et les contrôles d'accès adaptés à l'utilisation d'un système de fichiers partagé.  
Explication générale  
Cette question teste vos connaissances sur les types de stockage AWS et sur celui conçu pour fournir une interface NFS gérée. La bonne réponse est le service NFS entièrement géré, car il offre la conformité POSIX, des montages simultanés entre instances et zones de disponibilité, ainsi qu'une capacité élastique. Les autres options sont le stockage par blocs (EBS), la virtualisation de sauvegarde/bande (Tape Gateway) et le stockage d'objets d'archivage (Glacier), mais aucune ne constitue un système de fichiers NFS géré.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 16Correct  
Une entreprise doit déployer des applications sur le cloud AWS le plus rapidement possible. Elle doit également minimiser la complexité liée à la gestion des ressources AWS. Quel service AWS doit-elle utiliser pour répondre à ces exigences ?  
A. Configuration AWS

#### Explications

AWS Config est un service de gouvernance et de conformité qui enregistre et évalue l'état de configuration des ressources AWS au fil du temps. Il facilite l'audit, le suivi des modifications et les évaluations de conformité, mais ne déploie ni ne gère les environnements d'exécution d'applications ; il ne répond donc pas aux exigences d'un déploiement d'applications rapide et nécessitant peu de gestion.  
**Votre réponse est correcte**  
B. AWS Elastic Beanstalk

#### Explications

Elastic Beanstalk est une plateforme applicative entièrement gérée (PaaS) qui automatise le provisionnement, l'allocation de capacité, l'équilibrage de charge, la mise à l'échelle automatique, la surveillance de l'état des applications et les déploiements pour les plateformes courantes. En masquant l'infrastructure sous-jacente et les tâches opérationnelles, elle permet un déploiement rapide des applications avec une charge de gestion des ressources minimale.  
C. Amazon EC2

#### Explications

Amazon EC2 fournit des serveurs virtuels bruts (IaaS) qui nécessitent que les clients provisionnent les instances, gèrent le système d'exploitation, assurent la mise à l'échelle, configurent les équilibreurs de charge et effectuent les mises à jour et la surveillance. Ce contrôle accru implique une charge de travail plus importante lors de la configuration et de la gestion continue, ce qui rend EC2 moins adapté à l'objectif affiché d'un déploiement rapide et simple.  
D. Amazon Personnaliser

#### Explications

Amazon Personalize est un service d'apprentissage automatique permettant de créer des recommandations personnalisées de produits et de contenus. Il est axé sur l'entraînement et l'inférence de modèles d'apprentissage automatique pour les cas d'utilisation de la personnalisation et n'a aucun lien avec le déploiement ou la gestion d'environnements d'applications généraux.  
Explication générale  
The question tests knowledge of AWS services that reduce operational effort for deploying applications. AWS Elastic Beanstalk is the correct choice because it is a managed application platform that automates infrastructure provisioning, scaling, and monitoring, enabling fast deployments with minimal management. The distractors are either governance/compliance (AWS Config), infrastructure that requires more hands‑on management (EC2), or a specialized ML service (Amazon Personalize), none of which meet both requirements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 17Incorrect  
A company wants to migrate its PostgreSQL database to AWS. The company does not use the database frequently. Which AWS service or resource will meet these requirements with the LEAST management overhead?  
A. PostgreSQL on Amazon EC2

#### Explications

Running PostgreSQL on Amazon EC2 places full responsibility on you for the OS and database lifecycle: provisioning, patching, backups, replication, HA configuration, monitoring, and scaling. There is no built-in auto-pause or managed failover, and compute is billed continuously even when the database is idle, so this option has the greatest operational overhead.  
B. Amazon RDS for PostgreSQL

#### Explications

Amazon RDS for PostgreSQL is a managed relational database that automates backups, minor version upgrades, snapshots, and Multi‑AZ failover, reducing operational burden versus EC2. However, it uses provisioned instance classes that remain running (and billed) when idle and does not provide automatic pause/resume, so it does not minimize cost and management for infrequently used workloads as effectively as a serverless option.  
**Votre réponse est incorrecte**  
C. Amazon Aurora PostgreSQL-Compatible Edition

#### Explications

Amazon Aurora (provisioned) offers a managed, high‑performance, PostgreSQL‑compatible engine with storage autoscaling and read replicas. Despite these benefits, the provisioned model requires selecting and managing DB instance capacity (compute instances) that are billed while running; it does not automatically pause for inactivity unless you choose a serverless configuration.  
**Bonne réponse**  
D. Amazon Aurora Serverless

#### Explications

Amazon Aurora Serverless (PostgreSQL‑compatible) is a managed serverless option that automatically starts, stops, and scales capacity in fine‑grained Aurora Capacity Units (ACUs) based on workload demand and can auto‑pause during periods of inactivity, reducing both administrative tasks and idle compute costs—making it the best fit for infrequently used databases.  
Explication générale  
The question tests choosing the lowest‑management, cost‑efficient option for an infrequently used PostgreSQL database. A serverless managed database that can auto‑scale and auto‑pause is optimal. Aurora Serverless for PostgreSQL provides auto start/stop, ACU‑based scaling, and pay‑per‑use billing with AWS handling maintenance—unlike EC2 (full management) or provisioned RDS/Aurora (always‑on provisioned compute)—so it minimizes both operational overhead and idle costs.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 18Correct  
Which AWS offering can analyze a company’s AWS environment to discover security vulnerabilities on Amazon EC2 instances?  
**Votre réponse est correcte**  
A. Amazon Inspector

#### Explications

Amazon Inspector is the AWS service purpose-built for automated vulnerability and configuration assessments of compute resources. It analyzes EC2 instances (and container images in newer versions), identifies known CVEs, insecure configurations, and unintended network exposure, and produces prioritized findings with remediation guidance and integrations (for example, with AWS Security Hub) to support remediation workflows.  
B. Amazon Macie

#### Explications

Amazon Macie is a data protection service that uses machine learning to discover, classify, and protect sensitive data in Amazon S3 (for example, personally identifiable information). It does not perform host- or OS-level vulnerability scanning of EC2 instances and therefore does not address the question.  
C. AWS Shield Standard

#### Explications

AWS Shield (Standard) is a managed service that provides automatic DDoS protection for AWS resources (such as CloudFront, ELB, and Route 53). It defends against volumetric and protocol-layer attacks but does not perform vulnerability assessments of EC2 instances.  
D. Security groups

#### Explications

Security groups are stateful virtual firewalls applied to EC2 instances that control inbound and outbound traffic by rules. They are a network control mechanism and do not scan or analyze instances for vulnerabilities or configuration weaknesses.  
Explication générale  
The question asks which AWS offering performs vulnerability discovery on EC2 instances. Amazon Inspector is the dedicated automated assessment service that scans compute resources for vulnerabilities, insecure configurations, and deviations from best practices and returns prioritized findings and remediation advice. The other choices focus on different security responsibilities: Macie discovers sensitive data in S3, Shield protects against DDoS, and security groups enforce network access — none perform vulnerability scanning of EC2 hosts.  
Domaine  
Domain 2: Security and Compliance  
Question 19Correct  
Which AWS services can a company use to achieve a loosely coupled architecture? (Choose two.)  
A. Amazon WorkSpaces

#### Explications

Incorrect — This service provides managed virtual desktops for end users. It addresses desktop and user access needs rather than providing messaging or orchestration primitives needed to decouple application components.  
**Votre sélection est correcte**  
B. Amazon Simple Queue Service (Amazon SQS)

#### Explications

Correct — This is a fully managed, durable message-queuing service that enables asynchronous communication between producers and consumers. By buffering requests and allowing independent processing rates, it reduces direct dependencies, improves fault tolerance, and supports scalable, loosely coupled architectures (integrates with Lambda, ECS, Step Functions, etc.).  
C. Amazon Connect

#### Explications

Incorrect — This is a cloud contact-center service focused on customer interactions. It does not provide messaging queues or workflow orchestration capabilities used to decouple application components.  
D. AWS Trusted Advisor

#### Explications

Incorrect — This service offers best-practice checks and recommendations for cost, security, performance, and fault tolerance. It is advisory only and does not provide integration, messaging, or orchestration features to achieve loose coupling.  
**Votre sélection est correcte**  
E. AWS Step Functions

#### Explications

Correct — This serverless workflow orchestration service coordinates distributed AWS services using state machines and built-in error handling, retries, and asynchronous task patterns. It enables components to remain independent while being coordinated, supporting fault-tolerant, loosely coupled designs.  
Explication générale  
Loosely coupled architectures are achieved by removing direct dependencies between components so each can operate, scale, and fail independently. Durable message queuing provides asynchronous communication (reducing caller/callee coupling), and workflow orchestration coordinates distributed tasks and error handling without tight integration. In this question, the appropriate choices are the managed queuing service and the serverless orchestration service; the other options are either end-user/customer solutions or advisory tools and do not provide the required integration primitives.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 20Correct  
A user needs a relational database but does not have the resources to manage the hardware, resiliency, and replication. Which AWS service option meets the user's requirements?  
A. Run MySQL on Amazon Elastic Container Service (Amazon ECS).

#### Explications

Amazon ECS is a container orchestration service for running containers. Hosting a database in containers leaves responsibility for the database engine, data durability, backups, replication, patching, and automated failover to the customer—so it is not a fully managed relational database solution for minimizing operational overhead.  
B. Run MySQL on Amazon EC2.

#### Explications

Amazon EC2 provides raw virtual servers (IaaS). Running MySQL on EC2 requires you to manage the operating system, database installation, backups, replication, patching, scaling, and high-availability configuration, so it does not meet the requirement of avoiding hardware and resiliency management.  
**Votre réponse est correcte**  
C. Choose Amazon RDS for MySQL.

#### Explications

Amazon RDS is a managed relational database service that automates provisioning, software patching, automated backups and snapshots, point-in-time recovery, monitoring, and provides built-in high availability (Multi-AZ) and read replicas for scalability and replication—so it offloads hardware, resiliency, and replication management from the customer.  
D. Choose Amazon ElastiCache for Redis.

#### Explications

Amazon ElastiCache (Redis) is an in-memory caching/data-store service designed for low-latency key-value workloads. It is not a relational database (no SQL-based relational model, schema, or ACID RDBMS features), so it does not satisfy the user's requirement for a relational database.  
Explication générale  
The user needs a managed relational database where AWS handles hardware, resiliency, and replication. Amazon RDS for MySQL is the appropriate choice because it provides a fully managed relational DB engine with automated backups, Multi-AZ high availability, automated software patching, and replication options. Running MySQL on ECS or EC2 requires the customer to manage OS, backups, replication, and failover; ElastiCache is a non-relational in-memory store and therefore unsuitable.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 21Incorrect  
Which cloud transformation journey phase of the AWS Cloud Adoption Framework (AWS CAF) focuses on demonstrating how the cloud helps accelerate business outcomes?  
**Bonne réponse**  
A. Scale

#### Explications

This transformation phase is purpose-built to expand cloud adoption organization-wide and to prove value by measuring business KPIs (for example, time-to-market, cost efficiency, and development velocity). Activities in this phase include operationalizing automation, collecting metrics and business-level outcomes, and using those results to drive broader adoption and investment decisions—exactly the work required to demonstrate how the cloud accelerates business outcomes.  
**Votre réponse est incorrecte**  
B. Envision

#### Explications

This phase is focused on defining strategy: articulating business goals, creating a high-level cloud vision and roadmap, prioritizing opportunities, and building a business case. It establishes direction and stakeholder buy-in but is primarily planning and alignment work rather than the phase that demonstrates realized business acceleration.  
C. Align

#### Explications

This area centers on ensuring cloud initiatives are aligned with business priorities, governance, and stakeholder expectations. It is about organizational and governance alignment rather than proving or scaling measurable business outcome improvements across the enterprise.  
D. Launch

#### Explications

This stage typically covers initial deployments, pilots, or go‑live activities to validate technical approaches and deliver working solutions. While it can produce early results, its scope is executional and limited; demonstrating accelerated business outcomes at scale comes later when adoption is expanded and outcomes are measured.  
Explication générale  
The question targets the AWS Cloud Adoption Framework transformation journey stage that is responsible for proving and amplifying cloud value. The correct stage is the one that scales adoption and measures business KPIs to demonstrate acceleration of outcomes. By contrast, the planning/strategy phase defines vision and business case, the alignment phase handles stakeholder and governance alignment, and the launch/pilot phase focuses on initial deployments rather than organization-wide demonstration of impact.  
Domaine  
Domain 1: Cloud Concepts  
Question 22Correct  
A company wants to automatically add and remove Amazon EC2 instances. The company wants the EC2 instances to adjust to varying workloads dynamically. Which service or feature will meet these requirements?  
A. Amazon DynamoDB

#### Explications

DynamoDB is a fully managed NoSQL database service that handles key-value and document workloads and scales storage and read/write capacity for data access. It does not provide lifecycle management or automated provisioning of EC2 compute instances, so it cannot be used to add or remove EC2 instances in response to workload changes.  
B. Amazon EC2 Spot Instances

#### Explications

Spot Instances are a pricing option that lets you run EC2 capacity at discounted rates using spare AWS capacity. They do not include the control-plane mechanisms to automatically scale a fleet based on metrics or schedules by themselves (though they can be launched by an auto-scaling mechanism). Spot is a cost model, not an autoscaling service.  
C. AWS Snow Family

#### Explications

The Snow Family consists of physical edge and data transfer devices for offline data migration and edge compute in disconnected environments. These appliances are not a service for dynamically provisioning or terminating EC2 instances in the AWS cloud.  
**Votre réponse est correcte**  
D. Amazon EC2 Auto Scaling

#### Explications

Auto scaling groups provide automated capacity management for EC2 by using scaling policies (target-tracking, step, and scheduled), CloudWatch metrics, health checks, and lifecycle hooks. This enables automatic addition and removal of instances to maintain performance and optimize cost across Availability Zones and integrates with load balancers and instance health monitoring.  
Explication générale  
This item tests understanding of how to automatically adjust compute capacity for variable workloads. The correct solution is the AWS capability that manages EC2 instance fleets using scaling groups, policies, and CloudWatch metrics to add or remove instances automatically. The other choices describe a NoSQL database service, a discounted pricing option, and physical edge/data-transfer devices — none of which provide the control-plane features required to autoscale EC2 instances.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 23Correct  
Which AWS service gives users the ability to build interactive business intelligence dashboards that include machine learning insights?  
A. Amazon Athena

#### Explications

Amazon Athena is a serverless interactive query service that lets you run ANSI SQL directly against data stored in Amazon S3 (uses a Presto/Trino-based engine). It is a query/data-source layer rather than a BI/dashboarding service and does not provide built-in ML-powered visualization features; BI tools (for example, QuickSight) typically consume results from Athena.  
B. Amazon Kendra

#### Explications

Amazon Kendra is an ML-powered enterprise search service designed to index and retrieve unstructured content and answer natural-language queries. Its purpose is search and relevance ranking across document repositories, not creating interactive BI dashboards or providing ML-driven visual insights like anomaly detection or forecasting.  
**Votre réponse est correcte**  
C. Amazon QuickSight

#### Explications

Amazon QuickSight is a fully managed, serverless business intelligence service that creates interactive dashboards and visualizations and embeds ML-powered insights (for example, anomaly detection, forecasting, natural-language Q, and automated narrative insights). It can connect to AWS data sources (Redshift, Athena, RDS, S3, etc.) and uses the SPICE in‑memory engine for fast analytics, enabling ML insights to appear directly within dashboards.  
D. Amazon Redshift

#### Explications

Amazon Redshift is a fully managed, petabyte-scale data warehouse optimized for large-scale analytic queries and reporting. It serves as a powerful data source for BI tools and includes capabilities such as Redshift ML for model training via SQL, but it does not provide the end-user dashboarding UI and embedded ML visualization features that a BI service like QuickSight provides.  
Explication générale  
The question tests recognition of the AWS service that combines interactive BI dashboards with built-in ML insights. Amazon QuickSight is the correct choice because it is the managed BI service that natively provides interactive dashboards plus ML-powered features (anomaly detection, forecasting, natural-language querying and narrative insights). The other options are analytics or search components (Athena: query engine on S3; Redshift: data warehouse; Kendra: enterprise search) that act as data sources or search tools rather than full BI platforms with embedded ML visualizations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 24Correct  
Which of the following is the customer's responsibility under the AWS shared responsibility model? (Choose two.)  
A. Maintain the configuration of infrastructure devices.

#### Explications

Incorrect. The configuration and management of physical network and infrastructure devices (physical routers, switches, hosts, and the physical hypervisor layer) are managed by AWS as part of ‘security of the cloud.’ Customers do not perform low-level device configuration for AWS-managed infrastructure.  
B. Maintain patching and updates within the hardware infrastructure.

#### Explications

Incorrect. Patching and maintenance of physical hardware and the underlying virtualization/hypervisor layer are AWS responsibilities. Customers are instead responsible for patching guest operating systems and software that they run on compute resources they control.  
**Votre sélection est correcte**  
C. Maintain the configuration of guest operating systems and applications.

#### Explications

Correct. When customers run compute resources (for example EC2 instances or containers), they are responsible for operating-system-level configuration, patching, hardening, and application security. This is part of the customer’s duties for ‘security in the cloud’ such as OS management, application updates, and runtime configuration.  
**Votre sélection est correcte**  
D. Manage decisions involving encryption options.

#### Explications

Correct. Customers make encryption and key-management decisions for their data: selecting encryption at rest/in transit, choosing between AWS-managed and customer-managed keys, configuring AWS KMS key policies and rotation, and implementing client-side encryption when required. AWS provides encryption services and primitives but customers govern keys and data protection choices.  
E. Maintain infrastructure hardware.

#### Explications

Incorrect. Physical servers and other infrastructure hardware are owned, maintained, and replaced by AWS as part of the managed infrastructure. Customers do not maintain AWS’s data-center hardware (except in specific hybrid offerings where different responsibilities apply).  
Explication générale  
This item tests the AWS Shared Responsibility Model. AWS is responsible for the security and maintenance of the cloud infrastructure (physical hardware, facilities, network, and hypervisor), while customers are responsible for what they put in the cloud: operating systems, applications, data, access controls, and decisions about encryption and key management. Therefore the customer responsibilities are the OS/application configuration and encryption/key-management decisions (C and D); the hardware and low-level infrastructure tasks remain AWS responsibilities (A, B, E).  
Domaine  
Domain 2: Security and Compliance  
Question 25Correct  
Which AWS service or feature provides log information of the inbound and outbound traffic on network interfaces in a VPC?  
A. Amazon CloudWatch Logs

#### Explications

CloudWatch Logs is a storage and analysis destination for log data (including flow logs) but does not itself generate network-level traffic records. VPC Flow Logs produces the flow records and can publish them to CloudWatch Logs or S3 for retention and analysis.  
B. AWS CloudTrail

#### Explications

CloudTrail records AWS management and data‑plane API calls and user activity for auditing and compliance; it does not capture IP‑level or packet metadata for traffic on ENIs, so it cannot provide inbound/outbound network interface flow records.  
**Votre réponse est correcte**  
C. VPC Flow Logs

#### Explications

VPC Flow Logs captures metadata about IP traffic to and from network interfaces (ENIs) at the VPC, subnet, or ENI level. Records include fields such as source/destination IP, ports, protocol, packet/byte counts, and an action (ACCEPT/REJECT). Flow logs can be filtered (ALL/ACCEPT/REJECT) and delivered to CloudWatch Logs or Amazon S3 for monitoring, security analysis, and troubleshooting. Note: flow logs record metadata only, not packet payloads.  
D. AWS Identity and Access Management (IAM)

#### Explications

IAM is the identity and access management service for creating and managing users, roles, and permissions. It does not monitor or log network traffic, although IAM policies control who can create or view flow logs and related logging destinations.  
Explication générale  
La question porte sur la fonctionnalité AWS permettant de visualiser le trafic des interfaces réseau entrantes et sortantes d'un VPC. La fonctionnalité appropriée est VPC Flow Logs : elle génère des enregistrements de métadonnées sur le trafic IP pour les interfaces réseau externes (ou par sous-réseau/VPC) et les envoie à CloudWatch Logs ou à S3. CloudWatch Logs est une destination de stockage et d'analyse, CloudTrail enregistre l'activité des API (et non les métadonnées des paquets réseau), et IAM gère l'identité et les autorisations plutôt que l'enregistrement du trafic.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 26Correct  
L'environnement cloud d'une entreprise comprend des instances Amazon EC2 et des équilibreurs de charge d'application. L'entreprise souhaite renforcer la protection de ses ressources cloud contre les attaques DDoS et obtenir une visibilité en temps réel sur toute attaque DDoS. Quel service AWS répond à ces exigences ?  
A. Norme AWS Shield

#### Explications

Ce service offre une protection DDoS automatique et permanente au niveau du réseau et du transport pour des services tels que EC2, ELB, CloudFront et Route 53, sans frais supplémentaires. Il ne comprend cependant pas de fonctionnalités avancées d'atténuation, de diagnostics d'attaque détaillés, de métriques DDoS quasi temps réel dans CloudWatch, ni d'accès 24 h/24 et 7 j/7 à l'équipe de réponse DDoS d'AWS. Par conséquent, il ne répond pas aux exigences d'une protection renforcée avec visibilité en temps réel.  
B. Gestionnaire de pare-feu AWS

#### Explications

Un service centralisé de gestion des politiques et des règles qui applique les politiques WAF, Shield Advanced et des groupes de sécurité à l'ensemble des comptes. Il orchestre la protection, mais ne prend pas en charge l'atténuation avancée des attaques DDoS ni ne fournit les données de télémétrie et de diagnostic nécessaires en cas d'attaque.  
**Votre réponse est correcte**  
C. AWS Shield Advanced

#### Explications

Offre une protection DDoS renforcée par abonnement, avec des mesures d'atténuation avancées, des diagnostics d'attaque quasi temps réel et des indicateurs CloudWatch DDoS, un accès 24 h/24 et 7 j/7 à l'équipe de réponse DDoS AWS (DRT) et une protection des coûts pour la mise à l'échelle pendant les attaques. Ces fonctionnalités assurent une protection accrue pour EC2 et ALB, ainsi que la visibilité en temps réel nécessaire.  
D. Amazon GuardDuty

#### Explications

Ce service de détection des menaces analyse les journaux de flux VPC, CloudTrail et DNS afin d'identifier les comportements malveillants ou non autorisés. Utile pour détecter les compromissions et les activités suspectes, il ne propose cependant pas de mesures d'atténuation des attaques DDoS ni la télémétrie spécialisée en temps réel fournie par Shield Advanced.  
Explication générale  
Cette question teste vos connaissances sur les options de protection DDoS d'AWS. AWS Shield Advanced est le service d'abonnement qui offre une protection DDoS renforcée, des diagnostics d'attaque (métriques CloudWatch DDoS), une assistance 24 h/24 et 7 j/7 de l'équipe de réponse DDoS et une maîtrise des coûts, répondant ainsi aux exigences d'une protection accrue et d'une visibilité en temps réel. Shield Standard propose uniquement une protection automatique de base, Firewall Manager gère uniquement les politiques et GuardDuty assure la détection des menaces sans atténuation des attaques DDoS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 27Correct  
Quel service AWS les entreprises peuvent-elles utiliser pour créer une infrastructure à partir de code ?  
A. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Incorrect — EKS is a managed Kubernetes service used to run and manage containerized applications (Kubernetes control plane, worker nodes, Fargate integration). It is not an infrastructure-as-code (IaC) tool; you use IaC solutions to define and provision resources that might include an EKS cluster, but EKS itself does not provide templated, declarative infrastructure provisioning.  
B. AWS Outposts

#### Explications

Incorrect — Outposts provides AWS-managed hardware and services in on-premises locations to enable hybrid deployments. It is a form factor for running AWS infrastructure locally, not a mechanism for authoring or deploying infrastructure via code or templates.  
C. AWS CodePipeline

#### Explications

Incorrect — CodePipeline is a CI/CD orchestration service that automates build, test, and deployment workflows. While it can execute deployments that use IaC (for example, by invoking CloudFormation), it is not the IaC technology that defines resources declaratively.  
**Votre réponse est correcte**  
D. AWS CloudFormation

#### Explications

Correct — CloudFormation is AWS's native Infrastructure as Code service: you define resources declaratively in JSON or YAML templates, create and manage stacks, use Change Sets for safe updates, and rely on features such as drift detection and stack policies to provision and maintain AWS (and some third‑party) resources reproducibly.  
Explication générale  
The question tests knowledge of Infrastructure as Code. The correct answer is CloudFormation because it is the AWS service designed to model and provision resources through declarative templates and stacks. The other options are different classes of services: EKS manages Kubernetes clusters, Outposts provides on-premises AWS hardware, and CodePipeline orchestrates CI/CD—none are the native IaC engine for defining infrastructure.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 28Correct  
What is the best resource for a user to find compliance-related information and reports about AWS?  
**Votre réponse est correcte**  
A. AWS Artifact

#### Explications

Provides on-demand access to AWS compliance reports, certifications, and attestations (SOC, ISO, PCI, etc.) plus customer-specific agreements and audit artifacts. This portal is the official AWS location for downloading the documentation customers need for audits, regulatory reviews, and compliance validation.  
B. AWS Marketplace

#### Explications

An online catalog for third-party software and SaaS products that run on AWS; it is focused on procurement and deployment of solutions, not a repository of AWS’s own compliance reports or certifications.  
C. Amazon Inspector

#### Explications

A runtime and assessment service that scans workloads for security vulnerabilities and deviations from best practices. It generates findings for remediation but does not act as a centralized store for AWS compliance reports or formal attestations.  
D. AWS Support

#### Explications

A paid technical support channel that helps with troubleshooting and guidance. Support can assist with questions about compliance, but it is not the primary source for obtaining official compliance reports or certifications.  
Explication générale  
The correct resource is the AWS compliance reports portal, which is the official location to obtain AWS-issued compliance documentation (certifications, audit reports, and attestation letters) required for audits and regulatory assessments. Other choices describe services for software procurement, security assessments, or technical help, none of which serve as the centralized repository for AWS compliance artifacts.  
Domaine  
Domain 2: Security and Compliance  
Question 29Correct  
A company has multiple SQL-based databases located in a data center. The company needs to migrate all database servers to the AWS Cloud to reduce the cost of operating physical servers. Which AWS service or resource will meet these requirements with the LEAST operational overhead?  
A. Amazon EC2 instances

#### Explications

Amazon EC2 provides raw virtual servers (IaaS) that can run any database engine, but it places responsibility for OS and database installation, backups, patching, replication, failover, and scaling on the customer. That additional operational burden makes EC2 unsuitable when the goal is to minimize operational overhead.  
**Votre réponse est correcte**  
B. Amazon RDS

#### Explications

Amazon RDS is a managed relational database service that automates provisioning, automated backups and snapshots, automated minor version patching, Multi‑AZ deployments for high availability, read replicas for scaling reads, and integrates with IAM, CloudWatch, and AWS Backup. These managed capabilities significantly reduce DBA and infrastructure operational tasks, making RDS the best fit for migrating SQL databases with the least operational overhead.  
C. Amazon DynamoDB

#### Explications

Amazon DynamoDB is a fully managed NoSQL key‑value/document database with different data models and query capabilities than relational SQL databases. While managed, it is not a drop‑in replacement for SQL databases and therefore does not meet the requirement to migrate existing SQL‑based database servers.  
D. OpenSearch

#### Explications

OpenSearch (Amazon OpenSearch Service) is a managed search and analytics engine designed for full‑text search, log analytics, and observability. It is not a relational OLTP database and does not provide the relational features expected when migrating SQL database servers.  
Explication générale  
The question asks which option minimizes operational overhead when migrating SQL‑based databases. Amazon RDS is the managed relational database service that handles routine administrative tasks (backups, patching, HA, scaling) and supports common SQL engines, so it requires the least operational effort. In contrast, EC2 requires full self‑management, DynamoDB is a NoSQL service with incompatible data models, and OpenSearch is for search/analytics rather than relational workloads.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 30Correct  
A company uses Amazon S3 to store records that can contain personally identifiable information (PII). The company wants a solution that can monitor all S3 buckets for PII and immediately alert staff about vulnerabilities. Which AWS service will meet these requirements?  
A. Amazon GuardDuty

#### Explications

Incorrect. This service is focused on threat detection across AWS accounts by analyzing AWS CloudTrail, VPC Flow Logs, and DNS logs for malicious or anomalous activity. It does not provide data classification or automated discovery of PII within S3 objects.  
B. Amazon Detective

#### Explications

Incorrect. This service is used to investigate and visualize security findings (for example, those produced by GuardDuty) to speed incident analysis. It does not perform content inspection or identify sensitive data stored in S3 buckets.  
**Votre réponse est correcte**  
C. Amazon Macie

#### Explications

Correct. This managed data-security service uses machine learning and pattern matching to automatically discover and classify sensitive data (including PII) in S3. It provides continuous monitoring, generates findings for sensitive-data exposures, and integrates with EventBridge/CloudWatch/SNS and Security Hub so teams can be alerted and take remediation actions immediately.  
D. AWS Shield

#### Explications

Incorrect. This service provides DDoS protection for applications and edge services. Its focus is network- and application-layer availability protection, not content inspection or sensitive-data classification in object storage.  
Explication générale  
The requirement is to discover and monitor PII in S3 and alert staff immediately. The correct choice is the service purpose-built for automated sensitive-data discovery and classification in S3 with alerting integrations. The other options address different security concerns: threat detection and investigation or DDoS protection, and therefore do not meet the PII discovery and monitoring need.  
Domaine  
Domain 2: Security and Compliance  
Question 31Correct  
Which option is an environment that consists of one or more data centers?  
A. Amazon CloudFront

#### Explications

CloudFront is a global content delivery network composed of edge locations and regional caches optimized for low-latency content delivery. It does not represent an environment made up of one or more data centers; edge locations are cache points rather than full AWS data center environments like Availability Zones.  
**Votre réponse est correcte**  
B. Availability Zone

#### Explications

An Availability Zone is the AWS construct that maps to one or more discrete, physically separated data centers within an AWS Region. AZs provide independent power, networking, and connectivity to support fault isolation and high availability, which is why this option describes an environment of one or more data centers.  
C. VPC

#### Explications

A Virtual Private Cloud is a logically isolated virtual network within the AWS Cloud that provides subnets, routing, and network controls for resources. It is a virtual networking construct and does not equate to physical data centers or an AZ grouping.  
D. AWS Outposts

#### Explications

Outposts are racks of AWS-managed hardware installed at a customer site to provide consistent on-premises access to AWS services. They extend AWS infrastructure to customer locations but are not themselves an AWS environment composed of multiple data centers (they are hardware deployed in a single on‑premises location).  
Explication générale  
This question tests knowledge of AWS physical infrastructure. Availability Zones are the correct concept because they correspond to one or more physical data centers within a Region, designed for redundancy and isolation. The other choices describe different service types: CloudFront (CDN edge/cache locations), VPC (logical virtual network), and Outposts (on‑premises racks), none of which are AWS environments composed of one or more data centers.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 32Correct  
Which AWS service can companies use to subscribe to RSS feeds for updates about all AWS service issues?  
A. Amazon Simple Notification Service (Amazon SNS)

#### Explications

Incorrect. Amazon SNS is a pub/sub messaging service that delivers notifications to endpoints such as email, SMS, HTTP(S), Lambda, and SQS. SNS does not itself publish a public RSS feed of AWS service status. (You can route health events to SNS via other services, but SNS is a delivery mechanism, not the canonical source of AWS service-status RSS.)  
**Votre réponse est correcte**  
B. AWS Health Dashboard

#### Explications

Correct. The AWS public Service Health Dashboard (part of the AWS Health family) publishes RSS feeds that report service- and region-level incidents and status updates so subscribers can receive updates about AWS service issues. Note that the Personal/Account-specific AWS Health (Personal Health Dashboard) provides tailored events for your resources and can integrate with EventBridge/SNS, whereas the Service Health Dashboard is the canonical RSS source for broad, public service-status feeds.  
C. AWS Config

#### Explications

Incorrect. AWS Config is a configuration-tracking and compliance-auditing service that records resource configuration history and evaluates compliance rules. It does not provide AWS service-status notifications or RSS feeds about AWS-wide service incidents.  
D. AWS CodeCommit

#### Explications

Incorrect. AWS CodeCommit is a managed Git-based source control service for storing and versioning code. It does not provide service health monitoring or RSS feeds for AWS service issues.  
Explication générale  
This question tests knowledge of where to get RSS-based updates about AWS service incidents. The public Service Health Dashboard (part of AWS Health) is the canonical source that publishes RSS feeds for service- and region-level issues. The Personal/Account-specific Health Dashboard offers individualized alerts and integrates with EventBridge/SNS for automated notifications, while SNS, Config, and CodeCommit are delivery, configuration-auditing, and source-control services respectively and are not the primary RSS source for AWS service-wide status.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 33Correct  
Which design principles support the reliability pillar of the AWS Well-Architected Framework? (Choose two.)  
A. Perform operations as code.

#### Explications

Using infrastructure and operational automation (Infrastructure as Code, CI/CD pipelines, AWS CloudFormation, AWS CDK) is an Operational Excellence principle. It improves repeatability and reduces human error, but it is not one of the primary design principles identified for the Reliability pillar.  
B. Enable traceability.

#### Explications

Collecting logs, metrics, and traces (AWS CloudTrail, Amazon CloudWatch, AWS X-Ray) supports auditing, troubleshooting, and security posture. This traceability is important for operations and security, but it is not one of the core Reliability design principles the question targets.  
**Votre sélection est correcte**  
C. Automatically scale to meet demand.

#### Explications

Design systems to adjust capacity automatically using elastic scaling mechanisms (Amazon EC2 Auto Scaling, Application Auto Scaling, AWS Lambda concurrency). Elastic scaling prevents overload during demand spikes, supports the ‘stop guessing capacity’ and horizontal-scaling reliability practices, and helps maintain availability and performance.  
D. Deploy resources globally to improve response time.

#### Explications

Placing resources in multiple geographic locations (CloudFront, multi‑Region deployments) primarily addresses latency and Performance Efficiency. While multi‑Region architectures can aid availability for disaster recovery, the option as stated focuses on response time and therefore aligns more with Performance Efficiency than the Reliability pillar.  
**Votre sélection est correcte**  
E. Automatically recover from failure.

#### Explications

Design for automatic detection and recovery so services self‑heal without manual intervention (health checks, Auto Scaling replacement of unhealthy instances, Amazon RDS Multi‑AZ failover, Route 53 failover policies). These patterns minimize downtime and directly implement Reliability pillar principles.  
Explication générale  
The Reliability pillar emphasizes designs that maintain availability and recover from failures: dynamic capacity management and automated recovery are central. The correct choices map to elastic scaling to handle demand and self‑healing/failover mechanisms to restore service after failures. The distractors describe Operational Excellence (automation and traceability) or Performance Efficiency (global deployment for latency), which are important but not the primary Reliability design principles tested here.  
Domaine  
Domain 1: Cloud Concepts  
Question 34Correct  
Which design principles are included in the reliability pillar of the AWS Well-Architected Framework? (Choose two.)  
**Votre sélection est correcte**  
A. Automatically recover from failure.

#### Explications

Verified as a reliability pillar principle: the Well‑Architected reliability guidance emphasizes detecting failures and using automation to restore healthy states without human intervention. Typical AWS mechanisms that implement this principle include health checks and failover (Route 53, Elastic Load Balancing), automated instance replacement and scaling (Auto Scaling, EC2 Auto Recovery), CloudWatch alarms/EventBridge to trigger remediation, and infrastructure as code to enable rapid, consistent recovery.  
B. Grant everyone access to increase AWS service quotas.

#### Explications

Incorrect: Granting broad access to increase service quotas contradicts security and governance best practices (principle of least privilege). Service Quotas and IAM/Organizations should be used to manage quotas and permissions; this is an operational/governance concern, not a reliability design principle.  
**Votre sélection est correcte**  
C. Stop guessing capacity.

#### Explications

Verified as a reliability pillar principle: avoiding guessed capacity is about designing for elasticity and using scaling and managed services so capacity matches demand. AWS approaches include Auto Scaling, serverless (AWS Lambda), managed services with automatic scaling (Amazon DynamoDB, Amazon S3), and using CloudWatch metrics and predictive scaling to remove manual, error‑prone capacity estimates.  
D. Design applications to run in a single Availability Zone.

#### Explications

Incorrect: Intentionally running applications in a single Availability Zone reduces fault tolerance and increases risk of outage. The reliability pillar recommends distributing resources across multiple AZs (and where appropriate, regions), using load balancing and database Multi‑AZ deployments to maintain availability during component failures.  
E. Plan to increase AWS service quotas first in a secondary AWS Region.

#### Explications

Incorrect: Requesting higher quotas in a secondary Region is an operational or disaster‑recovery action but is not listed as a core design principle of the reliability pillar. Quota management is done via Service Quotas and planning, but the pillar focuses on architecture patterns (redundancy, automation, scaling) rather than specific quota request ordering.  
Explication générale  
The question tests knowledge of the AWS Well‑Architected reliability pillar design principles. The correct principles are automation for failure detection and recovery (A) and eliminating guessed capacity through elasticity and scaling (C). The distractors describe insecure practices (B), anti‑reliability architecture (D), or operational quota actions that are not core pillar principles (E).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 35Correct  
What is the primary use case for Amazon GuardDuty?  
A. Prevention of DDoS attacks

#### Explications

Incorrect. GuardDuty is not a DDoS mitigation service. DDoS protections are provided by AWS Shield (and Shield Advanced) and can be combined with AWS WAF for application-layer protections. GuardDuty focuses on detecting suspicious activity and delivering findings rather than performing network-level attack mitigation.  
B. Protection against SQL injection attacks

#### Explications

Incorrect. Protection specifically against injection attacks at the web application layer is the responsibility of a web application firewall such as AWS WAF (and security best practices in application code). GuardDuty does not block or filter HTTP requests; it analyzes logs and network metadata to surface threats and anomalies.  
**Votre réponse est correcte**  
C. Automatic monitoring for threats to AWS workloads

#### Explications

Correct. GuardDuty is a managed threat detection service that continuously analyzes AWS CloudTrail event logs, VPC Flow Logs, DNS logs (and other supported data sources) using threat intelligence, anomaly detection, and machine learning. It generates prioritized findings about malicious or unauthorized activity across accounts and regions and integrates with Amazon EventBridge, Security Hub, and automated remediation workflows.  
D. Automatic provisioning of AWS resources

#### Explications

Incorrect. Resource provisioning and orchestration are handled by services like AWS CloudFormation, AWS CDK, and AWS Service Catalog. GuardDuty does not create or manage infrastructure; its role is to monitor and detect security-relevant activity.  
Explication générale  
Amazon GuardDuty is designed for continuous threat detection across AWS environments. It ingests CloudTrail, VPC Flow Logs, DNS logs, and other telemetry, applies threat intelligence and ML-based anomaly detection, and produces prioritized security findings. It is a detection and alerting service—not a DDoS mitigator, WAF, or provisioning tool—and is typically used together with services such as AWS Shield, AWS WAF, and automated remediation (EventBridge \+ Lambda) for comprehensive protection.  
Domaine  
Domain 2: Security and Compliance  
Question 36Correct  
Which AWS service is a key-value database that provides sub-millisecond latency on a large scale?  
**Votre réponse est correcte**  
A. Amazon DynamoDB

#### Explications

DynamoDB is a fully managed NoSQL key-value and document database that is engineered for single-digit millisecond performance at virtually any scale. For even lower-latency read-heavy workloads, DynamoDB can be paired with DynamoDB Accelerator (DAX) to provide microsecond (sub-millisecond) response times. Features such as on-demand or provisioned capacity, adaptive capacity, SSD-backed storage, and multi-AZ durability make it the appropriate choice for large-scale, low-latency key-value workloads.  
B. Amazon Aurora

#### Explications

Aurora is a high-performance relational database compatible with MySQL and PostgreSQL, optimized for transactional relational workloads and complex queries. Its architecture and SQL-based relational model make it inappropriate as a purpose-built key-value store optimized for sub-millisecond latency at large scale.  
C. Amazon DocumentDB (with MongoDB compatibility)

#### Explications

DocumentDB is a managed document (JSON-like) database designed for MongoDB-compatible document workloads and complex document queries. While it supports document-oriented access patterns, it is not specifically optimized as a key-value store for guaranteed sub-millisecond latency at extreme scale.  
D. Amazon Neptune

#### Explications

Neptune is a purpose-built graph database service optimized for traversing highly connected data using graph query languages (Gremlin, SPARQL). Its design targets graph workloads rather than general key-value access patterns and therefore is not the right fit for large-scale sub-millisecond key-value use cases.  
Explication générale  
This item tests recognition of the appropriate AWS database type for low-latency key-value access. DynamoDB is the managed service designed for key-value and document workloads with predictable single-digit millisecond latency and can achieve sub-millisecond reads when used with DAX. The other options are specialized for relational, document query, or graph workloads and do not target high-scale, sub-millisecond key-value performance.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 37Correct  
A company wants its Amazon EC2 instances to operate in a highly available environment, even if there is a natural disaster in a particular geographic area. Which approach will achieve this goal?  
**Votre réponse est correcte**  
A. Use EC2 instances in multiple AWS Regions.

#### Explications

Le déploiement des charges de travail dans plusieurs régions AWS assure une isolation physique et géographique : les régions sont des emplacements distincts et indépendants, dotés d'une alimentation électrique, d'un réseau et d'une connectivité isolés. Un déploiement multirégional permet aux services et aux données de rester disponibles même si une région est touchée par un sinistre. Pour mettre en œuvre ce modèle, il est nécessaire de combiner la réplication des données interrégionales (par exemple, S3 CRR, les réplicas de lecture RDS ou les sauvegardes), le basculement DNS (Amazon Route 53\) et le basculement des applications ou le routage du trafic entre les régions.  
B. Utilisez des instances EC2 dans plusieurs emplacements Amazon CloudFront.

#### Explications

Amazon CloudFront utilise des points de présence comme CDN mondial pour la mise en cache et la distribution de contenu au plus près des utilisateurs. Ces points de présence ne sont pas des environnements d'exécution d'instances EC2 ; ils mettent en cache le contenu et peuvent exécuter des fonctions légères (Lambda@Edge), mais ne fournissent pas l'infrastructure ni l'isolation nécessaires à la reprise après sinistre au niveau d'EC2.  
C. Utilisez des instances EC2 dans plusieurs emplacements périphériques.

#### Explications

Les points de présence (Edge) sont optimisés pour la diffusion de contenu (mise en cache à faible latence) et ne sont pas conçus pour héberger des instances EC2 ni pour assurer la redondance au niveau régional. Ils ne disposent pas de l'infrastructure distincte et totalement indépendante des régions et ne peuvent donc pas garantir la résilience des charges de travail EC2 en cas de sinistre régional.  
D. Utilisez des instances EC2 dans les zones locales AWS.

#### Explications

Les zones locales AWS étendent une région parente à une zone métropolitaine spécifique afin de réduire la latence pour les utilisateurs locaux. Elles font partie de l'infrastructure de la même région (liées à une région parente) et ne fournissent donc pas l'isolation interrégionale nécessaire pour résister à une catastrophe naturelle touchant l'ensemble de la région.  
Explication générale  
Cette question évalue les connaissances sur l'infrastructure mondiale d'AWS et sur la manière de renforcer la résilience face aux sinistres géographiques. Seul le déploiement sur plusieurs régions AWS offre l'isolation géographique indépendante nécessaire pour survivre à une panne régionale. Les points de présence du CDN et les zones locales ont des objectifs différents (mise en cache du contenu et calcul local à faible latence) et ne fournissent pas l'isolation des pannes interrégionales requise pour la reprise après sinistre d'EC2.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 38Correct  
Une entreprise utilise un fournisseur d'identité tiers (IdP). Elle souhaite donner accès à ses employés aux comptes et services AWS sans exiger d'identifiants de connexion supplémentaires. Quel service AWS répond à ce besoin ?  
A. Service d'annuaire AWS

#### Explications

AWS Directory Service fournit une instance Microsoft Active Directory gérée (Managed Microsoft AD, AD Connector) pour l'intégration d'annuaires et l'authentification Windows. Bien qu'elle puisse s'intégrer à une solution de fédération plus vaste (par exemple, avec AD FS), elle n'est pas spécifiquement conçue pour l'authentification unique (SSO) au niveau du compte et basée sur SAML, et ne propose pas, à elle seule, le mappage centralisé des autorisations et les flux SSO offerts par IAM Identity Center.  
B. Amazon Cognito

#### Explications

Amazon Cognito is designed for application-level authentication and authorization (user pools and identity pools) and supports social and enterprise IdPs for web/mobile apps. It is not used to grant users direct access to AWS Management Console or to manage AWS account permissions across multiple accounts.  
**Votre réponse est correcte**  
C. AWS IAM Identity Center

#### Explications

AWS IAM Identity Center (formerly AWS Single Sign-On) is the correct service: it integrates with external SAML 2.0 IdPs, supports SCIM provisioning, maps users to permission sets that create IAM roles in target accounts, and issues temporary credentials so employees can access AWS accounts and services with their existing corporate credentials without creating separate IAM users.  
D. AWS Resource Access Manager (AWS RAM)

#### Explications

AWS Resource Access Manager (RAM) is a resource-sharing service that lets you share AWS resources (subnets, Route 53 Resolver rules, transit gateways, etc.) across accounts or organizations. It is unrelated to user authentication or federated single sign-on and cannot provide IdP-based access to AWS accounts.  
Explication générale  
The question tests identity federation for AWS account access. AWS IAM Identity Center is the service designed to connect third‑party SAML IdPs and provide centralized single sign‑on and permission mapping across AWS accounts, enabling users to use existing credentials and receive temporary IAM role credentials. Directory Service and Cognito serve different purposes (directory integration and application auth, respectively), and RAM is for resource sharing, so they are not appropriate for this requirement.  
Domaine  
Domain 2: Security and Compliance  
Question 39Correct  
Which perspective in the AWS Cloud Adoption Framework (AWS CAF) includes capabilities for configuration management and patch management?  
A. Platform

#### Explications

Emphasizes the technical foundation: provisioning, platform services, and architecture (compute, storage, networking, orchestration). It focuses on building and delivering platform capabilities rather than owning the day‑to‑day operational processes that perform centralized configuration and automated OS/application patching.  
**Votre réponse est correcte**  
B. Operations

#### Explications

Responsible for operational runbooks, monitoring, incident/change management, and lifecycle activities such as centralized configuration and automated patching. In AWS implementations these capabilities are implemented using services and tools like AWS Systems Manager (State Manager, Patch Manager, Automation) and CloudWatch for visibility and automation, which together provide the configuration and patch management functionality.  
C. Security

#### Explications

Concentrates on identity, access management, encryption, logging, threat detection and compliance controls. Vulnerability and configuration posture are security concerns, but the execution of automated configuration management and patch deployment is typically delivered by operational processes and tools rather than by security controls alone (e.g., IAM, KMS, GuardDuty, Security Hub do not orchestrate patching).  
D. Governance

#### Explications

Covers policies, organizational structure, account strategy, compliance and risk management — it defines governance, guardrails and standards for how configuration and patching should be performed, but it does not execute the technical configuration management or automated patch workflows.  
Explication générale  
The CAF allocates responsibilities across perspectives. Configuration management and patching are operational lifecycle activities requiring runbooks, automation and monitoring, so they belong to the Operations perspective. Platform, Security, and Governance provide the foundational services, controls, and policies that guide operations but do not themselves perform centralized configuration/patch orchestration. AWS Systems Manager and CloudWatch are common services used to implement the operational capabilities referenced.  
Domaine  
Domain 1: Cloud Concepts  
Question 40Correct  
Which of the following is an AWS Well-Architected Framework design principle for operational excellence in the AWS Cloud?  
A. Go global in minutes.

#### Explications

Incorrect — this describes the advantage of AWS’s global infrastructure and rapid regional deployment. That concept relates to scalability, performance, and global reach rather than the Operational Excellence pillar’s design principles, which focus on processes, procedures, and operational practices.  
**Votre réponse est correcte**  
B. Make frequent, small, reversible changes.

#### Explications

Correct — the Operational Excellence pillar promotes deploying incremental, easily reversible updates to reduce risk and enable rapid feedback and continuous improvement. This approach is implemented through practices such as CI/CD pipelines, automated testing and deployment, monitoring and observability, and automated rollback/runbook automation to minimize blast radius and accelerate learning.  
C. Implement a strong foundation of identity and access management

#### Explications

Incorrect — identity and access management is a fundamental control in the Security pillar (authentication, authorization, and privileged access management). It supports secure operations but is not the specific design principle from the Operational Excellence pillar being tested.  
D. Stop spending money on hardware infrastructure for data center operations.

#### Explications

Incorrect — this statement describes cost/modernization benefits of moving away from on‑premises hardware and is aligned with Cost Optimization (and migration) concerns, not the operational practices and process-focused principles of Operational Excellence.  
Explication générale  
The question tests knowledge of the Well‑Architected Framework’s Operational Excellence pillar. The correct concept emphasizes making small, incremental, and reversible changes to enable rapid feedback, reduce risk, and support continuous improvement through automation and monitoring. The distractors refer to other cloud advantages or different pillars: global reach (performance/reliability), IAM (security), and reducing hardware spend (cost optimization).  
Domaine  
Domain 1: Cloud Concepts  
Question 41Correct  
Under the AWS shared responsibility model, which of the following is a responsibility of the customer?  
A. Shred disk drives before they leave a data center.

#### Explications

Incorrect — Physical security and hardware lifecycle tasks (including media sanitization and secure destruction of storage devices) are performed and managed by AWS as part of the infrastructure owner responsibilities. Customers do not perform physical disposal or shredding of drives in AWS data centers.  
B. Prevent customers from gathering packets or collecting traffic at the hypervisor level.

#### Explications

Incorrect — AWS is responsible for the virtualization layer and hypervisor isolation that prevents cross-tenant access to network traffic. Customers can capture traffic only within resources they control (their instances, containers, or by using VPC Flow Logs), but preventing hypervisor-level packet capture is an AWS responsibility.  
**Votre réponse est correcte**  
C. Patch the guest operating system with the latest security patches.

#### Explications

Correct — For customer-controlled compute resources, the customer is responsible for operating-system and application-level security. This includes applying OS patches and updates, configuration management, and hardening of instances (the "security in the cloud" responsibilities for IaaS-type services).  
D. Maintain security systems that provide physical monitoring of data centers.

#### Explications

Incorrect — Maintaining physical security systems, facility access controls, and environmental monitoring for data centers are responsibilities of AWS (the provider) under the "security of the cloud" portion of the shared responsibility model.  
Explication générale  
This item tests the AWS Shared Responsibility Model. AWS handles security of the cloud (physical data center security, hardware disposal, hypervisor and virtualization controls). Customers are responsible for security in the cloud for resources they manage — notably OS-level patching, application configuration, and data protection on their instances. Therefore the option concerning OS-level patching (customer-managed maintenance) is correct; the other choices describe provider responsibilities.  
Domaine  
Domain 2: Security and Compliance  
Question 42Correct  
A company needs to quickly and securely move files over long distances between its client and an Amazon S3 bucket. Which S3 feature will meet this requirement?  
A. S3 Versioning

#### Explications

S3 Versioning preserves, stores, and retrieves multiple variants of an object to enable recovery from unintended deletes or overwrites. It is a data protection feature and does not change network routing, client-to-S3 upload endpoints, or transfer performance over long distances.  
**Votre réponse est correcte**  
B. S3 Transfer Acceleration

#### Explications

Transfer Acceleration routes uploads to the nearest Amazon edge location and then carries data over Amazon’s optimized global network to the destination bucket, reducing latency and improving throughput for long-distance transfers. Clients use the s3-accelerate endpoint and benefit from TCP optimizations and edge ingress before data traverses the AWS backbone. Note there are additional charges compared with standard S3 transfers.  
C. S3ACLs

#### Explications

Les listes de contrôle d'accès (ACL) S3 sont un mécanisme d'autorisation hérité qui détermine qui peut accéder aux compartiments et aux objets. Les ACL affectent la sécurité et l'accès, mais pas le routage des données ni la vitesse de chargement ; elles ne répondent donc pas aux exigences de transfert longue distance.  
D. S3 Hiérarchisation intelligente

#### Explications

La hiérarchisation intelligente S3 est une classe de stockage qui déplace automatiquement les objets entre les niveaux d'accès optimisés en fonction des modèles d'accès. Elle optimise le coût du stockage, et non les performances réseau ; par conséquent, elle n'accélère pas les chargements sur de longues distances géographiques.  
Explication générale  
Cette question évalue la connaissance des fonctionnalités S3 permettant d'améliorer les performances des transferts réseau. L'accélération des transferts S3 exploite les points de présence et le réseau dorsal mondial d'AWS pour accélérer les chargements depuis des clients géographiquement éloignés. Les autres options (gestion des versions, listes de contrôle d'accès et hiérarchisation intelligente) concernent respectivement la protection des données, le contrôle d'accès et la gestion du stockage en fonction des coûts, sans incidence sur le routage des chargements ni sur la latence.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 43Incorrect  
Une entreprise souhaite concevoir un système de stockage centralisé pour gérer les données de configuration et les mots de passe de ses applications métier critiques. Quel service ou fonctionnalité AWS répondra à ces exigences de la manière la plus rentable ?  
**Bonne réponse**  
A. Magasin de paramètres AWS Systems Manager

#### Explications

Stocke la configuration et les secrets sous forme de paramètres de deux types (String et SecureString). Les valeurs SecureString sont chiffrées avec des clés AWS KMS, prennent en charge le versionnage et les noms hiérarchiques, et sont accessibles via l'API SSM ou les SDK. Les paramètres standard ne sont pas facturés mensuellement par secret, et des contrôles IAM précis permettent de limiter l'accès à des paramètres spécifiques, ce qui en fait l'option gérée la plus économique lorsque la rotation automatique intégrée n'est pas requise.  
**Votre réponse est incorrecte**  
B. Gestionnaire de secrets AWS

#### Explications

Ce service de gestion des secrets propose une rotation automatique, une intégration native avec les flux de travail de rotation RDS et Lambda, ainsi qu'une auditabilité. Il convient lorsque la rotation automatique et des fonctionnalités avancées de gestion du cycle de vie des secrets sont requises, mais son coût par secret le rend moins rentable pour le simple stockage de nombreuses valeurs de configuration ou de mots de passe.  
C. Configuration AWS

#### Explications

Ce service d'évaluation de la configuration et de conformité enregistre et évalue les configurations des ressources AWS au fil du temps. Il ne s'agit pas d'un service de stockage de secrets ou de paramètres et, par conséquent, il ne peut pas être utilisé pour gérer de manière centralisée les mots de passe ou la configuration des applications.  
D. Amazon S3

#### Explications

Le stockage objet S3 permet de chiffrer les données au repos et de contrôler l'accès via IAM et les politiques de compartiment, mais il ne propose pas de fonctionnalités natives de gestion des secrets telles que les types de paramètres SecureString, les contrôles d'accès par paramètre, les paramètres versionnés et les flux de travail de rotation. L'utilisation de S3 pour les secrets nécessite des outils spécifiques et engendre des coûts d'exploitation supplémentaires.  
Explication générale  
Cette question évalue vos connaissances des services AWS permettant de stocker la configuration et les secrets de manière économique. Systems Manager Parameter Store propose des paramètres SecureString chiffrés, une nomenclature hiérarchique, des contrôles d'accès IAM et un niveau standard gratuit ou peu coûteux, ce qui en fait la solution idéale lorsque la rotation intégrée n'est pas requise. Secrets Manager offre la rotation et des fonctionnalités avancées de gestion du cycle de vie, mais engendre des coûts par secret. AWS Config et S3 ne sont pas des services spécialisés dans la gestion des secrets et sont moins appropriés sans développement spécifique supplémentaire.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 44Correct  
Une entreprise doit, conformément à la réglementation, consigner et évaluer les modifications de configuration, ainsi que mettre en œuvre des actions correctives sur ses ressources AWS. Quel service AWS doit-elle utiliser ?  
**Votre réponse est correcte**  
A. Configuration AWS

#### Explications

Conçu spécifiquement pour l'enregistrement continu de la configuration des ressources (éléments de configuration) et des instantanés historiques, cet outil évalue l'état des ressources par rapport aux politiques à l'aide des règles AWS Config et des packs de conformité. Il prend également en charge la correction automatisée en invoquant des runbooks Systems Manager Automation ou des fonctions Lambda et peut publier des événements de conformité via Amazon EventBridge pour l'orchestration, répondant ainsi à l'exigence d'enregistrer, d'évaluer et de corriger les modifications de configuration à des fins de conformité.  
B. Gestionnaire de secrets AWS

#### Explications

Un service de gestion des secrets qui stocke et renouvelle automatiquement les identifiants (chiffrés avec AWS KMS) en toute sécurité. Il offre un contrôle d'accès précis et une rotation automatique. Il ne suit ni n'évalue les configurations générales des ressources AWS et ne fournit aucun cadre pour la mise en conformité de l'état des ressources.  
C. AWS CloudTrail

#### Explications

Ce service enregistre l'activité et les événements de l'API (événements de gestion et de données) à des fins d'audit, d'analyse forensique et de surveillance, et transfère les journaux vers S3, CloudWatch Logs ou CloudTrail Lake. Il offre une visibilité sur les actions effectuées, mais ne conserve pas l'historique des éléments de configuration, n'évalue pas les configurations de ressources par rapport aux règles et n'effectue pas de correction automatisée directe.  
D. Conseiller de confiance AWS

#### Explications

Ce service de vérification et de recommandation des meilleures pratiques met en évidence les améliorations possibles en matière de coûts, de performances, de sécurité et de tolérance aux pannes. Il fournit des conseils et effectue des vérifications, mais n'enregistre pas en continu l'historique détaillé des configurations ni n'exécute de processus de correction automatisés pour garantir la conformité.  
Explication générale  
Cette question permet de déterminer quel service AWS est conçu pour le suivi, l'évaluation et la correction des configurations, dans une optique de conformité. La bonne réponse est le service qui enregistre les éléments de configuration, les évalue à l'aide de règles de configuration/packs de conformité et prend en charge la correction automatisée (via SSM Automation ou Lambda). Les autres options offrent des fonctionnalités similaires : journalisation des audits d'API (CloudTrail), gestion du cycle de vie des secrets (Secrets Manager) et recommandations de bonnes pratiques (Trusted Advisor). Cependant, aucune ne combine l'enregistrement continu de la configuration, l'évaluation basée sur des règles et l'orchestration intégrée de la correction.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 45Correct  
Parmi les propositions suivantes, lesquelles constituent des recommandations de bonnes pratiques AWS pour l'utilisation d'AWS Identity and Access Management (IAM) ? (Choisissez deux réponses.)  
A. Utilisez le compte utilisateur racine AWS pour l'accès quotidien.

#### Explications

Incorrect. The root account has unrestricted, account-wide privileges and should be used only for a very small set of account-and-billing tasks. Best practice is to create individual IAM identities or roles with least-privilege policies, secure the root account with a strong password and MFA, and avoid using it for routine administration.  
B. Use access keys and secret access keys on Amazon EC2.

#### Explications

Incorrect. Placing long‑term access keys on EC2 instances risks key exposure. The recommended approach is to attach an IAM role (instance profile) to the instance so it obtains temporary, automatically rotated credentials via the AWS Security Token Service (STS), reducing the need for embedded keys.  
**Votre sélection est correcte**  
C. Rotate credentials on a regular basis.

#### Explications

Correct. Regular credential rotation reduces the time window in which compromised credentials can be exploited. Implement key/password rotation policies, use AWS Secrets Manager or Systems Manager Parameter Store for secret management, and favor temporary credentials (IAM roles) to minimize the need for static keys.  
D. Create a shared set of access keys for system administrators.

#### Explications

Incorrect. Shared access keys undermine auditing and accountability and make revocation difficult. Instead, give each administrator an individual IAM user or, preferably, grant permissions via IAM roles or federated access, and apply least-privilege policies for traceable, revocable credentials.  
**Votre sélection est correcte**  
E. Configure multi-factor authentication (MFA).

#### Explications

Correct. Enabling multi-factor authentication (MFA) adds a second factor beyond passwords, substantially reducing the risk of unauthorized access if credentials are compromised. AWS recommends enabling MFA for the root account and for privileged IAM users; MFA can be enforced via policies or conditional checks (for example, requiring aws:MultiFactorAuthPresent).  
Explication générale  
This question tests IAM security best practices. The correct choices emphasize reducing credential exposure and strengthening authentication: regularly rotating credentials limits the window of compromise, and requiring MFA adds an additional authentication factor. The incorrect options describe insecure practices (daily use of the root account, embedding or sharing long‑term access keys) that should be replaced by IAM users/roles, instance profiles, and per‑user accountability.  
Domaine  
Domain 2: Security and Compliance  
Question 46Correct  
A company wants to operate a data warehouse to analyze data without managing the data warehouse infrastructure. Which AWS service will meet this requirement?  
A. Amazon Aurora

#### Explications

Incorrect — Amazon Aurora is a managed relational database engine (MySQL/PostgreSQL-compatible) optimized for OLTP/transactional workloads. It provides features like read replicas, high availability, and an Aurora Serverless option for variable transactional capacity, but it is not designed or optimized as a petabyte-scale analytics/data warehouse service.  
**Votre réponse est correcte**  
B. Amazon Redshift Serverless

#### Explications

Correct — Amazon Redshift Serverless is a purpose-built, fully managed data warehousing service that abstracts cluster management. It automatically provisions and scales compute for analytic queries, separates storage and compute, integrates with S3/Redshift Spectrum for data lake queries, and supports SQL-based analytics, enabling large-scale analysis without managing infrastructure.  
C. AWS Lambda

#### Explications

Incorrect — AWS Lambda is a serverless compute service for running short-lived functions in response to events. It does not provide a query engine, persistent data warehousing, or the performance characteristics required for large-scale analytical workloads; it can be used in ingestion or ETL pipelines but not as the data warehouse itself.  
D. Amazon RDS

#### Explications

Incorrect — Amazon RDS provides managed relational databases for transactional applications with automated backups, patching, and vertical scaling. It is not optimized for large-scale analytical queries or petabyte-scale data warehousing; a purpose-built analytics service is more appropriate for those workloads.  
Explication générale  
The question tests selection of a fully managed data warehouse. The correct choice is the serverless data warehousing service that provides automatic provisioning, scaling, and analytics integrations so the customer need not manage infrastructure. The distractors are transactional databases or a serverless compute service, which are not intended or optimized to serve as a managed data warehouse.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 47Correct  
A company wants to discover, prepare, move, and integrate data from multiple sources for data analytics and machine learning. Which AWS serverless data integration service should the company use to meet these requirements?  
**Votre réponse est correcte**  
A. AWS Glue

#### Explications

AWS Glue is a serverless data integration service that provides automated data discovery (crawlers), a centralized Data Catalog, and managed ETL capabilities (Spark-based jobs, Glue Studio, and Glue DataBrew). These features collectively enable schema discovery, visual and programmatic data preparation, job orchestration, and movement of data between sources (S3, RDS, Redshift, JDBC sources) without provisioning infrastructure—matching the question’s requirements for discover, prepare, move, and integrate for analytics and ML.  
B. AWS Data Exchange

#### Explications

AWS Data Exchange is a marketplace for discovering and subscribing to third‑party datasets. It facilitates access and licensing of external data but does not provide serverless ETL, automated data discovery across an organization’s sources, or integrated data preparation/orchestration needed for building analytics/ML pipelines.  
C. Amazon Athena

#### Explications

Amazon Athena is a serverless interactive query service (Presto/Trino) for running SQL queries directly against data in Amazon S3, often using the AWS Glue Data Catalog for schema metadata. Athena is for querying and ad‑hoc analysis, not for automated discovery, ETL orchestration, or moving and preparing data from multiple source systems.  
D. Amazon EMR

#### Explications

Amazon EMR is a managed Hadoop/Spark cluster platform used for large‑scale distributed processing. It is oriented to heavy data processing workloads and traditionally involves cluster management (though EMR Serverless exists); it is not the serverless, metadata/catalog-driven ETL and data‑integration service that Glue provides for discovery and streamlined preparation/integration.  
Explication générale  
The scenario requires a serverless service that can discover schemas, prepare (clean/transform) data, move it between systems, and integrate multiple sources for analytics and ML. AWS Glue provides an integrated, serverless Data Catalog plus automated discovery (crawlers), visual and code-based ETL tooling, and orchestration—making it the best fit. The other options are specialized: Data Exchange for third‑party data subscriptions, Athena for querying S3 data, and EMR for cluster-based big data processing, so they don’t cover the end‑to‑end serverless ETL/discovery/integration needs.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 48Correct  
Which AWS service helps users audit API activity across their AWS account?  
**Votre réponse est correcte**  
A. AWS CloudTrail

#### Explications

CloudTrail is the service designed to provide an audit trail of AWS API activity. It records management and data-plane events made via the console, SDKs, CLI, and AWS services, supports multi-region trails and organization-level aggregation, and delivers logs to S3, CloudWatch Logs, or EventBridge for analysis, alerting, and long-term retention — all features required for auditing API activity.  
B. Amazon Inspector

#### Explications

Amazon Inspector performs automated security assessments to identify vulnerabilities and deviations from best practices on compute resources (for example EC2 instances and container images). It is not an account-wide API call logging or auditing service.  
C. AWS WAF

#### Explications

AWS WAF is a Layer 7 web application firewall that inspects and filters HTTP/S requests to protect web applications (integrates with CloudFront, ALB, API Gateway). It protects web traffic but does not provide a comprehensive audit log of AWS API calls across an account.  
D. AWS Config

#### Explications

AWS Config captures resource configuration snapshots and configuration change history to evaluate resource compliance. It is focused on resource state and compliance rules, not on recording every API call; it often relies on CloudTrail events as one of its data sources.  
Explication générale  
The question tests knowledge of which AWS service provides API-level auditing. CloudTrail is the correct choice because it is explicitly built to log API calls and related events across an account or organization and integrate with storage and monitoring services for audit, security analysis, and troubleshooting. The other options address different concerns: Inspector (vulnerability assessment), WAF (application-layer traffic protection), and Config (resource configuration and compliance), so none replace an API-auditing trace.  
Domaine  
Domain 2: Security and Compliance  
Question 49Correct  
A company needs to track the activity in its AWS accounts, and needs to know when an API call is made against its AWS resources. Which AWS tool or service can be used to meet these requirements?  
A. Amazon CloudWatch

#### Explications

CloudWatch provides metrics, logs, alarms, and operational monitoring for resources and applications. It is not designed to produce a complete, account-level audit trail of AWS API calls; it does not by itself retain the detailed, immutable history of who called which AWS API and when.  
B. Amazon Inspector

#### Explications

Amazon Inspector performs automated security assessments (vulnerability and configuration scanning) of EC2 instances, container images, and workloads. It is not an auditing service and does not record or retain a history of AWS API calls across an account.  
**Votre réponse est correcte**  
C. AWS CloudTrail

#### Explications

CloudTrail is the audit service that records, stores, and delivers a history of AWS API calls and related events across accounts and regions. It captures management events and optional data events (for services like S3 and Lambda), delivers logs to Amazon S3 (and optionally to CloudWatch Logs or EventBridge), and provides features such as log file validation and encryption for compliance — making it the correct choice for detecting when API calls occur and who made them.  
D. AWS IAM

#### Explications

AWS Identity and Access Management (IAM) defines users, groups, roles, and permissions to control access. IAM enforces and manages access but does not itself act as the auditing/logging mechanism that records API call history; that auditing is performed by services such as CloudTrail.  
Explication générale  
The question tests knowledge of AWS auditing versus monitoring and security assessment services. AWS CloudTrail is the purpose-built auditing service that records API calls and user activity (management and optional data events), enabling investigation and compliance. Other services mentioned serve different roles: CloudWatch is for operational metrics and alarms, IAM manages identities and permissions, and Inspector performs vulnerability assessments — none provide the authoritative API-level audit trail that CloudTrail does.  
Domaine  
Domain 2: Security and Compliance  
Question 50Correct  
Which AWS service can a company use to visually design and build serverless applications?  
A. AWS Lambda

#### Explications

Incorrect — This service is a serverless compute offering for running code in response to events (functions as a service). It provides execution and scaling for function code but does not provide a graphical, drag‑and‑drop environment for visually composing an entire serverless application.  
B. AWS Batch

#### Explications

Incorrect — This service orchestrates and runs batch computing workloads by managing job queues and compute environments. It is focused on high‑throughput batch jobs, not on visual application design or composing serverless architectures.  
**Votre réponse est correcte**  
C. AWS Application Composer

#### Explications

Correct — This tool provides a visual, drag‑and‑drop canvas to assemble serverless architectures and automatically generates the underlying infrastructure as code (for example, AWS SAM/CloudFormation). It speeds prototyping by letting architects connect resources (like functions, APIs, and data stores), configure integrations, and export deployable templates.  
D. AWS App Runner

#### Explications

Incorrect — This is a fully managed service to build, deploy, and run containerized web applications. It targets container-based workloads and deployment automation rather than providing a graphical designer for composing serverless services.  
Explication générale  
The question tests recognition of the AWS tool meant for visually composing serverless applications. The correct choice is the visual application composer, which lets users graphically assemble resources and exports deployable infrastructure-as-code templates. The distractors describe services with different purposes: managed function execution, batch job orchestration, and container application deployment — none provide a graphical serverless design canvas.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 51Correct  
A user wants to review all Amazon S3 buckets with ACLs and S3 bucket policies in the S3 console. Which AWS service or resource will meet this requirement?  
A. S3 Multi-Region Access Points

#### Explications

Incorrect. Multi-Region Access Points provide a single global endpoint to access S3 objects across multiple AWS Regions and simplify cross-region data access and resiliency. They do not perform analysis or listing of bucket policies or ACLs.  
B. S3 Storage Lens

#### Explications

Partially related but not sufficient. S3 Storage Lens delivers account- or organization-level metrics and dashboards (usage, activity, and some indicators such as buckets with public access) for visibility and optimization. It does not enumerate or analyze individual bucket policies and ACLs in the S3 console in the same way an access analyzer does.  
C. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

Incorrect. AWS IAM Identity Center (AWS SSO) is an identity and access management service for centralizing user sign-in and assigning permission sets across accounts. It does not inspect or report on S3 bucket policies or ACLs.  
**Votre réponse est correcte**  
D. Access Analyzer for S3

#### Explications

Correct. Access Analyzer for S3 inspects S3 bucket policies and ACLs and generates findings that identify public or cross-account access. It is integrated into the S3 console and is the intended tool to review and remediate bucket-level access configurations.  
Explication générale  
The question tests how to review S3 access controls. Access Analyzer for S3 is built to analyze bucket policies and ACLs and surface findings about public or external access directly in the S3 console, so it is the correct choice. Storage Lens provides aggregated metrics and visibility but not detailed policy/ACL findings; Multi-Region Access Points are for cross-region access; IAM Identity Center manages identities and SSO rather than inspecting S3 access settings.  
Domaine  
Domain 2: Security and Compliance  
Question 52Correct  
Which of the following is a characteristic of the AWS account root user?  
A. The root user is the only user that can be configured with multi-factor authentication (MFA).

#### Explications

Incorrect — The root account supports MFA, but it is not unique in this capability. IAM users and roles can also be protected with MFA (virtual or hardware MFA devices). AWS best practices call for enabling MFA on the root and on privileged IAM principals.  
B. The root user is the only user that can access the AWS Management Console.

#### Explications

Incorrect — AWS Management Console access can be granted to IAM users and federated identities by issuing console credentials or using federation. Console access is not limited to the root account.  
**Votre réponse est correcte**  
C. The root user is the first sign-in identity that is available when an AWS account is created.

#### Explications

Correct — The root account is the original account owner credential created when the AWS account is established; it possesses unrestricted administrative privileges (including billing and account-level settings). Because of its broad authority, AWS recommends securing it with MFA and using IAM principals with least privilege for everyday tasks.  
D. The root user has a password that cannot be changed.

#### Explications

Incorrect — The root account password can be changed through the account settings. It is not immutable; AWS recommends rotating and tightly controlling root credentials.  
Explication générale  
The item tests knowledge of the AWS account root user: the root is the original account owner credential with full, unrestricted access to the account and special privileges (billing and account settings). Correct handling is to secure the root (enable MFA, avoid routine use) and delegate regular operations to least-privilege IAM identities. The distractors are incorrect because MFA and console access are available to IAM identities and because the root password can be changed.  
Domaine  
Domain 2: Security and Compliance  
Question 53Correct  
A developer wants AWS users to access AWS services by using temporary security credentials. Which AWS service or feature should the developer use to provide these credentials?  
A. IAM policies

#### Explications

Incorrect. IAM policies are JSON documents that define permissions (allow/deny) and are attached to users, groups, or roles. Policies control what actions are allowed but do not create or issue any form of credentials. Temporary credentials are obtained by assuming roles or using STS APIs, which operate in conjunction with policies attached to the role.  
B. IAM user groups

#### Explications

Incorrect. IAM groups are a way to manage and apply permissions to multiple IAM users at once. Groups themselves do not generate credentials or issue temporary access; members still require user credentials or must assume a role (via STS) to obtain temporary credentials.  
**Votre réponse est correcte**  
C. AWS Security Token Service (AWS STS)

#### Explications

Correct. AWS Security Token Service (STS) issues temporary, limited-privilege credentials (access key ID, secret access key, and session token) via APIs such as AssumeRole, GetSessionToken, AssumeRoleWithSAML, and AssumeRoleWithWebIdentity. These credentials have configurable durations and are used for cross-account access, federation, mobile/web identity scenarios, and any workflow that requires short-lived credentials.  
D. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

Incorrect. IAM Identity Center (AWS Single Sign-On) centralizes user access and SSO across AWS accounts and applications and integrates with external identity providers. It can result in the issuance of temporary AWS role credentials for console or CLI access, but it is a higher-level access management service; the direct issuance of programmatic temporary credentials is performed by STS (IAM Identity Center relies on underlying federation mechanisms and STS).  
Explication générale  
The question tests knowledge of how AWS issues short-lived credentials. AWS STS is the service designed to generate temporary, limited-privilege credentials (via AssumeRole, GetSessionToken, etc.), making it the correct choice. IAM policies and groups control permissions but do not create credentials, and IAM Identity Center provides SSO and access management (and uses federation mechanisms) rather than directly serving as the API for programmatic temporary credential issuance.  
Domaine  
Domain 2: Security and Compliance  
Question 54Correct  
A company wants to run relationship databases in the AWS Cloud. The company wants to use a managed service that will install the database and run regular software updates. Which AWS service will meet these requirements?  
A. Amazon S3

#### Explications

Amazon S3 is an object storage service for storing and retrieving files (objects). It does not provide a runtime for database engines, nor does it install or patch database software; at best it can store backups or exports of a database, so it does not meet the managed relational-database requirement.  
**Votre réponse est correcte**  
B. Amazon RDS

#### Explications

Amazon RDS is a purpose-built, fully managed relational database service that provisions supported engines (Aurora, MySQL, PostgreSQL, MariaDB, Oracle, SQL Server), automates engine installation, OS and database patching, backups, snapshots, automated minor-version upgrades (configurable), monitoring, and Multi-AZ high availability — satisfying the requirement for managed installation and regular software updates.  
C. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS provides persistent block-level storage for EC2 instances. It supplies durable volumes for an operating system or database files but does not manage database software, perform engine installation, or apply automated database patches; those responsibilities remain with the customer when running databases on EC2.  
D. Amazon DynamoDB

#### Explications

Amazon DynamoDB is a fully managed NoSQL key-value and document database optimized for low-latency, high-scale workloads. It is not a relational SQL database and does not provide the relational database engines or relational-database-specific patching and management required by this question.  
Explication générale  
The question asks for a managed service that installs and maintains relational databases, including running regular software updates. Amazon RDS is explicitly designed to provision and manage relational database engines and automate patching, backups, and maintenance. The other choices are either storage services (S3, EBS) or a NoSQL database (DynamoDB) and therefore do not provide the managed relational database runtime and automated patching that RDS does.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 55Correct  
A company wants to integrate its online shopping website with social media login credentials. Which AWS service can the company use to make this integration?  
A. AWS Directory Service

#### Explications

AWS Directory Service is for provisioning and managing Microsoft Active Directory-compatible directories in AWS (or proxying to on‑prem AD via AD Connector). It provides domain join, LDAP/Kerberos integration, and directory services for AWS resources — it does not offer OAuth/OIDC-based federation or a hosted consumer sign-in flow for social identity providers.  
B. AWS Identity and Access Management (IAM)

#### Explications

IAM controls authentication and authorization for AWS accounts and resources using IAM users, roles, policies, and temporary credentials (STS). It is not designed to authenticate external consumer users or to federate with social media identity providers for website sign‑in.  
**Votre réponse est correcte**  
C. Amazon Cognito

#### Explications

Amazon Cognito provides user pools (a user directory and authentication engine with a hosted UI) and identity pools (federated identities) and supports OAuth 2.0/OpenID Connect. It natively integrates with social identity providers (Facebook, Google, Login with Amazon, OIDC/SAML) and issues tokens/credentials suitable for consumer-facing social login on websites and mobile apps.  
D. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

AWS IAM Identity Center (AWS Single Sign‑On) is aimed at workforce SSO and managing single sign‑on access to AWS accounts and enterprise applications via corporate IdPs (SAML/OIDC). It is not intended to be used as a consumer-facing social login solution for public websites.  
Explication générale  
This item tests identity and authentication choices for consumer-facing applications. Amazon Cognito is the correct service because it supplies user pools, a hosted sign-in UI, OAuth/OIDC support, and built-in federation with social identity providers, enabling social logins for websites. The other services (directory services, IAM, and IAM Identity Center) address enterprise directory, AWS account access, or workforce SSO and do not provide the consumer-oriented social login flows Cognito offers.  
Domaine  
Domain 2: Security and Compliance  
Question 56Correct  
Which AWS service will help a company plan a migration to AWS by collecting the configuration, usage, and behavior data of on-premises data centers?  
A. AWS Resource Groups

#### Explications

Incorrect. Resource Groups is a management construct for organizing and operating AWS resources (tag-based grouping) and does not perform discovery of on‑premises servers, collect configuration, utilization, or dependency data required for migration planning.  
**Votre réponse est correcte**  
B. AWS Application Discovery Service

#### Explications

Correct. AWS Application Discovery Service is purpose-built to discover on‑premises environments by collecting server inventory, configuration details, resource utilization, and dependency information (via agent or agentless collectors). Its output supports migration planning and integration with AWS Migration Hub and other migration tools.  
C. AWS Service Catalog

#### Explications

Incorrect. AWS Service Catalog is used to create and manage approved catalogs of IT services for provisioning in AWS; it does not collect on‑premises configuration, usage, or dependency data for migration assessment.  
D. AWS Systems Manager

#### Explications

Incorrect. AWS Systems Manager provides operational management (Inventory, Run Command, Patch Manager) and can manage hybrid resources, but it is not the primary service for large‑scale discovery and dependency mapping used specifically for migration planning.  
Explication générale  
This question tests knowledge of AWS migration discovery tools. AWS Application Discovery Service is the appropriate service because it collects detailed on‑premises inventory, utilization, and dependency data (agent or agentless) to inform migration strategy and integrate with migration workflows. The other options are management/provisioning tools (resource grouping, Service Catalog, Systems Manager) that do not provide the comprehensive discovery and dependency mapping needed for migration planning.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 57Correct  
Which statements accurately describe the relationships among components of AWS global infrastructure? (Choose two.)  
A. There are more AWS Regions than Availability Zones.

#### Explications

Incorrect. AWS Regions are geographic areas that contain multiple Availability Zones (AZs). AZs are distinct, fault-isolated locations within Regions, so the total number of AZs is greater than the number of Regions.  
**Votre sélection est correcte**  
B. There are more edge locations than AWS Regions.

#### Explications

Correct. Edge locations are CloudFront/Route 53/Global Accelerator points of presence (PoPs) and regional edge caches deployed widely to cache and deliver content close to users. AWS operates many more PoPs than it does Regions.  
C. An edge location is an Availability Zone.

#### Explications

Incorrect. Edge locations are CDN/DNS PoPs used for caching and routing at the network edge. Availability Zones are isolated data center locations inside a Region that provide compute, storage, and networking for services like EC2, EBS, and RDS — they are different concepts and serve different purposes.  
D. There are more AWS Regions than edge locations.

#### Explications

Incorrect. Because edge locations (PoPs and regional edge caches) are deployed extensively to reduce latency worldwide, their count exceeds the number of Regions; therefore Regions do not outnumber edge locations.  
**Votre sélection est correcte**  
E. There are more Availability Zones than AWS Regions.

#### Explications

Correct. Each Region comprises multiple Availability Zones that are designed for fault isolation and connected by low-latency links; as a result, the aggregate number of AZs is larger than the number of Regions.  
Explication générale  
Cette question porte sur les relations au sein de l'infrastructure globale d'AWS. Les régions sont des zones géographiques qui regroupent plusieurs zones de disponibilité (donc le nombre de zones de disponibilité est supérieur au nombre de régions). Les points de présence (CloudFront/PoP et caches régionaux) sont déployés à grande échelle et sont plus nombreux que les régions. Les options B et E décrivent correctement ces relations ; les autres options inversent les nombres ou confondent différents composants d'infrastructure.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 58Correct  
Quel service AWS est un service de stockage cloud hybride qui offre aux utilisateurs sur site un accès à un stockage cloud pratiquement illimité ?  
A. AWS DataSync

#### Explications

DataSync est un service accéléré, basé sur des agents, permettant le transfert et la synchronisation de grands ensembles de données entre le stockage local et AWS (S3, EFS, FSx). Il est conçu pour optimiser les déplacements de données (tâches ponctuelles ou récurrentes), et non pour présenter le stockage cloud comme un point de terminaison de stockage local et permanent pour les applications sur site.  
B. Amazon S3 Glacier

#### Explications

Glacier désigne un service de stockage d'archives à long terme et à faible coût sur Amazon S3, conçu pour les données rarement consultées et les récupérations différées. Sa finalité et ses caractéristiques d'accès (flux de travail d'archivage/récupération) le rendent inadapté comme solution hybride offrant un accès immédiat sur site à une capacité cloud quasi illimitée.  
**Votre réponse est correcte**  
C. Passerelle de stockage AWS

#### Explications

Fournit des interfaces d'appliance locale ou virtuelle (Fichier : NFS/SMB, Volume : iSCSI, Bande : VTL) qui mettent en cache les données sur site tout en stockant les données principales sur Amazon S3. Cette architecture offre aux applications sur site un accès à faible latence avec la capacité quasi illimitée de stockage S3, ainsi qu'une intégration avec IAM et KMS pour la sécurité — correspondant exactement à la capacité de stockage hybride décrite.  
D. Amazon Elastic Block Store (Amazon EBS)

#### Explications

EBS propose des volumes durables au niveau bloc qui s'attachent aux instances EC2 au sein d'une même zone de disponibilité. Il n'est pas exposé aux serveurs sur site et ne fournit pas d'interface de stockage hybride accessible sur site et reposant sur un stockage cloud quasi illimité.  
Explication générale  
La question porte sur les capacités de stockage hybride d'AWS. La solution adéquate offre des interfaces sur site (fichier, bloc, bande), une mise en cache locale pour une faible latence et une persistance dans le cloud sur Amazon S3 pour une capacité quasi illimitée — des fonctionnalités fournies par la gamme Storage Gateway. Les autres options sont plus spécialisées : DataSync permet de transférer des données entre environnements, Glacier est dédié à l'archivage avec des délais de récupération, et EBS est un stockage bloc attaché à EC2, limité au cloud.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 59Correct  
Une entreprise exploitant des serveurs sur site décide de lancer une nouvelle activité. Elle détermine que des serveurs supplémentaires sont nécessaires pour les nouvelles charges de travail. Quel avantage du cloud computing peut l'aider à provisionner cette infrastructure supplémentaire le plus rapidement possible ?  
A. Bénéficier d'économies d'échelle massives

#### Explications

Les économies d'échelle désignent les avantages de coûts liés aux opérations à grande échelle et aux remises accordées par les fournisseurs, qui permettent de réduire le coût unitaire au fil du temps. Il s'agit d'un avantage financier et opérationnel, et non d'un mécanisme permettant la mise en place immédiate et à la demande d'infrastructures supplémentaires.  
**Votre réponse est correcte**  
B. Augmenter la vitesse et l'agilité

#### Explications

Cloud providers expose self-service, on-demand APIs, consoles, and infrastructure-as-code tools that let teams launch compute, storage, and networking resources in minutes without purchasing hardware. AWS examples include Amazon EC2 for on-demand instances, AWS CloudFormation and AWS CDK for automated provisioning, and Auto Scaling for elasticity—collectively enabling rapid rollout of new infrastructure and faster time-to-market.  
C. Trade fixed expense for variable expense

#### Explications

Shifting from fixed (capital) expenses to variable (operational) expenses describes the billing model of cloud consumption (pay-as-you-go). This provides financial flexibility but does not by itself explain how infrastructure can be provisioned quickly.  
D. Go global in minutes

#### Explications

Global deployment capabilities let organizations run workloads in multiple regions to reduce latency and reach customers worldwide. While related to speed of expansion across geographies, it is not the primary concept for quickly provisioning additional infrastructure for a new workload in the near term—the key enabler is on-demand provisioning and elasticity.  
Explication générale  
The question tests a core cloud benefit: the ability to provision infrastructure rapidly. The cloud enables self-service, on-demand provisioning and elasticity (via services and automation tools) so new compute and storage can be instantiated in minutes without hardware procurement. The distractors refer to other cloud advantages—economies of scale and OpEx/CapEx conversion are cost-related benefits, and global reach concerns geographic deployment—none directly explain the immediate provisioning capability.  
Domaine  
Domain 1: Cloud Concepts  
Question 60Correct  
Which benefits does a company gain when the company moves from on-premises IT architecture to the AWS Cloud? (Choose two.)  
**Votre sélection est correcte**  
A. Reduced or eliminated tasks for hardware troubleshooting, capacity planning, and procurement

#### Explications

Correct. Migrating to AWS transfers responsibility for the physical data-center hardware and its maintenance to AWS and lets the customer consume on-demand compute, storage, and managed services. Features such as EC2, RDS, autoscaling, and managed services reduce procurement cycles, eliminate physical hardware troubleshooting for the customer, and simplify capacity planning through elasticity and pay-as-you-go scaling.  
B. Elimination of the need for trained IT staff

#### Explications

Incorrect. Moving to the cloud reduces certain operational tasks but does not remove the need for skilled personnel. Cloud environments still require architects, engineers, and operators to design, configure, secure, automate, and optimize services, manage costs, and ensure compliance.  
C. Automatic security configuration of all applications that are migrated to the cloud

#### Explications

Incorrect. AWS does not automatically configure security for customer applications. Security is a shared responsibility: AWS manages the security of the cloud (infrastructure), while customers are responsible for security in the cloud (configuration, access control, application security). AWS provides tools (IAM, Security Hub, GuardDuty, Inspector, Config) to help, but customers must implement and maintain security settings.  
D. Elimination of the need for disaster recovery planning

#### Explications

Incorrect. Disaster recovery planning remains a customer responsibility. AWS provides resilient building blocks (multi-AZ, multi-region architectures, backups, snapshots, Route 53 failover, AWS Backup), but customers must design DR strategies, define RTO/RPO, and implement recovery procedures.  
**Votre sélection est correcte**  
E. Faster deployment of new features and applications

#### Explications

Correct. The AWS Cloud enables faster delivery by providing on-demand resources, automation, and managed platforms. Infrastructure-as-Code (CloudFormation, CDK), CI/CD services (CodePipeline, CodeDeploy), serverless (Lambda) and container services (ECS, EKS) accelerate provisioning, testing, and deployment, reducing time to market.  
Explication générale  
The question tests core cloud benefits: operational offload and increased agility. The correct choices reflect that AWS assumes responsibility for physical hardware and offers on-demand, automatable services that speed deployment. The incorrect options mistake cloud convenience for elimination of customer responsibilities (staffing, security configuration, and disaster recovery planning), whereas AWS provides tools and infrastructure but customers must architect, configure, and operate their workloads.  
Domaine  
Domain 1: Cloud Concepts  
Question 61Incorrect  
A new AWS user needs to interact with AWS Support by using API calls. Which AWS Support plan will meet this requirement MOST cost-effectively?  
A. AWS Basic Support

#### Explications

Incorrect — The Basic support tier does not provide programmatic access to AWS Support. It offers documentation, whitepapers, forums, and basic account/billing assistance but no AWS Support API or ability to create/manage support cases via API calls.  
**Bonne réponse**  
B. AWS Developer Support

#### Explications

Correct — The Developer support tier is the lowest-cost paid plan that includes the AWS Support API, allowing programmatic creation, description, and management of support cases and related support operations. It is intended for users experimenting or developing on AWS who need API access without the broader, higher-cost operational features of higher tiers.  
**Votre réponse est incorrecte**  
C. AWS Business Support

#### Explications

Incorrect — Business support does include the AWS Support API and production-grade features (faster response times, expanded Trusted Advisor checks, 24/7 access to Cloud Support Engineers), but its pricing and feature set are aimed at production environments, making it less cost-effective if only API access is required.  
D. AWS Enterprise Support

#### Explications

Incorrect — Le support aux grandes entreprises offre l'ensemble de services le plus complet (gestionnaire de compte technique, assistance personnalisée, SLA premium et accès API) conçu pour les grandes organisations complexes. Son coût élevé et ses services axés sur les grandes entreprises dépassent les besoins d'un nouvel utilisateur nécessitant uniquement une interaction de support automatisée.  
Explication générale  
Cet élément permet de déterminer quels plans de support AWS incluent l'API de support AWS et lequel est le plus rentable pour un accès programmatique. Les niveaux payants, à partir de Developer, offrent un accès à l'API de support ; Developer est le plan le plus économique permettant la création et la gestion programmatiques des demandes de support. Les niveaux Business et Enterprise offrent également un accès à l'API, mais ajoutent des services coûteux, orientés production, et des SLA plus rapides, inutiles pour un nouvel utilisateur dont le seul besoin est l'interaction avec l'API.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 62Correct  
Une entreprise exploite une application monolithique sur site qui ne passe pas à l'échelle et dont la maintenance est complexe. Elle prévoit de migrer cette application vers AWS et de la décomposer en microservices. Quelle bonne pratique du framework AWS Well-Architected suit-elle dans le cadre de ce plan ?  
A. Intégrer les tests fonctionnels dans le cadre du déploiement AWS.

#### Explications

Ce document décrit l'intégration de tests fonctionnels automatisés dans les pipelines de déploiement (CI/CD). Il s'agit d'une bonne pratique DevOps/d'automatisation prise en charge par AWS CodePipeline, CodeBuild et les frameworks de test, mais elle ne répond pas à l'objectif architectural de décomposition d'un monolithe en services indépendants.  
B. Utilisez l'automatisation pour déployer les modifications.

#### Explications

L'automatisation (CI/CD, IaC) est importante pour des déploiements cohérents et des mises en production plus rapides (par exemple, CloudFormation, AWS CDK, CodeDeploy), mais il s'agit d'une pratique opérationnelle plutôt que du principe architectural fondamental requis pour diviser un monolithe en composants fonctionnant indépendamment.  
C. Déployer l'application sur plusieurs emplacements.

#### Explications

Le déploiement sur plusieurs sites augmente la disponibilité et la reprise après sinistre (multi-AZ, multi-région, Route 53, Global Accelerator), mais ne modifie pas en soi le couplage entre les composants ni ne permet une décomposition indépendante des services.  
**Votre réponse est correcte**  
D. Mettre en œuvre des dépendances faiblement couplées.

#### Explications

Le faible couplage réduit les dépendances entre les composants, permettant ainsi à chaque service d'être développé, déployé, mis à l'échelle et restauré indépendamment. Ce principe de conception, propre aux architectures performantes, est mis en œuvre à l'aide de modèles et de services AWS tels que API Gateway, Amazon SQS/SNS, EventBridge, Lambda et les services de conteneurs (ECS/EKS) afin de minimiser les dépendances synchrones et fortes et de réduire l'impact des incidents.  
Explication générale  
Le projet de découper une application monolithique en microservices illustre le principe de Well-Architected qui consiste à implémenter des dépendances faiblement couplées. Ce faible couplage permet un développement, un déploiement, une mise à l'échelle et une isolation des pannes indépendants. Les autres options (tests, automatisation du déploiement, déploiement multi-sites) constituent des pratiques opérationnelles pertinentes, mais ne décrivent pas directement l'objectif architectural de réduction du couplage entre les services qui motive la migration vers les microservices.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 63Correct  
Which AWS service or feature can be used to create a private connection between an on-premises workload and an AWS Cloud workload?  
A. Amazon Route 53

#### Explications

Amazon Route 53 is a DNS service (including private hosted zones for VPCs) and is used for name resolution and routing policies; it does not provide a dedicated or private network link between on-premises infrastructure and AWS.  
B. Amazon Macie

#### Explications

Amazon Macie is a data security and data privacy service that discovers and protects sensitive data in Amazon S3; it is not a networking or connectivity service and cannot create private network connections.  
**Votre réponse est correcte**  
C. AWS Direct Connect

#### Explications

AWS Direct Connect provides a dedicated, private network connection from an on-premises location to AWS. It supports private virtual interfaces to connect directly to VPCs (bypassing the public internet), offers consistent bandwidth and lower latency, and can integrate with AWS Transit Gateway for scalable on‑premises to multi-VPC connectivity — making it the correct choice for creating private on‑premises to AWS connections.  
D. AWS PrivateLink

#### Explications

AWS PrivateLink (interface VPC endpoints) enables private connectivity to AWS services and partner services from within a VPC without using the public internet, but it is limited to traffic inside the AWS network and VPC-level endpoints; it does not itself establish a direct, dedicated link from an on-premises data center to AWS.  
Explication générale  
This question tests knowledge of AWS connectivity options. AWS Direct Connect is the managed service specifically designed to create a dedicated, private network link between on‑premises environments and AWS VPCs (option C). The other options are unrelated to establishing a dedicated on‑premises-to‑AWS connection: Route 53 is DNS, Macie is a data security service, and PrivateLink is for private in‑cloud service endpoints rather than a physical or dedicated on‑premises connection.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 64Correct  
Which AWS service helps deliver highly available applications with fast failover for multi-Region and Multi-AZ architectures?  
A. AWS WAF

#### Explications

AWS WAF is an application-layer (Layer 7\) firewall that protects HTTP/S endpoints from common exploits and malicious requests. It does not provide traffic routing, health checks, or cross-Region failover capabilities needed to deliver highly available multi-Region applications.  
**Votre réponse est correcte**  
B. AWS Global Accelerator

#### Explications

Global Accelerator provides global anycast IPs and routes user traffic over the AWS global network to healthy endpoints. It continuously monitors endpoint health and shifts traffic across Availability Zones and Regions within milliseconds, enabling faster failover and more consistent performance than DNS-based approaches for multi-Region, multi-AZ architectures.  
C. AWS Shield

#### Explications

AWS Shield is a managed service for DDoS protection (Shield Standard and Shield Advanced) that defends network and application layers from volumetric and protocol attacks. Shield protects availability from attacks but does not perform traffic routing or automated cross-Region failover for application endpoints.  
D. AWS Direct Connect

#### Explications

AWS Direct Connect offre des connexions réseau privées dédiées entre vos sites et AWS afin de réduire la latence et de garantir une bande passante constante. Il s'agit d'un service de connectivité, et non d'un mécanisme de routage du trafic global ou de basculement pour la disponibilité des applications multirégionales.  
Explication générale  
Ce test évalue vos connaissances des services AWS assurant le routage du trafic global et un basculement rapide. AWS Global Accelerator est la solution idéale car il exploite le réseau mondial AWS, les adresses IP anycast et des contrôles d'intégrité continus pour rediriger rapidement le trafic entre les points de terminaison à travers les zones de disponibilité et les régions. Les autres options sont axées sur la sécurité (WAF, Shield) ou la connectivité privée (Direct Connect) et ne proposent pas les capacités de basculement multirégional rapide et automatique requises ici.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 65Correct  
Quel service AWS est un service de gestion de la posture de sécurité du cloud (CSPM) qui agrège les alertes provenant de divers services AWS et produits partenaires dans un format standardisé ?  
**Votre réponse est correcte**  
A. AWS Security Hub

#### Explications

Security Hub centralise et normalise les résultats de sécurité provenant des services AWS et des produits tiers au format AWS Security Finding Format (ASFF). Il effectue des contrôles de posture automatisés et continus (conformément aux normes CIS et PCI), prend en charge l'agrégation inter-comptes via AWS Organizations et fournit un tableau de bord unique ainsi que des intégrations de flux de travail pour l'investigation et la correction.  
B. Conseiller de confiance AWS

#### Explications

Trusted Advisor fournit des recommandations de bonnes pratiques en matière de coûts, de performances, de sécurité et de tolérance aux pannes. Ses résultats sont des recommandations et non une agrégation et une normalisation continues et standardisées des constats de sécurité ; il ne s’agit donc pas d’un agrégateur CSPM.  
C. Amazon EventBridge

#### Explications

EventBridge est un bus d'événements sans serveur utilisé pour acheminer et distribuer des événements entre les services AWS et les applications personnalisées. Il peut transporter des événements de sécurité, mais n'exécute pas de fonctions CSPM telles que les contrôles de posture continus, la normalisation des vulnérabilités (ASFF) ou un tableau de bord de sécurité centralisé.  
D. Amazon GuardDuty

#### Explications

GuardDuty est un service de détection des menaces qui analyse différentes sources de données (journaux de flux VPC, CloudTrail, DNS) et génère des rapports de sécurité. Il s'agit d'une source de détections et non d'un agrégateur de gestion de la posture de sécurité ; les résultats de GuardDuty sont généralement transmis à une solution CSPM comme Security Hub pour centralisation et normalisation.  
Explication générale  
La question porte sur le service CSPM qui agrège et normalise les alertes provenant des services AWS et de ses partenaires. Security Hub est conçu à cet effet : il collecte les résultats, les normalise au format ASFF, assure des contrôles continus et une visibilité centralisée, et s’intègre aux autres sources de sécurité AWS. Les autres options sont liées à ce sujet, mais ne sont pas des agrégateurs CSPM (Trusted Advisor \= recommandations, EventBridge \= routage des événements, GuardDuty \= détection des menaces/source des résultats).  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 66Correct  
Une entreprise souhaite permettre à ses employés de travailler à distance depuis leur domicile. Ces employés utilisent des ordinateurs de bureau Windows ou Linux. Ils doivent pouvoir accéder à leurs ressources depuis n'importe où et à tout moment, depuis n'importe quel appareil compatible. Quel service AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Espaces de travail Amazon

#### Explications

WorkSpaces propose des bureaux virtuels cloud persistants et gérés pour Windows et Linux, accessibles via des applications natives ou un navigateur web. Il prend en charge l'authentification d'entreprise (AWS Directory Service, AD Connector ou Active Directory), chiffre le trafic réseau et externalise la maintenance, les correctifs et la mise à l'échelle du système d'exploitation vers AWS, garantissant ainsi un accès sécurisé depuis n'importe quel appareil compatible.  
B. Amazon AppStream 2.0

#### Explications

AppStream 2.0 propose des applications en flux continu (principalement des applications Windows) plutôt que des environnements de bureau complets et persistants. Optimisé pour l'accès aux applications et le streaming par session, il ne fournit pas l'expérience de bureau virtuel polyvalente requise pour les flux de travail multi-bureaux.  
C. Espaces de clés Amazon (pour Apache Cassandra)

#### Explications

Amazon Keyspaces est un service de base de données géré compatible avec Apache Cassandra. Il est indépendant des solutions d'accès à distance ou de bureau à distance et ne propose ni espace de travail utilisateur ni fonctionnalités de bureau à distance.  
D. AWS Cloud9

#### Explications

AWS Cloud9 est un environnement de développement intégré basé sur un navigateur permettant d'écrire, d'exécuter et de déboguer du code. Il fournit des espaces de travail pour les développeurs dédiés aux tâches de codage, et non des bureaux virtuels Windows/Linux complets destinés à l'accès distant des employés.  
Explication générale  
Cette question évalue les connaissances sur les offres de calcul AWS destinées aux utilisateurs finaux. Amazon WorkSpaces est la solution de bureau à distance gérée idéale pour fournir des bureaux persistants Windows ou Linux accessibles depuis de nombreux appareils et emplacements clients. AppStream 2.0 diffuse des applications (et non des bureaux complets), Cloud9 est un environnement de développement intégré (IDE) et Keyspaces est un service de base de données ; aucun de ces services ne propose l’expérience de bureau à distance généraliste requise.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 67Correct  
Une entreprise souhaite utiliser un service AWS pour lui fournir des recommandations de produits basées sur les données de ses clients. Quel service AWS répond à ce besoin ?  
A. Amazon Polly

#### Explications

Incorrect. Ce service se concentre sur la synthèse vocale à partir de texte et n'inclut pas de fonctionnalités pour l'entraînement de modèles de recommandation, l'ingestion d'ensembles de données d'interaction utilisateur-article ou la fourniture de recommandations de produits personnalisées.  
**Votre réponse est correcte**  
B. Amazon Personnaliser

#### Explications

Tout à fait. Il s'agit d'un service d'apprentissage automatique entièrement géré, conçu spécifiquement pour la personnalisation et les recommandations. Il entraîne des modèles sur des données utilisateur, article et interaction, effectue l'ingénierie des caractéristiques et l'optimisation des hyperparamètres automatisées, et propose une inférence en temps réel et par lots (campagnes et traitements par lots) pour renvoyer des listes d'articles classées et personnalisées.  
C. Amazon Comprendre

#### Explications

Incorrect. Ce service propose des fonctionnalités de traitement automatique du langage naturel (extraction d'entités, analyse des sentiments, identification des expressions clés, modélisation thématique) pour l'analyse de texte ; il ne permet pas d'entraîner ni de diffuser des modèles de recommandation personnalisés.  
D. Reconnaissance d'Amazon

#### Explications

Incorrect. Ce service propose l'analyse d'images et de vidéos (détection d'objets/visages/textes, reconnaissance de scènes, modération) et ne fournit pas de fonctionnalités pour la création ou la diffusion de systèmes de recommandation de produits.  
Explication générale  
Ce test évalue vos connaissances des offres d'IA/ML d'AWS pour la personnalisation. Amazon Personalize est le service entièrement géré idéal pour créer des recommandations de produits personnalisées à partir des données client (utilisateurs, articles, interactions) et pour diffuser ces recommandations en temps réel ou par lots. Les autres options sont des services d'IA spécialisés (synthèse vocale, traitement automatique du langage naturel, analyse d'images et de vidéos) qui ne proposent ni l'entraînement de modèles de recommandation ni le classement personnalisé.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 68Correct  
Laquelle des propositions suivantes décrit le mieux l'avantage d'utiliser le framework AWS Well-Architected lors de la conception de solutions cloud ?  
**Votre réponse est correcte**  
A. Il propose un ensemble de bonnes pratiques pour la gestion des coûts, la sécurité, la fiabilité, la performance et l'excellence opérationnelle.

#### Explications

Le cadre AWS Well-Architected propose un ensemble structuré de bonnes pratiques, organisé en cinq piliers (excellence opérationnelle, sécurité, fiabilité, performance et optimisation des coûts). Il permet d'analyser les charges de travail via l'outil AWS Well-Architected, d'identifier les risques et les compromis de conception, et de générer des recommandations de correction priorisées afin d'aider les architectes à améliorer la sécurité, les coûts, les performances, la fiabilité et l'exploitation de leurs solutions cloud.  
B. Elle garantit que tous les services AWS sont configurés de manière sécurisée sans effort supplémentaire.

#### Explications

Incorrect : le cadre propose des conseils et des processus de révision, mais ne configure pas automatiquement les ressources. La mise en place et l’application de configurations sécurisées nécessitent des services et des contrôles tels qu’AWS IAM, AWS Config (règles), AWS Security Hub, AWS Control Tower, Organizations ou des outils de déploiement/configuration automatisés (CloudFormation, CDK).  
C. Il s'agit d'un outil utilisé exclusivement pour migrer des applications sur site existantes vers AWS.

#### Explications

Incorrect : le framework n’est pas un outil de migration. Les services dédiés à la migration incluent AWS Application Migration Service, Migration Hub et Database Migration Service. Le framework Well-Architected sert à concevoir et à évaluer des architectures pour toute charge de travail (y compris les charges de travail migrées), et non à effectuer la migration elle-même.  
D. Il automatise le déploiement d'applications sur l'infrastructure AWS.

#### Explications

Incorrect : ce framework n’automatise pas le déploiement. Le déploiement et l’intégration continue/déploiement continu (CI/CD) sont gérés par des services tels qu’AWS CloudFormation, AWS CDK, AWS CodePipeline/CodeDeploy et Elastic Beanstalk. Ce framework fournit des recommandations architecturales et opérationnelles, mais n’exécute pas les déploiements.  
Explication générale  
Cette question évalue votre connaissance du cadre AWS Well-Architected. La bonne réponse est celle qui le décrit comme un ensemble structuré de bonnes pratiques réparties en cinq piliers et un processus d'analyse (via l'outil Well-Architected) permettant d'identifier les risques et de recommander des améliorations. Les autres options sont trompeuses et confondent les recommandations avec la configuration automatisée, les outils de migration ou l'automatisation du déploiement — des fonctionnalités fournies par d'autres services AWS.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 69Correct  
Une entreprise souhaite exécuter une partie de sa charge de travail dans le cloud AWS. Pour des raisons de conformité, elle doit également conserver une partie de cette charge dans son centre de données sur site. Quel service AWS répond à ces exigences ?  
A. AWSConfig

#### Explications

Incorrect. AWS Config est un service de suivi des ressources et d'audit de conformité qui enregistre l'état de la configuration et évalue les modifications apportées aux comptes AWS. Il ne fournit ni ressources de calcul sur site, ni matériel AWS géré dans un centre de données client, ni extension des API AWS pour exécuter des charges de travail localement. Par conséquent, il ne peut pas répondre à l'exigence de conserver les charges de travail sur site.  
**Votre réponse est correcte**  
B. Postes avancés AWS

#### Explications

Exactement. AWS Outposts fournit du matériel de calcul et de stockage géré par AWS, installé dans le centre de données du client, et expose les mêmes API, services et outils de gestion AWS que dans les régions AWS. Cela permet d'exécuter des charges de travail localement pour répondre aux exigences de résidence des données, de conformité ou de faible latence, tout en s'intégrant au plan de contrôle AWS.  
C. Voile lumineuse Amazon

#### Explications

Incorrect. Amazon Lightsail est un service simplifié d'hébergement VPS et d'applications fonctionnant exclusivement dans les régions AWS. Il permet de déployer facilement des instances et de gérer des ressources. Il n'étend pas l'infrastructure AWS aux centres de données sur site et ne permet pas les déploiements hybrides.  
D. Amazon Connect

#### Explications

Incorrect. Amazon Connect est un centre de contact basé sur le cloud (SaaS) utilisé pour les interactions clients. Il n'a rien à voir avec la fourniture d'infrastructures sur site ou de capacités de calcul hybrides et ne répond donc pas à la condition.  
Explication générale  
Cette question évalue vos connaissances sur les options de déploiement hybride d'AWS. La bonne réponse est le service qui étend l'infrastructure, les API et les services AWS au centre de données du client, permettant ainsi l'exécution locale des charges de travail pour répondre aux exigences de conformité ou de résidence des données. Les autres options sont les services AWS d'audit de configuration, l'hébergement VPS cloud simple ou les fonctionnalités de centre de contact ; aucune de ces solutions ne propose d'infrastructure hybride ou de calcul gérée sur site.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 70Correct  
Une entreprise a une charge de travail temporaire et variable. Elle doit utiliser des instances Amazon EC2 pour la gérer. Ces instances doivent pouvoir traiter des pics de charge de travail courts et continus. Quelle option d'achat répond à ces exigences ?  
A. Exemples ponctuels

#### Explications

La capacité Spot correspond à de la capacité EC2 disponible à un prix très réduit, mais qui peut être récupérée par AWS avec un préavis très court (les notifications d'interruption d'une instance EC2 Spot sont envoyées quelques minutes à l'avance). Étant donné que le fournisseur peut mettre fin à ces instances en cas de besoin, cette option est inadaptée aux charges de travail qui doivent s'exécuter jusqu'à leur terme sans interruption.  
**Votre réponse est correcte**  
B. Instances à la demande

#### Explications

L'option EC2 à paiement à l'usage offre une capacité facturée à la seconde, sans engagement à long terme. Les instances restent en cours d'exécution jusqu'à ce que vous les arrêtiez ou les supprimiez (elles ne sont pas récupérées par AWS pour optimiser les coûts). Ce fonctionnement la rend idéale pour les charges de travail temporaires et variables, ainsi que pour les pics d'activité de courte durée qui ne peuvent être interrompus.  
C. Plan d'épargne

#### Explications

Savings Plans are a pricing commitment that exchange predictable spend for lower rates; they change how you are billed, not the interruption behavior or capacity guarantees of instances. They do not provide temporary capacity or protect a workload from being interrupted.  
D. Reserved Instances

#### Explications

Reserved Instances (and their billing constructs) provide discounted pricing in exchange for a 1‑ or 3‑year commitment to usage attributes; they are a cost/commitment mechanism, not a guarantee of non‑interruptible short‑term capacity. (Note: Capacity Reservations are a separate feature if you need guaranteed capacity.)  
Explication générale  
This question evaluates knowledge of EC2 purchase and pricing options. The correct pay‑as‑you‑go purchase model is best because it provides dedicated instance lifecycle and immediate capacity without long‑term commitment, ensuring short, non‑interruptible bursts complete. The distractors either allow interruptions (spot) or are pricing/commitment constructs intended for predictable, long‑term usage (Savings Plans, Reserved Instances) and therefore do not meet the requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 71Correct  
A company is planning its migration to the AWS Cloud. The company is identifying its capability gaps by using the AWS Cloud Adoption Framework (AWS CAF) perspectives. Which phase of the cloud transformation journey includes these identification activities?  
A. Envision

#### Explications

Incorrect. The Envision phase is about defining the high-level business vision, objectives, and cloud strategy (business case, priorities, and desired outcomes). It does not include the detailed, perspective-by-perspective capability assessment needed to identify specific gaps and readiness issues.  
**Votre réponse est correcte**  
B. Align

#### Explications

Correct. This phase performs a current‑state assessment against the AWS CAF perspectives (business, people, governance, platform, security, operations), maps required capabilities, surfaces gaps and dependencies, and produces a prioritized roadmap and target operating model to address those gaps before migration.  
C. Scale

#### Explications

Incorrect. The Scale phase focuses on expanding adoption, operationalizing best practices, automating, and optimizing workloads at scale after initial migration and readiness work. It is not the stage for first identifying capability gaps via the CAF perspectives.  
D. Launch

#### Explications

Incorrect. The Launch phase is concerned with executing migrations, deployments, and go‑live activities following planning and readiness. Identifying capability gaps is preparatory work that occurs earlier, not during launch.  
Explication générale  
This question tests which transformation phase uses the AWS CAF perspectives to identify capability gaps. The correct phase performs a current‑state assessment across CAF perspectives, identifies capability and skill gaps, and creates a roadmap to address them—preparing the organization for migration. The other options relate to setting high‑level vision (Envision), executing migrations (Launch), or expanding/optimizing post‑adoption (Scale), so they do not fit the described activity.  
Domaine  
Domain 1: Cloud Concepts  
Question 72Correct  
Quelle tâche incombe à AWS, selon le modèle de responsabilité partagée d'AWS ?  
A. Appliquer les correctifs du système d'exploitation invité aux instances Amazon EC2.

#### Explications

La maintenance et la mise à jour du système d'exploitation des serveurs virtuels que vous lancez relèvent de la responsabilité du client, conformément au modèle de responsabilité partagée. AWS est responsable de l'infrastructure sous-jacente (matériel hôte, réseau et hyperviseur), mais les clients gèrent les mises à jour du système d'exploitation invité, les logiciels installés et la configuration de leurs instances.  
B. Assurer le suivi des systèmes de gestion de l'information sur les ressources humaines (GRIRH).

#### Explications

La surveillance des applications métier (telles que les applications RH) incombe au client. AWS fournit des services de surveillance et des indicateurs d'infrastructure, mais il appartient au client d'instrumenter, d'exploiter et de gérer la surveillance spécifique à ses applications, sauf s'il utilise un service géré incluant explicitement cette fonctionnalité.  
**Votre réponse est correcte**  
C. Effectuer des sauvegardes automatisées des instances Amazon RDS.

#### Explications

Amazon RDS est un service de base de données géré ; AWS gère le plan de contrôle et de nombreuses fonctions de service. Les sauvegardes automatisées, la planification des instantanés, le stockage des sauvegardes et l’infrastructure nécessaire à la restauration à un point précis dans le temps sont inclus dans le service géré RDS. Les clients configurent toujours la durée de conservation et les paramètres associés, mais le mécanisme de sauvegarde et le stockage sont gérés par AWS.  
D. Optimiser les coûts d'exécution des services AWS.

#### Explications

Il incombe au client de maîtriser et de réduire ses dépenses AWS. AWS fournit des outils (Cost Explorer, Budgets, Trusted Advisor) et des options tarifaires, mais le choix des types d'instances, des architectures, la réduction du gaspillage et les décisions d'optimisation des coûts restent à la charge du client.  
Explication générale  
Cette question teste le modèle de responsabilité partagée d'AWS. AWS est responsable de la sécurité et des aspects opérationnels des services gérés et de l'infrastructure cloud sous-jacente ; pour Amazon RDS, cela inclut les mécanismes de sauvegarde automatisés et le stockage. Les clients sont responsables de la gestion de leurs systèmes d'exploitation invités, de la surveillance et de la gestion des applications, ainsi que des décisions d'optimisation des coûts, même si AWS fournit des outils pour les aider dans ces tâches.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 73Correct  
Quel principe de conception AWS Cloud une entreprise utilise-t-elle lorsqu'elle implémente AWS CloudTrail ?  
**Votre réponse est correcte**  
A. Activer la traçabilité.

#### Explications

AWS CloudTrail enregistre et fournit un historique quasi complet des appels d'API AWS et de l'activité du compte (événements de gestion et événements de données optionnels), générant ainsi une piste d'audit immuable qui peut être conservée dans Amazon S3, analysée avec CloudWatch Logs/Events et AWS Athena, et intégrée à AWS Config et à la surveillance de la sécurité. Cette journalisation et cette auditabilité offrent la visibilité et les preuves nécessaires aux organisations pour les enquêtes de sécurité, les rapports de conformité et le dépannage opérationnel.  
B. Utiliser des architectures de calcul sans serveur.

#### Explications

This option describes an architectural choice to favor managed, event-driven compute services that reduce operational overhead (for example, AWS Lambda, Fargate). That design principle concerns how you build applications, not how you capture and audit account-level API activity; CloudTrail is a logging/audit service rather than a serverless compute pattern.  
C. Perform operations as code.

#### Explications

This refers to treating operational procedures as code using tools such as AWS CloudFormation, the AWS CDK, or automation pipelines to provision and manage resources. Those practices automate change and improve repeatability, but they do not by themselves provide the audit trail and API-recording capabilities that CloudTrail provides.  
D. Go global in minutes.

#### Explications

This principle focuses on designing systems for rapid, global reach using multiple AWS Regions and edge services (for example, Amazon CloudFront and multi-region deployments). While CloudTrail can be enabled across regions, the principle of rapid global deployment is about distribution and latency, not about capturing API activity and audit logs.  
Explication générale  
CloudTrail provides account- and API-level logging, giving organizations the visibility, auditability, and forensic data required for security, compliance, and operational investigation — the core idea being enablement of traceability. The other options describe unrelated design goals (serverless architectures, infrastructure-as-code, and global deployment) that do not themselves create the audit trail CloudTrail delivers.  
Domaine  
Domain 2: Security and Compliance  
Question 74Correct  
A systems administrator wants to monitor the CPU utilization of a company's Amazon EC2 instances. Which AWS service can provide this information?  
A. AWS Config

#### Explications

AWS Config records and tracks the configuration state and changes of AWS resources to support compliance auditing and configuration history. It does not collect or report operational performance metrics (such as CPU utilization) from running instances.  
B. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor runs best-practice checks and gives optimization recommendations for cost, security, fault tolerance, and performance. It provides guidance and checks, but it does not act as a metrics collection service for continuous CPU utilization monitoring.  
C. AWS CloudTrail

#### Explications

AWS CloudTrail captures API calls and management events for auditing, security analysis, and operational troubleshooting. It logs who did what and when, but it does not collect runtime resource metrics like EC2 CPU utilization.  
**Votre réponse est correcte**  
D. Amazon CloudWatch

#### Explications

Amazon CloudWatch is the dedicated monitoring service that collects, stores, and visualizes metrics and logs. For EC2 it provides CPUUtilization metrics (with basic five-minute granularity, optional one-minute detailed monitoring or agent-provided custom metrics), supports dashboards and alarms, and can trigger automated responses—making it the correct choice for monitoring CPU usage.  
Explication générale  
Cette question évalue vos connaissances des services de surveillance AWS. Amazon CloudWatch est le service approprié car il est conçu pour collecter et générer des rapports sur les métriques opérationnelles (notamment l'utilisation du processeur EC2), créer des tableaux de bord et déclencher des alertes. Les autres options répondent à des besoins différents : AWS Config pour la configuration des ressources et la conformité, Trusted Advisor pour les recommandations de bonnes pratiques et CloudTrail pour la journalisation des API et des événements ; aucune ne fournit de métriques continues de l'utilisation du processeur EC2.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 75Correct  
Une entreprise souhaite en savoir plus sur les avantages du cloud computing. Elle cherche à comprendre les gains d'agilité opérationnels. Comment AWS assure-t-il cette agilité à ses utilisateurs ?  
A. La capacité à garantir une haute disponibilité en déployant les charges de travail sur plusieurs régions

#### Explications

Le déploiement multirégional est une stratégie de disponibilité et de résilience qui améliore la tolérance aux pannes, la reprise après sinistre et la latence. Toutefois, il ne permet pas à lui seul le provisionnement rapide, l'itération et la flexibilité opérationnelle qui caractérisent l'agilité du cloud.  
B. Un modèle de paiement à l'utilisation pour de nombreux services et ressources

#### Explications

Un modèle de tarification au paiement à l’utilisation offre une flexibilité financière et une efficacité en termes de coûts (facturation de l’utilisation réelle), mais il s’intéresse davantage à la gestion des coûts qu’à la rapidité et à la réactivité opérationnelle (provisionnement/déprovisionnement) associées à l’agilité.  
C. La capacité de transférer la gestion de l'infrastructure vers le cloud AWS

#### Explications

L'utilisation des services gérés d'AWS peut réduire les frais généraux opérationnels et transférer la responsabilité des tâches d'infrastructure indifférenciées à AWS, mais l'agilité fait spécifiquement référence à la rapidité et à la facilité avec lesquelles les clients peuvent créer, modifier ou supprimer des ressources — des capacités rendues possibles par les API à la demande, l'automatisation et l'infrastructure en tant que code plutôt que par le simple déchargement de la gestion.  
**Votre réponse est correcte**  
D. La capacité à allouer et à déprovisionner rapidement des ressources avec un minimum d'efforts

#### Explications

L'agilité sur AWS repose sur le provisionnement et le déprovisionnement de ressources à la demande via la console, les API/SDK, l'interface de ligne de commande (CLI) et les outils d'automatisation (par exemple, les instances EC2 à la demande, Auto Scaling, AWS CloudFormation et les services sans serveur tels qu'AWS Lambda). Ces fonctionnalités permettent aux entreprises d'itérer, de faire évoluer et d'adapter rapidement leurs environnements avec un délai minimal.  
Explication générale  
L'atout majeur d'AWS en matière d'agilité opérationnelle réside dans sa capacité à provisionner et à supprimer rapidement des ressources à la demande, permettant ainsi une expérimentation, une mise à l'échelle et une adaptation rapides. Si les déploiements multirégionaux améliorent la disponibilité, le paiement à l'usage permet de maîtriser les coûts et les services gérés réduisent la charge opérationnelle, la capacité d'agilité déterminante demeure le provisionnement et l'automatisation rapides et fluides des ressources (option D).  
Domaine  
Domaine 1 : Concepts du cloud  
Question 76Correct  
Quel mécanisme permet aux développeurs d'accéder aux services AWS depuis le code de l'application ?  
**Votre réponse est correcte**  
A. Kit de développement logiciel AWS

#### Explications

Les SDK spécifiques à chaque langage fournissent des API programmatiques, l'intégration de fournisseurs d'informations d'identification (IAM, informations d'identification temporaires), la signature de requêtes (SigV4), des tentatives de nouvelle connexion intégrées, des assistants de pagination et des abstractions de haut niveau qui permettent au code d'application d'appeler les API de service AWS de manière fiable et sécurisée.  
B. Console de gestion AWS

#### Explications

The web-based management console is for interactive, manual resource management through a browser UI. It is not intended for embedding calls in application code or for programmatic automation.  
C. AWS CodePipeline

#### Explications

A continuous delivery service for building, testing and deploying application changes. It automates release pipelines but is not the mechanism an application uses to call AWS service APIs at runtime.  
D. AWS Config

#### Explications

A configuration-assessment and resource-auditing service that records resource states and evaluates compliance. It is used for governance and monitoring, not for providing programmatic access from application code.  
Explication générale  
Applications call AWS service APIs using language-specific SDKs that handle signing, credentials and common client behavior. The other options are management, CI/CD, or auditing tools that serve different operational purposes and do not provide the runtime programmatic libraries needed inside application code.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 77Correct  
Which AWS service or tool can be used to set up a firewall to control traffic going into and coming out of an Amazon VPC subnet?  
A. Security group

#### Explications

A stateful, instance-level virtual firewall that attaches to network interfaces (ENIs). It evaluates rules per instance and automatically allows return traffic, so it cannot enforce network controls across an entire subnet.  
B. AWS WAF

#### Explications

A web application firewall that filters HTTP(S) requests at the application layer (used with CloudFront, ALB, API Gateway, etc.). It protects web applications from common exploits but does not operate as a network-layer firewall for VPC subnets.  
C. AWS Firewall Manager

#### Explications

A centralized security management service that helps deploy and enforce firewall-related policies (for services such as WAF, Shield, and security group rules) across accounts. It manages rules and compliance but is not the subnet-level firewall that directly enforces ingress/egress on a VPC subnet.  
**Votre réponse est correcte**  
D. Network ACL

#### Explications

A stateless, subnet-level access control mechanism applied to all traffic entering and leaving a subnet. It uses ordered ingress and egress rules with explicit allow and deny entries; because it enforces rules at the subnet boundary, it is the correct choice for controlling subnet traffic.  
Explication générale  
Controlling traffic at the subnet boundary is accomplished with Network ACLs, which are stateless, subnet-level access control lists with explicit allow/deny rules for ingress and egress. Instance-level controls are stateful and attached to ENIs, WAF protects application-layer HTTP(S) traffic, and Firewall Manager centralizes policy management but does not itself act as the subnet firewall.  
Domaine  
Domain 2: Security and Compliance  
Question 78Correct  
What is a customer responsibility under the AWS shared responsibility model when using AWS Lambda?  
A. Maintenance of the underlying Lambda hardware.

#### Explications

Incorrect. AWS is responsible for the physical servers, storage, and host hardware that run AWS services. Under the shared responsibility model AWS manages hardware maintenance, not the customer.  
B. Maintenance of the Lambda networking infrastructure.

#### Explications

Incorrect. AWS operates and maintains the underlying networking infrastructure (physical network, routers, and AWS-managed network services) used by Lambda. Customers may configure VPC access and security groups for their functions, but not the low-level networking hardware maintenance.  
**Votre réponse est correcte**  
C. The code and libraries that run in the Lambda functions.

#### Explications

Correct. Customers are responsible for their function code and any libraries or dependencies they include, plus secure coding practices, dependency updates/patching, configuration (environment variables, timeouts, memory), and the IAM permissions granted to the function. These are application-level responsibilities under the shared responsibility model for serverless.  
D. The Lambda server software.

#### Explications

Incorrect. AWS manages the Lambda service software and the underlying operating systems and runtimes on the infrastructure it controls. While customers supply code and can include custom runtimes or layers, AWS is responsible for maintaining the service platform and host OS.  
Explication générale  
This question tests the shared responsibility model for serverless (AWS Lambda). AWS is responsible for the infrastructure, service software, and host maintenance; the customer is responsible for their application-level artifacts — the function code, dependencies, configuration, and access control. The correct choice identifies an application-level responsibility; the distractors describe infrastructure or service maintenance tasks that AWS manages.  
Domaine  
Domain 2: Security and Compliance  
Question 79Correct  
Which security service automatically recognizes and classifies sensitive data or intellectual property on AWS?  
A. Amazon GuardDuty

#### Explications

A threat-detection service that analyzes CloudTrail, VPC Flow Logs, and DNS logs to identify malicious or unauthorized activity; it does not inspect object contents or perform sensitive-data classification.  
**Votre réponse est correcte**  
B. Amazon Macie

#### Explications

A data security and privacy service that uses machine learning and pattern matching to discover, classify, and monitor sensitive data (for example, PII and intellectual property) stored in S3. It produces automated findings and dashboards to support data-access controls and compliance, which is why it fits this requirement.  
C. Amazon Inspector

#### Explications

An automated assessment service that scans EC2 instances, container images, and associated configurations for vulnerabilities and deviations from best practices; it assesses system and application security posture, not the contents of data objects, so it does not classify sensitive data.  
D. AWS Shield

#### Explications

A managed service that provides DDoS protection at the network and transport layers for AWS resources; its focus is attack mitigation and availability, not discovery or classification of sensitive data.  
Explication générale  
This item tests knowledge of AWS services for data discovery and protection. The correct service is the one designed to automatically discover and classify sensitive data in AWS storage (not a threat detector, vulnerability scanner, or DDoS mitigation product). That service uses machine learning and pattern matching to identify PII and intellectual property in S3 and generate findings for monitoring and access control; the other listed services address different security concerns and do not perform object-level data classification.  
Domaine  
Domain 2: Security and Compliance  
Question 80Correct  
A company is exploring the use of the AWS Cloud, and needs to create a cost estimate for a project before the infrastructure is provisioned. Which AWS service or feature can be used to estimate costs before deployment?  
A. AWS Free Tier

#### Explications

The Free Tier offers limited, no‑cost usage for selected services (12‑month and always‑free offers) to help evaluate AWS. It reduces actual charges for eligible usage but does not provide a modeling or estimation interface for forecasting costs of a planned architecture prior to deployment.  
**Votre réponse est correcte**  
B. AWS Pricing Calculator

#### Explications

This web-based modeling tool lets you compose an architecture (EC2, RDS, S3, data transfer, etc.), enter expected usage patterns, apply Savings Plan or Reserved Instance assumptions, and receive detailed monthly/annual cost breakdowns and exportable estimates. It is designed specifically for pre‑deployment cost estimation and budgeting.  
C. AWS Billing and Cost Management

#### Explications

Billing and Cost Management focuses on account billing, invoices, payment settings, and links to cost tools (Budgets, Cost Explorer). It helps manage and pay charges and configure alerts, but it is not the primary tool for building a forward-looking cost model before provisioning resources.  
D. AWS Cost and Usage Report

#### Explications

The Cost and Usage Report (CUR) provides granular historical usage and cost data for analysis, billing reconciliation, and chargeback. It is intended for post‑facto reporting and analytics, not for interactive pre‑deployment cost modeling.  
Explication générale  
The question tests knowledge of AWS cost‑estimation tools. The Pricing Calculator is the correct choice because it provides a purpose-built, configurable modeling interface to estimate costs before resources are provisioned. The other options cover free trial usage (Free Tier), account billing and alerts (Billing and Cost Management), or historical detailed usage data (Cost and Usage Report), which are useful for managing or analyzing costs after usage has occurred but not for creating upfront deployment estimates.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 81Correct  
Which option is an advantage of AWS Cloud computing that minimizes variable costs?  
A. High availability

#### Explications

Designing for redundancy, fault tolerance, and multi‑AZ/Region deployments improves uptime and resilience, but those resiliency measures usually require additional infrastructure and management and therefore do not inherently reduce per‑unit (variable) costs.  
**Votre réponse est correcte**  
B. Economies of scale

#### Explications

AWS’s large, multi‑tenant infrastructure and centralized procurement lower the provider’s per‑unit infrastructure and operational costs; those savings are passed to customers through lower unit pricing, volume discounts and flexible pricing models (pay‑as‑you‑go, Savings Plans), which directly reduce variable costs as usage grows.  
C. Global reach

#### Explications

A global footprint (Regions, Edge Locations) reduces latency and enables worldwide deployment and compliance, which improves performance and market reach but does not directly drive lower per‑unit variable costs.  
D. Agility

#### Explications

Operational agility speeds provisioning and innovation and can reduce waste from overprovisioning, but it is primarily a flexibility and time‑to‑market benefit rather than a direct mechanism for lowering a provider’s per‑unit variable costs.  
Explication générale  
The question assesses cost‑optimization benefits of cloud providers. The correct choice reflects the provider’s ability to lower per‑unit costs through large‑scale operations and centralized purchasing, which directly reduces customers’ variable costs. The other options describe real benefits (resilience, global presence, agility) but do not primarily explain reductions in variable unit costs.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 82Correct  
Who enables encryption of data at rest for Amazon Elastic Block Store (Amazon EBS)?  
A. AWS Support

#### Explications

The AWS support organization provides guidance, troubleshooting, and account assistance but does not make configuration changes within a customer’s AWS account as the primary actor. Enabling EBS encryption is a configuration action performed in the customer’s account (via console, CLI, API, or automation) and requires the appropriate IAM permissions; support can advise but does not itself enable encryption as the responsible actor.  
**Votre réponse est correcte**  
B. AWS customers

#### Explications

Enabling encryption for EBS volumes is performed by the AWS account owner or by IAM principals with the required permissions when creating volumes or by turning on default EBS encryption for the account/region. EBS uses envelope encryption and requests data keys from AWS KMS (either AWS-managed or customer-managed CMKs), but the customer initiates the encryption setting and selects/authorizes the KMS key.  
C. AWS Key Management Service (AWS KMS)

#### Explications

AWS Key Management Service (KMS) is the managed service that creates, stores, and performs cryptographic operations with customer master keys (CMKs). KMS provides and protects the keys EBS uses, but it does not itself toggle EBS encryption settings — it supplies keys and performs crypto operations on behalf of services when requested.  
D. AWS Trusted Advisor

#### Explications

Trusted Advisor performs automated checks and gives best-practice recommendations (including security-related checks) but does not change resource configurations. It can flag or recommend enabling encryption, yet it cannot enable encryption on EBS volumes by itself.  
Explication générale  
This question tests responsibility for enabling encryption at rest for an AWS service. The customer (account owner or authorized IAM principals) is responsible for enabling EBS encryption by configuring volumes or enabling default EBS encryption; AWS KMS supplies and manages the cryptographic keys used by EBS. AWS Support and Trusted Advisor can advise or recommend actions but are not the actors that enable encryption within the customer’s account.  
Domaine  
Domain 2: Security and Compliance  
Question 83Correct  
Which of the following can be components of a VPC in the AWS Cloud? (Choose two.)  
A. Amazon API Gateway

#### Explications

Amazon API Gateway is a managed API hosting service (regional or edge-optimized) and not a native VPC construct. It can integrate with resources inside a VPC using VPC Link or private integrations, but the API Gateway itself is a service endpoint outside the VPC object model.  
B. Amazon S3 buckets and objects

#### Explications

Amazon S3 is an object storage service that exists outside a VPC. Access from a VPC is achieved via public endpoints or VPC endpoints (gateway/interface), so buckets and objects are service resources, not components that reside inside a VPC.  
C. AWS Storage Gateway

#### Explications

AWS Storage Gateway is a hybrid storage appliance/service that connects on-premises environments to AWS storage. Although it can interact with VPC-hosted resources and may run on EC2 or on-premises VMs, it is not a native VPC component like subnets or gateways.  
**Votre sélection est correcte**  
D. Internet gateway

#### Explications

A horizontally scaled, redundant networking attachment that you associate with a VPC to enable IPv4/IPv6 traffic between the VPC and the internet. It appears in the VPC resource model and is referenced by route table entries to provide internet access for resources with public IPs.  
**Votre sélection est correcte**  
E. Subnet

#### Explications

A logical subdivision of a VPC's CIDR block that defines an IP address range for placing resources. Subnets determine where you launch instances and are associated with route tables, network ACLs, and other VPC configuration—making them core VPC components.  
Explication générale  
The question tests knowledge of native VPC constructs versus stand-alone AWS services. Subnets and Internet Gateways are intrinsic VPC resources used to allocate IP ranges and provide internet connectivity. API Gateway, S3, and Storage Gateway are AWS services that can interoperate with a VPC (via VPC Link or endpoints) but are not components of the VPC itself.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 84Correct  
Which of the following is a software development framework that a company can use to define cloud resources as code and provision the resources through AWS CloudFormation?  
A. AWS CLI

#### Explications

The AWS Command Line Interface is an imperative tool for calling AWS service APIs and managing resources; while it can invoke CloudFormation APIs (for example to create or update stacks), it does not provide a software development framework that models infrastructure as code and synthesizes CloudFormation templates or reusable constructs.  
B. AWS Developer Center

#### Explications

This is not an AWS service or framework for infrastructure-as-code. The phrase typically refers to documentation or developer resources, not a tool that defines resources in code or produces CloudFormation templates for provisioning.  
**Votre réponse est correcte**  
C. AWS Cloud Development Kit (AWS CDK)

#### Explications

AWS CDK is a development framework that lets developers declare infrastructure using familiar programming languages, provides higher-level reusable constructs, and performs a synthesis step that produces CloudFormation templates. Deployment uses CloudFormation stacks to provision the resulting resources, which is why it fits the question requirement.  
D. AWS CodeStar

#### Explications

AWS CodeStar is a project management and CI/CD orchestration service that helps set up development toolchains (CodeCommit, CodeBuild, CodePipeline, etc.). It supports application delivery workflows but is not a framework for authoring infrastructure-as-code that synthesizes CloudFormation templates as its primary function.  
Explication générale  
The question tests recognition of a development framework that authoritatively converts code into CloudFormation templates and relies on CloudFormation to provision resources. The AWS CDK fulfills this by letting engineers define infrastructure in programming languages, synthesizing CloudFormation templates, and deploying via CloudFormation stacks. The other choices are either tooling for API/cli access, documentation, or CI/CD project setup and do not serve as a framework that synthesizes and provisions CloudFormation templates.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 85Correct  
What does the Amazon S3 Intelligent-Tiering storage class offer?  
A. Payment flexibility by reserving storage capacity

#### Explications

Incorrect — Intelligent‑Tiering does not provide reservation-based payment or capacity reservations. AWS cost-commitment products (for example, Reserved Instances or Savings Plans) apply to compute and other services, not to S3 Intelligent‑Tiering.  
B. Long-term retention of data by copying the data to an encrypted Amazon Elastic Block Store (Amazon EBS) volume

#### Explications

Incorrect — This describes block storage (Amazon EBS). EBS volumes are attached to EC2 instances and are unrelated to S3 Intelligent‑Tiering, which is an S3 object-storage feature. Long-term archival in S3 is provided by Glacier/Deep Archive classes, not by copying to EBS.  
**Votre réponse est correcte**  
C. Automatic cost savings by moving objects between tiers based on access pattern changes

#### Explications

Correct — S3 Intelligent‑Tiering continuously monitors object access patterns and automatically moves objects between access tiers (frequent, infrequent, and available archive tiers) to lower storage costs without operational changes. It includes a small monitoring/automation charge; archive tiers can have different retrieval costs and latencies.  
D. Secure, durable, and lowest cost storage for data archival

#### Explications

Incorrect — This describes S3 Glacier or Glacier Deep Archive, which are purpose-built, very-low-cost archival storage classes with higher retrieval latencies and distinct retrieval pricing. Intelligent‑Tiering is for automatic tiering of active S3 objects, not for deep archival-only storage.  
Explication générale  
S3 Intelligent‑Tiering is an S3 storage class that optimizes cost for objects with unknown or changing access patterns by automatically moving objects between access tiers based on observed usage. It reduces the need for manual lifecycle policies. The other options describe unrelated features: reserved-capacity/payment commitments, EBS block storage, and Glacier archival storage, which serve different use cases.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 86Correct  
A company needs to host a web server on Amazon EC2 instances for at least 1 year. The web server cannot tolerate interruption. Which EC2 instance purchasing option will meet these requirements MOST cost-effectively?  
A. On-Demand Instances

#### Explications

Pay-as-you-go hourly pricing with no long-term commitment is flexible but results in the highest total cost for a steady, non-interruptible one-year workload because no reservation discount is applied.  
**Votre réponse est correcte**  
B. Partial Upfront Reserved Instances

#### Explications

A one-year reservation with a partial upfront payment produces a larger effective hourly discount than a no‑upfront reservation while retaining continuous, non‑interruptible instance use. The billing discount is applied for the term to matching instance usage, making this the most cost‑effective option among the listed choices for a steady, one‑year web server.  
C. Spot Instances

#### Explications

Pricing that uses spare EC2 capacity delivers deep discounts but is interruptible by AWS (with only short notice). Because instances can be reclaimed, this model is unsuitable for services that cannot tolerate interruption.  
D. No Upfront Reserved Instances

#### Explications

A one‑year reservation with no upfront payment does provide a discounted hourly rate versus pay‑as‑you‑go, but the total savings are typically smaller than options that require some upfront payment; therefore it is less cost‑effective than the partial‑upfront reservation when affordability of a partial upfront payment is acceptable.  
Explication générale  
The question tests selecting the most cost‑effective EC2 purchasing option for a continuous, non‑interruptible web server for at least one year. The correct choice is the reserved‑term option that combines a one‑year commitment with a partial upfront payment because it lowers the effective hourly cost while not introducing interruption. Pay‑as‑you‑go is more expensive over a year, and spare‑capacity pricing is interruptible and therefore unsuitable.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 87Correct  
Which AWS service provides on-premises applications with low-latency access to data that is stored in the AWS Cloud?  
A. Amazon CloudFront

#### Explications

Incorrect. Amazon CloudFront is a global content delivery network that caches and serves content from edge locations to end users. It optimizes delivery to clients over the internet but does not present a local storage interface (NFS/SMB/iSCSI) to on‑premises applications for direct, read/write low‑latency access to cloud‑stored data.  
**Votre réponse est correcte**  
B. AWS Storage Gateway

#### Explications

Correct. AWS Storage Gateway is a hybrid storage service that exposes cloud-backed storage through on‑premises interfaces (File Gateway for NFS/SMB, Volume Gateway for iSCSI, and Tape Gateway). It keeps a local cache of frequently accessed data so on‑premises applications can access cloud data with low latency while asynchronously persisting data to Amazon S3 or EBS snapshots in AWS.  
C. AWS Backup

#### Explications

Incorrect. AWS Backup centralizes and automates backups across AWS services and supported on‑premises resources, but it is a data protection/orchestration service for snapshots and backups—not a persistent, low‑latency storage interface for running on‑premises applications.  
D. AWS DataSync

#### Explications

Incorrect. AWS DataSync is a high‑performance, managed data transfer service for synchronizing or migrating data between on‑premises storage and AWS. It accelerates transfers and automates recurring syncs but does not provide a continuously mounted, cached storage interface that delivers persistent low‑latency access to cloud data from on‑premises applications.  
Explication générale  
This question tests knowledge of hybrid storage solutions. AWS Storage Gateway is the correct choice because it provides on‑premises protocols (NFS/SMB/iSCSI), a local cache for frequently accessed data, and seamless persistence to AWS, enabling low‑latency access to cloud‑stored data. The other options address related but different needs: CloudFront is a CDN for end‑user delivery, DataSync is for bulk/sync transfers, and AWS Backup handles backup orchestration rather than providing a live storage interface.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 88Correct  
A company wants to manage deployed IT services and govern its infrastructure as code (IaC) templates. Which AWS service will meet this requirement?  
A. AWS Resource Explorer

#### Explications

Resource Explorer provides indexed, read-only discovery and search across AWS resources (cross-account and cross-region), enabling queries and exploration. It does not provide provisioning, product portfolios, launch constraints, or template governance needed to manage and govern IaC artifacts and deployed IT services.  
**Votre réponse est correcte**  
B. AWS Service Catalog

#### Explications

Provides a centralized product catalog model where administrators publish versioned products implemented as AWS CloudFormation templates (products/artifacts within portfolios), apply launch constraints, enforce parameter constraints, control which IAM principals can provision products, and manage updates — enabling governance, standardized deployments, and lifecycle control of infrastructure-as-code-based services.  
C. AWS Organizations

#### Explications

Organizational tooling for account management, consolidated billing, organizational units, and Service Control Policies. It governs account-level permissions and billing organization structure but does not itself provide a catalog or lifecycle governance for IaC templates and deployed service artifacts.  
D. AWS Systems Manager

#### Explications

A set of operational management capabilities (Run Command, State Manager, Automation, Patch Manager, Parameter Store, Inventory) for configuring and operating instances and applications. Useful for operations and automation, but it does not offer a curated product catalog or the template/version/launch governance features required for IaC template governance.  
Explication générale  
The scenario requires centralized governance and lifecycle management of infrastructure-as-code templates and deployed IT services. The correct service implements a product/portfolio model, versioning, provisioning constraints, and access control for templates (primarily AWS CloudFormation) to standardize and control deployments. The other choices address resource discovery, account-level governance, or operational management, so they do not provide the cataloging and template governance that this requirement demands.  
Domaine  
Domain 2: Security and Compliance  
Question 89Correct  
A user wants to allow applications running on an Amazon EC2 instance to make calls to other AWS services. The access granted must be secure. Which AWS service or feature should be used?  
A. Security groups

#### Explications

Incorrect — this feature enforces network-level traffic rules (a stateful virtual firewall) for instances. It does not issue identity-based credentials or manage API permissions for applications running on the instance.  
B. AWS Firewall Manager

#### Explications

Incorrect — this service centralizes firewall and WAF/Shield policies across accounts and resources. It manages network/security policy enforcement, but it does not provide credentials or IAM-style permissions for EC2-hosted applications to call other AWS services.  
**Votre réponse est correcte**  
C. IAM roles

#### Explications

Correct — attach an IAM role (instance profile) to the EC2 instance so applications receive temporary security credentials (issued by STS) via the instance metadata service. AWS SDKs and the CLI automatically retrieve and rotate these credentials (use IMDSv2 for secure retrieval). This avoids embedding long-term keys and supports least-privilege access control.  
D. IAM user SSH keys

#### Explications

Incorrect — SSH key pairs are for host login (or IAM SSH keys used for CodeCommit) and do not grant API permissions to AWS services. Granting an IAM user long-term access keys would provide API access but is less secure than using roles with temporary credentials.  
Explication générale  
The question tests secure ways to grant EC2-hosted applications permission to call AWS services. The recommended approach is an IAM role attached to the instance (instance profile), which provides temporary, automatically rotated credentials via STS/IMDS that AWS SDKs consume. Network controls (security groups, Firewall Manager) protect connectivity but do not provide identity-based credentials; SSH keys or IAM user long-term keys are not the secure, best-practice method for service-to-service access from EC2.  
Domaine  
Domain 2: Security and Compliance  
Question 90Correct  
Which Amazon EC2 Reserved Instances term commitment will give users the MOST cost savings?  
A. 1 year

#### Explications

A shorter-term Reserved Instance commitment yields smaller hourly discounts than longer commitments. While still cheaper than on-demand pricing, shorter commitments offer less total savings compared with the longest-supported RI term.  
B. 2 years

#### Explications

AWS does not offer a two-year Reserved Instance term as a standard option; RI and Savings Plan discounts are based on the officially supported term lengths, so a two-year commitment is not applicable for maximizing RI savings.  
**Votre réponse est correcte**  
C. 3 years

#### Explications

AWS provides the largest discount for the longest supported Reserved Instance term. Committing to the maximum available RI term increases the per-hour discount (for Standard RIs especially) and therefore produces the greatest cost savings over on-demand pricing. Note that payment options (All Upfront, Partial Upfront, No Upfront) and RI type (Standard vs Convertible) also affect the effective savings, but the longer term yields the highest baseline reduction.  
D. 5 years

#### Explications

A five-year term is not offered for EC2 Reserved Instances. Because this term length is not available, it cannot provide additional savings; customers seeking long-term discounts should use the supported RI terms or Savings Plans instead.  
Explication générale  
The question tests understanding that Reserved Instances trade an instance-term commitment for reduced hourly costs. AWS supports specific RI term lengths, and the longest supported term provides the highest baseline discount, making it the best choice for maximum cost savings. Distractors are either shorter-term commitments (which offer smaller discounts) or invalid term lengths that AWS does not offer.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 91Correct  
Which option is an AWS Cloud Adoption Framework (AWS CAF) business perspective capability?  
A. Culture evolution

#### Explications

This capability is primarily about organizational change, workforce skills, roles, and cultural readiness. Those responsibilities map to the People perspective in the AWS Cloud Adoption Framework, not the Business perspective.  
B. Event management

#### Explications

This capability relates to operational processes such as monitoring, incident response, and service health — responsibilities aligned with the Operations perspective of AWS CAF rather than the Business perspective.  
**Votre réponse est correcte**  
C. Data monetization

#### Explications

This capability is about converting data assets into measurable financial and strategic value through analytics, pricing models, and new offerings. That activity aligns with the Business perspective of AWS CAF, which focuses on value realization, business case development, and outcomes measurement.  
D. Platform architecture

#### Explications

This capability focuses on infrastructure, runtime environments, and architectural design decisions. Those concerns fall under the Platform perspective of AWS CAF, which addresses technical architecture and platform services rather than business strategy.  
Explication générale  
The question tests recognition of a Business perspective capability within the AWS Cloud Adoption Framework. The correct choice describes turning organizational data into measurable business value — a core Business perspective concern (value realization, metrics, business models). The other options map to different AWS CAF perspectives: organizational change to People, operational processes to Operations, and infrastructure design to Platform, so they are not Business-perspective capabilities.  
Domaine  
Domain 1: Cloud Concepts  
Question 92Correct  
A company wants to update its online data processing application by implementing container-based services that run for 4 hours at a time. The company does not want to provision or manage server instances. Which AWS service will meet these requirements?  
A. AWS Lambda

#### Explications

Incorrect — this service is a serverless function platform but enforces a maximum execution duration (15 minutes) even when you deploy container images as functions, so it cannot host a container workload that must run for 4 hours.  
**Votre réponse est correcte**  
B. AWS Fargate

#### Explications

Correct — this service is a serverless compute engine for containers that runs tasks for Amazon ECS or EKS without provisioning or managing EC2 instances. It supports long-running container tasks, integrates with VPC, IAM, and logging, and lets you pay for the container resources used rather than managing servers.  
C. Amazon EC2

#### Explications

Incorrect — this service provides virtual machines (EC2 instances) that you must provision, configure, patch, and scale. It can run containers but does not meet the requirement to avoid server instance management.  
D. AWS Elastic Beanstalk

#### Explications

Incorrect — this platform-as-a-service simplifies deployments but typically provisions and manages underlying EC2 resources for you; it is not a serverless container runtime and therefore does not satisfy the "no server management" requirement.  
Explication générale  
The question requires a serverless container execution environment able to run multi-hour workloads without provisioning or managing servers. The serverless container engine for ECS/EKS meets that need because it runs container tasks without EC2 management and supports long-running jobs. Other choices fail because of execution time limits (serverless functions) or because they require managing EC2 instances or use managed EC2 behind the scenes (EC2, Elastic Beanstalk).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 93Correct  
To assist companies with Payment Card Industry Data Security Standard (PCI DSS) compliance in the cloud, AWS provides:  
A. Inspections physiques des centres de données sur rendez-vous.

#### Explications

Incorrect. AWS n'autorise pas les inspections physiques de ses centres de données par ses clients ; AWS publie plutôt des preuves d'audit indépendantes réalisées par des tiers (par exemple, des rapports SOC et l'AOC) qui documentent ses contrôles physiques et environnementaux. Les clients consultent ces documents d'audit au lieu d'effectuer des inspections sur site.  
B. Certifications de conformité PCI requises pour toute application exécutée sur AWS.

#### Explications

Incorrect. AWS ne certifie pas les applications clientes selon la norme PCI DSS. La conformité PCI est une responsabilité partagée : AWS est responsable de la sécurité du cloud (l’infrastructure et les services gérés concernés), tandis que les clients sont responsables de la sécurité dans le cloud (leurs applications, données et configurations) et doivent obtenir et maintenir les attestations PCI requises pour leurs charges de travail.  
**Votre réponse est correcte**  
C. un rapport d'attestation de conformité AWS (AOC) pour des services AWS spécifiques.

#### Explications

Exact. AWS fournit une attestation de conformité (AOC) pour certains services et régions AWS, accessible via AWS Artifact. L'AOC est délivrée sur la base d'audits indépendants réalisés par des tiers sur les contrôles d'AWS et atteste que les services gérés par AWS respectent les exigences PCI DSS. Les clients utilisent l'AOC pour démontrer que l'infrastructure AWS sous-jacente est conforme aux obligations PCI, tout en mettant en œuvre leurs propres contrôles applicatifs.  
D. Services professionnels de conformité PCI.

#### Explications

Incorrect. AWS fournit des conseils, des outils et un accès aux services professionnels AWS et aux partenaires APN qui peuvent conseiller sur la conformité, mais AWS n'agit pas en tant qu'organisme certificateur PCI externe du client et ne fournit pas directement de services de certification PCI pour l'environnement du client. Les clients font généralement appel à des évaluateurs ou des partenaires qualifiés pour les services de conformité formels.  
Explication générale  
Cette question évalue les connaissances relatives aux artefacts de conformité AWS et au modèle de responsabilité partagée. AWS accompagne ses clients dans leur mise en conformité PCI DSS en leur fournissant des rapports d'audit tiers et une attestation de conformité (AOC) pour les services AWS concernés, via AWS Artifact. Ces artefacts documentent les contrôles mis en place par AWS pour l'infrastructure, mais ne dispensent pas le client de sa responsabilité en matière de sécurisation de ses applications ou d'obtention de ses propres attestations PCI. Par conséquent, l'option AOC est correcte ; les autres choix décrivent soit des fonctionnalités qu'AWS ne propose pas à ses clients, soit témoignent d'une mauvaise compréhension du modèle de responsabilité partagée.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 94Correct  
Une entreprise souhaite déployer une base de données PostgreSQL sur Amazon RDS. Cette base de données doit être hautement disponible et tolérante aux pannes. Quelle solution AWS l'entreprise devrait-elle utiliser pour répondre à ces exigences ?  
A. Amazon RDS avec une seule zone de disponibilité

#### Explications

Incorrect : un déploiement mono-AZ place l’instance de base de données principale et son stockage dans une seule zone de disponibilité. Une panne dans cette zone de disponibilité entraîne une interruption de service, car il n’existe ni sauvegarde synchrone ni basculement automatique vers une autre zone de disponibilité.  
B. Instantanés Amazon RDS

#### Explications

Incorrect — Les snapshots RDS sont des sauvegardes à un instant précis stockées dans Amazon S3 à des fins de restauration et de conservation. Ils ne fournissent ni la réplication en temps réel ni le basculement automatique nécessaires à une haute disponibilité en cas de panne.  
**Votre réponse est correcte**  
C. Amazon RDS avec plusieurs zones de disponibilité

#### Explications

Exact : l’option Multi-AZ gérée provisionne une instance de secours synchrone dans une zone de disponibilité différente et effectue un basculement automatique en cas de défaillance de l’instance principale. Cela garantit la tolérance aux pannes et une interruption de service minimale pour Amazon RDS pour PostgreSQL ; notez que l’instance de secours n’est pas utilisée pour le trafic de lecture (utilisez les réplicas de lecture pour la mise à l’échelle en lecture).  
D. Service de migration de bases de données AWS (AWS DMS)

#### Explications

Incorrect — AWS Database Migration Service est conçu pour migrer ou répliquer en continu des données entre bases de données (y compris les migrations hétérogènes). Il ne s'agit pas d'une configuration de haute disponibilité avec basculement automatique géré pour une instance RDS.  
Explication générale  
La haute disponibilité et la tolérance aux pannes d'une base de données RDS PostgreSQL sont assurées par une base de données de secours synchrone gérée, située dans une zone de disponibilité différente et bénéficiant d'un basculement automatique. RDS Multi-AZ offre ce comportement. À l'inverse, les déploiements mono-AZ ne proposent pas de redondance au niveau de la zone de disponibilité, les snapshots sont des sauvegardes (et non une solution de basculement en temps réel) et DMS est un outil de migration/réplication plutôt qu'une solution de haute disponibilité RDS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 95Correct  
Selon le modèle de responsabilité partagée d'AWS, lesquelles des propositions suivantes relèvent de la responsabilité d'AWS ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. Infrastructure réseau et virtualisation de l'infrastructure

#### Explications

AWS est responsable des composants d'infrastructure qui constituent le fondement de son offre cloud, notamment les équipements réseau physiques des centres de données et la couche de virtualisation/hyperviseur qui isole les ressources de calcul des clients. Il incombe à AWS de sécuriser et de maintenir l'infrastructure cloud sous-jacente.  
B. Sécurité des données de l'application

#### Explications

La protection des données applicatives (classification, chiffrement, contrôle d'accès et gestion du cycle de vie des données) incombe au client. Ce dernier doit configurer le chiffrement, gérer les clés (ou choisir les options KMS) et appliquer des contrôles d'accès au niveau applicatif pour les données stockées ou traitées dans AWS.  
C. Systèmes d'exploitation invités

#### Explications

Le système d'exploitation invité des machines virtuelles que vous lancez (correctifs, renforcement de la sécurité, configuration et contrôles de sécurité basés sur l'hôte) est généralement de la responsabilité du client pour les ressources IaaS telles que EC2. (Remarque : pour certains services gérés, AWS gère le système d'exploitation, mais la question porte sur la répartition générale des responsabilités.)  
**Votre sélection est correcte**  
D. Sécurité physique du matériel

#### Explications

AWS est responsable de la sécurité physique des centres de données et de la protection du matériel — y compris le contrôle d'accès aux installations, la surveillance, les contrôles environnementaux et l'élimination sécurisée des équipements — dans le cadre de son obligation de maintenir une infrastructure sécurisée.  
E. Qualifications et politiques

#### Explications

La gestion des identités, des informations d'identification des utilisateurs, des politiques IAM et des contrôles d'authentification incombe au client. AWS fournit les services IAM et les services associés, mais les clients doivent créer et appliquer les informations d'identification, les rôles, les politiques et l'authentification multifacteurs pour leurs comptes et leurs ressources.  
Explication générale  
Dans le cadre du modèle de responsabilité partagée d'AWS, AWS gère la sécurité du cloud (infrastructures physiques, matériel, réseau et couches de virtualisation), tandis que les clients gèrent la sécurité dans le cloud (données, système d'exploitation invité, applications et configuration des identités et des accès). Par conséquent, la responsabilité de l'infrastructure et de la sécurité physique incombe à AWS (réponses A et D), tandis que la protection des données, la gestion du système d'exploitation et la configuration IAM restent à la charge du client.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 96Correct  
Quel groupe partage la responsabilité avec AWS en matière de sécurité et de conformité des comptes et des ressources AWS ?  
A. Fournisseurs tiers

#### Explications

Les fournisseurs tiers peuvent proposer des outils de sécurité ou des services gérés dans le cadre d'un contrat, mais ils n'assument pas automatiquement les obligations de sécurité et de conformité au niveau du compte définies par le modèle de responsabilité partagée d'AWS. Le propriétaire du compte demeure responsable de la configuration, du contrôle d'accès, de la protection des données et de la conformité, sauf s'il délègue explicitement ces responsabilités via la gestion des identités et des accès (IAM) ou des accords.  
**Votre réponse est correcte**  
B. Clients

#### Explications

Le modèle de responsabilité partagée d'AWS attribue à AWS la responsabilité de la sécurité du cloud (infrastructure physique, matériel, réseau, hyperviseur et services de base), tandis que le propriétaire du compte gère la sécurité dans le cloud (gestion des identités et des accès, configuration des ressources, chiffrement des données, application des correctifs au système d'exploitation et aux applications, et journalisation des audits). C'est pourquoi le propriétaire du compte partage les responsabilités en matière de sécurité et de conformité avec AWS.  
C. Partenaires revendeurs

#### Explications

Les partenaires revendeurs peuvent revendre ou proposer des services AWS, mais n'héritent pas automatiquement des responsabilités du client en matière de sécurité et de conformité. Tout rôle opérationnel ou administratif qu'un revendeur peut jouer doit être explicitement autorisé par le client (par exemple, via des rôles IAM ou des contrats de service) ; la responsabilité de la conformité incombe toujours au titulaire du compte.  
D. Fournisseurs d'accès Internet

#### Explications

Les fournisseurs d'accès Internet assurent la connectivité réseau et sont responsables de leur propre infrastructure et de leur transit. Ils ne sont pas parties prenantes au modèle de responsabilité partagée d'AWS et ne gèrent pas la sécurité des ressources, des configurations ou des données des comptes AWS dans le cloud.  
Explication générale  
Ce test évalue la connaissance du modèle de responsabilité partagée d'AWS : AWS sécurise l'infrastructure cloud, tandis que le titulaire du compte sécurise les ressources, les configurations, les données et les accès au sein de son compte. Par conséquent, le client/titulaire du compte est la partie qui partage la responsabilité avec AWS. Les fournisseurs tiers, les revendeurs et les FAI peuvent apporter une aide opérationnelle, mais ne sauraient se substituer aux obligations de sécurité et de conformité de base du client, sauf accord contractuel explicite.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 97Correct  
Une entreprise a besoin d'un stockage de fichiers entièrement géré, hautement fiable et évolutif, accessible via le protocole SMB (Server Message Block). Quel service AWS répond à ces exigences ?  
A. Amazon S3

#### Explications

Incorrect. Amazon S3 is object storage accessed via HTTP APIs (REST) and does not natively present an SMB network file share. Exposing S3 as an SMB share requires additional components (for example, AWS Storage Gateway File Gateway or third-party gateways), so S3 does not meet the requirement for a native, fully managed SMB file server.  
B. Amazon Elastic File System (Amazon EFS)

#### Explications

Incorrect. Amazon EFS is a POSIX-compliant, NFS-based file system designed for Linux workloads (NFSv4). It does not provide native SMB protocol support, Windows ACLs, or Active Directory integration required for Windows SMB file shares.  
**Votre réponse est correcte**  
C. Amazon FSx for Windows File Server

#### Explications

Correct. Amazon FSx for Windows File Server is a fully managed, Windows-native file system that exposes SMB shares, supports Windows ACLs and Active Directory integration, provides automated backups and durability, and scales performance and capacity—meeting the requirement for highly reliable, scalable SMB-accessible file storage.  
D. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Incorrect. Amazon EBS provides block-level storage volumes attached to EC2 instances and is not a network file system. EBS requires an operating system to host a filesystem and cannot natively present SMB shares to multiple clients, so it does not satisfy the SMB file-share requirement.  
Explication générale  
This question evaluates which AWS service natively provides a fully managed SMB network file share. Amazon FSx for Windows File Server is the appropriate choice because it is a Windows-native, SMB-compatible managed file system with AD integration and enterprise features. The other options are different storage models: S3 is object storage (no native SMB), EFS is NFS for Linux, and EBS is block storage for EC2—none offer native SMB file shares.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 98Correct  
A retail company is building a new mobile app. The company is evaluating whether to build the app at an on-premises data center or in the AWS Cloud. Which of the following are benefits of building this app in the AWS Cloud? (Choose two.)  
A. A large, upfront capital expense and low variable expenses

#### Explications

Incorrect. This describes a capital-intensive, on-premises model. AWS uses pay‑as‑you‑go pricing and managed services to minimize upfront capital expenditure and convert costs to operating expenses.  
**Votre sélection est correcte**  
B. Increased speed for trying out new projects

#### Explications

Correct. AWS enables rapid experimentation and faster time-to-market through on-demand provisioning, managed platform services, and developer tooling (for example, AWS CloudFormation, AWS Elastic Beanstalk, AWS Lambda, and CI/CD services) that remove infrastructure setup bottlenecks.  
C. Complete control over the physical security of the infrastructure

#### Explications

Incorrect. Under the AWS shared responsibility model, AWS is responsible for physical infrastructure and facility security, while customers are responsible for security in the cloud (data, identity, application configuration), so customers do not have complete control over physical security.  
**Votre sélection est correcte**  
D. Flexibility to scale up in minutes as the application becomes popular

#### Explications

Correct. AWS provides elasticity and on-demand scalability (Auto Scaling, Elastic Load Balancing, serverless scaling with AWS Lambda, etc.) so capacity can be increased or decreased in minutes to match demand.  
E. Ability to pick the specific data centers that will host the application servers

#### Explications

Incorrect. Customers select AWS Regions and Availability Zones but cannot choose specific physical data centers; placement groups and AZ selection influence instance placement but do not permit picking an individual data center.  
Explication générale  
This question tests core cloud benefits: building in AWS reduces upfront capital expense, speeds up innovation, and provides rapid, on‑demand scalability. Options B and D are correct because AWS enables quick project iteration and elastic scaling via on‑demand and managed services. The distractors conflated on‑premises characteristics (large capex), misconstrued control over physical infrastructure (shared responsibility), or overstated ability to select specific data centers (Regions/AZs only).  
Domaine  
Domain 1: Cloud Concepts  
Question 99Correct  
A company has an on-premises application. The application has processing times of less than 5 minutes and is invoked only a few times each day. The company wants to move the application to the AWS Cloud. Which AWS service will support this application MOST cost-effectively?  
A. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Elastic Container Service (ECS) is a container orchestration platform that requires packaging the app into containers and running tasks on either EC2 instances or Fargate. It introduces more operational setup and typically incurs continuous or task-level resource billing that makes it less cost‑effective than a serverless option for a few short, infrequent executions.  
**Votre réponse est correcte**  
B. AWS Lambda

#### Explications

AWS Lambda is a serverless compute service that charges based on number of requests and actual execution duration (measured in milliseconds) plus allocated memory. It requires no server provisioning, automatically scales, and supports short-lived event-driven workloads—making it the most cost-effective fit for an application invoked only a few times per day with run times under 5 minutes.  
C. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Elastic Kubernetes Service (EKS) provides managed Kubernetes, which adds control-plane and worker-node considerations and is best suited for complex container orchestration and sustained workloads. The additional operational overhead and resource footprint make it an inefficient choice for very infrequent, short tasks.  
D. Amazon EC2

#### Explications

Using virtual machines requires provisioning and managing compute instances. Even with per-second billing, running EC2 instances for an application invoked only sporadically adds management overhead and can be more expensive than a pay-per-use serverless model for short, infrequent executions.  
Explication générale  
The scenario describes a short-duration, infrequently invoked workload. Serverless compute that bills per request and execution time is the best fit because it avoids provisioning and idle-capacity costs. Lambda meets these requirements (automatic scaling, per‑millisecond billing, no infrastructure management). Container orchestration (ECS/EKS) or EC2 introduces more operational complexity and resource costs, so they are less cost‑effective for this use case.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 100Correct  
A company has deployed an Amazon EC2 instance. Which option is an AWS responsibility under the AWS shared responsibility model?  
A. Managing and encrypting application data

#### Explications

Responsibility for application data handling, encryption, and the management of encryption keys lies with the customer. AWS provides encryption services and tooling (for example AWS KMS, S3 server-side encryption, and TLS support) but the customer must decide encryption scope, configure it, and manage keys and access controls for their applications and data.  
B. Installing updates and security patches of guest operating system

#### Explications

For Amazon EC2 (IaaS), the customer is responsible for the guest operating system and the software running on the instance, including applying OS and application security patches. AWS manages the underlying host, hypervisor, and physical infrastructure, whereas patching the guest environment is a customer duty (AWS performs OS patching for some managed services such as Amazon RDS).  
**Votre réponse est correcte**  
C. Configuration of infrastructure devices

#### Explications

AWS is responsible for the physical layer and foundational infrastructure — data centers, physical servers, networking hardware, and the hypervisor — which constitute “security of the cloud.” Configuration, maintenance, and physical security of that infrastructure are managed by AWS under the shared responsibility model.  
D. Configuration of security groups on each instance

#### Explications

Security groups are virtual firewall constructs associated with ENIs/instances; customers define and manage the ingress and egress rules and attach security groups to their resources. AWS supplies the security group capability, but configuring rules and access is the customer’s responsibility.  
Explication générale  
Under the AWS shared responsibility model, AWS handles security of the cloud (physical infrastructure, network hardware, hypervisor), while customers handle security in the cloud (their data, guest OS, applications, and network rules). The correct choice reflects AWS responsibility for the underlying infrastructure; the other options describe customer responsibilities such as data encryption, OS patching, and security group configuration.  
Domaine  
Domain 2: Security and Compliance  
Question 101Correct  
A company wants to migrate its applications to the AWS Cloud. The company plans to identify and prioritize any business transformation opportunities and evaluate its AWS Cloud readiness. Which AWS service or tool should the company use to meet these requirements?  
**Votre réponse est correcte**  
A. AWS Cloud Adoption Framework (AWS CAF)

#### Explications

AWS CAF is a guidance framework that helps organizations assess cloud readiness and prioritize business transformation by analyzing gaps across its perspectives (Business, People, Governance, Platform, Security, and Operations). It provides a structured way to map capabilities, identify high-impact transformation opportunities, and create a migration/adoption roadmap aligned with business objectives.  
B. AWS Managed Services (AMS)

#### Explications

AWS Managed Services (AMS) delivers operational management and ongoing runbook-driven operations for AWS environments. It focuses on operating and managing workloads at scale, not on performing an organization-wide cloud readiness assessment or prioritizing business transformation opportunities.  
C. AWS Well-Architected Framework

#### Explications

The AWS Well-Architected Framework provides best-practice guidance to review and improve workload architectures across pillars such as security, reliability, performance efficiency, and cost optimization. It is architecture-centric and intended for workload reviews rather than for evaluating enterprise cloud readiness or business transformation strategy.  
D. AWS Migration Hub

#### Explications

AWS Migration Hub provides a centralized dashboard to track the discovery and migration progress of applications across migration tools. It helps monitor migration status and task tracking but does not provide the strategic readiness assessment or business-transformation prioritization guidance that AWS CAF does.  
Explication générale  
The question tests knowledge of tools for assessing organizational readiness and identifying transformation opportunities. AWS CAF is the correct choice because it is specifically designed to evaluate readiness across multiple perspectives and produce a prioritized adoption roadmap. The other options address different phases: AMS manages operations, Well-Architected reviews workload design, and Migration Hub tracks migration progress — none provide the holistic, business-and-people-focused readiness assessment that CAF does.  
Domaine  
Domain 1: Cloud Concepts  
Question 102Correct  
Which programming languages does AWS Cloud Development Kit (AWS CDK) currently support? (Choose two.)  
**Votre sélection est correcte**  
A. Python

#### Explications

AWS CDK provides official, first-class support for Python (CDK v2). Python apps can author CDK constructs, synthesize to CloudFormation, and use the same high-level construct libraries via jsii-generated bindings.  
B. Swift

#### Explications

Swift is not an official CDK language. CDK’s multi-language capability relies on jsii language targets, and Swift is not supported by jsii, so there are no official Swift bindings for CDK.  
**Votre sélection est correcte**  
C. TypeScript

#### Explications

TypeScript is the original and primary implementation language of the AWS CDK. Construct libraries are authored in TypeScript, offering full, native feature support and direct synthesis to CloudFormation.  
D. Ruby

#### Explications

Ruby is not an official CDK target. The jsii toolchain does not produce official Ruby bindings for the CDK, so any Ruby integrations would be community-maintained rather than part of the supported SDKs.  
E. PHP

#### Explications

PHP n'est pas officiellement pris en charge par AWS CDK. Les langages cibles officiels de CDK incluent JavaScript/TypeScript, Python, Java, .NET et Go (CDK v2) ; PHP n'en fait pas partie, bien que des projets communautaires puissent exister.  
Explication générale  
Le kit de développement logiciel AWS (CDK) prend officiellement en charge TypeScript et Python (ainsi que Java, .NET et Go dans la version 2 du CDK). TypeScript est l'implémentation native et Python bénéficie de liaisons de premier ordre générées par jsii. Les langages non pris en charge par jsii, tels que Swift, Ruby et PHP, ne sont pas des cibles officielles du CDK et ne constituent donc pas des choix appropriés.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 103Correct  
Quel service AWS offre aux utilisateurs un accès à la demande et en libre-service aux rapports de contrôle de conformité AWS ?  
A. Configuration AWS

#### Explications

AWS Config est un service de suivi et d'évaluation de la configuration des ressources qui enregistre les modifications de configuration, gère un inventaire des ressources et évalue leur conformité aux règles établies. Il contribue à la conformité continue au niveau des ressources, mais ne fournit pas d'accès à la demande aux rapports de contrôle de conformité AWS (SOC, ISO, PCI) destinés aux auditeurs.  
B. Amazon GuardDuty

#### Explications

Amazon GuardDuty est un service de détection des menaces géré qui analyse les sources de données (journaux de flux VPC, CloudTrail, journaux DNS) afin de générer des rapports de sécurité signalant les activités potentiellement malveillantes ou non autorisées. Ce service est axé sur la détection des menaces et ne permet pas de fournir des rapports de conformité AWS à la demande.  
C. Conseiller de confiance AWS

#### Explications

AWS Trusted Advisor effectue des vérifications automatisées des meilleures pratiques et fournit des recommandations en matière d'optimisation des coûts, de performances, de sécurité et de tolérance aux pannes. Il propose des conseils d'optimisation et de sécurité, mais ne constitue pas un référentiel pour les documents de conformité officiels d'AWS ni pour les rapports de contrôle.  
**Votre réponse est correcte**  
D. Artefact AWS

#### Explications

AWS Artifact est un service AWS conçu pour fournir un accès en libre-service et à la demande aux rapports de conformité AWS et à la documentation relative à la sécurité et à la conformité (par exemple, les rapports SOC, les certifications ISO et les rapports PCI). Il met à disposition les rapports et accords Artifact afin que les clients et les auditeurs puissent télécharger les attestations et documents de conformité officiels d'AWS.  
Explication générale  
Cette question permet d'identifier le service AWS offrant un accès à la demande et en libre-service aux rapports officiels de conformité AWS. La bonne réponse est le service qui sert de référentiel et de mécanisme de distribution pour les documents d'attestation et de conformité AWS. D'autres services mentionnés concernent l'audit de configuration, la détection des menaces ou les recommandations de bonnes pratiques, mais seul le service correct fournit des rapports de conformité téléchargeables pour les auditeurs et les clients.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 104Correct  
Les développeurs d'applications d'une entreprise doivent provisionner et gérer rapidement des services AWS à l'aide de scripts. Quelle offre AWS doivent-ils utiliser pour répondre à ces besoins ?  
**Votre réponse est correcte**  
A. Interface de ligne de commande AWS

#### Explications

Fournit une interface de ligne de commande unifiée pour les API AWS, conçue pour le scripting et l'automatisation. Elle permet le provisionnement et la gestion programmatiques de la quasi-totalité des services AWS, s'intègre aux pipelines CI/CD, prend en charge les profils nommés et la gestion des identifiants, et peut être appelée depuis des scripts shell ou des outils d'automatisation pour automatiser les tâches liées au cycle de vie des ressources.  
B. AWS CodeBuild

#### Explications

Un service de construction géré qui compile le code source, exécute les tests et produit les artefacts. Bien qu'il puisse exécuter des scripts dans le cadre d'un pipeline de construction et appeler les API AWS, sa vocation première est l'automatisation CI/CD/construction, et non une interface de script généraliste pour le provisionnement ad hoc et la gestion directe des ressources.  
C. Cadre d'adoption du cloud AWS (AWS CAF)

#### Explications

Ce recueil de recommandations organisationnelles, de bonnes pratiques et d'analyses des capacités facilite la planification de l'adoption du cloud. Il s'agit d'un cadre stratégique et de gouvernance qui ne fournit ni outils de programmation ni API pour provisionner ou gérer les ressources AWS.  
D. Gestionnaire de session AWS Systems Manager

#### Explications

Une fonctionnalité d'accès interactif sécurisé pour la gestion des instances en cours d'exécution et autres ressources sans ouverture de ports entrants. Elle est utilisée pour l'accès basé sur les sessions et les tâches opérationnelles sur les ressources, et non pour la création de scripts permettant le provisionnement et la gestion à grande échelle des services AWS.  
Explication générale  
Cette question évalue les connaissances relatives aux outils AWS de provisionnement programmatique. L'interface de ligne de commande est conçue spécifiquement pour la création de scripts et l'automatisation des API des services AWS ; c'est donc le choix approprié. Les autres options représentent un service de construction (utilisé pour l'intégration continue et le déploiement continu), un cadre d'accompagnement à l'adoption (stratégie/gouvernance) et un outil d'accès aux sessions (accès opérationnel). Aucun de ces outils ne constitue l'interface de script générale pour le provisionnement des ressources AWS.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 105Correct  
Une entreprise souhaite utiliser un service de calcul sans serveur pour une application. Quel service AWS répond à ce besoin ?  
**Votre réponse est correcte**  
A. AWS Lambda

#### Explications

Offre une véritable architecture de calcul sans serveur : vous déployez des fonctions qui s’exécutent à la demande en réponse à des événements, AWS gérant intégralement le provisionnement, les correctifs, la mise à l’échelle et la haute disponibilité. La facturation est basée sur les invocations et la durée d’exécution, ce qui en fait le service idéal pour exécuter du code sans gérer de serveurs.  
B. AWS CloudFormation

#### Explications

CloudFormation est un service d'infrastructure en tant que code permettant de provisionner et de gérer les ressources AWS de manière déclarative (modèles JSON/YAML). Il n'exécute pas de code applicatif et ne fournit pas d'environnement d'exécution ; il ne s'agit donc pas d'un service de calcul sans serveur.  
C. AWS Elastic Beanstalk

#### Explications

Elastic Beanstalk automatise le déploiement et la gestion des environnements applicatifs, mais provisionne et exécute les applications sur des ressources de calcul gérées (par exemple, des instances EC2 ou des conteneurs). Il s'agit d'un service de plateforme géré, et non d'un environnement d'exécution de fonctions sans serveur.  
D. Équilibrage élastique de la charge

#### Explications

Elastic Load Balancing répartit le trafic entrant entre différentes cibles (instances EC2, conteneurs, adresses IP ou, dans certaines intégrations, fonctions Lambda). Il s'agit d'un service de distribution de trafic et non d'un service de calcul ou d'exécution ; il n'exécute pas de code applicatif.  
Explication générale  
The question asks specifically for a serverless compute service. AWS Lambda is designed to run application code without provisioning or managing servers (event-driven functions, automatic scaling, per-invocation billing). The other options are distinct: CloudFormation is IaC, Elastic Beanstalk is a managed deployment platform that still uses underlying compute resources, and Elastic Load Balancing handles traffic distribution rather than providing a runtime.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 106Correct  
Which of the following is a recommended design principle of the AWS Well-Architected Framework?  
A. Reduce downtime by making infrastructure changes infrequently and in large increments.

#### Explications

Incorrect. AWS best practices emphasize reducing risk through small, frequent, and automated changes (for example via CI/CD and deployment strategies such as rolling, blue/green, or canary releases) rather than infrequent, large updates that increase blast radius.  
B. Invest the time to configure infrastructure manually.

#### Explications

Incorrect. Manual configuration is error-prone and not scalable. The Well‑Architected approach recommends automation and Infrastructure as Code (IaC) — e.g., AWS CloudFormation or AWS CDK — plus automated deployment pipelines to ensure repeatability and consistency.  
**Votre réponse est correcte**  
C. Learn to improve from operational failures.

#### Explications

Correct. This reflects the Operational Excellence pillar of the AWS Well‑Architected Framework: use telemetry, post-incident reviews, runbooks, and continuous improvement to learn from failures and iterate on processes and architecture (tools include Amazon CloudWatch, AWS X‑Ray, AWS Config, etc.).  
D. Use monolithic application design for centralization.

#### Explications

Incorrect. The framework favors designing for loose coupling, modularity, and scalability; while monolithic designs can be appropriate in some cases, they are not a recommended general principle compared with decoupled/microservices or serverless patterns that improve scalability and resilience.  
Explication générale  
The question tests knowledge of the AWS Well‑Architected Framework, specifically the Operational Excellence pillar. Learning from operational failures (C) is a core recommended practice because it drives continuous improvement using telemetry, reviews, and runbooks. The distractors reflect practices that are contrary to Well‑Architected guidance (large infrequent changes, manual configuration) or context‑dependent architectural choices (monolith vs. decoupled designs).  
Domaine  
Domain 1: Cloud Concepts  
Question 107Correct  
A company has data lakes designed for high performance computing (HPC) workloads. Which Amazon EC2 instance type should the company use to meet these requirements?  
A. General purpose instances

#### Explications

M-series (general purpose) instances provide a balanced mix of CPU, memory, and networking for a wide range of workloads. For CPU-bound, high-throughput HPC tasks they typically deliver lower sustained per-core performance and worse price-performance than instance families optimized specifically for compute.  
**Votre réponse est correcte**  
B. Compute optimized instances

#### Explications

Compute-optimized families (for example C5/C6/C7 variants) provide high vCPU-to-memory ratios, higher clock speeds, and are tuned for CPU-bound workloads. They support enhanced networking (ENA) and many variants can use Elastic Fabric Adapter (EFA) for low-latency, high-throughput inter-node communication — features that improve performance and price-performance for HPC workloads.  
C. Memory optimized instances

#### Explications

Memory-optimized instances (R/X families) provide large amounts of RAM for memory-bound workloads like in-memory databases and analytics. They are optimized for capacity and memory throughput rather than raw CPU/core performance, so they are not the ideal choice when the workload is primarily CPU-bound HPC.  
D. Storage optimized instances

#### Explications

Storage-optimized instances (I family and similar) deliver very high local NVMe throughput and IOPS for data-intensive I/O tasks (databases, data lakes, heavy local storage). Their design prioritizes I/O and storage throughput rather than delivering the highest CPU performance per core required by compute-heavy HPC jobs.  
Explication générale  
The key factor for HPC in EC2 is raw CPU performance, high vCPU counts, and low-latency networking for tightly coupled jobs. Compute-optimized instances provide those characteristics (high clock speeds, favorable vCPU-to-memory ratios, ENA/EFA support), giving better performance and price-performance for CPU-bound HPC. General purpose is balanced, memory-optimized targets RAM-heavy workloads, and storage-optimized targets I/O-heavy workloads — none are as suited as compute-optimized for pure compute-intensive HPC tasks.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 108Correct  
An online gaming company needs to choose a purchasing option to run its Amazon EC2 instances for 1 year. The web traffic is consistent, and any increases in traffic are predictable. The EC2 instances must be online and available without any disruption. Which EC2 instance purchasing option will meet these requirements MOST cost-effectively?  
A. On-Demand Instances

#### Explications

Incorrect — On‑Demand is best for short‑term, variable, or unpredictable workloads because it requires no up‑front commitment. For a predictable, year‑long, always‑on requirement it is more expensive than term‑based purchasing options.  
**Votre réponse est correcte**  
B. Reserved Instances

#### Explications

Correct — Reserved Instances (RIs) provide substantial hourly cost discounts in exchange for a one‑ or three‑year commitment. When scoped to a specific Availability Zone (zonal RIs) they can also reserve capacity to help ensure instance availability, making RIs the most cost‑effective choice for steady, predictable, always‑on EC2 usage over one year.  
C. Spot Instances

#### Explications

Incorrect — Spot Instances deliver the deepest discounts by using spare EC2 capacity but are interruptible (with a short warning) when AWS needs the capacity back. This interruption behavior makes them unsuitable for workloads that require guaranteed, continuous availability.  
D. Spot Fleet

#### Explications

Incorrect — Spot Fleet automates provisioning across Spot (and optionally On‑Demand) Instances to meet capacity targets at low cost. However, if configured primarily with Spot it inherits Spot interruption risk; it does not by itself guarantee uninterrupted, reserved capacity unless mixed with non‑interruptible options.  
Explication générale  
This item tests knowledge of EC2 purchasing models for a steady, predictable, one‑year workload that must remain online. Reserved Instances (one‑year term) offer the best cost savings for predictable, always‑on instances and can provide capacity reservation when purchased zonally. On‑Demand is flexible but costlier for long‑term steady usage; Spot options are inexpensive but interruptible and therefore not appropriate for guaranteed availability.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 109Correct  
A company wants to use AWS. The company has stringent requirements about low-latency access to on-premises systems and data residency. Which AWS service should the company use to design a solution that meets these requirements?  
A. AWS Wavelength

#### Explications

AWS Wavelength places compute at telecom 5G edge locations to reduce latency for mobile devices and applications that need proximity to cellular networks. It is not designed to host customer-managed infrastructure inside a company’s on‑premises datacenter, nor does it guarantee data residency in the customer’s country or physical control over where data is stored.  
B. AWS Transit Gateway

#### Explications

AWS Transit Gateway is a regional network hub that simplifies routing between VPCs and on‑premises networks (via VPN or AWS Direct Connect). It addresses connectivity and routing, but it does not provide local, on‑premises AWS compute/storage nor a mechanism for keeping data physically within a customer’s own facility for residency or the ultra‑low local latency achieved by colocated hardware.  
C. AWS Ground Station

#### Explications

AWS Ground Station is a managed service for contacting and receiving data from satellites. Its purpose is satellite communications and downlink processing, so it is unrelated to providing on‑premises compute, low‑latency access to internal systems, or data residency controls for enterprise datacenters.  
**Votre réponse est correcte**  
D. AWS Outposts

#### Explications

AWS Outposts delivers AWS-managed hardware installed in the customer’s facility that exposes many of the same AWS APIs, services, and management plane as in the AWS Region. Because the racks run locally, applications get native AWS compute and storage with single‑digit millisecond access to on‑premises systems, and data can remain physically in the customer’s location to meet residency requirements while still integrating with the AWS control plane.  
Explication générale  
This question tests knowledge of hybrid deployment options for meeting stringent low‑latency and data‑residency requirements. The correct solution is the service that brings AWS-managed compute and storage physically into the customer’s datacenter so workloads can access local systems with minimal latency and retain data on premises. The distractors provide edge networking (Wavelength), routing/connectivity (Transit Gateway), or satellite services (Ground Station), none of which deliver on‑premises AWS infrastructure for residency and local latency guarantees.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 110Correct  
When a user wants to utilize their existing per-socket, per-core, or per-virtual machine software licenses for a Microsoft Windows server running on AWS, which Amazon EC2 instance type is required?  
A. Spot Instances

#### Explications

Spot Instances are spare, interruptible EC2 capacity offered at a discount. They do not guarantee dedicated physical tenancy or host-level visibility, and their ephemeral nature and lack of control over the underlying server prevent compliance with per-socket, per-core, or per-VM license tracking requirements.  
B. Dedicated Instances

#### Explications

Dedicated Instances run on single-tenant hardware (tenant isolation) but do not provide host-level visibility or explicit control over physical sockets/cores. Because you cannot inventory and assign specific physical resources, they are not suitable for meeting license reporting and allocation requirements associated with per-socket or per-core BYOL scenarios.  
**Votre réponse est correcte**  
C. Dedicated Hosts

#### Explications

Dedicated Hosts allocate an entire physical server to a single AWS account, exposing host attributes (sockets, cores, host ID) and providing APIs to manage instance placement. This visibility and control allow customers to map and track per-socket, per-core, or per-VM Windows Server licenses to physical resources, meeting Microsoft licensing requirements for BYOL.  
D. Reserved Instances

#### Explications

Reserved Instances are a billing construct that provide a pricing discount for long-term instance usage; they do not change tenancy or provide physical server allocation or visibility, so they do not enable the license-tracking and compliance features required for BYOL of per-socket/core/VM licenses.  
Explication générale  
The question tests knowledge of EC2 tenancy and license compliance. Bringing existing per-socket, per-core, or per-VM Windows Server licenses requires physical-host allocation and host-level visibility so licenses can be mapped to sockets/cores—capabilities provided by Dedicated Hosts. The other options address pricing (Reserved Instances), ephemeral capacity (Spot), or basic single-tenant isolation without host visibility (Dedicated Instances), and therefore do not satisfy BYOL license-tracking requirements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 111Correct  
Which AWS tool gives users the ability to plan their service usage, service costs, and instance reservations, and also allows them to set custom alerts when their costs or usage exceed established thresholds?  
A. Cost Explorer

#### Explications

Cost Explorer provides interactive visualizations, historical cost and usage reports, forecasts, and recommendations (for example, RI and Savings Plan purchase suggestions). It is an analysis and reporting tool, not a budget/alerting system, so it does not provide threshold-based notifications.  
**Votre réponse est correcte**  
B. AWS Budgets

#### Explications

AWS Budgets enables creation of cost, usage, reservation, and Savings Plan budgets and can trigger notifications (email or Amazon SNS) and automated budget actions when thresholds are exceeded. It is the primary AWS service for planning spend, tracking reservations, and receiving custom alerts.  
C. AWS Cost and Usage Report

#### Explications

The AWS Cost and Usage Report delivers the most granular billing and usage data to Amazon S3 for downstream analysis and integration with analytics tools. It is a raw data export and does not itself provide budget threshold alerts or notification workflows.  
D. Reserved Instance reporting

#### Explications

Reserved instance reporting (utilization and coverage reports) focuses on measuring how effectively reserved capacity is being used and whether coverage is sufficient. It helps with reservation optimization but does not serve as a general-purpose budgeting/alerting tool.  
Explication générale  
The question targets AWS cost-management capabilities. AWS Budgets is designed specifically to plan costs and reservations and to send custom alerts when cost or usage thresholds are breached. Other tools mentioned—Cost Explorer, the Cost and Usage Report, and RI reporting—provide analysis, raw billing data, or reservation metrics but do not replace Budgets for proactive threshold-based notifications.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 112Correct  
A company wants to migrate its on-premises infrastructure to the AWS Cloud. Which advantage of cloud computing will help the company reduce upfront costs?  
A. Go global in minutes

#### Explications

This option describes rapid global deployment using AWS Regions and Edge Locations, which improves latency and reach. It addresses deployment speed and geographic availability rather than reducing upfront capital expenditure required for migration.  
B. Increase speed and agility

#### Explications

Improving speed and agility reduces time-to-market and enables faster iteration, but it does not by itself eliminate large initial capital purchases for servers, networking, or datacenter facilities.  
C. Benefit from massive economies of scale

#### Explications

AWS achieves lower unit costs through massive economies of scale (shared infrastructure and multitenancy), which lowers ongoing prices over time. However, this is a longer-term cost advantage and does not directly substitute for the capital investment reduced at the start of a migration.  
**Votre réponse est correcte**  
D. Trade fixed expense for variable expense

#### Explications

Moving from capital expenditure (CapEx) to operational expenditure (OpEx) lets organizations avoid large up-front investments in hardware and datacenter facilities. AWS pay-as-you-go pricing (On-Demand, Savings Plans, Reserved Instances) and managed services (EC2, S3, RDS, etc.) enable consumption-based billing, reducing initial procurement and provisioning costs during migration.  
Explication générale  
Le principal avantage de la migration vers le cloud pour réduire les coûts initiaux réside dans la transformation des investissements initiaux en dépenses opérationnelles récurrentes, basées sur l'utilisation. Ce modèle de consommation élimine la nécessité d'acheter et de provisionner d'importantes quantités de matériel avant le lancement des charges de travail. Les autres avantages mentionnés – couverture mondiale, agilité accrue et économies d'échelle – sont certes des atouts réels d'AWS, mais ne visent pas directement à réduire les dépenses initiales de la même manière.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 113Correct  
Une entreprise souhaite recevoir des alertes pour suivre ses coûts d'exploitation globaux pour son infrastructure de cloud public AWS. Quelle offre AWS répond à ces exigences ?  
A. Amazon EventBridge

#### Explications

EventBridge est un service de routage d'événements permettant de concevoir des architectures événementielles et d'intégrer des applications et des fournisseurs SaaS. Il ne propose pas de tableaux de bord de suivi des coûts intégrés ni d'alertes de dépassement de seuil budgétaire ; il ne constitue donc pas l'offre AWS principale pour le suivi des coûts d'exploitation globaux d'AWS.  
B. Calcul des plans d'épargne

#### Explications

Les forfaits d'économies de calcul sont un engagement tarifaire qui réduit les coûts de calcul en échange d'un engagement d'utilisation prévisible. Ils modifient les tarifs de facturation, mais ne proposent aucune fonctionnalité de suivi, de seuillage ou d'alerte pour les coûts récurrents.  
**Votre réponse est correcte**  
C. Budgets AWS

#### Explications

AWS Budgets vous permet de définir des budgets de coûts, d'utilisation, d'utilisation des instances réservées/plans d'économie et de réservation, de définir des seuils (réels ou prévisionnels) et d'envoyer des notifications par e-mail ou via les réseaux sociaux en cas de dépassement de ces seuils. Il est spécifiquement conçu pour surveiller les dépenses et alerter les parties prenantes lorsque les coûts approchent ou dépassent les montants budgétés.  
D. Évaluateur de migration

#### Explications

Migration Evaluator (anciennement TSO Logic) est un outil de découverte et d'évaluation permettant d'estimer les coûts de migration et de planifier l'adoption du cloud. Il génère des estimations de coûts et des recommandations de dimensionnement, mais n'est pas conçu pour un suivi continu des coûts ni pour l'envoi d'alertes sur les coûts opérationnels.  
Explication générale  
Il est nécessaire de surveiller en continu les coûts d'exploitation du cloud et de recevoir des alertes en cas de dépassement des seuils de dépenses. AWS Budgets est conçu spécifiquement pour ce cas d'utilisation : il prend en charge les budgets de coûts et d'utilisation, les alertes prévisionnelles et les notifications. Les autres options concernent le routage d'événements (EventBridge), les engagements tarifaires (Compute Savings Plans) ou les évaluations de migration (Migration Evaluator), mais aucune ne propose la fonctionnalité d'alerte budgétaire continue offerte par Budgets.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 114Correct  
Une entreprise souhaite estimer le coût de sa solution d'architecture AWS avant la migration. Quel service ou fonctionnalité AWS répond à ce besoin ?  
A. Détective Amazon

#### Explications

Incorrect — Amazon Detective est un service d'analyse de sécurité qui agrège et analyse des données (telles que les journaux de flux VPC, AWS CloudTrail et les résultats d'Amazon GuardDuty) afin d'aider à identifier la cause première des problèmes de sécurité. Il ne propose ni modèles de tarification ni outils de prévision des coûts d'architecture ; il ne peut donc pas être utilisé pour l'estimation des coûts avant migration.  
B. Budgets AWS

#### Explications

Incorrect — AWS Budgets is used to set cost, usage, Reserved Instance, and Savings Plan budgets and to trigger alerts when actual spending or usage deviates from those budgets. It is a monitoring and control tool for ongoing spend management after resources are deployed, not a modeling tool for estimating expected costs before migration.  
C. AWS Resource Explorer

#### Explications

Incorrect — AWS Resource Explorer provides a searchable inventory and metadata view of resources across accounts and regions to help locate and manage resources. It does not include pricing calculators or cost‑modeling capabilities, so it cannot generate upfront cost estimates for an architecture.  
**Votre réponse est correcte**  
D. AWS Pricing Calculator

#### Explications

Correct — The AWS Pricing Calculator is the dedicated online tool for creating detailed cost estimates before deployment. It lets you model services and configurations, input expected usage patterns, produce line‑item monthly and annual cost breakdowns, and export or share estimates for planning and budgeting during migration.  
Explication générale  
This question tests recognition of the AWS tool designed for upfront cost modeling. The AWS Pricing Calculator is purpose‑built to model service configurations and expected usage to produce detailed cost estimates prior to migration. The other options address different needs: Amazon Detective for security investigation, AWS Budgets for post‑deployment cost monitoring and alerts, and AWS Resource Explorer for resource discovery — none provide pre‑deployment pricing estimation features.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 115Correct  
Which AWS Support plans provide access to an AWS technical account manager (TAM)? (Choose two.)  
A. AWS Basic Support

#### Explications

Basic (free) support is limited to account and billing assistance, access to documentation, whitepapers, and the Service Health Dashboard; it does not provide technical support staff or a dedicated Technical Account Manager (TAM).  
B. AWS Developer Support

#### Explications

Developer Support targets developers with guidance for development and test environments, offering business-hours access to Cloud Support Associates and higher-touch technical help than Basic, but it does not include a dedicated TAM or the full proactive services found in Enterprise-level plans.  
C. AWS Business Support

#### Explications

Business Support provides 24/7 access to Cloud Support Engineers, full AWS Trusted Advisor checks, and faster SLAs for urgent issues, but it does not include a dedicated Technical Account Manager—TAMs are reserved for Enterprise-tier offerings.  
**Votre sélection est correcte**  
D. AWS Enterprise On-Ramp Support

#### Explications

Enterprise On-Ramp is an Enterprise-tier offering designed for growing customers that includes access to a Technical Account Manager for proactive architecture guidance and prioritized escalation; it provides selected Enterprise-level TAM services (though scope/terms may be more limited than full Enterprise Support).  
**Votre sélection est correcte**  
E. AWS Enterprise Support

#### Explications

Enterprise Support includes a dedicated Technical Account Manager who provides ongoing, proactive guidance (architecture reviews, operational best practices, escalation management, and coordination with AWS specialists) alongside 24/7 support and additional Enterprise services.  
Explication générale  
Only Enterprise-tier offerings provide a dedicated Technical Account Manager. Enterprise Support delivers a full-time TAM with proactive guidance and additional Enterprise services; Enterprise On-Ramp also provides TAM access for eligible customers as a pathway to full Enterprise capabilities. Basic, Developer, and Business provide technical support of varying levels but do not include a dedicated TAM.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 116Correct  
A university receives a grant to conduct research by using AWS services. The research team needs to make sure the grant money lasts for the entire school year. The team has decided on a monthly allocation that adds up to the total grant amount. Which AWS service or feature will notify the team if spending exceeds the planned amount?  
**Votre réponse est correcte**  
A. AWS Budgets

#### Explications

AWS Budgets is the AWS service purpose-built for enforcing cost controls: you can create monthly budgets that match the grant allocation, configure thresholds on actual or forecasted spend, and receive notifications when those thresholds are breached. Budgets integrates with Amazon SNS to send email/SMS or trigger automated actions, making it the correct choice for proactively alerting the research team about overspend.  
B. Cost Explorer

#### Explications

Cost Explorer provides historical cost/usage reports, visualizations, and forecasting to help analyze spending patterns. It is an analysis and reporting tool and does not provide built-in alerting or threshold-based notifications for budget overrun, so it does not meet the notification requirement.  
C. Cost allocation tags

#### Explications

Cost allocation tags are used to label resources so you can attribute costs to projects, teams, or grants and produce granular reports. They improve cost tracking and reporting but do not generate alerts when spending exceeds a budget.  
D. Cost categories

#### Explications

Cost categories let you group and reclassify costs into logical buckets for reporting and filtering (for example by project or cost center). They help with organization and reporting but do not provide notification/alerting capabilities for overspend.  
Explication générale  
This item tests knowledge of AWS cost-management tools. AWS Budgets is the appropriate service because it lets you define monthly budgets, set threshold alerts on actual or forecasted spend, and notify stakeholders (via email or SNS) when spending exceeds the planned amount. The other options (Cost Explorer, cost allocation tags, cost categories) are useful for analysis and organization but do not provide proactive alerting.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 117Correct  
A company is building a new application on AWS. The company needs the application to remain available if an individual application component fails. Which design principle should the company use to meet this requirement?  
A. Disposable resources

#### Explications

The disposable-resources concept (ephemeral/replaceable infrastructure) promotes easy replacement of instances or containers (for example, using Auto Scaling and immutable images). While it speeds recovery and simplifies updates, it does not by itself isolate failures between components; if components are tightly connected, a failed component can still cascade and cause downtime.  
B. Automation

#### Explications

Automation (CloudFormation, AWS CDK, CodePipeline, Systems Manager) improves consistency, repeatability, and recovery speed. It helps deploy and restore resources quickly but does not inherently prevent a single component failure from affecting application availability — it supports remediation rather than isolation.  
C. Rightsizing

#### Explications

Rightsizing is the process of selecting appropriate instance types, sizes, and resource allocations to balance cost and performance. This addresses cost-efficiency and performance tuning, not architectural fault isolation or resilience to individual component failure.  
**Votre réponse est correcte**  
D. Loose coupling

#### Explications

Designing components to be decoupled and communicate via well-defined, often asynchronous interfaces (for example, using Amazon SQS, SNS, EventBridge, or API Gateway) isolates failures so one component can fail or be repaired without bringing down others. Patterns that support this include message queues, retries with backoff, dead-letter queues, idempotent operations, and health checks combined with Auto Scaling — all of which preserve overall application availability when an individual component fails.  
Explication générale  
The question tests the architectural principle of isolating failures so the application remains available when a single component fails. Decoupling components (using asynchronous messaging, well-defined interfaces, and fault-isolation patterns) is the correct approach because it prevents failure propagation. Other choices (disposable resources, automation, rightsizing) are useful practices but address replaceability, operational efficiency, or cost/performance rather than primary fault isolation.  
Domaine  
Domain 1: Cloud Concepts  
Question 118Correct  
An ecommerce company has migrated its IT infrastructure from an on-premises data center to the AWS Cloud. Which cost is the company’s direct responsibility?  
**Votre réponse est correcte**  
A. Cost of application software licenses

#### Explications

Customers are responsible for procuring, managing, and ensuring compliance for the software they run on AWS (operating systems, middleware, commercial application licenses). This responsibility includes Bring-Your-Own-License (BYOL) scenarios, license-included offerings, and any associated license management and support obligations. These licensing costs and compliance controls are not covered by AWS under the shared responsibility model.  
B. Cost of the hardware infrastructure on AWS

#### Explications

AWS owns and operates the physical servers, storage, and networking hardware in its regions and recovers those capital and operational expenses through service pricing. Customers pay for AWS services (compute, storage, networking) by usage, rather than directly paying for the underlying hardware infrastructure.  
C. Cost of power for the AWS servers

#### Explications

Facility power and utilities are part of AWS’s data center operational costs and are managed by AWS; those costs are incorporated into AWS service prices. Customers do not receive separate power bills for AWS-managed hardware.  
D. Cost of physical security for the AWS data center

#### Explications

Physical security of AWS data centers (perimeter controls, guards, facility access, environmental controls) is the responsibility of AWS and is covered by AWS physical security controls and compliance attestations. Customers retain responsibility for security 'in the cloud'—their accounts, IAM, data, and guest OS/app configuration—not the data center’s physical safeguards.  
Explication générale  
This item tests cost ownership under AWS’s shared responsibility model with emphasis on billing: customers are directly responsible for costs they incur for their own software licenses and associated compliance. AWS is responsible for the underlying data center, hardware, power, and physical security; those are reflected in service pricing rather than billed to customers as separate infrastructure or facility charges.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 119Correct  
Which AWS Cloud Adoption Framework (AWS CAF) perspective focuses on real-time insights and answers questions about strategy?  
A. Operations

#### Explications

Incorrect — this perspective is about day-to-day cloud operations: monitoring, incident management, runbooks, automation, and maintaining service health. Those responsibilities support reliable operations but do not provide the business-level, strategic insights described in the question.  
B. People

#### Explications

Incorrect — this perspective covers organizational change, roles, skills, recruiting, and training to enable cloud adoption. It addresses people and culture, not the generation of strategic, real-time business insights.  
**Votre réponse est correcte**  
C. Business

#### Explications

Correct — this perspective is focused on aligning cloud initiatives with business goals, defining KPIs and value metrics, and enabling portfolio/financial management. It emphasizes business outcomes and the dashboards/metrics that provide the real-time insights used to answer strategic questions.  
D. Platform

#### Explications

Incorrect — this perspective addresses infrastructure and platform design, provisioning, automation, and developer enablement (platform engineering). Its remit is technical architecture and platform services rather than business strategy or real-time strategic insights.  
Explication générale  
Le cadre d'adoption du cloud AWS regroupe les recommandations en fonction de différentes perspectives. La perspective métier met l'accent sur la stratégie, la création de valeur, les indicateurs clés de performance (KPI) et les tableaux de bord fournissant des informations en temps réel sur l'activité. Les autres perspectives (opérations, ressources humaines, plateforme, sécurité, gouvernance) se concentrent sur les aspects opérationnels, organisationnels, techniques ou de conformité et ne sont donc pas les plus adaptées pour répondre à une question relative à la vision stratégique en temps réel.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 120Correct  
Une entreprise souhaite consolider la facturation de plusieurs comptes AWS. Elle doit utiliser un seul compte pour payer l'ensemble des autres comptes. Quel service ou outil AWS doit-elle utiliser pour répondre à ce besoin ?  
A. Conseiller de confiance AWS

#### Explications

Incorrect. AWS Trusted Advisor est un service d'optimisation et de recommandations de bonnes pratiques qui effectue des vérifications et fournit des recommandations concernant les coûts, les performances, la sécurité et la tolérance aux pannes. Il ne propose pas de liaison de comptes, de fonctionnalité de compte payeur ni de mécanisme de consolidation de la facturation entre plusieurs comptes AWS.  
**Votre réponse est correcte**  
B. Organisations AWS

#### Explications

Exact. AWS Organizations permet une gestion centralisée des comptes et une facturation consolidée grâce à la désignation d'un compte de gestion qui règle les frais des comptes membres. Il offre une facturation consolidée (facture unique et visibilité des coûts), le regroupement des comptes et une gouvernance basée sur des politiques pour l'ensemble des comptes.  
C. Budgets AWS

#### Explications

Incorrect. AWS Budgets sert à créer des budgets de coûts et d'utilisation et à générer des alertes en cas de dépassement de seuils. Bien qu'il permette de surveiller et de contrôler les dépenses (y compris entre comptes liés), il n'établit pas de hiérarchies de comptes et ne fait pas office de payeur pour d'autres comptes.  
D. Catalogue de services AWS

#### Explications

Incorrect. AWS Service Catalog permet aux administrateurs de définir et de gérer des catalogues approuvés de produits informatiques (modèles de provisionnement et configurations) pour les utilisateurs. Il est axé sur le provisionnement et la gouvernance standardisés, et non sur la consolidation de la facturation ou la gestion des paiements.  
Explication générale  
AWS Organizations est le service idéal pour consolider la facturation, car il fournit un compte de gestion permettant de régler les frais des comptes membres et offre une visibilité et une gouvernance centralisées des coûts. Les autres options répondent à des besoins spécifiques : Trusted Advisor propose des vérifications des bonnes pratiques, AWS Budgets assure le suivi budgétaire et les alertes, et Service Catalog gère l’allocation des ressources approuvées ; aucune ne propose de compte payeur ni de fonctionnalité de facturation consolidée.  
Domaine  
Domaine 4 : Facturation, tarification et assistance

