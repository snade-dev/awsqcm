Question 1Correct  
Une entreprise migre son site web public vers AWS. Elle souhaite héberger le nom de domaine de son site sur AWS. Quel service AWS doit-elle utiliser pour répondre à ce besoin ?  
A. AWS Lambda

#### Explications

Incorrect. Lambda est un service de calcul sans serveur piloté par les événements, permettant d'exécuter du code applicatif (fonctions) en réponse à des déclencheurs. Il ne fournit pas les fonctionnalités DNS, d'enregistrement de domaine ni de gestion des enregistrements DNS nécessaires à l'hébergement d'un nom de domaine.  
**Votre réponse est correcte**  
B. Route 53 d'Amazonie

#### Explications

Exact. Route 53 est le service DNS et d'enregistrement de domaines d'AWS. Il permet d'enregistrer des noms de domaine, de créer et de gérer des enregistrements DNS (A, CNAME, alias, etc.), de configurer des politiques de routage (latence, géolocalisation, basculement) et d'utiliser des contrôles d'intégrité pour acheminer le trafic vers des points de terminaison opérationnels. Il s'intègre directement aux autres ressources AWS (CloudFront, ELB, S3) pour acheminer un domaine vers les points de terminaison d'un site web.  
C. Amazon CloudFront

#### Explications

Incorrect. CloudFront est un réseau de diffusion de contenu (CDN) mondial qui met en cache et distribue du contenu depuis des points de présence afin de réduire la latence. Bien que les distributions soient généralement associées à des noms de domaine, CloudFront n'enregistre pas de serveur DNS et n'en fait pas office ; les enregistrements DNS doivent être gérés par un service DNS tel que Route 53\.  
D. AWS Direct Connect

#### Explications

Incorrect. Direct Connect fournit une connectivité réseau dédiée entre les environnements sur site et AWS pour des connexions privées à haut débit. Il s'agit d'un service de transport réseau et non d'une fonctionnalité d'enregistrement de domaine ou d'hébergement DNS.  
Explication générale  
Cette question vise à déterminer quel service AWS est utilisé pour héberger et gérer un nom de domaine. Le service approprié est Route 53, car il assure l'enregistrement de noms de domaine et la gestion des enregistrements DNS, ainsi que des fonctionnalités avancées de routage et de contrôle d'intégrité pour acheminer le trafic vers les points de terminaison du site web. Les autres options sont sans rapport avec ce service : Lambda est une plateforme de calcul, CloudFront est un CDN (qui peut être utilisé comme serveur de noms de domaine, mais ne gère pas les enregistrements DNS), et Direct Connect est une liaison réseau dédiée.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 2Correct  
Une entreprise prévoit de migrer vers le cloud AWS. Elle collecte des informations sur son infrastructure sur site et a besoin de données telles que le nom d'hôte, l'adresse IP et l'adresse MAC. Quel service AWS répond à ces besoins ?  
A. AWS DataSync

#### Explications

AWS DataSync est un service de transfert de données géré permettant de déplacer des fichiers entre un stockage local et les services de stockage AWS (Amazon S3, Amazon EFS, Amazon FSx). Il n'effectue aucun inventaire ni découverte des serveurs et ne collecte aucune métadonnée telle que les noms d'hôte, les adresses IP ou les adresses MAC.  
B. Service de migration d'applications AWS

#### Explications

AWS Application Migration Service (également appelé MGN) effectue une réplication continue au niveau bloc, basée sur des agents ou sur la réplication AWS, pour migrer les serveurs vers AWS et automatiser la bascule. Il se concentre sur l'orchestration de la réplication et de la migration, et non sur la découverte ou l'inventaire des identifiants réseau ou matériels tels que les adresses MAC.  
**Votre réponse est correcte**  
C. Service de découverte d'applications AWS

#### Explications

AWS Application Discovery Service is designed to collect detailed on-premises server metadata and dependency information for migration planning. It supports agent-based and agentless collection and captures attributes such as hostnames, IP addresses, MAC addresses, running processes, and network dependencies; it can export this inventory to AWS Migration Hub or other planning tools.  
D. AWS Database Migration Service (AWS DMS)

#### Explications

AWS Database Migration Service (AWS DMS) is specialized for migrating database schemas and data between source and target database engines with minimal downtime. It does not inventory on-premises server hardware or network identifiers and is not intended for collecting host-level metadata.  
Explication générale  
The question tests knowledge of AWS migration tooling and which service performs discovery/inventory. AWS Application Discovery Service is the correct choice because it is specifically built to gather on-premises server metadata (hostnames, IPs, MACs) and dependency information for migration planning. The other options (DataSync, Application Migration Service, DMS) serve data transfer, replication/migration, or database migration purposes and do not provide comprehensive discovery/inventory of on-premises hosts.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 3Correct  
Which AWS service provides command line access to AWS tools and resources directly from a web browser?  
A. AWS CloudHSM

#### Explications

A managed hardware security module service for generating and storing cryptographic keys and performing crypto operations. It is accessed via cryptographic APIs (PKCS\#11, JCE, CNG) and used for key custody and HSM-backed operations — it does not provide an interactive, browser-based command-line environment for running AWS CLI commands.  
**Votre réponse est correcte**  
B. AWS CloudShell

#### Explications

Provides an authenticated, browser-based shell environment preconfigured with AWS CLI v2, common SDKs, and development tools. Sessions run inside the AWS Management Console using the caller's IAM permissions and include a persistent home directory per region, enabling command-line interaction with AWS resources without installing local tooling. This is why it is the correct choice.  
C. Amazon WorkSpaces

#### Explications

A Desktop-as-a-Service offering that delivers persistent virtual Windows or Linux desktops to end users. It is designed for full desktop access via clients or streaming protocols, not for a lightweight, web-based shell to run AWS CLI commands within the console.  
D. AWS Cloud Map

#### Explications

A service discovery and naming registry that allows applications to register and discover service endpoints via DNS or API calls. Its purpose is service discovery for microservices and resources, not to provide interactive command-line access from a web browser.  
Explication générale  
The question tests recognition of the AWS service that exposes a browser-based command-line environment. The correct service provides a preauthenticated shell in the AWS Management Console with AWS CLI/SDKs and a persistent home directory, allowing users to run CLI commands without local installation. The other options are distinct services: hardware key management (CloudHSM), virtual desktops (WorkSpaces), and service discovery (Cloud Map), none of which supply a web-based AWS CLI shell.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 4Correct  
Which AWS service supports the deployment and management of applications in the AWS Cloud?  
A. Amazon CodeGuru

#### Explications

Incorrect. This service provides ML-powered code review and application performance recommendations (profiler), not deployment or runtime management of applications.  
B. AWS Fargate

#### Explications

Incorrect. This is a serverless container compute engine used to run tasks and services (with Amazon ECS/EKS); it provides container execution but not a PaaS that automates full application provisioning, scaling, and platform management.  
C. AWS CodeCommit

#### Explications

Incorrect. This is a fully managed Git-compatible source control repository service. It stores code but does not deploy or run applications (deployment typically uses services like CodePipeline/CodeDeploy).  
**Votre réponse est correcte**  
D. AWS Elastic Beanstalk

#### Explications

Correct. This managed Platform-as-a-Service automates provisioning of infrastructure, load balancing, auto scaling, application health monitoring, and platform updates to simplify deploying and managing web applications and services.  
Explication générale  
The question tests knowledge of AWS services used for application deployment and management. The correct choice is the managed PaaS that automates infrastructure provisioning, scaling, load balancing, and health monitoring. The other options are developer tools or compute/source services that either aid development, run containers, or store code, but do not provide the end-to-end application deployment and platform management that the PaaS offers.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 5Correct  
A company plans to migrate its custom marketing application and order-processing application to AWS. The company needs to deploy the applications on different types of instances with various configurations of CPU, memory, storage, and networking capacity. Which AWS service should the company use to meet these requirements?  
A. AWS Lambda

#### Explications

AWS Lambda is a serverless (FaaS) compute service that abstracts away servers. It lets you configure memory and execution time for functions but does not provide control over instance families, exact CPU allocation, persistent block storage choices, or low-level network configuration required for hosting applications on specific instance types.  
B. Amazon Cognito

#### Explications

Amazon Cognito is an identity management service that handles user sign-up, sign-in, and access control. It does not provision or manage compute resources or allow selection of instance-level hardware configurations.  
C. Amazon Athena

#### Explications

Amazon Athena is a serverless interactive query service for running SQL against data in Amazon S3 (uses a Presto/Trino engine). It is designed for analytics and querying data, not for hosting or configuring application servers.  
**Votre réponse est correcte**  
D. Amazon EC2

#### Explications

Amazon EC2 provides virtual servers where you can choose instance families and sizes (general purpose, compute‑optimized, memory‑optimized, etc.), select AMIs, attach EBS volumes or use instance store, and configure VPC networking and enhanced networking features—offering the granular CPU, memory, storage, and network control required for the scenario.  
Explication générale  
The requirement is to run custom applications on specific instance types with precise CPU, memory, storage, and networking configurations. Amazon EC2 supplies virtual machines and related storage/networking options that give this level of control. The other choices address serverless functions (Lambda), identity (Cognito), or data querying (Athena), so they do not meet the instance-selection and infrastructure-control requirements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 6Incorrect  
A company wants to transfer a virtual Windows Server 2022 that is currently running in its own data center to AWS. The company wants to automatically convert the existing server to run directly on AWS infrastructure instead of visualized hardware. Which AWS service will meet these requirements?  
**Votre réponse est incorrecte**  
A. AWS DataSync

#### Explications

DataSync is a managed service for fast, secure file and object data transfer between on‑premises storage and AWS storage services (for example, S3, EFS, FSx). It does not perform block‑level replication, VM conversion, or automated server cutover required to run an on‑premises VM natively on EC2.  
B. AWS Database Migration Service (AWS DMS)

#### Explications

AWS Database Migration Service focuses on migrating databases (schema and data) to and from various database engines and AWS database services. It is not used to migrate entire server images or convert virtual machine operating environments to run on EC2.  
C. AWS Application Discovery Service

#### Explications

Application Discovery Service inventories on‑premises servers and their dependencies to aid migration planning. It provides discovery and assessment data but does not perform replication, conversion, or automated launch of servers on AWS.  
**Bonne réponse**  
D. AWS Application Migration Service

#### Explications

AWS Application Migration Service (AWS MGN) provides agent‑based/block‑level continuous replication of source servers, automated transformation of the disk and boot configuration so instances can boot as native EC2 instances, and orchestration for test and cutover. It is designed specifically for automated lift‑and‑shift migrations of Windows and Linux servers with minimal manual reconfiguration and supports Windows Server 2022\.  
Explication générale  
Cette question teste vos connaissances des outils de migration AWS. Le service approprié pour une conversion automatisée « lift-and-shift » d'un serveur virtuel sur site vers une exécution native sur AWS est AWS Application Migration Service (AMS). En effet, il réplique les serveurs au niveau des blocs, automatise les conversions de format et de démarrage, et orchestre les lancements et les basculements. Les autres options concernent le transfert de données, la migration de bases de données ou la découverte/planification, et ne prennent pas en charge la conversion complète du serveur ni le basculement automatisé.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 7Correct  
Une entreprise n'utilise souvent pas toute sa capacité Amazon EC2 actuelle pour exécuter des charges de travail sans état. Elle souhaite optimiser ses coûts EC2. Quel type d'instance EC2 répondra à ces exigences ?  
**Votre réponse est correcte**  
A. Exemples ponctuels

#### Explications

Utilise la capacité EC2 disponible à prix fortement réduit pour les charges de travail tolérantes aux interruptions. Offre des économies importantes par rapport à l'offre à la demande, prévient des interruptions de deux minutes et est couramment utilisé avec l'Auto Scaling, les flottes Spot ou les architectures tolérantes aux pannes pour exécuter des tâches sans état ou par lots tout en minimisant les dépenses.  
B. Instances dédiées

#### Explications

Les instances sont exécutées sur du matériel dédié à un seul client afin de garantir l'isolation physique et la conformité. Ce modèle engendre des coûts supplémentaires (absence de remises sur capacité partagée) et est conçu pour répondre aux exigences d'isolation ou de licence, et non pour optimiser les coûts en exploitant la capacité inutilisée.  
C. Instances réservées

#### Explications

Nécessite un engagement de 1 ou 3 ans (ou des plans d'économies) pour bénéficier d'une tarification horaire réduite en cas d'utilisation stable et prévisible. Offre des avantages économiques pour les charges de travail constantes, mais ne convient pas aux charges de travail sans état, très variables ou interruptibles, qui nécessitent une utilisation opportuniste de la capacité disponible.  
D. Instances à la demande

#### Explications

Ce service propose une facturation à la seconde sans engagement à long terme, offrant ainsi une grande flexibilité pour les charges de travail ponctuelles ou imprévisibles. Il ne propose cependant pas les mêmes remises importantes que les options de capacité disponible et n'est donc pas le choix le plus judicieux lorsque l'objectif principal est l'optimisation des coûts par l'utilisation de la capacité EC2 inutilisée.  
Explication générale  
Cette question évalue votre connaissance des options d'achat de instances EC2 pour optimiser les coûts des charges de travail sans état et interruptibles. La bonne réponse permet d'exploiter la capacité EC2 inutilisée à des prix très avantageux, tout en acceptant d'éventuelles interruptions et en utilisant une architecture tolérante aux interruptions. Les autres options (dédiées, réservées, à la demande) entraînent soit une augmentation du coût pour l'isolation, soit un engagement à long terme pour des économies stables, soit une flexibilité moindre sans le même niveau de réduction.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 8Correct  
Une entreprise souhaite un serveur de fichiers Windows entièrement géré pour ses applications Windows. Quel service AWS répond à ce besoin ?  
**Votre réponse est correcte**  
A. Amazon FSx

#### Explications

Amazon FSx pour Windows File Server est un système de fichiers natif Windows entièrement géré qui prend en charge le protocole SMB, l'intégration Active Directory, la sémantique NTFS, les listes de contrôle d'accès Windows, les quotas d'utilisateurs et les sauvegardes automatisées. Il offre un stockage de fichiers partagé à faible latence, fonctionnellement équivalent à un serveur de fichiers Windows sur site, et constitue le service AWS idéal pour les applications Windows nécessitant un serveur de fichiers géré.  
B. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Amazon EKS is a managed Kubernetes control plane for running containerized workloads. It does not provide a managed Windows SMB file server; containers running on EKS must use block or network storage (EBS, EFS, or S3) or deploy their own file-server containers, which do not replace a native Windows file server with AD/NTFS/ACL support.  
C. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Amazon ECS is a container orchestration service for running Docker containers. Like EKS, it does not offer a native, fully managed Windows file server with SMB, Active Directory integration, or NTFS features; persistent storage for containers is provided via EBS, EFS, or S3, not a Windows file server service.  
D. Amazon EMR

#### Explications

Amazon EMR is a managed big data platform for running frameworks such as Hadoop and Spark on clusters. It is designed for data processing and analytics, not for providing a managed Windows file server or SMB-compatible shared file storage.  
Explication générale  
The question tests knowledge of AWS services that provide Windows-compatible, fully managed file storage. The correct choice is the FSx for Windows File Server offering because it supplies SMB protocol access, Active Directory integration, NTFS semantics, and other native Windows file-server features. The other options (EKS, ECS, EMR) are for container orchestration or big data processing and do not provide a native, managed Windows file-server service.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 9Correct  
A company wants durable storage for static content and infinitely scalable data storage infrastructure at the lowest cost. Which AWS service should the company choose?  
A. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS is block-level storage that is attached to individual EC2 instances within a single Availability Zone. It is optimized for low-latency block storage for running operating systems and databases, not for serving highly durable, globally accessible static objects at massive scale. Scaling EBS for large amounts of static content requires provisioning and managing many volumes and instances, and costs are generally higher than cloud-native object storage for this use case.  
**Votre réponse est correcte**  
B. Amazon S3

#### Explications

Amazon S3 is a cloud-native object storage service that provides extremely high durability (11 nines), virtually unlimited capacity, and a pay-for-what-you-use pricing model with multiple low-cost storage classes and lifecycle policies. It supports static website hosting, direct integration with Amazon CloudFront for global content delivery, and is specifically optimized for storing and serving static content at minimal cost per GB.  
C. AWS Storage Gateway

#### Explications

AWS Storage Gateway is a hybrid service that provides on-premises applications access to AWS storage (cached or tape-like interfaces). It is intended to bridge on-premises infrastructure and AWS, not to act as a cloud-native, infinitely scalable, low-cost object store for hosting static content directly.  
D. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed, elastic NFS file system that provides shared filesystem semantics for EC2 and other compute resources. It is designed for workloads that require POSIX file access and shared mounts. Although it scales automatically, it is typically more expensive and not optimized for low-cost static object hosting compared with S3.  
Explication générale  
The requirement is durable, infinitely scalable, and lowest-cost storage for static content. Amazon S3 is the appropriate service because it is a purpose-built, highly durable object store with virtually unlimited capacity, inexpensive storage classes, lifecycle policies, and features (static website hosting \+ CloudFront integration) that optimize cost and delivery. The other options are block/file or hybrid storage solutions meant for compute-attached or on-premises integration and do not provide the same cost-efficiency or global object-serving model.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 10Correct  
A company needs to continuously run an experimental workload on an Amazon EC2 instance and stop the instance after 12 hours. Which instance purchasing option will meet this requirement MOST cost-effectively?  
**Votre réponse est correcte**  
A. On-Demand Instances

#### Explications

This option is the best fit for a one-off 12-hour run because it provides guaranteed, non-interruptible EC2 capacity without requiring a long-term commitment. For short-duration continuous workloads, paying for compute only while it runs avoids the upfront or multi-year costs of commitment-based options and the availability risk of interruptible capacity.  
B. Reserved Instances

#### Explications

Not suitable for a single 12-hour experiment. These options require a 1- or 3-year commitment (or equivalent billing commitment) to achieve their discounts, making them cost-inefficient for short-term, one-time workloads.  
C. Spot Instances

#### Explications

Not appropriate when uninterrupted execution is required. This purchasing model offers steep discounts by using spare capacity that can be reclaimed with short notice (interruptions with a brief warning), so it’s intended for fault-tolerant or restartable jobs.  
D. Dedicated Instances

#### Explications

Not cost-effective for transient experiments. These provide single-tenant hardware for compliance or licensing reasons and carry a pricing premium, so they are chosen for isolation requirements rather than short-term cost savings.  
Explication générale  
For a workload that must run continuously for a limited 12-hour period, the best balance of guaranteed capacity and cost is the pay-as-you-go option that incurs no long-term commitment. Commitment-based options incur unnecessary multi-year costs, interruptible capacity can be reclaimed by AWS and would risk the run, and dedicated hardware is more expensive and intended for isolation/compliance—not short experiments.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 11Correct  
A company needs to move 75 petabytes of data from its on-premises data centers to AWS. Which AWS service should the company use to meet these requirements MOST cost-effectively?  
A. AWS Snowball Edge Storage Optimized

#### Explications

Snowball Edge appliances are physical devices with tens to low hundreds of terabytes of usable capacity each. Moving 75 PB would require an impractically large number of devices, creating significant operational overhead (device provisioning, shipping, import/export, data consolidation) and higher aggregate cost and time compared with solutions designed for exabyte-scale moves.  
**Votre réponse est correcte**  
B. AWS Snowmobile

#### Explications

Snowmobile is a purpose-built, truck‑based data transfer service for exabyte- and multi‑petabyte‑scale migrations. A single Snowmobile can ingest up to  
C. AWS Direct Connect

#### Explications

AWS Direct Connect provides a dedicated network connection for ongoing, low‑latency, high‑bandwidth use cases. It is not optimized for a one‑time bulk migration of tens of petabytes because network transfer would take a very long time even at high bandwidth, incur networking and data transfer costs, and require sustained provisioning rather than a single physical ingest operation.  
D. AWS Storage Gateway

#### Explications

AWS Storage Gateway is a hybrid storage integration service (file, volume, or tape gateway) intended for seamless access between on‑premises environments and AWS for ongoing workloads or tape replacement. It is not designed as the most practical or cost‑effective method for a one‑time, multi‑petabyte bulk data migration at this scale.  
Explication générale  
This question tests selection of the appropriate AWS data‑transfer mechanism for very large, one‑time migrations. For 75 petabytes, a truck‑based Snowmobile is the best fit because it can ingest tens of petabytes per unit, offers physical high‑throughput transfer and strong security controls, and reduces operational complexity and total cost. Smaller devices like Snowball Edge require many units and more logistics; Direct Connect and Storage Gateway are better suited to ongoing networked or hybrid use cases, not single massive bulk transfers.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 12Incorrect  
Which design principle aligns with performance efficiency pillar of the AWS Well-Architected Framework?  
**Bonne réponse**  
A. Using serverless architectures

#### Explications

Serverless services (for example AWS Lambda, AWS Fargate and Amazon Aurora Serverless) provide automatic, on‑demand scaling and abstract capacity provisioning. By removing the need to provision and tune infrastructure and by using metered billing, these services enable systems to meet variable demand while minimizing idle resources—directly supporting the Performance Efficiency pillar’s focus on efficient resource use and rapid adaptation to changing requirements.  
**Votre réponse est incorrecte**  
B. Scaling horizontally

#### Explications

Distributing load across more compute instances (horizontal scaling) is a common scalability and availability technique that increases aggregate capacity and fault tolerance. It is primarily emphasized in the Reliability pillar (to improve availability and fault tolerance). While horizontal scaling can affect performance, the Performance Efficiency pillar focuses on choosing appropriate resource types, elasticity, and advanced technologies to optimize performance rather than simply adding more identical instances.  
C. Measuring the cost of workloads

#### Explications

Tracking and measuring the cost of workloads (using tools like AWS Cost Explorer or Cost and Usage Reports) is a Cost Optimization practice. It helps control spending and make financial trade‑offs but does not by itself address the design principles specific to improving performance efficiency.  
D. Using managed services

#### Explications

Adopting managed services (such as Amazon RDS or Amazon DynamoDB) reduces operational overhead and can improve reliability and operational excellence by offloading undifferentiated heavy lifting. Although managed services can enable better performance indirectly, the explicit design principles listed under the Performance Efficiency pillar call out serverless and other performance‑focused approaches, so this option is not the primary match for that pillar.  
Explication générale  
The Performance Efficiency pillar emphasizes designing systems to use computing resources efficiently and to adapt rapidly to changing demand. The best match is leveraging serverless services because they provide automatic, on‑demand scaling and eliminate manual capacity provisioning. The other options describe valid cloud practices—horizontal scaling (availability/scalability), cost measurement (cost optimization), and managed services (operational efficiency)—but they align more closely with other Well‑Architected pillars.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 13Correct  
A company has a website on AWS. The company wants to deliver the website to a worldwide audience and provide low-latency response times for global users. Which AWS service will meet these requirements?  
A. AWS CloudFormation

#### Explications

Incorrect. AWS CloudFormation is an infrastructure-as-code service for provisioning and managing AWS resources via templates and stacks. It does not provide global content caching, edge locations, or any CDN functionality that would reduce end-user latency for a worldwide audience.  
**Votre réponse est correcte**  
B. Amazon CloudFront

#### Explications

Correct. Amazon CloudFront is AWS’s content delivery network that caches content at a global network of edge locations. By serving static and dynamic assets from the edge nearest the user, using configurable cache behaviors and TTLs, and integrating with origins such as S3, ALB, or custom origins, CloudFront significantly reduces latency for global users and supports features like HTTPS, HTTP/2, signed URLs, and integration with WAF and Shield for secure, low-latency delivery.  
C. Amazon ElastiCache

#### Explications

Incorrect. Amazon ElastiCache provides in-memory caching (Redis or Memcached) to speed up application data access within a region and reduce backend latency for application servers. It does not provide distributed edge caching or deliver website assets from locations near end users globally, so it’s not a replacement for a CDN.  
D. Amazon DynamoDB

#### Explications

Incorrect. Amazon DynamoDB is a managed NoSQL database offering low-latency read/write operations and optional multi-region replication (Global Tables) for availability and locality of data. It is a data store, not a content distribution service and does not cache or serve website assets from edge locations to reduce global user latency.  
Explication générale  
This question tests knowledge of how to deliver web content with low latency to a global audience. A CDN is the appropriate solution because it caches and serves content from edge locations close to users. Amazon CloudFront is the AWS service that provides this global edge caching and related delivery features. The other services listed (CloudFormation, ElastiCache, DynamoDB) provide infrastructure provisioning, regional in-memory caching, and database storage/replication respectively, but none offer the global edge delivery that a CDN provides.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 14Correct  
Which AWS service or feature is used to send both text and email messages from distributed applications?  
**Votre réponse est correcte**  
A. Amazon Simple Notification Service (Amazon SNS)

#### Explications

SNS provides a fully managed pub/sub notification service where applications publish to topics and SNS delivers messages to subscribed endpoints using multiple protocols, including SMS and email. It scales automatically, supports delivery status/metrics, and integrates with other AWS services for distributed architectures, making it appropriate for sending both text and email from distributed applications.  
B. Amazon Simple Email Service (Amazon SES)

#### Explications

SES is an email-focused service for sending and receiving transactional and bulk email (SMTP and API interfaces), with deliverability and reputation features. It does not provide native SMS/text capabilities, so it cannot satisfy both email and SMS requirements by itself.  
C. Amazon CloudWatch alerts

#### Explications

CloudWatch is a monitoring and observability service that creates alarms based on metrics and logs. Alarms can trigger actions by publishing to notification services (for example, SNS) or invoking Lambda, but CloudWatch itself is not a direct SMS/email delivery service.  
D. Amazon Simple Queue Service (Amazon SQS)

#### Explications

SQS is a durable message queuing service for decoupling components (visibility timeouts, long polling, dead-letter queues). It does not provide outbound delivery to SMS or email endpoints and is not used for direct end-user notifications.  
Explication générale  
This question distinguishes between AWS notification, email, monitoring, and queuing services. The correct choice is the notification service that natively supports multiple delivery protocols (SMS and email) via topics and subscriptions. Email-only services and infrastructure/monitoring/queueing services either lack SMS support or are designed for different purposes, though they can integrate with the notification service to enable alerts or deliveries.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 15Correct  
Which AWS service provides the ability to host a NoSQL database in the AWS Cloud?  
A. Amazon Aurora

#### Explications

Aurora is a high-performance, managed relational database engine compatible with MySQL and PostgreSQL. It provides ACID transactions, SQL querying, and a distributed, fault-tolerant storage layer for OLTP workloads — characteristics of relational databases rather than NoSQL key-value or document stores.  
**Votre réponse est correcte**  
B. Amazon DynamoDB

#### Explications

This service is a fully managed, serverless NoSQL database that supports key-value and document data models, automatic scaling, predictable single-digit millisecond latency, on-demand and provisioned capacity modes, Global Tables for multi-region replication, and integrations such as DAX (in-memory caching). Those features make it the appropriate choice for NoSQL workloads on AWS.  
C. Amazon RDS

#### Explications

Amazon RDS manages traditional relational database engines (for example, MySQL, PostgreSQL, MariaDB, Oracle, SQL Server). It provides managed backups, Multi-AZ high availability, and automated maintenance for SQL-based relational systems, not for schema-less NoSQL key-value or document use cases.  
D. Amazon Redshift

#### Explications

Redshift is a managed, petabyte-scale data warehouse built for analytics. It uses columnar storage and MPP (massively parallel processing) to run complex analytical queries over large datasets — an OLAP/data-warehouse service rather than a transactional NoSQL database.  
Explication générale  
The question tests knowledge of AWS database categories. The correct choice is the fully managed NoSQL offering because it natively supports key-value and document models, serverless scaling, and low-latency access patterns required for NoSQL workloads. The other options are relational (Aurora, RDS) or analytical/data-warehouse focused (Redshift) and therefore do not fit the NoSQL use case.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 16Correct  
A company wants to consolidate its call centers to improve the customer voice and chat experience with call center agents. Which AWS service or tool will meet these requirements?  
A. Amazon Simple Notification Service (Amazon SNS)

#### Explications

Amazon SNS is a pub/sub messaging service for notifications (email, SMS, mobile push) and event fan-out. It does not provide contact-center features such as IVR/contact flows, agent routing, real‑time agent workspace, call recording, or built‑in chat/voice session management required to operate a call center.  
B. AWS Support Center

#### Explications

The AWS Support Center is a customer support portal and ticketing system for AWS account and technical support. It is not a platform for hosting or managing customer-facing voice/chat contact centers or routing customer interactions to agents.  
C. Amazon Cognito

#### Explications

Amazon Cognito is an identity and access management service for web and mobile applications (user pools, identity pools, authentication, and federation). It addresses user authentication and profiles, not contact-center interaction handling, call routing, or agent collaboration features.  
**Votre réponse est correcte**  
D. Amazon Connect

#### Explications

This AWS-managed contact-center offering provides omnichannel voice and chat, contact-flow design, agent workspace, routing profiles, real-time and historical metrics, and integrations (for example with Amazon Lex, Lambda, S3, and Kinesis) to build and scale call-center operations—matching the requirements to consolidate centers and improve agent/customer interactions.  
Explication générale  
The question tests knowledge of AWS services for contact-center workloads. The correct choice is the AWS contact-center solution because it delivers the necessary features for voice and chat, routing, agent tools, and integrations to consolidate and modernize call centers. The other options are AWS offerings for notifications (SNS), account support (Support Center), and identity/authentication (Cognito), which do not provide the contact‑center capabilities required here.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 17Correct  
Which AWS service is a relational database compatible with MySQL and PostgreSQL?  
A. Amazon Redshift

#### Explications

Incorrect — Amazon Redshift is a fully managed, petabyte-scale data warehouse that uses columnar storage and MPP (massively parallel processing) to optimize analytical (OLAP) queries. It is designed for analytics and reporting, not as a transactional relational database compatible with MySQL/PostgreSQL engines.  
B. Amazon DynamoDB

#### Explications

Incorrect — Amazon DynamoDB is a fully managed NoSQL key-value and document database offering single-digit millisecond latency and a schemaless data model. It does not implement SQL relational engine compatibility with MySQL or PostgreSQL and is not used for traditional relational workloads.  
**Votre réponse est correcte**  
C. Amazon Aurora

#### Explications

Correct — Amazon Aurora is an RDS-compatible relational database engine that provides MySQL and PostgreSQL compatibility. It delivers managed relational features (automated backups, read replicas, fault-tolerant distributed storage, high availability, and scalability options including Aurora Serverless and Global Database) while maintaining compatibility with MySQL/PostgreSQL client tools and drivers.  
D. Amazon Neptune

#### Explications

Incorrect — Amazon Neptune is a fully managed graph database service supporting property graph (Gremlin) and RDF (SPARQL) models. It is optimized for graph queries and relationships, not for providing MySQL/PostgreSQL-compatible relational database functionality.  
Explication générale  
This item assesses knowledge of AWS database offerings. Amazon Aurora is the managed relational database engine that is compatible with MySQL and PostgreSQL and provides the typical relational features and compatibility required for those workloads. The distractors represent other database categories: Redshift for data warehousing/analytics, DynamoDB for NoSQL key-value/document storage, and Neptune for graph databases—none of which provide MySQL/PostgreSQL-compatible relational engines.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 18Correct  
A development team wants to deploy multiple test environments for an application in a fast, repeatable manner. Which AWS service should the team use?  
A. Amazon EC2

#### Explications

Incorrect. EC2 is a compute (IaaS) service that provides virtual servers; provisioning many identical, full environments with EC2 alone requires manual instance setup or custom automation. It does not provide built‑in, template‑driven orchestration for entire stacks the way infrastructure-as-code services do.  
**Votre réponse est correcte**  
B. AWS CloudFormation

#### Explications

Correct. AWS CloudFormation is the infrastructure-as-code service that defines and provisions AWS resources from declarative JSON/YAML templates. Templates, parameters, nested stacks, change sets and stack sets enable automated, repeatable creation of complete environments (and predictable rollbacks), which is ideal for rapidly deploying multiple test environments.  
C. Amazon QuickSight

#### Explications

Incorrect. Amazon QuickSight is a business intelligence and analytics service for building dashboards and visualizations; it does not provision or manage infrastructure environments and therefore is not relevant for environment deployment.  
D. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Incorrect. Amazon ECS is a container orchestration service for running and scaling containers. While it runs application workloads, it does not by itself provide template‑based provisioning of an entire environment (networks, databases, load balancers, IAM, etc.) without additional tooling such as CloudFormation or CDK.  
Explication générale  
This item tests knowledge of infrastructure-as-code and repeatable environment provisioning. CloudFormation is the appropriate choice because it uses declarative templates to automate creation, update, and deletion of complete AWS stacks, enabling fast, consistent reproduction of test environments. The other options (EC2, ECS, QuickSight) are real AWS services but either provide raw compute, container orchestration, or BI capabilities and do not natively deliver full, template-driven environment provisioning.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 19Correct  
A company hosts a large amount of data in AWS. The company wants to identify if any of the data should be considered sensitive. Which AWS service will meet the requirement?  
A. Amazon Inspector

#### Explications

This service performs automated security assessments (vulnerability and configuration checks) for compute and container resources and reports findings such as CVEs and deviations from best practices. It does not analyze the contents of stored data to discover or classify sensitive information.  
**Votre réponse est correcte**  
B. Amazon Macie

#### Explications

This managed service applies machine learning and pattern matching to inspect objects in Amazon S3 for personally identifiable information (PII) and other sensitive data, produces findings and dashboards, and integrates with Security Hub and EventBridge for alerting and remediation—making it the appropriate choice for data discovery and classification.  
C. AWS Identity and Access Management (IAM)

#### Explications

This service handles identity, authentication, and authorization (users, roles, policies, and permissions). It governs who can access resources but does not provide capabilities to scan or classify data for sensitivity.  
D. Amazon CloudWatch

#### Explications

Ce service fournit des indicateurs, des journaux, des alarmes et une visibilité sur les ressources et applications AWS. Il est axé sur la surveillance et la télémétrie opérationnelle et ne prend pas en charge la détection ni la classification des données sensibles stockées.  
Explication générale  
Il s'agit d'identifier si les données stockées doivent être considérées comme sensibles. Le service approprié est l'offre de classification des données gérées, qui analyse les objets S3 à l'aide de l'apprentissage automatique et de la reconnaissance de formes, génère des résultats et s'intègre aux outils de sécurité AWS. Les autres options concernent l'évaluation des vulnérabilités (et non l'inspection du contenu), le contrôle d'identité et d'accès, ou la surveillance ; aucune ne permet la détection et la classification automatisées des données sensibles.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 20Correct  
Quels services AWS sont sans serveur ? (Choisissez-en deux.)  
**Votre sélection est correcte**  
A. AWS Fargate

#### Explications

Fargate élimine la nécessité de provisionner ou de gérer des instances EC2 pour les charges de travail conteneurisées : AWS prend en charge l’infrastructure de calcul sous-jacente, le placement des tâches et la mise à l’échelle. La facturation se fait par vCPU et par mémoire utilisée par les tâches, et vous n’avez pas à gérer de serveurs ni de clusters, ce qui correspond au modèle sans serveur.  
B. Amazon Managed Streaming pour Apache Kafka

#### Explications

Amazon MSK est un service Apache Kafka géré qui nécessite généralement que vous configuriez la capacité des brokers et des clusters. (AWS propose également MSK Serverless pour des cas d'utilisation spécifiques, mais le service MSK standard implique la gestion de clusters et n'est donc généralement pas considéré comme un service sans serveur.)  
C. Amazon EMR

#### Explications

Amazon EMR fournit des clusters Hadoop/Spark gérés, exécutés sur des instances EC2 ou des groupes de nœuds gérés ; vous provisionnez généralement la capacité et gérez le cycle de vie du cluster. Bien qu'AWS propose EMR Serverless séparément, le service EMR standard n'est pas entièrement sans serveur.  
**Votre sélection est correcte**  
D. Amazon S3

#### Explications

Amazon S3 est un service de stockage d'objets qui s'adapte automatiquement, ne nécessite aucune gestion de serveur ou d'instance et utilise une facturation basée sur l'utilisation pour le stockage et les requêtes — caractéristiques d'un service de stockage entièrement sans serveur.  
E. Amazon EC2

#### Explications

Amazon EC2 fournit des machines virtuelles (instances) que vous lancez, configurez et gérez (y compris le système d'exploitation et les décisions de mise à l'échelle), il s'agit donc d'un service d'infrastructure plutôt que d'un service sans serveur.  
Explication générale  
Le terme « sans serveur » signifie l'absence de provisionnement de serveurs, une mise à l'échelle automatique gérée par le service et une facturation à l'usage. Les meilleures options sont Fargate (calcul conteneurisé sans serveur) et S3 (stockage d'objets sans serveur). Les autres solutions (MSK, EMR, EC2) impliquent le provisionnement ou le dimensionnement des ressources de calcul, de courtage et de cluster selon leur configuration standard (remarque : certains services proposent des modes sans serveur distincts, mais les offres gérées par défaut nécessitent une gestion de la capacité).  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 21Correct  
Laquelle des propositions suivantes décrit le mieux le modèle de responsabilité partagée d'AWS ?  
**Votre réponse est correcte**  
A. AWS gère la sécurité \*de\* l'infrastructure cloud, tandis que le client gère la sécurité \*dans\* le cloud.

