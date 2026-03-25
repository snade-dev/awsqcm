Question 1Correct  
**Une entreprise souhaite gérer de manière centralisée l'accès de ses employés à plusieurs comptes AWS.**  
**Quel service ou fonctionnalité AWS l'entreprise devrait-elle utiliser pour répondre à ce besoin ?**  
A. Analyseur d'accès AWS Identity and Access Management

#### Explications

Access Analyzer examine les politiques basées sur les ressources, les politiques d'organisation et les politiques basées sur l'identité afin de détecter les partages de ressources en dehors des limites prévues. Il s'agit d'un outil d'analyse et de validation des accès aux ressources, et non d'un service centralisé de gestion des identités ou des autorisations permettant d'attribuer des accès aux utilisateurs sur plusieurs comptes AWS.  
B. Gestionnaire de secrets AWS

#### Explications

Secrets Manager stocke, renouvelle et récupère en toute sécurité les informations d'identification et autres secrets des applications et services. Il ne propose pas de fédération d'identités, d'authentification unique ni de gestion centralisée des utilisateurs et des autorisations pour l'ensemble des comptes AWS.  
**Votre réponse est correcte**  
C. Centre d'identité AWS IAM

#### Explications

IAM Identity Center centralise l'authentification unique et la gestion des autorisations pour plusieurs comptes AWS (généralement intégrés à AWS Organizations). Il utilise des ensembles d'autorisations pour définir des politiques d'accès réutilisables, prend en charge les fournisseurs d'identité externes (SAML/OIDC) et le provisionnement basé sur SCIM, et attribue les informations d'identification ou les rôles temporaires nécessaires à l'accès à la console et à l'API, évitant ainsi la création et la gestion d'utilisateurs IAM individuels dans chaque compte.  
D. Service de jetons de sécurité AWS (AWS STS)

#### Explications

AWS STS délivre des identifiants temporaires à privilèges limités (par exemple via AssumeRole ou la fédération) et est couramment utilisé pour permettre l'accès inter-comptes ou fédéré. STS ne fournit pas d'annuaire centralisé, d'interface utilisateur ni de système d'attribution des autorisations pour gérer l'accès des employés à plusieurs comptes.  
Explication générale  
La gestion centralisée des accès des employés sur plusieurs comptes AWS nécessite un service offrant l'authentification unique (SSO), la gestion des groupes et des autorisations, ainsi que l'intégration avec AWS Organizations — des fonctionnalités fournies par IAM Identity Center. Les autres options (Access Analyzer, Secrets Manager, STS) assurent des fonctions de sécurité importantes (analyse des politiques, gestion des secrets et émission d'identifiants temporaires), mais ne proposent pas les fonctionnalités centralisées d'identité, de provisionnement et d'attribution des autorisations nécessaires à la gestion des utilisateurs sur plusieurs comptes.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 2Incorrect  
Une entreprise souhaite surveiller les groupes de sécurité mal configurés qui autorisent un accès illimité à certains ports. Quel service AWS répond à ce besoin ?  
**Bonne réponse**  
A. Conseiller de confiance AWS

#### Explications

Trusted Advisor intègre un contrôle de sécurité dédié qui détecte les règles de groupe de sécurité autorisant un accès entrant illimité (par exemple, 0.0.0.0/0) à certains ports et propose des recommandations concrètes pour renforcer ces règles. Conçu pour la validation de la configuration des ressources de compte, ce service est idéal pour identifier et corriger les groupes de sécurité mal configurés.  
B. Amazon CloudWatch

#### Explications

CloudWatch collects metrics, logs, and events and is used to monitor performance and set alarms. It does not perform configuration assessments of AWS resources (such as identifying security group rules that allow 0.0.0.0/0) and therefore is not the right tool for detecting misconfigured security groups.  
C. Amazon GuardDuty

#### Explications

GuardDuty is a threat detection service that analyzes VPC flow logs, DNS logs, and CloudTrail events to surface malicious or anomalous activity (for example port scanning or compromised instances). It focuses on behavioral detection and not on static configuration checks of security group rules, so it won’t directly flag 'open to the world' ports as a configuration issue.  
**Votre réponse est incorrecte**  
D. AWS Health Dashboard

#### Explications

The AWS Health Dashboard reports the health and status of AWS services and events that affect an account’s access to AWS services. It does not evaluate or audit resource configurations like security group rules, so it cannot be used to monitor misconfigured security groups.  
Explication générale  
This question tests identification of the AWS service that performs security configuration checks. The correct choice is the service that flags security group rules permitting unrestricted access to specific ports because it performs configuration validation and offers remediation guidance. Other options focus on metrics/logs (CloudWatch), behavioral threat detection (GuardDuty), or service health (Health Dashboard), and therefore do not directly detect misconfigured security group rules. For continuous compliance you can also use AWS Config rules or aggregate findings in Security Hub, but Trusted Advisor provides the specific check described.  
Domaine  
Domain 2: Security and Compliance  
Question 3Correct  
A company wants to use a centralized AWS service to enforce compliance with the organizational business standards. The company wants to use an AWS service that can govern and control who can deploy, manage, and decommission AWS resources. Which AWS service will meet these requirements?  
A. Amazon CloudWatch

#### Explications

Amazon CloudWatch is an observability service (metrics, logs, alarms, dashboards, Events/EventBridge) used for monitoring and operational insight. It does not provide centralized governance or mechanisms to restrict who can provision, configure, or decommission approved resource offerings across an organization.  
**Votre réponse est correcte**  
B. AWS Service Catalog

#### Explications

AWS Service Catalog lets administrators create centrally managed portfolios of approved products (CloudFormation-based provisioning artifacts), apply constraints (launch/template constraints, TagOptions), and grant access via IAM and AWS Organizations. This enables enforcement of organizational standards, controlled provisioning, and lifecycle management (approved versions and deprovisioning) — matching the governance requirement.  
C. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat-detection service that analyzes VPC Flow Logs, AWS CloudTrail, and DNS logs to identify malicious or unauthorized activity. It improves security visibility but does not control or enforce which resources or configurations users may deploy.  
D. AWS Security Hub

#### Explications

AWS Security Hub aggregates, normalizes, and prioritizes security findings and compliance status across accounts and services (including standards like CIS or PCI). It provides visibility and automated checks but does not itself enforce deployment permissions or manage resource lifecycles.  
Explication générale  
The question targets centralized governance to enforce approved configurations and control who can provision and decommission resources. AWS Service Catalog is designed for that use case: administrators publish approved products and apply constraints and access controls so teams can only deploy compliant offerings. The other options (CloudWatch, GuardDuty, Security Hub) provide monitoring, threat detection, or findings aggregation — useful for security and observability, but not for enforcing and controlling resource provisioning and lifecycle.  
Domaine  
Domain 2: Security and Compliance  
Question 4Correct  
Which tasks are responsibilities of the customer, according to the AWS shared responsibility model? (Choose two.)  
A. Secure the virtualization layer.

#### Explications

Incorrect. The hypervisor, host hardware, physical data center, and virtualization stack are part of AWS’s responsibility (the “security of the cloud”). Customers do not manage or secure the underlying virtualization layer for AWS-managed compute services.  
**Votre sélection est correcte**  
B. Encrypt data and maintain data integrity.

#### Explications

Correct. Customers are responsible for protecting their data and ensuring its confidentiality and integrity within their AWS accounts. This includes selecting and implementing encryption (client-side, server-side, or KMS-managed keys), data classification, integrity checks, and managing access to encryption keys and data.  
C. Patch the Amazon RDS operating system.

#### Explications

Incorrect. Amazon RDS is a managed database service where AWS handles the underlying operating system and database engine patching and maintenance for managed instances. Customers remain responsible for database-level configuration, schemas, and user access; if a database runs on EC2, OS patching would be the customer’s responsibility.  
**Votre sélection est correcte**  
D. Maintain identity and access management controls.

#### Explications

Correct. Identity and access management within a customer’s AWS account is the customer’s responsibility. This covers creating and managing IAM users, roles, policies, groups, applying least-privilege permissions, enforcing MFA, and governing access across accounts (for example via AWS Organizations or IAM Identity Center).  
E. Secure Availability Zones.

#### Explications

Incorrect. Availability Zones and the physical datacenter infrastructure (including physical security, power, and networking redundancy) are operated and secured by AWS as part of the cloud provider’s obligations.  
Explication générale  
Cette question évalue la connaissance du modèle de responsabilité partagée d'AWS : AWS est responsable de la protection de l'infrastructure (installations physiques, réseau, virtualisation et zones de disponibilité), tandis que les clients sont responsables de la sécurité de leurs déploiements dans le cloud. La gestion de la protection des données (chiffrement et intégrité) et des contrôles d'identité et d'accès incombe aux clients, tandis que la sécurisation de la couche de virtualisation, des zones de disponibilité et du système d'exploitation sous-jacent RDS relève de la responsabilité d'AWS.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 5Correct  
**Quel service ou ressource AWS permet de bénéficier de réductions sur certains coûts des services AWS en échange d'un engagement de dépenses ?**  
A. Détective Amazon

#### Explications

Incorrect — Ce service est une offre d'investigation de sécurité et d'analyse des menaces qui agrège et analyse les données de journalisation (par exemple, les journaux de flux VPC, AWS CloudTrail et les résultats de GuardDuty) afin d'identifier la cause première des problèmes de sécurité. Il ne s'agit pas d'un programme tarifaire ou d'engagement et il n'offre aucune réduction en cas d'engagement de dépenses.  
B. Calculateur de prix AWS

#### Explications

Incorrect — Cet outil d'estimation des coûts et de budgétisation modélise les frais AWS prévus. Il permet de planifier et de comparer les coûts, mais n'accorde pas de prix réduits et n'exige aucun engagement de dépenses. Les remises sont proposées par le biais de programmes tels que les Savings Plans ou les instances réservées, et non par le calculateur de prix.  
**Votre réponse est correcte**  
C. Plans d'épargne

#### Explications

Exact — Les Savings Plans sont des programmes de tarification basés sur l'engagement, offrant des tarifs réduits en échange d'un engagement de dépenses fixes (en $/heure) sur une période de 1 ou 3 ans. Il en existe deux principaux types : les Savings Plans de calcul (les plus flexibles ; applicables à EC2, AWS Fargate et AWS Lambda) et les Savings Plans d'instances EC2 (applicables à des familles d'instances ou régions spécifiques). Les Savings Plans réduisent les tarifs à la demande lorsque l'utilisation engagée est atteinte.  
D. Soutien de base

#### Explications

Incorrect — Le niveau d'assistance de base comprend une aide gratuite pour la gestion du compte et la facturation, la documentation et des vérifications limitées par un conseiller de confiance. Il s'agit d'une offre d'assistance et non d'une réduction de prix ou de programmes nécessitant un engagement financier.  
Explication générale  
Cette question porte sur les programmes de réduction des coûts d'AWS. La bonne réponse est l'option de tarification avec engagement, qui propose des tarifs réduits pour un engagement de 1 ou 3 ans en $/heure (Savings Plans). Les autres options sont un service de sécurité, un outil d'estimation des coûts et un niveau de support ; aucune ne propose de réduction liée à un engagement de dépenses. Notez la différence avec les instances réservées : ces dernières sont plus spécifiques à une instance, tandis que les Savings Plans (en particulier les Compute Savings Plans) sont plus flexibles.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 6Incorrect  
**Une entreprise utilise Amazon Aurora comme service de base de données. Elle souhaite chiffrer ses bases de données et leurs sauvegardes.**  
**Selon le modèle de responsabilité partagée d'AWS, qui gère le chiffrement des clusters de bases de données et des instantanés de bases de données ?**  
**Votre réponse est incorrecte**  
A. AWS

#### Explications

Incorrect. AWS is responsible for the security "of" the cloud — the physical infrastructure, hypervisor, and managed-service control plane — but not for configuring a customer's database-level encryption or key policies. AWS may provide service-owned KMS keys and the encryption capability, yet enabling encryption for an Aurora cluster, selecting/creating KMS keys, and controlling access to snapshots are actions the customer must perform.  
**Bonne réponse**  
B. The company

#### Explications

Correct. Under the shared responsibility model the customer is responsible for protecting their data in the cloud. For Aurora this includes enabling encryption at rest for clusters and snapshots, choosing whether to use AWS-managed or customer-managed AWS KMS keys, managing key policies/rotation and IAM controls, and controlling access to encrypted snapshots and backups.  
C. AWS Marketplace partners

#### Explications

Incorrect. AWS Marketplace sellers provide third-party software or tools but do not assume responsibility for a customer’s encryption configuration by default. Marketplace offerings can help with encryption or key management if deployed, but responsibility to enable and manage database encryption remains with the customer unless a specific managed-services contract says otherwise.  
D. Third-party partners

#### Explications

Incorrect. Third-party partners or managed-service providers can be contracted to manage encryption on the customer's behalf, but responsibility does not automatically transfer to them under AWS's shared responsibility model. Unless explicitly agreed in a service contract, the customer retains responsibility for enabling encryption, key selection, and access control for Aurora and its snapshots.  
Explication générale  
This question tests understanding of the AWS shared responsibility model for data protection. AWS secures the underlying cloud infrastructure, while customers are responsible for protecting their data, including enabling encryption for Aurora clusters and snapshots and managing KMS keys and IAM access. The correct choice identifies the customer as responsible; the distractors confuse AWS infrastructure responsibilities or suggest third parties are automatically responsible.  
Domaine  
Domain 2: Security and Compliance  
Question 7Incorrect  
**Which task requires a user to sign in as the AWS account root user?**  
**Votre réponse est incorrecte**  
A. The deletion of IAM users

#### Explications

Incorrect — Deleting IAM users does not require the root user. Any IAM principal (user or role) granted the IAM:DeleteUser permission — for example via a least-privilege policy or AdministratorAccess — can remove IAM users. Root credentials are reserved for account-level, highly sensitive tasks and should not be used for routine identity management.  
**Bonne réponse**  
B. The deletion of an AWS account

#### Explications

Correct — Closing (deleting) an AWS account is an account-level, irreversible action that AWS restricts to the account root user. AWS requires root credentials to initiate account closure to protect against accidental or unauthorized termination; even IAM users with full administrative permissions cannot close the account.  
C. The creation of an organization in AWS Organizations

#### Explications

Incorrect — Creating an AWS Organization is performed by the management account and requires the Organizations:CreateOrganization permission. An IAM user or role in the account with the appropriate Organizations permissions can create an organization; this action is not strictly limited to the root user.  
D. The deletion of Amazon EC2 instances

#### Explications

Incorrect — Deleting (terminating) Amazon EC2 instances is controlled by EC2 permissions (for example EC2:TerminateInstances). IAM users or roles granted the necessary EC2 permissions can terminate instances; root sign-in is not required for this resource-level operation.  
Explication générale  
The root user is reserved for a small set of highly sensitive, account-wide operations. Closing an AWS account requires root sign-in because it affects the entire account and its billing and access. Most administrative and resource-level tasks (managing IAM users, creating an organization with proper permissions, terminating EC2 instances) can be performed by IAM principals granted the appropriate permissions.  
Domaine  
Domain 2: Security and Compliance  
Question 8Correct  
**Which task is a responsibility of AWS, according to the AWS shared responsibility model?**  
A. Configure identity and access management for applications.

#### Explications

Incorrect. Customers are responsible for defining and enforcing identity and access controls for their accounts and applications — creating IAM users, roles, policies, and federation settings. AWS provides the IAM service and the features, but it does not configure or manage your application-level access decisions for you.  
B. Manage encryption options for data that is stored on AWS.

#### Explications

Incorrect. While AWS offers encryption features and services (for example, server-side encryption and AWS KMS with AWS-managed or customer-managed CMKs), selecting encryption settings, applying encryption to customer data, and managing keys (when using customer-managed keys) are responsibilities of the customer under the shared responsibility model.  
C. Configure security groups for Amazon EC2 instances.

#### Explications

Incorrect. Security groups are virtual firewall rules that control inbound and outbound traffic for customer resources. Customers create and manage security group rules and network configurations for their EC2 instances and other resources; AWS provides the capability but does not configure your security group rules.  
**Votre réponse est correcte**  
D. Maintain the physical hardware of the infrastructure.

#### Explications

Correct. AWS is responsible for the physical infrastructure and its maintenance — data centers, physical servers, network hardware, racks, and the environmental and physical security controls — which falls under AWS’s “security of the cloud” responsibilities.  
Explication générale  
Ce test évalue le modèle de responsabilité partagée d'AWS. AWS est responsable de la « sécurité du cloud » (infrastructure physique, installations, matériel et services de base), tandis que les clients sont responsables de la « sécurité dans le cloud » (leurs données, la gestion des identités et des accès, la configuration du réseau et les choix de chiffrement). L'option D est correcte car la maintenance du matériel physique et l'exploitation des centres de données relèvent de la responsabilité d'AWS ; les autres options décrivent les responsabilités des clients.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 9Ignoré  
**Un développeur doit interagir avec AWS via l'interface de ligne de commande AWS (AWS CLI).**  
**Quelle fonctionnalité de sécurité ou quel service AWS doit être provisionné dans son compte pour répondre à ce besoin ?**  
A. Nom d'utilisateur et mot de passe

#### Explications

Un nom d'utilisateur et un mot de passe permettent uniquement de se connecter de manière interactive à la console de gestion AWS. L'interface de ligne de commande AWS (AWS CLI) requiert des informations d'identification programmées (clé d'accès/secret ou jetons temporaires) et non un simple mot de passe de console.  
B. Gestionnaire de systèmes AWS

#### Explications

AWS Systems Manager est une suite d'outils opérationnels (Session Manager, Parameter Store, Run Command) permettant de gérer les ressources ; il ne fournit pas lui-même les informations d'identification programmatiques nécessaires pour appeler les API AWS via l'interface de ligne de commande (CLI).  
C. Accès au mot de passe root

#### Explications

L'utilisation des identifiants du compte racine est fortement déconseillée. Bien que le compte racine puisse générer des identifiants par programmation, il est recommandé d'éviter complètement son utilisation et de privilégier les identités IAM ou les identifiants de rôles temporaires avec le principe du moindre privilège.  
**Bonne réponse**  
D. Clé d'accès AWS

#### Explications