#### Explications

AWS is responsible for protecting the underlying global cloud infrastructure — physical data centers, hosts, networking, and the virtualization/hypervisor layers — and for the security of managed services' underlying components. Customers are responsible for what they put in the cloud and how they configure it: their data, applications, operating systems (for IaaS), identity and access management, encryption keys and configuration of security controls. Responsibilities shift by service model (IaaS/PaaS/SaaS), but this division — infrastructure by AWS, in-cloud configuration and data by the customer — is the core of the model.  
B. AWS manages security \*in\* the cloud, while the customer manages security \*of\* the cloud infrastructure.

#### Explications

This reverses the model. AWS does not manage customer-level configuration, data protection, or user access inside a customer’s account; those are the customer’s responsibilities. AWS manages the underlying infrastructure that runs the cloud.  
C. Both AWS and the customer share equal responsibility for all aspects of security.

#### Explications

Security responsibilities are shared but not equally or identically for every control. AWS owns the infrastructure; customers control their data, identities, and configurations. Some managed services reduce customer responsibilities, but that does not make every security aspect equally shared.  
D. AWS is responsible for all security measures, including customer data and user management.

#### Explications

AWS does not take responsibility for customer data protection or user account management. AWS provides security controls and services (for example, IAM, KMS, and encryption features) but customers must configure and operate them to protect their data and manage user access.  
Explication générale  
The AWS shared responsibility model splits security between AWS and the customer: AWS secures the cloud’s infrastructure and managed-service foundations, while customers secure what they run and store in the cloud (data, applications, OS/configuration, and access controls). The correct choice reflects this clear division; the distractors either invert the roles, claim equal responsibility for all aspects, or incorrectly assign customer data/user management to AWS. Responsibility boundaries can shift depending on service type (IaaS vs PaaS vs SaaS).  
Domaine  
Domain 2: Security and Compliance  
Question 22Correct  
Which AWS service is used to provide encryption for Amazon EBS?  
A. AWS Certificate Manager

#### Explications

Incorrect — AWS Certificate Manager issues and manages TLS/SSL certificates for securing network communications (HTTPS). It does not provide or manage the encryption keys used to encrypt Amazon EBS volumes at rest.  
B. AWS Systems Manager

#### Explications

Incorrect — AWS Systems Manager provides operational tooling (Run Command, Session Manager, Parameter Store, State Manager) for managing and automating instances and configuration. It does not perform key management or provide the encryption keys used by EBS volumes.  
**Votre réponse est correcte**  
C. AWS KMS

#### Explications

Exact — AWS Key Management Service (KMS) crée, stocke et contrôle les clés cryptographiques (CMK gérées par le client ou par AWS). Amazon EBS s'intègre à KMS pour le chiffrement de l'enveloppe : EBS utilise une CMK KMS pour chiffrer/déchiffrer les données de volume au repos, et KMS applique les règles d'accès aux clés via IAM et les politiques de clés KMS.  
D. Configuration AWS

#### Explications

Incorrect — AWS Config enregistre et évalue les configurations de ressources à des fins d'audit et de conformité. Il permet de suivre les modifications et d'évaluer la conformité, mais ne fournit pas de chiffrement ni de gestion des clés pour EBS.  
Explication générale  
Amazon EBS utilise AWS KMS pour gérer les clés cryptographiques qui chiffrent les données au repos. Lorsqu'un volume ou un instantané EBS est chiffré, EBS effectue un chiffrement d'enveloppe à l'aide d'une clé principale KMS (gérée par AWS ou par le client). KMS contrôle le cycle de vie et l'accès aux clés. Les autres solutions (ACM, Systems Manager, AWS Config) offrent respectivement la gestion des certificats, la gestion opérationnelle et l'audit de la configuration, mais ne fournissent pas les clés ni les fonctionnalités de gestion des clés nécessaires au chiffrement des volumes EBS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 23Correct  
Une entreprise souhaite mettre en place un processus automatisé pour analyser en continu ses instances Amazon EC2 afin de détecter les vulnérabilités logicielles. Quel service AWS répond à ces exigences ?  
A. Amazon GuardDuty

#### Explications

Incorrect. GuardDuty est un service de détection des menaces géré qui analyse les journaux de flux VPC, les journaux d'événements AWS CloudTrail et les journaux DNS afin de détecter les activités suspectes ou malveillantes. Il se concentre sur la détection et l'alerte, et non sur l'analyse des vulnérabilités logicielles au niveau de l'hôte des instances EC2.  
**Votre réponse est correcte**  
B. Inspecteur Amazon

#### Explications

Exact. Amazon Inspector assure une évaluation automatisée et continue des vulnérabilités des ressources de calcul, identifiant les vulnérabilités logicielles, les problèmes de configuration et les expositions sur les instances EC2 (et autres types de ressources de calcul). Il génère des résultats priorisés (y compris des correspondances CVE) et s'intègre aux processus de correction et aux services de sécurité AWS.  
C. Détective Amazon

#### Explications

Incorrect. Amazon Detective construit un graphique comportemental à partir des journaux pour faciliter l'investigation et la visualisation de la cause première et de l'étendue des incidents de sécurité. Il prend en charge l'investigation des incidents et l'analyse forensique, mais n'effectue pas d'analyses automatisées des vulnérabilités des logiciels d'instance.  
Monsieur Amazon Cognito

#### Explications

Incorrect. Amazon Cognito est un service de gestion des identités permettant l'inscription, la connexion et le contrôle d'accès des utilisateurs. Il n'a aucun lien avec l'évaluation des vulnérabilités ou l'analyse des instances EC2.  
Explication générale  
Il est nécessaire d'effectuer une analyse automatisée et continue des vulnérabilités logicielles des instances EC2. Amazon Inspector est le service AWS conçu pour l'évaluation des vulnérabilités et l'analyse continue, produisant des résultats priorisés et des informations CVE pouvant être intégrées aux processus de correction. Les autres services mentionnés remplissent des fonctions de sécurité/identité différentes — GuardDuty (détection des menaces), Detective (investigation) et Cognito (identité) — et ne répondent donc pas à l'exigence d'analyse.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 24Correct  
Laquelle des propositions suivantes décrit le mieux l'avantage d'utiliser les services cloud AWS pour une organisation ?  
A. Les services cloud AWS éliminent le besoin de toute infrastructure sur site.

#### Explications

Incorrect. AWS can reduce on‑premises infrastructure needs but does not eliminate them for every organization. Many customers use hybrid architectures for latency, data residency, regulatory requirements, or legacy applications. AWS provides hybrid solutions (for example, AWS Outposts, Storage Gateway, AWS Snow Family, and AWS Direct Connect) to integrate on‑premises resources with the cloud.  
**Votre réponse est correcte**  
B. AWS cloud services provide scalable, on-demand resources that can be quickly adjusted to meet changing business needs.

#### Explications

Correct. AWS delivers elasticity and on‑demand capacity so resources can be provisioned and scaled quickly to match changing workloads. This is enabled by services and features such as Amazon EC2 Auto Scaling, Elastic Load Balancing, AWS Lambda, and the pay‑as‑you‑go pricing model, which help avoid overprovisioning and support rapid business changes.  
C. Using AWS guarantees increased security without any additional effort from the organization.

#### Explications

Incorrect. Security in AWS follows the Shared Responsibility Model: AWS is responsible for security of the cloud (infrastructure, hardware, and foundational services) while customers are responsible for security in the cloud (data, identity and access management, OS/application configuration, network controls). AWS provides security tools (IAM, KMS, Security Hub, Config) but organizations must configure and operate them.  
D. AWS services are always cheaper than traditional on-premises solutions.

#### Explications

Incorrect. AWS pricing can be cost‑effective but is not universally cheaper than on‑premises. Total cost depends on architecture, utilization, data transfer, licensing, and chosen pricing models (On‑Demand, Reserved Instances, Savings Plans, Spot). AWS provides the AWS Pricing Calculator, Cost Explorer, and Budgets to analyze and optimize costs.  
Explication générale  
The core concept tested is cloud elasticity and on‑demand provisioning. The correct option emphasizes AWS’s ability to quickly adjust capacity to meet business needs using elastic services and pay‑as‑you‑go pricing. Distractors are wrong because AWS does not force removal of on‑premises systems (hybrid is supported), security responsibilities are shared between AWS and the customer, and cost advantages depend on workload and architecture rather than being guaranteed.  
Domaine  
Domain 1: Cloud Concepts  
Question 25Correct  
A company runs many Amazon EC2 instances in its VPC. The company wants to use a native AWS security resource to control network traffic between certain EC2 instances. Which AWS service or feature will meet this requirement?  
A. Network ACLs

#### Explications

Network ACLs (NACLs) are stateless, subnet-level access control lists. They apply to all traffic entering or leaving a subnet and require explicit inbound and outbound rules for return traffic. Because they operate at the subnet boundary and are coarse-grained and stateless, they are not appropriate for fine-grained, instance-to-instance traffic control within a VPC.  
B. AWS WAF

#### Explications

AWS WAF est un pare-feu d'applications web qui protège les points de terminaison HTTP/S (par exemple, les distributions CloudFront, les équilibreurs de charge d'application et API Gateway) contre les attaques web courantes. Il inspecte et filtre les requêtes web au niveau de la couche application et n'est pas conçu pour contrôler le trafic réseau générique entre les instances EC2.  
C. Amazon GuardDuty

#### Explications

Amazon GuardDuty est un service de détection des menaces qui analyse les journaux de flux VPC, les événements CloudTrail et les journaux DNS afin d'identifier les activités suspectes. Il s'agit d'un service de surveillance et de détection, et non d'un mécanisme de filtrage du trafic ou de contrôle d'accès ; par conséquent, il ne peut pas être utilisé pour appliquer des règles réseau entre les instances.  
**Votre réponse est correcte**  
D. Groupes de sécurité

#### Explications

Les groupes de sécurité sont des pare-feu virtuels avec état, au niveau de l'instance, associés aux interfaces réseau élastiques (ENI) ou aux instances. Ils permettent de définir des règles par protocole, port et source/destination, et peuvent référencer d'autres groupes de sécurité pour autoriser une communication contrôlée entre des instances spécifiques. Du fait de leur gestion de l'état de la connexion et de leur application par instance, ils constituent la fonctionnalité native AWS idéale pour contrôler le trafic inter-instances.  
Explication générale  
Cette question teste vos connaissances des primitives de sécurité réseau AWS. Les groupes de sécurité constituent la bonne réponse, car ce sont des pare-feu avec état, au niveau de l'instance, qui prennent en charge des règles granulaires et la référence à d'autres groupes de sécurité pour contrôler le trafic entre les instances EC2. Les listes de contrôle d'accès réseau (ACL) sont au niveau du sous-réseau et sans état (donc trop grossières), AWS WAF fonctionne au niveau de la couche application HTTP(S) pour les points de terminaison web, et GuardDuty est un service de surveillance et de détection plutôt qu'un mécanisme de contrôle du trafic.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 26Incorrect  
Une entreprise souhaite donner à l'un de ses employés l'accès à Amazon RDS. Elle souhaite également limiter l'interaction à l'interface de ligne de commande AWS (AWS CLI) et aux kits de développement logiciel (SDK) AWS. Quelles actions l'entreprise doit-elle entreprendre pour satisfaire ces exigences tout en respectant le principe du moindre privilège ? (Choisissez deux réponses.)  
**Votre sélection est incorrecte**  
A. Créez un utilisateur IAM et accordez-lui uniquement l'accès à la console de gestion AWS.

#### Explications

L'accès via console uniquement ne fournit pas les informations d'identification programmatiques (ID de clé d'accès et clé d'accès secrète) requises pour l'interface de ligne de commande AWS ou les kits de développement logiciel ; par conséquent, il ne satisfait pas à l'exigence de limiter l'interaction aux interfaces programmatiques.  
**Sélection correcte**  
B. Créez un utilisateur IAM et accordez-lui uniquement un accès programmatique.

#### Explications

L'accès programmatique octroie des informations d'identification permanentes ou temporaires utilisables par l'interface de ligne de commande AWS et les kits de développement logiciel (SDK). Associé à une stratégie IAM à portée limitée n'accordant que les actions d'API RDS et les ARN de ressources nécessaires, il respecte le principe du moindre privilège.  
C. Créez un rôle IAM et accordez-lui uniquement l'accès à la console de gestion AWS.

#### Explications

Limiter un rôle à l'accès à la console ne permet toujours qu'une connexion interactive via navigateur et ne fournit pas les informations d'identification programmatiques nécessaires à l'utilisation de l'interface de ligne de commande/du kit de développement logiciel ; les rôles sont généralement assumés et peuvent émettre des informations d'identification temporaires, mais une configuration limitée à la console ne répond pas à cette exigence.  
D. Créez une stratégie IAM avec accès administrateur et associez-la à l'utilisateur IAM.

#### Explications

Attaching an administrator-level policy grants broad, account-wide privileges that exceed what is required for RDS access and violates least-privilege security practices; instead, grant only specific RDS permissions.  
**Votre sélection est correcte**  
E. Create an IAM policy with Amazon RDS access and attach it to the IAM user.

#### Explications

A dedicated IAM policy scoped to the required Amazon RDS actions and specific resource ARNs lets you grant only the permissions needed (for example, appropriate rds:\* actions or the narrower set required for the task, and rds-db:connect when using IAM DB authentication), implementing least privilege while supporting CLI/SDK access.  
Explication générale  
Provide an IAM identity with programmatic-only credentials and attach a narrowly scoped IAM policy that permits only the necessary Amazon RDS API actions on the required resources. This combination (programmatic access \+ least-privilege RDS policy) enables CLI/SDK interaction while minimizing permissions. Console-only access or granting administrator privileges are inappropriate because they either do not provide the required programmatic access or violate least-privilege principles.  
Domaine  
Domain 2: Security and Compliance  
Question 27Correct  
Which of the following best describes the AWS shared responsibility model?  
**Votre réponse est correcte**  
A. AWS is responsible for security \*of\* the cloud, and the customer is responsible for security \*in\* the cloud.

#### Explications

This option correctly reflects the AWS shared responsibility model: AWS is accountable for securing the underlying cloud infrastructure (physical facilities, hardware, network, hypervisor, and foundational services), while customers retain responsibility for what they place in the cloud — e.g., their data, applications, identity and access management, encryption keys, OS and runtime patching when using IaaS, and configuration of security controls. The exact boundary shifts by service model (IaaS vs. PaaS vs. SaaS), but the core division—"security of the cloud" vs. "security in the cloud"—is accurate.  
B. AWS is responsible for all aspects of security, including customer data and applications.

#### Explications

Incorrect because AWS does not assume responsibility for customer data, customer-managed applications, or customer-configured security controls. While AWS protects the infrastructure, customers must configure access controls, encryption, data classification, and application security. Some AWS managed services reduce customer operational burden, but they do not transfer responsibility for customer data and application configuration to AWS.  
C. Customers are responsible for all security measures, and AWS provides only hardware resources.

#### Explications

Incorrect. AWS provides more than raw hardware; it also secures the physical data centers, network, and virtualization layers. Customers are not solely responsible for all security measures—responsibilities are shared. For example, on EC2 the customer must manage the guest OS and applications, but AWS manages the host infrastructure and physical security.  
D. AWS handles security for both the cloud infrastructure and customer data.

#### Explications

Incorrect because AWS does not handle protection of customer data and customer-managed application logic by default. Customers must implement and maintain data protection (encryption, access policies) and application security controls. AWS handles infrastructure-level controls, not customer data governance unless a specific managed service explicitly includes that responsibility.  
Explication générale  
The question tests understanding of the AWS shared responsibility model: AWS secures the cloud infrastructure (physical facilities, hardware, networking, and foundational services), while customers secure what they put in the cloud (data, applications, OS/configuration, IAM, and encryption). Option 1 captures this division correctly; the other options incorrectly assign customer data/application responsibilities to AWS or claim customers bear all infrastructure security.  
Domaine  
Domain 2: Security and Compliance  
Question 28Correct  
A company's compliance officer wants to review the AWS Service Organization Control (SOC) reports. Which AWS service or feature should the compliance officer use to complete this task?  
**Votre réponse est correcte**  
A. AWS Artifact

#### Explications

Provides a self-service compliance portal in the AWS Management Console that hosts downloadable third‑party audit reports (SOC 1/2/3, ISO, PCI DSS, etc.) and contractual compliance documents. This is the official place for customers and compliance officers to obtain and review SOC reports and related evidence without needing to open a support case.  
B. AWS Concierge Support

#### Explications

Concierge Support is an account- and billing-focused advisory service available to Enterprise Support customers for high-level account assistance and guidance. It does not function as a repository for official audit reports and therefore is not the primary way to retrieve SOC documentation.  
C. AWS Support

#### Explications

AWS Support (the technical support service) helps with operational and technical issues according to the chosen support plan. It does not serve as the centralized location for accessing published compliance reports; those are published in the AWS compliance portal instead.  
D. AWS Trusted Advisor

#### Explications

Trusted Advisor runs automated checks and gives recommendations for cost optimization, security, fault tolerance, and performance. It does not provide access to third‑party audit or compliance reports such as SOC reports.  
Explication générale  
The question targets knowledge of AWS compliance resources. The correct resource is the AWS compliance portal that centrally publishes third‑party audit reports (SOC 1/2/3, ISO, PCI, etc.) for customers to download and review. The other options (Concierge Support, AWS Support, Trusted Advisor) provide account, technical, or optimization assistance but do not act as the official repository for SOC reports.  
Domaine  
Domain 2: Security and Compliance  
Question 29Correct  
Which AWS service or feature allows a user to establish a dedicated network connection between a company’s on-premises data center and the AWS Cloud?  
**Votre réponse est correcte**  
A. AWS Direct Connect

#### Explications

Direct Connect provisions a private, dedicated network circuit from your on-premises location into AWS. It supports private and public virtual interfaces, provides more consistent throughput and lower jitter/latency than internet-based links, integrates with Transit Gateway and VPCs, and is commonly used for large data transfers or workloads with strict performance or compliance requirements.  
B. VPC peering

#### Explications

VPC peering links two VPCs so they can route traffic privately within AWS. It does not create connectivity to on-premises networks, and it does not provide transitive routing between VPCs and external networks.  
C. AWS VPN

#### Explications

AWS Site-to-Site VPN creates encrypted IPsec tunnels over the public internet to connect on-premises networks to AWS. It provides secure connectivity but is internet-based (so less predictable bandwidth/latency) and is often used as a backup or complement to a dedicated connection.  
D. Amazon Route 53

#### Explications

Amazon Route 53 is a DNS and traffic management service for domain name resolution, health checking, and routing policies. It operates at the DNS/HTTP layer and does not establish network-level links between on-premises data centers and AWS.  
Explication générale  
This question tests hybrid networking options. The correct choice is the service that provides a physical/dedicated network circuit into AWS, offering predictable bandwidth and low latency for on-premises integration. Internet-based VPNs, VPC peering, and DNS services do not provide that dedicated physical connection—VPNs are encrypted over the internet, VPC peering only connects VPCs within AWS, and Route 53 is for DNS.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 30Correct  
Which of the following best describes the primary benefit of adopting the AWS Well-Architected Framework when designing cloud solutions?  
**Votre réponse est correcte**  
A. It provides a set of best practices to ensure security, reliability, and performance of applications.

#### Explications

The AWS Well-Architected Framework provides a prescriptive review process (the five pillars and the AWS Well-Architected Tool) that helps teams identify architectural risks, prioritize remediation, and apply AWS design principles. It is intended to guide architecture decisions and continuous improvement through structured questions, benchmarks, and recommended best practices.  
B. It guarantees cost savings by automatically reducing resource usage.

#### Explications

Incorrect — The framework includes the Cost Optimization pillar and guidance, but it does not itself change or throttle resources. Real cost savings require implementing recommendations and using services/features (for example, rightsizing, Auto Scaling, Savings Plans, or Cost Explorer) or operational changes.  
C. It simplifies the process of migrating existing on-premises applications without any additional planning.

#### Explications

Incorrect — The framework helps assess architecture and inform migration strategy, but it does not automate migrations or remove the need for planning. Actual migrations require planning and tools such as AWS Migration Hub, AWS Application Migration Service (MGN), or replatform/refactor efforts.  
D. It replaces the need for security assessments by external auditors.

#### Explications

Incorrect — The framework provides security guidance and risk identification (Security pillar) but is not a substitute for formal compliance verification or third-party audits. Organizations still rely on AWS compliance documentation (AWS Artifact) and external auditors for certification and compliance evidence.  
Explication générale  
The Well-Architected Framework offers a structured set of pillars, questions, and the AWS Well-Architected Tool to evaluate architectures, surface risks, and recommend improvements so teams can design resilient, efficient, and secure systems. It is guidance to inform decisions and remediation—not an automated cost-cutting tool, a migration engine, or a replacement for formal audits.  
Domaine  
Domain 1: Cloud Concepts  
Question 31Correct  
A company is learning about its responsibilities that are related to the management of Amazon EC2 instances. Which tasks for EC2 instances are the company’s responsibility, according to the AWS shared responsibility model? (Choose two.)  
A. Install and patch the machine hypervisor.