L'interface de ligne de commande AWS (AWS CLI) requiert des informations d'identification programmatiques (un ID de clé d'accès et une clé d'accès secrète, ou des informations d'identification temporaires obtenues via un rôle IAM/STS) pour signer les requêtes d'API. Utilisez des utilisateurs ou des rôles IAM dotés de politiques appropriées et privilégiez les informations d'identification temporaires lorsque cela est possible.  
Explication générale  
L'interface de ligne de commande AWS (AWS CLI) effectue des appels d'API et requiert des informations d'identification par programmation pour signer ces requêtes. La méthode appropriée consiste à utiliser des clés d'accès ou, de préférence, des informations d'identification temporaires provenant d'un rôle IAM/STS ; le nom d'utilisateur et le mot de passe de la console ou Systems Manager ne répondent pas à cette exigence, et l'utilisation du compte racine est non sécurisée.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 10Ignoré  
**Quel service AWS fournit des ressources de calcul sans serveur pour une utilisation avec des conteneurs ?**  
A. Amazon Simple Queue Service (Amazon SQS)

#### Explications

Incorrect — Amazon SQS est un service de file d'attente de messages entièrement géré, utilisé pour découpler et mettre en mémoire tampon les composants d'une application. Il ne fournit aucun environnement de calcul et ne peut ni exécuter ni gérer de charges de travail conteneurisées.  
**Bonne réponse**  
B. AWS Fargate

#### Explications

Exact — Fargate est un moteur de calcul sans serveur pour conteneurs qui permet d'exécuter des conteneurs sans provisionner ni gérer d'instances EC2. Il s'intègre à Amazon ECS et Amazon EKS, gère le placement et la mise à l'échelle des tâches/pods, et facture en fonction des ressources vCPU et mémoire utilisées par tâche.  
C. AWS Elastic Beanstalk

#### Explications

Incorrect — Elastic Beanstalk est un service de déploiement d'applications qui automatise le provisionnement et l'orchestration. Bien qu'il puisse déployer des applications conteneurisées, il provisionne et gère généralement les ressources de calcul sous-jacentes (telles que EC2 ou ECS) pour votre compte, plutôt que de fournir un environnement d'exécution de conteneurs sans serveur.  
D. Amazon SageMaker

#### Explications

Incorrect — Amazon SageMaker is a managed machine learning platform for building, training, and deploying models. Although it may host models in containers, its purpose and features target ML workflows, not general-purpose serverless container compute for arbitrary applications.  
Explication générale  
This item tests which AWS service provides a serverless runtime for containers. Fargate is the correct choice because it abstracts EC2 instance management and runs container tasks/pods for ECS and EKS with per-task resource billing. The distractors are different service types: SQS is messaging, Elastic Beanstalk automates deployments but manages underlying compute, and SageMaker is focused on ML workloads.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 11Ignoré  
**A company wants to migrate petabytes of data from its on-premises data center to AWS. The company does not want to use an internet connection to perform the migration.**  
**Which AWS service will meet these requirements?**  
A. AWS DataSync

#### Explications

DataSync is a network-based service for automated, accelerated transfers between on‑premises storage and AWS (supports NFS/SMB and S3 endpoints and can run over Direct Connect). It requires a network path and is not designed for offline, petabyte/exabyte-scale migrations where physical transport is preferred.  
B. Amazon Connect

#### Explications

Amazon Connect is a cloud contact-center service for customer interactions. It is unrelated to bulk data migration and does not provide mechanisms for moving large datasets to AWS.  
**Bonne réponse**  
C. AWS Snowmobile

#### Explications

Provides an offline, large-capacity physical transport solution built for extremely large migrations (petabyte to exabyte scale). Data is loaded into a ruggedized container, encrypted during transit with AWS-managed key controls, transported to AWS, and ingested into AWS storage—eliminating the need to transfer over an internet connection.  
D. AWS Direct Connect

#### Explications

Direct Connect offers a private, dedicated network connection to AWS that improves bandwidth and latency compared to the public internet. However, it is still a network transfer method (not a physical offline shipment) and becomes impractical for very large, petabyte-scale one‑time migrations due to transfer time and cost.  
Explication générale  
The question requires migrating petabytes without using an internet connection. The correct choice is the physical, offline transport designed for extremely large datasets with secure, encrypted handling and AWS ingestion. The other options are either network-based (suitable for ongoing or smaller transfers) or unrelated services, so they do not meet the offline, petabyte-scale requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 12Ignoré  
**A company is in the early stages of planning a migration to AWS. The company wants to obtain the monthly predicted total AWS cost of ownership for future Amazon EC2 instances and associated storage.**  
**Which AWS service or tool should the company use to meet these requirements?**  
**Bonne réponse**  
A. AWS Pricing Calculator

#### Explications

The AWS pricing-estimation web tool provides configurable, service-level pricing models and can produce monthly and annual cost breakdowns. It lets you specify EC2 instance families, instance sizes, VPC/networking, EBS volumes and IOPS, data transfer, reserved instance or Savings Plan options, and outputs predicted monthly totals for compute and storage to support migration budgeting.  
B. AWS Compute Optimizer

#### Explications

This service analyzes historical utilization (CloudWatch metrics) to recommend right-sizing, instance family changes, and potential cost savings for existing resources. It does not produce forward-looking, month-by-month cost forecasts for planned deployments or full TCO estimates required during initial migration planning.  
C. AWS Trusted Advisor

#### Explications

The Advisor service runs best-practice checks across security, fault tolerance, performance and cost optimization and provides recommendations and limited cost-savings estimates. It is advisory in nature and does not create detailed predicted monthly cost models for future EC2/storage configurations.  
D. AWS Application Migration Service

#### Explications

The migration automation service streamlines lift-and-shift migrations by replicating servers and orchestrating cutover. Its focus is migration execution and server conversion, not producing detailed cost-of-ownership forecasts or monthly pricing predictions for planned infrastructure.  
Explication générale  
This question tests knowledge of AWS tools for financial planning. The correct choice is the AWS cost-estimation tool because it is designed to model and output predicted monthly costs for EC2 and associated storage based on configurable inputs. The other options provide optimization recommendations, best-practice checks, or migration automation, but do not generate detailed, forward-looking monthly cost estimates for planned deployments.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 13Ignoré  
**Which AWS service or resource can identify and provide reports on IAM resources in one AWS account that is shared with another AWS account?**  
A. IAM credential report

#### Explications

The IAM credential report documents the status of user credentials (passwords, access keys, MFA) for IAM users in a single account. It does not analyze resource-based policies or identify principals in other accounts that have access to resources, so it cannot report on cross-account resource sharing.  
B. AWS IAM Identity Center (AWS Single Sign-On)

#### Explications

IAM Identity Center centralizes user sign-in and assigns permissions sets across AWS accounts but is focused on authentication and authorization workflows (SSO, permission sets) rather than analyzing resource-based policies or producing cross-account access findings.  
**Bonne réponse**  
C. AWS Identity and Access Management Access Analyzer

#### Explications

Access Analyzer evaluates resource-based policies and generates findings that show which external principals (including other AWS accounts) can access your resources. It supports continuous monitoring and analyzers at the account or organization level, and identifies cross-account access for resources such as S3 buckets, KMS keys, IAM roles and other supported resource types, making it the appropriate tool for this task.  
D. Amazon Cognito user pool

#### Explications

Amazon Cognito user pools handle application-level user directories and authentication for apps. They are unrelated to AWS account IAM resource policies and do not provide analysis or reports of cross-account IAM resource sharing.  
Explication générale  
The question tests identification of a service that detects and reports cross-account access. AWS IAM Access Analyzer inspects resource-based policies and produces findings that reveal when resources are shared with external principals or other AWS accounts. The other choices either report only on credentials (credential report), provide SSO/permission management (IAM Identity Center), or manage application user identities (Cognito), none of which perform cross-account resource access analysis.  
Domaine  
Domain 2: Security and Compliance  
Question 14Ignoré  
**Which AWS service or tool can provide rightsizing recommendations for Amazon EC2 resources at no additional cost?**  
A. AWS Well-Architected Tool

#### Explications

The Well-Architected Tool provides a framework and review templates to evaluate workloads against AWS best practices across the five pillars. It produces improvement plan items and guidance, but it does not generate automated, usage-based EC2 rightsizing recommendations.  
B. Amazon CloudWatch

#### Explications

CloudWatch collects and visualizes metrics, logs, and alarms for resources and applications. While it provides the telemetry needed to assess utilization, it does not itself produce automated EC2 rightsizing recommendations — that analysis is performed by services like Cost Explorer or Compute Optimizer.  
**Bonne réponse**  
C. AWS Cost Explorer

#### Explications

Cost Explorer analyzes historical cost and usage data and includes a Rightsizing Recommendations feature that examines EC2 utilization patterns and suggests instance size/family changes and termination opportunities. This functionality is available through the AWS billing tools at no additional charge and is designed specifically to help reduce cost by matching instance types to workload needs.  
D. Amazon S3 analytics

#### Explications

S3 Storage Class Analysis (S3 analytics) examines object access patterns to recommend storage class transitions for S3 objects. It is focused on storage optimization and does not provide recommendations for EC2 instance sizing or compute resources.  
Explication générale  
The question tests knowledge of AWS cost-optimization tools. Cost Explorer (via the billing console) provides built-in rightsizing recommendations for EC2 by analyzing historical usage and suggesting instance size/family changes or terminations at no extra cost. Other offerings — the Well-Architected Tool, CloudWatch, and S3 analytics — serve architecture reviews, monitoring/telemetry, and storage optimization respectively and do not produce the same automated EC2 rightsizing recommendations (though Compute Optimizer is another AWS service that provides advanced size recommendations).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 15Ignoré  
**Which AWS service should a company use to organize, characterize, and search large numbers of images?**  
A. Amazon Transcribe

#### Explications

Amazon Transcribe is a managed automatic speech recognition (ASR) service for converting spoken audio into text. It does not provide image analysis, labeling, face detection, or image-search capabilities required to organize and search large image collections.  
**Bonne réponse**  
B. Amazon Rekognition

#### Explications

Amazon Rekognition provides pre-trained APIs and features for extracting metadata from images and videos (label detection, face detection, face collections and search, custom labels, and content moderation). It integrates with S3 for large-scale storage and indexing, enabling automated characterization and searchable image catalogs at scale.  
C. Amazon Aurora

#### Explications

Amazon Aurora is a high-performance, managed relational database (MySQL‑ and PostgreSQL‑compatible). While it can store image metadata or pointers, it does not perform visual analysis or provide built-in image-search/indexing features.  
D. Amazon QuickSight

#### Explications

Amazon QuickSight is a business intelligence and visualization service for creating dashboards and insights from data sources. It is not an image-analysis or image-search service, though it can visualize metadata extracted by other services.  
Explication générale  
This question tests mapping use cases to AWS services for image analysis and search. The correct service is Rekognition because it extracts visual metadata (labels, faces, custom models) and supports indexing/search workflows for large image sets. The other options are for audio transcription (Transcribe), relational databases (Aurora), or analytics/visualization (QuickSight), and therefore do not natively provide the image-analysis and search capabilities required.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 16Ignoré  
**A company wants a time-series database service that makes it easier to store and analyze trillions of events each day.**  
**Which AWS service will meet this requirement?**  
A. Amazon Neptune

#### Explications

Amazon Neptune is a managed graph database optimized for storing and querying highly connected data using graph models (Gremlin, SPARQL). It is not a purpose-built time-series database and does not provide time-series-specific ingestion scaling, tiered storage, or query functions required for handling trillions of time-stamped events per day.  
**Bonne réponse**  
B. Amazon Timestream

#### Explications

Amazon Timestream is a purpose-built, serverless time-series database optimized for time-stamped data. It provides automatic scaling, built-in time-series query and aggregation functions, and tiered storage (in-memory and magnetic) with data-retention policies to efficiently ingest and query very large volumes of events (integration with Kinesis/IoT/CloudWatch is common). These capabilities make it the appropriate choice for storing and analyzing trillions of events daily.  
C. Amazon Forecast

#### Explications

Amazon Forecast is a machine learning service that creates forecasts from historical time-series data. It is designed for predictive modeling (demand forecasting, capacity planning) rather than as a scalable, managed data store for ingesting and querying trillions of raw time-series events.  
D. Amazon DocumentDB (with MongoDB compatibility)

#### Explications

Amazon DocumentDB is a managed document (JSON) database compatible with MongoDB workloads. It is intended for document-oriented applications and is not optimized with time-series-specific storage tiers, query functions, or serverless scaling geared toward ingesting and analyzing very large volumes of time-stamped events.  
Explication générale  
The question targets a service designed for large-scale time-series data. Amazon Timestream is the correct choice because it is purpose-built for time-stamped data with serverless scaling, time-series query primitives, and tiered storage to handle massive ingestion and analysis. The other options (Neptune, Forecast, DocumentDB) serve graph queries, forecasting ML, and document storage respectively, and do not provide the time-series storage, scaling, and query optimizations that Timestream offers.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 17Ignoré  
**A company plans to migrate its application from on premises to the AWS Cloud. The company needs to gather usage and configuration data for the application components.**  
**Which AWS service will meet these requirements?**  
A. AWS Database Migration Service (AWS DMS)

#### Explications

AWS Database Migration Service is specialized for migrating and replicating databases to AWS (continuous or one-time data replication). It does not perform application component inventory, configuration profiling, or dependency mapping required for migration planning, so it does not meet the discovery requirement.  
B. AWS Transfer Family

#### Explications

AWS Transfer Family is a managed service for transferring files over protocols such as SFTP, FTPS, and FTP. It handles file transfer endpoints and authentication, but it does not collect usage metrics, configuration details, or dependency information about on‑premises application components.  
**Bonne réponse**  
C. AWS Application Discovery Service

#### Explications

AWS Application Discovery Service is designed to collect on‑premises inventory, configuration, performance, and dependency data to support migration planning. It can use agents or agentless collectors to capture system attributes (CPU, memory, disk, network), running processes, and inter‑server connections, and it integrates with migration tools and Migration Hub to size and plan target deployments in AWS—addressing the stated requirements.  
D. AWS Global Accelerator

#### Explications

AWS Global Accelerator is a networking service that improves availability and performance by routing user traffic to optimal AWS endpoints using static Anycast IPs. It does not provide tools for discovering on‑premises application configuration, usage metrics, or dependency mapping, so it is not applicable for migration data collection.  
Explication générale  
The question tests knowledge of AWS migration discovery tooling. The correct choice is the service purpose‑built to inventory and profile on‑premises environments (collecting configuration, utilization, and dependency data) to support migration planning. The other options are AWS services with different purposes—database migration, file transfer, and traffic acceleration—and therefore do not satisfy the requirement to gather application usage and configuration data.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 18Ignoré  
**Une entreprise possède une base de données MariaDB hébergée sur site. Elle souhaite migrer ces données vers le cloud AWS.**  
**Quel service AWS permettra d'héberger cette base de données avec le moins de coûts opérationnels ?**  
**Bonne réponse**  
A. Amazon RDS

#### Explications

Amazon RDS est un service de base de données relationnelle géré qui prend en charge nativement MariaDB. Il automatise les tâches opérationnelles courantes (sauvegardes automatisées, correctifs logiciels, multi-AZ pour une haute disponibilité, basculement automatique, surveillance (CloudWatch) et options de mise à l'échelle verticale/horizontale), ce qui réduit considérablement la charge administrative par rapport à l'exécution et à la maintenance d'une base de données autogérée sur EC2.  
B. Amazon Neptune

#### Explications

Amazon Neptune est un service de base de données graphiques géré, optimisé pour les charges de travail de type graphes de propriétés (Apache TinkerPop/Gremlin) et RDF (SPARQL). Son modèle de données et ses langages de requêtes sont conçus pour le parcours de graphes et non pour le SQL relationnel ; il ne convient donc pas comme solution de remplacement directe pour une base de données relationnelle MariaDB.  
C. Amazon S3

#### Explications

Amazon S3 est un service de stockage d'objets à haute durabilité conçu pour stocker des fichiers, des sauvegardes et des objets statiques. Il ne fournit pas de moteur de base de données ni de fonctionnalités de requêtes SQL pour les charges de travail relationnelles transactionnelles ; il peut stocker des sauvegardes de bases de données, mais ne peut pas héberger une instance MariaDB active.  
D. Amazon DynamoDB

#### Explications

Amazon DynamoDB est une base de données NoSQL clé-valeur et document entièrement gérée, offrant une mise à l'échelle sans serveur et une faible charge opérationnelle. Cependant, son modèle de données, ses modèles de requêtes et sa sémantique transactionnelle diffèrent de ceux d'un SGBD relationnel ; par conséquent, elle ne peut pas remplacer directement un schéma MariaDB existant sans une refonte importante.  
Explication générale  
Cette question évalue vos connaissances sur les offres de bases de données managées d'AWS et sur celle qui minimise la charge opérationnelle d'un moteur relationnel. Le service relationnel managé offre une automatisation intégrée pour les sauvegardes, les correctifs, la disponibilité et la mise à l'échelle, et prend explicitement en charge MariaDB, ce qui en fait la solution idéale. Les autres options sont des services spécialisés (bases de données graphiques, stockage objet, NoSQL) qui ne proposent pas de moteur relationnel MariaDB natif et ne conviennent donc pas comme solutions d'hébergement à faible surcharge pour une base de données MariaDB existante.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 19Ignoré  
**Un utilisateur AWS souhaite détecter de manière proactive toute compromission potentielle d'une instance ou d'un compte, ou toute menace d'attaque.**  
**Quel service AWS doit-il choisir ?**  
**Bonne réponse**  
A. Amazon GuardDuty

#### Explications

Ce système assure une détection continue des menaces au niveau du compte en analysant les journaux de flux VPC, les événements de gestion AWS CloudTrail et les journaux DNS. Il utilise l'apprentissage automatique et la détection d'anomalies pour identifier les problèmes (instances compromises, activité API inhabituelle, utilisation abusive d'identifiants) et s'intègre à EventBridge et Security Hub pour la génération d'alertes et la réponse automatisée, ce qui en fait la solution idéale pour la détection proactive.  
B. AWS WAF

#### Explications

A web-application firewall inspects and filters HTTP/HTTPS traffic to protect applications (e.g., CloudFront, ALB) from exploits like SQL injection or XSS. It does not analyze account telemetry (CloudTrail) or VPC Flow Logs for behavioral indicators of compromise across instances or IAM activity, so it isn’t a general proactive threat-detection service.  
C. AWS Shield

#### Explications

Provides DDoS mitigation (Shield Standard/Advanced) to protect against volumetric and protocol attacks at the network/edge layer. Its focus is availability and attack mitigation, not continuous behavioral analysis of account or instance activity for signs of compromise.  
D. Amazon Inspector

#### Explications

Performs vulnerability and configuration assessments (scanning images, instances, and workloads) to identify CVEs and deviations from best practices. Useful for vulnerability management, but it does not provide continuous, real-time behavioral threat detection across account telemetry.  
Explication générale  
This item tests recognition of AWS security services and their purposes. The correct choice is the service that provides continuous, behavior-based threat detection by analyzing CloudTrail, VPC Flow Logs, and DNS logs and producing actionable findings. The distractors protect at the web layer (WAF), mitigate DDoS (Shield), or perform vulnerability assessments (Inspector), none of which deliver the same continuous account-level threat detection.  
Domaine  
Domain 2: Security and Compliance  
Question 20Ignoré  
**Which action is a security best practice for access to sensitive data that is stored in an Amazon S3 bucket?**  
A. Enable S3 Cross-Region Replication (CRR) on the S3 bucket.

#### Explications

Incorrect. Cross-Region Replication (CRR) is designed to copy objects between S3 buckets in different AWS Regions for durability, compliance, or locality; it does not provide authentication, authorization, or access-control capabilities for who can read or write objects in the source bucket.  
**Bonne réponse**  
B. Use IAM roles for applications that require access to the S3 bucket.

#### Explications

Correct. Assigning IAM roles gives applications temporary, automatically rotated credentials (via STS) and enables least-privilege permission scoping (instance profiles, ECS task roles, Lambda execution roles). This avoids embedded long‑term credentials and works together with bucket policies, IAM policies, S3 Block Public Access, and AWS KMS to enforce secure access to sensitive S3 data.  
C. Configure AWS WAF to prevent unauthorized access to the S3 bucket.

#### Explications

Incorrect. AWS WAF is a web application firewall that filters HTTP/S requests at CloudFront, API Gateway, or an Application Load Balancer; it does not manage S3 API permissions. While WAF can protect web-facing endpoints that serve S3 content through CloudFront/ALB, it is not an S3 access control mechanism.  
D. Configure Amazon GuardDuty to prevent unauthorized access to the S3 bucket.

#### Explications

Incorrect. Amazon GuardDuty is a threat-detection service that analyzes logs (CloudTrail, VPC Flow Logs, DNS) and produces findings for suspicious activity; it is detective and alerting-focused and does not itself prevent or enforce S3 access permissions.  
Explication générale  
The question tests secure access control for S3. The best practice is to use IAM roles so applications obtain temporary, least-privilege credentials rather than embedding long-lived keys. Other choices address different concerns: CRR handles replication, WAF filters web traffic at the edge, and GuardDuty detects threats — none are primary mechanisms for controlling S3 access.  
Domaine  
Domain 2: Security and Compliance  
Question 21Ignoré  
**A company purchased Amazon EC2 Standard Reserved Instances (RIs) for a workload in the AWS Cloud. The company needs to move part of the workload to an instance family that does not match the instance family of these Standard RIs.**  
**How can the company take advantage of the Standard RIs that it no longer needs?**  
A. Contact the AWS Support team, and ask the team to sell the Standard RIs

#### Explications

AWS Support cannot list or sell Reserved Instances on behalf of a customer. Selling an unused Standard RI is a self-service transaction that the account owner performs through the EC2 Reserved Instance Marketplace; Support may advise but does not execute marketplace listings.  
**Bonne réponse**  
B. Sell the Standard RIs on the Amazon EC2 Reserved Instance Marketplace

#### Explications

The EC2 Reserved Instance Marketplace is the AWS service designed for customers to list unused Standard Reserved Instances for sale to other AWS customers. Listing recoveries the remaining monetary value of the commitment when the original purchaser no longer needs that instance family, subject to the marketplace eligibility requirements.  
C. Sell the Standard RIs as a third-party seller on the AWS Marketplace

#### Explications

AWS Marketplace is a catalog for third-party software, AMIs, and SaaS offerings — it is not the platform to resell EC2 Reserved Instances. RIs must be sold via the EC2 Reserved Instance Marketplace rather than the general AWS Marketplace.  
D. Convert the Standard RIs to Savings Plans

#### Explications

Savings Plans are a separate pricing commitment purchased independently and cannot be created by converting existing Standard Reserved Instances. Convertible RIs can be exchanged for different instance attributes, but Standard RIs have limited modification options and must be sold if you need a different instance family.  
Explication générale  
This question tests how to recoup value from unused Standard EC2 Reserved Instances. The correct action is to list eligible Standard RIs on the Amazon EC2 Reserved Instance Marketplace so other customers can buy the remaining term. AWS Support cannot perform the sale, AWS Marketplace is for software products (not RIs), and Standard RIs cannot be converted into Savings Plans (Convertible RIs offer exchange flexibility but are a different product).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 22Ignoré  
**A library wants to automate the classification of electronic books based on the contents of the books.**  
**Which AWS service should the library use to meet this requirement?**  
A. Amazon Redshift

#### Explications

Redshift is a petabyte-scale data warehouse for analytic queries (OLAP). It stores and queries large structured datasets but does not provide natural language processing or document classification capabilities; you would use an NLP service to classify text and could store results in Redshift instead.  
B. Amazon CloudSearch

#### Explications

CloudSearch is a managed search/indexing service designed to provide full-text search and simple ranking/faceting. It indexes text for retrieval and search relevance but does not perform ML-based document classification or provide NLP features like entity extraction or custom classifiers.  
**Bonne réponse**  
C. Amazon Comprehend

#### Explications

This service offers managed natural language processing APIs including pre-built and custom document classification, entity and key-phrase extraction, sentiment analysis, and batch or real-time processing. It can be trained with labeled examples, integrates with S3/Lambda for pipelines, and returns confidence scores—making it suitable for automated classification of book contents.  
D. Amazon Aurora

#### Explications

Aurora is a MySQL- and PostgreSQL-compatible relational database engine optimized for transactional workloads. It is used to store structured data with high availability and performance, not to perform text analysis or machine learning-based classification.  
Explication générale  
The task requires an AWS service that performs natural language processing and document classification. The correct choice provides managed NLP APIs (including custom document classification and batch processing) suitable for analyzing book contents. The other options are data storage or search services that either index/retrieve text or store results but do not perform ML-based text classification.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 23Ignoré  
**An external auditor has requested that a company provide a list of all its IAM users, including the status of users' credentials and access keys.**  
**What is the SIMPLEST way to provide this information?**  
A. Create an IAM user account for the auditor, granting the auditor administrator permissions.

#### Explications

Incorrect. Creating an IAM user with administrator permissions grants excessive privileges and violates the principle of least privilege. It also does not directly produce the requested, machine-readable list of credential statuses; granting broad access to an auditor is a security risk compared with exporting an audit report.  
B. Take a screenshot of each user's page in the AWS Management Console, then provide the screenshots to the auditor.

#### Explications

Incorrect. Screenshots are manual, error-prone, and not machine-readable. They do not scale for many users, can omit metadata (timestamps, last-used data), and are unsuitable for formal auditing or automatic analysis.  
**Bonne réponse**  
C. Download the IAM credential report, then provide the report to the auditor.

#### Explications

Correct. The IAM credential report is a built-in, machine-readable CSV that lists all IAM users and fields such as password\_enabled, password\_last\_used, password\_last\_changed, access\_key\_1\_active, access\_key\_1\_last\_used\_date, etc. It can be generated from the IAM console or via the AWS CLI (aws iam generate-credential-report and aws iam get-credential-report) and is the simplest secure way to provide the auditor with the requested credential and access key status.  
D. Download the AWS Trusted Advisor report, then provide the report to the auditor.

#### Explications

Incorrect. AWS Trusted Advisor provides best-practice checks and recommendations (and some security checks) but does not produce a per-user credential status listing. It is not designed to export detailed IAM user credential metadata required by auditors.  
Explication générale  
Use the IAM credential report: it is the simplest, secure, and auditable way to provide a complete, machine-readable list of IAM users and their credential/access-key statuses. Alternative approaches (creating an admin user for the auditor, screenshots, or Trusted Advisor) either grant excessive access, are impractical, or do not contain the required per-user credential details.  
Domaine  
Domain 2: Security and Compliance  
Question 24Ignoré  
**Which AWS services can host PostgreSQL databases?**  
**(Choose two.)**  
A. Amazon S3

#### Explications

Amazon S3 is an object storage service offering highly durable, scalable storage for files and backups. It does not provide a managed relational database engine or the transactional, queryable storage semantics required to run PostgreSQL.  
**Sélection correcte**  
B. Amazon Aurora

#### Explications

Amazon Aurora (as part of Amazon RDS) provides a managed, PostgreSQL-compatible relational database engine with features such as automated backups, automated patching, read replicas, Multi-AZ fault tolerance, and storage autoscaling—making it a supported and fully managed option for PostgreSQL workloads.  
**Sélection correcte**  
C. Amazon EC2

#### Explications

Amazon EC2 supplies raw compute and networking resources where you can install and operate PostgreSQL yourself. This IaaS approach gives full control over database configuration, versioning, patching, and backups, but also places operational responsibilities (maintenance, replication, scaling) on the customer.  
D. Amazon OpenSearch Service

#### Explications

Amazon OpenSearch Service is a managed search and analytics service (based on the OpenSearch/Elasticsearch engines) optimized for indexing and full‑text search, log analytics, and monitoring. It is not a relational database engine and is not suitable for running PostgreSQL.  
E. Amazon Elastic File System (Amazon EFS)

#### Explications

Amazon EFS is a managed NFS file system that provides shared file storage for EC2 and other services. While it can store database files, it does not provide a database engine or the I/O characteristics and transactional guarantees expected for production PostgreSQL deployments; databases are typically hosted on RDS/Aurora or on EC2 with local or block storage.  
Explication générale  
The question tests where PostgreSQL can be run on AWS. Amazon Aurora (RDS) offers a fully managed, PostgreSQL‑compatible relational engine with automated management features, and Amazon EC2 lets you install and manage PostgreSQL yourself. The other options are storage or analytics services (S3, EFS, OpenSearch) that do not provide a PostgreSQL database engine and therefore are not appropriate choices.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 25Ignoré  
**Which AWS service can run a managed PostgreSQL database that provides online transaction processing (OLTP)?**  
A. Amazon DynamoDB

#### Explications

DynamoDB is a fully managed NoSQL key-value and document database that provides single-digit millisecond latency at scale and supports its own transactional API. It is not a relational engine and does not run PostgreSQL or provide SQL-based OLTP with PostgreSQL features (ACID in a relational engine, PostgreSQL extensions, SQL dialect).  
B. Amazon Athena

#### Explications

Athena is a serverless interactive query service for analyzing data stored in Amazon S3 (using Presto/Trino). It is designed for ad-hoc analytics/OLAP over object data, not for hosting or managing a continuously running relational OLTP database such as PostgreSQL.  
**Bonne réponse**  
C. Amazon RDS

#### Explications

Amazon RDS is the managed relational database service that provisions and operates relational engines (including PostgreSQL). It automates tasks such as provisioning, patching, backups, Multi-AZ failover, and read replicas, and is intended for transactional (OLTP) workloads using PostgreSQL-compatible engines.  
D. Amazon EMR

#### Explications

EMR is a managed big-data platform for running frameworks like Hadoop, Spark, and Hive for large-scale data processing and analytics. It is built for batch and stream processing/analytics rather than providing a managed relational PostgreSQL OLTP database.  
Explication générale  
The question tests which AWS service provides a managed PostgreSQL relational database suitable for OLTP. Amazon RDS is the appropriate choice because it offers managed PostgreSQL engines with automated operational tasks and features required by transactional applications. The other options are either NoSQL (DynamoDB), serverless analytics over S3 (Athena), or big-data processing platforms (EMR), none of which provide a managed PostgreSQL OLTP database.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 26Ignoré  
**A company is using AWS for all its IT infrastructure. The company's developers are allowed to deploy applications on their own. The developers want to deploy their applications without having to provision the infrastructure themselves.**  
**Which AWS service should the developers use to meet these requirements?**  
A. AWS CloudFormation

#### Explications

CloudFormation is an infrastructure-as-code service that provisions and manages AWS resources via templates (stacks). It requires authorship and maintenance of resource definitions (networks, compute, load balancers, etc.), so it does not remove the need for developers to provision or manage underlying infrastructure when deploying applications.  
B. AWS CodeBuild

#### Explications

CodeBuild is a fully managed continuous integration build service that compiles source code, runs tests, and produces artifacts. It does not provide a runtime platform or automatically provision and manage the application environment for deployments.  
**Bonne réponse**  
C. AWS Elastic Beanstalk

#### Explications

Elastic Beanstalk is a Platform-as-a-Service offering that lets developers upload application code while AWS provisions and manages underlying resources (EC2 instances, Auto Scaling groups, Elastic Load Balancers), handles capacity, health monitoring, and application updates—so developers can deploy without manually provisioning infrastructure.  
D. AWS CodeDeploy

#### Explications

CodeDeploy automates the process of deploying application revisions to targets (EC2, on-premises servers, ECS, Lambda) and supports deployment strategies (in-place, blue/green). It assumes target environments already exist and does not itself provision or manage the underlying infrastructure.  
Explication générale  
The question tests understanding of managed deployment platforms versus infrastructure provisioning and CI/CD tools. The correct choice is the PaaS that abstracts infrastructure so developers only supply application code; other options focus on infrastructure-as-code or build/deploy mechanics and therefore do not remove the need to provision or manage the runtime environment.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 27Ignoré  
**An administrator observed that multiple AWS resources were deleted yesterday.**  
**Which AWS service will help identify the cause and determine which user deleted the resources?**  
**Bonne réponse**  
A. AWS CloudTrail

#### Explications

CloudTrail provides a continuous, account-level record of API activity (management events and optionally data events) including who (IAM principal), what API call, when (timestamp), source IP, and request/response details. These logs can be queried via Event History, delivered to S3, analyzed with CloudTrail Lake, Athena, or forwarded to CloudWatch Logs to reconstruct deletion events and attribute them to a specific user or role.  
B. Amazon Inspector

#### Explications

Amazon Inspector performs automated security assessments of workloads (vulnerability and configuration assessments) to find software vulnerabilities and deviations from best practices. It does not provide an audit trail of API calls or identify which IAM user performed resource deletions.  
C. Amazon GuardDuty

#### Explications

Amazon GuardDuty is an intelligent threat detection service that analyzes data sources (e.g., VPC Flow Logs, DNS logs, and selected CloudTrail events) to surface suspicious activity. While it can flag anomalous or malicious behavior, it is not the primary source for a complete, queryable audit trail of all API calls needed to determine exactly which user deleted resources.  
D. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor delivers best-practice recommendations across cost, performance, security, fault tolerance, and service limits. It does not record or expose per-API-call audit logs or identify which IAM principal executed specific resource deletions.  
Explication générale  
To investigate who deleted resources, you need a service that records API-level activity with identity, timestamps, and request details. CloudTrail is the authoritative audit logging service that captures those events and supports querying or exporting logs for forensic analysis. The other options (Inspector, GuardDuty, Trusted Advisor) provide vulnerability assessment, threat detection, and best-practice recommendations respectively, but do not serve as the primary audit log for user-initiated API actions.  
Domaine  
Domain 2: Security and Compliance  
Question 28Ignoré  
**A company wants its AWS usage to be more sustainable. The company wants to track, measure, review, and forecast polluting emissions that result from its AWS applications.**  
**Which AWS service or tool can the company use to meet these requirements?**  
A. AWS Health Dashboard

#### Explications

The AWS Health Dashboard (and the AWS Health API) reports account- and service-level operational events, such as outages, scheduled changes, and advisories. It does not calculate or report greenhouse‑gas or carbon emissions metrics, so it cannot by itself track, measure, or forecast the company’s AWS-related polluting emissions.  
**Bonne réponse**  
B. AWS customer carbon footprint tool

#### Explications

The AWS Customer Carbon Footprint Tool analyzes your AWS usage/billing data and applies energy- and region-specific emissions factors and consumption models to produce estimates, historical breakdowns, and forecasts of carbon emissions attributable to your AWS workloads. It supports filtering and aggregation by account, service, and region, making it the appropriate tool for tracking, measuring, reviewing, and forecasting emissions from AWS usage.  
C. AWS Support Center

#### Explications

The AWS Support Center (and AWS Support cases) provide technical assistance, guidance, and access to support engineers. While Support can help with troubleshooting and best-practice guidance, it does not provide built-in carbon-emissions measurement or forecasting capabilities.  
D. Amazon QuickSight

#### Explications

Amazon QuickSight is a business intelligence and data-visualization service. It can visualize and analyze emissions data if you export or ingest those metrics from another source, but it does not generate emissions estimates or forecasts natively — it’s for reporting and dashboards, not for calculating AWS carbon footprints.  
Explication générale  
Use the AWS Customer Carbon Footprint Tool because it is specifically designed to estimate, break down, and forecast emissions associated with your AWS usage by leveraging billing/usage data and regional emissions factors. The other options serve different purposes: the Health Dashboard reports operational events, Support provides technical assistance, and QuickSight is a visualization tool that can display emissions data but does not compute it.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 29Ignoré  
**Which of the following can the AWS Pricing Calculator do?**  
**Bonne réponse**  
A. Project monthly AWS costs.

#### Explications

Le calculateur de prix AWS est un outil de planification qui génère des estimations de coûts service par service à partir des configurations et des hypothèses d'utilisation fournies par l'utilisateur. Il produit des estimations détaillées (mensuelles et/ou initiales), prend en charge les dimensions de tarification courantes (calcul, stockage, transfert de données, etc.) et vous permet d'exporter ou d'enregistrer les estimations pour la budgétisation et la planification de l'architecture.  
B. Calculer les coûts historiques d'AWS.

#### Explications

Incorrect : l’analyse des dépenses historiques nécessite l’accès aux données de facturation réelles. AWS Cost Explorer, la console de gestion des coûts et de la facturation, ainsi que le rapport sur les coûts et l’utilisation fournissent une analyse historique des coûts et de l’utilisation ; le calculateur de prix ne génère que des estimations prévisionnelles à partir des données que vous fournissez.  
C. Fournir des informations détaillées sur les stratégies de tarification d'AWS.

#### Explications

Incorrect : le calculateur affiche une estimation des coûts pour les services et options sélectionnés, mais ne fournit pas d’indications détaillées sur les stratégies de tarification ni sur les décisions d’optimisation. Pour connaître les modèles de tarification, les bonnes pratiques et les recommandations d’optimisation, consultez la documentation AWS Pricing, le pilier « Optimisation des coûts bien architecturé » ou les services de support et de conseil AWS.  
D. Donner aux utilisateurs l'accès à leurs factures mensuelles.

#### Explications

Incorrect : les factures mensuelles sont uniquement disponibles via la console AWS Billing & Cost Management et les rapports associés (factures, rapports de coûts et d’utilisation). Le calculateur de prix ne peut pas accéder aux enregistrements de facturation de votre compte ni afficher les factures réelles.  
Explication générale  
Cette question évalue vos connaissances des outils de calcul des coûts AWS. Le calculateur de prix AWS permet d'établir des estimations de coûts futurs en fonction des services sélectionnés et des hypothèses d'utilisation (réponse A). Il n'accède pas à l'historique de facturation du compte, ne l'analyse pas et n'émet pas de factures (ces fonctionnalités sont disponibles dans Cost Explorer et les services de gestion des coûts et de la facturation). De plus, il ne remplace pas les conseils en matière de tarification ni les services de conseil en optimisation.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 30Ignoré  
**Une entreprise possède une application qui génère des données non structurées en continu. Elle doit stocker ces données de manière à ce qu'elles soient pérennes et facilement interrogeables.**  
**Quel service AWS peut-elle utiliser pour répondre à ces exigences ?**  
A. Amazon RDS

#### Explications

Une base de données relationnelle gérée est construite autour de schémas prédéfinis et de charges de travail transactionnelles basées sur SQL. Cette rigidité des schémas et les caractéristiques de mise à l'échelle typiques des moteurs relationnels la rendent peu adaptée à l'ingestion et au stockage de données non structurées (sans schéma) produites en continu.  
B. Amazon Aurora

#### Explications

Bien qu'il offre des performances et une durabilité élevées pour les charges de travail relationnelles, ce moteur demeure un système relationnel basé sur un schéma. Les flux continus d'attributs arbitraires ou évolutifs sont mieux gérés par des bases de données NoSQL à schéma flexible que par un cluster relationnel.  
C. Amazon QuickSight

#### Explications

Il s'agit d'un service de veille stratégique et de visualisation qui analyse les données provenant de systèmes de stockage ou de bases de données ; il ne fournit pas de stockage primaire et durable d'objets ou de documents pour une ingestion continue.  
**Bonne réponse**  
D. Amazon DynamoDB

#### Explications

A fully managed NoSQL document/key-value service with a flexible schema model, multi‑AZ replication for durability, and features that enable efficient queries (primary key access, Global/Local Secondary Indexes, PartiQL support, DynamoDB Streams, optional DAX caching). These capabilities make it well suited to durable storage and low-latency querying of continuously produced unstructured data.  
Explication générale  
The question tests knowledge of storage models for continuous unstructured data. A flexible-schema NoSQL service that provides managed durability, horizontal scaling, and indexing/query features is the correct choice. Relational engines require predefined schemas and are optimized for structured data, while analytics/visualization tools are consumers of stored data rather than storage solutions.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 31Ignoré  
**Which AWS service or feature can a user configure to limit network access at the subnet level?**  
A. AWS Shield

#### Explications

Incorrect — AWS Shield is a DDoS protection service (Shield Standard and Shield Advanced) that provides detection and mitigation for volumetric and protocol attacks and integrates with services like CloudFront and ELB. It does not offer subnet-level allow/deny packet filtering or per-subnet access control.  
B. AWS WAF

#### Explications

Incorrect — AWS WAF is a web application firewall that inspects and filters HTTP(S) requests at the application layer (Layer 7\) when associated with CloudFront, Application Load Balancer, or API Gateway. It is not designed to control network traffic at the VPC subnet level.  
**Bonne réponse**  
C. Network ACL

#### Explications

Correct — Network ACLs are stateless packet filters applied to subnets within a VPC. They evaluate numbered inbound and outbound rules, support explicit allow and deny entries, and require explicit rules for return traffic because they are stateless. This makes them the appropriate mechanism for limiting network access at the subnet level.  
D. Security group

#### Explications

Incorrect — Security groups are stateful virtual firewalls attached to network interfaces/instances. They operate at the instance (ENI) level, automatically allow return traffic, and support only allow rules. They do not provide subnet-level, stateless allow/deny filtering.  
Explication générale  
The question tests knowledge of AWS network security scope. To enforce access controls at the subnet level within a VPC you use a stateless, per-subnet mechanism that evaluates inbound and outbound rules (Network ACLs). Security groups control traffic at the instance/ENI level and are stateful; AWS WAF and Shield protect at the application and DDoS mitigation layers respectively, not at the subnet layer.  
Domaine  
Domain 2: Security and Compliance  
Question 32Ignoré  
**A user needs programmatic access to AWS resources through the AWS CLI or the AWS API.**  
**Which option will provide the user with the appropriate access?**  
A. Amazon Inspector

#### Explications

Incorrect — Amazon Inspector is a security assessment service that scans EC2 instances, container images, and Lambda functions for vulnerabilities and deviations from best practices. It does not provide credentials or a mechanism to authenticate and sign AWS CLI/API requests.  
**Bonne réponse**  
B. Access keys

#### Explications

Correct — IAM access keys (an access key ID and a secret access key) are credentials used to cryptographically sign programmatic requests made by the AWS CLI, SDKs, or direct API calls. Best practices include avoiding use of the root account, creating IAM users or, preferably, using IAM roles and temporary credentials (STS) where possible, rotating keys regularly, and restricting key permissions with least privilege.  
C. SSH public keys

#### Explications

Incorrect — SSH public keys authenticate users at the operating-system level for SSH access to EC2 instances (shell/OS access). They are not used to sign or authenticate AWS API or CLI calls.  
D. AWS Key Management Service (AWS KMS) keys

#### Explications

Incorrect — AWS Key Management Service (KMS) manages cryptographic keys for data encryption, signing, and key lifecycle. KMS keys control encryption operations and access to ciphertext but do not serve as user credentials to authenticate programmatic AWS API/CLI requests.  
Explication générale  
Programmatic access to AWS requires credentials that can sign API requests. IAM access keys (access key ID \+ secret access key) are the mechanism for long‑term programmatic access used by the AWS CLI and SDKs. However, security best practices favor IAM roles and temporary STS credentials or instance profiles over long‑lived access keys. The other options (Inspector, SSH keys, KMS) provide vulnerability scanning, OS-level login, and encryption/key management respectively and do not grant API/CLI authentication.  
Domaine  
Domain 2: Security and Compliance  
Question 33Ignoré  
**Which AWS services are supported by Savings Plans?**  
**(Choose two.)**  
**Sélection correcte**  
A. Amazon EC2

#### Explications

Compute Savings Plans and EC2 Instance Savings Plans provide discounted pricing in exchange for a committed dollar-per-hour spend. Compute Savings Plans apply broadly across instance families, regions, OS, and tenancy and cover instance-hour compute usage (and also apply to services such as AWS Fargate and Lambda), while EC2 Instance Savings Plans give deeper discounts when you commit to a specific instance family in a region. This is why EC2 compute is eligible under Savings Plans.  
B. Amazon RDS

#### Explications

Relational database services are not covered by Savings Plans. Instead, they use Reserved DB Instances or other database-specific pricing options (e.g., RDS Reserved Instances or on-demand billing) to obtain lower rates for long-term usage.  
**Sélection correcte**  
C. Amazon SageMaker

#### Explications

There are SageMaker Savings Plans that offer discounted SageMaker training and inference usage in exchange for a committed spend (measured in $/hour). These SageMaker-specific Savings Plans are separate from Compute Savings Plans and directly reduce SageMaker costs when a commitment is made.  
D. Amazon Redshift

#### Explications

Data warehouse services use their own reservation models rather than Savings Plans. Redshift offers reservation/reserved node pricing and other capacity-reservation mechanisms to secure lower rates, so it is not covered by Savings Plans.  
E. Amazon DynamoDB

#### Explications

No Savings Plan coverage exists for the NoSQL capacity models. DynamoDB pricing uses on‑demand and provisioned capacity modes (and related reserved capacity or autoscaling features) rather than Savings Plans, so it isn’t eligible.  
Explication générale  
Savings Plans are commit-to-spend pricing programs that reduce costs for eligible compute services. The two correct choices reflect that EC2 compute is covered by Compute and EC2 Instance Savings Plans and SageMaker has its own SageMaker Savings Plans. The other services listed (RDS, Redshift, DynamoDB) use their own reserved-instance/reserved-capacity or service-specific billing models and therefore are not covered by Savings Plans.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 34Ignoré  
**A company wants to run a NoSQL database on Amazon EC2 instances.**  
**Which task is the responsibility of AWS in this scenario?**  
A. Update the guest operating system of the EC2 instances.

#### Explications

Incorrect. When you run EC2 instances you are responsible for the instance’s guest operating system lifecycle — installing updates, applying OS patches, and hardening the OS. AWS provides tools (for example, AWS Systems Manager Patch Manager) to help automate this, but the customer must configure and execute those tasks for their instances.  
B. Maintain high availability at the database layer.

#### Explications

Incorrect. AWS provides infrastructure features (multiple Availability Zones, networking, and services) that enable high availability, but designing and operating database-level HA (replication, clustering, failover configuration, and testing) for a self-managed NoSQL database on EC2 is the customer’s responsibility. Alternatively, a managed service (Amazon RDS, Amazon DynamoDB) would shift more HA responsibilities to AWS.  
**Bonne réponse**  
C. Patch the physical infrastructure that hosts the EC2 instances.

#### Explications

Correct. Under the AWS shared responsibility model, AWS is responsible for the security and maintenance of the underlying physical infrastructure — the data center facilities, physical servers, network devices, hypervisor/host software, and firmware. This includes patching and maintaining that hardware and host-level software that runs and supports customer EC2 instances.  
D. Configure the security group firewall.

#### Explications

Incorrect. Security groups are a configurable virtual firewall applied to customer resources; customers define inbound/outbound rules and manage those security group configurations. AWS provides the security group service and enforces the rules, but it does not design or configure a customer’s security group rules on their behalf.  
Explication générale  
This question tests the AWS shared responsibility model. AWS is responsible for the physical infrastructure and host-level components (hardware, firmware, networking, hypervisor) that support EC2 instances — tasks such as patching that physical infrastructure fall to AWS. In contrast, customers are responsible for everything they install and configure on their EC2 instances (guest OS, database software, security group rules, and database-level high availability). Therefore the responsibility described is an AWS responsibility, making the infrastructure-patching choice correct.  
Domaine  
Domain 2: Security and Compliance  
Question 35Ignoré  
**A company has multiple AWS accounts. The company needs to receive a consolidated bill from AWS and must centrally manage security and compliance.**  
**Which AWS service or feature should the company use to meet these requirements?**  
A. AWS Cost and Usage Report

#### Explications

The Cost and Usage Report (CUR) delivers detailed usage and cost data for analysis and export, but it is a reporting tool only. It does not provide account management, consolidated billing setup across accounts (that is performed by Organizations), or mechanisms to centrally enforce security and compliance policies.  
**Bonne réponse**  
B. AWS Organizations

#### Explications

AWS Organizations is the management service that links multiple AWS accounts under a single management (formerly payer) account. It provides consolidated billing for member accounts and centralized governance features such as Organizational Units and Service Control Policies (SCPs) to enforce security and compliance controls across the organization.  
C. AWS Config

#### Explications

AWS Config records resource configurations, evaluates resource compliance, and can aggregate compliance data across accounts and regions with an Aggregator, but it is focused on configuration tracking and compliance reporting. It does not perform consolidated billing or handle account creation/organization-level policy enforcement for billing.  
D. AWS Security Hub

#### Explications

AWS Security Hub centralizes and prioritizes security findings from multiple AWS services and third-party products; it can be enabled across an organization for visibility. However, it does not manage account hierarchies or provide consolidated billing capabilities.  
Explication générale  
The requirement calls for a single service that both consolidates billing across multiple accounts and enables centralized security/compliance management. AWS Organizations meets both needs by linking accounts under a management account for consolidated billing and by providing governance controls (Organizational Units, Service Control Policies) to centrally enforce security and compliance. The other options (CUR, Config, Security Hub) provide reporting or security/compliance visibility but do not handle account-level billing and organizational policy management together.  
Domaine  
Domain 2: Security and Compliance  
Question 36Ignoré  
**A company is releasing a business-critical application. Before the release, the company needs strategic planning assistance from AWS. During the release, the company needs AWS infrastructure event management and real-time support.**  
**What should the company do to meet these requirements?**  
**(Choose two)**  
A. Access AWS Trusted Advisor

#### Explications

Incorrect. AWS Trusted Advisor is an automated best-practices checker that provides recommendations (cost optimization, security, fault tolerance, performance, and service limits). It does not provide hands-on strategic planning engagements, a Technical Account Manager, or AWS-run Infrastructure Event Management during a launch.  
B. Contact the AWS Partner Network (APN)

#### Explications

Incorrect. The AWS Partner Network (APN) includes independent consulting and technology partners that can deliver implementation and managed services. While APN partners may assist with planning or execution, they are third parties and do not provide AWS-managed support features such as a TAM or Infrastructure Event Management offered under AWS Enterprise Support.  
**Sélection correcte**  
C. Sign up for AWS Enterprise Support

#### Explications

Correct. AWS Enterprise Support offers 24/7 access to Cloud Support Engineers, escalation paths, and a designated Technical Account Manager (TAM) for proactive operational guidance. Enterprise customers can also engage Infrastructure Event Management (IEM) for planning and real-time support during major launches, making this service appropriate for in-release operational support.  
**Sélection correcte**  
D. Contact AWS Professional Services

#### Explications

Correct. AWS Professional Services is an AWS-operated consulting organization that provides strategic planning, architecture design workshops, runbook development, and hands-on pre-release assistance. It is suited to the pre-release strategic planning requirement and is commonly used together with Enterprise Support for operational coverage during the release.  
Explication générale  
The situation requires both pre-release strategic planning and live operational support during rollout. AWS Professional Services supplies the strategic, hands-on planning and architecture work before release, while AWS Enterprise Support (Enterprise level) provides 24/7 operational coverage, a TAM, and Infrastructure Event Management during the release. Trusted Advisor only gives automated recommendations, and APN partners are third-party providers and do not replace AWS-managed IEM/TAM capabilities.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 37Ignoré  
**A company acquired another corporation. The company now has two AWS accounts.**  
**Which AWS service or tool can the company use to consolidate the billing for these two accounts?**  
A. AWS Systems Manager

#### Explications

Incorrect. Systems Manager is an operations management service (automation, patching, inventory, Session Manager, Run Command) for administering compute resources; it does not provide account linking or centralized payment/billing features.  
**Bonne réponse**  
B. AWS Organizations

#### Explications

Correct. AWS Organizations provides account management with a management (formerly payer) account and member accounts, enabling consolidated billing so usage and charges from member accounts are aggregated under the management account for a single payment method and to enable volume pricing and consolidated cost reporting.  
C. AWS License Manager

#### Explications

Incorrect. License Manager is for tracking and enforcing software license usage (BYOL) across AWS and on-premises environments; it does not perform account linking or aggregate billing for multiple AWS accounts.  
D. Cost Explorer

#### Explications

Incorrect. Cost Explorer is a cost-analysis and visualization tool for understanding usage and spend (reports, graphs, forecasts); it analyzes billing data but does not link accounts or establish consolidated billing relationships — that is done via Organizations.  
Explication générale  
This item tests knowledge of AWS account and billing management. The correct solution is the account-management service that links multiple AWS accounts under a single management account to aggregate charges and payments. The other choices are operational, licensing, or cost-analysis tools that do not establish consolidated billing relationships.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 38Ignoré  
**A company has applications that control on-premises factory equipment.**  
**Which AWS service should the company use to run these applications with the LEAST latency?**  
**Bonne réponse**  
A. AWS Outposts

#### Explications

Verified correct. Outposts places AWS-managed compute and storage hardware inside the customer’s facility so AWS APIs, EC2/EBS-based instances, and container orchestration can run locally under AWS management. This removes cloud-region network hops and provides deterministic, low-latency access required for real-time equipment control and industrial automation.  
B. Amazon EC2

#### Explications

Incorrect. Amazon EC2 runs in AWS Regions and Availability Zones; communicating with on-premises equipment requires network traversal (even with Direct Connect), which adds latency and jitter that make it a poor choice for the lowest-latency, on-site control loops.  
C. AWS Lambda

#### Explications

Incorrect. AWS Lambda is a region-based, event-driven serverless service with cold-start behavior and execution model constraints; it is not designed for always-on, deterministic, low-latency control of local hardware and cannot be deployed on-premises in the same way Outposts can.  
D. AWS Fargate

#### Explications

Incorrect. AWS Fargate provides a serverless container runtime in AWS-managed cloud infrastructure. Because it does not provision compute on the customer’s premises, it cannot eliminate the network latency between cloud and local factory equipment.  
Explication générale  
This item tests choosing an AWS option for the strictest on-premises latency requirements. Outposts is the correct selection because it installs AWS-managed compute and storage at the customer site, eliminating round-trip network latency to AWS Regions. The other choices run in the cloud (EC2, Lambda, Fargate) and therefore introduce additional latency or are unsuitable for deterministic, continuous control of factory equipment.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 39Ignoré  
**Which AWS tool or feature acts as a VPC firewall at the subnet level?**  
A. Security group

#### Explications

Incorrect. Security groups are stateful virtual firewalls that attach to network interfaces (instances). They operate at the instance/ENI level, automatically allow return traffic, and only support allow rules — they do not function as a subnet-level firewall.  
**Bonne réponse**  
B. Network ACL

#### Explications

Correct. Network ACLs are stateless VPC components that apply to subnets. They evaluate numbered inbound and outbound rules (allow and deny) and affect all resources in the subnet. Because they are stateless, return traffic must be explicitly allowed by rules.  
C. Traffic Mirroring

#### Explications

Incorrect. VPC Traffic Mirroring is used to copy network traffic from ENIs to monitoring/inspection appliances for analysis or troubleshooting. It does not enforce or block traffic and therefore is not a firewall.  
D. Internet gateway

#### Explications

Incorrect. An Internet Gateway provides scalable, redundant connectivity between a VPC and the internet. It is a routing/attachment component and does not perform packet filtering; firewalling for internet traffic is enforced by security groups and NACLs.  
Explication générale  
This question tests knowledge of where firewall controls are applied in a VPC. Network ACLs operate at the subnet level and are stateless, allowing explicit allow/deny rules that affect all instances in a subnet. Security groups provide instance-level (stateful) filtering. Traffic Mirroring and Internet Gateways serve monitoring and connectivity roles respectively and do not act as subnet firewalls.  
Domaine  
Domain 2: Security and Compliance  
Question 40Ignoré  
**Which AWS services or features provide disaster recovery solutions for Amazon EC2 instances? (Choose two.)**  
A. EC2 Reserved Instances

#### Explications

Reserved Instances are a pricing/commitment construct that lowers hourly costs for EC2 capacity. They do not provide imaging, backup, snapshot, cross‑AZ/region copies, or automated recovery procedures needed to restore instances after a failure, so they are not a disaster recovery mechanism.  
**Sélection correcte**  
B. EC2 Amazon Machine Images (AMIs)

#### Explications

Amazon Machine Images capture an instance’s root volume, configuration, and metadata so you can launch identical replacement instances. AMIs can be copied across Availability Zones and regions and used in automated recovery runbooks to rebuild servers quickly during a DR event.  
**Sélection correcte**  
C. Amazon Elastic Block Store (Amazon EBS) snapshots

#### Explications

EBS snapshots provide point‑in‑time, incremental backups of block volumes. Snapshots can be used to restore volumes or create new volumes (and can be copied across regions), making them a core building block for data recovery and rebuilding EC2-backed storage.  
D. AWS Shield

#### Explications

AWS Shield is a managed DDoS protection service that defends network and application endpoints from volumetric and protocol attacks. It does not provide backups, images, or restore capabilities required for recovering EC2 instances after data loss or infrastructure failure.  
E. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat-detection and continuous security monitoring service that identifies suspicious activity. It improves security visibility and incident response but does not perform backups or provide mechanisms to restore instances or data for disaster recovery.  
Explication générale  
Effective DR for EC2 relies on image- and storage-level backups that let you rebuild instances and restore data: machine images provide consistent instance configurations for rapid relaunch, and EBS snapshots provide point‑in‑time volume recovery and cross‑region copy capability. Billing constructs and security services (Reserved Instances, Shield, GuardDuty) address cost optimization or protection/monitoring but do not supply the backup/restore mechanisms required for disaster recovery.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 41Ignoré  
**A company wants a web application to interact with various AWS services.**  
**Which AWS service or resource will meet this requirement?**  
A. AWS CloudShell

#### Explications

CloudShell is an interactive, browser-hosted shell intended for administrators and developers to run CLI commands and scripts. It is not designed to be the runtime or API surface for a web application to interact programmatically with AWS services.  
B. AWS Marketplace

#### Explications

AWS Marketplace is a catalog for discovering and procuring third-party software and services. It does not provide an interface or APIs for a customer's web application to interact with AWS services.  
**Bonne réponse**  
C. AWS Management Console

#### Explications

The AWS web-based management interface lets users perform actions across AWS services from a browser, so when the requirement is to use a web application (browser-based UI) to interact with AWS resources, this GUI-based interface meets that need. For backend programmatic integration, however, SDKs and service APIs are the typical approach.  
D. AWS CLI

#### Explications

The AWS Command Line Interface provides scriptable, command-line access to AWS APIs and is intended for automation and administrative tasks. It is not a web application interface and therefore is not the appropriate choice if the requirement specifically calls for a browser-based web application to interact with services.  
Explication générale  
This question tests recognition of AWS offerings that provide a browser-based web interface versus command-line or catalog solutions. The web-based management interface is the appropriate choice when the requirement is a web application (graphical browser UI) to interact with AWS services. The other options are either command-line tools (suitable for automation), catalogs, or admin shells and do not serve as a browser-based application interface. Note: for programmatic integration by an application (not a human-facing web UI), AWS SDKs or service APIs with proper IAM credentials are the recommended approach.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 42Ignoré  
**A company needs to organize its resources and track AWS costs on a detailed level. The company needs to categorize costs by business department, environment, and application.**  
**Which solution will meet these requirements?**  
A. Access the AWS Cost Management console to organize resources, set an AWS budget, and receive notifications of unintentional usage.

#### Explications

Incorrect — The Billing & Cost Management (Cost Management) console provides budgets, alerts (AWS Budgets) and cost visualizations (Cost Explorer), but it does not by itself create resource-level categorizations. Detailed cost attribution requires applying resource tags and activating them for cost allocation or using the Cost and Usage Report.  
**Bonne réponse**  
B. Use tags to organize the resources. Activate cost allocation tags to track AWS costs on a detailed level.

#### Explications

Correct — Applying consistent resource tags (for example: Department, Environment, Application) and activating those tags as cost allocation tags in the Billing console enables Cost Explorer and the Cost and Usage Report (CUR) to attribute costs at a detailed level. Enforce tagging via tag policies or automation to ensure complete and accurate cost reporting.  
C. Create Amazon CloudWatch dashboards to visually organize and track costs individually.

#### Explications

Incorrect — Amazon CloudWatch dashboards are for visualizing operational metrics, logs and alarms. They are not designed to produce detailed, tag-based billing or cost-allocation reports; use Cost Explorer or the CUR for billing breakdowns.  
D. Access the AWS Billing and Cost Management dashboard to organize and track resource consumption on a detailed level.

#### Explications

Incorrect — The Billing and Cost Management dashboard gives high-level cost overviews and links to cost tools, but it does not automatically categorize resources by department/application. Detailed breakdowns require activated cost allocation tags and use of Cost Explorer or the Cost and Usage Report.  
Explication générale  
Use resource tags and activate them as cost allocation tags so AWS cost tools (Cost Explorer and the Cost and Usage Report) can report costs by department, environment, and application. Console dashboards, CloudWatch, and budgets provide monitoring, metrics, and alerts but cannot produce detailed, resource-level cost allocation without tags enabled and properly applied.  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 43Ignoré  
**A company is using a central data platform to manage multiple types of data for its customers. The company wants to use AWS services to discover, transform, and visualize the data.**  
**Which combination of AWS services should the company use to meet these requirements?**  
**(Choose two.)**  
**Sélection correcte**  
A. AWS Glue

#### Explications

Provides a serverless data-integration platform with automated metadata discovery (crawlers) and the AWS Glue Data Catalog; offers ETL capabilities (Glue Studio, Spark-based Glue Jobs) to transform and prepare data for analytics and downstream services.  
B. Amazon Elastic File System (Amazon EFS)

#### Explications

A POSIX-compliant network file system for shared file storage (for EC2, ECS, Lambda). It is storage only and does not provide metadata discovery, ETL, or BI visualization features required by the scenario.  
C. Amazon Redshift

#### Explications

A columnar data warehouse optimized for large-scale analytics and complex queries. Useful for storing and analyzing transformed data, but not primarily a discovery or ETL service—typically used downstream of ETL tools like Glue.  
**Sélection correcte**  
D. Amazon QuickSight

#### Explications

A fully managed business-intelligence service for creating interactive dashboards and visualizations; integrates with AWS data sources (via the Glue Data Catalog, Athena, Redshift, S3) and is the appropriate service for the visualization requirement.  
E. Amazon Quantum Ledger Database (Amazon QLDB)

#### Explications

A purpose-built ledger database that provides an immutable, cryptographically verifiable journal for transactional integrity. It is not designed for general-purpose data discovery, transformation, or BI visualization.  
Explication générale  
The question targets the data lifecycle: discovery, transformation, and visualization. AWS Glue supplies automated discovery (crawlers, Data Catalog) and ETL capabilities to prepare data, while Amazon QuickSight provides the managed BI/visualization layer. The other options are storage (EFS), a data warehouse (Redshift) or a ledger (QLDB) and do not by themselves cover the full discover-\>transform-\>visualize workflow.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 44Ignoré  
**Which benefit is always free of charge with AWS, regardless of a user’s AWS Support plan?**  
A. AWS Developer Support

#### Explications

AWS Developer Support is a paid AWS Support tier. It provides technical support during business hours and account guidance for a monthly fee; it is not a free benefit available to all AWS customers.  
**Bonne réponse**  
B. AWS Developer Forums

#### Explications

The AWS Developer Forums are a community-run, public forum accessible to all AWS account holders at no cost. They are not part of the paid Support plans and do not carry official SLAs or direct AWS-support case routing.  
C. Programmatic case management

#### Explications

Programmatic case management (creating/managing support cases via the AWS Support API) is a capability associated with Business and Enterprise support levels; API-driven support features and automated case workflows are not available to all accounts for free.  
D. AWS technical account manager (TAM)

#### Explications

A Technical Account Manager (TAM) is a premium, dedicated support resource provided only with the Enterprise Support plan. It is a paid, account-specific service and therefore not universally free.  
Explication générale  
The AWS Developer Forums are the only option listed that is universally available at no cost — they are community forums open to all AWS users and are not tied to any Support plan. The other choices are paid support features or plan-dependent capabilities (paid support tiers, API-based case management available only with higher-tier plans, and TAM for Enterprise).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 45Ignoré  
**A company has a centralized group of users with large file storage requirements that have exceeded the space available on premises. The company wants to extend its file storage capabilities for this group while retaining the performance benefit of sharing content locally.**  
**What is the MOST operationally efficient AWS solution for this scenario?**  
A. Create an Amazon S3 bucket for each user. Mount each bucket by using an S3 file system mounting utility.

#### Explications

Amazon S3 is object storage, not a native POSIX file system. Tools that mount S3 as a filesystem (s3fs, etc.) provide limited POSIX semantics, can suffer performance and consistency issues for many small files, and managing a separate bucket per user increases operational overhead rather than simplifying shared, low-latency access.  
**Bonne réponse**  
B. Configure and deploy an AWS Storage Gateway file gateway. Connect each user’s workstation to the file gateway.

#### Explications

AWS Storage Gateway (File Gateway) presents standard NFS/SMB file interfaces to on‑premises applications while caching hot data locally and storing objects in Amazon S3. It is a managed hybrid storage service that preserves local sharing performance, scales S3 capacity transparently, and reduces administrative effort compared with building and operating custom file servers.  
C. Move each user’s working environment to Amazon WorkSpaces. Set up an Amazon WorkDocs account for each user.

#### Explications

Amazon WorkSpaces and Amazon WorkDocs address virtual desktops and document collaboration. They do not provide an on‑prem SMB/NFS file share with local caching to extend existing file servers, so they are not the most direct or operationally efficient solution for extending a centralized on‑prem shared file store.  
D. Deploy an Amazon EC2 instance and attach an Amazon Elastic Block Store (Amazon EBS) Provisioned IOPS volume. Share the EBS volume directly with the users.

#### Explications

Amazon EBS is block storage intended to be attached to a single EC2 instance; it is not a shared file system for many concurrent users. While Multi‑Attach exists for specific use cases, it requires cluster‑aware file systems and adds significant operational complexity. Using EBS would typically require running and managing a file server on EC2, increasing operational burden.  
Explication générale  
The question tests hybrid file storage options. The File Gateway of AWS Storage Gateway is the best operationally efficient choice because it exposes NFS/SMB shares with local caching while storing data durably in S3, minimizing on‑prem capacity and management. The distractors either misuse object/block storage (S3 mounts, EBS) or propose different services (WorkSpaces/WorkDocs) that do not provide a seamless, low‑latency extension of an on‑prem shared file environment.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 46Ignoré  
**Which AWS service or tool provides recommendations to help users get rightsized Amazon EC2 instances based on historical workload usage data?**  
A. AWS Pricing Calculator

#### Explications

AWS Pricing Calculator is a planning and cost-estimation tool where you input service configurations and usage assumptions to estimate costs. It does not ingest historical Amazon CloudWatch metrics or apply automated workload analysis to produce EC2 rightsizing recommendations.  
**Bonne réponse**  
B. AWS Compute Optimizer

#### Explications

AWS Compute Optimizer uses machine learning to analyze historical utilization metrics from Amazon CloudWatch and resource configuration to generate rightsizing recommendations for EC2 instances (including family/type/size) and other supported resources. It can recommend instance size/family changes based on observed CPU, network, and (when available via the CloudWatch agent) memory usage, which is why it is the correct service for workload-based EC2 rightsizing.  
C. AWS App Runner

#### Explications

AWS App Runner is a fully managed service for deploying and running containerized web applications and APIs from source code or container images. It is not a monitoring or optimization tool and does not provide rightsizing recommendations based on historical workload data.  
D. AWS Systems Manager

#### Explications

AWS Systems Manager provides operational management, automation, inventory, and Run Command capabilities to manage compute resources. While it helps operate and maintain instances and can collect operational data, it does not perform the automated, ML-driven rightsizing analysis of historical workload metrics that Compute Optimizer provides.  
Explication générale  
The question targets knowledge of AWS services for resource optimization. AWS Compute Optimizer is the purpose-built service that analyzes historical CloudWatch metrics and resource configuration (using machine learning) to recommend right-sized EC2 instances. The other options are different-purpose tools: Pricing Calculator for cost estimation, App Runner for app deployment, and Systems Manager for operational management, none of which produce workload-based EC2 rightsizing recommendations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 47Ignoré  
**A company wants to develop an accessibility application that will convert text into audible speech.**  
**Which AWS service will meet this requirement?**  
A. Amazon MQ

#### Explications

Amazon MQ is a fully managed message broker for Apache ActiveMQ and RabbitMQ that provides queuing and pub/sub messaging (supports JMS, AMQP, MQTT, STOMP). It handles message delivery and broker management, not speech synthesis; it does not provide text‑to‑speech capabilities or the APIs/SSML features needed for converting text into audio.  
**Bonne réponse**  
B. Amazon Polly

#### Explications

This AWS service provides text‑to‑speech (TTS) synthesis, including neural voices, real‑time streaming, SSML support, multiple languages/accents, and SDK/API integrations for accessibility and IVR use cases. Those features make it the appropriate choice for converting text into audible speech.  
C. Amazon Neptune

#### Explications

Amazon Neptune is a managed graph database optimized for highly connected datasets and supports graph query languages such as Apache TinkerPop Gremlin and RDF/SPARQL. Its functionality is data storage and graph queries, not media generation or speech synthesis.  
D. Amazon Timestream

#### Explications

Amazon Timestream est une base de données de séries temporelles rapide et sans serveur, conçue pour stocker et analyser des données de télémétrie horodatées (IoT, indicateurs opérationnels). Elle est dédiée à l'ingestion et à l'interrogation de séries temporelles et ne propose aucun service ni API permettant de générer de l'audio à partir de texte.  
Explication générale  
Cette question teste vos connaissances des services AWS pour les médias et l'accessibilité. La bonne réponse est le service qui propose la synthèse vocale avec des voix neuronales, le streaming et la prise en charge de SSML. Les autres options sont des services d'infrastructure fondamentaux (courtier de messages, base de données graphiques, base de données de séries temporelles) qui ne prennent pas en charge la synthèse vocale et ne conviennent donc pas à la conversion de texte en parole audible.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 48Ignoré  
**Une entreprise souhaite déployer une application web sous forme d'application conteneurisée. Elle souhaite utiliser un service géré capable de créer automatiquement des images de conteneurs à partir du code source et de déployer l'application conteneurisée.**  
**Quel service AWS répond à ces exigences ?**  
A. AWS Elastic Beanstalk

#### Explications

Incorrect. AWS Elastic Beanstalk est une plateforme PaaS permettant de déployer des applications web (y compris des déploiements basés sur Docker), mais elle ne propose pas de service intégré de création automatique d'images conteneurisées à partir de dépôts sources. Le déploiement d'applications conteneurisées avec Beanstalk nécessite généralement de fournir un Dockerfile ou une image pré-construite, ou de créer un pipeline CI/CD distinct (par exemple, avec CodeBuild/CodePipeline) pour générer les images.  
B. Amazon Elastic Container Service (Amazon ECS)

#### Explications

Incorrect. Amazon ECS est un service d'orchestration de conteneurs géré (définitions de tâches, clusters, types de lancement Fargate/EC2) qui exécute des conteneurs, mais nécessite que les images de conteneur soient fournies dans un registre (tel qu'Amazon ECR). ECS ne génère pas d'images de conteneur à partir du code source ; la génération et le déploiement des images doivent être gérés par un outil CI/CD (CodeBuild/CodePipeline ou un outil tiers).  
**Bonne réponse**  
C. AWS App Runner

#### Explications

Tout à fait. AWS App Runner est un service entièrement géré qui permet de créer des images de conteneur directement à partir de référentiels sources (ou de les exécuter à partir d'images de conteneur dans ECR), puis de déployer et d'exécuter le service résultant. Il intègre les flux de travail source-déploiement, assure la génération automatique et le déploiement continu à partir des référentiels compatibles, et gère l'équilibrage de charge, le protocole TLS et la mise à l'échelle automatique sans que vous ayez à gérer l'infrastructure ni les pipelines de génération distincts.  
D. Amazon EC2

#### Explications

Incorrect. Amazon EC2 fournit des machines virtuelles (instances) sur lesquelles vous pouvez installer des environnements d'exécution de conteneurs et exécuter des conteneurs, mais ne propose aucun flux de travail automatisé intégré pour la création et le déploiement d'images de conteneurs à partir de sources. L'utilisation d'EC2 nécessite que vous provisionniez et gériez vous-même le système d'exploitation, les outils de construction et les processus de déploiement.  
Explication générale  
The question asks for a managed AWS service that can automatically create container images from source code and deploy the containerized application. AWS App Runner is designed for source-to-deploy scenarios: it can build images from source repositories (or deploy from ECR), manage deployment, scaling, and networking. The other options (Elastic Beanstalk, ECS, EC2) either require you to supply images or to set up separate CI/CD/build pipelines and do not provide the integrated automatic image build-from-source capability that App Runner provides.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 49Ignoré  
**A company wants to integrate natural language processing (NLP) into business intelligence (BI) dashboards. The company wants to ask questions and receive answers with relevant visualizations.**  
**Which AWS service or tool will meet these requirements?**  
A. Amazon Macie

#### Explications

This is a data security and privacy service that uses machine learning to discover, classify, and protect sensitive data (for example, in S3). It does not provide natural-language querying or visualization capabilities for BI dashboards, so it does not meet the requirement.  
B. Amazon Rekognition

#### Explications

This service provides image and video analysis (object/scene detection, face analysis, moderation, OCR for images) using deep learning. It is not a natural-language–to–visualization BI tool and does not natively integrate with dashboards to answer data questions in natural language.  
**Bonne réponse**  
C. Amazon QuickSight Q

#### Explications

QuickSight Q is the QuickSight capability that interprets natural-language questions against your data and returns appropriate charts, tables, or plain-language answers. It’s powered by ML to map user phrasing to the underlying dataset, choose the best visualization, and integrate results directly into QuickSight dashboards, matching the described requirement.  
D. Amazon Lex

#### Explications

This service provides automatic speech recognition and natural language understanding to build conversational interfaces (chatbots). While it handles intent recognition and dialog, it does not automatically generate BI visualizations or provide an out-of-the-box NL-to-visualization experience inside dashboards without substantial custom integration.  
Explication générale  
The requirement is for natural-language querying that returns relevant visualizations inside BI dashboards. QuickSight Q is specifically designed for NL question answering against datasets and producing visualizations within Amazon QuickSight. The other options are focused on security classification, image/video analysis, or conversational interfaces and do not provide the built-in NL-to-visualization BI experience.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 50Ignoré  
**What is the purpose of having an internet gateway within a VPC?**  
A. To create a VPN connection to the VPC

#### Explications

Incorrect. VPN connectivity for a VPC is provided by Virtual Private Gateways (VGW), AWS Transit Gateway, or AWS Client VPN endpoints. An internet gateway is not used to establish encrypted site-to-site or client VPN tunnels into a VPC.  
**Bonne réponse**  
B. To allow communication between the VPC and the internet

#### Explications

Correct. An Internet Gateway is a horizontally scaled, redundant, and highly available VPC component that provides a route between resources in the VPC and the public internet. To enable internet access, the route table must direct internet-bound traffic (for example, 0.0.0.0/0) to the IGW and the instance must have a public IPv4 address or Elastic IP (or an IPv6 address). The IGW is not a NAT device; NAT Gateways or NAT instances are used for private-instance outbound-only internet access.  
C. To impose bandwidth constraints on internet traffic

#### Explications

Incorrect. An Internet Gateway does not throttle or shape traffic. Bandwidth and throughput behavior are governed by instance/network performance, the instance type, and AWS networking limits. Traffic control or bandwidth limiting must be implemented at the instance, application, or external network device, not via the IGW itself.  
D. To load balance traffic from the internet across Amazon EC2 instances

#### Explications

Incorrect. Distributing incoming internet traffic across EC2 instances is the role of load balancers (ELB/ALB/NLB). The Internet Gateway simply provides a path between the VPC and the internet; it does not perform load balancing, health checks, or listener routing.  
Explication générale  
This question tests basic VPC networking: an Internet Gateway enables direct connectivity between VPC resources and the public internet when route tables and public IP addressing are configured. It does not create VPN connections (use VGW/Transit Gateway), impose bandwidth controls, or perform load balancing (use ELB). The IGW provides the network path and attaches to the VPC; other AWS services handle VPN, NAT, bandwidth management, and load distribution.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 51Ignoré  
**A company is building a web application using AWS.**  
**Which AWS service will help prevent network layer DDoS attacks against the web application?**  
A. AWS WAF

#### Explications

Incorrect — AWS WAF is a web application firewall that inspects and filters HTTP/S (Layer 7\) traffic to block common application-layer attacks (for example, SQL injection, cross-site scripting). While it can use rate-based rules to limit abusive requests to an application, it does not provide network- or transport-layer (Layer 3/4) DDoS mitigation.  
B. AWS Firewall Manager

#### Explications

Incorrect — AWS Firewall Manager is a centralized policy management service that automates deployment of WAF rules, Shield Advanced protections, and VPC security group policies across multiple accounts. It orchestrates and enforces policies but does not itself perform DDoS mitigation.  
C. Amazon GuardDuty

#### Explications

Incorrect — Amazon GuardDuty is a threat-detection service that analyzes telemetry (VPC Flow Logs, CloudTrail, DNS logs) to identify suspicious or malicious activity and generates findings. It provides detection and alerting, not active DDoS traffic mitigation or protection.  
**Bonne réponse**  
D. AWS Shield

#### Explications

Correct — AWS Shield provides DDoS protection at the network and transport layers. Shield Standard automatically defends against common volumetric and protocol-layer attacks at no extra charge; Shield Advanced offers enhanced detection and mitigation for larger or more sophisticated attacks, access to the DDoS Response Team (DRT), cost protection for scaling during attacks, and integration with WAF and Firewall Manager for coordinated defenses.  
Explication générale  
The question targets DDoS protection at the network/transport layer. AWS Shield is the service designed to mitigate Layer 3/4 DDoS attacks (Standard for basic protections, Advanced for enhanced mitigation and support). Other options address different needs: WAF protects HTTP/S (Layer 7\) application attacks, Firewall Manager manages and deploys security policies across accounts, and GuardDuty detects suspicious activity — none provide the primary network-layer DDoS mitigation that Shield does.  
Domaine  
Domain 2: Security and Compliance  
Question 52Ignoré  
**A user has limited knowledge of AWS services, but wants to quickly deploy a scalable Node.js application in the AWS Cloud.**  
**Which service should be used to deploy the application?**  
A. AWS CloudFormation

#### Explications

Incorrect. CloudFormation is a declarative infrastructure-as-code service used to provision and orchestrate AWS resources using templates. It requires writing and maintaining templates and an understanding of resource relationships, so it is not the fastest path for a beginner who wants an out-of-the-box application deployment.  
**Bonne réponse**  
B. AWS Elastic Beanstalk

#### Explications

Correct. Elastic Beanstalk is a managed application platform that automates provisioning of compute, networking, load balancing, auto scaling, and health monitoring for supported runtimes (including Node.js). It lets users deploy application code (via console, CLI, or CI) without having to configure underlying infrastructure, making it ideal for quick, scalable deployments by users with limited AWS experience.  
C. Amazon EC2

#### Explications

Incorrect. EC2 provides raw virtual machines that give full control over the operating system and runtime, but require manual setup of the application environment, patching, scaling, and load balancing. That operational overhead makes EC2 unsuitable for rapid, beginner-friendly deployments.  
D. AWS OpsWorks

#### Explications

Incorrect. OpsWorks is a configuration-management service (Chef/Puppet–based) for automating operational tasks and managing application stacks. It is geared toward users familiar with configuration management and automation, not beginners seeking a simple, quick deploy option.  
Explication générale  
Elastic Beanstalk is the best choice because it is a managed, platform-level service that automates provisioning, scaling, and health management for Node.js applications, enabling quick deployment with minimal AWS knowledge. The other options are lower-level or specialist tools: CloudFormation is for template-based infrastructure provisioning, EC2 is unmanaged virtual servers, and OpsWorks is for configuration-management automation—each requiring more expertise and operational effort.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 53Ignoré  
**Which AWS services or features form the AWS Cloud global infrastructure?**  
**(Choose two.)**  
**Sélection correcte**  
A. Availability Zones

#### Explications

These are the physical, isolated data center locations inside a geographic area that provide independent power, networking, and cooling so you can place resources in separate failure domains to achieve high availability and fault tolerance. They are a foundational, physical element of AWS global infrastructure.  
B. Amazon ElastiCache

#### Explications

A managed, in-memory caching service that runs within Regions and AZs to accelerate application performance. It is a regional service built on top of the infrastructure, not a physical infrastructure building block itself.  
**Sélection correcte**  
C. AWS Regions

#### Explications

A geographic deployment area composed of multiple isolated data center locations; customers select a Region for data residency, latency, and regulatory requirements. Regions are the primary geographic units that make up AWS’s global footprint.  
D. Amazon S3

#### Explications

An object storage service that stores data in specific Regions and can offer features like cross-region replication. It is a regional service and application-level offering rather than a physical component of the global infrastructure.  
E. Amazon VPC

#### Explications

A virtual networking service that creates isolated networks for resources within a Region (and across AZs in that Region). It is a logical construct provisioned on top of AWS infrastructure, not a physical infrastructure component.  
Explication générale  
The AWS global infrastructure is defined by its geographic and physical building blocks: Regions (geographic areas) and the isolated data center locations within them that enable high availability and fault isolation. Managed services such as ElastiCache, S3, and VPC operate inside Regions and AZs but are service-layer constructs rather than the underlying global infrastructure components.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 54Ignoré  
**Which options are AWS Cloud Adoption Framework (AWS CAF) security perspective capabilities? (Choose two.)**  
A. Observability

#### Explications

Monitoring, telemetry and system-state analysis are capabilities typically associated with the Operations perspective of the AWS CAF. While these capabilities support security (for detection and forensics), they are not enumerated as core security-perspective capabilities in the CAF documentation.  
B. Incident and problem management

#### Explications

Processes for managing operational incidents and problem resolution align with operational runbooks and service management (Operations perspective). Security-specific processes emphasize detection, containment, forensics and coordinated remediation, which is distinct from general incident/problem management.  
**Sélection correcte**  
C. Incident response

#### Explications

The security perspective mandates capabilities for detecting, investigating, containing and recovering from security events. AWS services commonly used to implement this include centralized logging and audit (AWS CloudTrail), threat detection (Amazon GuardDuty), aggregation/coordination (AWS Security Hub), and automated orchestration/response (AWS Lambda, AWS Systems Manager).  
**Sélection correcte**  
D. Infrastructure protection

#### Explications

Protecting compute, network and storage resources via architecture and controls is a core security capability. Practical implementations include secure VPC design, security groups and NACLs, host hardening, encryption and key management (AWS KMS), and edge/web protections (AWS WAF, AWS Shield), plus least-privilege access through IAM.  
E. Availability and continuity

#### Explications

High availability, business continuity and disaster recovery are resilience objectives typically handled by the Operations and Platform perspectives (multi‑AZ architectures, backups, Route 53 failover). They support overall reliability but are not listed as primary security-perspective capabilities in the CAF.  
Explication générale  
The AWS CAF security perspective focuses on protecting cloud assets and managing security events. The primary security capabilities include measures to shield infrastructure and processes to detect, analyze, contain and recover from security events (the verified answers). Other items such as monitoring/observability, general incident/problem management, and availability/continuity support security but are mainly surfaced under the Operations or Platform perspectives rather than as core security-perspective capabilities.  
Domaine  
Domain 2: Security and Compliance  
Question 55Ignoré  
**What can a cloud practitioner use to retrieve AWS security and compliance documents and submit them as evidence to an auditor or regulator?**  
A. AWS Certificate Manager

#### Explications

Incorrect. Certificate management services issue and manage TLS/SSL certificates to secure data in transit; they do not serve as a repository for AWS compliance attestations, audit reports, or contractual agreements that auditors require.  
B. AWS Systems Manager

#### Explications

Incorrect. Systems Manager is an operations and management service (Run Command, Patch Manager, Parameter Store, Automation) for administering resources; it is not intended to provide AWS-issued compliance reports or audit-ready artifacts for regulators.  
**Bonne réponse**  
C. AWS Artifact

#### Explications

Correct. AWS Artifact is the official portal that provides on-demand access to AWS compliance reports and security and privacy documents. It exposes two primary artifact types—Reports (SOC, PCI, ISO, etc.) and Agreements (contractual artifacts customers can accept)—so customers can download audit reports and submit them as evidence to auditors or regulators.  
D. Amazon Inspector

#### Explications

Incorrect. Amazon Inspector performs automated security assessments to identify vulnerabilities and deviations from best practices in workloads and produces findings to remediate security issues; it does not provide AWS's formal compliance certifications or audit reports for regulators.  
Explication générale  
This item tests where to obtain AWS-provided audit artifacts. AWS Artifact is the dedicated service for retrieving official compliance reports and contractual agreements (e.g., SOC, PCI, ISO, BAAs) that can be submitted to auditors. The distractors are valid AWS services (certificate management, operations management, vulnerability assessment) but do not function as a repository of AWS compliance documents.  
Domaine  
Domain 2: Security and Compliance  
Question 56Ignoré  
**A company is hosting a web application on Amazon EC2 instances. The company wants to implement custom conditions to filter and control inbound web traffic.**  
**Which AWS service will meet these requirements?**  
A. Amazon GuardDuty

#### Explications

GuardDuty is an intelligent threat detection service that analyzes AWS account and workload telemetry (VPC Flow Logs, CloudTrail, DNS logs) to surface suspicious activity and findings. It is designed for detection and alerting, not for inline request filtering or blocking of HTTP(S) traffic to applications.  
**Bonne réponse**  
B. AWS WAF

#### Explications

Provides an inline web application firewall capability that lets you author rule statements (IP sets, geographic match, string/regex match, SQLi/XSS protections, rate-based rules, managed rule groups) and apply allow/block/count actions to HTTP(S) requests. It integrates with Amazon CloudFront, Application Load Balancer, and API Gateway, making it the correct service for implementing custom conditions to filter and control inbound web traffic.  
C. Amazon Macie

#### Explications

Macie uses machine learning to discover, classify, and protect sensitive data in Amazon S3 (e.g., PII). Its scope is data discovery and privacy protection, not request-level traffic inspection or blocking for web applications.  
D. AWS Shield

#### Explications

Shield focuses on DDoS protection: Standard provides automatic network-layer protections, and Advanced adds additional detection/mitigation and response support. While it helps mitigate volumetric and protocol attacks, it does not provide the granular, condition-based HTTP request filtering and rule authoring needed to control inbound web traffic.  
Explication générale  
The question tests knowledge of services that can perform conditional, request-level filtering for web applications. The correct choice is the web application firewall capability, which supports custom rule statements (IP, header, URI, string/regex, rate-based, managed rules) and integrates with CloudFront, ALB, and API Gateway to allow blocking or allowing HTTP(S) requests. The other services—GuardDuty, Macie, and Shield—provide detection/monitoring, data classification, and DDoS mitigation respectively, but do not offer inline, customizable request filtering.  
Domaine  
Domain 2: Security and Compliance  
Question 57Ignoré  
**A company is migrating its on-premises server to an Amazon EC2 instance. The server must stay active at all times for the next 12 months.**  
**Which EC2 pricing option is the MOST cost-effective for the company's workload?**  
A. On-Demand

#### Explications

A pay-as-you-go compute model with no long-term commitment; billed by the second/hour and provides maximum flexibility. For a workload that must run continuously for 12 months, this option results in a higher total cost compared with capacity commitments (Reserved Instances or Savings Plans).  
B. Dedicated Hosts

#### Explications

Physical servers dedicated to a single customer to meet compliance, licensing, or isolation requirements. These are typically more expensive than shared tenancy options and are unnecessary for a standard always-on migration unless specific regulatory or licensing constraints demand dedicated hardware.  
C. Spot Instances

#### Explications

Provisioning of spare EC2 capacity at steep discounts but with the possibility of interruption (with short notice) when AWS reclaims capacity. Because the instance can be terminated or stopped unexpectedly, this option is unsuitable for a server that must remain active without interruption for 12 months.  
**Bonne réponse**  
D. Reserved Instances

#### Explications

Purchasing capacity with a 1‑ or 3‑year commitment reduces hourly charges substantially compared with on‑demand pricing; options include Standard and Convertible RIs and provide instance- or regional-level billing discounts. For predictable, steady-state, always-on workloads over a 12‑month period, this reserved capacity approach yields the lowest effective cost among the choices.  
Explication générale  
The question tests knowledge of EC2 pricing models for a predictable, always-on workload. Committing to reserved capacity for a 1‑year term provides the largest predictable cost savings for a server that must remain active continuously for 12 months. The other choices are either more expensive for steady-state usage (pay-as-you-go), interruptible (spot capacity), or designed for specialized compliance/use cases (dedicated physical hosts).  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 58Ignoré  
**A company stores a large amount of data that auditors access only twice each year.**  
**Which Amazon S3 storage class should the company use to store the data with the LOWEST cost?**  
A. Amazon S3 Outposts

#### Explications

S3 on Outposts delivers AWS S3 APIs and object storage locally for workloads that require on‑premises data residency and low latency. It involves Outposts infrastructure and associated costs, so it is not the lowest‑cost option for long‑term, infrequently accessed archival data.  
**Bonne réponse**  
B. Amazon S3 Glacier Instant Retrieval

#### Explications

The Glacier Instant Retrieval storage class is designed for long‑term, infrequently accessed objects while offering very fast (millisecond) retrieval. It has a much lower per‑GB monthly storage charge than S3 Standard and avoids the ongoing monitoring/automation fees associated with Intelligent‑Tiering; for data accessed only twice a year among the listed choices, it yields the lowest overall storage cost (noting retrieval requests and data retrieval fees still apply).  
C. Amazon S3 Standard

#### Explications

S3 Standard is optimized for frequently accessed data and provides high durability and availability at a correspondingly higher per‑GB storage price. For data accessed predictably only twice per year, its storage cost will be higher than archival classes.  
D. Amazon S3 Intelligent-Tiering

#### Explications

S3 Intelligent‑Tiering automatically moves objects between access tiers based on observed access patterns and includes a small monthly monitoring and automation charge; while it reduces cost for unpredictable patterns, for data that is predictably and very rarely accessed, explicitly choosing an archival class is generally more cost‑effective.  
Explication générale  
The question tests selection of the lowest‑cost S3 storage class for data accessed very infrequently (twice per year). Choose the archival/infrequent‑access class that minimizes per‑GB storage charges while meeting retrieval requirements. Among the provided options, the Glacier Instant Retrieval class offers the best balance of very low storage cost and rapid retrieval. The other choices are either designed for frequent access (S3 Standard), on‑premises residency (Outposts), or for unpredictable access patterns (Intelligent‑Tiering), and therefore are not the lowest‑cost fit for this predictable, infrequent access scenario.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 59Ignoré  
**A company wants to create templates that the company can reuse to deploy multiple AWS resources.**  
**Which AWS service or feature can the company use to meet this requirement?**  
A. AWS Marketplace

#### Explications

AWS Marketplace is a catalog for third-party software and AMIs that customers can subscribe to or deploy; it is not an infrastructure-as-code service for authoring reusable templates that declaratively define multiple AWS resources.  
B. Amazon Machine Image (AMI)

#### Explications

An Amazon Machine Image (AMI) is a VM image used to launch EC2 instances (OS \+ software). It captures a single instance configuration and does not provide a declarative way to define or orchestrate multiple AWS resources as a reusable template.  
**Bonne réponse**  
C. AWS CloudFormation

#### Explications

AWS CloudFormation is the AWS Infrastructure-as-Code service that uses JSON or YAML templates to declaratively define and provision collections of AWS resources as stacks. It supports parameters, outputs, nested stacks, change sets, stack sets (multi-account/region deployments), drift detection and integration with CI/CD—making it the appropriate choice for reusable templates to deploy multiple resources.  
D. AWS OpsWorks

#### Explications

AWS OpsWorks is a configuration-management service (Chef/Puppet) for automating software configuration and lifecycle on instances. It focuses on instance-level configuration and application management rather than providing general-purpose declarative templates to provision arbitrary collections of AWS infrastructure.  
Explication générale  
This question tests knowledge of AWS infrastructure-as-code solutions. AWS CloudFormation is the correct choice because it provides declarative, reusable JSON/YAML templates and stack orchestration for provisioning multiple AWS resources. The distractors describe related but different offerings: Marketplace is a software catalog, AMIs are VM images for EC2 instances, and OpsWorks is for configuration management rather than multi-resource templated provisioning.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 60Ignoré  
**Which pricing model will interrupt a running Amazon EC2 instance if capacity becomes temporarily unavailable?**  
A. On-Demand Instances

#### Explications

Billed per second or hour with no long-term commitment, this pricing model runs until you stop or terminate it. AWS does not reclaim these instances due to temporary capacity shortages, so they are not subject to the automatic interruptions described in the question.  
B. Standard Reserved Instances

#### Explications

Cette option correspond à un engagement de facturation offrant un prix horaire effectif réduit pour une utilisation stable. Il s'agit d'un système de tarification/remise qui n'entraîne aucune interruption des instances en cours d'exécution sur AWS ; la réservation de capacité est une fonctionnalité distincte si vous avez besoin d'une capacité garantie au niveau de votre zone de disponibilité.  
**Bonne réponse**  
C. Exemples ponctuels

#### Explications

Utilise la capacité EC2 inutilisée à un tarif préférentiel et peut être récupérée par AWS lorsqu'elle est nécessaire ailleurs. Les instances peuvent recevoir une notification d'interruption de deux minutes, puis être arrêtées, supprimées ou mises en hibernation selon le comportement d'interruption choisi. Idéal pour les charges de travail tolérantes aux pannes, flexibles ou par lots pouvant supporter les interruptions.  
D. Instances réservées convertibles

#### Explications

Permet de modifier les attributs de l'instance réservé en échange d'un engagement sur une période donnée, offrant ainsi une plus grande flexibilité de facturation. À l'instar des autres offres réservées, il s'agit avant tout d'un mécanisme de tarification et non d'une interruption forcée des instances en cours d'exécution par AWS en raison d'une indisponibilité temporaire de capacité.  
Explication générale  
Les instances Spot sont le modèle de tarification EC2 qui utilise la capacité disponible et peut être récupérée par AWS, ce qui peut entraîner des interruptions (avec un court préavis) des instances en cours d'exécution lorsque cette capacité est nécessaire. Les autres modèles mentionnés (à la demande et réservés) sont des options de tarification ou d'engagement qui n'entraînent pas d'interruption des instances par AWS en cas de pénurie temporaire de capacité ; les réservations de capacité sont une fonctionnalité distincte permettant de garantir la capacité au niveau de la zone de disponibilité.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 61Ignoré  
**Une entreprise souhaite configurer ses charges de travail pour qu'elles remplissent leurs fonctions prévues et se rétablissent rapidement en cas de panne.**  
**Quel pilier du cadre AWS Well-Architected correspond à ces objectifs ?**  
A. Efficacité de la performance

#### Explications

Ce document décrit le pilier « Efficacité des performances », qui met l'accent sur le choix des types de ressources, leur dimensionnement et les modèles architecturaux appropriés pour atteindre les objectifs de performance et d'efficacité du système (par exemple, la mise en cache, le dimensionnement des instances et le choix de la base de données). Il ne traite pas de la conception pour la tolérance aux pannes, les objectifs de reprise après incident ni les processus de reprise automatisés ; par conséquent, il n'aborde pas directement la reprise rapide après une panne.  
B. Durabilité

#### Explications

Ce document décrit le pilier « Durabilité », qui vise à minimiser l’impact environnemental et à optimiser la consommation des ressources (mesure de l’empreinte carbone, utilisation efficace des capacités de calcul et de stockage). Il ne traite pas de la résilience du système, de la tolérance aux pannes ni de la planification de la reprise après sinistre.  
**Bonne réponse**  
C. Fiabilité

#### Explications

Ce pilier vise à garantir le bon fonctionnement des systèmes et leur capacité de récupération en cas de panne. Il couvre les architectures tolérantes aux pannes, la redondance, la sauvegarde et la restauration, la définition des objectifs de temps de récupération (RTO) et de point de récupération (RPO), la récupération automatisée, les contrôles d'intégrité et les tests des procédures de récupération. Parmi les modèles et services AWS couramment utilisés pour assurer cette fiabilité, on trouve les déploiements multi-AZ/multi-régions, la mise à l'échelle automatique, l'équilibrage de charge élastique, Amazon RDS multi-AZ, la durabilité d'Amazon S3, le basculement Route 53, Amazon SQS pour le découplage et la surveillance/les alertes avec Amazon CloudWatch.  
D. Sécurité

#### Explications

Ce document décrit le pilier Sécurité, qui vise à protéger la confidentialité, l'intégrité et la disponibilité grâce à la gestion des identités et des accès, le chiffrement, les contrôles réseau, la journalisation et la réponse aux incidents. Bien que la disponibilité soit un aspect important de la sécurité, ce pilier se concentre principalement sur la protection et la gestion des menaces, plutôt que sur la conception pour la tolérance aux pannes, les objectifs de reprise après sinistre et la résilience opérationnelle (qui constituent le cœur du pilier Fiabilité).  
Explication générale  
Cette question évalue la connaissance des piliers du cadre AWS Well-Architected. Le pilier Fiabilité est le plus pertinent car il traite explicitement de la garantie que les charges de travail exécutent leurs fonctions prévues et redémarrent rapidement grâce à la tolérance aux pannes, la redondance, la planification des sauvegardes et des restaurations, ainsi que les modèles de restauration automatisés. Les autres piliers (Performances, Durabilité, Sécurité) se concentrent sur des objectifs différents (efficacité des ressources, impact environnemental et protection des systèmes et des données) et ne constituent donc pas la réponse principale.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 62Ignoré  
**Une entreprise souhaite déployer une partie de ses ressources dans le cloud AWS. Pour se conformer aux exigences réglementaires, les données doivent rester locales et sur site. La latence entre AWS et les ressources de l'entreprise doit être faible.**  
**Quel service ou fonctionnalité AWS permet de répondre à ces exigences ?**  
A. Zones locales AWS

#### Explications

Les zones locales rapprochent les ressources de calcul et de stockage AWS des grandes zones métropolitaines afin de réduire la latence du réseau pour les utilisateurs finaux, mais il s'agit d'extensions gérées par AWS situées dans des installations de colocation métropolitaines — et non de matériel installé dans le centre de données d'un client — elles ne garantissent donc pas la résidence des données sur site exigée par certaines réglementations.  
B. Zones de disponibilité

#### Explications

Les zones de disponibilité sont des emplacements de centres de données distincts et isolés au sein d'une région AWS, conçus pour une haute disponibilité et l'isolation des pannes. Elles font partie de l'infrastructure cloud AWS et ne peuvent pas être déployées dans les locaux d'un client ; elles ne répondent donc pas aux exigences de résidence des données sur site ni d'accès natif à faible latence aux systèmes locaux.  
**Bonne réponse**  
C. Postes avancés AWS

#### Explications

Outposts fournit des racks de calcul et de stockage gérés par AWS, installés sur le site du client et intégrés au plan de contrôle AWS. Cela permet d'exécuter localement les mêmes API et services AWS, de conserver les données sur site pour répondre aux exigences de résidence et de bénéficier d'un accès à faible latence entre les ressources locales et l'infrastructure gérée par AWS ; une solution parfaitement adaptée à ce scénario.  
D. Zones de longueur d'onde AWS

#### Explications

Wavelength intègre la puissance de calcul AWS aux points d'accès des opérateurs 5G afin de minimiser la latence pour les appareils et réseaux mobiles. Conçue pour les cas d'usage en périphérie de réseau, cette solution diffère de l'installation d'une infrastructure AWS au sein même du centre de données d'une entreprise et ne répond donc pas aux exigences strictes de résidence des données sur site.  
Explication générale  
The question tests knowledge of AWS offerings that extend cloud services to customer premises. AWS Outposts is purpose-built to deliver AWS infrastructure and services on‑premises, preserving local data residency and providing low-latency access to on‑site resources. The other options (Local Zones, Availability Zones, Wavelength) extend AWS infrastructure or reduce latency in specific ways but are not installed in a customer’s own data center and therefore do not meet strict on‑prem regulatory requirements.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 63Ignoré  
**A company wants its Amazon EC2 instances to be in different locations but share the same geographic area. The company also wants to use multiple power grids and independent networking connectivity for the EC2 instances.**  
**Which solution meets these requirements?**  
A. Use EC2 instances in multiple edge locations in the same AWS Region.

#### Explications

Edge locations are part of Amazon CloudFront and the global edge network used for caching, content delivery, and running lightweight edge functions (e.g., Lambda@Edge). They are not deployment targets for standard EC2 instances and do not represent AWS data-center constructs with independent power grids and networking like Availability Zones do.  
**Bonne réponse**  
B. Use EC2 instances in multiple Availability Zones in the same AWS Region.

#### Explications

Availability Zones (AZs) are AWS data-center locations within a single Region that consist of one or more discrete data centers with independent power, cooling, and physical network connectivity. AZs are intentionally isolated from failures in other AZs but are connected by low-latency AWS backbone links, making them the correct construct for deploying EC2 instances across different physical locations in the same geographic area for fault isolation and high availability.  
C. Use EC2 instances in multiple Amazon Connect locations in the same AWS Region.

#### Explications

Amazon Connect is a managed cloud contact-center service. Its notion of ‘locations’ relates to contact-center resources and routing, not to physical data-center placement for EC2 instances, so it does not provide independent power grids or separate networking enclaves for EC2.  
D. Use EC2 instances in multiple AWS Artifact locations in the same AWS Region.

#### Explications

AWS Artifact is a customer portal for on-demand access to compliance reports and security and compliance documentation. It is not a physical or compute location and therefore irrelevant for deploying EC2 instances or meeting requirements for independent power and networking.  
Explication générale  
The requirement—EC2 instances in different physical locations within the same geographic area, with independent power grids and networking—maps to AWS Availability Zones. AZs are discrete data centers (or groups of data centers) within a Region designed for fault isolation and independent infrastructure. The other choices are either CDN/edge components (edge locations), service-specific constructs (Amazon Connect), or a compliance portal (AWS Artifact), none of which provide EC2 deployment across independent physical infrastructures.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 64Ignoré  
**A company is migrating its applications from on-premises to the AWS Cloud. The company wants to ensure that the applications are assigned only the minimum permissions that are needed to perform all operations.**  
**Which AWS service will meet these requirements?**  
**Bonne réponse**  
A. AWS Identity and Access Management (IAM)

#### Explications

IAM provides centralized, fine‑grained access control using identities (users, groups, roles) and JSON policy documents. It enables least‑privilege by attaching narrowly scoped permissions, using roles and temporary credentials for applications, and adding policy conditions (resource, action, principal, and context) to limit access vectors.  
B. Amazon CloudWatch

#### Explications

Amazon CloudWatch is an observability and monitoring service (metrics, logs, alarms, dashboards). It does not provision or manage access control policies for identities or resources, so it cannot enforce least‑privilege permissions for applications.  
C. Amazon Macie

#### Explications

Amazon Macie is a data security service that discovers and classifies sensitive data (for example, in S3) using machine learning. It helps protect data but does not perform identity or permission management for applications.  
D. Amazon GuardDuty

#### Explications

Amazon GuardDuty is a threat detection service that analyzes event sources (CloudTrail, VPC Flow Logs, DNS) for malicious activity. It provides security findings but does not assign or manage IAM permissions.  
Explication générale  
This question tests the principle of least privilege and which AWS service is used to assign and enforce access permissions. The correct choice is the identity and access management service that creates identities, roles, and policy documents to grant the minimum required permissions. The other options (monitoring, data classification, and threat detection services) provide security-related capabilities but do not manage or enforce application permissions.  
Domaine  
Domain 2: Security and Compliance  
Question 65Ignoré  
**A company has deployed applications on Amazon EC2 instances. The company needs to assess application vulnerabilities and must identify infrastructure deployments that do not meet best practices.**  
**Which AWS service can the company use to meet these requirements?**  
A. AWS Trusted Advisor

#### Explications

Provides prescriptive, account-level recommendations across cost, performance, security, fault tolerance and service limits by checking AWS resource configurations and usage patterns. It does not perform workload-level vulnerability scanning or produce CVE findings for software running on EC2 instances.  
**Bonne réponse**  
B. Amazon Inspector

#### Explications

Performs automated security assessments of workloads (EC2 and container images), identifying known software vulnerabilities (CVEs), insecure configurations and deviations from security best practices. Findings can be exported to Security Hub or EventBridge for remediation workflows, making it the appropriate service for application vulnerability scanning.  
C. AWS Config

#### Explications

Continuously evaluates and records AWS resource configurations against rules to assess compliance and detect drift. Useful for configuration governance and audit trails, but it does not perform vulnerability scanning of application binaries or OS packages running on instances.  
D. Amazon GuardDuty

#### Explications

Continuously analyzes AWS logs and telemetry (CloudTrail, VPC Flow Logs, DNS) to detect malicious or anomalous activity and compromised resources. It detects threats and suspicious behavior, not vulnerabilities in application software or CVE-level issues.  
Explication générale  
The requirement is to assess application vulnerabilities and flag infrastructure not meeting security best practices at the workload level. Amazon Inspector is designed to scan EC2 instances and container images for software vulnerabilities and configuration issues and integrate findings into remediation workflows. Trusted Advisor, AWS Config, and GuardDuty address related but different needs: advisory checks, resource-configuration compliance, and threat detection respectively, so they do not replace Inspector’s vulnerability assessments.  
Domaine  
Domain 2: Security and Compliance  
Question 66Ignoré  
**Which Amazon S3 storage class is MOST cost-effective for unknown access patterns?**  
A. S3 Standard

#### Explications

Optimized for frequently accessed objects with low latency and high throughput; its higher per‑GB storage cost makes it less cost‑effective if many objects are rarely accessed or access patterns are unknown.  
B. S3 Standard-Infrequent Access (S3 Standard-IA)

#### Explications

Intended for long‑lived but infrequently accessed objects; offers lower storage cost than frequent‑access tiers but imposes retrieval fees and a minimum storage duration (typically 30 days), so it can be costly if access unexpectedly becomes frequent.  
C. S3 One Zone-Infrequent Access (S3 One Zone-IA)

#### Explications

Stores data in a single Availability Zone for lower storage cost but reduced resilience; it also has retrieval fees and minimum retention charges, making it unsuitable when access patterns are unknown or higher durability/availability is required.  
**Bonne réponse**  
D. S3 Intelligent-Tiering

#### Explications

Monitors object access and automatically moves objects between access tiers (frequent, infrequent, and optional archive tiers) to optimize cost without user intervention; this automated tiering makes it the best choice for unknown or changing access patterns (note: a small monitoring/automation charge applies).  
Explication générale  
S3 Intelligent‑Tiering is designed for unknown or unpredictable access patterns by automatically monitoring usage and shifting objects between appropriate access tiers to minimize cost while preserving access. The other classes assume known access/durability characteristics (frequent access, infrequent access with retrieval fees, or single‑AZ storage) and can therefore incur higher storage or retrieval costs or provide lower resilience if access patterns differ from expectations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 67Ignoré  
**A company wants to migrate its on-premises relational databases to the AWS Cloud. The company wants to use infrastructure as close to its current geographical location as possible.**  
**Which AWS service or resource should the company use to select its Amazon RDS deployment area?**  
A. Amazon Connect

#### Explications

Amazon Connect is a managed cloud contact-center service for voice and chat interactions. It is focused on customer engagement functionality and does not provide mechanisms for choosing geographic deployment locations for database services like Amazon RDS.  
B. AWS Wavelength

#### Explications

AWS Wavelength places compute and networking at the telecom edge to support ultra-low-latency 5G applications. It is not the mechanism for selecting where RDS database instances are hosted; RDS is provisioned within standard AWS Regions and Availability Zones rather than Wavelength zones.  
**Bonne réponse**  
C. AWS Regions

#### Explications

AWS Regions are distinct geographic areas that contain multiple Availability Zones. When you provision Amazon RDS you select a Region (and optionally AZs within it), which determines the physical location of data, affects latency to on-premises systems, and supports data-residency and compliance requirements—making Regions the appropriate choice for selecting where to deploy RDS.  
D. AWS Direct Connect

#### Explications

AWS Direct Connect provides a dedicated network link between on-premises environments and AWS to improve bandwidth, consistency, and latency for connectivity. It helps with network access to AWS resources but does not itself determine which geographic Region RDS instances are deployed in.  
Explication générale  
The question tests understanding of AWS geographic and deployment constructs. Selecting an Amazon RDS deployment area is achieved by choosing an AWS Region (and Availability Zone), which determines where the database and its data physically reside and impacts latency and compliance. The other options are unrelated: Amazon Connect is a contact-center service, AWS Wavelength is for edge/5G low-latency compute, and Direct Connect is a connectivity service rather than a deployment-location selector.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 68Ignoré  
**Which AWS services or tools can identify rightsizing opportunities for Amazon EC2 instances? (Choose two.)**  
**Sélection correcte**  
A. AWS Cost Explorer

#### Explications

Cost Explorer includes a Rightsizing Recommendations feature that analyzes historical usage and cost data to surface underutilized or oversized EC2 instances. It uses aggregated cost and CloudWatch usage metrics to suggest instance size adjustments or terminations from a cost-optimization perspective.  
B. AWS Billing Conductor

#### Explications

AWS Billing Conductor is a billing and charge-allocation service that lets you customize how costs are aggregated and billed across organizational units. It does not analyze instance-level utilization or produce rightsizing recommendations.  
C. Amazon CodeGuru

#### Explications

Amazon CodeGuru provides automated code reviews and runtime profiling focused on application code performance. While profiler findings can hint at inefficient code, it does not produce EC2 instance rightsizing recommendations based on resource utilization.  
D. Amazon SageMaker

#### Explications

Amazon SageMaker is a managed machine-learning platform for building, training, and deploying models. It is not a cost/usage analysis or infrastructure-rightsizing tool and does not provide EC2 rightsizing recommendations.  
**Sélection correcte**  
E. AWS Compute Optimizer

#### Explications

Compute Optimizer analyzes resource configuration and CloudWatch utilization metrics (CPU, memory where available, network, EBS) to recommend optimal EC2 instance types and sizes, including projected savings and confidence levels—making it a purpose-built rightsizing service.  
Explication générale  
The question targets tools that identify EC2 rightsizing opportunities. Cost Explorer and Compute Optimizer are the two correct choices: Cost Explorer surfaces rightsizing recommendations from cost and usage trends, while Compute Optimizer provides detailed instance-type and size recommendations using configuration and CloudWatch utilization metrics. The other options are unrelated to instance rightsizing—Billing Conductor manages billing constructs, CodeGuru focuses on code quality and profiling, and SageMaker is for ML model development.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 69Ignoré  
**A company plans to migrate to the AWS Cloud. The company wants to use the AWS Cloud Adoption Framework (AWS CAF) to define and track business outcomes as part of its cloud transformation journey.**  
**Which AWS CAF governance perspective capability will meet these requirements?**  
**Bonne réponse**  
A. Benefits management

#### Explications

This governance capability defines measurable business objectives, assigns ownership, and establishes KPIs and benefit-realization plans to track whether cloud investments deliver the expected outcomes. It creates a benefits register and reporting cadence so stakeholders can validate realized value throughout the migration and transformation lifecycle.  
B. Risk management

#### Explications

This capability addresses identification, assessment, and mitigation of threats, controls, and compliance requirements. It informs acceptable-risk decisions but focuses on risk posture and controls rather than establishing or tracking business outcome metrics.  
C. Application portfolio management

#### Explications

This capability inventories, assesses, and rationalizes applications to prioritize migrations, modernization, or retirement decisions. It supports technical and migration planning but is concerned with the application landscape rather than defining organization-level business outcomes and benefit realization.  
D. Cloud financial management

#### Explications

This capability concentrates on cost allocation, budgeting, optimization, and FinOps practices to manage cloud spend. It produces financial metrics and cost savings analysis but does not by itself define the broader strategic business outcomes or the non-financial benefits targeted by cloud adoption.  
Explication générale  
The question targets the AWS CAF governance perspective capability responsible for defining and tracking business outcomes. The correct governance function establishes measurable objectives, KPIs, ownership, and benefit-realization plans so organizations can verify that cloud investments deliver intended value. The other options (risk management, application portfolio management, cloud financial management) address risk/control, application planning, and cost control respectively—each important but not the primary mechanism for defining and tracking overall business outcomes.  
Domaine  
Domain 1: Cloud Concepts  
Question 70Ignoré  
**Which tasks are the responsibility of AWS according to the AWS shared responsibility model? (Choose two.)**  
A. Configure AWS Identity and Access Management (IAM).

#### Explications

Incorrect. Customers are responsible for configuring and managing identities, roles, policies, and permissions in IAM. AWS provides the IAM service but does not make access-control decisions for customer accounts—that configuration and ongoing user/role management is the customer's responsibility.  
B. Configure security groups on Amazon EC2 instances.

#### Explications

Incorrect. Security groups are virtual network firewalls attached to resources in a customer's account; creating and maintaining those rules (ingress/egress, associated instances) is managed by the customer. AWS provides the security group capability but not the specific rule configuration for each account.  
**Sélection correcte**  
C. Secure the access of physical AWS facilities.

#### Explications

Correct. AWS is responsible for physical controls and the security of its data centers (access control, facility monitoring, guards, environmental protections and physical hardware lifecycle). This falls under AWS’s responsibility for the security of the cloud.  
D. Patch applications that run on Amazon EC2 instances.

#### Explications

Incorrect. Patching operating systems and application software running on EC2 instances is the customer's responsibility because those run in the customer's guest environment. (AWS does patch the underlying host, virtualization layer, and infrastructure.)  
**Sélection correcte**  
E. Perform infrastructure patching and maintenance.

#### Explications

Correct. AWS manages and maintains the underlying cloud infrastructure (physical servers, network, storage, host OS/virtualization layer) including infrastructure-level patching and maintenance as part of its Security of the Cloud responsibilities.  
Explication générale  
This question tests the AWS Shared Responsibility Model: AWS is responsible for security of the cloud (physical facilities, infrastructure, and the host/virtualization layers), while customers are responsible for security in the cloud (identity/configuration, network rules, guest OS and application patching). Therefore the AWS responsibilities are the physical security of facilities and infrastructure patching/maintenance (answers C and E); the other options describe customer responsibilities.  
Domaine  
Domain 2: Security and Compliance  
Question 71Ignoré  
**Which pillar of the AWS Well-Architected Framework focuses on the ability to recover automatically from service interruptions?**  
A. Security

#### Explications

The Security pillar is about protecting data, identities, and infrastructure through controls such as IAM, encryption, logging, and threat detection. Those controls improve confidentiality, integrity, and security posture but do not primarily define strategies for automated recovery and fault tolerance.  
B. Performance efficiency

#### Explications

The Performance Efficiency pillar focuses on selecting right-sized resources, monitoring and tuning performance, and using scalable architectures to meet demand. It targets optimization and scalability rather than designing automatic recovery or failover mechanisms.  
C. Operational excellence

#### Explications

The Operational Excellence pillar covers operational processes: change management, runbooks, monitoring, incident response, and continual improvement. It informs how you operate and respond to events but does not itself prescribe the architectural redundancy and automated recovery mechanisms that provide resilience.  
**Bonne réponse**  
D. Reliability

#### Explications

The Reliability pillar defines design principles and practices to ensure a workload can withstand and recover from failures: fault isolation, redundancy, automated failover and recovery testing, backups, and defined RTO/RPO. It maps directly to AWS features (for example, Multi‑AZ deployments, Auto Scaling, Route 53 health checks, ELB failover, and automated backup/restore) that enable automatic recovery and sustained availability.  
Explication générale  
This question tests recognition of the Well‑Architected pillars and which one is concerned with resilience and automated recovery. Reliability is the pillar that focuses on fault tolerance, redundancy, automated failover, backup/recovery planning, and testing. The other pillars (Security, Performance Efficiency, Operational Excellence) address important but different concerns: protection of assets, efficient use of resources, and operational processes respectively.  
Domaine  
Domain 1: Cloud Concepts  
Question 72Ignoré  
**A global company wants to use a managed security service for protection from SQL injection attacks. The service also must provide detailed logging information about access to the company's ecommerce applications.**  
**Which AWS service will meet these requirements?**  
A. AWS Network Firewall

#### Explications

This is a stateful/ stateless network firewall for VPC traffic that operates at the network and transport layers. It can filter by IP, port, protocol and use Suricata-compatible rules for some intrusion prevention, but it does not inspect HTTP/HTTPS request bodies for application-layer attacks (for example SQL injection) nor provide per-request web access logging tailored to web application traffic.  
B. Amazon RDS for SQL Server

#### Explications

This is a managed relational database service. It provides database management, backups, encryption, and database-level logging/auditing, but it does not act as a web application firewall and cannot block or log HTTP requests to the ecommerce application that carry SQL injection attempts at the application layer.  
C. Amazon GuardDuty

#### Explications

This is a threat detection service that analyzes VPC Flow Logs, CloudTrail events and DNS logs to identify suspicious activity and anomalies. It provides detection and alerts but does not provide inline, request-level protection for HTTP/HTTPS traffic nor detailed per-request web access logs used to inspect or block SQL injection attempts.  
**Bonne réponse**  
D. AWS WAF

#### Explications

This service inspects HTTP/HTTPS requests at the application (Layer 7\) level, supports managed SQL‑injection rule sets and custom rules, and can block or allow traffic based on those rules. It also supports logging of web requests (via Amazon Kinesis Data Firehose delivery to S3, CloudWatch Logs, or third‑party sinks) so you can retain and analyze detailed access records for the ecommerce application.  
Explication générale  
The requirement is application-layer protection against SQL injection plus detailed per-request access logging. The correct choice is the web application firewall that inspects HTTP/HTTPS traffic, provides managed and custom SQLi rules, and can deliver detailed request logs. Network- or host-level services and threat-detection tools provide complementary protections but do not perform inline Layer 7 request inspection and logging the way a WAF does.  
Domaine  
Domain 2: Security and Compliance  
Question 73Ignoré  
**According to security best practices, how should an Amazon EC2 instance be given access to an Amazon S3 bucket?**  
A. Hard code an IAM user’s secret key and access key directly in the application, and upload the file.

#### Explications

Hard-coding an IAM user's access key and secret key inside application code or configuration embeds long-term credentials that cannot be rotated automatically, are likely to be leaked via code repos or AMIs, and violate AWS credential management best practices. AWS recommends avoiding static credentials and using temporary credentials instead.  
B. Store the IAM user’s secret key and access key in a text file on the EC2 instance, read the keys, then upload the file.

#### Explications

Storing long-term access keys in a text file on the instance exposes them to compromise if the instance or its filesystem is accessed, backed up, or included in an AMI. This approach also makes key rotation and centralized credential management difficult. Use instance-assigned roles and temporary credentials instead.  
**Bonne réponse**  
C. Have the EC2 instance assume a role to obtain the privileges to upload the file.

#### Explications

Attaching an IAM role to the EC2 instance (via an instance profile) is the recommended approach: the instance receives temporary, automatically rotated credentials (STS) through the EC2 Instance Metadata Service (use IMDSv2), and AWS SDKs can retrieve and refresh them. This enables least-privilege access without embedding long-term secrets.  
D. Modify the S3 bucket policy so that any service can upload to it at any time.

#### Explications

Making the bucket policy permissive enough that any service can upload is overly broad and insecure. S3 bucket policies should grant access to specific principals or conditions (for example a particular IAM role, account, or VPC endpoint). Overly permissive policies increase risk of unauthorized access and data exfiltration.  
Explication générale  
The secure, AWS-recommended method is to give the EC2 instance an IAM role (instance profile) so it obtains temporary credentials automatically. This enforces least privilege, enables automatic credential rotation, and avoids embedding long-term secrets. The distractors propose insecure patterns (hard-coded or file-stored keys) or overly permissive policies, both of which increase risk and complicate credential management.  
Domaine  
Domain 2: Security and Compliance  
Question 74Ignoré  
**A company has moved all its infrastructure to the AWS Cloud. To plan ahead for each quarter, the finance team wants to track the cost and usage data of all resources from previous months. The finance team wants to automatically generate reports that contains the data.**  
**Which AWS service or feature should the finance team use to meet these requirements?**  
A. Amazon Detective

#### Explications

Incorrect. Amazon Detective is a security analysis service that helps investigate and visualize security findings (for example, from Amazon GuardDuty). It does not provide cost or usage reporting or historical billing data.  
B. AWS Pricing Calculator

#### Explications

Incorrect. AWS Pricing Calculator is an estimation tool for forecasting costs of proposed or planned architectures before deployment. It does not provide historical cost or usage reports for resources already running in an account.  
**Bonne réponse**  
C. AWS Budgets

#### Explications

Correct. AWS Budgets lets finance teams define cost and usage budgets, track actual spend against those budgets, and receive automated alerts when thresholds are crossed. It integrates with AWS Cost and Usage data (and with Cost Explorer) to monitor historical and ongoing spend and can notify stakeholders via email or Amazon SNS—making it suitable for automated budget-based reporting and monitoring.  
D. AWS Savings Plans

#### Explications

Incorrect. AWS Savings Plans are a pricing commitment model that reduces costs for eligible compute usage in exchange for a commitment to a consistent amount of usage. They are a cost-optimization mechanism, not a tool for tracking or reporting historical cost and usage data.  
Explication générale  
This question tests knowledge of AWS billing and reporting tools. Among the given choices, AWS Budgets is the appropriate service for tracking cost and usage against defined budgets and for delivering automated alerts/reports based on actual spend. (For detailed, line-item historical exports you would use the AWS Cost and Usage Report; for interactive historical analysis and scheduled visual reports you can use Cost Explorer.)  
Domaine  
Domain 4: Billing, Pricing, and Support  
Question 75Ignoré  
**A company needs to plan, schedule, and run hundreds of thousands of computing jobs on AWS.**  
**Which AWS service can the company use to meet this requirement?**  
A. AWS Step Functions

#### Explications

Step Functions implements serverless orchestration (state machines) to coordinate tasks and services with built-in error handling and visual workflows. It is optimized for sequencing and orchestrating distributed work, not for submitting, scheduling, and provisioning compute to execute very large volumes of batch jobs.  
B. AWS Service Catalog

#### Explications

Service Catalog provides a centralized catalog of approved IT resources (CloudFormation-based portfolios) for governance and standardized provisioning. It is intended for product/IT service management and compliance, not for job scheduling or running batch compute workloads.  
C. Amazon Simple Queue Service (Amazon SQS)

#### Explications

Amazon SQS is a managed message queue for decoupling components and buffering work. While it can hold work items for workers to consume, it does not provide job definitions, scheduling, dependency handling, or automatic provisioning of compute resources required to run and scale hundreds of thousands of batch jobs.  
**Bonne réponse**  
D. AWS Batch

#### Explications

AWS Batch is purpose-built for batch computing: it accepts job submissions, uses job definitions and job queues, and runs jobs on managed compute environments that automatically provision EC2 (including Spot) or Fargate instances. It performs scheduling, dependency management, retries, and autoscaling to efficiently run very large numbers of batch jobs.  
Explication générale  
This question tests which AWS service is designed for high-throughput batch compute. AWS Batch is the correct choice because it provides job definitions, job queues, scheduling, and managed compute environments that automatically provision and scale compute (EC2/Spot/Fargate) to run hundreds of thousands of jobs. The other options focus on orchestration (Step Functions), governance/catalog management (Service Catalog), or messaging/decoupling (SQS), and therefore do not provide the integrated scheduling and compute provisioning features required for massive batch workloads.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 76Ignoré  
**Which option is a shared responsibility between AWS and its customers under the AWS shared responsibility model?**  
A. Configuration of Amazon EC2 instance operating systems

#### Explications

Managing the guest operating system on an EC2 instance (OS configuration, installed packages, user accounts, and OS-level security settings) is the customer's responsibility under the shared responsibility model. AWS is responsible for the underlying physical host, network, and hypervisor, not the customer-managed OS running on virtual instances.  
B. Application file system server-side encryption

#### Explications

Encryption at the application or filesystem level is generally implemented and configured by the customer. AWS offers service-level encryption features (for example, SSE-S3, SSE-KMS, EBS encryption) and key management via AWS KMS, but application-level/file-system encryption and how keys are used within an application's runtime are controlled by the customer and thus not inherently a shared operational responsibility in the same way as infrastructure tasks.  
**Bonne réponse**  
C. Patch management

#### Explications

Patch management is a classic shared responsibility: AWS patches and maintains the physical infrastructure, hypervisor, and the managed service control planes, while customers must patch their guest operating systems, middleware, libraries, and applications on compute resources they manage (such as EC2 instances, containers, or on-premises components). For AWS managed services (for example, RDS, Elastic Beanstalk), AWS may handle OS and database engine patching according to service scope and configuration.  
D. Security of the physical infrastructure

#### Explications

Physical data center security, hardware maintenance, and the physical network are controlled and secured by AWS as part of the 'security of the cloud.' Customers do not manage physical access, facility controls, or hardware lifecycle of AWS data centers.  
Explication générale  
The AWS shared responsibility model splits security and operational duties: AWS is responsible for security 'of' the cloud (physical facilities, hardware, network, and managed service control planes) while customers are responsible for security 'in' the cloud (guest OS, applications, data, and configurations). Patch management is shared because AWS maintains and patches the underlying infrastructure and managed service control planes, whereas customers must patch guest operating systems and application components. The other options are either solely the customer's responsibility (guest OS configuration, application-level encryption choices) or solely AWS's responsibility (physical infrastructure).  
Domaine  
Domain 2: Security and Compliance  
Question 77Ignoré  
**A company wants to use Amazon EC2 instances to provide a static website to users all over the world. The company needs to minimize latency for the users.**  
**Which solution meets these requirements?**  
A. Use EC2 instances in multiple edge locations.

#### Explications

Incorrect — Les instances Amazon EC2 s’exécutent dans les régions et zones de disponibilité AWS, et non dans les points de présence CloudFront. Ces points de présence hébergent les caches CDN et les ressources de calcul en périphérie (CloudFront, Lambda@Edge). Pour minimiser la latence globale du contenu statique, il est nécessaire d’utiliser un CDN qui met en cache les données dans ces points de présence, plutôt que de déployer des instances EC2 en périphérie.  
B. Utilisez des instances EC2 dans la même zone de disponibilité, mais dans des régions AWS différentes.

#### Explications

Incorrect — Cette affirmation est incohérente (les zones de disponibilité sont spécifiques à une région) et le déploiement d'instances entre régions nécessite une réplication et une configuration du routage du trafic (routage basé sur la latence Route 53 ou Global Accelerator). Cette approche complexifie le système sans pour autant offrir la mise en cache automatique en périphérie et la distribution à faible latence qu'un CDN propose pour les ressources statiques.  
**Bonne réponse**  
C. Utilisez Amazon CloudFront avec les instances EC2 configurées comme source.

#### Explications

Exact — Amazon CloudFront est un réseau de distribution de contenu (CDN) mondial qui met en cache les objets statiques sur des serveurs périphériques à travers le monde. Configurer une instance EC2 comme origine permet à CloudFront d'effectuer une extraction du cache vers l'origine, réduisant ainsi la latence pour les utilisateurs, la charge sur l'origine et offrant des fonctionnalités supplémentaires telles que la terminaison TLS, la prise en charge HTTP/2/3, le contrôle du cache et une protection DDoS intégrée (AWS Shield Standard).  
D. Utilisez des instances EC2 dans la même zone de disponibilité, mais dans des comptes AWS différents.

#### Explications

Incorrect — Placer des instances dans différents comptes AWS ou les conserver dans la même zone de disponibilité n’améliore pas la latence globale. Les déploiements inter-comptes servent à l’isolation, à la facturation et à la gouvernance, et non à l’amélioration des performances à l’échelle mondiale. Améliorer les temps de réponse globaux nécessite la mise en cache en périphérie ou des services de routage/réplication globaux, et non la séparation des comptes.  
Explication générale  
Pour diffuser un site web statique avec une latence globale minimale, il est nécessaire de mettre en cache le contenu au niveau des points de présence. Amazon CloudFront est le CDN conçu à cet effet et peut utiliser une instance EC2 comme origine (extraction depuis l'origine). Les autres solutions proposent de déplacer ou d'isoler les instances EC2 (ou contiennent des informations incorrectes concernant les zones de disponibilité et les régions), ce qui ne permet pas de bénéficier de la mise en cache globale automatique et des performances offertes par CloudFront.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 78Ignoré  
**Quelles affirmations illustrent la rentabilité du cloud AWS ?**  
**(Choisissez deux réponses.)**  
**Sélection correcte**  
A. Les utilisateurs peuvent échanger des dépenses fixes contre des dépenses variables.

#### Explications

Exact. Les modèles de tarification d'AWS (à la demande, à l'usage et facturation à la consommation) permettent aux clients d'éviter d'importantes dépenses d'investissement initiales et d'engager plutôt des coûts qui évoluent en fonction de l'utilisation réelle, améliorant ainsi l'adéquation des coûts et la gestion des flux de trésorerie.  
B. Les utilisateurs peuvent déployer leurs solutions partout dans le monde en quelques minutes.

#### Explications

Incorrect. La rapidité de déploiement global est un avantage en termes d'agilité et de disponibilité — elle réduit le délai de mise sur le marché et améliore la latence — mais ce n'est pas un mécanisme principal pour réduire les coûts pour le client.  
C. AWS offre une vitesse et une agilité accrues.

#### Explications

Incorrect. L'augmentation de la vitesse et de l'agilité génère des avantages opérationnels (innovation plus rapide, cycles de développement plus courts), qui peuvent indirectement affecter les coûts, mais il ne s'agit pas de caractéristiques directes de tarification ou de structure de coûts du cloud AWS.  
D. AWS est responsable de la mise à jour de l'infrastructure.

#### Explications

Incorrect. Dans le cadre du modèle de responsabilité partagée d'AWS, AWS gère et met à jour l'infrastructure physique sous-jacente et les services gérés, mais les clients restent responsables de la mise à jour des systèmes d'exploitation et des applications sur les ressources IaaS. Il s'agit d'une question de responsabilité en matière de sécurité et d'exploitation, et non d'un principe fondamental de rentabilité.  
**Sélection correcte**  
E. Les utilisateurs bénéficient d'économies d'échelle.

#### Explications

Exact. AWS tire parti de son envergure massive et de la demande agrégée pour réduire les coûts unitaires (matériel, réseau, énergie) et peut répercuter les économies sur ses clients grâce à des niveaux de prix inférieurs, des remises sur volume, des instances réservées et des plans d'économies.  
Explication générale  
La rentabilité d'AWS repose sur la tarification et l'échelle : les clients paient uniquement ce qu'ils consomment (ce qui minimise les investissements initiaux et aligne les coûts sur l'utilisation) et bénéficient des économies d'échelle d'AWS qui réduisent les coûts unitaires. Les autres options décrivent des avantages réels d'AWS (portée mondiale, agilité et responsabilités opérationnelles), mais n'expliquent pas directement comment AWS rend l'exécution des charges de travail plus rentable.  
Domaine  
Domaine 4 : Facturation, tarification et assistance  
Question 79Ignoré  
**Une entreprise souhaite organiser ses utilisateurs afin de pouvoir leur attribuer des autorisations en groupe.**  
**Quel service ou outil AWS peut-elle utiliser pour répondre à ce besoin ?**  
A. Groupes de sécurité

#### Explications

Un pare-feu virtuel au niveau du réseau qui contrôle le trafic entrant et sortant des ressources de calcul et autres. Il applique des règles de trafic, et non l'identité des utilisateurs ; il ne peut donc pas être utilisé pour organiser les utilisateurs ni pour attribuer des autorisations aux comptes humains.  
**Bonne réponse**  
B. Gestion des identités et des accès AWS (IAM)

#### Explications

Le service d'identité AWS permet de gérer l'authentification et l'autorisation. Il permet aux administrateurs de créer des utilisateurs, de définir des groupes (regroupements logiques de ces utilisateurs), d'associer des politiques (gérées ou intégrées) à ces groupes et ainsi d'octroyer des autorisations cohérentes et basées sur le principe du moindre privilège à tous les membres du groupe. Ceci répond directement au besoin d'organiser les utilisateurs pour la gestion des permissions.  
C. Groupes de ressources

#### Explications

Un outil permettant de regrouper les ressources AWS (par étiquettes ou autres critères) afin de simplifier leur gestion et leur automatisation. Il est destiné à l'organisation des ressources et aux tâches opérationnelles, et non à la gestion des comptes utilisateurs ou à l'attribution des autorisations IAM.  
D. AWS Security Hub

#### Explications

Ce service centralise les informations relatives à la sécurité et à la conformité des comptes et services. Il met en évidence les alertes et les normes de conformité, mais ne propose pas de fonctionnalités de gestion des identités, des groupes d'utilisateurs ou des permissions.  
Explication générale  
La solution adéquate est le service d'identité AWS, qui prend en charge les utilisateurs, les groupes, les rôles et les politiques, permettant ainsi aux administrateurs de regrouper les utilisateurs et d'attribuer des autorisations de manière centralisée. Les autres options concernent un pare-feu réseau (contrôle du trafic), l'organisation des ressources et les outils d'évaluation de la sécurité ; aucune ne gère le regroupement des utilisateurs ni l'attribution des autorisations.  
Domaine  
Domaine 2 : Sécurité et conformité  
Question 80Ignoré  
**Which options are AWS Cloud Adoption Framework (AWS CAF) people perspective capabilities? (Choose two.)**  
**Sélection correcte**  
A. Organizational alignment

#### Explications

This capability belongs to the people perspective because it addresses aligning teams, roles, responsibilities, and reporting relationships across the enterprise to support cloud initiatives, enabling clear accountability and collaboration during adoption and change management.  
B. Portfolio management

#### Explications

This is a business-facing capability concerned with prioritizing investments, product and service portfolios, and return-on-investment decisions; it is normally mapped to the business perspective of the AWS CAF rather than the people perspective.  
**Sélection correcte**  
C. Organization design

#### Explications

This capability focuses on defining organizational structures, role definitions, skills matrices, and team composition so the workforce can operate and deliver in a cloud operating model—core topics in the people perspective.  
D. Risk management

#### Explications

Managing threats, controls, compliance and enterprise risk is primarily part of the governance/security perspectives; although people are involved, the capability targets risk frameworks and controls rather than workforce organization or skills.  
E. Modern application development

#### Explications

This describes technical practices (DevOps, CI/CD, microservices, platform architecture) that belong to the technology/platform perspective, not the people-focused capabilities of the AWS CAF.  
Explication générale  
The AWS Cloud Adoption Framework people perspective centers on workforce-related capabilities: organizational structures, role and responsibility alignment, staffing and skills development required for cloud adoption. The two correct choices map to those workforce and organizational-change capabilities. The other options represent capabilities in other CAF perspectives (business/portfolio management, governance/security, and technology/platform) and therefore are not correct for the people perspective.  
Domaine  
Domain 1: Cloud Concepts  
Question 81Ignoré  
**A company needs to set up dedicated network connectivity between its on-premises data center and the AWS Cloud. The network cannot use the public internet.**  
**Which AWS service or feature will meet these requirements?**  
A. AWS Transit Gateway

#### Explications

Transit Gateway is a regional routing hub that simplifies connectivity between multiple VPCs and on‑premises networks. It provides route propagation and centralized routing but does not itself create a dedicated physical circuit from your datacenter to AWS; a separate physical connection (Direct Connect or partner circuit) is required for that capability.  
B. AWS VPN

#### Explications

AWS Site-to-Site VPN establishes encrypted IPSec tunnels that typically traverse the public internet (or a customer-managed WAN). Because the tunnels use internet paths, this option does not satisfy a requirement that traffic must avoid the public internet. (VPN can be used over a Direct Connect link for redundancy, but the VPN mechanism itself is not a dedicated physical circuit.)  
C. Amazon CloudFront

#### Explications

Amazon CloudFront is a content delivery network for caching and delivering web content at edge locations. It does not provide a private network link or a dedicated on‑premises to AWS connection and is not applicable for direct datacenter-to-AWS connectivity requirements.  
**Bonne réponse**  
D. AWS Direct Connect

#### Explications

Direct Connect provisions a dedicated, physical network connection from your premises into AWS locations and supports private virtual interfaces to connect directly to VPCs (and Direct Connect Gateway for multi-region access). It bypasses the public internet, provides consistent bandwidth and lower latency, and therefore meets the requirement for a non-internet, dedicated connection.  
Explication générale  
The scenario requires a private, dedicated network link that does not traverse the public internet. The correct solution is the service that provisions a physical circuit and private virtual interfaces into AWS, providing predictable bandwidth and lower latency. Other choices either provide routing/functionality within AWS (Transit Gateway), rely on encrypted tunnels over the internet (VPN), or are unrelated (CloudFront), so they do not meet the non-internet dedicated connectivity requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 82Ignoré  
**A company needs to convert video files and audio files to a format that will play on smartphones.**  
**Which AWS service will meet this requirement?**  
A. Amazon Comprehend

#### Explications

Incorrect — Amazon Comprehend is a natural language processing service used to extract entities, sentiment, syntax, and key phrases from text. It does not provide media transcoding or convert audio/video file formats.  
B. Amazon Rekognition

#### Explications

Incorrect — Amazon Rekognition performs image and video analysis (label detection, face recognition, content moderation, activity detection) but does not transcode, repackage, or convert media into device-specific codecs/containers.  
**Bonne réponse**  
C. Amazon Elastic Transcoder

#### Explications

Correct — Elastic Transcoder is an AWS service that converts (transcodes) audio and video between codecs and container formats, supports device-specific presets (bitrate, resolution, codecs), and integrates with Amazon S3 for input/output, enabling creation of smartphone-compatible media. (For more advanced/professional workflows, AWS Elemental MediaConvert is a newer, feature-rich alternative.)  
D. Amazon Polly

#### Explications

Incorrect — Amazon Polly is a text-to-speech service that generates spoken audio from text; it does not convert existing video or audio files from one codec/container to another.  
Explication générale  
The requirement is to convert (transcode) existing audio and video files into formats playable on smartphones. That task is handled by an AWS transcoding service that changes codecs, containers, bitrates, and resolutions and integrates with S3. Elastic Transcoder provides those capabilities (with MediaConvert as a more advanced option). The other services listed perform text or media analysis or text-to-speech and do not perform format conversion.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 83Ignoré  
**What is the total volume of data that can be stored in Amazon S3?**  
A. 10 PB

#### Explications

This option asserts a fixed total-storage cap. Amazon S3 does not impose a predefined total-capacity limit; instead S3 is architected to scale to exabytes and beyond. The relevant S3 limit to be aware of is per-object size (maximum 5 TB), not a global storage quota.  
B. 50 PB

#### Explications

This option again presents a specific total-capacity value. S3’s design is to scale storage elastically for customers rather than enforce a fixed total-volume limit. Operational quotas that do exist (for example, default bucket count per account) do not constrain the aggregate bytes you can store.  
C. 100 PB

#### Explications

This choice proposes another fixed numeric cap. It is incorrect because S3 allows an unlimited number of objects and scales storage capacity as needed; there is no documented fixed upper bound on total stored data for an AWS account or across AWS.  
**Bonne réponse**  
D. Virtually unlimited

#### Explications

Amazon S3 does not enforce a single, fixed limit on the total volume of data you can store. It can scale to exabyte-level workloads and beyond, supports an unlimited number of objects, and has a maximum per-object size of 5 TB. Service quotas that do exist (for example, default bucket count or request-rate guidance per prefix) are separate from aggregate storage capacity.  
Explication générale  
The question tests understanding that Amazon S3 is a massively scalable object storage service without a predefined total-storage cap. The distractors list specific fixed totals, which are incorrect because S3 scales to exabytes and supports an effectively unlimited number of objects; the relevant technical limit is the maximum object size (5 TB), not total account storage.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 84Ignoré  
**Which of the following best describes the benefit of using the AWS Well-Architected Framework when designing cloud solutions?**  
A. It provides a structured approach for migrating on-premises data centers to AWS.

#### Explications

Incorrect. The Well-Architected Framework provides design principles and best practices across its five pillars (operational excellence, security, reliability, performance efficiency, cost optimization). Migration planning and execution are handled by separate AWS services and programs (for example AWS Application Migration Service, AWS Migration Hub, and the Migration Acceleration Program).  
**Bonne réponse**  
B. It offers a set of best practices and guidelines to help build secure, high-performing, resilient, and efficient infrastructure for applications on AWS.

#### Explications

Correct. The framework codifies the five pillars, offers prescriptive design principles and review questions, and is supported by the AWS Well-Architected Tool to identify architectural risks and recommend improvements that help make workloads secure, performant, resilient, and cost-effective.  
C. It automatically optimizes costs by adjusting resource allocations based on usage patterns.

#### Explications

Incorrect. The framework is advisory and does not change resources automatically. Automated scaling and optimization are provided by services such as Auto Scaling, AWS Compute Optimizer, and Cost Explorer; the framework guides how to apply best practices and which tools to use.  
D. It guarantees compliance with all regulatory standards across different industries.

#### Explications

Incorrect. While the framework includes security and compliance considerations, it does not itself enforce or guarantee regulatory compliance. Achieving compliance requires implementing controls, following applicable standards, and working within the AWS Shared Responsibility Model and any AWS compliance programs.  
Explication générale  
The AWS Well-Architected Framework is a best-practices framework centered on five pillars that helps architects evaluate and improve cloud architectures. It is an advisory tool (supported by the Well-Architected Tool) to identify risks and recommend remediations; it is not a migration service, an automatic optimization engine, or a compliance certification.  
Domaine  
Domain 1: Cloud Concepts  
Question 85Ignoré  
**A company wants to migrate to the AWS Cloud. The company needs the ability to acquire resources when the resources are necessary. The company also needs the ability to release those resources when the resources are no longer necessary.**  
**Which architecture concept of the AWS Cloud meets these requirements?**  
**Bonne réponse**  
A. Elasticity

#### Explications

This AWS architectural principle enables on‑demand provisioning and deprovisioning of resources so capacity can grow or shrink to match workload changes. In AWS this is implemented with services and features such as Amazon EC2 Auto Scaling, Application Auto Scaling (for ECS, DynamoDB, etc.), and serverless offerings like AWS Lambda that automatically scale — enabling cost efficiency by releasing capacity when it is no longer needed.  
B. Availability

#### Explications

Availability refers to the ability of a system to remain accessible and operational (high availability patterns such as multi‑AZ deployments, Elastic Load Balancing, Route 53 health checks). It describes uptime and fault tolerance, not the automatic acquisition and release of resources in response to demand.  
C. Reliability

#### Explications

Reliability describes the ability of a system to perform consistently and recover from failures (fault‑tolerant design, backups, retries, multi‑region architectures). It focuses on stability and recovery, not on dynamically scaling resources up and down based on workload.  
D. Durability

#### Explications

Durability is about long‑term persistence and protection against data loss (for example, Amazon S3’s high durability guarantees and EBS snapshots). It pertains to data resilience, not to provisioning or releasing compute/storage resources on demand.  
Explication générale  
The question targets the AWS concept that permits automatic acquisition and release of resources to match demand. The correct concept is the one implemented via Auto Scaling and serverless services, which provision capacity when needed and release it when not. The other choices describe different characteristics—availability (uptime), reliability (fault tolerance and recovery), and durability (data persistence)—which do not by themselves provide dynamic on‑demand resource provisioning.  
Domaine  
Domain 1: Cloud Concepts  
Question 86Ignoré  
**Which AWS service enables users to create copies of resources across AWS Regions?**  
A. Amazon ElastiCache

#### Explications

ElastiCache is an in-memory caching service (Redis, Memcached) used to improve application performance by storing frequently accessed data. It does not provide functionality to copy or recreate AWS resources across Regions; it only manages cache clusters within a region.  
**Bonne réponse**  
B. AWS CloudFormation

#### Explications

CloudFormation is an infrastructure-as-code service that defines and provisions AWS resources from templates. By deploying the same template in multiple Regions (creating stacks per Region), users can reproduce resource configurations across Regions. Note it recreates resources from a template rather than performing service-level data replication.  
C. AWS CloudTrail

#### Explications

CloudTrail records and stores AWS API activity for governance, compliance, and auditing. While it can be configured as a multi-Region trail to capture events from multiple Regions, it does not create or copy resources across Regions.  
D. AWS Systems Manager

#### Explications

Systems Manager provides operational tooling (Run Command, Automation, State Manager, Parameter Store, Patch Manager) to manage and automate tasks on resources. It helps operate resources but is not a service for copying or provisioning resource copies across Regions.  
Explication générale  
The question tests knowledge of which AWS service is used to reproduce infrastructure across Regions. CloudFormation (infrastructure as code) lets you define resource configurations in templates and deploy those templates in different Regions to recreate resources. The other options are different functional categories: ElastiCache is a caching service, CloudTrail is for API logging/auditing, and Systems Manager is for operational management; none are intended to provision resource copies across Regions. For data/state replication you would use service-specific replication (for example S3 Cross-Region Replication, RDS read replicas, or AWS Backup).  
Domaine  
Domain 3: Cloud Technology and Services  
Question 87Ignoré  
**A company is designing workloads in the AWS Cloud. The company wants the workloads to perform their intended function correctly and consistently throughout their lifecycle.**  
**Which pillar of the AWS Well-Architected Framework does this goal represent?**  
A. Operational excellence

#### Explications

Incorrect. Operational excellence addresses how you run and improve your systems and processes (procedures, automation, deployment practices, runbooks, CI/CD, monitoring for continuous improvement). Those practices help operations but do not specifically define workload correctness and lifecycle consistency, which is the focus of a different pillar.  
B. Security

#### Explications

Incorrect. Security focuses on protecting confidentiality, integrity, and availability through controls such as IAM, encryption, network protections, and logging. While security supports system integrity and availability, it does not primarily describe ensuring workloads perform their intended function correctly and consistently across their lifecycle.  
**Bonne réponse**  
C. Reliability

#### Explications

Exact. Le pilier Fiabilité vise à concevoir des systèmes qui exécutent leurs fonctions prévues de manière correcte et constante dans le temps. Il englobe la tolérance aux pannes, la reprise automatique (auto-réparation), les sauvegardes et restaurations, la gestion des capacités et des quotas, la gestion des changements et des incidents éprouvée, ainsi que la surveillance. Parmi les fonctionnalités AWS qui contribuent à la fiabilité, on trouve Auto Scaling, Elastic Load Balancing, les architectures multi-AZ/multi-régions, les contrôles d'intégrité Route 53 et les alarmes et métriques CloudWatch.  
D. Efficacité de la performance

#### Explications

Incorrect. L'efficacité des performances repose sur le choix des types et des tailles de ressources appropriés, la surveillance des performances et la mise à l'échelle pour répondre à la demande (optimisation du débit et de la latence). Elle vise l'efficacité et l'optimisation plutôt que la correction, la tolérance aux pannes ou la cohérence du cycle de vie des charges de travail.  
Explication générale  
Cette question s'inscrit dans le cadre du référentiel AWS Well-Architected : garantir le bon fonctionnement et la cohérence des charges de travail tout au long de leur cycle de vie est au cœur du pilier Fiabilité (tolérance aux pannes, reprise après sinistre, gestion des changements et conception résiliente). Les autres piliers sont liés à ce pilier, mais se concentrent sur des aspects différents : l'Excellence opérationnelle porte sur les processus et leur amélioration, la Sécurité sur la protection des actifs et l'Efficacité des performances sur l'optimisation des ressources.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 88Ignoré  
**Quelles actions relèvent de la responsabilité d'AWS, selon le modèle de responsabilité partagée d'AWS ? (Choisissez deux réponses.)**  
**Sélection correcte**  
A. Sécurisation de la couche de virtualisation

#### Explications

AWS est responsable de la sécurisation de l'infrastructure sous-jacente — y compris les centres de données, les hôtes physiques et la couche hyperviseur/virtualisation — dans le cadre de ses responsabilités en matière de « sécurité du cloud » (conception, exploitation et mise à jour du plan de contrôle et de l'hyperviseur).  
B. Application de correctifs au système d'exploitation des instances Amazon EC2

#### Explications

Il s'agit d'une responsabilité du client : la mise à jour et le renforcement du système d'exploitation invité sur les instances EC2 relèvent de la « sécurité dans le cloud » (les clients gèrent le système d'exploitation, les applications et la configuration associée même si AWS fournit des outils comme Systems Manager pour les aider).  
C. Mise en œuvre d'une politique de mots de passe stricte pour les utilisateurs IAM