#### Explications

Incorrect. The hypervisor and underlying virtualization layer are managed by AWS as part of the infrastructure (the “security OF the cloud”). Customers do not install or patch the hypervisor for Amazon EC2.  
**Votre sélection est correcte**  
B. Patch the guest operating system.

#### Explications

Correct. For EC2 instances the customer is responsible for securing and maintaining the guest operating system, which includes applying OS updates and patches, configuring system-level security, and managing installed software.  
**Votre sélection est correcte**  
C. Encrypt data at rest on associated storage.

#### Explications

Correct. Ensuring data is encrypted at rest for storage attached to an instance is a customer responsibility (security IN the cloud). Customers can enable EBS encryption, configure S3 encryption, and manage keys via AWS KMS or their own key management solution.  
D. Install the physical hardware and cabling.

#### Explications

Incorrect. Physical hardware, rack equipment, and cabling are part of AWS’s facility and infrastructure responsibilities; customers do not perform physical installation in AWS data centers.  
E. Provide physical security for the EC2 instances.

#### Explications

Incorrect. Physical data center security (facility access, perimeter controls) is handled by AWS. Customers are responsible for logical security of their instances—network controls, security groups, OS hardening, and IAM—but not physical site security.  
Explication générale  
This question tests the AWS shared responsibility model. AWS is responsible for the physical infrastructure and virtualization layer (the cloud’s underlying hardware, hypervisor, and facility security). Customers are responsible for what they deploy into the cloud—managing and patching the guest OS and securing their data (including configuring encryption at rest and key management). The other options describe AWS-side responsibilities and are therefore incorrect.  
Domaine  
Domain 2: Security and Compliance  
Question 32Correct  
A company need an AWS service that provides a clear baseline of what the company runs in its on-premises data centers. The company needs the projected cost to run its on-premises workloads in the AWS Cloud. What AWS service or tool will meet these requirements?  
A. AWS Compute Optimizer

#### Explications

Compute Optimizer analyzes resource utilization and provides size/type recommendations for existing AWS compute resources (EC2, EBS, Lambda, Auto Scaling). It relies on AWS monitoring data and does not perform on-premises inventorying or produce migration cost projections, so it does not meet the requirement.  
B. AWS Cost Explorer

#### Explications

Cost Explorer uses historical AWS billing and usage data to visualize spend and forecast future AWS costs. It cannot discover or baseline on-premises workloads nor produce migration-specific TCO estimates from on-premises telemetry.  
C. AWS Systems Manager Agent (SSM Agent)

#### Explications

The Systems Manager Agent is software that enables Systems Manager capabilities (Run Command, Session Manager, Inventory, Patch Manager) on managed instances. While Inventory can collect metadata from machines, the agent alone does not perform full migration assessments or generate AWS cost projections for on-premises environments.  
**Votre réponse est correcte**  
D. Migration Evaluator

#### Explications

This service collects on-premises workload metadata (via a lightweight collector/appliance), creates an inventory and performance baseline, maps workloads to appropriate AWS instance types, and generates total cost of ownership and projected AWS spend for those workloads—providing the required baseline and cost projection for migration planning.  
Explication générale  
The question tests knowledge of AWS migration assessment tools. The correct solution is the service that inventories on-premises workloads, builds performance baselines, maps them to AWS resources, and produces TCO/migration cost projections. Other options are AWS-centric (Compute Optimizer and Cost Explorer) or are management agents (SSM Agent) and therefore do not provide end-to-end on-premises baselineing and cost projection for migration.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 33Correct  
Which AWS service allows users to model and provision AWS resources using common programming languages?  
A. AWS CloudFormation

#### Explications

CloudFormation is a declarative Infrastructure as Code service that defines stacks using JSON or YAML templates. It provisions resources based on those templates but does not natively let you author resource definitions using general-purpose programming languages; higher-level tools can generate CloudFormation templates instead.  
B. AWS CodePipeline

#### Explications

CodePipeline is a continuous delivery orchestration service that automates build, test, and deployment stages. It can run IaC tools as steps in a pipeline but is not itself a service for modelling or defining infrastructure resources.  
**Votre réponse est correcte**  
C. AWS Cloud Development Kit (AWS CDK)

#### Explications

The AWS Cloud Development Kit (CDK) provides high-level libraries (constructs) and allows developers to define cloud infrastructure using familiar languages (TypeScript, Python, Java, .NET). CDK code is synthesized into CloudFormation templates (cdk synth) and deployed via CloudFormation (cdk deploy), combining language features, reuse, and testing with AWS provisioning.  
D. AWS Systems Manager

#### Explications

Systems Manager is an operations and management service offering capabilities like Parameter Store, Run Command, Automation, and Patch Manager to operate and maintain resources. It is focused on operational tasks and configuration management, not on modelling and provisioning infrastructure via programming languages.  
Explication générale  
This item tests Infrastructure-as-Code knowledge. The Cloud Development Kit (CDK) is the appropriate choice because it enables modelling AWS resources programmatically in general-purpose languages and synthesizes those definitions into CloudFormation for provisioning. The other options either use declarative templates (CloudFormation), orchestrate CI/CD workflows (CodePipeline), or provide operational management (Systems Manager), and therefore do not provide the same language-based modelling & synthesis workflow.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 34Correct  
A company has a physical tape library to store data backups. The tape library is running out of space. The company needs to extend the tape library's capacity to the AWS Cloud. Which AWS service should the company use to meet this requirement?  
A. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed, scalable NFS file system for Linux-based workloads and on‑prem access via NFS clients. It is not designed to present virtual tape libraries or integrate with backup applications that expect tape/VTL interfaces, so it cannot directly extend a physical tape library workflow.  
B. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS provides block storage for EC2 instances (AZ-scoped volumes) and is optimized for attached disk storage for VMs. It does not provide a tape library or VTL interface and is not suitable as a drop‑in extension for tape-based backup systems or long‑term archival workflows.  
C. Amazon S3

#### Explications

Amazon S3 is durable object storage commonly used for backups and archives (including S3 Glacier/Glacier Deep Archive for archival). However, S3 by itself does not emulate tape hardware or present an iSCSI VTL to existing backup software; a gateway is required to present virtual tapes while storing data in S3/Glacier.  
**Votre réponse est correcte**  
D. AWS Storage Gateway

#### Explications

AWS Storage Gateway (Tape Gateway) presents virtual tape libraries (VTLs) via an iSCSI interface to existing backup applications, storing virtual tape cartridges as objects in Amazon S3 and allowing archival to S3 Glacier/Glacier Deep Archive. This preserves existing tape workflows while moving capacity to AWS, making it the correct service for extending a physical tape library to the cloud.  
Explication générale  
Cette question évalue les connaissances sur les services AWS qui s'intègrent aux flux de travail de sauvegarde sur bande sur site. AWS Storage Gateway Tape Gateway fournit une interface VTL que les logiciels de sauvegarde existants peuvent utiliser pour stocker des bandes virtuelles dans S3 (et les archiver dans Glacier), étendant ou remplaçant ainsi directement une bibliothèque de bandes physiques. EFS et EBS sont des solutions de stockage de fichiers/blocs pour le calcul, et S3 est le système de stockage d'objets principal ; aucun de ces services ne propose à lui seul l'interface bande/VTL nécessaire au maintien des flux de travail de sauvegarde sur bande existants.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 35Correct  
Une entreprise souhaite utiliser des piles d'applications pour exécuter une charge de travail dans le cloud AWS. Elle souhaite utiliser des instances préconfigurées. Quel service AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Voile lumineuse Amazon

#### Explications

Lightsail est une offre de serveur privé virtuel (VPS) géré avec des modèles prêts à l'emploi (piles d'applications et images de système d'exploitation), une mise en réseau simplifiée, un stockage et une tarification prévisible qui permettent aux utilisateurs de lancer des environnements d'applications courants (par exemple, LAMP, WordPress, Node.js) sans avoir à construire et configurer l'infrastructure à partir de zéro.  
B. Amazone Athéna

#### Explications

Athena est un service de requêtes interactives sans serveur qui exécute des requêtes SQL directement sur les données stockées dans Amazon S3. Il ne fournit ni instances de calcul gérées ni piles d'applications préconfigurées pour le déploiement des charges de travail applicatives.  
C. Postes avancés AWS

#### Explications

Outposts fournit l'infrastructure et les services AWS sur site pour prendre en charge les charges de travail sensibles à la latence ou nécessitant une présence des données sur site. Cette solution repose sur du matériel et des racks et n'est pas conçue pour fournir des piles d'applications préconfigurées hébergées dans le cloud pour un déploiement rapide.  
D. Amazon EC2

#### Explications

EC2 propose des machines virtuelles brutes (IaaS) offrant un contrôle total sur l'installation du système d'exploitation et des logiciels. Bien qu'il soit possible de créer ou de trouver des AMI, ou d'utiliser la Marketplace pour simplifier le déploiement, EC2 exige une configuration et une gestion plus manuelles qu'un service géré basé sur un modèle prédéfini.  
Explication générale  
Cette question teste vos connaissances des services AWS offrant des environnements applicatifs clés en main. La bonne réponse est le service VPS managé, qui fournit des modèles d'application préconfigurés, une gestion simplifiée, ainsi que des services réseau et de stockage intégrés, facilitant ainsi un déploiement rapide. Les autres options (Athena, Outposts, EC2) répondent à des besoins différents : requêtes interactives, extension sur site et serveurs virtuels bruts respectivement, et ne satisfont donc pas aux exigences relatives aux piles d'applications préconfigurées hébergées dans le cloud.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 36Correct  
Laquelle des propositions suivantes décrit le mieux le modèle de responsabilité partagée d'AWS ?  
A. AWS est responsable de la sécurité \*à la fois\* du cloud et \*dans\* le cloud.

#### Explications

Incorrect. Cette option attribue à AWS la responsabilité à la fois de l'infrastructure et des ressources contrôlées par le client. En réalité, AWS gère l'infrastructure sous-jacente (installations physiques, matériel, réseau, hyperviseur et services de base), tandis que les clients doivent sécuriser leurs propres données, systèmes d'exploitation, applications et contrôles d'accès au sein du cloud.  
**Votre réponse est correcte**  
B. AWS est responsable de la sécurité \*du\* cloud, et le client est responsable de la sécurité \*dans\* le cloud.

#### Explications

Correct. AWS is responsible for security "of" the cloud — the physical data centers, global network, hardware, and foundational managed services. Customers are responsible for security "in" the cloud — their data, identity and access management (IAM), OS and application patching, encryption keys and configuration of network controls (security groups, NACLs). The exact split shifts by service model (IaaS vs PaaS vs SaaS). Examples: AWS secures the hypervisor and host for EC2; the customer secures the guest OS and application. For S3, AWS secures the service; customers configure bucket policies and encryption for their data.  
C. Customers are responsible for security \*of\* the cloud, and AWS handles security \*in\* the cloud.

#### Explications

Incorrect. This option reverses the roles. Customers do not manage the physical infrastructure, facilities, or core networking — those are AWS responsibilities. Placing infrastructure-level security on the customer would contradict the shared responsibility model.  
D. Both AWS and customers are responsible for security \*of\* the cloud.

#### Explications

Incorrect. This implies customers share responsibility for securing the underlying cloud infrastructure. In practice, customers do not control or secure AWS physical infrastructure and hypervisor; their responsibilities are limited to resources and configurations they manage within the cloud environment.  
Explication générale  
This question tests understanding of the AWS shared responsibility model: AWS handles security of the cloud (physical infrastructure, global network, and foundational services); customers handle security in the cloud (data, IAM, OS/applications, and resource configuration). Answer Option 2 correctly reflects that division. The other options either place all responsibility on AWS, reverse the responsibilities, or incorrectly assign infrastructure security to customers.  
Domaine  
Domain 2: Security and Compliance  
Question 37Correct  
A company is running and managing its own Docker environment on Amazon EC2 instances. The company wants an alternative to help manage cluster size, scheduling, and environment maintenance. Which AWS service meets these requirements?  
A. AWS Lambda

#### Explications

Designed for short-lived, event-driven function execution, this service runs individual function code in response to events and does not provide cluster orchestration, scheduling, or automatic management of container host infrastructure.  
B. Amazon RDS

#### Explications

A managed relational database service that automates database tasks (backups, patching, scaling of DB instances) and has no functionality for scheduling containers or managing container clusters.  
**Votre réponse est correcte**  
C. AWS Fargate

#### Explications

A serverless container compute option that removes the need to provision or manage EC2 capacity for containers. It integrates with container orchestration (ECS/EKS) and handles task placement, scaling, and underlying infrastructure maintenance (capacity, patching), which meets the requirements for reducing cluster-size and environment management overhead.  
D. Amazon Athena

#### Explications

Un service de requêtes interactives pour l'analyse de données dans le stockage d'objets ; il permet d'effectuer des requêtes SQL sur des fichiers dans S3 et n'offre pas de gestion de clusters de conteneurs, de planification ou de maintenance de l'environnement hôte.  
Explication générale  
Cette question évalue vos connaissances sur les options de conteneurs gérés d'AWS. La bonne réponse propose un modèle de calcul sans serveur pour les conteneurs, éliminant ainsi la nécessité de provisionner et de gérer les instances EC2 et les opérations de cluster associées. Les autres options correspondent à des services gérés sans rapport avec ce sujet (fonction en tant que service, bases de données gérées et requêtes interactives) et ne traitent donc pas du dimensionnement, de la planification ni de la maintenance de l'environnement des clusters de conteneurs.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 38Correct  
Une entreprise souhaite migrer sa base de données vers un service AWS géré compatible avec PostgreSQL. Quels services AWS répondent à ces exigences ? (Choisissez deux réponses.)  
A. Amazone Athéna

#### Explications

Athena est un service de requêtes interactives sans serveur qui exécute des requêtes SQL directement sur les données stockées dans Amazon S3. Il s'agit d'un service d'analyse et de requêtes, et non d'un moteur de base de données relationnelle géré. Il ne prend donc pas en charge la compatibilité avec le protocole PostgreSQL ni les fonctionnalités de base de données gérée (correctifs, sauvegardes automatisées, disponibilité multi-AZ) nécessaires à une migration PostgreSQL simple.  
**Votre sélection est correcte**  
B. Amazon RDS

#### Explications

Le moteur PostgreSQL d'RDS est une solution de base de données relationnelle entièrement gérée qui automatise le provisionnement, les correctifs logiciels, les sauvegardes, la restauration à un point précis dans le temps et la haute disponibilité multi-AZ. Il prend en charge les fonctionnalités natives de PostgreSQL et les méthodes de migration standard (par exemple, via AWS Database Migration Service ou les fonctions natives pg\_dump/pg\_restore), ce qui le rend idéal pour la migration de bases de données PostgreSQL existantes.  
C. Amazon EC2

#### Explications

EC2 fournit des instances de calcul brutes permettant d'installer et d'exécuter PostgreSQL, mais le client est responsable de l'installation, des correctifs, des sauvegardes, de la mise à l'échelle et de la haute disponibilité de la base de données. Ces tâches administratives n'étant pas gérées par AWS sur EC2, cette solution ne répond pas aux exigences d'un service compatible PostgreSQL géré.  
D. Amazon DynamoDB

#### Explications

DynamoDB est une base de données NoSQL clé-valeur et document entièrement gérée, conçue pour une faible latence à grande échelle. Son modèle de données et son API ne sont pas compatibles avec SQL/PostgreSQL ; elle ne peut donc pas servir de cible directe pour les migrations PostgreSQL ni accepter les clients utilisant le protocole réseau PostgreSQL.  
**Votre sélection est correcte**  
E. Amazon Aurora

#### Explications

L'édition d'Amazon Aurora compatible avec PostgreSQL implémente le protocole et le dialecte PostgreSQL, tout en offrant un moteur natif du cloud et géré, avec un stockage distribué et tolérant aux pannes, des performances accrues, des réplicas en lecture et une mise à l'échelle automatique du stockage. Elle prend en charge les outils de migration PostgreSQL standard et AWS DMS, ce qui en fait une cible gérée idéale pour les migrations PostgreSQL.  
Explication générale  
Cette question teste la connaissance des services gérés AWS compatibles avec PostgreSQL. Les réponses correctes sont les moteurs de bases de données relationnelles gérés qui implémentent la compatibilité avec PostgreSQL et offrent des solutions de migration et des fonctionnalités opérationnelles gérées : RDS (moteur PostgreSQL) et Aurora (compatible PostgreSQL). Les réponses incorrectes sont des services aux finalités différentes : Athena (analyse S3), DynamoDB (NoSQL) et EC2 (calcul autogéré), qui ne proposent aucun service de base de données géré et compatible PostgreSQL adapté à la migration.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 39Correct  
Une entreprise souhaite migrer son infrastructure de conteneurs sur site vers le cloud AWS. Elle souhaite éviter les coûts imprévus d'administration et d'exploitation et adopter une architecture sans serveur. Quel service AWS répond à ces exigences ?  
A. Amazon Connect

#### Explications

Incorrect — Amazon Connect est le service de centre de contact cloud d'AWS pour les interactions clients (voix, chat). Il ne propose pas d'orchestration de conteneurs ni de calcul sans serveur pour conteneurs et n'a aucun lien avec la migration des charges de travail conteneurisées.  
**Votre réponse est correcte**  
B. AWS Fargate

#### Explications

Exact — AWS Fargate est un moteur de calcul sans serveur pour conteneurs qui s'exécute avec Amazon ECS et Amazon EKS. Il élimine la nécessité de provisionner, configurer ou gérer des instances EC2, ainsi que la facturation par vCPU et par ressource mémoire. Il réduit ainsi les coûts opérationnels et les risques de dépenses imprévues liées à l'administration et à l'exploitation lors de la migration d'applications conteneurisées.  
C. Voile lumineuse Amazon

#### Explications

Incorrect — Amazon Lightsail est une plateforme d'hébergement VPS et d'applications simplifiée, conçue pour les charges de travail simples et de petite taille. Elle n'offre pas les mêmes capacités de calcul conteneurisé sans serveur et entièrement gérées, ni l'intégration d'orchestration (ECS/EKS \+ Fargate) nécessaires pour éliminer la gestion de l'infrastructure à grande échelle.  
D. Amazon EC2

#### Explications

Incorrect — Amazon EC2 est une infrastructure en tant que service (serveurs virtuels) qui nécessite un provisionnement, des mises à jour, une gestion de la capacité et une mise à l'échelle. L'utilisation d'EC2 transfère la responsabilité opérationnelle au client et ne répond pas à l'exigence d'adopter une architecture de conteneurs sans serveur.  
Explication générale  
Ce test évalue vos connaissances en matière de calcul de conteneurs sans serveur sur AWS. AWS Fargate est la solution idéale car elle fournit un environnement d'exécution géré et sans serveur pour les conteneurs (intégré à ECS/EKS), éliminant ainsi la nécessité de gérer les instances EC2 sous-jacentes et réduisant les coûts administratifs et opérationnels imprévus. Les autres options sont soit sans rapport avec les conteneurs (Amazon Connect), soit centrées sur l'infrastructure et nécessitant une gestion plus poussée (EC2), soit une offre VPS simplifiée non conçue pour l'orchestration de conteneurs sans serveur (Lightsail).  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 40Correct  
Quel service ou fonctionnalité AWS prend en charge la gouvernance, la conformité et l'audit des risques des comptes AWS ?  
A. Authentification multifactorielle (MFA)

#### Explications

Incorrect. L'authentification multifacteur (MFA) est un contrôle d'authentification qui ajoute un deuxième facteur à la connexion utilisateur afin de réduire les risques de compromission de compte. Elle ne permet pas l'enregistrement, l'audit ou la génération de rapports centralisés sur l'activité des API au sein d'un compte ou d'une organisation AWS.  
B. AWS Lambda

#### Explications

Incorrect. AWS Lambda est un service de calcul sans serveur permettant d'exécuter du code en réponse à des événements. Bien que Lambda puisse traiter les journaux d'audit ou y répondre, il ne fournit pas de fonctionnalités de gouvernance, de conformité ou d'audit.  
C. Service de notification simple d'Amazon (Amazon SNS)

#### Explications

Incorrect. Amazon SNS est un service de messagerie et de notification de type publication/abonnement utilisé pour diffuser des messages et des alertes. Il peut servir à distribuer des notifications concernant des événements, mais n'enregistre pas l'activité de l'API ni ne réalise d'audit.  
**Votre réponse est correcte**  
D. AWS CloudTrail

#### Explications

Exact. AWS CloudTrail enregistre les appels d'API AWS et les événements associés au sein d'un compte (événements de gestion et événements de données optionnels), transfère les journaux vers Amazon S3 (et peut les diffuser en continu vers CloudWatch Logs), et s'intègre aux services d'analyse et de sécurité (Athena, GuardDuty, Security Hub, AWS Config). Ces événements enregistrés permettent la gouvernance, la production de rapports de conformité, l'analyse forensique et l'audit des risques.  
Explication générale  
Cette question évalue les connaissances relatives aux services AWS offrant des fonctionnalités d'audit et de gouvernance. AWS CloudTrail est le service approprié car il capture, stocke et permet l'analyse de l'activité et des événements des API sur l'ensemble des comptes AWS, facilitant ainsi la conformité et l'audit des risques. Les autres options concernent l'authentification (MFA), le calcul (Lambda) ou la messagerie (SNS) et ne proposent pas de journalisation d'audit centralisée ni d'historique des événements.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 41Correct  
Une entreprise a déployé plusieurs applications publiques derrière des équilibreurs de charge d'application. Elle souhaite améliorer les performances de ces applications. Quel service AWS répond à ces exigences ?  
**Votre réponse est correcte**  
A. Accélérateur mondial AWS

#### Explications

Global Accelerator est la solution optimale car elle optimise les chemins réseau entre l'utilisateur et l'application en utilisant le réseau mondial AWS et des adresses IP anycast statiques. Le trafic est ainsi dirigé vers le point de présence AWS le plus approprié, puis acheminé via le réseau dorsal AWS jusqu'aux points de terminaison ALB. Cela réduit la latence et la perte de paquets pour les utilisateurs du monde entier sans nécessiter de modifications applicatives et s'intègre directement aux ALB en tant que points de terminaison.  
B. Amazon Connect

#### Explications

Incorrect. Amazon Connect est un service de centre de contact cloud géré pour les flux de travail voix/chat. Il ne propose pas d'optimisation du chemin réseau, de routage du trafic global ni d'accélération pour les applications web publiques.  
C. Amazon ElastiCache

#### Explications

Pertinent, mais pas idéal. ElastiCache est un service de cache en mémoire qui réduit la latence de récupération des données côté application depuis les bases de données, améliorant ainsi les performances du serveur pour les opérations avec état. Il ne prend pas en charge le routage global du trafic ni l'accélération du transport réseau client-serveur entre régions ou sur l'Internet public.  
D. Amazon CloudWatch

#### Explications

Incorrect. Amazon CloudWatch offre des fonctionnalités d'observabilité (métriques, journaux, alarmes) et peut aider à détecter les problèmes de performance et à y répondre, mais il ne modifie pas le routage réseau ni ne réduit la latence côté client en accélérant le trafic.  
Explication générale  
La question vise à améliorer les performances des applications publiques derrière des équilibreurs de charge d'application (ALB) pour les utilisateurs finaux. La solution appropriée est Global Accelerator, car elle réduit la latence entre le client et AWS en utilisant le réseau mondial d'AWS et des adresses IP anycast statiques, et en acheminant le trafic vers le point de terminaison opérationnel le plus proche (y compris les ALB). Les autres solutions répondent à d'autres besoins : ElastiCache accélère l'accès aux données backend (nécessite une intégration à l'application), CloudWatch propose une surveillance et des alertes, et Amazon Connect est un produit pour centres de contact ; aucune n'offre l'accélération au niveau du réseau global proposée par Global Accelerator.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 42Correct  
Quels sont les avantages de la migration vers le cloud AWS ? (Choisissez trois réponses.)  
**Votre sélection est correcte**  
A. Économies réalisées grâce à la tarification à l'utilisation

#### Explications

AWS facture la consommation de ressources et propose des options d'achat flexibles (instances à la demande, instances réservées, plans d'économies, instances Spot), ainsi que des outils de gestion des coûts (Cost Explorer, Budgets, Trusted Advisor). Ces fonctionnalités permettent aux entreprises de transformer d'importants investissements initiaux en dépenses d'exploitation maîtrisables et d'optimiser leurs dépenses en fonction de leur utilisation réelle.  
B. Complexité opérationnelle accrue

#### Explications

Cette option décrit un inconvénient, et non un avantage. AWS propose de nombreux services gérés et d'automatisation (AWS CloudFormation, Systems Manager, RDS, ECS/EKS) qui réduisent généralement les coûts opérationnels ; bien que les migrations puissent engendrer une complexité temporaire, une complexité opérationnelle accrue à long terme ne constitue pas un avantage intrinsèque.  
**Votre sélection est correcte**  
C. Évolutivité et flexibilité accrues

#### Explications

AWS offre une évolutivité et une élasticité natives grâce à des services tels qu'Amazon EC2 Auto Scaling, Elastic Load Balancing, le calcul sans serveur (AWS Lambda) et les services gérés à grande échelle (Amazon RDS, Amazon ECS/EKS). Ces fonctionnalités permettent aux applications d'adapter rapidement leur capacité à l'évolution de la demande sans provisionnement manuel.  
D. Portée géographique limitée

#### Explications

AWS exploite une infrastructure mondiale de régions et de zones de disponibilité, ainsi que des points de présence (Amazon CloudFront, Global Accelerator), ce qui étend sa couverture géographique et assure une diffusion mondiale à faible latence. Par conséquent, l'expression « couverture géographique limitée » est incorrecte.  
**Votre sélection est correcte**  
E. Amélioration de la sécurité et de la conformité grâce aux services AWS

#### Explications

AWS propose un large éventail de fonctionnalités de sécurité et de conformité (AWS Identity and Access Management, AWS KMS, contrôles réseau VPC, CloudTrail, AWS Config, AWS Shield) et détient de nombreuses attestations de conformité. REMARQUE : la sécurité est assurée dans le cadre du modèle de responsabilité partagée d’AWS ; il incombe donc aux clients de configurer et d’utiliser correctement ces services.  
Explication générale  
Les principaux avantages du cloud testés sont la tarification à la consommation et les fonctionnalités d'optimisation des coûts d'AWS, son évolutivité et sa flexibilité intégrées, ainsi que les outils de sécurité et de conformité fournis par AWS. Les réponses faisant référence à ces avantages sont correctes ; les distracteurs décrivant des conséquences négatives (complexité opérationnelle accrue ou portée géographique limitée) sont incorrects car les services gérés et l'infrastructure mondiale d'AWS répondent à ces préoccupations. Une utilisation appropriée des services AWS et le respect du modèle de responsabilité partagée sont nécessaires pour bénéficier de ces avantages.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 43Incorrect  
Un ingénieur cloud souhaite stocker des données sur Amazon S3. Il accédera à certaines données annuellement et à d'autres quotidiennement. Quelle classe de stockage S3 répondra le mieux à ces exigences en termes de coût ?  
A. Norme S3

#### Explications

S3 Standard offre une haute disponibilité et une faible latence pour les objets fréquemment consultés, mais son coût de stockage est plus élevé que pour les données rarement consultées ou archivées. Utiliser Standard pour des données consultées seulement une fois par an serait inutilement coûteux par rapport aux options hiérarchisées ou d'archivage.  
Archives profondes du glacier B. S3

#### Explications

S3 Glacier Deep Archive offre la solution de stockage la plus économique pour la conservation à long terme, mais elle est conçue pour les données d'archivage dont les temps de récupération se comptent en heures et qui engendrent des coûts supplémentaires. Elle ne convient pas aux données nécessitant un accès quotidien ou exigeant une faible latence.  
**Votre réponse est incorrecte**  
C. S3 Une zone \- Accès peu fréquent (S3 Une zone \- IA)

#### Explications

S3 One Zone-IA stocke les objets dans une seule zone de disponibilité à un coût inférieur à celui des classes IA multi-AZ, mais il ne bénéficie pas de la même résilience et ne reclasse pas automatiquement les objets en fonction de l'évolution des modèles d'accès. Il n'est donc pas adapté lorsque certains objets nécessitent un accès fréquent, voire quotidien, tandis que d'autres sont consultés rarement.  
**Bonne réponse**  
D. S3 Hiérarchisation intelligente

#### Explications

La hiérarchisation intelligente surveille de manière transparente les habitudes d'accès aux objets et déplace ces derniers entre les différents niveaux d'accès (accès fréquent et peu fréquent, ainsi que des niveaux d'archivage optionnels) afin de réduire les coûts de stockage pour les ensembles de données dont les comportements d'accès sont variés ou fluctuants. Elle engendre des frais minimes de surveillance et d'automatisation par objet, mais supprime la nécessité de définir manuellement les règles de cycle de vie, ce qui la rend rentable pour un usage mixte, avec des accès quotidiens et annuels.  
Explication générale  
Cette question évalue le choix d'une classe de stockage S3 adaptée à des modèles d'accès mixtes. L'option la plus rentable est Intelligent-Tiering, car elle répartit automatiquement les objets entre les niveaux d'accès en fonction de leur utilisation réelle, évitant ainsi la gestion manuelle du cycle de vie et réduisant les coûts pour les éléments rarement consultés, tout en prenant en charge les objets fréquemment consultés. Les autres options sont soit trop coûteuses pour les données rarement consultées (Standard), soit trop lentes/axées sur l'archivage pour un accès quotidien (Glacier Deep Archive), soit ne proposent pas de hiérarchisation automatique ni de compromis optimal en matière de résilience (One Zone-IA).  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 44Correct  
Quel service AWS prend en charge les fonctionnalités d'inscription et d'authentification des utilisateurs pour les applications mobiles et Web ?  
**Votre réponse est correcte**  
A. Amazon Cognito

#### Explications

Fournit une solution d'identité entièrement gérée pour les utilisateurs d'applications : les groupes d'utilisateurs servent d'annuaire et prennent en charge les flux d'inscription et de connexion, l'interface utilisateur hébergée, la vérification par e-mail/téléphone, l'authentification multifacteur et l'émission de jetons JWT standard pour la gestion des sessions ; les groupes d'identités fédérés associent les identités authentifiées à des informations d'identification AWS temporaires et prennent en charge la fédération sociale et d'entreprise (SAML/OIDC). Ces fonctionnalités répondent directement aux exigences d'authentification des applications mobiles et web.  
B. Configuration AWS

#### Explications

Ce service de suivi et de conformité des configurations de ressources enregistre, évalue et audite les configurations des ressources AWS (règles Config, packs de conformité, instantanés de configuration). Il ne dispose ni d'annuaire d'utilisateurs, ni de processus d'inscription, ni d'authentification par jeton pour les utilisateurs de l'application ; il ne répond donc pas à la question posée.  
C. Amazon GuardDuty

#### Explications

Ce service de détection des menaces, géré par nos soins, analyse les journaux CloudTrail, les journaux de flux VPC et les journaux DNS afin de détecter les activités suspectes et les failles de sécurité. Il est destiné à la surveillance et à l'alerte de sécurité, et non à la gestion des identités ou à l'authentification des utilisateurs finaux.  
D. Responsable des systèmes AWS

#### Explications

Service d'exploitation et de gestion permettant d'exécuter des commandes, de gérer des sessions, de stocker des paramètres et d'automatiser les tâches opérationnelles (Exécuter une commande, Gestionnaire de sessions, Gestionnaire de paramètres, Gestionnaire de correctifs). Il est axé sur la gestion des ressources et les outils opérationnels, et ne propose pas d'inscription ni d'authentification des utilisateurs pour les applications.  
Explication générale  
Cette question porte sur les fonctionnalités d'identité et d'authentification d'AWS. La solution appropriée est le service d'identité géré qui propose des groupes d'utilisateurs pour l'inscription et la connexion, l'émission de jetons, la fédération avec les fournisseurs d'identité d'entreprise et de réseaux sociaux, ainsi qu'un mappage optionnel vers les identifiants AWS — des fonctionnalités indispensables aux applications mobiles et web. Les autres options concernent la gestion de la configuration, la détection des menaces ou la gestion opérationnelle et ne prennent pas en charge l'inscription et l'authentification des utilisateurs finaux.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 45Correct  
Une entreprise envisage de migrer vers le cloud AWS. Elle souhaite identifier des résultats commerciaux mesurables qui démontreront la valeur de sa décision de migration. À quelle phase du parcours de transformation vers le cloud appartiennent ces activités ?  
**Votre réponse est correcte**  
A. Envisager

#### Explications

Cette phase initiale de la transformation vers le cloud définit les objectifs stratégiques et les traduit en résultats commerciaux mesurables et en indicateurs clés de performance (KPI). Les activités typiques comprennent la définition des indicateurs de succès, la quantification des avantages attendus (par exemple, les économies de coûts, l'amélioration du délai de mise sur le marché ou l'agilité opérationnelle) et la création d'une analyse de rentabilité axée sur la valeur qui orientera la planification et la priorisation ultérieures.  
B. Align

#### Explications

Cette phase est axée sur l'alignement des parties prenantes, la gouvernance et l'élaboration de la feuille de route de migration et du modèle opérationnel. Elle privilégie la recherche de consensus et la planification plutôt que la définition des résultats commerciaux mesurables qui justifieraient le passage au cloud.  
C. Échelle

#### Explications

This stage comes after initial adoption and is focused on broadening and optimizing cloud use—standardizing platforms, automating operations, and scaling workloads. Its goals are expansion and operational maturity, not the upfront definition of business outcomes and KPIs.  
D. Launch

#### Explications

This stage is execution-oriented, covering pilots, proofs of concept, and initial migrations to validate assumptions and deliver early workloads. It is concerned with implementation and delivery, not the strategic task of identifying the measurable outcomes that demonstrate migration value.  
Explication générale  
The question targets knowledge of the cloud transformation journey phases. The correct choice is the initial phase that defines strategic objectives, success metrics, and a business case—this is where measurable business outcomes are identified. The other phases focus on stakeholder alignment and governance, executing pilots and migrations, or scaling and optimization, so they are not the primary phases for defining those outcomes.  
Domaine  
Domain 1: Cloud Concepts  
Question 46Incorrect  
In which situations should a company create an IAM user instead of an IAM role?  
A. When an application that runs on Amazon EC2 instances requires access to other AWS services

#### Explications

Applications running on Amazon EC2 should assume an IAM role via an instance profile. Roles provide short‑lived, automatically rotated credentials through the EC2 instance metadata service (IMDS), avoiding long‑term access keys and improving security and credential management.  
**Bonne réponse**  
B. When the company creates AWS access credentials for individuals

#### Explications

IAM users represent long‑term identities within an AWS account and are appropriate when individuals require persistent credentials (console password and/or programmatic access keys). Use IAM users together with IAM policies and groups to manage permissions for those identities, while considering federation or AWS IAM Identity Center for enterprise SSO.  
C. When the company creates an application that runs on a mobile phone that makes requests to AWS

#### Explications

Embedding permanent credentials in a mobile app is insecure. Mobile and web apps should obtain temporary credentials by using an identity provider (for example Amazon Cognito, OIDC, or a federated provider) that exchanges authentication for an IAM role with temporary credentials.  
**Votre réponse est incorrecte**  
D. When the company needs to add users to IAM groups

#### Explications

IAM groups are collections of IAM users used to apply common policies. While creating a user is a prerequisite for membership in an IAM group, this is a user‑management detail rather than a primary justification for choosing a user over a role; many organizations prefer federation/SSO instead of creating long‑term IAM users.  
E. When users are authenticated in the corporate network and want to be able to use AWS without having to sign in a second time

#### Explications

This scenario describes federated single sign‑on. Best practice is to grant access through federation and assume IAM roles (via SAML, OIDC, or IAM Identity Center) so users authenticate with corporate credentials and receive temporary AWS permissions rather than creating separate IAM users.  
Explication générale  
The question tests understanding of IAM identities vs. roles. IAM users are persistent identities for individuals who need long‑term AWS credentials and integration with IAM policies and groups. IAM roles are for temporary, delegated access (for EC2, mobile/web apps via Cognito, federated users, cross‑account access). Option B is the correct choice because it reflects the appropriate use of an IAM user; the other options describe cases where roles or federation and temporary credentials are the recommended approach.  
Domaine  
Domain 2: Security and Compliance  
Question 47Correct  
A company's employees are working from home. The company wants its employees to use their personal devices to connect to a managed workstation in the AWS Cloud. Which AWS service should the company use to provide the remote environment?  
**Votre réponse est correcte**  
A. Amazon Workspaces

#### Explications

Provides a fully managed Desktop-as-a-Service (DaaS) solution hosted in AWS that delivers persistent virtual desktops to end users. It integrates with AWS Directory Service or AD Connector for authentication, supports encryption in transit and at rest, centralized image and patch management, and client applications for multiple personal device types — all features that meet the requirement for managed workstations accessible from employee personal devices.  
B. AWS Cloud9

#### Explications

A cloud-based integrated development environment (IDE) intended for coding, debugging, and terminal access. It runs development environments (usually on EC2) and lacks the persistent, full-featured managed desktop experience, centralized OS image management, and DaaS controls needed for company-managed workstations for general employee use.  
C. AWS Outposts

#### Explications

An on-premises extension of AWS infrastructure for running selected AWS services locally. It requires physical hardware at a customer site and is intended to bring AWS services closer to on-premises workloads — not to provide cloud-hosted managed virtual desktops for remote workers connecting from personal devices.  
D. Amazon Lightsail

#### Explications

A simplified virtual private server offering for small applications and websites with predictable pricing. It provides basic instances and networking but does not provide a managed desktop/DaaS environment, enterprise directory integration, or the centralized desktop management features required for a company-managed workstation solution.  
Explication générale  
The scenario requires a cloud-hosted, managed desktop environment that employees can access from personal devices. The correct choice is the AWS service that offers fully managed virtual desktops with directory integration, encryption, centralized image/patch management and client support across device types. The other options are targeted at development IDEs (Cloud9), on-premises infrastructure extension (Outposts), or simple VPS hosting (Lightsail), and therefore do not satisfy the managed workstation/DaaS requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 48Correct  
A company needs to use dashboards and charts to analyze insights from business data. Which AWS service will provide the dashboards and charts for these insights?  
A. Amazon Macie

#### Explications

Macie is a security service that uses machine learning to discover, classify, and protect sensitive data (particularly in S3). It focuses on data security and privacy, not on providing business intelligence dashboards or charting capabilities.  
B. Amazon Aurora

#### Explications

Aurora is a managed, high-performance relational database compatible with MySQL and PostgreSQL. It can serve as a data source for analytics, but it does not provide built-in dashboarding or visualization features.  
**Votre réponse est correcte**  
C. Amazon QuickSight

#### Explications

The AWS managed business intelligence service provides interactive dashboards, charting, embeddable visuals, and a high-performance in-memory engine (SPICE). It connects to many AWS and external data sources, supports sharing and row-level access, and includes ML-powered insights — making it the appropriate choice for creating dashboards and charts.  
D. AWS CloudTrail

#### Explications

CloudTrail records and logs AWS API activity for auditing, compliance, and security analysis. While its logs can be analyzed by analytics tools, CloudTrail itself does not provide business dashboards or visualization tooling.  
Explication générale  
This tests recognition of AWS services for business intelligence. The correct service is the fully managed BI solution that delivers interactive dashboards, visualizations, and an in-memory engine for fast analysis. The other options are for security/data classification (Macie), relational databases (Aurora), or audit logging (CloudTrail), and therefore do not provide the integrated dashboard/visualization capabilities required.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 49Correct  
What is the MOST secure way to store passwords on AWS?  
A. Store passwords in an Amazon S3 bucket.

#### Explications

Amazon S3 is object storage and can be encrypted with SSE-S3 or SSE-KMS and access-controlled with IAM, but it does not provide secret lifecycle features (rotation, versioned secrets, fine-grained secret access APIs) and is more prone to accidental public exposure if misconfigured. For credential storage, a purpose-built secrets service is preferred.  
B. Store passwords as AWS CloudFormation parameters.

#### Explications

CloudFormation parameters are input values used during stack operations; they are not a secret-management service. Although parameters can be hidden in some views (NoEcho), CloudFormation does not offer managed encryption, rotation, or secure retrieval APIs for ongoing secret management. Use Secrets Manager or SSM Parameter Store (SecureString) for secrets instead.  
C. Store passwords in AWS Storage Gateway.

#### Explications

AWS Storage Gateway is a hybrid storage service for on-premises integration (file, volume, or tape interfaces) and is unrelated to secret management. It does not provide features such as secret rotation, versioning, or secrets-specific access controls.  
**Votre réponse est correcte**  
D. Store passwords in AWS Secrets Manager.

#### Explications

AWS Secrets Manager is a managed secrets service that stores secrets encrypted with AWS KMS, supports automatic rotation (often via Lambda), provides fine-grained IAM policies and APIs for secure retrieval, and integrates with CloudTrail for auditing. These capabilities address both protection and credential lifecycle management, making it the appropriate choice for passwords.  
Explication générale  
The correct choice is the managed secrets service because it provides encryption with KMS, built-in rotation, versioning, secure API retrieval, and auditability—features required for secure credential lifecycle management. General-purpose storage (S3) or hybrid storage (Storage Gateway) lack these secret-specific capabilities, and CloudFormation parameters are for stack inputs rather than long-term secret management.  
Domaine  
Domain 2: Security and Compliance  
Question 50Correct  
A company wants to build, train, and deploy machine learning (ML) models. Which AWS service can the company use to meet this requirement?  
A. Amazon Personalize

#### Explications

Personalize is a managed recommendation service that provides prebuilt workflows and recipes for building and serving personalized recommendations. It is specialized for recommender use cases and does not provide a general-purpose environment for developing, training, and deploying arbitrary ML models.  
B. Amazon Comprehend

#### Explications

Comprehend is a fully managed natural language processing service that offers pretrained capabilities (sentiment, entity recognition, topic modeling). It is not intended as a platform for training and hosting custom machine learning models across diverse problem types.  
C. Amazon Forecast

#### Explications

Forecast is a managed time-series forecasting service that automates building and evaluating forecasting models for demand planning and similar scenarios. It is specialized for forecasting and does not offer a general model development and deployment platform for arbitrary ML workloads.  
**Votre réponse est correcte**  
D. Amazon SageMaker

#### Explications

SageMaker is a fully managed, end-to-end machine learning service that provides tools for data labeling, Jupyter notebooks, built-in and custom training (including distributed training and hyperparameter tuning), model registry, and deployment options (real-time endpoints, serverless inference, and batch transform). These capabilities collectively address building, training, and deploying ML models at scale, matching the requirement.  
Explication générale  
The question tests knowledge of AWS services for the full ML lifecycle. The correct choice is the managed, end-to-end ML platform that supports data preparation, training (including distributed and hyperparameter tuning), model registry, and multiple deployment options. The other options are specialized, fully managed services tailored to specific tasks (recommendations, NLP, forecasting) and do not provide a general-purpose environment for building, training, and deploying arbitrary ML models.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 51Correct  
Which of the following is an advantage that the AWS Cloud provides to users?  
**Votre réponse est correcte**  
A. Users eliminate the need to guess about infrastructure capacity requirements.

#### Explications

AWS provides elasticity and on-demand resource provisioning so customers can scale capacity up or down as needed (for example via Auto Scaling, on‑demand/spot/\_reserved instances, Elastic Load Balancing, and serverless services like AWS Lambda). This removes the need for long-term capacity guessing and lets customers pay for actual usage.  
B. Users decrease their variable costs by maintaining sole ownership of IT hardware.

#### Explications

Maintaining sole ownership of hardware is an on‑premises model that increases capital expenditure and fixed costs. The AWS Cloud shifts spending to operational expense with shared, multi‑tenant infrastructure and pay‑as‑you‑go pricing, so sole ownership of hardware is not a cloud advantage.  
C. Users maintain control of underlying IT infrastructure hardware.

#### Explications

AWS is responsible for the physical infrastructure (hardware, networking, and facilities) for AWS services. Customers do not control underlying physical servers; they control resources at the service level (for example, instance configuration on Amazon EC2) but not the host hardware.  
D. Users maintain control of operating systems for managed services.

#### Explications

Managed services (for example Amazon RDS, DynamoDB, S3, and Lambda) abstract operating system and infrastructure management from the customer. While EC2 instances require OS management by the customer, managed services remove that responsibility, so customers do not retain OS control for those services.  
Explication générale  
The question tests knowledge of core cloud benefits: elasticity and on‑demand provisioning. AWS enables dynamic scaling and pay‑for‑use, which reduces the need for upfront capacity planning. Distractors describe on‑premises ownership or misunderstand managed services and AWS’s responsibility for physical infrastructure, which are not cloud advantages.  
Domaine  
Domain 1: Cloud Concepts  
Question 52Correct  
A company stores data in an Amazon S3 bucket. Which task is the responsibility of AWS?  
A. Configure an S3 Lifecycle policy.

#### Explications

Lifecycle rules are a bucket-level configuration that transition or expire objects (e.g., move to Glacier, delete after retention). These are settings that the customer must define and manage for their data lifecycle; AWS does not create or manage customers' lifecycle rules.  
B. Activate S3 Versioning.

#### Explications

Versioning is a bucket-level feature that must be explicitly enabled by the customer to keep multiple object versions and support recovery from accidental deletes/overwrites. AWS provides the capability but does not turn on versioning for customer buckets.  
C. Configure S3 bucket policies.

#### Explications

Bucket policies are resource-based access control policies attached to an S3 bucket and are authored and maintained by the customer (using IAM policy language). AWS supplies the policy framework but does not configure access controls on behalf of customers.  
**Votre réponse est correcte**  
D. Protect the infrastructure that supports S3 storage.

#### Explications

Under the AWS Shared Responsibility Model, AWS is responsible for ‘Security of the Cloud’ — protecting the physical data centers, servers, networking, storage infrastructure, and the underlying platform that runs S3. That infrastructure-level protection is an AWS responsibility.  
Explication générale  
This question tests the Shared Responsibility Model. Customers are responsible for configuring S3 features that control their data (lifecycle rules, versioning, bucket policies). AWS is responsible for protecting and operating the underlying infrastructure that provides S3 (physical hosts, networking, facilities, and the storage platform), making the infrastructure protection the AWS responsibility and the correct choice.  
Domaine  
Domain 2: Security and Compliance  
Question 53Correct  
Which characteristic of the AWS Cloud helps users eliminate underutilized CPU capacity?  
A. Agility

#### Explications

Describes the ability to move quickly to develop and deploy applications (rapid provisioning and iteration). That capability improves time-to-market but does not automatically change running compute capacity to remove idle CPU — scaling mechanisms are required for that purpose.  
**Votre réponse est correcte**  
B. Elasticity

#### Explications

Refers to the cloud capability that automatically adjusts compute capacity to match workload demand. In AWS this is implemented with services and features such as Amazon EC2 Auto Scaling (Auto Scaling groups), AWS Auto Scaling, Elastic Load Balancing and metric-driven scaling using Amazon CloudWatch. Automatic scale-out/scale-in and event-driven scaling (for example AWS Lambda concurrency) reduce the number of idle instances and underutilized vCPUs.  
C. Reliability

#### Explications

Focuses on keeping systems available and recoverable (fault tolerance, multi-AZ deployments, health checks). Availability and fault tolerance address uptime and resiliency, not the dynamic reduction of unused CPU capacity.  
D. Durability

#### Explications

Concerns long-term preservation and protection of data (for example Amazon S3’s 11‑9s durability). Durability is about storage persistence and data integrity, not compute resource utilization.  
Explication générale  
The question tests identification of the cloud characteristic that matches compute capacity to actual demand to avoid idle CPU. The correct concept is the capability to automatically scale compute resources (implemented in AWS by Auto Scaling, ELB and CloudWatch-driven policies), which reduces underutilized CPU. The other choices (rapid development speed, system reliability, and data durability) address different cloud benefits and do not by themselves eliminate idle compute capacity.  
Domaine  
Domain 1: Cloud Concepts  
Question 54Correct  
A company wants to run a graph query that provides credit card users’ names, addresses, and transactions. The company wants the graph to show if the names, addresses, and transactions indicate possible fraud. Which AWS database service will meet these requirements?  
A. Amazon DocumentDB (with MongoDB compatibility)

#### Explications

DocumentDB is a managed document (JSON) database with MongoDB-compatible APIs and is optimized for storing and querying semi-structured documents and running aggregation pipelines. It does not provide a native graph engine or graph traversal/query languages, so multi-hop relationship queries required for fraud pattern detection would be inefficient or require significant application-side logic.  
B. Amazon Timestream

#### Explications

Timestream is a serverless time-series database designed for high-scale ingestion and analysis of time-stamped metrics and events, offering time-series functions and retention policies. It is not intended for modeling or querying richly connected entities and relationships, so it’s unsuitable for graph-based fraud detection queries.  
C. Amazon DynamoDB

#### Explications

DynamoDB is a highly scalable key-value and document NoSQL database offering single-digit millisecond performance, transactions, and global replication. It lacks a native graph traversal/query capability; modeling complex relationships requires denormalization, additional indexes, or multiple round-trips, making multi-hop relationship analysis inefficient for fraud detection use cases.  
**Votre réponse est correcte**  
D. Amazon Neptune

#### Explications

Neptune is a purpose-built, fully managed graph database that supports both property graph (Apache TinkerPop Gremlin) and RDF/SPARQL models. It is optimized for fast, multi-hop traversals and querying of highly connected data (users, addresses, transactions), making it well suited for detecting fraud patterns via relationship analysis and graph algorithms.  
Explication générale  
The scenario requires efficient multi-hop relationship queries across users, addresses, and transactions to detect potential fraud. A purpose-built graph database that supports graph query languages and fast traversals is the appropriate choice. Amazon Neptune provides these capabilities (Gremlin and SPARQL, optimized traversal engine), whereas DocumentDB, Timestream, and DynamoDB are respectively document, time-series, or key-value/document stores that do not natively support graph traversals and would be poor fits for this use case.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 55Correct  
Which of the following is a key benefit of migrating existing applications to the AWS Cloud?  
A. Increased operational complexity

#### Explications

Incorrect. La migration vers AWS est généralement utilisée pour réduire la charge opérationnelle en adoptant des services gérés et l'automatisation (par exemple, Amazon RDS, AWS Lambda, AWS Systems Manager et AWS CloudFormation), qui simplifient les opérations plutôt que d'en accroître la complexité.  
**Votre réponse est correcte**  
B. Réduction des coûts grâce à la tarification à l'utilisation

#### Explications

Exactement. Migrer les charges de travail vers AWS permet une tarification à la consommation (à la demande) et un passage des dépenses d'investissement aux dépenses d'exploitation : les entreprises ne paient que pour leur consommation réelle. Ce modèle est renforcé par les outils d'optimisation des coûts et les options d'achat d'AWS (Savings Plans, Instances réservées, Auto Scaling, AWS Cost Explorer, AWS Budgets) qui contribuent à réduire le coût total de possession.  
C. Contrôles de sécurité et de conformité réduits

#### Explications

Incorrect. La migration ne réduit pas intrinsèquement la sécurité ni la conformité. AWS propose un modèle de responsabilité partagée et de nombreux services de sécurité et de conformité (IAM, AWS Config, AWS CloudTrail, Amazon GuardDuty, AWS Shield) et maintient des certifications et des attestations pour aider ses clients à respecter les exigences réglementaires.  
D. Évolutivité et flexibilité limitées

#### Explications

Incorrect. Le cloud AWS accroît l'évolutivité et la flexibilité grâce à des services tels que Auto Scaling, Elastic Load Balancing, Amazon EC2, Amazon S3 et les options sans serveur (AWS Lambda), permettant ainsi aux ressources de s'adapter à la demande plutôt que d'être limitées.  
Explication générale  
Le principal avantage testé est l'optimisation des coûts grâce à une tarification à l'usage et à la conversion des dépenses d'investissement (CapEx) en dépenses d'exploitation (OpEx), rendue possible par les modèles de tarification et les outils de gestion des coûts d'AWS. Parmi les autres avantages courants figurent une meilleure évolutivité, une plus grande agilité et une sécurité maintenue ou renforcée grâce aux services gérés d'AWS. Les autres options sont des éléments de distraction qui décrivent des résultats contraires aux avantages typiques du cloud.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 56Correct  
Quel est le cas d'utilisation recommandé pour les instances à la demande d'Amazon EC2 ?  
A. Une charge de travail stable qui nécessite une configuration d'instance EC2 particulière pendant une longue période.

#### Explications

Décrit une charge de travail prévisible et de longue durée. Pour ce type d'utilisation stable, AWS propose des instances réservées ou des plans d'économies (et des hôtes dédiés pour les besoins de location), qui permettent de réaliser des économies importantes par rapport à la tarification à la demande pour les engagements à long terme.  
B. Une charge de travail pouvant être interrompue pour un projet nécessitant le coût le plus bas possible

#### Explications

Il s'agit de charges de travail tolérantes aux interruptions et optimisées pour un coût minimal. Les instances Spot d'AWS sont le choix idéal pour les tâches interruptibles et tolérantes aux pannes, car elles offrent des remises importantes en contrepartie d'une possible résiliation lorsque la capacité est récupérée.  
**Votre réponse est correcte**  
C. Une charge de travail imprévisible qui ne nécessite pas d'engagement à long terme

#### Explications

Les instances à la demande offrent une capacité de calcul flexible et immédiate, sans engagement à long terme ni paiement initial. Elles sont idéales pour les charges de travail variables ou imprévisibles, les tâches de courte durée, le développement et les tests, ou les pics de demande nécessitant une mise en service et une libération rapides de la capacité.  
D. Une charge de travail qui devrait s'exécuter pendant plus d'un an

#### Explications

A workload expected to run for a year or more is better served by Reserved Instances or Savings Plans, which lock in usage for a term (typically one or three years) to deliver lower effective hourly costs than On-Demand pricing.  
Explication générale  
On-Demand Instances are designed for flexibility: pay-per-use compute without long-term commitment, making them ideal for unpredictable, short-term, or bursty workloads and for development/test environments. They are not the lowest-cost option for interruptible work (Spot Instances are) nor the most economical choice for stable, long-term workloads (Reserved Instances or Savings Plans are preferable).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 57Incorrect  
What is a benefit of using AWS serverless computing?  
**Votre réponse est incorrecte**  
A. Application deployment and management are not required.

#### Explications

Incorrect. Serverless still requires packaging, configuring, and deploying your application code (for example, creating Lambda functions or deploying via AWS SAM/CloudFormation). What serverless abstracts away is the management of servers, not the need to build and deploy the application itself.  
B. Application security will be fully managed by AWS.

#### Explications

Incorrect. Under the AWS Shared Responsibility Model, AWS secures the underlying infrastructure (hardware, network, hypervisor), but customers remain responsible for securing application code, data, IAM policies, and configuration. Serverless reduces some operational tasks, but application-level security must still be implemented by the customer.  
C. Monitoring and logging are not needed.

#### Explications

Incorrect. Observability is still required in serverless architectures: CloudWatch metrics and logs, X-Ray traces, and alarms are used for troubleshooting, performance tuning, and cost control. Omitting monitoring prevents diagnosing failures and optimizing function performance and billing.  
**Bonne réponse**  
D. Management of infrastructure is offloaded to AWS.

#### Explications

Correct. With serverless offerings (for example, AWS Lambda, API Gateway, and managed data services), AWS handles provisioning, patching, capacity management, and automatic scaling of the underlying compute and infrastructure, allowing teams to focus on code, business logic, and configuration.  
Explication générale  
The question tests understanding of what serverless computing changes: it removes the operational burden of managing servers, capacity, and patching so teams can concentrate on application code and configuration. It does not eliminate deployment work, remove the customer's responsibility for application security, or remove the need for monitoring and logging. The best choice reflects the offloading of underlying infrastructure operations to AWS.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 58Correct  
A user is moving a workload from a local data center to an architecture that is distributed between the local data center and the AWS Cloud. Which type of migration is this?  
A. On-premises to cloud native

#### Explications

Describes a full move into a cloud-only, cloud-native model (refactoring to use managed services, containers, or serverless). That does not match the scenario because the workload remains split across the local data center and AWS rather than being migrated entirely to the cloud.  
B. Hybrid to cloud native

#### Explications

Refers to converting an existing hybrid deployment into a fully cloud-native implementation. The question instead describes creating or maintaining a deployment that spans both on‑premises and AWS, so this direction does not apply.  
**Votre réponse est correcte**  
C. On-premises to hybrid

#### Explications

Matches a hybrid migration pattern where on‑premises systems are extended into AWS so components run across both environments. Typical AWS mechanisms for this include private connectivity (AWS Direct Connect or VPN), hybrid services (AWS Outposts, AWS Storage Gateway), and integrated identity/networking, enabling a distributed architecture rather than a full cloud-only relocation.  
D. Cloud native to hybrid

#### Explications

Represents the reverse scenario — moving from a cloud-native, cloud-only environment back to a hybrid setup. The question starts with the workload in the local data center, so this option describes the wrong migration direction.  
Explication générale  
This item assesses migration type recognition. Because the workload will be distributed between the local data center and AWS, the correct classification is a migration that extends on‑premises infrastructure into a hybrid architecture. The incorrect choices describe moves to or from fully cloud-native (cloud-only) environments, which do not match the described distributed deployment.  
Domaine  
Domain 1: Cloud Concepts  
Question 59Correct  
A company wants to use an AWS networking solution that can act as a centralized gateway between multiple VPCs and on-premises networks. Which AWS service or feature will meet this requirement?  
A. Gateway VPC endpoint

#### Explications

Gateway VPC endpoints provide private, routed access from a VPC to specific AWS services (for example, S3 and DynamoDB) by adding entries to route tables or creating interface endpoints. They do not provide VPC-to-VPC or on-premises transit routing and therefore cannot act as a centralized gateway between multiple VPCs and on-prem networks.  
B. AWS Direct Connect

#### Explications

AWS Direct Connect provisions a dedicated private network connection from an on-premises location to AWS, offering consistent low-latency and high-throughput connectivity via virtual interfaces. By itself it is a transport link, not a managed hub for interconnecting multiple VPCs; you must combine it with a Direct Connect Gateway or Transit Gateway to reach many VPCs.  
**Votre réponse est correcte**  
C. AWS Transit Gateway

#### Explications

Managed Transit Gateway provides a hub-and-spoke architecture to interconnect large numbers of VPCs and on-premises networks. It supports VPC attachments, VPN attachments, and integration with Direct Connect Gateway, uses centralized route tables and propagation for scalable routing, and is specifically designed to be a central gateway for multi-VPC and hybrid connectivity.  
D. AWS PrivateLink

#### Explications

AWS PrivateLink (interface endpoints) exposes and consumes specific services privately using ENIs in a VPC so traffic stays on the AWS network. It provides per-service private connectivity (cross-account/service endpoints) and is not a general-purpose routing hub for connecting multiple VPCs and on-premises networks.  
Explication générale  
This question tests understanding of AWS networking patterns for hybrid and multi-VPC architectures. The correct solution is the managed hub service that provides centralized routing, attachments for VPCs, VPNs, and Direct Connect integration, and scalable route table management—making it suitable as a single gateway between multiple VPCs and on-premises networks. The other options are point solutions: gateway endpoints give private access to specific AWS services, Direct Connect is a dedicated transport link (not a hub by itself), and PrivateLink provides per-service private endpoints rather than centralized routing.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 60Correct  
A company wants the ability to automatically acquire resources as needed and release the resources when they are no longer needed. Which cloud concept describes this functionality?  
A. Availability

#### Explications

Describes system uptime and accessibility achieved through redundancy, failover, and geographically distributed deployments (for example using multiple Availability Zones or Regions, load balancers, and health checks). That concept focuses on keeping services reachable during failures rather than automatically provisioning or releasing capacity in response to demand.  
**Votre réponse est correcte**  
B. Elasticity

#### Explications

Refers to automatically adjusting compute and other resources up and down to match workload demand. In AWS this is implemented by features and services such as EC2 Auto Scaling groups, Application Auto Scaling, Amazon ECS/EKS service autoscaling, and serverless platforms that scale automatically. This behavior optimizes cost and performance by provisioning capacity only when needed and removing it when it is no longer required.  
C. Durability

#### Explications

Concerns the long-term persistence and protection of data (examples: Amazon S3’s eleven‑nines durability, EBS snapshots, and database backups). It addresses loss prevention and data integrity, not dynamic provisioning or deprovisioning of runtime resources.  
D. Reliability

#### Explications

Relates to consistent operation and fault tolerance achieved through design patterns, monitoring, and resilience (for example distributed architecture, retries, and multi-AZ deployments). While it helps systems perform reliably, it does not describe the automatic acquire/release lifecycle of resources driven by demand.  
Explication générale  
The question tests the cloud concept of automatic, demand-driven provisioning and deprovisioning of resources. The correct choice describes the ability to scale resources in real time (using AWS features like Auto Scaling, Application Auto Scaling, and serverless scaling) to match workload changes, reducing cost and maintaining performance. The other choices describe related but different concerns—service uptime and redundancy, data persistence, consistent operation, or manual processes—which do not capture the automatic scale-in/scale-out behavior.  
Domaine  
Domain 1: Cloud Concepts  
Question 61Correct  
Which of the following are benefits of using the AWS Cloud? (Choose two)  
**Votre sélection est correcte**  
A. On-demand self-service provisioning

#### Explications

AWS enables provisioning and configuration of compute, storage, networking, and other resources via APIs, the AWS Management Console, CLI, SDKs, and infrastructure-as-code tools (CloudFormation, CDK) without requiring AWS personnel. This supports automation, rapid deployment, and integration with CI/CD pipelines.  
B. Fixed capacity resources

#### Explications

This is incorrect. AWS resources are designed to be elastic and scalable (Auto Scaling, serverless services like AWS Lambda, managed databases) so capacity can grow or shrink with demand; fixed-capacity is characteristic of traditional on-premises deployments.  
**Votre sélection est correcte**  
C. Pay-as-you-go pricing model

#### Explications

AWS primarily uses a consumption-based billing model where charges are metered (compute by second/minute, storage by GB-month, API calls, data transfer, etc.), allowing customers to avoid large upfront capital expense and pay only for what they use. Cost-management tools (AWS Cost Explorer, Budgets) and optional savings plans/reservations further optimize spend.  
D. Limited geographic availability

#### Explications

This is incorrect. AWS operates a global infrastructure composed of Regions, Availability Zones, and Edge Locations that provide broad geographic coverage, redundancy, and options for data locality and low-latency access.  
E. Proprietary hardware only

#### Explications

This is incorrect. Customers consume AWS managed services and documented instance types rather than being limited to "proprietary hardware only." AWS abstracts the underlying hardware details; many services run on standard or third-party hardware while AWS manages the operational aspects.  
Explication générale  
The question assesses fundamental cloud value propositions: rapid, self-directed provisioning and consumption-based pricing are core benefits because they deliver speed, operational agility, and cost efficiency. The other choices describe attributes of traditional or incorrect deployment models (fixed capacity, limited geography, hardware-focused) and therefore are not valid benefits of using AWS.  
Domaine  
Domain 1: Cloud Concepts  
Question 62Correct  
Which benefit of cloud computing gives a company the ability to deploy applications to users all over the world through a network of AWS Regions, Availability Zones, and edge locations?  
A. Economy of scale

#### Explications

Refers to cost advantages from large-scale operations—AWS spreads fixed costs across many customers, enabling lower per-unit pricing and volume-driven discounts. This explains pricing benefits, not the capability to deploy applications worldwide via Regions, Availability Zones, and edge locations.  
**Votre réponse est correcte**  
B. Global reach

#### Explications

AWS’s global infrastructure (multiple Regions, Availability Zones, and edge locations used by services like Amazon CloudFront and AWS Global Accelerator) is what enables delivering applications to users around the world with reduced latency. This is the benefit that describes geographic distribution and global delivery of workloads.  
C. Agility

#### Explications

Describes the ability to rapidly provision, iterate, and release resources and applications (faster time-to-market and development velocity). While it improves speed and responsiveness, it does not specifically describe deploying applications across a worldwide network of AWS locations.  
D. High availability

#### Explications

Focuses on designing systems to minimize downtime and tolerate failures (using multiple Availability Zones, failover, and redundancy). This addresses resiliency and uptime rather than the global distribution of application endpoints to users.  
Explication générale  
The question targets the cloud benefit that explains AWS’s ability to place application resources close to users. ‘Global reach’ corresponds to AWS’s worldwide footprint (Regions, AZs, edge locations/CloudFront, Global Accelerator) that enables low-latency, global delivery. The other choices describe valid cloud benefits—cost savings (economy of scale), rapid provisioning (agility), and resiliency (high availability)—but do not specifically refer to geographic distribution for global user access.  
Domaine  
Domain 1: Cloud Concepts  
Question 63Correct  
A company wants to use machine learning capabilities to analyze log data from its Amazon EC2 instances and efficiently conduct security investigations. Which AWS service will meet these requirements?  
A. Amazon Inspector

#### Explications

Not appropriate: this service performs automated vulnerability and configuration assessments of EC2 instances and container images (finding software vulnerabilities, deviating configurations and network reachability issues). It does not ingest and analyze runtime logs with ML or provide graph-based investigation visualizations for security incidents.  
B. Amazon QuickSight

#### Explications

Not appropriate: this is a business intelligence and dashboarding service for visualization and ad-hoc analytics. It does not include built-in security-focused log ingestion, behavioral analytics, or ML-driven investigation workflows required for security incident analysis.  
**Votre réponse est correcte**  
C. Amazon Detective

#### Explications

Correct: this managed service aggregates data such as CloudTrail, VPC Flow Logs, DNS logs and GuardDuty findings, constructs a behavior graph, and applies statistical analysis and ML to reveal relationships and anomalous patterns. It provides interactive visualizations and guided workflows to accelerate root-cause analysis of EC2- and account-level security incidents.  
D. Amazon GuardDuty

#### Explications

Partially related but not sufficient: this service continuously analyzes telemetry (CloudTrail, VPC Flow Logs, DNS) with ML to generate security findings (threat detection and alerts). It focuses on detection and produces findings rather than performing the deeper graph-based forensic analysis and visualization used for investigations.  
Explication générale  
The question distinguishes threat detection, vulnerability assessment, BI, and investigative capabilities. The best fit is the service that aggregates logs, builds a behavior graph, and uses ML and visualizations to support forensic investigations. Detection services and vulnerability scanners surface alerts or vulnerabilities, and BI tools produce dashboards, but they do not provide the integrated, ML-assisted investigation and relationship visualizations offered by the correct service.  
Domaine  
Domain 2: Security and Compliance  
Question 64Correct  
A company plans to deploy containers on AWS. The company wants full control of the compute resources that host the containers. Which AWS service will meet these requirements?  
A. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Amazon EKS is a managed Kubernetes control plane. While you can attach self-managed EC2 worker nodes to an EKS cluster and thereby gain full control over those instances, EKS itself does not inherently provide direct control of the compute hosts — it primarily manages orchestration and the control plane. For a requirement that explicitly asks for direct control of the compute resources, selecting the underlying compute (EC2) is the clearer answer.  
B. AWS Fargate

#### Explications

AWS Fargate is a serverless container runtime that abstracts the underlying servers and virtual machines. It intentionally removes access to and management of host instances (no SSH, no AMI/instance type choices), so it does not meet a requirement for full control of the compute resources.  
**Votre réponse est correcte**  
C. Amazon EC2

#### Explications

Amazon EC2 provides virtual machines with full administrative control over the operating system, instance type, AMI, networking, storage attachments, and installed runtimes. You can run container engines (Docker, containerd), host orchestration components, and configure the host OS and kernel settings directly — satisfying the requirement for full control over the compute that hosts containers.  
D. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Amazon ECS is a container orchestration service. When used with the EC2 launch type, ECS tasks run on customer-managed EC2 instances and therefore can provide full control over the hosts; however, ECS as a service focuses on orchestration rather than being the compute layer itself. Because the question asks which service meets the requirement for control of the compute resources, the underlying EC2 instances are the direct answer.  
Explication générale  
Cette question évalue la compréhension des différences entre les environnements d'exécution de conteneurs gérés et le contrôle direct des ressources de calcul. Amazon EC2 est la bonne réponse, car il s'agit du service de calcul sous-jacent qui offre un contrôle administratif complet sur les instances hôtes (système d'exploitation, AMI, type d'instance, réseau, stockage), permettant ainsi d'héberger des conteneurs sur des serveurs que vous gérez. Fargate est sans serveur (aucun contrôle sur l'hôte) ; EKS et ECS fournissent l'orchestration et peuvent s'exécuter sur des nœuds de calcul EC2, mais les services d'orchestration seuls ne permettent pas un contrôle direct des ressources de calcul ; ce sont les instances EC2 qui le permettent.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 65Incorrect  
Une entreprise souhaite gérer ses ressources cloud à l'aide de modèles d'infrastructure en tant que code (IaC). Elle doit se conformer aux exigences réglementaires. Quel service AWS doit-elle utiliser pour répondre à ces exigences ?  
**Votre réponse est incorrecte**  
A. Artefact AWS