#### Explications

La gestion et l'application des politiques IAM spécifiques au compte (complexité du mot de passe, rotation, MFA) sont effectuées par le client à l'aide des fonctionnalités AWS IAM ; AWS fournit le service IAM mais ne définit ni n'applique la politique de mot de passe d'un compte individuel pour vous.  
**Sélection correcte**  
D. Application de correctifs au système d'exploitation sur les instances Amazon RDS

#### Explications

Amazon RDS est un service de base de données géré, et AWS prend en charge les tâches de maintenance du système d'exploitation et du moteur de base de données sous-jacents (y compris les correctifs de sécurité et les mises à jour de routine) pour les instances RDS standard, sauf si vous optez pour une configuration gérée personnalisée.  
E. Configuration des groupes de sécurité et des listes de contrôle d'accès réseau

#### Explications

La configuration des contrôles d'accès au niveau du réseau (groupes de sécurité et listes de contrôle d'accès réseau) est à la charge du client ; AWS fournit le VPC et les primitives de sécurité, mais les clients définissent et maintiennent les règles qui contrôlent le trafic.  
Explication générale  
This question tests the AWS shared responsibility model: AWS handles ‘security of the cloud’ (physical infrastructure, hypervisor, and maintenance for managed services like RDS), while customers handle ‘security in the cloud’ (guest OS on EC2, IAM policies, security groups/NACLs). Therefore the correct AWS responsibilities are the virtualization/physical infrastructure and managed-service patching (A and D); the other options describe customer-managed duties.  
Domaine  
Domain 2: Security and Compliance  
Question 89Ignoré  
**To reduce costs, a company is planning to migrate a NoSQL database to AWS.**  
**Which AWS service is fully managed and can automatically scale throughput capacity to meet database workload demands?**  
A. Amazon Redshift

#### Explications

This service is a fully managed, columnar data warehouse designed for OLAP and large-scale analytics. It optimizes complex queries and large datasets rather than providing a NoSQL key-value/document store or automatic, request-level throughput autoscaling suitable for transactional NoSQL workloads.  
B. Amazon Aurora

#### Explications

This is a MySQL/PostgreSQL-compatible relational engine that provides high performance for relational workloads. While it offers features like serverless/autoscaling variants for compute, it is not a NoSQL database and does not provide the NoSQL-style automatic throughput scaling (on-demand or auto-scaling capacity modes) required by NoSQL migrations.  
**Bonne réponse**  
C. Amazon DynamoDB

#### Explications

This fully managed key-value and document database provides single-digit millisecond performance and two built-in scaling models: on-demand capacity (automatic scaling of request capacity in response to traffic) and provisioned capacity with auto scaling. Those features make it the appropriate AWS service for migrating NoSQL workloads that need automatic throughput scaling.  
D. Amazon RDS

#### Explications

This is a managed relational database service for traditional SQL engines (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server). It supports read replicas and some automated maintenance, but it is not a NoSQL store and does not offer the same automatic request-level throughput autoscaling used for NoSQL workloads.  
Explication générale  
The question tests recognition of the AWS service best suited for NoSQL migrations that requires automatic throughput scaling. The correct service is the managed NoSQL key-value/document database that offers on-demand capacity and auto-scaling for provisioned capacity, enabling cost-effective scaling with unpredictable or variable traffic. The other options are relational databases or a data warehouse optimized for analytical queries and therefore are not appropriate when automatic NoSQL throughput scaling is the requirement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 90Ignoré  
**A company that has multiple business units wants to centrally manage and govern its AWS Cloud environments. The company wants to automate the creation of AWS accounts, apply service control policies (SCPs), and simplify billing processes.**  
**Which AWS service or tool should the company use to meet these requirements?**  
**Bonne réponse**  
A. AWS Organizations