#### Explications

AWS Artifact est un portail de documents de conformité qui donne accès aux rapports de sécurité et de conformité AWS ainsi qu'aux accords contractuels (par exemple, les rapports SOC, ISO et PCI). Il ne fournit pas d'outils permettant de définir, de provisionner ou d'appliquer des modèles d'infrastructure en tant que code (IaC), ni de restreindre les modèles que les utilisateurs peuvent déployer ; par conséquent, il ne répond pas aux exigences de gouvernance IaC.  
B. Explorateur de ressources AWS

#### Explications

AWS Resource Explorer est un service d'inventaire et de découverte permettant de localiser et de visualiser les ressources à travers les comptes et les régions. Il améliore la visibilité, mais ne fournit pas de mécanismes pour créer, approuver, distribuer ou appliquer des modèles IaC approuvés pour un provisionnement conforme.  
C. Gestionnaire de licences AWS

#### Explications

AWS License Manager centralise la gestion des licences logicielles afin de prévenir leur utilisation abusive et d'en suivre l'usage. Il gère la gouvernance des licences, mais pas la création, l'approbation, la distribution ni l'application des modèles d'infrastructure en tant que code nécessaires à la mise à disposition conforme des ressources.  
**Bonne réponse**  
D. Catalogue de services AWS

#### Explications

Service Catalog permet aux administrateurs de publier et de gérer des « produits » approuvés, implémentés sous forme de modèles CloudFormation, de les organiser en portefeuilles et d'appliquer des contraintes de lancement, des contrôles d'accès basés sur IAM et des restrictions de paramètres. Les portefeuilles peuvent être distribués aux organisations AWS et suivis via la journalisation et les outils AWS Config/Audit, garantissant ainsi que seuls des modèles et des configurations préapprouvés et conformes sont utilisés pour le provisionnement, ce qui renforce la gouvernance basée sur l'infrastructure en tant que code (IaC).  
Explication générale  
L'objectif est de gérer les ressources via l'infrastructure en tant que code (IaC) tout en garantissant la conformité. AWS Service Catalog permet de publier, de gérer les versions, de restreindre et de distribuer les produits CloudFormation approuvés, ainsi que d'appliquer des contraintes et des contrôles d'accès, assurant ainsi la gouvernance des déploiements IaC. Les autres options fournissent des rapports de conformité (Artifact), la découverte des ressources (Resource Explorer) ou le suivi des licences (License Manager), mais n'imposent pas l'utilisation de modèles IaC approuvés pour le provisionnement.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 66Correct  
Quel composant VPC une entreprise peut-elle utiliser pour configurer un pare-feu virtuel au niveau de l'instance Amazon EC2 ?  
A. ACL réseau

#### Explications

Incorrect. Network ACLs are stateless access control lists applied at the subnet boundary; they evaluate traffic per subnet and require explicit rules for both directions, so they cannot provide instance-level, stateful firewalling.  
**Votre réponse est correcte**  
B. Security group

#### Explications

Correct. Security groups act as stateful virtual firewalls that are attached to network interfaces (ENIs) or instances; they control inbound and outbound traffic using allow rules and are evaluated at the instance/ENI level.  
C. Route table

#### Explications

Incorrect. Route tables define how traffic is routed between subnets and to gateways or virtual appliances; they do not perform packet filtering or access control at the instance level.  
D. NAT gateway

#### Explications

Incorrect. NAT gateways perform network address translation to allow instances in private subnets to access the internet; they provide connectivity (NAT), not firewalling or instance-level access control.  
Explication générale  
The question tests knowledge of AWS networking security controls. Security groups are the instance/ENI-level, stateful virtual firewalls used to permit or restrict traffic to EC2 instances. By contrast, Network ACLs are stateless and operate at the subnet level, while route tables and NAT gateways handle routing and NAT functionality, not firewalling.  
Domaine  
Domain 2: Security and Compliance  
Question 67Correct  
Which of the following best describes the benefit of using AWS Cloud for deploying applications?  
A. It guarantees unlimited scalability without any additional cost.

#### Explications

Incorrect. While AWS provides scalable services, scalability is not automatically 'unlimited' or free. Resources must be provisioned or configured to scale (for example using Auto Scaling or serverless services), and increased usage incurs additional charges under the pay‑as‑you‑go pricing model.  
**Votre réponse est correcte**  
B. It provides on-demand resources that can be scaled up or down based on application needs, reducing costs and increasing flexibility.

#### Explications

Correct. AWS enables elastic, on‑demand provisioning of compute, storage, and managed services so capacity can be adjusted to match demand. Features such as Amazon EC2 Auto Scaling, AWS Lambda (serverless), Elastic Load Balancing and scalable storage services allow architectures to scale and avoid overprovisioning; combined with pay‑as‑you‑go pricing and cost‑optimization options, this reduces capital expenses and increases deployment flexibility.  
C. It eliminates the need for any security measures in the cloud environment.

#### Explications

Incorrect. Security in AWS follows the shared responsibility model: AWS is responsible for the security of the cloud (physical infrastructure, hypervisor, regions) while customers are responsible for security in the cloud (OS, applications, data, IAM, network configuration, encryption). AWS provides security tools (IAM, KMS, Security Hub, etc.), but customers must implement and manage appropriate controls.  
D. It requires a fixed infrastructure setup before deployment, limiting flexibility.

#### Explications

Incorrect. AWS prend en charge une infrastructure dynamique, et non fixe. L'infrastructure peut être provisionnée et modifiée à la demande via la console, les API ou les outils d'infrastructure en tant que code (AWS CloudFormation, AWS CDK). Les modèles cloud permettent des déploiements flexibles et reproductibles, ainsi qu'une mise à l'échelle horizontale et verticale, sans nécessiter une configuration prédéfinie.  
Explication générale  
Cette question évalue la compréhension des principaux avantages du cloud : l’élasticité et la mise à disposition de ressources à la demande. La meilleure réponse décrit la capacité d’AWS à adapter dynamiquement les ressources et à aligner les coûts sur l’utilisation (réduisant ainsi les dépenses d’investissement). Les réponses incorrectes exagèrent les garanties (gratuit/illimité), ignorent la responsabilité partagée en matière de sécurité ou présentent à tort le cloud comme nécessitant une infrastructure fixe.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 68Incorrect  
Où les utilisateurs peuvent-ils trouver des exemples de conception de solutions AWS Cloud ?  
**Votre réponse est incorrecte**  
A. Place de marché AWS

#### Explications

AWS Marketplace est un catalogue de logiciels tiers, d'AMI et de produits SaaS/EC2 que vous pouvez acheter et déployer. Il se concentre sur les listes de logiciels et les modèles de licence/abonnement, et non sur la publication de schémas d'architecture de référence ou de recommandations de conception.  
B. Catalogue de services AWS

#### Explications

AWS Service Catalog permet aux organisations de créer et de gérer un portefeuille de produits informatiques approuvés et sélectionnés avec soin, à des fins de gouvernance interne et de déploiements standardisés. Il s'agit de contrôler et de provisionner des ressources approuvées, et non de fournir des architectures de référence publiques ou des exemples de conception.  
**Bonne réponse**  
C. Centre d'architecture AWS

#### Explications

Le Centre d'architecture AWS est le référentiel officiel des architectures de référence, des modèles de conception, des guides d'implémentation, des livres blancs et des exemples de diagrammes AWS. Il regroupe les recommandations Well-Architected, les implémentations de référence et les fiches de solutions illustrant la conception de systèmes sécurisés, fiables et économiques sur AWS ; c'est pourquoi il constitue la source idéale pour des exemples de conception de solutions.  
D. Conseiller de confiance AWS

#### Explications

AWS Trusted Advisor effectue des vérifications automatisées et fournit des recommandations en temps réel concernant l'optimisation des coûts, les performances, la sécurité, la tolérance aux pannes et les limites de service de votre compte AWS. Il propose des conseils opérationnels et des suggestions de correction plutôt que des exemples d'architecture prédéfinis.  
Explication générale  
Le Centre d'architecture AWS est la ressource centrale d'AWS qui publie des architectures de référence, des modèles de conception et des guides de mise en œuvre pour le développement sur AWS. D'autres options répondent à des besoins différents : AWS Marketplace permet d'acquérir des logiciels tiers, Service Catalog assure la gouvernance interne des catalogues et le provisionnement standardisé, et Trusted Advisor fournit des recommandations opérationnelles ; aucune de ces solutions ne constitue la source principale de modèles d'architecture de référence.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 69Correct  
Une entreprise souhaite suivre les coûts et l'utilisation mensuels de toutes ses instances Amazon EC2 dans un environnement AWS spécifique. Quel service ou outil AWS répond à ces besoins ?  
A. Détection des anomalies de coûts AWS

#### Explications

Incorrect — This capability is focused on detecting unusual or unexpected spend patterns using statistical/ML-based alerts. It surfaces anomalies and can trigger notifications, but it does not provide ongoing monthly cost tracking, budget thresholds, or filtering by service/tags for regular reporting.  
**Votre réponse est correcte**  
B. AWS Budgets

#### Explications

Correct — Provides the ability to create monthly cost and usage budgets, filter by service, linked accounts, or tags, compare actual vs forecasted amounts, and send notifications (or trigger automated actions) when thresholds or forecasts are breached. This makes it suitable for tracking EC2 monthly cost and usage across an environment.  
C. AWS Compute Optimizer

#### Explications

Incorrect — Offers resource-rightsizing recommendations (based on utilization metrics) for EC2, Lambda, EBS, and Auto Scaling groups to optimize performance and cost. It does not serve as a cost- or usage-reporting tool for monthly tracking.  
D. AWS Trusted Advisor

#### Explications

Incorrect — Delivers best-practice checks and optimization recommendations across cost, security, fault tolerance, and performance (some cost-related checks identify underutilized resources). It is advisory in nature and not designed for continuous monthly cost/usage tracking or budgeting workflows.  
Explication générale  
The requirement is ongoing monthly tracking and alerting for EC2 cost and usage. The correct choice provides budget creation, filtering by service/tags/accounts, actual vs forecast comparisons, and threshold alerts or actions. Other options (anomaly detection, compute optimizer, Trusted Advisor) address spikes, right-sizing recommendations, or best-practice checks respectively, but do not provide the primary budgeting and regular cost-tracking features needed.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 70Incorrect  
Which AWS service makes it easier to monitor and troubleshoot application logs and cloud resources?  
A. Amazon EC2

#### Explications

Provides virtual servers (compute instances) and exposes instance-level metrics, but does not offer centralized log aggregation, interactive log queries, dashboards, or built-in alerting for application and multi-resource troubleshooting. EC2 relies on other services to collect, store, analyze, and visualize operational telemetry.  
B. AWS Identity and Access Management (IAM)

#### Explications

A service for managing identities, roles, and permissions. It controls who can access monitoring and logging services but does not collect, store, or analyze application logs or operational metrics.  
**Bonne réponse**  
C. Amazon CloudWatch

#### Explications

A fully managed monitoring service that centralizes operational telemetry: it ingests metrics and logs, provides CloudWatch Logs for storage, Logs Insights for interactive log queries, Alarms for threshold-based notifications, Dashboards for visualization, and agents/integrations to collect custom metrics—making it the appropriate tool for monitoring and troubleshooting applications and AWS resources.  
**Votre réponse est incorrecte**  
D. AWS CloudTrail

#### Explications

Captures API calls and service activity for auditing, governance, and compliance. While it can deliver events to storage or to logs for later analysis, it is focused on audit trails of control-plane activity rather than real-time application metrics, interactive log analytics, or operational alerting.  
Explication générale  
This item assesses knowledge of AWS monitoring and logging services. The correct choice is the managed monitoring service that centralizes metrics, logs, dashboards, alarms, and query tools for operational troubleshooting. The distractors are other valid AWS services with different primary purposes: compute (EC2), identity and access management (IAM), and audit/event recording (CloudTrail), none of which provide the centralized, real-time monitoring and log-analysis capabilities required here.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 71Correct  
A company is hosting an application in the AWS Cloud. The company wants to verify that underlying AWS services and general AWS infrastructure are operating normally. Which combination of AWS services can the company use to gather the required information? (Choose two.)  
**Votre sélection est correcte**  
A. AWS Personal Health Dashboard

#### Explications

AWS Personal Health Dashboard (PHD) provides account-specific health information and alerts for AWS services and resources that directly affect your account. It surfaces events such as service disruptions, scheduled maintenance, and account-targeted issues, and can be consumed programmatically via the AWS Health API or routed to EventBridge/CloudWatch Events and SNS for automated notification and remediation workflows.  
B. AWS Systems Manager

#### Explications

AWS Systems Manager is an operations management service for your AWS and on‑premises resources (Run Command, Session Manager, Automation, Patch Manager, OpsCenter), used to automate tasks and troubleshoot instances. It does not report the health or operational status of AWS-managed services or the overall AWS infrastructure.  
C. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor analyzes your AWS environment and provides best-practice recommendations across cost optimization, security, fault tolerance, performance, and service limits. While useful for optimizing and preventing issues, it is not a real‑time service status or infrastructure health dashboard and does not report AWS service outages.  
**Votre sélection est correcte**  
D. AWS Service Health Dashboard

#### Explications

AWS Service Health Dashboard is the public, region-aware dashboard that shows the current operational status and historical incidents for AWS services across regions. It provides real‑time information about service outages and regional impairments affecting the AWS infrastructure, which complements the account-specific alerts from the Personal Health Dashboard.  
E. AWS Service Catalog

#### Explications

AWS Service Catalog lets organizations create and manage catalogs of approved IT services and provisioning templates for governance and self-service. It is focused on controlled provisioning and compliance, not on reporting AWS service health or infrastructure status.  
Explication générale  
Use the AWS Personal Health Dashboard for account-level, targeted events and recommended remediation, and the AWS Service Health Dashboard for the broader, public regional status of AWS services. The other options—Systems Manager, Trusted Advisor, and Service Catalog—provide resource management, best-practice recommendations, and provisioning/governance capabilities respectively, but they do not provide the AWS service or infrastructure health views required by this question.  
Domaine  
Domain 1: Cloud Concepts  
Question 72Correct  
Which AWS service or tool can be used to capture information about inbound and outbound traffic in an Amazon VPC?  
**Votre réponse est correcte**  
A. VPC Flow Logs

#### Explications

Records metadata about IP traffic (source/destination IPs, ports, protocol, packets, bytes) for ENIs, subnets, or entire VPCs and exports those records to destinations such as Amazon CloudWatch Logs or Amazon S3. This enables network monitoring, security analysis, and troubleshooting of inbound and outbound VPC traffic.  
B. Amazon Inspector

#### Explications

Amazon Inspector is an automated security assessment service that finds vulnerabilities and deviations from best practices in EC2 instances and container images. It evaluates host and application security posture but does not capture or log per-connection VPC network flows.  
C. VPC endpoint services

#### Explications

VPC endpoint services (AWS PrivateLink) provide private connectivity between VPCs and services using Network Load Balancers; they enable private routing but do not themselves collect or export network flow data for traffic analysis.  
D. NAT gateway

#### Explications

A NAT gateway provides managed network address translation so private instances can access the internet. It performs packet forwarding but does not offer traffic-capture or flow-logging functionality; VPC Flow Logs are used to observe that traffic.  
Explication générale  
This item tests knowledge of VPC monitoring tools. The correct choice is the service that captures VPC IP traffic metadata and exports logs for analysis (delivered to CloudWatch Logs or S3). The distractors provide security assessment, connectivity, or NAT functionality and do not provide VPC-wide traffic capture or flow logging.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 73Correct  
A company that is planning to migrate to the AWS Cloud is based in an isolated area that has limited internet connectivity. The company needs to perform local data processing on premises. The company needs a solution that can operate without a stable internet connection. Which AWS service will meet these requirements?  
A. Amazon S3

#### Explications

This option describes AWS object storage in the cloud, which depends on network connectivity to read and write objects and does not provide bundled local compute for processing data offline. Because the scenario requires independent on‑premises processing without stable internet, this cloud-only storage option is not suitable.  
**Votre réponse est correcte**  
B. AWS Snowball Edge

#### Explications

A Snow Family edge device provides local, ruggedized storage plus compute capabilities that can run workloads at the edge (supports running EC2-compatible instances and Lambda functions). It is designed to operate in disconnected or intermittently connected environments, buffer and process data locally, and then transfer data to AWS when connectivity is available — matching the requirement for local processing without stable internet.  
C. AWS Storage Gateway

#### Explications

This hybrid storage appliance offers local caching and integration with AWS storage but relies on connectivity to synchronize data with cloud storage and to manage lifecycle operations. It isn’t intended for long‑term operation in fully isolated environments where no reliable internet exists.  
D. AWS Backup

#### Explications

This is a managed service for centralizing backups of AWS resources and orchestrating backup policies. It requires access to AWS control plane and storage and does not provide on‑device local compute for offline data processing.  
Explication générale  
The question tests knowledge of AWS edge and data transfer solutions for disconnected environments. The Snow Family edge device is the correct choice because it combines on‑device compute and durable storage to run workloads locally and defer transfers to AWS until network connectivity is available. The other options either are cloud‑only services (requiring stable connectivity) or hybrid solutions that depend on syncing to AWS and are not designed for sustained offline processing.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 74Incorrect  
A company wants an AWS service that can automate software deployment in Amazon EC2 instances and on-premises instances. Which AWS service will meet this requirement?  
A. AWS CodeCommit

#### Explications

Incorrect. AWS CodeCommit is a fully managed source control service for hosting private Git repositories. It stores and manages source code and can trigger CI/CD pipelines, but it does not perform or orchestrate deployments to compute instances itself.  
B. AWS CodeBuild

#### Explications

Incorrect. AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces build artifacts. It is not a deployment service and does not push application revisions to EC2 or on‑premises servers.  
**Bonne réponse**  
C. AWS CodeDeploy

#### Explications

Correct. AWS CodeDeploy is a managed deployment service that automates application releases to multiple compute targets, including Amazon EC2 instances and on‑premises servers. It supports in‑place and blue/green deployment strategies, uses deployment groups and lifecycle event hooks, integrates with CodePipeline, and requires an agent or integration on target instances to coordinate deployments and enable automated rollbacks.  
**Votre réponse est incorrecte**  
D. AWS CodePipeline

#### Explications