#### Explications

AWS Organizations provides centralized management of multiple AWS accounts by grouping them into organizational units (OUs), enabling programmatic account creation via the CreateAccount API, enforcing governance with Service Control Policies (SCPs), and consolidating billing under a management (payer) account. It integrates with services like AWS Control Tower for automated landing-zone setup but the core features for account lifecycle and policy enforcement come from AWS Organizations.  
B. Cost Explorer

#### Explications

Cost Explorer is a cost-visualization and analysis tool used to view, filter, and forecast AWS spending and usage. It does not provide account lifecycle management, organization-wide policy enforcement (SCPs), or automated account creation capabilities.  
C. AWS Budgets

#### Explications

AWS Budgets lets you set cost and usage thresholds and receive alerts (for example via Amazon SNS) when those thresholds are exceeded. It is focused on cost controls and notifications, not on creating or governing AWS accounts or applying organization-level policies.  
D. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor performs account-level best-practice checks and gives optimization recommendations across cost, performance, security, and fault tolerance. It is an advisory service and does not manage accounts, enforce SCPs, or automate account provisioning.  
Explication générale  
The question tests knowledge of centralized account governance: AWS Organizations is the service designed to centrally create and manage accounts, apply SCPs for governance, and consolidate billing. The other options (Cost Explorer, AWS Budgets, Trusted Advisor) are cost/optimization or advisory tools and do not provide account provisioning or organization-level policy enforcement.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 91Ignoré  
**A company wants to automate infrastructure deployment by using infrastructure as code (IaC). The company wants to scale production stacks so the stacks can be deployed in multiple AWS Regions.**  
**Which AWS service will meet these requirements?**  
A. Amazon CloudWatch

#### Explications

Amazon CloudWatch is an observability service that collects metrics, logs, and alarms and can trigger actions, but it is not an infrastructure-as-code tool and does not provision or manage CloudFormation stacks across regions.  
B. AWS Config

#### Explications

AWS Config provides resource inventory, configuration history, and compliance evaluation (Config Rules). It records and assesses resource states but does not define or deploy infrastructure templates or orchestrate multi-region stack deployments.  
C. AWS Trusted Advisor

#### Explications

AWS Trusted Advisor analyzes your AWS environment and delivers best-practice recommendations for cost, performance, security, and fault tolerance. It is an advisory service and does not perform provisioning or manage infrastructure as code.  
**Bonne réponse**  
D. AWS CloudFormation

#### Explications

AWS CloudFormation uses declarative templates to model and provision AWS resources as code. For multi-region or multi-account deployments it supports AWS CloudFormation StackSets, enabling automated creation, update, and deletion of stacks across multiple Regions and accounts with change-set management, drift detection, and rollback capabilities.  
Explication générale  
The question tests knowledge of AWS services for infrastructure-as-code and multi-region stack deployment. AWS CloudFormation is the IaC service that models and provisions resources via templates; its StackSets feature specifically enables deploying and scaling stacks across multiple AWS Regions and accounts. The other options are monitoring, configuration auditing, or advisory services and do not provision or manage stacks.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 92Ignoré  
**Which combination of AWS services can be used to move a commercial relational database to an Amazon-managed open-source database? (Choose two.)**  
**Sélection correcte**  
A. AWS Database Migration Service (AWS DMS)