Incorrect. AWS CodePipeline is a continuous delivery orchestration service that models and automates pipeline stages (source, build, test, deploy). While it coordinates deployments and can invoke deployment actions, it delegates the actual deployment work to services such as CodeDeploy or ECS rather than directly deploying to instances.  
Explication générale  
The question targets the service responsible for automating software deployment to both EC2 and on‑premises instances. The correct solution is the managed deployment service that directly handles pushing application revisions, coordinating lifecycle events, and supporting deployment strategies across those targets. The other options provide source control (CodeCommit), build/CI (CodeBuild), or pipeline orchestration (CodePipeline), but none directly perform automated deployments to EC2 and on‑premises servers in the way the deployment service does.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 75Correct  
Which AWS resource can help a company reduce its costs in exchange for a usage commitment when using Amazon EC2 instances?  
**Votre réponse est correcte**  
A. Compute Savings Plans

#### Explications

Provides lower pricing in exchange for a commitment to a consistent amount of compute usage (measured as $/hour) over 1‑ or 3‑year terms. This commitment applies across EC2 instance families, sizes, operating systems, and regions, delivering greater per‑hour discounts than On‑Demand while preserving more flexibility than some Reserved Instance options.  
B. Auto Scaling group

#### Explications

Auto Scaling automatically adjusts the number of running EC2 instances to match demand, improving availability and cost efficiency through right‑sizing, but it does not provide discounted pricing tied to a long‑term usage commitment.  
C. On-Demand Instance

#### Explications

On‑Demand instances operate on a pay‑as‑you‑go model with no long‑term commitment; they maximize flexibility but do not offer the reduced hourly rates that come from committing to sustained usage.  
D. EC2 instance store

#### Explications

EC2 instance store is ephemeral, physically attached block storage that affects data persistence and performance for an instance; it is unrelated to EC2 pricing models or discounts obtained via usage commitments.  
Explication générale  
This item tests AWS pricing knowledge: Savings Plans at the compute level are the mechanism that exchange a 1‑ or 3‑year commitment to a consistent compute spend for lower rates across EC2 instance families and regions. The other choices describe scaling behavior (Auto Scaling), pay‑as‑you‑go usage (On‑Demand), or a storage feature (instance store), none of which provide cost reductions based on a committed usage contract.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 76Correct  
A company plans to migrate its application to AWS and run the application on Amazon EC2 instances. The application will have continuous usage for 1 year. Which EC2 instance purchasing option will meet these requirements MOST cost-effectively?  
**Votre réponse est correcte**  
A. Reserved Instances

#### Explications

A one-year term reservation with EC2 provides a billing discount in exchange for a commitment. For workloads that run continuously and predictably for the term, this purchasing option lowers cost compared with pay-as-you-go pricing by applying a discounted hourly rate for the reserved capacity. It is the appropriate choice for a steady, uninterrupted application running for one year.  
B. Spot Instances

#### Explications

This option offers EC2 capacity at steep discounts but instances can be terminated by AWS when capacity is reclaimed (with short notice). Because it is interruptible and intended for fault-tolerant or flexible jobs (batch, analytics), it is not suitable for an application that requires continuous, uninterrupted operation for a year.  
C. On-Demand Instances

#### Explications

On‑demand pricing charges by usage with no long-term commitment, giving maximum flexibility. For a predictable, continuous 1‑year workload this results in higher total cost than committing to a term-based discounted option, so it is not the most cost‑effective choice here.  
D. Dedicated Hosts

#### Explications

These provide a physical server dedicated to a single customer for compliance or licensing needs and expose sockets/cores for software licensing. They incur higher costs and are intended for specific regulatory or licensing scenarios, not for general cost optimization of a continuous standard workload.  
Explication générale  
For a predictable, continuously running application over a one‑year period, committing to a reserved EC2 purchasing option yields the best cost savings versus pay‑as‑you‑go or interruptible options. The distractors are unsuitable because spot instances are interruptible, on‑demand is more expensive for steady long‑term usage, and dedicated hosts are costlier and used for compliance/licensing rather than general cost reduction.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 77Correct  
Which AWS network services or features allow CIDR block notation when providing an IP address range? (Choose two.)  
**Votre sélection est correcte**  
A. Security groups

#### Explications

Instance-level, stateful firewall rules allow specifying IP address ranges using CIDR notation for inbound and outbound rules. These rules are evaluated with connection state awareness and can also reference other security groups, but CIDR blocks are supported when you need to allow or restrict specific IP ranges.  
B. Amazon Machine Image (AMI)

#### Explications

An Amazon Machine Image is a template used to launch EC2 instances (OS, configuration, and software). It does not define network access control rules or accept CIDR-formatted IP ranges.  
**Votre sélection est correcte**  
C. Network access control list (network ACL)

#### Explications

Subnet-level, stateless access control lists use numbered allow/deny entries that accept CIDR blocks for source and destination addresses. Because they are stateless, return traffic requires explicit rules, and CIDR notation is used to define the IP ranges those rules apply to.  
D. AWS Budgets

#### Explications

AWS Budgets is a cost-management service for tracking and alerting on AWS spending. It has no functionality for defining network traffic rules or IP address ranges.  
E. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS provides block storage volumes attached to EC2 instances; it is a storage service and does not involve IP addressing or CIDR-based network rule definitions.  
Explication générale  
CIDR notation is used when defining IP address ranges for network control mechanisms. The two network constructs that accept CIDR blocks are instance-level security group rules (stateful) and subnet-level network ACLs (stateless). The other options (AMI, Budgets, EBS) are unrelated to network ACLs or firewall rule definitions and therefore do not use CIDR notation for access control.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 78Correct  
A company wants to create a globally accessible ecommerce platform for its customers. The company wants to use a highly available and scalable DNS web service to connect users to the platform. Which AWS service will meet these requirements?  
A. Amazon EC2

#### Explications

Amazon EC2 is an Infrastructure as a Service (IaaS) that provides resizable compute capacity (virtual servers). It is not a managed DNS solution; while you could run your own DNS software on EC2, EC2 does not provide global DNS routing, health checks, or managed DNS features required for a highly available, scalable public DNS service.  
B. Amazon VPC

#### Explications

Amazon VPC provides isolated virtual networking and includes an Amazon-provided DNS resolver for name resolution inside a VPC. That DNS is private to the VPC (or limited to linked resources) and does not serve as a global, public DNS web service with routing policies, global anycast endpoints, or health checks for internet-facing applications.  
**Votre réponse est correcte**  
C. Amazon Route 53

#### Explications

Route 53 is a managed, highly available, global DNS service that uses an anycast network to resolve domain names from edge locations worldwide. It supports health checks and DNS failover, multiple routing policies (simple, weighted, latency-based, geolocation, failover, multi-value), domain registration, and tight integration with services like Elastic Load Balancing and CloudFront—features that enable scalable, resilient global traffic routing for an ecommerce platform.  
D. Amazon RDS

#### Explications

Amazon RDS is a managed relational database service for running databases (MySQL, PostgreSQL, Aurora, etc.). It provides managed storage, backups, and maintenance for databases but does not perform DNS resolution or global traffic routing for end users.  
Explication générale  
The question tests knowledge of AWS services used for global DNS and traffic routing. A managed DNS web service with global reach, routing policies, and health checks is required; Route 53 provides these capabilities via an anycast network and built-in routing/health features. EC2, VPC, and RDS are core compute, networking, and database services respectively and do not provide the managed, global DNS features needed for this use case.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 79Correct  
Which Amazon S3 feature or storage class uses the AWS backbone network and edge locations to reduce latencies from the end user to Amazon S3?  
A. S3 Cross-Region Replication

#### Explications

Cross-Region Replication asynchronously copies objects between AWS regions for durability, compliance, or locality of data. It does not route end-user traffic through edge locations or the AWS global network to reduce upload/download latency for clients.  
**Votre réponse est correcte**  
B. S3 Transfer Acceleration

#### Explications

This capability directs clients to the nearest Amazon edge location, accepts transfers there, and forwards data over the AWS global backbone to the destination S3 bucket. The result is lower round-trip time and higher throughput for geographically distant users compared with sending traffic directly to the bucket's regional endpoint.  
C. S3 Event Notifications

#### Explications

Event notifications are a mechanism to publish object-level events to targets such as Lambda, SQS, or SNS for workflow automation. They do not change how client traffic is routed to S3 or provide any latency-reduction network path.  
D. S3 Standard-Infrequent Access (S3 Standard-IA)

#### Explications

The Standard-Infrequent Access storage class optimizes cost for data that is accessed less frequently and has different retrieval charges and minimum retention. It is a storage tier and does not provide network acceleration or use edge locations to speed client transfers.  
Explication générale  
The question tests knowledge of S3 networking features. The correct choice describes S3's transfer acceleration-style mechanism that uses nearest edge locations and the AWS backbone to speed transfers between end users and S3. The other options describe replication, event-driven operations, or a storage tier—none of which alter client network routing via edge locations to reduce latency.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 80Incorrect  
A company is building an application that will receive millions of database queries each second. The company needs the data store for the application to scale to meet these needs. Which AWS service will meet this requirement?  
**Bonne réponse**  
A. Amazon DynamoDB

#### Explications

DynamoDB is a fully managed, serverless key‑value and document database that is designed for massive, predictable throughput. It uses automatic partitioning and capacity modes (on‑demand and provisioned with auto scaling) to scale horizontally across many servers, supports single‑digit millisecond latency, and can be augmented with DAX for in‑memory read acceleration and Global Tables for multi‑region workloads — making it appropriate for workloads with millions of requests per second.  
B. AWS Cloud9

#### Explications

AWS Cloud9 is a cloud‑based integrated development environment (IDE) for writing, running, and debugging code. It is not a database or data storage service and therefore cannot serve as the scalable data store required to handle millions of queries per second.  
**Votre réponse est incorrecte**  
C. Amazon ElastiCache for Memcached

#### Explications

ElastiCache for Memcached is an in‑memory caching service that improves read performance by storing transient copies of data. It is not a durable primary datastore: data is ephemeral, there is no persistence or advanced querying like a database, and operational considerations (evictions, client sharding) make it unsuitable as the primary store for the described high‑scale transactional workload.  
D. Amazon Neptune

#### Explications

Amazon Neptune is a managed graph database optimized for highly connected data and graph traversals (Gremlin/SPARQL). Its architecture targets relationship queries and graph workloads rather than ultra‑high throughput key‑value/document access patterns, so it is not the best fit for a service that must serve millions of simple database queries per second.  
Explication générale  
The question tests selecting the appropriate AWS data service for extreme request throughput. DynamoDB is architected for horizontal scaling, automatic partitioning, and on‑demand or provisioned capacity to support millions of requests per second, which directly meets the requirement. The other choices are not suitable: Cloud9 is an IDE (not a datastore), ElastiCache is a transient cache (not a durable primary database), and Neptune is a graph DB optimized for connected data rather than massive key‑value/document throughput.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 81Correct  
A company wants to migrate critical on-premises production systems to Amazon EC2 instances. The production instances will be used for at least 3 years. The company wants a pricing option that will minimize cost. Which solution will meet these requirements?  
A. On-Demand Instances

#### Explications

Pay-as-you-go compute without a multi-year commitment results in higher effective cost for steady-state, long-term production workloads; it's designed for flexibility rather than minimizing multi-year spend.  
**Votre réponse est correcte**  
B. Reserved Instances

#### Explications

Committing to a 1‑ or 3‑year reserved pricing agreement provides substantial hourly‑rate discounts (standard RIs can deliver the largest savings versus on‑demand, depending on term and payment option). Features include scope choices (regional vs zonal), payment options (All Upfront, Partial Upfront, No Upfront), and instance‑size flexibility for certain RI types — making reserved pricing the cost‑effective choice for critical EC2 servers expected to run for multiple years.  
C. Spot Instances

#### Explications

Uses spare EC2 capacity at steep discounts but instances are interruptible and can be reclaimed by AWS with little notice; suitable for fault‑tolerant or batch jobs but inappropriate for non‑interruptible, critical production systems.  
D. AWS Free Tier

#### Explications

A limited introductory offering for new accounts (commonly 12 months) with small usage caps; not intended for long‑term, production‑scale deployments spanning multiple years.  
Explication générale  
For multi‑year, critical EC2 workloads the lowest predictable cost comes from committing to a multi‑year reserved pricing option, which exchanges a time commitment for significant discounts and predictable billing. Alternatives — on‑demand (higher unit cost), spot (interruptible), and the free tier (temporary/limited) — do not provide the same combination of price certainty and suitability for sustained, critical production use.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 82Correct  
Which cloud concept is demonstrated by using AWS Compute Optimizer?  
A. Security validation

#### Explications

Security validation is about identifying vulnerabilities, misconfigurations, and compliance issues. AWS services that perform security assessments include Amazon Inspector, AWS Security Hub, and IAM Access Analyzer. AWS Compute Optimizer analyzes resource utilization and cost/performance trade-offs, not security posture, so it does not fulfill security validation.  
**Votre réponse est correcte**  
B. Rightsizing

#### Explications

AWS Compute Optimizer uses machine learning and CloudWatch utilization metrics to analyze resources (EC2 instances, EBS volumes, Lambda functions, and Auto Scaling groups) and recommends optimal instance families/sizes, volume types, or memory settings. These recommendations reduce overprovisioning and improve cost-efficiency and performance — the core activity known as rightsizing.  
C. Elasticity

#### Explications

Elasticity refers to automatically scaling resources in and out in response to demand (for example via EC2 Auto Scaling, Application Auto Scaling, or managed services like AWS Lambda). Compute Optimizer provides sizing recommendations based on historical usage but does not perform automatic scaling, so it does not itself demonstrate elasticity.  
D. Global reach

#### Explications

Global reach refers to AWS’s global infrastructure (Regions, Availability Zones, Edge Locations, and services like Amazon CloudFront) that enables worldwide deployment and low-latency delivery. Compute Optimizer’s purpose is per-resource optimization within an account/region and is unrelated to global infrastructure or geographic distribution.  
Explication générale  
The question tests understanding of cloud optimization concepts. AWS Compute Optimizer analyzes historical utilization data and provides machine-learning-based recommendations to adjust resource sizes and types, which is the definition of rightsizing. It does not perform security assessment, automatic scaling, or provide global infrastructure capabilities — those are handled by other AWS services.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 83Correct  
A company wants to deploy a non-containerized Java-based web application on AWS. The company wants to use a managed service to quickly deploy the application. The company wants the service to automatically provision capacity, load balance, scale, and monitor application health. Which AWS service will meet these requirements?  
A. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Incorrect. Amazon ECS is a container orchestration service that schedules and runs Docker containers on EC2 or with AWS Fargate. The service requires the application to be packaged as containers and does not provide the single-step managed deployment and platform-level provisioning for non-containerized Java web apps described in the scenario.  
B. AWS Lambda

#### Explications

Incorrect. AWS Lambda is an event-driven, serverless compute service for short-lived function executions. While Lambda can expose HTTP endpoints via API Gateway, it is not intended to host traditional, long-running web server processes or to automatically provision EC2-based web server fleets with ELB, Auto Scaling groups, and platform health monitoring as required here.  
C. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Incorrect. Amazon EKS is a managed Kubernetes control plane for running containerized workloads using Kubernetes. It requires containerization and Kubernetes configuration, so it does not meet the requirement for a managed, out-of-the-box deployment of a non-containerized Java web application.  
**Votre réponse est correcte**  
D. AWS Elastic Beanstalk

#### Explications

Correct. Elastic Beanstalk is a platform-as-a-service that automates environment provisioning for supported runtimes (including Java). It provisions and manages EC2 instances, configures Elastic Load Balancing, sets up Auto Scaling, and integrates with Amazon CloudWatch for health monitoring and metrics, enabling quick deployment without managing underlying infrastructure.  
Explication générale  
This item tests selection of a managed deployment service for a non-containerized Java web application. AWS Elastic Beanstalk is the appropriate choice because it automates provisioning of compute resources, configures Elastic Load Balancing and Auto Scaling, and provides health monitoring (CloudWatch) for supported platforms. The other options are container orchestration (ECS, EKS) or serverless function (Lambda) services that do not directly provide the described managed platform for non-containerized web apps.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 84Correct  
A company wants a customized assessment of its current on-premises environment. The company wants to understand its projected running costs in the AWS Cloud. Which AWS service or tool will meet these requirements?  
A. AWS Trusted Advisor

#### Explications

Trusted Advisor runs best-practice checks and provides recommendations for cost optimization, performance, security, fault tolerance, and service limits, but it analyzes resources within AWS accounts. It does not perform an on‑premises inventory or produce migration cost projections for moving workloads to AWS.  
B. Amazon Inspector

#### Explications

Amazon Inspector is a vulnerability and security assessment service for applications and EC2 instances. It identifies security issues and deviations from security best practices, but it does not analyze on‑premises infrastructure or estimate future AWS running costs.  
C. AWS Control Tower

#### Explications

AWS Control Tower automates the setup and governance of multi‑account AWS environments and applies guardrails. It helps establish landing zones and governance, but it does not analyze on‑premises workloads or generate migration cost estimates.  
**Votre réponse est correcte**  
D. Migration Evaluator

#### Explications

Migration Evaluator collects on‑premises inventory and utilization data, analyzes workload characteristics, maps servers to appropriate AWS resource types, and generates detailed total cost of ownership and monthly cost projections plus migration grouping recommendations—making it the appropriate tool for customized on‑premises assessments and AWS cost estimates.  
Explication générale  
Cette question évalue les connaissances relatives aux outils d'évaluation de la migration AWS. Migration Evaluator est conçu pour analyser les données d'inventaire et d'utilisation sur site et générer des projections de coûts et des recommandations de migration basées sur ces données, répondant ainsi directement à l'exigence. Les autres options se concentrent sur les bonnes pratiques AWS (Trusted Advisor), les évaluations de sécurité (Amazon Inspector) ou la gouvernance des comptes et les zones d'atterrissage (Control Tower) et ne permettent donc pas d'effectuer les projections de coûts sur site demandées.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 85Incorrect  
Une entreprise souhaite transformer ses effectifs en attirant et en développant une main-d'œuvre performante et maîtrisant les outils numériques. Elle souhaite recruter un personnel diversifié et inclusif, possédant un juste équilibre de compétences techniques et non techniques. Quelle perspective du cadre d'adoption du cloud AWS (AWS CAF) répond à ces exigences ?  
**Votre réponse est incorrecte**  
A. Affaires

#### Explications

Incorrect. L'approche métier vise à aligner la stratégie cloud sur les objectifs organisationnels, la création de valeur, l'implication des parties prenantes et l'élaboration d'un plan d'affaires. Elle se concentre sur les capacités métier et les indicateurs clés de performance (KPI) plutôt que sur le recrutement, le développement des compétences ou les programmes de diversité au sein des effectifs.  
**Bonne réponse**  
B. Les gens

#### Explications

Exact. La perspective « Personnes » du CAF d’AWS porte explicitement sur la transformation des effectifs : définition des rôles et responsabilités organisationnels, identification des compétences requises, planification des formations et des parcours professionnels, et mise en œuvre des pratiques de gestion culturelle et du changement nécessaires pour attirer, développer et fidéliser un personnel diversifié et à l’aise avec les outils numériques.  
C. Plateforme

#### Explications

Incorrect. L'approche « Plateforme » englobe la pile technologique et l'architecture de la plateforme (infrastructure, environnements d'exécution, services partagés et cibles de migration). Elle concerne la conception technique et les décisions opérationnelles relatives à la plateforme, et non l'attraction des talents ou le développement des compétences.  
D. Opérations

#### Explications

Incorrect. La perspective Opérations se concentre sur les processus opérationnels, la gestion des incidents et des événements, l'exploitation des services, la surveillance et la gouvernance opérationnelle. Bien qu'elle influence le fonctionnement des équipes, elle ne traite pas principalement des objectifs de recrutement, de formation ou de diversité au sein des effectifs.  
Explication générale  
Ce scénario vise la transformation des effectifs (compétences, rôles, formation et diversité), qui relève de la perspective « People » du CAF AWS. Les perspectives « Business », « Plateforme » et « Opérations » traitent respectivement de la stratégie, de l’architecture technique et des processus d’exécution ; elles ne répondent donc pas directement à l’objectif de l’entreprise d’attirer et de développer des effectifs diversifiés et performants.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 86Correct  
Selon le modèle de responsabilité partagée d'AWS, quelle tâche relève de sa responsabilité ?  
A. Activez le chiffrement côté client pour les objets stockés dans Amazon S3.

#### Explications

Incorrect. Le chiffrement côté client exige que le client effectue des opérations de chiffrement et gère les clés de chiffrement (ou la gestion des clés) sur le client avant l'envoi des données à S3. AWS propose des options de chiffrement côté serveur (SSE-S3, SSE-KMS, SSE-C) et AWS KMS pour la gestion des clés, mais le chiffrement côté client est mis en œuvre et contrôlé par le client.  
B. Configurez les politiques de sécurité IAM pour qu'elles respectent le principe du moindre privilège.

#### Explications

Incorrect. Configuring IAM policies and defining permissions is the customer's responsibility. IAM is an AWS service that enables fine-grained access control, but customers must create, apply, and maintain policies that follow the principle of least privilege for their identities and resources.  
C. Patch the guest operating system on an Amazon EC2 instance.

#### Explications

Incorrect. For Amazon EC2 instances the customer is responsible for the guest operating system, including installing updates and security patches. Managed services (for example, RDS or AWS Lambda) shift more of the OS and runtime maintenance to AWS, but for IaaS EC2 the OS is managed by the customer.  
**Votre réponse est correcte**  
D. Apply updates to the Nitro Hypervisor.

#### Explications

Correct. The Nitro Hypervisor and the underlying virtualization/hardware stack are part of AWS’s managed infrastructure. Patching, updating, and securing that hypervisor are AWS responsibilities under the “security of the cloud” portion of the shared responsibility model.  
Explication générale  
This question tests the AWS shared responsibility model: AWS is responsible for the security “of” the cloud (physical hosts, hypervisor, networking, and foundational services) while customers are responsible for security “in” the cloud (data, identity and access management, OS and application patching for IaaS). Option D is correct because Nitro is part of AWS-managed infrastructure; the other options describe customer responsibilities (client-side encryption, IAM policy configuration, and EC2 guest OS patching).  
Domaine  
Domain 2: Security and Compliance  
Question 87Correct  
Using AWS Identity and Access Management (IAM) to grant access only to the resources needed to perform a task is a concept known as:  
A. restricted access.

#### Explications

Incorrect — this choice is a generic phrase meaning limited permissions or controls but is not the formal AWS security principle. In AWS IAM the emphasis is on defining explicit permission policies, roles, and boundaries that precisely grant only required actions on specific resources, rather than a vague notion of ‘restricted’ access.  
B. as-needed access.

#### Explications

Incorrect — this is an informal description that approximates the idea but is not the formal term used in AWS guidance. AWS security best practices describe this concept by specifying exact IAM policies, roles, permission boundaries, and conditions to limit permissions to what is required.  
**Votre réponse est correcte**  
C. least privilege access.

#### Explications

Correct — this refers to the security principle that identities (users, groups, roles) should be granted only the permissions necessary to perform their tasks. In AWS this is implemented with carefully scoped IAM policies, roles, permission boundaries, resource-based policies, and organizational controls (SCPs), which minimize blast radius and reduce the risk of accidental or malicious access.  
D. token access.

#### Explications

Incorrect — this refers to authentication/temporary credentials (for example, tokens issued by AWS STS) used to assume identities or grant temporary access. Tokens address how credentials are delivered and scoped in time, but do not describe the security principle of minimizing granted permissions.  
Explication générale  
This item tests the core IAM security principle of granting identities only the permissions they need to perform their tasks. The correct choice corresponds to that principle which AWS enforces through scoped IAM policies, roles, permission boundaries, and organizational controls. The distractors are either informal wording of the idea or refer to different concepts (for example, temporary credentials), and therefore are not the precise AWS best-practice term.  
Domaine  
Domain 2: Security and Compliance  
Question 88Correct  
Which of the following best describes the primary benefit of deploying applications in the AWS Cloud compared to traditional on-premises infrastructure?  
A. It requires a longer setup time but offers more control over hardware components.

#### Explications

Incorrect. Cloud deployments typically reduce provisioning and setup time through automation and managed services. AWS provides infrastructure and managed platform services so you avoid physical hardware procurement; when you need low-level control you can use EC2, but that does not require longer setup than on‑premises hardware provisioning.  
**Votre réponse est correcte**  
B. It provides scalable resources that can grow or shrink based on demand, reducing upfront investment.

#### Explications

Correct. AWS supports elastic, on‑demand capacity (Auto Scaling, Amazon EC2, AWS Lambda, managed databases, S3) and a pay‑as‑you‑go pricing model, enabling resources to grow or shrink with demand and shifting costs from up‑front capital expenditure to operational expense.  
C. It eliminates the need for any security measures, as AWS handles all security automatically.

#### Explications

Incorrect. Security in AWS follows the shared responsibility model: AWS secures the underlying cloud infrastructure, but customers are responsible for securing guest OSs, applications, data, IAM configuration, and other customer-managed controls. AWS offers security services (IAM, KMS, Shield, etc.) but does not automatically eliminate customer security tasks.  
D. It guarantees compliance with all industry standards without additional effort.

#### Explications

Incorrect. AWS participates in many compliance programs and provides artifacts and tooling (AWS Artifact, AWS Config, CloudTrail), but achieving and demonstrating compliance depends on customer configuration, implemented controls, and how services are used—compliance is not guaranteed simply by using AWS.  
Explication générale  
The primary benefit tested is cloud elasticity and the operational cost model: AWS enables on‑demand scaling and managed services that reduce upfront capital investment and let workloads adapt to demand. The correct choice emphasizes scalability and cost advantages; the distractors incorrectly assert longer setup, absolved security responsibility, or guaranteed compliance—areas governed by the shared responsibility model or by customer configuration.  
Domaine  
Domain 1: Cloud Concepts  
Question 89Correct  
A social media company wants to protect its web application from common web exploits such as SQL injections and cross-site scripting. Which AWS service will meet these requirements?  
A. Amazon Inspector

#### Explications

Amazon Inspector performs automated security assessments of EC2 instances, container images, and some OS-level configurations to identify vulnerabilities and deviations from best practices. It is an assessment and scanning service, not a live request-filtering firewall, so it cannot block SQL injection or XSS attacks at the application edge.  
**Votre réponse est correcte**  
B. AWS WAF

#### Explications

AWS WAF is a web application firewall that evaluates incoming HTTP/S requests against customizable and managed rule sets (including SQL injection and cross-site scripting protections), and can allow, block, or count requests. It integrates with CloudFront, Application Load Balancer, API Gateway, and AppSync to provide inline protection and mitigation for web applications.  
C. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat detection service that analyzes AWS logs (CloudTrail, VPC Flow Logs, DNS) to identify suspicious activity and compromises. It generates findings for investigation and can trigger responses, but it is not designed to inspect and block individual web requests for SQLi/XSS at the application layer.  
D. Amazon CloudWatch

#### Explications

Amazon CloudWatch provides monitoring, metrics, logs, and alarms for AWS resources and applications. It helps observe and alert on operational and security-related metrics, but it does not provide request-level web application filtering or built-in protections against SQL injection or XSS.  
Explication générale  
The question targets knowledge of AWS services that protect web applications from application-layer exploits. AWS WAF is the appropriate choice because it inspects HTTP(S) requests using rules (including managed rules for SQL injection and XSS) and can block malicious traffic inline. The other services listed (Inspector, GuardDuty, CloudWatch) provide vulnerability assessment, threat detection, and monitoring/observability respectively, but do not perform inline web request filtering to prevent SQLi/XSS attacks.  
Domaine  
Domain 2: Security and Compliance  
Question 90Correct  
A company wants a solution that will automatically adjust the number of Amazon EC2 instances that are being used based on the current load. Which AWS offering will meet these requirements?  
A. Dedicated Hosts

#### Explications

Dedicated Hosts give you control over physical server tenancy for licensing and compliance, but they do not include any automated capacity management. They do not scale EC2 instance counts in response to load.  
B. Placement groups

#### Explications

Placement groups influence how instances are placed on the underlying hardware (cluster, spread, partition) to optimize network latency or fault isolation. They do not provide mechanisms to change the number of instances automatically based on demand.  
**Votre réponse est correcte**  
C. Auto Scaling groups

#### Explications

EC2 Auto Scaling (Auto Scaling groups) automatically adjusts the number of instances to meet demand by using scaling policies (target tracking, step scaling, scheduled actions) driven by CloudWatch metrics and health checks, and integrates with load balancers to maintain application availability.  
D. Reserved Instances

#### Explications

Reserved Instances are a billing/commitment construct that provide a discounted hourly rate for a long-term usage commitment. They affect pricing (and in some cases capacity reservations) but do not perform automatic provisioning or scaling of instances.  
Explication générale  
The correct solution is Auto Scaling groups because they are specifically designed to add or remove EC2 instances automatically in response to metrics, schedules, or scaling policies. The other options address physical tenancy, instance placement, or billing discounts and do not manage instance counts dynamically.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 91Correct  
Which AWS service enables users to check for vulnerabilities on Amazon EC2 instances by using predefined assessment templates?  
A. AWS WAF

#### Explications

AWS WAF is an application-layer firewall that filters HTTP(S) requests to protect web applications from common exploits (for example, SQL injection, XSS). It does not perform host-level or OS-level vulnerability assessments on EC2 instances or run predefined assessment templates.  
B. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor analyzes your AWS environment and provides best-practice recommendations across cost, performance, security, fault tolerance, and service limits. It offers configuration guidance but does not run vulnerability scans or produce CVE-level findings for EC2 instances.  
**Votre réponse est correcte**  
C. Amazon Inspector

#### Explications

Amazon Inspector is a managed security assessment service that performs automated vulnerability and configuration assessments on EC2 instances. It uses predefined assessment templates (rules packages) to detect known CVEs, insecure configurations, and deviations from security benchmarks, and produces prioritized findings that can be scheduled or run on demand and integrated with other security services.  
D. AWS Shield

#### Explications

AWS Shield provides managed protection against distributed denial-of-service (DDoS) attacks (Standard and Advanced tiers). Its scope is DDoS mitigation for applications and networking, not vulnerability scanning of EC2 hosts.  
Explication générale  
The question targets the AWS service purpose-built for host-level vulnerability and configuration assessments. Amazon Inspector is the correct choice because it runs automated scans using predefined assessment templates/rules packages and returns prioritized findings for EC2 instances. The distractors address other security concerns: WAF protects web traffic, Trusted Advisor offers high-level best-practice recommendations, and Shield defends against DDoS attacks—none perform EC2 vulnerability scans.  
Domaine  
Domain 2: Security and Compliance  
Question 92Correct  
Which option is a responsibility of AWS under the AWS shared responsibility model?  
A. Application data security

#### Explications

Protecting application data (including encryption, backups, and data classification) is the customer's responsibility under the shared responsibility model—customers control what data is stored and how it is secured in AWS and must use services like AWS KMS, S3 encryption, and application-level controls to protect it.  
B. Patch management for applications that run on Amazon EC2 instances

#### Explications

When you run applications on Amazon EC2 (IaaS), you are responsible for the guest operating system and application stack, including installing and patching application software; AWS provides the underlying compute but does not patch customer-installed applications on EC2 instances.  
**Votre réponse est correcte**  
C. Patch management of the underlying infrastructure for managed services

#### Explications

AWS is responsible for patching and maintaining the underlying infrastructure for its managed services (the “security of the cloud”): for services such as Amazon RDS, AWS Patch Manager, Lambda, and S3, AWS maintains the host OS, hypervisor, physical hardware, and networking components while customers manage their data and configuration.  
D. Application identity and access management

#### Explications

Managing application identities, permissions, and access policies is a customer responsibility: AWS provides IAM and related services, but customers must configure roles, policies, tokens, and application-level authentication/authorization to control access to their resources.  
Explication générale  
The AWS shared responsibility model splits duties: AWS handles the security and maintenance of the cloud infrastructure (physical hosts, network, hypervisor, and managed-service host patching), while customers handle security in the cloud (data, applications, OS, and access control). The correct choice highlights AWS responsibility for patching the underlying infrastructure of managed services; the other options describe tasks that remain the customer's responsibility.  
Domaine  
Domain 2: Security and Compliance  
Question 93Correct  
A company needs a fully managed file server that natively supports Microsoft workloads and file systems. The file server must also support the SMB protocol. Which AWS service should the company use to meet these requirements?  
A. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed NFS file system designed for Linux-based workloads and exposes NFSv4 mounts. It does not provide native SMB protocol support, Windows ACL/NTFS semantics, or built-in Active Directory integration required for Windows-native file shares.  
B. Amazon FSx for Lustre

#### Explications

Amazon FSx for Lustre delivers high-performance POSIX-compliant file systems for compute- and HPC-focused Linux workloads and S3 integration. It uses the Lustre protocol (not SMB) and lacks Windows-native features such as SMB, NTFS semantics, and AD integration.  
**Votre réponse est correcte**  
C. Amazon FSx for Windows File Server

#### Explications

Amazon FSx for Windows File Server is a fully managed, native Windows file system that implements the SMB protocol, supports NTFS permissions and Windows ACLs, integrates with Microsoft Active Directory (including AWS Managed Microsoft AD), and provides automated backups and encryption — matching the requirements for Microsoft workloads and SMB file sharing.  
D. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS provides block-level storage volumes for attachment to a single EC2 instance. It is not a managed network file server; SMB would have to be configured and managed on an EC2 instance, and EBS does not provide the native Windows file-sharing features or AD integration required.  
Explication générale  
The requirement is a fully managed file server that natively supports Microsoft workloads and the SMB protocol. Amazon FSx for Windows File Server is purpose-built for Windows file shares (SMB), NTFS semantics, Windows ACLs, and Active Directory integration, so it directly meets the need. The other options are for NFS/Linux (EFS), high-performance Lustre (FSx for Lustre), or block storage for EC2 (EBS), and therefore do not provide the native SMB/Windows capabilities required.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 94Correct  
Under the AWS shared responsibility model, which tasks will be the company’s responsibility when building an application that uses AWS Lambda to run Python code? (Choose two.)  
A. Management of the underlying infrastructure.

#### Explications

Incorrect. For AWS Lambda the provider is responsible for the underlying compute infrastructure (servers, virtualization, networking, scaling). Customers do not manage or patch those physical/virtual hosts when using managed serverless services.  
B. Management of the operating system.

#### Explications

Incorrect. The Lambda service is a managed runtime environment; AWS handles the operating system, patching, and the execution environment for provided runtimes so customers do not manage the OS for standard Lambda functions.  
**Votre sélection est correcte**  
C. Writing the business logic code.

#### Explications

Correct. Customers are responsible for the application code and its deployment artifacts, including packaging dependencies, implementing business logic, input validation, error handling, and configuration of the function (timeouts, memory, triggers).  
D. Installation of the computer language runtime.

#### Explications

Incorrect. Standard language runtimes (e.g., Python) are provided and managed by AWS for Lambda. While you can supply a custom runtime or use layers, you still supply the runtime code; AWS manages its installation on the managed execution environment, not the customer managing underlying installation on hosts.  
**Votre sélection est correcte**  
E. Providing AWS Identity and Access Management (IAM) access to the Lambda service.

#### Explications

Correct. Customers must configure IAM identities, roles, and policies to control who/what can invoke functions and what AWS resources those functions can access; access management and least-privilege permissions are the customer’s responsibility.  
Explication générale  
This question tests the AWS shared responsibility model for serverless services. AWS manages the physical and execution infrastructure (hosts, OS, provided runtimes), while the customer remains responsible for their application assets and security controls around access. The best answers indicate responsibilities owned by the customer: providing and managing the function’s code/dependencies and configuring IAM access (C and E). The other options describe responsibilities that AWS handles for managed Lambda runtimes and infrastructure.  
Domaine  
Domain 2: Security and Compliance  
Question 95Correct  
Which AWS service provides highly durable object storage?  
**Votre réponse est correcte**  
A. Amazon S3

#### Explications

S3 is AWS’s managed object storage service engineered for extreme durability. AWS states 99.999999999% (11 nines) durability for objects by redundantly storing data across multiple Availability Zones within a region and automatically repairing data when inconsistencies are detected. S3 also provides multiple storage classes and lifecycle features for long-term retention, making it the appropriate choice when the requirement is highly durable object storage.  
B. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed, regional file system that provides POSIX-compliant, shared file storage for EC2 instances (NFS). It is optimized for file-based workloads with semantics like directories and file locking. Because it is file storage (not an object store) and is designed for different access patterns, it is not the service marketed for the 11‑nine object durability guarantees.  
C. Amazon Elastic Block Store (Amazon EBS)

#### Explications

Amazon EBS provides block-level storage volumes that attach to EC2 instances and are designed for low-latency, transactional storage for a single AZ (with some multi‑attach options). EBS is not an object storage service; while snapshots can be copied to Amazon S3 for durability, EBS itself is AZ-scoped and intended for VM-attached block devices rather than durable, highly-available object storage.  
D. Amazon FSx

#### Explications

Amazon FSx offers fully managed file systems (for example, Windows File Server or Lustre) tailored to specific workloads that require file system features and protocols. FSx is file storage with different performance and feature trade-offs and is not the AWS object storage service that provides the 11‑nine durability SLA.  
Explication générale  
The question tests knowledge of AWS storage service categories and durability guarantees. The correct choice is the AWS object storage service that provides 99.999999999% durability by replicating objects across multiple Availability Zones and offering storage-class and lifecycle controls. The other options are file or block storage solutions (EFS, EBS, FSx) designed for different access patterns and do not provide the same object-storage semantics or the advertised 11‑nine durability.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 96Correct  
Which AWS service or resource can a company use to deploy AWS WAF rules?  
A. Amazon EC2

#### Explications

EC2 instances are compute resources that run applications but are not a supported attachment point for AWS WAF. To protect web traffic served by EC2, you associate a WAF Web ACL with a supported front-end (for example an Application Load Balancer or CloudFront) that sits in front of the instances.  
**Votre réponse est correcte**  
B. Application Load Balancer

#### Explications

AWS WAF is attached to a resource as a Web ACL. Application Load Balancers operate at the application (Layer 7\) and support direct association of a WAF Web ACL so HTTP/HTTPS requests can be inspected and filtered before reaching backend targets.  
C. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor is an account-level advisory service that provides best-practice checks and recommendations (cost, performance, security, fault tolerance). It does not process network traffic or host WAF rules and cannot be used to deploy AWS WAF protections.  
D. Network Load Balancer

#### Explications

Network Load Balancers operate at the transport layer (Layer 4\) and do not support AWS WAF integration. Because WAF inspects application-layer (HTTP/S) requests, it must be associated with a Layer 7 service (ALB, CloudFront, API Gateway), not an NLB.  
Explication générale  
AWS WAF is a web application firewall implemented as a Web ACL that must be associated with supported front-end resources that handle HTTP/HTTPS at Layer 7\. An Application Load Balancer is a supported attachment point and therefore the correct choice. EC2 and NLB cannot host WAF directly, and Trusted Advisor is only an advisory service, not a traffic-filtering resource.  
Domaine  
Domain 2: Security and Compliance  
Question 97Incorrect  
A company is planning to migrate applications to the AWS Cloud. During a system audit, the company finds that its content management system (CMS) application is incompatible with cloud environments. Which migration strategies will help the company to migrate the CMS application with the LEAST effort? (Choose two.)  
**Votre sélection est incorrecte**  
A. Retire

#### Explications

Retiring an application means decommissioning it. That does not migrate functionality or data to the cloud — it only applies when the system is no longer required, so it is not a migration strategy for keeping the CMS available in the cloud.  
**Sélection correcte**  
B. Rehost

#### Explications

Moving the existing system to infrastructure-as-a-service (lift-and-shift) runs the application with minimal or no code changes by hosting it on Amazon EC2 (or equivalent VM-based resources). This is typically the fastest, lowest-effort way to move non-cloud-native software because it preserves the current runtime environment while placing it on cloud infrastructure.  
**Votre sélection est correcte**  
C. Repurchase

#### Explications

Replacing the current product with a cloud/SaaS alternative (drop-and-shop) avoids deep application changes by adopting a managed, cloud-native CMS or marketplace offering. This is often low-effort from a development perspective, though it requires planning for data migration and configuration.  
D. Replatform

#### Explications

Replatforming requires making targeted changes so the app can use some managed cloud services (for example moving a database to Amazon RDS or deploying to Elastic Beanstalk). It reduces operational overhead but involves more modification and testing than lift-and-shift or repurchasing.  
E. Refactor

#### Explications

Refactoring (re-architecting) rewrites the application to be cloud-native (microservices, serverless, managed services). This delivers long-term scalability and cloud advantages but requires significant development effort and is not a least-effort option.  
Explication générale  
The least-effort approaches for migrating an application that is not cloud-native are: moving it as-is onto cloud infrastructure (lift-and-shift to EC2) or replacing it with a cloud/SaaS solution. Both minimize development changes compared with replatforming or refactoring; retiring simply removes the application. Therefore Rehost and Repurchase are the best low-effort choices.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 98Correct  
Which of the following best describes the AWS shared responsibility model?  
**Votre réponse est correcte**  
A. AWS manages security of the cloud infrastructure, while the customer is responsible for security in the cloud.

#### Explications

AWS is responsible for protecting and operating the underlying global cloud infrastructure — the physical datacenters, networking, hosts, and foundational software — while customers retain responsibility for how they configure and use AWS services. Practical customer responsibilities include managing identities and permissions (IAM), configuring network controls (VPC, security groups, NACLs), securing and patching guest operating systems and applications on EC2, and protecting their data (encryption, backups, access controls). The exact split varies by service model (IaaS vs managed services), but the core distinction—security of the cloud vs security in the cloud—makes this option correct.  
B. AWS is responsible for all security aspects, including customer data and applications.

#### Explications

This overstates AWS’s role. AWS does not assume responsibility for customers’ data, application logic, or how customers configure access controls. Customers retain control over and responsibility for data classification, encryption keys (customer-managed KMS keys or application-level encryption), IAM policies, and application security. Even for managed services, customers must secure their data and access settings.  
C. Customers have no responsibilities under the shared responsibility model.

#### Explications

Incorrect because customers always have security duties when using AWS. Typical customer tasks include configuring IAM identities and policies, securing data and applications, applying patches to guest OS and application stacks (when applicable), and setting network access rules. The shared responsibility model explicitly assigns these responsibilities to customers.  
D. Security responsibilities are shared equally between AWS and the customer, with no clear delineation.

#### Explications

Incorrect: responsibilities are not an undefined 50/50 split. The model provides a clear delineation—AWS secures the infrastructure, customers secure what they deploy on that infrastructure—and responsibilities shift depending on the service model (for example, more AWS responsibility for underlying components in SaaS/PaaS vs IaaS).  
Explication générale  
The AWS shared responsibility model delineates that AWS secures the underlying cloud infrastructure (physical datacenters, networking, hosts, and foundational software), while customers are responsible for securing their data, identities, applications, and configurations within AWS. This distinction is service-model dependent (IaaS vs managed services) but remains the guiding principle. The correct option captures that split; the distractors either assign all responsibility to AWS, deny customer duties, or imply an undefined equal sharing, all of which contradict the model.  
Domaine  
Domain 2: Security and Compliance  
Question 99Correct  
What is the customer ALWAYS responsible for managing, according to the AWS shared responsibility model?  
A. Software licenses

#### Explications

Responsibility for licensing third‑party software you run on cloud instances can fall to you, but AWS also offers license‑included and managed offerings where AWS handles licensing. Because management depends on the chosen service and licensing model, it is not an absolute, always‑customer responsibility.  
B. Networking

#### Explications

AWS operates and maintains the underlying physical network and backbone, while customers configure and manage their virtual network settings (VPCs, subnets, security groups, route tables) inside their accounts. Network management is therefore shared and depends on the service and layer of the stack.  
**Votre réponse est correcte**  
C. Customer data

#### Explications

The data you upload, store, process and generate in your AWS account is always your responsibility. Under the shared responsibility model customers must classify data, control access (IAM, resource policies), protect confidentiality and integrity (encryption choices, backups, lifecycle policies), and meet compliance requirements for that information.  
D. Encryption keys

#### Explications

Control of cryptographic key material can be shared: AWS offers both AWS‑managed keys and customer‑managed keys (via KMS, Bring‑Your‑Own‑Key). If you select customer‑managed keys you are responsible for key policies, rotation and access control, but when AWS‑managed keys are used AWS handles key management—so key management is not universally an always‑customer task.  
Explication générale  
AWS is responsible for security of the cloud (hardware, global infrastructure and foundational services); customers are responsible for security in the cloud. The one constant customer responsibility is managing the information they put into AWS — including access control, protection, and compliance for that data. Other items listed (licensing, virtual network configuration, key management) can be shared or handled by AWS depending on the service and configuration, so they are not universally the customer’s sole responsibility.  
Domaine  
Domain 2: Security and Compliance  
Question 100Incorrect  
A company has a compute workload that is steady, predictable, and uninterruptible. Which Amazon EC2 instance purchasing options meet these requirements MOST cost-effectively? (Choose two.)  
**Votre sélection est incorrecte**  
A. On-Demand Instances

#### Explications

On‑Demand billing charges by the hour/second with no long‑term commitment. That flexibility comes at a higher unit price, so for steady, predictable, long‑running workloads it is not the most cost‑effective option compared with commitment‑based pricing models.  
**Votre sélection est correcte**  
B. Reserved Instances

#### Explications

Reserved Instances (RIs) provide a billing discount in exchange for a 1‑ or 3‑year commitment and payment options (All Upfront, Partial Upfront, No Upfront). Standard and Convertible RIs reduce hourly costs for consistent usage patterns, making them cost‑effective for predictable, non‑interruptible compute needs. (Note: RIs change pricing/billing — Capacity Reservations are a separate feature if physical capacity guarantees are required.)  
C. Spot Instances

#### Explications

Spot Instances use spare EC2 capacity at steep discounts but are interruptible — AWS can reclaim the instance with a short notification. Because the workload cannot tolerate interruptions, Spot is unsuitable despite its low cost.  
**Sélection correcte**  
D. Saving Plans

#### Explications

Savings Plans are a commitment to a consistent amount of compute spend (USD/hour) for 1 or 3 years and automatically apply discounted rates across eligible compute usage. Compute Savings Plans offer flexibility across instance families, sizes, regions, and AWS compute services, making them an effective cost‑optimization choice for steady, predictable workloads.  
E. Dedicated Hosts

#### Explications

Dedicated Hosts allocate an entire physical server to a single customer for compliance or licensing requirements. They typically cost more than shared tenancy options and are chosen for isolation/licensing reasons, not general cost savings for predictable workloads.  
Explication générale  
The question tests knowledge of AWS pricing models for steady, predictable, and non‑interruptible compute. Commitment‑based discounts (Reserved Instances and Savings Plans) deliver the best cost savings for continuous workloads because they lower unit costs in exchange for a term commitment. On‑Demand remains flexible but more expensive; Spot is unsuitable due to interruptions; Dedicated Hosts address isolation/compliance, not cost optimization in typical scenarios.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 101Correct  
A company launched an Amazon EC2 instance with the latest Amazon Linux 2 Amazon Machine Image (AMI). Which actions can a system administrator take to connect to the EC2 instance? (Choose two.)  
**Votre sélection est correcte**  
A. Use Amazon EC2 Instance Connect.

#### Explications

EC2 Instance Connect integrates with IAM and the ec2-instance-connect workflow to deliver a short-lived SSH public key to the instance's authorized\_keys (the instance needs the ec2-instance-connect package). This enables SSH access without pre-provisioning a long-lived key pair. Note that standard network controls still apply (the instance's security group must allow SSH/port 22 from the client).  
B. Use a Remote Desktop Protocol (RDP) connection.

#### Explications

RDP (Remote Desktop Protocol) is the standard remote GUI protocol for Windows. Amazon Linux 2 does not include an RDP server by default; using RDP would require installing a desktop environment and an RDP server and opening port 3389, which is nonstandard and not the intended method for connecting to a Linux EC2 instance.  
C. Use AWS Batch.

#### Explications

AWS Batch is a managed service for running batch computing jobs and job queues. It is not an interactive access mechanism and does not provide SSH/shell access to an arbitrary EC2 instance.  
**Votre sélection est correcte**  
D. Use AWS Systems Manager Session Manager.

#### Explications

AWS Systems Manager Session Manager provides interactive shell (or PowerShell) access via the SSM Agent over the AWS control plane, without opening inbound ports. It requires the SSM Agent on the instance and an instance role with appropriate SSM permissions (for example AmazonSSMManagedInstanceCore) and supports logging/auditing to CloudWatch or S3.  
E. Use Amazon Connect.

#### Explications

Amazon Connect is a cloud-based contact center service for customer engagement and telephony; it is unrelated to managing or establishing shell/desktop connections to EC2 instances.  
Explication générale  
The question tests which AWS services provide supported ways to access a Linux EC2 instance. The correct methods are EC2 Instance Connect and Systems Manager Session Manager: Instance Connect uses IAM and ephemeral SSH keys to enable SSH access, while Session Manager uses the SSM Agent and IAM roles to provide portless, auditable shell sessions. RDP is for Windows or a nonstandard Linux GUI setup, AWS Batch is for job orchestration (not interactive access), and Amazon Connect is a contact-center product.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 102Incorrect  
A company is deploying a machine learning (ML) research project that will require a lot of compute power over several months. The ML processing jobs do not need to run at specific times. Which Amazon EC2 instance purchasing option will meet these requirements at the lowest cost?  
A. On-Demand Instances

#### Explications

On‑demand capacity is billed by the second with no upfront commitment and is appropriate for short‑term, unpredictable workloads. Because it carries the highest per‑unit price compared with commitment‑based or spare‑capacity options, it is not the lowest‑cost choice for months‑long, interruptible ML processing.  
**Bonne réponse**  
B. Spot Instances

#### Explications

La charge de travail décrite tolère une certaine flexibilité dans la planification et les interruptions. L'utilisation de la capacité EC2 disponible sur AWS à des prix très avantageux (instances Spot Amazon EC2) permet d'obtenir le coût horaire le plus bas pour les tâches gourmandes en calcul et non critiques en termes de temps. L'architecture pour les instances Spot nécessite la gestion des interruptions (en utilisant la notification d'interruption de deux minutes, la création de points de contrôle ou la replanification des tâches via Spot Fleet, AWS Batch ou des services gérés comme la formation Spot gérée de SageMaker).  
C. Instances réservées

#### Explications

La capacité réservée nécessite un engagement de 1 ou 3 ans (instances réservées standard ou convertibles) et offre des réductions par rapport à la facturation à la demande pour une utilisation prévisible et stable. Pour un projet de recherche de plusieurs mois avec des horaires flexibles et une tolérance aux interruptions, les réservations à long terme sont moins rentables et moins flexibles que l'utilisation de modèles de tarification basés sur la capacité disponible.  
**Votre réponse est incorrecte**  
D. Instances dédiées

#### Explications

Les instances dédiées s'exécutent sur du matériel mono-locataire isolé au niveau de l'hôte afin de répondre à des exigences spécifiques de conformité ou de licence. Elles augmentent les coûts et n'offrent aucun avantage tarifaire pour les charges de travail d'apprentissage automatique à usage général et sensibles aux coûts, qui peuvent tolérer les interruptions.  
Explication générale  
Les tâches de ML pouvant s'exécuter à tout moment et tolérer les interruptions, le modèle d'achat EC2 le plus économique consiste à utiliser la capacité disponible proposée à prix fortement réduits et à concevoir la charge de travail pour une résilience optimale face aux interruptions. Les options basées sur l'engagement (instances réservées/plans d'économies) permettent de réduire les coûts pour une utilisation stable et prévisible, tandis que les instances à la demande ou dédiées sont soit plus onéreuses, soit destinées à des besoins différents.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 103Correct  
Une entreprise souhaite exécuter son application sur des instances Amazon EC2. Elle doit conserver l'application sur site pour des raisons de conformité. Quelle offre AWS répond à ces exigences ?  
A. Instances dédiées

#### Explications

Les instances dédiées offrent une capacité EC2 sur du matériel physique dédié à un seul compte AWS, mais ce matériel reste au sein des régions/zones de disponibilité AWS. Elles n'installent ni n'exécutent d'infrastructure sur le site du client et ne peuvent donc pas répondre à l'exigence de conserver l'application sur site. (Les hôtes dédiés fonctionnent de manière similaire, car leur matériel est hébergé par AWS.)  
B. Amazon CloudFront

#### Explications

Amazon CloudFront est un réseau de distribution de contenu (CDN) qui met en cache et distribue du contenu depuis les points de présence AWS afin d'améliorer la latence et les performances. Il ne fournit pas de ressources de calcul sur site ni la possibilité d'héberger des instances EC2 dans un centre de données client ; par conséquent, il ne répond pas aux exigences de conformité relatives aux infrastructures sur site.  
C. AWS Fargate

#### Explications

AWS Fargate est un moteur de calcul conteneurisé sans serveur pour ECS/EKS qui s'exécute sur l'infrastructure gérée par AWS. Il ne déploie ni serveurs physiques ni instances EC2 chez le client et ne peut donc pas être utilisé pour héberger l'application sur site à des fins de conformité.  
**Votre réponse est correcte**  
D. Postes avancés AWS

#### Explications

AWS Outposts étend l'infrastructure, les services et les API AWS à l'environnement sur site d'un client en installant des racks/appliances gérés par AWS dans le centre de données. Il prend en charge les instances EC2 natives, les volumes EBS et d'autres services AWS en local, tout en s'intégrant au plan de contrôle AWS, permettant ainsi de répondre aux exigences de conformité qui imposent le maintien des charges de travail sur site.  
Explication générale  
Cette question évalue les options de cloud hybride pour garantir la conformité aux exigences des infrastructures sur site. AWS Outposts est la solution idéale car elle déploie physiquement l'infrastructure AWS et les mêmes API AWS dans le centre de données du client, permettant ainsi l'exécution d'instances EC2 sur site. Les autres options sont des services hébergés par AWS (instances dédiées, CloudFront, Fargate) et n'installent pas de matériel de calcul chez le client.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 104Correct  
Parmi les services AWS suivants, lesquels sont sans serveur ? (Choisissez deux réponses.)  
A. Postes de contrôle AWS

#### Explications

Cette option permet de déployer l'infrastructure AWS sur site sous forme de solution hybride et nécessite la mise en service et la gestion de racks/capacités physiques ; elle ne dégage pas de toute responsabilité l'infrastructure sous-jacente, elle n'est donc pas sans serveur.  
B. Amazon EC2

#### Explications

Cette option fournit des instances de serveur virtuel que vous lancez, configurez et gérez (système d'exploitation, correctifs, mise à l'échelle) ; étant donné que vous gérez les instances de calcul, il ne s'agit pas d'un service sans serveur.  
C. Amazon Elastic Kubernetes Service (Amazon EKS)

#### Explications

Cette option propose un plan de contrôle Kubernetes géré, mais l'exécution des charges de travail implique généralement la gestion des nœuds de travail (ou l'utilisation de Fargate). La nécessité de gérer la capacité du cluster/des nœuds et l'orchestration signifie que le service n'est pas intrinsèquement sans serveur.  
**Votre sélection est correcte**  
D. AWS Fargate

#### Explications

Cette option est un moteur de calcul de conteneurs sans serveur qui vous permet d'exécuter des conteneurs sans provisionner ni gérer d'instances EC2 ; elle abstrait les serveurs sous-jacents, met à l'échelle les tâches automatiquement et facture les ressources vCPU et mémoire utilisées.  
**Votre sélection est correcte**  
E. AWS Lambda

#### Explications

Cette option est un service de calcul entièrement sans serveur qui exécute du code en réponse à des événements avec une mise à l'échelle automatique, sans provisionnement de serveur et avec une facturation à l'exécution ; elle s'intègre à de nombreuses sources d'événements AWS.  
Explication générale  
Les services sans serveur éliminent la nécessité de provisionner, gérer ou mettre à jour des serveurs et offrent une mise à l'échelle automatique ainsi qu'une facturation à l'usage. Les solutions optimales sont le moteur de calcul conteneurisé qui abstrait les instances et le service d'exécution de code événementiel, car tous deux suppriment la gestion des serveurs. Les autres solutions nécessitent la gestion de matériel physique, de serveurs virtuels ou de nœuds de conteneurs (sauf si elles sont spécifiquement associées à une option sans serveur) et ne peuvent donc pas être considérées comme telles individuellement.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 105Correct  
De quelles manières le cloud AWS offre-t-il un coût total de possession (TCO) des ressources informatiques inférieur à celui des centres de données sur site ? (Choisissez deux réponses.)  
**Votre sélection est correcte**  
A. AWS remplace les dépenses d'investissement initiales par des coûts à la carte.

#### Explications

Converting large capital purchases into recurring, usage-based operating expenses lets organizations avoid upfront hardware procurement and depreciation. AWS billing by consumption plus the ability to right-size and autoscale resources reduces idle capacity and lowers the capital tied up in infrastructure, which contributes directly to a lower TCO.  
B. AWS is designed for high availability, which eliminates user downtime.

#### Explications

High availability and redundancy can reduce downtime risk but do not by themselves guarantee lower TCO. Implementing multi‑AZ or multi‑Region architectures can actually increase resource and data transfer costs; availability is an operational/design benefit rather than the primary mechanism for reducing total ownership cost.  
C. AWS eliminates the need for on-premises IT staff.

#### Explications

Moving to AWS can reduce some infrastructure management tasks through managed services, but it does not eliminate the need for skilled personnel. Roles shift toward cloud architecture, operations, security, and cost governance; staffing and operational overhead remain components of TCO rather than being completely removed.  
**Votre sélection est correcte**  
D. AWS uses economies of scale to continually reduce prices.

#### Explications

Operating a global, multi‑tenant cloud allows AWS to spread fixed infrastructure costs across many customers, achieve lower per‑unit costs, and continually invest in efficiency. Those scale-driven efficiencies and operational automation enable AWS to lower prices and offer cost-saving purchasing options, which reduces ongoing customer costs.  
E. AWS offers a single pricing model for Amazon EC2 instances.