#### Explications

AWS Database Migration Service (DMS) is the purpose-built service for moving data between database engines and to Amazon-managed targets. It supports full-load plus ongoing change-data-capture (CDC) replication to minimize downtime, performs data validation, and integrates with other AWS migration tools to deliver reliable migrations to RDS or Amazon Aurora.  
B. AWS software development kits (SDKs)

#### Explications

AWS SDKs are programming libraries that let applications call AWS APIs and automate tasks. They are not a migration product and do not provide built-in schema conversion, continuous replication, or migration orchestration capabilities required for a database engine migration.  
**Sélection correcte**  
C. AWS Schema Conversion Tool

#### Explications

AWS Schema Conversion Tool (SCT) analyzes database metadata and converts database schema and database code (for example, stored procedures and functions) from a source engine to a compatible schema on the target. SCT produces assessment reports and converted DDL, and is commonly used together with DMS for heterogeneous migrations.  
D. AWS Systems Manager

#### Explications

AWS Systems Manager delivers operational tooling for managing and automating infrastructure (Run Command, Session Manager, Automation, Parameter Store). It is not designed to convert database schemas or perform ongoing data replication and therefore is not suitable as the primary database migration tool.  
E. Amazon EMR

#### Explications

Amazon EMR is a managed service for big-data processing (Hadoop, Spark, etc.) and analytics workflows. It is intended for large-scale data processing and not for transactional relational database schema conversion or continuous database migration.  
Explication générale  
The correct solution pairs a schema-conversion capability with a data-migration engine: use the Schema Conversion Tool to assess and convert database schema and database code for a heterogeneous target, and use AWS DMS to perform the data migration (initial load and CDC) to the Amazon-managed open-source database. The other options relate to SDKs, operational management, or big-data processing and do not provide the combined schema conversion plus data-replication functionality required for this scenario.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 93Ignoré  
**A company has been storing monthly reports in an Amazon S3 bucket. The company exports the report data into comma-separated values (.csv) files. A developer wants to write a simple query that can read all of these files and generate a summary report.**  
**Which AWS service or feature should the developer use to meet these requirements with the LEAST amount of operational overhead?**  
A. Amazon S3 Select

#### Explications

Incorrect. S3 Select allows running SQL-like queries against the contents of a single S3 object to retrieve only the data needed, which reduces data transfer for single-file access. It does not natively perform queries across multiple objects, so using it to summarize many CSV files would require orchestration or custom code to iterate over objects, increasing operational overhead.  
**Bonne réponse**  
B. Amazon Athena

#### Explications

Correct. Amazon Athena is a serverless, interactive query service (Presto/Trino-based) that runs ANSI SQL directly against data stored in S3. It can read many files in common formats (CSV, Parquet, ORC) without loading data or managing servers, integrates with the AWS Glue Data Catalog for schema management, and charges per data scanned—minimizing operational and administrative overhead for ad hoc summary queries.  
C. Amazon Redshift

#### Explications

Incorrect. Amazon Redshift is a managed, provisioned data warehouse that requires loading data into a cluster and managing cluster resources (provisioning, scaling, maintenance). While performant for large-scale analytics, it introduces more setup and operational management than a serverless S3-query solution for simple ad hoc CSV summaries.  
D. Amazon EC2

#### Explications

Incorrect. Using Amazon EC2 would require provisioning and managing virtual machines, installing and maintaining query tools or databases, and handling scaling, availability, and patching. This approach has substantially higher operational overhead compared with serverless services tailored for querying data in S3.  
Explication générale  
This scenario requires running SQL-style queries across multiple CSV files in S3 with minimal operational work. A serverless query service that reads files in place and requires no infrastructure management is the best fit. Athena provides that capability (reads multiple files, uses SQL, integrates with Glue, and is billed per data scanned). S3 Select is limited to single-object queries, while Redshift and EC2 require provisioning and ongoing management, increasing overhead.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 94Ignoré  
**Which option is a physical location of the AWS global infrastructure?**  
A. AWS DataSync

#### Explications

AWS DataSync is a managed data transfer service used to move large amounts of data between on-premises storage and AWS storage services (for example, Amazon S3, Amazon EFS). It is an application-level service and does not represent a physical location in AWS’s global infrastructure.  
**Bonne réponse**  
B. AWS Region

#### Explications

A Region is a geographically distinct area that contains multiple Availability Zones (physically separated data centers). Regions are the primary physical units of the AWS global infrastructure used to meet latency, resilience, and data-residency requirements.  
C. Amazon Connect

#### Explications

Amazon Connect is a cloud-based contact center service for building customer contact solutions. It is an AWS service (software) and does not denote a physical data center or geographic location.  
D. AWS Organizations

#### Explications

AWS Organizations is a management service for consolidating and centrally governing multiple AWS accounts. It is an account-management feature, not a physical infrastructure location.  
Explication générale  
The question tests knowledge of AWS global infrastructure terminology. The correct choice identifies the geographic, physical unit where AWS places its data centers (Regions, which contain multiple Availability Zones). The other choices are AWS services or account-management features and therefore are not physical locations.  
Domaine  
Domain 1: Cloud Concepts  
Question 95Ignoré  
**Which option is a customer responsibility under the AWS shared responsibility model?**  
**(Choose two.)**  
A. Maintenance of underlying hardware of Amazon EC2 instances

#### Explications

Incorrect — Responsibility for the physical servers, racks, host hardware and the underlying virtualization infrastructure lies with AWS. Customers do not manage or maintain the EC2 host hardware or the hypervisor layer.  
**Sélection correcte**  
B. Application data security

#### Explications

Correct — Protecting customer data and the security of applications running in the cloud is the customer’s responsibility. This includes data classification, encryption (client-side or AWS KMS), access control via IAM, secure application configuration, and backups.  
C. Physical security of data centers

#### Explications

Incorrect — AWS is responsible for data-center physical security, including facility access controls, environmental protections, and physical asset protection as part of AWS’s management of the global infrastructure.  
**Sélection correcte**  
D. Maintenance of VPC components

#### Explications

Correct — Customers design, configure, and maintain their VPC networking constructs (subnets, route tables, security groups, network ACLs, peering, VPNs). AWS provides and secures the underlying network fabric but customers manage VPC components and their configurations.  
Explication générale  
This question tests the shared responsibility model: AWS is responsible for security of the cloud (physical facilities, host hardware, underlying virtualization, and AWS-managed services), while customers are responsible for security in the cloud (their data, applications, guest OS, IAM, and network configuration). Options B and D describe customer responsibilities; options A and C describe AWS responsibilities.  
Domaine  
Domain 2: Security and Compliance  
Question 96Ignoré  
**Which AWS service is always provided at no charge?**  
A. Amazon S3

#### Explications

Object storage (Amazon S3) is billed by usage — GB-months of storage, request types, data retrieval, and data transfer — so it is not provided at no charge except for limited free-tier allowances.  
**Bonne réponse**  
B. AWS Identity and Access Management (IAM)

#### Explications

IAM is an account-level identity and access control feature provided without additional cost. You can create users, groups, roles, and policies at no charge. (Note: some complementary identity services such as AWS Directory Service or certain identity federation integrations may incur fees.)  
C. Elastic Load Balancers

#### Explications

Elastic Load Balancing incurs charges based on load balancer hours and capacity (LCUs) or per-hour/per-GB metrics depending on type; it is a metered service, not always free.  
D. AWS WAF

#### Explications

AWS WAF is a managed web application firewall with pricing for web ACLs, rules, and request inspections; it is billed based on usage and not provided at no charge.  
Explication générale  
The question tests knowledge of which core AWS access control capability is provided at no additional cost. IAM is included with AWS accounts and enables creation of identities and access policies without service charges. The other listed services (S3, ELB, WAF) are metered and incur usage-based fees (though some offer limited free-tier usage), so they are not always free.  
Domaine  
Domain 2: Security and Compliance  
Question 97Ignoré  
**Which AWS service supports MySQL database engines?**  
A. Amazon Dynamo DВ

#### Explications

Incorrect — Amazon DynamoDB is a fully managed NoSQL key-value and document database that delivers single-digit millisecond performance at scale. It does not provide a managed relational MySQL engine or MySQL-compatible SQL interface.  
**Bonne réponse**  
B. Amazon RDS

#### Explications

Correct — The managed relational database service offers MySQL as a supported engine option and provides relational-database features such as automated backups, Multi-AZ high availability, read replicas, automated patching, and scaling of compute and storage.  
C. Amazon DocumentDB (with MongoDB compatibility)

#### Explications

Incorrect — Amazon DocumentDB is a managed document database with compatibility for MongoDB APIs, designed for JSON/document workloads rather than providing a MySQL-compatible relational engine.  
D. Amazon ElastiCache

#### Explications

Incorrect — Amazon ElastiCache is a managed in-memory data store and caching service (Redis and Memcached) used to accelerate application performance; it is not a persistent relational database and does not host MySQL.  
Explication générale  
This question tests knowledge of AWS database offerings and which service provides a managed MySQL engine. The relational database service is the correct choice because it specifically supports MySQL and includes relational features (backups, Multi-AZ, replicas, patching). The other options are NoSQL (DynamoDB), document-store/MongoDB-compatible (DocumentDB), or in-memory cache services (ElastiCache), none of which provide a MySQL relational engine.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 98Ignoré  
**Which AWS service or feature can be used to monitor for potential disk write spikes on a system that is running on Amazon EC2?**  
A. AWS CloudTrail

#### Explications

CloudTrail records AWS API activity (management and optional data events) for auditing, security analysis, and compliance. It does not collect or emit real-time system performance metrics such as disk I/O on EC2 instances, so it cannot be used to detect disk write spikes.  
B. AWS Health Dashboard

#### Explications

The AWS Health Dashboard provides account- and service-level health notifications and guidance about AWS service events and scheduled changes. It does not gather instance-level performance metrics (for example, disk write activity) for EC2 systems.  
C. AWS Trusted Advisor

#### Explications

Trusted Advisor performs best-practice checks and gives optimization and security recommendations across your account. It is not a real-time monitoring system and does not report live disk I/O metrics or raise alarms on ephemeral spikes in disk writes.  
**Bonne réponse**  
D. Amazon CloudWatch

#### Explications

CloudWatch is the monitoring service that collects metrics and logs. It exposes EBS volume metrics (for example, VolumeWriteBytes and VolumeWriteOps) and—when the CloudWatch agent is installed—OS-level disk metrics from the instance. CloudWatch supports alarms, dashboards, and automated actions, enabling detection and notification when disk write activity spikes.  
Explication générale  
The tested concept is AWS monitoring: CloudWatch is the correct choice because it collects volume- and instance-level performance metrics (and can be extended with the CloudWatch agent), allows alarms and dashboards, and supports automated responses to spikes. The other options are for API/activity logging (CloudTrail), service health notifications (AWS Health Dashboard), or account-level best-practice checks (Trusted Advisor), none of which provide the required real-time disk I/O metrics.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 99Ignoré  
**A company has an AWS account. The company wants to audit its password and access key rotation details for compliance purposes.**  
**Which AWS service or tool will meet this requirement?**  
A. IAM Access Analyzer

#### Explications

Access Analyzer inspects resource-based and identity-based policies to identify unintended access paths and generates findings about external sharing or overly permissive policies. It does not produce historical data about IAM user passwords or access-key rotation dates, so it cannot be used to audit rotation compliance.  
B. AWS Artifact

#### Explications

AWS Artifact provides on-demand access to AWS compliance reports and certificates (for example, SOC, ISO, PCI) and contractual agreements. It is a compliance documentation portal and does not expose per-user credential metadata such as password or access key rotation history.  
**Bonne réponse**  
C. IAM credential report

#### Explications

The IAM credential report is a built-in IAM feature that generates a CSV containing each IAM user and fields like password\_enabled, password\_last\_changed, password\_last\_used, access\_key\_1\_active, access\_key\_1\_last\_rotated, access\_key\_1\_last\_used\_date (and equivalent for access\_key\_2). It is the direct, authoritative source for auditing password and access key rotation and can be produced via the console, CLI (aws iam generate-credential-report), or API.  
D. AWS Audit Manager

#### Explications

AWS Audit Manager automates evidence collection and maps AWS resources to audit controls and frameworks. While useful for broader audit workflows and control mapping, it requires configuration and is not the immediate source of per-user credential rotation timestamps—so it’s not the most direct tool for this specific audit requirement.  
Explication générale  
The question tests knowledge of which AWS tool provides per-user credential rotation details. The IAM credential report is the precise, authoritative output that lists password and access key last-changed/last-rotated timestamps for each IAM user. Other services mentioned address policy analysis (Access Analyzer), compliance documentation (Artifact), or audit automation (Audit Manager) but do not directly provide the detailed rotation history required for this compliance audit.  
Domaine  
Domain 2: Security and Compliance  
Question 100Ignoré  
**A company runs thousands of simultaneous simulations using AWS Batch. Each simulation is stateless, is fault tolerant, and runs for up to 3 hours.**  
**Which pricing model enables the company to optimize costs and meet these requirements?**  
A. Reserved Instances

#### Explications

Reserved Instances are a billing/discount mechanism that requires a one- or three-year commitment to a specific instance family, region, and tenancy (Standard or Convertible RIs). They provide lower hourly rates for steady-state, predictable workloads but lack the flexibility and cost-efficiency for large-scale, highly variable, short-duration, fault-tolerant batch jobs.  
**Bonne réponse**  
B. Spot Instances

#### Explications

Spot Instances use spare EC2 capacity offered at deep discounts and can be reclaimed by AWS with a short (typically two-minute) interruption notice. Because the simulations are stateless and fault tolerant, AWS Batch can restart or reschedule interrupted jobs onto other Spot or On‑Demand capacity, making Spot the most cost-effective choice for this workload.  
C. On-Demand Instances

#### Explications

On‑Demand Instances provide pay-as-you-go capacity without long-term commitments and no interruption risk from AWS, which is appropriate when jobs cannot tolerate interruption. However, they are more expensive than Spot for large-scale, interruptible workloads and therefore do not optimize cost as well in this scenario.  
D. Dedicated Instances

#### Explications

Dedicated Instances/Hosts provide physical isolation by running on hardware dedicated to a single customer and are used for specific compliance or licensing requirements. They carry a higher cost and do not offer the flexibility or price advantages needed for interruptible, cost-sensitive batch simulations.  
Explication générale  
This question tests selection of the EC2 pricing model that best matches a large-scale, stateless, fault-tolerant batch workload. Spot Instances are the optimal choice because they deliver the largest cost savings on spare EC2 capacity and integrate with AWS Batch to handle interruptions. The other options (Reserved, On‑Demand, Dedicated) are for steady-state savings, non‑interruptible needs, or dedicated isolation and therefore are less appropriate for the described simulations.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 101Ignoré  
**Une entreprise souhaite déployer une application dans plusieurs zones de disponibilité d'une même région AWS.**  
**Quel avantage ce déploiement lui apportera-t-il ?**  
A. Amélioration des performances de connexion pour les clients internationaux

#### Explications

Incorrect. Le déploiement de ressources dans plusieurs zones de disponibilité au sein d'une même région ne résout pas les problèmes de latence globale ni d'amélioration des performances de connexion. Les zones de disponibilité correspondent à des emplacements de centres de données distincts au sein d'une même région et permettent d'isoler les pannes. Pour optimiser les performances globales, il est nécessaire de déployer des solutions multirégionales, d'utiliser Amazon CloudFront (points de présence) ou le routage Route 53 basé sur la latence.  
**Bonne réponse**  
B. Architecture résiliente et solution à haute disponibilité

#### Explications