#### Explications

Incorrect — Amazon EC2 supports multiple pricing mechanisms (On‑Demand, Reserved Instances/Savings Plans, Spot Instances, Dedicated Hosts) each designed for different usage patterns. Claiming a single pricing model for EC2 is inaccurate and would not explain how AWS lowers TCO.  
Explication générale  
This question tests how AWS pricing and operational model reduce TCO. The primary levers are converting capital expenditures into consumption‑based operating expenses (so customers avoid large upfront hardware costs and reduce idle capacity) and AWS’s large scale, which lowers per‑unit infrastructure costs and enables ongoing price efficiencies. The distractors confuse other benefits (availability, staffing changes, or incorrect pricing claims) with the core cost drivers.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 106Correct  
Which of the following is entirely the responsibility of AWS, according to the AWS shared responsibility model?  
A. Security awareness and training

#### Explications

Customer responsibility. Security awareness and training are part of an organization’s internal security program (security in the cloud). AWS provides guidance and training resources, but customers must implement and operate employee training, policies, and processes to reduce human risk.  
B. Development of an IAM password policy

#### Explications

Customer responsibility. IAM is an AWS service, but configuration of identity and access (including password policies, user permissions, and MFA enforcement) is managed and enforced by the customer within their AWS accounts.  
C. Patching of the guest operating system

#### Explications

Customer responsibility for IaaS. When running guest operating systems on services like Amazon EC2, the customer is responsible for OS-level patching and hardening. Note the nuance: for fully managed AWS services (for example, Amazon RDS, AWS Lambda, or Amazon S3) AWS handles underlying OS and platform patching.  
**Votre réponse est correcte**  
D. Physical and environmental controls

#### Explications

AWS responsibility. Under the shared responsibility model AWS is responsible for security of the cloud — physical and environmental controls for data centers, facility access, power, networking, and the host infrastructure are managed and operated by AWS.  
Explication générale  
AWS and customers share security tasks: AWS is responsible for “security of the cloud” (physical datacenter security, host infrastructure, and foundational services), while customers are responsible for “security in the cloud” (configuration, data, identities, OS management, and training). Therefore the physical and environmental controls are AWS’s responsibility; the other choices describe customer-managed responsibilities (with the exception that some managed AWS services reduce customer responsibilities for underlying OS patching).  
Domaine  
Domain 2: Security and Compliance  
Question 107Correct  
Which of the following are benefits of migrating to the AWS Cloud? (Choose two)  
**Votre sélection est correcte**  
A. Cost savings through reduced infrastructure management

#### Explications

Migrating to AWS reduces capital expenditure and ongoing hardware maintenance by shifting to pay-as-you-go and managed-service models. AWS pricing and capacity features (On‑Demand, Reserved Instances, Savings Plans, Auto Scaling) let organizations right‑size resources and lower total cost of ownership versus maintaining equivalent on‑premises infrastructure.  
B. Increased hardware requirements for on-premises data centers

#### Explications

Incorrect. Moving workloads to AWS normally decreases the need for on‑premises hardware because compute, storage, and networking are provided by AWS. Migration typically enables consolidation or decommissioning of data center equipment rather than increasing it.  
**Votre sélection est correcte**  
C. Enhanced scalability and flexibility of resources

#### Explications

AWS provides elastic, on‑demand resource provisioning and services that automatically adjust capacity to demand (Auto Scaling, Elastic Load Balancing, serverless options such as Lambda, and global Regions/AZs). This built‑in elasticity and broad service catalogue deliver the scalability and flexibility described.  
D. Higher operational complexity and management overhead

#### Explications

Incorrect as stated. Many AWS managed services (for example, Amazon RDS, AWS Fargate, AWS Lambda) are designed to reduce operational burden by handling patching, backups, and underlying infrastructure. That said, cloud adoption does introduce new responsibilities (architecture, governance, cost management), but it does not inherently increase basic operational complexity compared with managing physical datacenters.  
E. Improved security and compliance posture

#### Explications

Partially true but not guaranteed. AWS offers extensive security controls and compliance programs (IAM, KMS, CloudTrail, Security Hub; certifications like ISO, SOC, PCI), which can improve security posture when used correctly. However, under the AWS shared responsibility model, customers remain responsible for configuration and data security — so migration alone does not automatically ensure improved security and compliance.  
Explication générale  
The question tests core cloud benefits: moving to AWS commonly reduces capital and operational costs through pay‑as‑you‑go and managed services, and provides elasticity that enables rapid scaling of resources. Statements about increased on‑premises hardware or inherently higher operations overhead are incorrect. Improved security/compliance is enabled by AWS capabilities but depends on proper customer configuration under the shared responsibility model.  
Domaine  
Domain 1: Cloud Concepts  
Question 108Correct  
Which AWS service gives users the ability to discover and protect sensitive data that is stored in Amazon S3 buckets?  
**Votre réponse est correcte**  
A. Amazon Macie

#### Explications

Correct — this managed AWS service uses machine learning and pattern matching to automatically discover and classify sensitive data (for example, PII and credentials) stored in Amazon S3. It generates findings and risk scores, supports managed and custom data identifiers, provides dashboards and alerts, and can forward findings to AWS Security Hub or EventBridge for automated workflows and remediation.  
B. Amazon Detective

#### Explications

Incorrect — this service is designed to help investigate and visualize the root cause of security issues by analyzing logs and building relationship graphs (for example, using AWS CloudTrail, VPC Flow Logs, and GuardDuty findings). It does not perform content inspection or classification of objects stored in S3.  
C. Amazon GuardDuty

#### Explications

Incorrect — this is a threat-detection service that continuously monitors for malicious or unauthorized behavior across AWS accounts using anomaly detection on logs (CloudTrail, VPC Flow Logs, DNS). It can surface suspicious activity related to S3 access but does not classify or discover sensitive data inside S3 objects.  
D. AWS IAM Access Analyzer

#### Explications

Incorrect — Access Analyzer evaluates resource-based policies and identifies resources that are shared with external principals or are publicly accessible. It helps find unintended access paths but does not inspect object contents or classify sensitive data in S3.  
Explication générale  
The question tests knowledge of AWS data-protection capabilities for S3. The correct choice is the service purpose-built for automated discovery, classification, and protection of sensitive data in S3 (using ML, managed/custom identifiers, findings, and integrations for remediation). The distractors are security or identity tools: one for investigation/visualization, one for threat detection, and one for access-policy analysis — none provide content-level data classification of S3 objects.  
Domaine  
Domain 2: Security and Compliance  
Question 109Correct  
Which task is the customer’s responsibility, according to the AWS shared responsibility model?  
A. Maintain the security of the AWS Cloud.

#### Explications

Incorrect. Under the AWS Shared Responsibility Model, AWS is responsible for “security of the cloud” — the underlying infrastructure that runs AWS services (physical facilities, hardware, network, and the virtualization layer). Customers do not maintain those infrastructure-level controls.  
**Votre réponse est correcte**  
B. Configure firewalls and networks.

#### Explications

Correct. Customers are responsible for “security in the cloud,” which includes configuring and managing network security controls such as security groups, network ACLs, VPC configuration, route tables, AWS WAF or Network Firewall rules, and any virtual appliance or third-party firewall they deploy to control traffic to their resources.  
C. Patch the operating system of Amazon RDS instances.

#### Explications

Incorrect. Amazon RDS is a managed database service: AWS handles the underlying host OS and many infrastructure-level patches for managed RDS instances. Customers remain responsible for database-level configuration, access control, data, and any client-side patching or self-managed databases running on EC2.  
D. Implement physical and environmental controls.

#### Explications

Incorrect. Physical and environmental controls for AWS data centers (perimeter security, power, cooling, and physical access) are AWS responsibilities. Customers are responsible for physical security of their on-premises systems and for protecting access to their AWS accounts and data.  
Explication générale  
This question tests the AWS Shared Responsibility Model: AWS is responsible for the security of the cloud infrastructure, while customers are responsible for security in the cloud. The best answer is the option about configuring network/firewall settings because that is a customer-managed activity (security groups, NACLs, VPCs, WAF/Network Firewall). The other options describe responsibilities AWS manages (infrastructure or physical controls) or responsibilities that differ for managed vs. self-managed services (RDS OS/infrastructure patching).  
Domaine  
Domain 2: Security and Compliance  
Question 110Correct  
Which of the following best describes the AWS shared responsibility model?  
**Votre réponse est correcte**  
A. AWS is responsible for security \*of\* the cloud, while the customer is responsible for security \*in\* the cloud.

#### Explications

This reflects the official AWS shared responsibility model: AWS controls and protects the foundational infrastructure (physical data centers, network, host hardware, hypervisor, and managed service control planes). Customers are responsible for security configurations and controls they deploy within their accounts — e.g., identity and access management (IAM), data classification and encryption, application security, OS and patch management for customer-managed instances, and network ACLs/security groups.  
B. AWS is responsible for all security aspects, including customer data and applications.

#### Explications

Incorrect. AWS does not take responsibility for customers' data, applications, or account-level configuration. Customers retain responsibility for how they configure services and protect their data (for example, choosing to encrypt objects in S3, managing KMS keys or IAM policies, and patching guest OS on EC2).  
C. Customers are responsible for security \*of\* the cloud, while AWS manages security \*in\* the cloud.

#### Explications

Incorrect. This reverses the model. AWS manages the underlying cloud infrastructure (hardware, networking, virtualization), while customers secure resources they deploy and configure inside the cloud environment.  
D. Security responsibilities are shared equally between AWS and the customer, with no clear delineation.

#### Explications

Incorrect. Responsibilities are explicitly delineated and depend on the service model (IaaS, PaaS, SaaS). For example, with EC2 customers manage the guest OS and applications, while with AWS-managed services (RDS, Lambda) AWS handles more of the underlying stack — but customers still control data, access, and configuration.  
Explication générale  
The AWS shared responsibility model separates duties: AWS secures the cloud infrastructure and managed service control planes; customers secure their content and configurations inside the cloud (data, applications, IAM, patching, encryption). Exact boundaries shift by service model (IaaS vs PaaS vs SaaS), but the correct choice captures AWS managing the cloud platform and customers managing their in-cloud resources.  
Domaine  
Domain 2: Security and Compliance  
Question 111Correct  
Elasticity in the AWS Cloud refers to which of the following? (Choose two.)  
A. How quickly an Amazon EC2 instance can be restarted

#### Explications

Incorrect. Elasticity concerns scaling resources in response to demand; the speed to restart a single EC2 instance relates to instance lifecycle and availability, not to the capacity to scale resources up or down automatically.  
**Votre sélection est correcte**  
B. The ability to rightsize resources as demand shifts

#### Explications

Correct. Elasticity means adjusting the quantity and size of resources to match workload changes (for example using Auto Scaling groups, Elastic Load Balancing, or serverless services) so capacity aligns with demand and cost is optimized.  
C. The maximum amount of RAM an Amazon EC2 instance can use

#### Explications

Incorrect. The maximum RAM of an EC2 instance is a fixed instance specification (instance type limit). Elasticity refers to changing provisioned capacity, not the hardware limits of a specific instance type.  
D. The pay-as-you-go billing model

#### Explications

Incorrect. Pay-as-you-go is a pricing model (consumption-based billing). While elasticity affects cost efficiency by scaling resources, pricing models describe how you are billed rather than the capability to scale resources automatically.  
**Votre sélection est correcte**  
E. How easily resources can be procured when they are needed

#### Explications

Correct. Elasticity includes the ability to rapidly provision and release resources on demand (for example launching EC2 instances, provisioning managed services, or relying on serverless scaling) so capacity can be obtained or removed as business needs change.  
Explication générale  
Elasticity is the cloud capability to dynamically increase or decrease computing resources automatically in response to workload changes, using services such as Auto Scaling, Elastic Load Balancing, and serverless platforms. The correct choices emphasize adjusting (rightsizing) resources and rapid provisioning/deprovisioning. The distractors confuse elasticity with instance restart time, fixed hardware limits, or billing models, which are related topics but not the definition of elasticity.  
Domaine  
Domain 1: Cloud Concepts  
Question 112Correct  
Which AWS service allows users to download security and compliance reports about the AWS infrastructure on demand?  
A. Amazon GuardDuty

#### Explications

Incorrect — Amazon GuardDuty is a managed threat detection service that analyzes VPC Flow Logs, AWS CloudTrail events, and DNS logs to generate security findings. It does not provide official AWS infrastructure compliance/audit reports for download.  
B. AWS Security Hub

#### Explications

Incorrect — AWS Security Hub centralizes and aggregates security findings, offers compliance standards checks and insights, and can produce posture summaries. It is not the repository for official AWS compliance audit artifacts (SOC, PCI, ISO reports) available for on-demand download.  
**Votre réponse est correcte**  
C. AWS Artifact

#### Explications

Correct — AWS Artifact is the AWS portal for on-demand access to AWS compliance reports and agreements (for example, SOC, PCI, ISO reports and legal agreements such as BAAs). It lets customers retrieve official AWS infrastructure audit documentation (typically PDFs) needed for compliance assessments.  
D. AWS Shield

#### Explications

Incorrect — AWS Shield provides DDoS protection (Standard and Advanced) for applications and related mitigations/response support. It is focused on attack mitigation, not delivering compliance or infrastructure audit reports.  
Explication générale  
The question assesses knowledge of where to obtain official AWS infrastructure compliance documentation. AWS Artifact is the dedicated service that provides on-demand access to AWS compliance reports and agreements. The other choices are security services with different responsibilities: GuardDuty (threat detection), Security Hub (findings aggregation and posture), and Shield (DDoS protection), so they do not serve as the source for downloadable compliance audit reports.  
Domaine  
Domain 2: Security and Compliance  
Question 113Correct  
Which tasks are customer responsibilities, according to the AWS shared responsibility model? (Choose two.)  
**Votre sélection est correcte**  
A. Configure the AWS provided security group firewall.

#### Explications

Configuring and managing security groups is a customer responsibility because security groups operate at the resource level and control inbound/outbound traffic for your AWS resources. AWS provides the security group capability, but customers must define rules, apply least-privilege network access, and maintain them as part of their security-in-the-cloud duties.  
**Votre sélection est correcte**  
B. Classify company assets in the AWS Cloud.

#### Explications

Classifying company assets and data sensitivity is a customer responsibility that informs choices for encryption, access controls, logging, and compliance. AWS does not determine your data governance or classification requirements—customers must evaluate business and regulatory needs and implement appropriate controls.  
C. Determine which Availability Zones to use for Amazon S3 buckets.

#### Explications

Incorrect. Amazon S3 is a regional service that automatically stores objects across multiple Availability Zones for durability; customers choose the AWS Region and storage class, not specific Availability Zones for S3 placement.  
D. Patch or upgrade Amazon DynamoDB.

#### Explications

Incorrect. Amazon DynamoDB is a fully managed AWS service; AWS is responsible for operating, patching, and upgrading the managed service infrastructure and software. Customers are responsible for their data, access policies, and application-level logic.  
E. Select Amazon EC2 instances to run AWS Lambda on.

#### Explications

Incorrect. AWS Lambda is a serverless service where AWS manages the underlying compute instances. Customers are responsible for function code, configuration (memory, timeout, IAM role), and permissions, but not selecting or managing EC2 instances for Lambda execution.  
Explication générale  
The AWS shared responsibility model splits duties: AWS secures the underlying cloud infrastructure and manages fully managed services, while customers are responsible for security in the cloud such as network-level controls and data governance. Configuring resource-level network controls (security groups) and classifying assets/data are customer tasks (A and B). The other options describe actions that AWS handles or are not applicable to the service behaviors (S3 AZ placement, DynamoDB patching, Lambda instance management).  
Domaine  
Domain 2: Security and Compliance  
Question 114Correct  
A company wants to migrate all of its on-premises infrastructure to the AWS Cloud. Before migration, the company wants estimate of costs for running its as-is infrastructure. Which AWS service or principle should the company use to meet this requirement?  
**Votre réponse est correcte**  
A. AWS Pricing Calculator

#### Explications

A web-based cost-modeling tool that lets you specify compute, storage, networking, database and other resource types, select regions and pricing options (On-Demand, Reserved Instances, Savings Plans), and produce a granular monthly cost estimate and breakdown for an as‑is environment. It supports manual input and import from discovery tools to model existing on-prem usage and compare pricing scenarios prior to migration.  
B. AWS Well-Architected Framework

#### Explications

Un ensemble de bonnes pratiques de conception (incluant un volet d'optimisation des coûts) pour la création et l'exploitation de charges de travail cloud. Il permet d'évaluer la qualité de l'architecture et de recommander des améliorations, mais ne fournit pas d'estimation des coûts ni de calculateur de prix pour les configurations sur site existantes.  
C. Modèle de responsabilité partagée d'AWS

#### Explications

Il s'agit d'un périmètre de sécurité et de conformité qui définit les responsabilités gérées par AWS et celles qui incombent au client. Ce périmètre concerne les rôles opérationnels et de sécurité, et non la tarification ou l'estimation des coûts de migration.  
D. Cadre d'adoption du cloud AWS (AWS CAF)

#### Explications

Ce cadre de référence aide les organisations à planifier leur transition vers le cloud en tenant compte des aspects humains, organisationnels et technologiques. Il soutient la stratégie et la préparation organisationnelle, mais ne fournit pas d'estimations de coûts détaillées pour l'infrastructure existante.  
Explication générale  
Utilisez le calculateur de prix AWS pour modéliser les ressources sur site actuelles de l'entreprise et obtenir des estimations de coûts détaillées pour l'exécution de l'environnement sur AWS. Les autres options (cadre Well-Architected, modèle de responsabilité partagée et cadre d'adoption du cloud) sont des cadres de référence et de gouvernance relatifs à l'architecture, aux responsabilités en matière de sécurité ou à la planification de l'adoption ; elles ne permettent pas de modéliser les coûts ni de fournir des estimations de prix directes.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 115Correct  
Une entreprise prévoit de migrer vers AWS et souhaite établir des estimations de coûts pour ses cas d'utilisation AWS. Quel service ou outil AWS peut-elle utiliser pour répondre à ces besoins ?  
**Votre réponse est correcte**  
A. Calculateur de prix AWS

#### Explications

Cet outil d'estimation en ligne est destiné aux scénarios de planification et de migration : il vous permet de modéliser une architecture prévue (sélection des services, des régions, des tailles d'instance, des classes de stockage et du transfert de données), produit une ventilation détaillée des coûts et une estimation mensuelle, et prend en charge l'exportation/le partage des résultats, ce qui en fait l'outil approprié pour créer des estimations de coûts initiales.  
B. Amazon CloudWatch

#### Explications

Un service de surveillance et d'observabilité qui collecte les métriques, les journaux et les alarmes pour une visibilité opérationnelle optimale. Il est utilisé pour le suivi des performances et des opérations, et non pour l'établissement d'estimations de coûts prévisionnelles pour une migration.  
C. AWS Cost Explorer

#### Explications

Un outil d'analyse des coûts qui visualise l'historique des dépenses et de l'utilisation, fournit des tendances, une répartition par catégories et des prévisions basées sur l'utilisation passée. Utile pour analyser et optimiser les dépenses existantes, il n'est cependant pas conçu comme outil principal pour modéliser de nouvelles estimations de coûts avant migration.  
D. Budgets AWS

#### Explications

Un outil de gouvernance permettant de définir des seuils, de recevoir des alertes et de suivre les budgets et l'utilisation (y compris les plans d'investissement/d'économies). Il contribue à la gestion et au contrôle des coûts courants, mais ne fournit pas la modélisation détaillée des coûts au niveau de l'architecture nécessaire aux estimations initiales de migration.  
Explication générale  
Cette question évalue vos connaissances des outils de calcul des coûts AWS. La bonne réponse est l'outil dédié à l'estimation des coûts, conçu pour modéliser l'utilisation prévue d'AWS et générer des estimations détaillées pour la planification des migrations. Les autres options sont utiles pour le suivi, l'analyse historique et la gestion continue des coûts, mais elles ne fournissent pas la modélisation des coûts prévisionnelle au niveau de l'architecture requise pour les estimations initiales.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 116Incorrect  
Une entreprise souhaite visualiser et gérer ses coûts et son utilisation du cloud AWS sur une période donnée. Quel service ou fonctionnalité AWS répond à ces besoins ?  
**Bonne réponse**  
A. Explorateur de coûts

#### Explications

Cet outil de gestion des coûts AWS propose des visualisations interactives et des rapports périodiques, permet de filtrer et de regrouper les coûts par compte associé, étiquette, service et type d'utilisation, et offre des prévisions et des recommandations d'achat. Grâce à ces fonctionnalités, il constitue la solution idéale pour analyser et gérer les coûts et l'utilisation sur une période donnée.  
B. Facturation consolidée

#### Explications

La facturation consolidée (une fonctionnalité d'agrégation de facturation au niveau du compte fournie via AWS Organizations) centralise la facturation et la répartition des coûts entre les comptes, mais ne fournit pas elle-même d'analyse visuelle interactive ni les fonctionnalités de reporting/prévision nécessaires pour visualiser les coûts au fil du temps.  
C. Organisations AWS

#### Explications

AWS Organizations est destiné à la gouvernance des comptes, à la gestion des politiques (SCP) et à la gestion centralisée de la facturation pour plusieurs comptes. Il ne propose pas les fonctionnalités interactives de visualisation des coûts et d'analyse des séries temporelles mentionnées dans la question.  
**Votre réponse est incorrecte**  
D. Budgets AWS

#### Explications

AWS Budgets permet de définir des seuils de coûts ou d'utilisation et de déclencher des alertes lorsque ces seuils sont atteints ou dépassés. Il contribue à faire respecter les limites, mais n'offre pas le même niveau de visualisation historique, de filtrage ou de prévision pour l'analyse des coûts.  
Explication générale  
La question porte sur la fonctionnalité AWS conçue pour visualiser et gérer les coûts et l'utilisation sur une période définie. La bonne réponse est l'outil d'analyse des coûts AWS, qui propose des rapports interactifs, des filtres précis, des prévisions et des recommandations. Les autres options concernent la facturation agrégée, la gestion de compte ou les alertes budgétaires ; bien que complémentaires, elles ne fournissent pas la fonctionnalité principale de visualisation et d'analyse demandée.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 117Correct  
Une entreprise doit catégoriser et suivre les coûts d'utilisation d'AWS en fonction de ses activités. Quel service ou fonctionnalité AWS doit-elle utiliser pour répondre à ces besoins ?  
**Votre réponse est correcte**  
A. Étiquettes d'affectation des coûts

#### Explications

Les étiquettes d'imputation des coûts sont des paires clé/valeur définies par l'utilisateur, appliquées aux ressources puis activées pour l'imputation des coûts dans la console de facturation. Une fois activées, ces étiquettes apparaissent dans l'Explorateur de coûts et le Rapport des coûts et de l'utilisation (RCU), permettant de regrouper, filtrer et imputer les dépenses par dimensions métier (par exemple, Projet, Département ou Application). Pour une utilisation optimale, il est essentiel d'utiliser des étiquettes cohérentes et de les activer correctement afin que les rapports incluent les données d'imputation pour l'analyse des coûts.  
B. Organisations AWS

#### Explications

AWS Organizations centralizes account management and supports consolidated billing and organizational units (OUs). It helps separate costs at the account or OU level but does not provide resource-level tagging or the tag-based categorization mechanism required to label and track costs by business category.  
C. AWS Security Hub

#### Explications

AWS Security Hub is a security posture and findings aggregation service; it focuses on security alerts and compliance checks across accounts and services and has no functionality for billing, cost allocation, or cost reporting.  
D. AWS Cost and Usage Report

#### Explications

The AWS Cost and Usage Report (CUR) produces detailed, raw billing records and can include activated cost allocation tags and resource IDs. CUR is the data source for analysis, but it is not the mechanism used to label resources by business category — tags are used to create those labels which CUR then can report on.  
Explication générale  
To categorize and track costs by business categories you must label resources with cost allocation tags (user-defined key/value pairs) and activate those tags for cost allocation. Cost Explorer and the Cost and Usage Report then consume those activated tags to present tag-based cost breakdowns. AWS Organizations and CUR are complementary (account-level separation and raw billing data respectively), while Security Hub is unrelated to billing.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 118Correct  
A company has multiple AWS accounts that include compute workloads that cannot be interrupted. The company wants to obtain billing discounts that are based on the company’s use of AWS services. Which AWS feature or purchasing option will meet these requirements?  
A. Resource tagging

#### Explications

Tagging is a cost-allocation and resource-management mechanism that helps categorize and report costs (for showback/chargeback and cost allocation reports). It does not change pricing tiers or aggregate usage across multiple accounts to produce volume-based discounts.  
**Votre réponse est correcte**  
B. Consolidated billing

#### Explications

AWS Organizations’ consolidated billing centralizes payment and aggregates usage from linked accounts under a single payer. Aggregated usage can meet higher pricing-tier thresholds and enables organization-level application of discounts and benefits (for example, shared Savings Plans/Reserved Instance benefits and volume pricing) without altering running compute instances.  
C. Pay-as-you-go pricing

#### Explications

On‑demand (pay-as-you-go) pricing charges based on actual consumption without long‑term commitment. It provides flexibility but does not by itself create cross-account volume discounts — those require consolidated billing, Savings Plans, or Reserved Instances.  
D. Spot Instances

#### Explications

Spot Instances provide steep discounts on spare EC2 capacity but are interruptible by AWS with short notice. They are inappropriate for workloads that cannot be interrupted.  
Explication générale  
The scenario requires volume-based billing discounts across multiple AWS accounts while keeping non‑interruptible compute running. Consolidated billing via AWS Organizations aggregates usage and enables organization-level discounts and sharing of certain purchasing benefits without interrupting workloads. Tagging helps cost reporting but not discounts; pay-as-you-go is flexible but doesn’t provide cross-account volume discounts; Spot Instances are interruptible and therefore unsuitable.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 119Correct  
Which Amazon EC2 pricing model provides the MOST cost savings for an always-up, right-sized database server running for a project that will last 1 year?  
A. On-Demand Instances

#### Explications

On-Demand Instances incur no long-term commitment and are billed per second or hour. That flexibility makes them costlier for continuous, predictable workloads because you miss the upfront commitment discounts that reserved models provide.  
B. Convertible Reserved Instances

#### Explications

Convertible Reserved Instances allow exchanging instance attributes during the term and provide discounts versus On-Demand. Because they trade some discount depth for flexibility, they usually yield less savings than Standard Reserved Instances for a stable, always-on server.  
C. Spot Instances

#### Explications

Spot Instances offer steep discounts by using spare EC2 capacity but can be interrupted with little notice. They are intended for fault-tolerant, flexible workloads and are unsuitable for an always-up, mission-critical database that requires continuous availability.  
**Votre réponse est correcte**  
D. Standard Reserved Instances

#### Explications

Standard Reserved Instances require a 1- or 3-year commitment to specific instance attributes and payment options, and in return deliver the largest per-instance discount relative to On-Demand for predictable, steady-state workloads. For a right-sized, always-on database for one year, this reservation model maximizes cost savings.  
Explication générale  
For an always-on, right-sized database running for a year, the best cost strategy is to commit to a reservation that trades flexibility for maximum discount. Standard Reserved Instances provide the deepest savings for predictable, continuous workloads. Convertible RIs and On-Demand preserve flexibility but cost more over a sustained period; Spot is cheaper only when interruptions are acceptable.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 120Correct  
A company is using multiple AWS accounts for different business teams. The finance team wants to receive one bill for all of the company's accounts. Which AWS service or tool should the finance team use to meet this requirement?  
**Votre réponse est correcte**  
A. AWS Organizations

#### Explications

Provides a single management (payer) account that receives one consolidated invoice for all member accounts. This setup aggregates usage across accounts for volume-based pricing benefits (for example, Savings Plans and Reserved Instance discounts) and integrates with Cost Explorer and Cost and Usage Reports so finance can review and attribute charges while retaining separate account boundaries.  
B. AWS Trusted Advisor

#### Explications

Un service de recommandations et de bonnes pratiques qui effectue des contrôles de sécurité, de tolérance aux pannes, de performance et d'optimisation des coûts ; il ne crée ni ne gère une seule facture et ne consolide pas la facturation entre les comptes.  
C. Explorateur de coûts

#### Explications

Outil de visualisation et d'analyse des coûts permettant d'explorer les dépenses historiques et prévisionnelles, de générer des rapports et de filtrer par compte ou étiquette. Il facilite l'analyse des coûts, mais ne génère pas de facture unique pour plusieurs comptes.  
D. Budgets AWS

#### Explications

Un outil de surveillance et d'alerte permettant de définir des seuils de coûts et d'utilisation et de recevoir des notifications. Utile pour maîtriser les dépenses, il ne permet cependant pas de consolider les factures ni de servir de compte payeur pour plusieurs comptes AWS.  
Explication générale  
La consolidation de la facturation, permettant au service financier de recevoir une seule facture, est gérée par AWS Organizations via un compte unique de gestion (payeur) qui regroupe les frais des comptes membres. Les outils associés (Trusted Advisor, Cost Explorer, AWS Budgets) fournissent des recommandations, des analyses et des alertes, mais ne créent pas de facture consolidée.  
Domaine  
Domaine 4 : Facturation, tarification et assistance