Exact. La répartition des ressources sur plusieurs zones de disponibilité (AZ) isole les ressources des pannes au niveau de l'AZ, car chaque AZ constitue un domaine de panne indépendant. Combinée à Elastic Load Balancing, à la mise à l'échelle automatique et aux services prenant en charge nativement les configurations multi-AZ (par exemple, Amazon RDS Multi-AZ), cette architecture permet un basculement automatique et garantit la disponibilité des applications.  
C. Réduction des coûts globaux de stockage des données

#### Explications

Incorrect. Les déploiements multi-AZ augmentent la redondance et impliquent généralement une réplication de données supplémentaire, ce qui peut accroître les coûts de stockage ou de transfert de données au lieu de les réduire. La réduction des coûts nécessite des stratégies spécifiques de stockage ou de cycle de vie (par exemple, les classes de stockage S3 ou le dimensionnement optimal), et non un simple placement des ressources dans plusieurs zones de disponibilité.  
D. Possibilité de désactiver une zone de disponibilité pendant les périodes de faible demande

#### Explications

Incorrect. AWS gère les zones de disponibilité ; il est impossible de « désactiver » une zone de disponibilité. Bien qu’il soit possible d’arrêter ou de réduire vos propres ressources au sein d’une zone de disponibilité, désactiver intentionnellement une zone de disponibilité pour réaliser des économies n’est ni une solution prise en charge ni une bonne pratique, et cela réduirait la disponibilité et la tolérance aux pannes.  
Explication générale  
Cette question porte sur le concept de zones de disponibilité et de haute disponibilité d'AWS. Le déploiement sur plusieurs zones de disponibilité renforce la résilience et la tolérance aux pannes en isolant les défaillances d'infrastructure et en activant le basculement automatique grâce à des services tels que ELB, Auto Scaling et RDS Multi-AZ. Il n'améliore cependant pas intrinsèquement les performances de connexion globales, ne réduit pas les coûts de stockage et ne permet pas de mettre hors service une zone de disponibilité.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 102Ignoré  
**Une entreprise migre ses charges de travail vers le cloud AWS. Elle doit conserver la maîtrise totale de la gestion des correctifs pour les systèmes d'exploitation invités hébergeant ses applications.**  
**Quel service AWS doit-elle utiliser pour répondre à ces exigences ?**  
A. Amazon DynamoDB

#### Explications

Incorrect — Amazon DynamoDB est un service de base de données NoSQL entièrement géré qui masque les serveurs et systèmes d'exploitation sous-jacents. Les clients n'ont pas accès au système d'exploitation invité et ne peuvent donc pas gérer les correctifs au niveau du système d'exploitation.  
**Bonne réponse**  
B. Amazon EC2

#### Explications

Correct — Amazon EC2 is Infrastructure as a Service (IaaS) that provides virtual servers where customers have administrative/root access to the guest operating system. This makes the customer responsible for OS patching and configuration; they can also use AWS Systems Manager (for example, Patch Manager) to automate patches while retaining full control.  
C. AWS Lambda

#### Explications

Incorrect — AWS Lambda is a serverless compute service where AWS manages the execution environment and underlying operating system. Customers cannot access or patch the guest OS, so Lambda does not meet the requirement for full OS patch control.  
D. Amazon RDS

#### Explications

Incorrect — Amazon RDS is a managed relational database service. AWS performs host maintenance and OS-level patching for RDS instances; customers have limited access to the database engine but not the underlying guest operating system, so they cannot fully control OS patch management.  
Explication générale  
This item tests understanding of shared responsibility and service models. To retain full control of guest operating system patching you need IaaS-level servers where you have administrative access; Amazon EC2 provides that. Managed services such as DynamoDB, RDS, and Lambda abstract the infrastructure and remove OS-level access, so AWS handles OS maintenance and patching and they are not suitable where the customer must manage guest OS patches.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 103Ignoré  
**Which AWS services or features enable users to connect on-premises networks to a VPC?**  
**(Choose two.)**  
**Sélection correcte**  
A. AWS VPN

#### Explications

Site-to-Site VPN (AWS-managed VPN) establishes encrypted IPsec tunnels between a customer gateway and an AWS virtual private gateway or Transit Gateway, enabling secure connectivity over the public Internet from an on-premises network to resources inside a VPC.  
B. Elastic Load Balancing

#### Explications

Elastic Load Balancing distributes inbound application or network traffic to targets within one or more VPCs; it does not provide WAN connectivity or a mechanism to link an on-premises network to a VPC.  
**Sélection correcte**  
C. AWS Direct Connect

#### Explications

AWS Direct Connect provides a dedicated network connection from an on-premises location to AWS and supports private virtual interfaces (and Direct Connect Gateway) to access VPCs, offering higher bandwidth, lower latency, and predictable network performance compared with Internet-based links.  
D. VPC peering

#### Explications

VPC peering creates direct routing between two VPCs so their instances can communicate, but it is not a mechanism for connecting on-premises networks to AWS and does not support transitive routing through a peered VPC to reach on-premises networks.  
E. Amazon CloudFront

#### Explications

Amazon CloudFront is a content delivery network that caches and delivers content via edge locations; it optimizes web delivery and does not establish network links between customer on-premises networks and a VPC.  
Explication générale  
The question tests knowledge of AWS connectivity options. The two correct services are the IPsec-based AWS Site-to-Site VPN and AWS Direct Connect, both designed to link on-premises networks to VPCs (VPN over the Internet or a dedicated fiber connection). The other choices are AWS services with different purposes: ELB and CloudFront handle traffic distribution and content delivery within AWS, and VPC peering connects VPCs to each other rather than to on-premises networks.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 104Ignoré  
**An ecommerce company has deployed a new web application on Amazon EC2 instances. The company wants to distribute incoming HTTP traffic evenly across all running instances.**  
**Which AWS service or resource will meet this requirement?**  
A. Amazon EC2 Auto Scaling

#### Explications

Amazon EC2 Auto Scaling (Auto Scaling groups) adjusts the number of instances based on policies and metrics. It does not perform request-level distribution; instead, Auto Scaling is typically paired with an Elastic Load Balancer so newly launched or terminated instances can receive traffic via the load balancer.  
**Bonne réponse**  
B. Application Load Balancer

#### Explications

Application Load Balancer (ALB) is a Layer 7 (HTTP/HTTPS) load balancer that routes and load balances HTTP traffic across target groups of EC2 instances. It performs health checks, supports content-based routing and evenly distributes incoming HTTP requests among healthy targets, making it the correct choice for this scenario.  
C. Gateway Load Balancer

#### Explications

Gateway Load Balancer (GWLB) is intended for deploying and scaling third-party virtual network appliances (traffic inspection, security appliances) and operates at the network/inspection layer. It is not designed for general HTTP request distribution to web servers.  
D. Network Load Balancer

#### Explications

Network Load Balancer (NLB) operates at Layer 4 and is optimized for extreme throughput and low latency (TCP/UDP). While it can forward HTTP traffic, it lacks Layer 7 features (content-based routing, HTTP header/path routing) that make ALB the better fit for typical HTTP web applications.  
Explication générale  
Distributing incoming HTTP traffic across EC2 instances requires an HTTP-aware load balancer. The Application Load Balancer is purpose-built for Layer 7 HTTP/HTTPS traffic, offering health checks, target groups, and content-aware routing to evenly distribute requests. Auto Scaling manages instance counts but does not route requests, Gateway Load Balancer is for virtual appliances, and Network Load Balancer is a Layer 4 option better suited to high-throughput TCP/UDP use cases.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 105Ignoré  
**A company needs Amazon EC2 instances for a workload that can tolerate interruptions.**  
**Which EC2 instance purchasing option meets this requirement with the LARGEST discount compared to On-Demand prices?**  
**Bonne réponse**  
A. Spot Instances

#### Explications

This purchasing model uses AWS’s spare EC2 capacity and therefore provides the steepest price reductions versus On‑Demand — often up to  
B. Convertible Reserved Instances

#### Explications

Convertible reservations exchange lower On‑Demand costs for a multi‑year commitment and the flexibility to change instance attributes. They reduce costs for predictable, long‑running workloads but do not match the deep discounts available from spare‑capacity buying options and are not optimized for interruptible workloads.  
C. Standard Reserved Instances

#### Explications

Standard reservations offer substantial discounts for steady, predictable use by committing to a specific instance family and term. They are not interruption‑based and therefore do not provide the largest discount for workloads that can tolerate instance termination.  
D. Dedicated Hosts

#### Explications

Dedicated physical hosts provide isolation and licensing benefits by allocating entire servers to a customer. They are typically more expensive per capacity unit and are used for compliance or licensing requirements, not for cost‑optimizing interruptible workloads.  
Explication générale  
For workloads that can tolerate interruptions, the spare‑capacity purchasing option delivers the largest discount compared to On‑Demand because it exploits unused EC2 capacity. The tradeoff is potential termination with short notice, so it’s appropriate for fault‑tolerant, batch, or checkpointed workloads. Reserved offerings and Dedicated Hosts reduce cost for predictable, long‑term or compliant use cases but do not provide the same maximum savings for interruptible workloads.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 106Ignoré  
**A company is planning to migrate a monolithic application to AWS. The company wants to modernize the application by splitting it into microservices. The company will deploy the microservices on AWS.**  
**Which migration strategy should the company use?**  
A. Rehost

#### Explications

Rehosting is a lift-and-shift approach that moves existing workloads to AWS with minimal or no code changes (for example, migrating virtual machines to Amazon EC2). It does not include redesigning the application into smaller services, so it doesn't meet the requirement to modernize by splitting a monolith into microservices.  
B. Repurchase

#### Explications

Repurchasing means replacing the application with a commercial, off-the-shelf SaaS product. While this may eliminate the need to manage the application, it does not address the goal of refactoring the existing monolith into microservices under the company's control.  
C. Replatform

#### Explications

Replatforming makes limited changes to optimize an application for the cloud (for example, migrating a database to Amazon RDS or containerizing with minimal code changes). It typically stops short of a full architectural redesign and therefore is not sufficient when the objective is to decompose a monolith into independent microservices.  
**Bonne réponse**  
D. Refactor

#### Explications

La refactorisation (ou réarchitecture) consiste à repenser certaines parties de l'application pour utiliser des modèles et des services natifs du cloud : par exemple, décomposer les fonctionnalités en services indépendants, conteneuriser ou adopter des fonctions sans serveur (Amazon ECS/EKS, AWS Lambda), utiliser API Gateway et introduire une communication asynchrone (Amazon SQS/SNS/EventBridge). Cette approche permet d'atteindre l'évolutivité, l'indépendance de déploiement et l'isolation des pannes nécessaires à une architecture de microservices.  
Explication générale  
Cette question évalue les connaissances relatives aux stratégies de migration AWS (les « 6 R »). La décomposition d'une application monolithique en microservices exige une refonte architecturale afin d'adopter des modèles et des services natifs du cloud ; c'est la définition même du refactoring/de la réarchitecture. Le réhébergement, le changement de plateforme et le rachat ne permettent pas d'effectuer les modifications profondes du code et de l'architecture nécessaires à la décomposition en microservices.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 107Ignoré  
**Quelle perspective du cadre d'adoption du cloud AWS (AWS CAF) se concentre sur l'organisation d'un inventaire de produits de données dans un catalogue de données ?**  
A. Opérations

#### Explications

Ce domaine se concentre sur les pratiques opérationnelles : procédures d’exploitation, surveillance, gestion des incidents, contrôle des changements et automatisation des charges de travail. Ces responsabilités garantissent la fiabilité des opérations, mais n’incluent pas la gouvernance des données, la gestion des métadonnées ni la création d’un catalogue de produits de données.  
**Bonne réponse**  
B. Gouvernance

#### Explications

Ce domaine englobe les politiques, la propriété des données, leur classification, leur gestion et leur conformité. L'organisation d'un inventaire des produits de données et la gestion des métadonnées pour faciliter leur découverte, leur traçabilité et le contrôle d'accès en font pleinement partie. Dans les déploiements AWS, cela se concrétise souvent à l'aide de services tels qu'AWS Glue Data Catalog et AWS Lake Formation pour enregistrer les actifs de données et appliquer les politiques d'accès.  
C. Entreprise

#### Explications

Ce document vise à aligner l'adoption du cloud sur les objectifs commerciaux, à définir les résultats attendus, à mobiliser les parties prenantes et à mesurer la valeur ajoutée pour l'entreprise. Il contribue à définir les priorités et les cas d'usage, mais ne prend pas en charge la gestion technique des métadonnées ni la création d'un catalogue de données.  
D. Plateforme

#### Explications

Ce document traite des fondements techniques : architecture, infrastructure, services de plateforme, provisionnement et CI/CD. Il permet le déploiement de plateformes de données, mais ne prend généralement pas en charge les activités de gouvernance telles que la gestion des métadonnées, la classification des données ou le catalogage.  
Explication générale  
La perspective AWS CAF responsable des inventaires de données et de la gouvernance des métadonnées est la perspective de gouvernance car elle définit les politiques, la propriété, la classification et la gestion nécessaires à la création et à la maintenance d'un catalogue de données. Les autres perspectives se concentrent sur les opérations (procédures d'exploitation/gestion des incidents), la plateforme (infrastructure et outils) et l'alignement avec les objectifs métier ; elles ne sont donc pas principalement responsables du catalogage et de la gestion des métadonnées.  
Domaine  
Domaine 1 : Concepts du cloud  
Question 108Ignoré  
**Quel service ou fonctionnalité AWS permet aux utilisateurs de créer de nouveaux comptes AWS, de regrouper plusieurs comptes pour organiser les flux de travail et d'appliquer des politiques à des groupes de comptes ?**  
A. Gestion des identités et des accès AWS (IAM)

#### Explications

Incorrect — IAM gère les identités et les accès au sein d'un compte AWS (utilisateurs, groupes, rôles et politiques IAM) et permet l'accès inter-comptes via les rôles IAM, mais ne crée pas de comptes AWS et ne fournit pas de regroupement ou de gouvernance au niveau de l'organisation sur plusieurs comptes.  
B. Conseiller de confiance AWS

#### Explications

Incorrect — Trusted Advisor effectue des contrôles de bonnes pratiques (optimisation des coûts, sécurité, tolérance aux pannes, performances et limites de service) et fournit des recommandations ; il s’agit d’un outil de conseil qui ne crée pas de comptes, ne regroupe pas les comptes et n’applique pas de politiques à l’échelle de l’organisation.  
C. AWS CloudFormation

#### Explications

Incorrect — CloudFormation est un service d'infrastructure en tant que code permettant de provisionner et de gérer des ressources AWS via des modèles. Bien que StackSets puisse déployer des piles sur plusieurs comptes, CloudFormation ne gère pas la création de comptes, le regroupement hiérarchique des comptes ni l'application de politiques de gouvernance à l'échelle de l'organisation.  
**Bonne réponse**  
D. Organisations AWS

#### Explications

Correct — AWS Organizations fournit une gestion centralisée des comptes : vous pouvez créer des comptes par programmation (CreateAccount), organiser les comptes en unités organisationnelles (UO), appliquer des politiques de contrôle des services (SCP) pour appliquer la gouvernance sur l’ensemble des comptes et utiliser une facturation consolidée et une administration déléguée à partir du compte de gestion.  
Explication générale  
AWS Organizations est le service conçu pour la gestion du cycle de vie des comptes et la gouvernance au niveau de l'organisation : il crée des comptes, les regroupe en unités organisationnelles (UO) et applique des politiques à l'ensemble des comptes (SCP), tout en proposant une facturation consolidée. Les autres options se concentrent sur l'identité (IAM), les recommandations (Trusted Advisor) ou le provisionnement des ressources (CloudFormation) et ne permettent pas la création de comptes ni l'application de politiques à l'échelle de l'organisation.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 109Ignoré  
**Quel est l'avantage d'utiliser un équilibreur de charge Elastic Load Balancing (ELB) avec des applications exécutées dans le cloud AWS ?**  
A. Un ELB adaptera automatiquement les ressources pour répondre aux besoins de capacité.

#### Explications

Incorrect. L'équilibreur de charge ne modifie pas le nombre d'instances d'application. La gestion de la capacité des instances (ajout ou suppression d'instances EC2) est assurée par Auto Scaling. Le rôle d'ELB est de répartir le trafic entre les cibles disponibles, et non d'effectuer une mise à l'échelle des ressources de calcul.  
**Bonne réponse**  
B. Un ELB peut répartir le trafic entre plusieurs ressources de calcul.

#### Explications

Exact. Elastic Load Balancing est un service géré qui répartit le trafic entrant des applications sur plusieurs cibles (par exemple, des instances EC2, des adresses IP ou des conteneurs) à travers les zones de disponibilité, améliorant ainsi la disponibilité et la tolérance aux pannes des applications et acheminant le trafic uniquement vers des cibles saines.  
C. Un ELB peut s'étendre sur plusieurs régions AWS.

#### Explications

Incorrect. ELB est déployé au sein d'une seule région AWS et fonctionne sur plusieurs zones de disponibilité de cette région. Pour répartir le trafic entre les régions, vous devez utiliser des architectures multirégionales avec des services tels qu'Amazon Route 53, AWS Global Accelerator ou des équilibreurs de charge régionaux distincts et un routage basé sur le DNS.  
D. Un ELB peut équilibrer le trafic entre plusieurs passerelles Internet.

#### Explications

Incorrect. An Internet Gateway is a VPC component that provides internet access to resources in a VPC; ELB routes client requests to application targets (in subnets/AZs) and does not balance traffic between internet gateways.  
Explication générale  
The primary benefit of using Elastic Load Balancing is to improve availability and fault tolerance by distributing incoming application traffic across multiple targets within a Region and Availability Zones. ELB manages traffic routing and health checks but does not manage the number of backend instances (Auto Scaling does) nor does it natively provide cross-region traffic distribution or balance between internet gateways.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 110Ignoré  
**Which capabilities are in the platform perspective of the AWS Cloud Adoption Framework (AWS CAF)? (Choose two.)**  
A. Performance and capacity management

#### Explications

This capability — monitoring, scaling, and capacity planning (for example Amazon CloudWatch metrics and Auto Scaling policies) — is primarily an operational responsibility that focuses on running and maintaining workloads. In the AWS CAF mappings it is aligned with the Operations perspective rather than the Platform perspective.  
**Sélection correcte**  
B. Data engineering

#### Explications

Building and operating data pipelines, storage, and processing services (for example AWS Glue, Amazon S3, Amazon EMR, and data-lake controls) is a platform-level capability because it provides the shared data infrastructure and engineering patterns that application teams consume. That responsibility maps to the Platform perspective in the AWS CAF.  
**Sélection correcte**  
C. Continuous integration and continuous delivery (CI/CD)

#### Explications

Automated build–test–deploy toolchains and pipelines (for example AWS CodePipeline, CodeBuild, CodeDeploy or other CI/CD toolchains) are platform-provided capabilities that enable repeatable, automated application delivery and developer productivity; as such they are part of the Platform perspective.  
D. Infrastructure protection

#### Explications

Controls and services that protect infrastructure (for example IAM, AWS KMS, AWS Shield, VPC network controls) are security-focused responsibilities. In the AWS CAF these protective controls are mapped to the Security perspective rather than the Platform perspective.  
E. Change and release management

#### Explications

Formal change control, release governance and approval processes (for example change windows, release approvals and rollback/runbook procedures) are operational governance activities tied to running services safely. The AWS CAF assigns these activities to the Operations perspective even though automation (tooling) that supports them may be provided by the platform.  
Explication générale  
The Platform perspective in the AWS Cloud Adoption Framework covers capabilities that provide shared engineering and delivery services for applications — notably data engineering (shared data pipelines and storage) and automated application delivery toolchains. Protective controls and formal change governance are mapped to the Security and Operations perspectives respectively, so they are not the best choices for this question.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 111Ignoré  
**Quel service AWS convertit du texte en voix réalistes ?**  
A. Transcription Amazon

#### Explications

Incorrect. Ce service effectue une reconnaissance vocale automatique (conversion de l'audio parlé en texte) à l'aide de l'apprentissage automatique et est utilisé pour la transcription et le sous-titrage en temps réel, et non pour la synthèse vocale à partir de texte.  
B. Reconnaissance d'Amazon

#### Explications

Incorrect. Il s'agit d'un service de vision par ordinateur pour l'analyse d'images et de vidéos (détection d'objets et de visages, analyse de scènes, reconnaissance de célébrités, etc.), et non d'un service de synthèse vocale.  
**Bonne réponse**  
C. Amazon Polly

#### Explications

Exact. Ce service offre une fonctionnalité de synthèse vocale avec des voix neuronales de haute qualité, prend en charge plusieurs langues et le protocole SSML pour un contrôle précis de la parole, et peut diffuser ou produire des fichiers audio destinés à être utilisés dans les systèmes IVR, l'accessibilité et les applications vocales.  
D. Extrait de texte Amazon

#### Explications

Incorrect. Ce service extrait le texte imprimé et manuscrit ainsi que les données structurées des documents numérisés (OCR et extraction de formulaires), mais il ne génère pas de lecture audio à partir de texte.  
Explication générale  
Cette question teste vos connaissances des services AWS de traitement de la parole et du texte. Le service approprié est celui qui synthétise l'audio à partir de texte à l'aide de voix neuronales et de SSML ; les autres options effectuent des tâches différentes (reconnaissance vocale, analyse d'images/vidéos ou reconnaissance optique de caractères de documents) et ne sont donc pas pertinentes.  
Domaine  
Domaine 3 : Technologies et services cloud  
Question 112Ignoré  
**Quel service AWS permet de migrer des données entre services de stockage AWS ?**  
**Bonne réponse**  
A. AWS DataSync

#### Explications

DataSync est un service de transfert de données géré, conçu spécifiquement pour déplacer de grands volumes de données de manière fiable et sécurisée. Il prend en charge les transferts entre le stockage sur site et AWS, ainsi qu'entre les points de terminaison de stockage AWS (par exemple, Amazon S3, Amazon EFS et Amazon FSx). Il fournit un agent pour les montages NFS/SMB sur site, optimise l'utilisation du réseau pour un débit élevé, effectue la validation de l'intégrité des données et prend en charge la planification et la surveillance des tâches de transfert, ce qui en fait l'outil de migration idéal pour ce scénario.  
B. AWS Direct Connect

#### Explications

AWS Direct Connect établit une connexion réseau dédiée entre les environnements sur site et AWS afin de réduire la variabilité du réseau et de garantir une bande passante constante. Il s'agit d'un service de connectivité, et non d'un service de migration ou d'orchestration de données ; il ne propose pas d'agents de transfert intégrés, de fonctionnalités de validation, de planification ou de migration de stockage à stockage.  
C. Formation du lac AWS

#### Explications

AWS Lake Formation est un service permettant de créer, de sécuriser et de gérer des lacs de données (ingestion, catalogage et contrôle d'accès). Il est axé sur la gouvernance et l'accès aux données plutôt que sur les transferts ou migrations directs entre services de stockage ; les tâches ETL ou d'ingestion (par exemple avec AWS Glue) sont utilisées pour déplacer ou transformer les données dans le lac.  
D. Amazon S3

#### Explications

Amazon S3 est un service de stockage d'objets utilisé pour stocker et récupérer des données. Bien que S3 puisse servir de source ou de destination dans les flux de travail de migration et offre des fonctionnalités telles que la réplication interrégionale et les opérations par lots pour les objets S3, il ne s'agit pas d'un service de migration/orchestration à usage général permettant de déplacer des données entre différents services de stockage AWS.  
Explication générale  
The question tests recognition of the AWS service designed specifically for moving data between storage locations. DataSync is the managed transfer tool offering agents, integrity checks, scheduling, and direct support for AWS storage services (S3, EFS, FSx), whereas the other options are a network connection (Direct Connect), a data‑lake governance service (Lake Formation), or a storage endpoint (S3) and therefore do not fulfill the role of an orchestration/migration service.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 113Ignoré  
**Which of the following is a managed AWS service that is used specifically for extract, transform, and load (ETL) data?**  
A. Amazon Athena

#### Explications

Incorrect. Amazon Athena is a serverless interactive query service that lets you run SQL queries directly against data in Amazon S3. It is a query/analytics engine and does not provide managed ETL workflows, job orchestration, schema discovery, or transformation jobs the way an ETL service does.  
**Bonne réponse**  
B. AWS Glue

#### Explications

Correct. AWS Glue is a fully managed, serverless ETL service that provides a Data Catalog, schema discovery via crawlers, Spark-based ETL jobs, job scheduling and orchestration, and native integrations with S3, Redshift, RDS, and other data stores to extract, transform, and load data for analytics.  
C. Amazon S3

#### Explications

Incorrect. Amazon S3 is durable object storage used to store raw or processed data (a data lake), but it does not perform ETL operations. It serves as a storage layer that ETL services (like AWS Glue) and query engines (like Athena) can read from and write to.  
D. AWS Snowball Edge

#### Explications

Incorrect. AWS Snowball Edge is a physical data transport and edge compute device used for offline large-scale data transfer and some edge processing. It is not a managed ETL service or orchestration platform for regular cloud-based ETL workflows.  
Explication générale  
AWS Glue is the managed service designed specifically for ETL: it discovers schemas, transforms data (Spark-based), and loads it into target stores with built-in orchestration and a Data Catalog. The other options are related but serve different roles—Athena for serverless querying, S3 for storage, and Snowball Edge for physical data transfer/edge compute—so they are not the managed ETL service being asked about.  
Domaine  
Domain 3: Cloud Technology and Services  
Question 114Ignoré  
**Which fully managed AWS service assists with the creation, testing, and management of custom Amazon EC2 images?**  
**Bonne réponse**  
A. EC2 Image Builder

#### Explications

Automates the end-to-end image lifecycle via repeatable image pipelines that build, test, version, and distribute hardened AMIs. Provides reusable components/recipes, scheduled builds, and integrations with services such as AWS Systems Manager and Amazon S3 to produce secure, compliant images for EC2.  
B. Amazon Machine Image (AMI)

#### Explications

An Amazon Machine Image (AMI) is the image artifact used to launch EC2 instances, not a managed service. It represents the result of an image build but does not itself provide automation, testing, or lifecycle management capabilities.  
C. AWS Launch Wizard

#### Explications

AWS Launch Wizard propose des déploiements guidés pour des applications spécifiques et dimensionne l'infrastructure pour ces charges de travail ; il n'inclut pas de fonctionnalités permettant d'automatiser la création, le test ou la gestion d'images EC2 personnalisées.  
D. AWS Elastic Beanstalk

#### Explications

AWS Elastic Beanstalk gère le déploiement et la mise à l'échelle des applications web en provisionnant et en exploitant les ressources sous-jacentes, mais ne fournit pas d'outils pour la création ou le test d'images EC2 personnalisées.  
Explication générale  
Ce test évalue vos connaissances du service AWS qui gère le cycle de vie des images EC2. La bonne réponse est le service entièrement géré qui crée, teste, versionne et distribue les AMI via des pipelines d'images automatisés et des intégrations avec d'autres services AWS. Les autres options sont soit l'artefact d'image lui-même (AMI), soit des services dédiés au déploiement d'applications plutôt qu'à la création et à la gestion d'images.  
Domaine  
Domaine 3 : Technologies et services cloud

