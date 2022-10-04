# Cloud Computing

`Cloud computing` is the on-demand delivery of compute power, database, storage, applications, and other IT resources through a cloud services platform via the Internet with pay-as-you-go pricing. Cloud computing provides a simple way to access servers, storage, databases and a broad set of application services over the Internet
Amazon EC2 is type of virtual server
Client can be a web browser
What is cloud computing? Is the on-demand delivery of IT resources over the internet with pay as you go pricing

Deployment modes for cloud computing

    1 Cloud based deployment run all part of the application in the cloud.. migrate existing application to the cloud, design and build new applications in the cloud.

    2 On premises deployment(private cloud Platform) deploy resources by using virtualization and resource management tools.

    3 Hybrid Deployment. Connect cloud-based respires to on premises infrastructure, Integrate could-based resources with legacy IT applications.

Why companies benefited from cloud computing

    1 trade the upfront expense for variable expense
    2 stop spending money to run and maintain data centers(focus more on your the tasks(applications and customers))
    3 stop guessing capacity(You can use only the capacity that you need)
    4 benefit from massive economics of scale(lower pay as you go prices)
    5 Increase speed and agility(flexibility of the could allow customers to develop and deploy applications easily)
    6 go global in minutes( customer can access applications with minimal delays)

Types of cloud computing

    - Infrastructure as a service (Provide access to network features, computers(virtual or dedicated hardware), and date storage space.
    It contains the basic building blocks for cloud IT and typically provides access to networking features, computers (virtual or on dedicated hardware), and data storage space.
    - IaaS provides you with the highest level of flexibility and management control over your IT resources and is most similar to existing IT resources that many IT departments and developers are familiar with today.
    Platform as a service (provide operating system, programing languages executive environment,  data base and web server)
    removes the need for your organization to manage the underlying infrastructure (usually hardware and operating systems) and allows you to focus on the deployment and management of your applications.
    - Software as a service (allows users to connect to and use cloud-based apps over the Internet. Common examples are email, calendaring, and office tools.
    provides you with a completed product that is run and managed by the service provider. In most cases, people referring to Software as a Service are referring to end-user applications.
    AWS is the most secure service provider. It’s a leading cloud platform.

Compute as a service

`Amazon Elastic Compute Cloud`(Amazon EC2) it’s a virtual sever that provide a secure, resizable compute capacity in the cloud as Amazon EC2 instances.
Multi-tenancy(the sharing underlying hardware between virtual machines but not knowing each other)
Vertical scaling(adding cpu or other things when in need)

You can save cost by paying only for sever capacity that you need or want.

### `The different type of Instances`

    General Purpose Instances(balanced of compute, memory, and networking resources) Application servers, gaming servers, backend servers for enterprise application

    Compute Optimized instances(idea for the compute bound application that benefit from high performance processors) Web, application, and gaming servers.

    Memory optimized Instance(Preloading process gives the CPU direct access to the computer program before running) High performance database or a workload that involves performing real time processing of a large amount of unstructured data.

    Accelerated computing instance(use a hardware accelerators or coprocessors, to perform some functions more efficiently that is possible in software running on CPUS) Floating point number of calculations, graphics processing and data patter matching.

    Storage optimized instances(designed for a workload that requires high, sequential read and write access to large datasets on local storage). Distributed file systems, data warehousing applications, and high frequency online transaction processing system.

Amazon EC2 pricing

1 on demand( It’s idea for short term goals, no long term or front const) developing and testing and running applications
2 Saving plan( low price in exchange for longer term unto 72 percent off compare to on demand when consistently committed 1 or 3 year term)
3 Reserved Instances(You can buy it for a 1 or a 3 year term, and scheduled reserved instance for a 1 year term, the 3 year term is more cost savings option )
4 Spot Instances(withstand interruptions you can get 90 percent off vs on demand)
5 Dedicated hosts(are a physical server with EC2 instance capacity that is fully dedicated to your use) It’s the most expensive one


AWS Billing and Pricing
Capex and Opex
Capital expenditure where you pay up from. It’s fixed, suck cost.
Operational expenditure which is where you pay for what you use. Think of Utility billing such as electricity, gas, water, etc.

    Pay as you go (no minimum requirement)
    Pay less when you reserver
    Pay even less per unit using more(more resources less pay)
    Pay even less as AWS grows
    Customer pricing

Drivers of Cost wit AWS

    Compute
    Storage
    And Data Outbound

Free Services

    Amazon VPC (100%)
    Elastic Beanstalk
    CloudFormatoin
    Identity Access Management
    Auto Opsworks

What determines price
    Clock hours of server time
    Instance type
    Pricing model
    Number of Instances
    Load balancing
    Detailed Monitoring

### `Scalability`

Scalability involves beginning with only the resources you need designing your architecture to automatically respond to chaining demand by scaling out or in.
“Everything fails all the time, so plan for the failure and nothing fails." Werner Vogels.

EC2 auto scaling, enable you to automatically add or remove Amazon EC2 instances in response to chaining application demand.
Two approaches

    1 Dynamic scaling responds to chaining demand
    2 Predictive scaling automatically schedules the right number of Amazon EC2 instance based on predicted demand.
    To scale faster use both approach together.

When creating an Auto Scaling group.

    - The Minimum Capacity is the number of EC2 instances that launch immediately after the have created the auto scaling group.
    - The Desired Capacity might be equal as the minimum capacity when we do not specify the desired capacity.
    - The maximum Capacity is the maximum number of instances that auto scaling create

Directly traffic with Elastic Load Balancing(ELB) is a service that automatically distribute incoming application traffic across multiple resources like EC2.
ELB and EC2 are separate services they work together.

`ELB come in 3 different flavors:`

- Application Load Balancers(layer 7 make intelligent decisions)
- Network Load Balancers (extreme performance/static IP address
- Classic Load Balancers(Test & dev, keep costs Low)

`Messaging and queuing`

    It is a process of sending messages from one service to another.

`Monolithic application`(tightly coupled) if one system fails everyone fails.

`Micro-service`(loosely coupled) It prevent the entire system from failing.

### Amazon Simple Notification Service(SNS)

- a publish/subscribe service

### Amazon Simple Queue Service(SQS)

- is a message queuing service. User or service retrieves a  message from the queue, process it, and then deletes it from the queue.

EC2 instances are virtual machines/computer it’s flexible, reliable, and scalable. Patching mean repairing vulnerable instances.
Host traditional applications(full access to the OS) use EC2

### `AWS Lambda`

- it is a server-less which means that the user cannot see or access the underlying server/infrastructure. Everything is taken care of and the user is only need to focus on their application. (Run the code on server but don’t provision or manage servers)
- It’s not for deep processing, it takes less than 15 minutes. Not for long running.
- To host short running functions, service oriented applications, event driven applications and not provision or managing servers look into AWS lambda

### `Containers`

- provide you with a standard way to package your applications code and dependencies into a single object.

`Docker` is a software platform that enable you to build, test, and deploy applications quickly.
Run Docker contains based workload on AWS

Container Orchestration tools(for efficiency and portability without lambda)

    1 Amazon Elastic Kubernetes Service (Amazon EKS)
    2 Amazon Elastic Container Service(Amazon ECS) at scale

- Container orchestration service help you to deploy, manage, and scale your containerized applications.
Either EC2 that you manage or AWS Fargate managed for you

Amazon Elastic Container Service enable you to run and scale containerized application on aws
EKS lets you run k/cabernets on aws

Amazon Fargate is a server less compute engine for containers. It works with both ECS and EKS. You do not need to provision or manage servers.

### Selecting a region

Some of the criteria to select a regional are

1. compliance(rule, data government and legal requirements)
2. Proximity to customers(because of latency)
3. Available service with a region(some region may not have the same service as others)\
4. Pricing(some region may have different pricing for the same service)

`Availability Zones` is a data center(a single or group) they are located tens of miles apart form each other.

`Region` geographical area that has two or more availability zone.

`GovCloud(US-West)`region only on US entities( only us green card holder) Federal company and private company
A community that was build for the government

`Edge locations`  is a set that Amazon cloud front users to store cached copies of your content closed to your customers to faster delivery. (Amazon route 53). (AWS outposts)

`Cloud frond` is a service that deliver data, video, application and api with low latency

Interacting with AWS services Accessing AWS

    How to interact with AWS services?
- Using API(Application Programing Interface)

    AWS management console(Test environments, view AWS bills, view monitoring, work with non-technical resource) It’s a web based interface for accessing and managing AWS services.
    AWS command line interface CLI( Make an API call using the terminal on your machine) automating the actions
    AWS Software Development Kts(SDK) allows you to use different language to interact with AWS. Write program to interact with AWS. simplify using AWS services in your applications with an Application Program Interface (API) tailored to your programming language or platform.


`AWS Elastic Beanstalk` you provide code and configuration setting, and elastic beanstalk deploy the resource necessary to perform the following tasks adjust capacity, load balancing, automatic scaling, application health monitoring.

`AWS Cloud formation` is an infrastructure as code tool used to define a wide variety of AWS resources( using text based template(writing code)for instance Json) It support storage, database, analytics machines learning and more.


### Module 4(Networking)

`Amazon Virtual Private Cloud(VPC)` is a private network. It enable people to have an isolated section in AWS cloud.
Subnets are a subdivision of IP address(it can be Public or Private) It breaks large networks into smaller, more manageable networks that run more efficiently.
It is a section of a VPC which you can group resources based on securing or operational needs.

Public Subnets accessible by the public.
Private Subnets accessible only through your private network( database that contains customer’s personal information and history)
A Packet is a unit of data sent over the internet or a network.
Internet Gateway allows traffic between client and severs. It is a connection between VPC and the internet.
To allow resources from Public traffic to VPC you need an Internet Gateway(IGW). It more of a door.

`Virtual Private Gateway` allows a VPN connects with VPC. it only allow to access private resources. (Good example is a body guard)

`AWS direct Connect`(it allows a network between the Data centre and VPC) no one share the network with you(it’s a dedicated private connection) It enable people to use service with low latency and high .

Subnets and Networks access
Networking( who should be allowed to communicate to each other)
Network Access Control list(ACL) it check a packet permission for subnets. It’s more of a passport.
VPC component that checks packet permissions for an Amazon EC2 instance is a Security Group.
Stateful Packet filtering remember previous decisions made for incoming packets.

Global Networking

`Domain Name system(DNS)` it is a the process of translating a name(website name) to an IP(internet Protocol) address.

`Amazon Route 53` A DNSe web server. It gives developers and business a reliable way to route end user to internet application hosted in AWS. It also record the existing domain names managed by other domain registrars.
Amazon Route 53 is a highly available and scalable, public authoritative DNS service from Amazon Web Services. You can register public domain name.
The first instate route is Route 66. They called Route 53 because it works port 53.
Module 5 (storage and database)

## Storage

`Block level storage` behave as a physical hard drives.

Instance store Volume will delete a data if the instance are stop(terminated) working (temporary block level storage for EC2).

`EBS(Amazon Elastic Block store)` you can create a virtual hard drive. 16 T maximum storage. The date can persist(remain) between the instance’s start and stop. It run in a single availability zone.
Snapshots: incremental backups(the first backup taken of a volume copies all the data.)

`Object Storage(IT consists data, metadata, and a key)`

That data might be image, video, text document, or any other type of file.

### `S3(Amazon Simple Storage Service)`

It is a storage for the internet. It is designed to make web-scale computing easier(you can use to store and retrieve any amount of date at anytime from anywhere from the web)

    A service that provides object-level storage. S3 stores data as objects in buckets.
    Bucket is a container for object stored in Amazon S3.
    That maximum file size fo an object in S3 is 5T and 99.9999 durable. (11 9s)
    Build guarantee 99.9% availability
    One write and read many.
    No need for a backup plan.

Objects are the fundamental entities stored in S3(consists of data and metadata)
Key is the unique identifier for an object within a bucket. Every object in a bucket has exactly one key.

`Amazon CloudFront`is a web service that gives businesses and web application developers an easy and cost effective way to distribute content with low latency and high data transfer speeds.

`Edge Location` is the location where content will be cached. This is separate to an AWS Region/AZ. They’re not read only you can write too.

Distribution is the name given the CDN which consist of a collection of Edge locations.
Origin all the file that the CDN(content delivery Network) will distribute. It can be S3 bucket, EC2 instance, Elastic Load Balancer, or Route53.

### S3 storage Classes (you pay only for what you use)

- The criteria for selecting

        How often you play to retrieve your data?
        How available you need your data to be?

S3 standard

    Designed for frequently access data
    a minimum of 3 availability zones
    Website, content distribution, and data analytics.

S3 standard Infrequent Access (standard IA)

    Ideal for infrequently accessed data
    lower storage price and higher retrial price
    3 availability Zones

One zone Infrequent Access(s3 one zone ai)

    store data in a Single availability zone
    has a lower storage price than s3 standard
    If you want to save cost on storage
    you can easily reproduce your data in the event of an availability zone failure

S3 Intelligent Tiering

    ideal for data with unknown or change access patterns
    requires a small monthly monitoring and automation fee per object

S3 Glacier

    Low cost storage designed for data archiving
    able to retrieve objects with a few minutes to hours
    low cost for date archiving(example older photo and video files)

S3 Glacier Deep Archive
    Lowest cost object storage class ideal for archiving
    able to retrieve object within 12 hours

File System
### `File storage`

    Multiple clients can access data that is stored in shared file folder.

### Amazon EFS(elastic file system)

    It allows multiple instance can access the data in EFS at the same time(on both AWS and on premise)
    It runs in multiple availability zones.
    Amazon EFS provides a simple, server-less, set-and-forget elastic file system. With Amazon EFS, you can create a file system, mount the file system on an Amazon EC2 instance, and then read and write data to and from your file system.

### `Relational database`

    data stored in a way that relates it to other pieces of data, and it uses Structured Query Language(SQL) to store and query data.
    It’s like a xcel spread sheet
    A relational database is structured, meaning the data is organized in tables. Many times, the data within these tables have relationships with one another, or dependencies.


- Amazon Relational Database Service(Amazon RDS) is a service that enable you to run relational databases in the AWS cloud.

    RDS has multiple availability zone(disaster recovery) Multi -AZ
    Read Replicas(for performance)

### AWS supported databases

        MySQL
        PostgreSQL
        Oracle
        Microsoft SQL server
        MariaDB

Amazon Aurora is an enterprise-class relational database. It is compatible with MYSQL and SQL relational database.

    It’s up to 5 times faster than mysql and 3 postgresql.
    It helps to reduce your database cost by reducing unnecessary I/O operations.
    Consider it if your workload require high availability.  1/10 of the cost.

### `Non-relational databases`

- create a table, to store and query data. Sometimes it refers as Nosql database. They use a structures other than rows and columns to organize data.

`Amazon DynamoDB` is a server-less database.(has a millisecond respond time, highly scalable).
It is a key-value database service. It delivers single-digit millisecond performance at any scale.

    Online Transaction processing(OLTP) things that are related and small data
    Online analytics processing(OLAP) huge number of records
    Data warehousing online Analytics processing it’s used for business intelligence.
    Amazon redshift is a data warehousing service that you can use for big data analytics.(It’s a data analysis, for historical analytics).

### `AWS Database Migration Service(AWS DMS)`

- enables you to migrate relational databases, non relational databases, and other types of data stores(moving between databases).
- Databases need not to be the same type.

The use of the DMS

- Homogenous Database( between the same type like from Microsoft SQL to Amazon RDS for SQL server).
- Heterogenous Database(schema structure, Data type, and database code are different)
- Development and test data migration(test without affecting production)
- Database consolidation (combining several databases to single database)
- Continuous replication (sending ongoing copies of your data to other target sources instead of doing a one-time migration)

Choosing the right database

- Amazon DocumentDB for content management and user profile. It support MongoDB workloads(a document database program)

- Amazon Neptune graph database service, for social networking, fraud detection, knowledge graphs.

- Amazon Quantum Ledger Database(QLDB) an immutable record(a ledger database, transparent database).

- Amazon managed Blockchain is a service that you can use to create and manage blockchain networks with open-source framework.

- Amazon ElastiCache (frequently identical queries) is a service that adds caching layers on top of your database to help improve the read time of common requests. (Two types of data store, Redis and Memcached)
  It returns the most common queries in faster, for performance.

- Amazon DynamoDB Accelerator (DAX) is an in memory cache for DynamoDB. It helps improve response time from single digit milliseconds to microseconds.

- Boot Strap Script(so that you don’t have to write manually)

Module 6
## `Security`

- `Both the AWS and customers are responsible for the security.`

`Shared Responsibility model`( AWS responsible for security` of `the cloud and The customers are responsive for the security `in` the cloud)

For example AWS is responsible for

    - the data center(physical)
    - network
    - hypervisor(a software that allocate cpus, memory, network, and storage that run a virtual machine).

Customers are responsive for

    - the Operating system
    - application
    - data

For example, retailers may let everybody see a picture but banks don’t let people to let know the account number and other private stuff.


`AWS Identity and Access Management(IAM)` enables you to manage access to AWS services and resources securely.

    - You don’t need to specify region It’s a global service.
    - AWS Root user can access and control any resource in the account. you can access it by signing with email and password that you used to create your AWS account.
    - Do not use the root user for everyday tasks.
    - By default it has no permission associated wit it. You have to allow some permission in order to use it.

- It’s called the `Principle of Least Privilege`. A user is granted access only to what they need.

More info [here](https://docs.aws.amazon.com/general/latest/gr/root-vs-iam.html)

We need to create a IAM user because for additional security by giving a unique set of security credentials.

- IAM policy is the Json(Javascript Object Notation) file that enable people to allow or deny the service. Document that describe permission.
- IAM group It is a collection of of IAM users. let the owner or higher employer to create a group instead of individual.
- IAM Roles is an identity that you can assume to gain temporary access to permission. It has associated permissions that allow and deny, assumed for temporary amounts of time. Has no username or password.
- User role to access to temporary permission .

Credential report that lists all users in your account.

    - Multi factor Authentication(MFA) provides an extra layer of security for your AWS account( more than a username and password) additional verification information( factors)
    - For example one time password(OTP).

`Organizations` is a central location to manage multiple AWS accounts.

    - centralized management
    - consolidated billing
    - hierarchical groupings
    - AWS service and API actions access control

`Service control policies`(SCP) is a feature that allows you to centrally control permission for the accounts in your organization.

- It enables you to place a restriction on the AWS services resources, and individual API actions of each account.
- It is for the organization root, an individual member accounts, or an OU.

`Organizational units(OU)` to make it easier to manage accounts with similar business or security requirements.

Compliance (regulation you are under) enables you to understand the robust controls in place at AWS to maintain security and data protection in the cloud. As systems are built on top of AWS Cloud infrastructure, compliance responsibilities will be shared

    For software and data (General data protection regulation(GDPR)
    For healthcare in US (Health insurance Portability and accountability Act(HIPAA)

`AWS Artifact` is a service that provide on-demand access to AWS security and compliance reports and select online agreements.(AWS Artifact agreements and AWS artifact reports)

The Customer Compliance Center contain resource to help you learn more about AWS Compliance.

Denial of Service attacks is a deliberate attempt to make a website or application unavailable to users.

    DDOS(distributed denial of service)
    UDP( User Datat protocol )
    Slowloris attack
    Security Groups

Elastic load balance is very helpful to keep things secure and distributed???
`AWS Shield` is a service that protects application against DDoS attacks.

Two services

    Standard protect customers at no cost.
    Advance is a paid serve that provide a detail attack diagnostic and the ability to detect and mitigate sophisticated DDoS attacks.

NoMAD ( no more active Directory) is an application that keeps Amazon Active Directory passwords and kerberos tickets synced with the local account on Mac.


Additional Security Service

    Encryption is securing a message or data in a way that only authorized parties can access it.
    Encryption at rest(storage) and encryption in transit(while it transmit)
    AWS Key management Service (AWS KMS) allows you to perform an encryption operations through the use of cryptographic keys. Use it to create, manage, and use cryptographic keys.

`AWS WAF(Web Application Firewall)` is a web application firewall that lets you monitor network request that come into your web applications.

    Work together with Amazon CloudFront and an Application Load Balancer.

`Amazon Inspector` it performs an automated security assessments.(checking for vulnerabilities)

`AWS Trusted Advisor` is a web service that inspect your AWS environment and provides real time recommendation in accordance with AWS best practices. Offer a recommended actions.

`Amazon GuardDuty` is a service that provides intelligent threat detection for your AWS Infrastructure and resources.( it uses machine learning)

### WAF vs AWS Shield

    - WAF layer it is designed to prevent your application from hacking.

- Shield protect your from DDoS attack

Module 7

## `Monitoring and Analytics`


    Monitoring is

    - observing systems
    - collecting metrics
    - using data to make decisions.

`Amazon CloudWatch` is a web service that enables you monitor and manage various metric and configure alarm actions based on data from those metrics.

    - It create graphs automatically that show how performance has changed over time.
    - Cloudwatch alarms set a threshold and perform actions, letting you that your metric has gone above or below a predefined threshold.
    - CloudWatch Dashboard it enables you to access all the metrics for your resources form a single location.

`Amazon CloudSearch` is a managed service in the AWS Cloud that makes it simple and cost-effective to set up, manage, and scale a search solution for your website or application.

### $ Trust $  but $ Verify$

`AWS CloudTrail `records API calls for your account. (The caller identity, the time, id address, and more). You can see a complete history of user activity and API calls for your applications and resources.

    - Events updated every 15 mins.
    - CloudTrail Insights allows an automatically detect unusual API activities in your AWS account.

`AWS Trusted Advisor` is a web service that inspects your AWS environment and provides real time recommendation in accordance with AWS best practices. Offer a recommended actions.

5 categories of Trusted Advisors.

    1. Cost Optimization
    2. Performance
    3. Security
    4. FAult tolerance
    5. Service limits

Module 8

## `Pricing and Support`

AWS Free Tier

3 type of service are available

    - Always free
    - 12 month free
    - trails)

    AWS lambda 1 million free invocation/request in a month.
    dynamoDB allows 25 GB free storage per month
    SW3 free 12 moths unto 5 GB
    AWS Lightsail offer 1 month trial of up to 750 hours of usage.

### Pricing Concepts

AWS offered a range of cloud computing services with pay as you go pricing. (Pay what you use, pay less when you receive, pay less with volume based discount when you use more)

`AWS pricing`calculator(estimate cost)

`AWS lambda pricing`allow 1 million free request and up to 3.2 million seconds of compute time per month.

- EC2 you pay for only the compute time that you use while your instance is running.
- S3(storage you pay only the storage that you us)

    - Request and data retrievals(you pay for request made to your Amazon s3 objects and buckets)
    - Data transfer(there is no cost data between different s3 buses or from s3 to services with the same Region, However you pay for d ta that you transfer into and out of amazon s3, with few exceptions)
    - Management and replication( for s3 inventory, analytics, and object tagging)

Billing Dashboard

Use the AWS Billing & Cost Management dashboard to pay your AWS bill, monitor your usage, and analyze and control your costs.

`Consolidated billing` it allow you to pay a single bill for multiple accounts in your organization.(simplifies billing process, and share saving across accounts and it’s free feature)
The maximum number of accounts allowed for an organization is 4, but you can contact AWS support to increase your quota if needed.

AWS budgets you can create budgets to play your service usage, service cots, and instance reservations. You’ll receive when you reach or close to your budgets.
The information in AWS budgets updates three times a day.

`AWS Cost Explorer` is a tool that enables you to visualize, understand, and manage your AWS cost and usage over time. It allows you about cost report. Custom resort as -ar.

`AWS Support Plans` help you troubleshoot issues, lower, cost, and efficiently use AWS services.

It offers for different support plans.

Basic support:

    - Everybody get a free basic support.
    - 24/7 customer service. Documentation, white papers, support forums
    - AWS trusted Advisor(limited) and AWS personal Health Dashboard(provides alerts and remediation guidance when AWS is experiencing event that ay affect you)

Developer Support tier

    - basic support
    - email access to customer support
    - client-site diagnostic tools.

Business Support tier
    - basic and developer support
    - Trusted advisor provides full self best practice check
    - direct phone access to cloud support engineers( 4 hours),
    - limited support for third-party software, such common operating systems and application stack components.

Enterprise support

    - Consultative relationship to support your company’s specific use cases and applications, infrastructure event management, a technical account manager.
    - Technical Account Manager(TAM): the enterprise support plan includes access to a TAM.
    - It provides across the full range of AWS services.

AWS Marketplace is a digital catalog that includes thousand of software listings from independent software vendors. It helps you find, test, and buy software that runs on AWS.
You can access detailed information on pricing options, available support, and reviews Fromm other AWS customers.


Module 9

### Migration and Innovation

- Migrating from on premise to cloud or cloud to cloud. Or vise versa.

`AWS Cloud Adoption Framework(CAF)` organize guidance into six area of focus called perspectives

    - (Business, People, Governance, Platform, Security, Operations)
    - helps organizations understand how cloud adoption transforms the way they work, and it provides structure to identify and address gaps in skills and processes.
    - The first three focus on the business capability. And the rest focus on the technical capabilities.

Business ensure that IT aligns with business needs and that IT investments like to key business results.
Business managers, Finance managers, Budget managers,  strategy stakeholders


    - The Business Perspective helps you to move from a model that separates business and IT strategies into a business model that integrates IT strategy.

    - People supports development of an organization wide change management strategy for successful cloud adoption.(Prioritize training, staffing and organizational changes)
Human resources, staffing, people managers

    - The People Perspective helps Human Resources (HR) employees prepare their teams for cloud adoption by updating organizational processes and staff skills to include cloud-based competencies.

    - Governance focus on the skills and processes to align IT strategy with business strategy.( maximize the business value and minimize risk) update the staff skills and processes necessary to ensure business governance in the cloud.

Chief information Officer(CIO)
Program managers
Enterprise architects
Business analysts
Portfolia managers

Platform includes principle and patterns for implementing new solutions on the cloud and migration on-premises workloads to the cloud. (Understand and communicate the structure of IT systems and their relationships)
Chief Technology Officer(CTO)
IT managers
Solutions Architects

    - Security ensure that the organization meets security objectives for visibility, audibility, control and agility.

            - The Security Perspective of the AWS Cloud Adoption Framework also helps you to identify areas on non-compliance and plan ongoing security initiatives.

Chief Information Security Officer(CISO)
IT security managers
IT security analysts

    - Operations helps you to enable, run, use operate and recover IT workloads to the level agreed upon with your business stakeholders.

        IT operations managers
        IT support managers
	    The Operations Perspective focuses on operating and recovering IT workloads to meet the requirements of your business stakeholders.

### 6 strategies for Migration (The 6 R’s )

        Rehosting(lift and shift) involving moving applications without changes.

        Replatfoming (lift, tinker, and shift) involves making a few cloud optimization to realize a tangible benefit. Without chairing the core architecture of the application

        Refactoriing (rearchitecting ) involves reimagine how an application is architected and developed by using cloud-native features. (For strong need for business, add feature, scale or performance)

        Repurchaing involves moving from a traditional license to a software as a service model.

        Rataining keeping an application that are critical for the business source environment.(for temporary stay)

        Retiring is the process of removing applications that are no longer needed.

AWS snow family members is a collection of physical devices that help to physically transport up to exabytes of data into and out of AWS.
It is composed of AWS snowcone, Snowball, and Snowmobile.

    - SnowCone is a small, rugged, and secure edge computing and data transfer device.(2CPUs, 4GB of memory and 8TB of storage)

    - Snowball edge storage optimization device are well suited for large scale data migrations and recurring transfer workflows. (80 TB hard disk drive, 1 TB ssd, 40 cpus) machine learning, full motion video analysis, analytics, and local computing stacks.

    - Snowmobile is an exabyte scale data transfer service used to move large amounts of data to AWS.( up to 100 petabytes, 45 foot long ruggedized shipping container)

Innovation with AWS

Your properly equipped to drive innovation in the cloud if you can clearly articulate the following conditions.

    The current state
    The desired state
    The problems you’re trying to solve
    Consider some of the paths you might explore in the future as you continue on your cloud journey.
    Serverless applications (they don’t require to you provision maintain, or administer servers, no need to worry about fault tolerance or availability)
    For example AWS Lambda.

Artificial intelligence (

    - Converts speech to text with Amazon Transcribe
    - Discover patter in the text with Amazon comprehend
    - Identify potentially fraudulent online activities with Amazon Fraud Detector
    build voice and text chat-bots with Amazon Lex. In Amazon Lex, you can quickly build, test, and deploy conversational chatbots to use in your applications.
    - Is a machine learning service that automatically extract text and data from scanned documents Amazon textract
    AWS DeepRacer is autonomous 1/18 scale race car that you can use to test reinforcement learning models.

    - Machine Learning development is complex, expensive, time consuming, and error prone.
    - Amazon SegeMaker to remove the difficult work from the process and empower you to build, Train, and deploy ML mode quickly.
    - You can use ML to analyze data, solve complex problems, and predict outcomes before they happen.

Module 10

### The cloud Journey

A AWS well Architected Structure/Framework helps you understand how to design and operate reliable, secure, efficient, and cost-effective system in the AWS cloud.

1. `Operational Excellence` is the ability to run and monitor system to deliver business value and to continually improve supporting processes and procedures.

    - Operations as code, annotating documentation, anticipating failure, and frequently, making small, reversible changes.

2. `Security`The ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.

    - Automate security best practices when possible.
    - Apply security at all layers.
    - Protect data in-trainsit and at rest.

3. `Reliability`(having in a different AZ) recovery planing.

    - Recover from infrastructure of service disruptions, dynamically acquire cympitn resources to meet demand
    - Mitigate disruptions such as misconfigurations or transient network issues
    - Reliability includes testing recovery procedures, scaling horizontally to increase aggregate system availability, and automatically recovering from failure.
    - It focuses on the ability of a workload to consistently and correctly perform its intended functions

4. `Performance Efficiency` using the right resource efficiently. The ability to use computing resources efficiently to meet system requirements and to maintain that efficiency as demand changes and technologies evolve.

    - Evaluating the performance efficiency of your architecture includes experimenting more often, using serverless architectures, and designing systems to be able to go global in minutes.

5. `Cost optimization`is the ability to run systems to deliver business value at the lowest price point.

    - Cost optimization includes adopting a consumption model, analyzing and attributing expenditure, and using managed services to reduce the cost of ownership.

`07/18/2022`

Cloud computing is the on-demand delivery of IT resources(Compute power, database storage, applications) via the internet with the pay-as-you-go pricing model.
It enables you to stop thinking of infrastructure as hardware. Instead, you'll think of it as software.

    - OpEx(Operational Expenditure) day-to-day expenses.
    - CapEx(Capital Expenditure) major purchases for the long term.

Before Cloud Computing

`Hardware solutions are physical`

    - require space, staff, physical security, planning, and capital expenditure).
    You have to go through the time, effort, and cost required to change all these.


- Software is Flexible(Cost-effective, Elasticity)

    - IaaS lift and shift operations. More control over the resources.
    - PasS these are managed services. Eg. RDS
    - Saas It’s already running. Eg. Excel, word, email. Convenience.

Three Cloud Deployment Models

    1. All-in cloud(cloud native)
    2. On-premises (private cloud)
    3. Hybrid

### `On premises`

    - Large initial purchase
    - Labor, patches, and upgrades cycles
    - systems administration plus innovations
    - fixed capacity
        Examples: Storage Are Network (SAN) Network Attached Storage (NAS) Relational Database Management System (RDBMS)

### `All in cloud`

    - No upfront cost
    - Low ongoing costs
    - Focus on innovation
    - Flexible capacity


Important Cloud terminology
    - High Availability (accessible when you need it)
    - Fault Tolerance (Ability to waistbands a certain failure and still remain functional)
    - Elasticity (ability to grow when required)
    - Scalability (ability to easily grow in size)

## `6 Advantages of Cloud Computing`

    1. Capex to variable expenses(Trade upfront expense for variable expense)
    2. Economies of Scale(Benefits from massive economies of scale)
    3. Capacity Planning(You don’t have to guess about capacity)
    4. Increase Speed and Agility(rapid availability of new resources, innovation, Increase experiments)
    5. Stop Spending Money on Data Centers(focus on customers)
    6. Go Global in Minutes

What are Web Services?

   `A web service is any piece of software that makes itself available over the internet and uses standardized formate(XML or JSON)
    It’s a client-server relationship. AWS is a secure cloud services provider it has over 200 services.`

Ways to interact with AWS Services

    1. Management console
    2. AWS CLI
    3. Software development kits(SDKs)

Siz Core Perspectives

    1. Business
    2. People
    3. Governance
    4. Platform
    5. Security
    6. Operations

`An SA focuses on more Platform, Security, and Operations Perspectives.`

Cloud Economics

Pay for AWS (Compute, Outbound data transfer, Storage, aggregated outbound data transfer)
there’s no cost for data transfer between services within the same region.

AWS pricing Policy:

    1. At the end of each month, you pay for what you use.
    2. Start or stop using a product at any time
    3. No long-term contracts required

Pay less by using more (volume-based discounts): the more you use the less you pay.

Services with no charge:

    - VPC
    - IAM
    - Consolidated
    - billing
    - Cloud Formation
    - Auto-Scaling
    - OpsWorks

### $Total Cost of Ownership(TCO)$ is the financial estimate to help identify direct and indirect costs of a system.

	Why use it? to compare the expenses between on-premise and All in Cloud(AWS)

TCO gives you detailed reports with 3 year TCO comparison
### $Simple Monthly Calculator $: to estimate monthly costs(accurate cost estimates resource based)


### AWS Global Infrastructure

`Foundation services (compute, networking, and storage)`

`A data center` is a location where actual physical data resides. All data centers are online. No data center is cold.
Typically have 50k - 80k physical servers.

`A region` is a geographical area: consists of 2 or more availability zones. Communication between regions uses AWS’s backbone network(maybe AWS fiber??) connections infrastructure(they don’t use different ISPs because there might be latency).

There are 26 Regions and 84 Availability zones as of right now.

`Availability Zone` is made up of one or more data centers, designed for fault isolation, interconnected with other AZs using high-speed private links.

`Edge Locations` is where users access AWS services. over 400 edge locations.

## AWS Core Services

### Compute

`Amazon Elastic Compute Cloud(EC2)`: Virtual computing environment in the cloud - known as instances.
    - Storage for EC2 (amazon simple storage services S3, Elastic File system EFS, Elastic Block store EBS)
    HPC(high power(performance) computing)

    - AMI(Amazon Machine Image) defines the initial software that will be on an instance.It defines every aspect of the software state at instance launch: os configuration, initial state of any patches, application, or system software.

    Pricing
        - On-demand instances (per second(amazon Linux and Ubuntu only) and per hour billing. Short-term, spiky, or unpredictable workloads. application development or testing.
        - Spot Instances(great for unrecognized capacity and the instances can be interrupted) Large scale dynamic workload. Application with flexible start and end times. For the test environment.
        - Reserved Instances(Reserved for 1 or 3 years) used for steady state or predictable usage workloads.
        - Dedicated Hosts(per hour billing) won’t share hardware resources with other people. Bring your own license.

`AWS Lambda:` fully managed serverless compute

`Amazon EC2 Autoscaling:` scales ec2 capacity as needed. improves availability.

`Elastic Load Balancing:` Distributes incoming traffic, and helps achieve higher levels of fault tolerance.

`AWS Elastic Beanstalk:` Quickly deploys, scales, and manages web apps. No charge for it.

`Amazon LightSail:` manage simple web and application servers.

`Amazon Elastic Container Service(Amazon ECS):` highly scalable, high-performance, container management service.

`Amazon Elastic Kubernetes Service(Amazon EKS):` Run Kubernetes without managing Kubernetes clusters

`AWS Fargate:` Containers without server or cluster management.

## 4 pillars of Cost optimization

    1. Right-sizing
        - (On-demand instance, Reserved Instance(), Spot Instance, Dedicated Hosts)
        selecting the appropriate instance types
        Downsize instances
        Right size, then reserve.

    2. Reserved Instance
    - `1` or `3` years of commitment
    - up to 75% savings

    3. Increase Elasticity
        - Using an instance when you need it, turning it off when you don't.
    4. Monitor and Improve

        - `AWS Trusted Advisor` (to optimize your AWS environment, reduce cost, increase performance,a nd improve security)
        - `AWS Cost Explorer` (View graph of your costs: The last 13 months, forecast your likely costs: the next 3 months)

## AWS Lambda

    - Fully managed serverless compute
        No servers to manage f
        Continuous Scaling
    - Even-driven invocation
    - Sub-second metering
    - Function timeout (running time) limited to a maximum of 15 minutes
    - multiple languages supported
    - AWS lambda free tier includes one million free request per month and 400,000 GB-seconds of compute time per month
`GB-seconds` is the amount of RAM multiplied by execution time(seconds).

## Elastic Beanstalk

    - An easy to use service for deploying and scaling web applications and services developed with some of the commond programming languages.

`Benefits`

    Fast and Simple
    Developer productivity
    Impossible to Outgrow
    Complete Resource Control

- For more info [AWS Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/?trk=12eea001-bcfd-40ce-9788-748f73400e32&sc_channel=ps&sc_campaign=acquisition&sc_medium=ACQ-P|PS-GO|Non-Brand|Desktop|SU|Compute|Solution|US|EN|DSA&ef_id=EAIaIQobChMI6aHY1bGF-QIVka7ICh0yhQ1REAAYAiAAEgKNkPD_BwE:G:s&s_kwcid=AL!4422!3!587995325191!!!g!!)

## Storage Solutions

### Amazon Elastic Block Store

Amazon Elastic Block Store (Amazon EBS) offers persistent storage for Amazon EC2 instances. Amazon EBS volumes are network-attached and persist independently from the life of an instance. Amazon EBS volumes are highly available, highly reliable volumes that can be leveraged as an Amazon EC2 instances boot partition or attached to a running Amazon EC2 instance as a standard block device.

It's 1:1 Relationship: you cannot attach Block storage to multiple EC2 instances.

Amazon EBS volumes deliver the following features:

    - Persistent storage: Volume lifetime is independent of any particular Amazon EC2 instance.
    - General purpose: Amazon EBS volumes are raw, unformatted block devices that can be used from any operating system.
    - High performance: Amazon EBS volumes are equal to or better than local Amazon EC2 drives.
    - High reliability: Amazon EBS volumes have built-in redundancy within an Availability Zone.
    - Designed for resiliency: The AFR (Annual Failure Rate) of Amazon EBS is between 0.1% and 1%.
    - Variable size: Volume sizes range from 1 GB to 16 TB.
    - Easy to use: Amazon EBS volumes can be easily created, attached, backed up, restored, and deleted.

`Benefit`: Retains data after power to that device is shut off.

### Volume Types

    - Solid State General purpose (Recommended for most workloads)
    - Drivers(SSD) Provisioned IOPS(Critical Business applications, Large Database worklodas (RDSMS))
    - Hard Disk Drives Throughput-Optimized(Data Warehouse)
    - Hard Disk Drives(Cold) the cheapest storage. 125 GiB is the smalles size available.

When estimating cost for Amazon EBS always consider:

    - Volume
    - IOPS
    - Snapshots
    - Data Transfer

More information [Amazon EBS](https://cloudcheckr.com/cloud-management/amazon-ebs-elastic-block-store-guide/?utm_term=&utm_campaign=Dynamic+Search+Ads+-+CloudCheckr&utm_source=adwords&utm_medium=ppc&hsa_acc=7635390263&hsa_cam=15233138622&hsa_grp=129128446025&hsa_ad=561039230306&hsa_src=g&hsa_tgt=dsa-19959388920&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=EAIaIQobChMI29bIgLOF-QIVgY3ICh2GKgCVEAAYAyAAEgIB_fD_BwE)

## Amazon Simple Storage Service(S3)

`Object Level Storage` managed cloud storage solution designed to scale seamlessly and provide 11 9s of durability.
    - stores as many objects as you want.
    - Data is stored redundantly.
    - S3 cannot be used as a bootable drive.
    - Data in transit and at rest can be encrypted automatically(through customer or AWS keys management service key).

### Amazon S3 Storage Classes

    - Standard(default) it's for hot data, which will be requested very frequently.
    - Standard-IA(Infrequent access)
    - One Zone-IA(more of a secondary backup)

    - Intelligent-Tiering(it has an ML functionality implemented to it in order to move the object into different classes based on how frequently accessed)
    - Glacier and Glacier Deep Archive(for large amount of data intended for long term storage)

Use cases

    - Storing application assets
    - Static web hosting
    - Backup and Disaster Recovery
    - Staging area for big data

When estimating the cost of S3 consider:

    - Types of storage classes
    - Amount of Storage
    - Requests
    - Data transfer(transferring data into S3 is free)

Bucket Versioning helps to save the original data instead of over-writing it.

More info [Amazon S3](https://www.amazonaws.cn/en/s3/)

More on [S3 pricing](https://aws.amazon.com/s3/pricing/?nc=sn&loc=4)

### Amazon Elastic File System (Amazon EFS)

File storage in the AWS cloud

    - Petabyte-scale
    - Low latency file system
    - Shared storage
    - Elastic storage

Supports the Network File system versions 4.0 and 4.1 (NFSv4) Protocol
Compatible with all Linux-based AMIs for Amazon EC2

### Amazon Virtual Private Computer(VPC)

Amazon Virtual Private Cloud (Amazon VPC) enables you to launch Amazon Web Services (AWS) resources into a virtual network that you defined. This virtual network closely resembles a traditional network that you would operate in your own data center, with the benefits of using the scalable infrastructure of AWS. You can create a VPC that spans multiple Availability Zones.

Enables you to provision virtual networks hosted on the AWS Cloud and dedicated to your AWS account.
Are logically isolated from other virtual networks.
Enables complete control of network configuration, including

    - IP address ranges
    - Subnet creation
    - Route table creation

- `5 VPC per account`

Each Amazon VPC must specify the Ipv4 address range by choosing a Classless Inter-Domain Routing(CIDR) block like 10.0.0.0/16

- Subnets: Segment of a VPC's IP address range where you can launch AWS Services.
- Route Tables: used to control traffic going out of the subnets.
- Dynamic Host Configuration Protocol(DHCP) option sets: provides a standard for passing configuration information to hosts on a TCP/IP network
- Security Groups: A virtual, stateful firewall.
Network Access Control List(network ACLs): Control access to subnets, and they are stateless.

`Internet gateway`: Allow access to the internet from the VPC.
`Elastic IP Address`: Static, public IP address that can be pulled from a pool for use ona temporary basis.
`Elastic network interface` Virtual network interface.
`Endpoints`. Direct connection to another AWS service.
`Peering` Allows two VPCs to communicate.
`Network address translation(NAT) gateways`: Accepts, translates, and forwards traffic within a private subnet.

Security Groups:firewall for Amazon EC2 instances.

Security groups act like a built-in firewall for your virtual servers.
Security group rules determine who has access to instances.
Security groups are state-full(they can remember)

Network access control lists(network ACls): firewall for associated subnets.

    - by default it denies the inbound and outbound networks

Key pairs:(handshake between the resources) Cryptography used to encrypt and decrypt login information

AWS CloudFront(Content Delivery network)

### `Benefits`

- Global, Growing content Delivery Network
- Secure Content at the Edge Location
- Programmable Content Delivery Network (CDN)
- High performance:
    - Low Latency

Cost Estimation

    - Traffic Distribution
    - Requests
    - Data Transfer out
## $Database Services$

 Database is `a combination of compute and storage.`

`Amazon Relational Database Service` (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud.
It provides cost-efficient and resizable capacity while managing time-consuming database administration tasks, which allows you to focus on your applications and business.
Amazon RDS provides you with six familiar database engines to choose from: Amazon Aurora, Oracle, Microsoft SQL Server, PostgreSQL, MySQL and MariaDB.

Relational Databases(Challenges)

    - Server maintenance and energy footprint
    - Software installation and patches
    - Database backups and high availability
    - Limits on scalability
    - Data security
    - OS installation and patches.

Amazon RDS is a managed service. You only have to work on the App optimization.

## AWS Core Services Balancing Monitoring Scaling

### Elastic Load Balancer

Elastic Load Balancing automatically distributes incoming application traffic across multiple Amazon EC2 instances. It enables you to achieve fault tolerance in your applications by seamlessly providing the required amount of load balancing capacity needed to route application traffic.

Use cases(Decoupling architecture)

Application Load Balancer (ALB) - Layer 7
    - HTTP
    - HTTPS
    Network Load Balancer (NLB) - Layer 4
    - TCP - Transmission Control Protocol
    Classic Load Balancer (CLB) It doesn't allow IPv6
    - Previous Generation(HTTP, HTTPS, TCP)

Interested in OSI model [here](https://dev.to/mariamantar/the-osi-model-explained-1lj5)

`Scalability: scaling up and scaling down, Elasticity:`

### Auto Scaling

Auto Scaling helps you maintain application availability and allows you to scale your Amazon EC2 capacity out or in automatically according to conditions you define. You can use Auto Scaling to help ensure that you are running your desired number of Amazon EC2 instances. Auto Scaling can also automatically increase the number of Amazon EC2 instances during demand spikes to maintain performance and decrease capacity during lulls to reduce costs. Auto Scaling is well suited to applications that have stable demand patterns or that experience hourly, daily, or weekly variability in usage.

AWS Auto Scaling provides a simple, powerful user interface that enables you to build scaling plan for resources including

    - EC2
    - DynamoDB tables
    - DynamoDB tables and indexes
    - Aurora Replicas

- Scaling Out: `Launch Instances`
- Scaling in: `Terminate Instances`

`Elasticity vs Scalability` more info [here](https://stackoverflow.com/questions/9587919/what-is-the-difference-between-scalability-and-elasticity#:~:text=on%20this%20post.-,Scalability%20handles%20the%20increase%20and%20decrease%20of%20resources%20according%20to,decrease%20the%20resources%20as%20needed.)

### Amazon CloudWatch

Tracks and Monitors the perfomance and health of your resources and applications.

    - collect and monitor log files

To use AWS in an `efficeint` way, you need `insight` into your AWS resources

 CloudWatch Terms

- `Metric` to monitor data points

- `Alarm` to notify

- `Events` to monitor changes


## AWS Cloud Security

Shared Responsibility Model: AWS is responsible for security `of` the cloud and Customer is responsible for security `in` the cloud.

$AWS$

    - OS and database patching
    - Firewall configuration
    - Disaster recovery

$Customer$

    - Logical access controls
    - protect account credentials

`Un-managed Services`

    - EC2
    - EBS

`Managed Services`

    - DynamoDB
    - Amazon RDS
    - Redshift
    - EMR
    - WorkSpaces

### AWS IAM

AWS Identity and Access Management (IAM) is a web service that enables Amazon Web Services (AWS) customers to manage users and user permissions in AWS.
With IAM, you can centrally manage users, security credentials such as access keys, and permissions that control which AWS resources users can access.

The basic structure of the statements in an IAM Policy is:

- `Effect` says whether to Allow or Deny the permissions.
- `Action` specifies the API calls that can be made against an AWS Service (eg cloudwatch:ListMetrics).
- `Resource` defines the scope of entities covered by the policy rule (eg a specific Amazon S3 bucket or Amazon EC2 instance, or * which means any resource).

`IAM` Offered as a feature of your aws account for no charge, which centrally manage access and authentication of your users to your AWS resources.

### `User`

    - an entity you create in aws
    - allow individuals to interact with
    - IAM users aren't necessarily people

### `Group`

    - Collections of IAM users
    - User can belong to multiple groups
    - permissions are defined using IAM policies

### `Role`

    - temporary access
    - is similar to a user in that it is an AWS identity with permissions policies that determine what actions the role can perform.It is used to delegate access to users.

 ### `Policies`: JSON documents structured to permit or deny certain actions on AWS resources(A policy defines what actions are allowed or denied for specific AWS resources)

`Authentication`(who can access)
`Authorization`(what can they do): by default there's `implicit Deny` you need to `explicitly allow`

 - If something is explicitly denied, it can never be allowed.

` Principle of least privilege `

    - AWS Account Root user
    - IAM

Best Practices:

    - Delete root user access keys
    - create an IAM user: full admin can control everything except deleting the root user.
    - grant administrator access
    - Enable MFA
    - Use IAM credential to interact with AWS

## AWS Trusted Advisor

It's a customized cloud expert
    - helps you follow best practices
    - inspect your AWS environment
    - Helps close security gaps

Provides best practices, or checks, in five categories:

    - Cost Optimization
    - Performance
    - Security
    - Fault Tolerance: autoscaling, health check, multi AZ ...
    - Service Limits: checks for service usage

## CloudTrail

CloudTrail is a web service that records API calls for your account and delivers long files to you.

Tracks who's doing what.

`CloudWatch vs CloudTrail`
CloudWatch focuses on the activity of AWS services and resources, reporting on their health and performance. On the other hand, CloudTrail is a log of all actions that have taken place inside your AWS environment.

## AWS Config

It is a fully managed service that enables you to passes, audit, and evaluate the configuration of your AWS resources.

    Continuous monitoring
    Continuous assessment
    Change management
    Operation troubleshooting

Day One with AWS

1. Stop using the AWS root user
2. Require MFA
3. Enable CloudTrail
4. Enable a billing report like AWS Cost and Usage Report

## AWS Service Catalog

AWS Service Catalog can be integrated with AWS CloudFormation for stack developments to help you meet compliance with corporate standards.

- Help you meet compliance with corporate standards
- Help employees quickly find and deploy approved IT services
- Centrally manage IT service lifecycle


## AWS Security Resources

1. AWS Account Teams: first pint of contact
2. AWS Enterprise Support(15 mins response time, 24/7 by phone, chat, or email, dedicated technical Account manager(TAM))
3. AWS Professional Services and AWS Partner Network(APN)
    a group of APN consulting partners and technology partners

    - The AWS Partner Network (APN) is a group of cloud software and service vendors that includes hundreds of certified AWS Consulting Partners worldwide to assist customers with their security and compliance needs.

    - AWS Professional Services and APN both help customers develop security policies and procedures based on well-proven designs, and help customersso that theirsecurity designs can meetinternal and external compliance requirements.

More AWS compliance [here](https://aws.amazon.com/compliance/resources/)


## Cloud Architecting

### AWS Well-Architected Framework

Acronyms
OSCR P. WellArch, CROPS

The AWS Well-Architected Framework documents a set of foundational questions that enable you to understand whether a specific architecture aligns well with cloud best practices. The framework provides a consistent approach to evaluating systems against the qualities you expect from modern cloud-based systems and the remediation that would be required to achieve those qualities.

- Operational Excellence: `Deliver business value `
- Security: `Protect and monitor systems  `
- Reliability: `Recover from failure and mitigate disruption  `
- Performance Efficiency: `Use resources sparingly, Select customizable solutions, consider tradeoffs, continually innovate`
- Cost Optimization: `Eliminate unneeded expense `

## Well-Architected Framework Design Principles

Design principles to facilitate good design in the cloud

- Stop guessing your capacity needs.
- Test systems at production scale.
- Automate to make architectural experimentation easier.
- Allow for evolutionary architectures.
- Drive architectures using data
- Improve through game days.

## Reliability and High Availability

What is Reliability?

    Reliability is the probability that an entire system, including all hardware, firmware, and software, will satisfactorily function for a specified period of time. Simply put, reliability is a measure of how long the item performs its intended function.
Reliability is a measure of how long a resource performs its intended function.

### What is High Availability?

    High availability (or HA) is about minimizing your application's downtime as much as possible without the need for human intervention. It views availability not as a series of replicated physical components, but rather as a set of system-wide, shared resources that cooperate to run essential services. High availability combines software with open standard hardware to minimize downtime by quickly restoring essential services when a system, component, or application fails. While it is not instantaneous, services are restored rapidly, often in less than a minute.

#### What is Fault Tolerance?

    Fault tolerance is often confused with high availability, but fault tolerance refers to the built-in redundancy of an application's components and its ability to remain operational even if some of the components of that system fail. Fault tolerance relies on specialized hardware to detect a hardware fault and instantaneously switch to a redundant hardware component, whether the failed component is a processor, memory board, power supply, I/O subsystem, or storage subsystem. The fault-tolerant model does not address software failures, which are the most common reason for downtime.

RTO vs RPO

## Cloud Billing and Support Services

AWS Organizations is an account management service that enables you to consolidate multiple AWS accounts into anorganizationthat you create and centrally manage.

The main benefits of AWS Organizations are:

    - Centrally managed access policies across multiple AWS accounts.
    - Controlled access to AWS services.
    - Automated AWS account creation and management.
    - Consolidated billing across multiple AWS accounts.

## AWS Billing and Cost Management

AWS Billing and Cost Management enables you to pay your AWS bill, monitor your usage, and budget your costs.

    - Forecast Future Costs and Usage
    - Set Time Interval and Granularity
    - Filter or Group Data
    - Understand Underlying Cost drivers
    - Review AWS Usage and Costs

Tools

    1. AWS Bills
    2. AWS Cost Explorer
    3. AWS Budgets
    4. AWS Cost and Usage Reports

## AWS Support Services

Support is an essential element for any system. Outages can result in a loss of productivity, high overhead rates, and even lost customers. Sometimes, it is helpful to have support that can provide deeper insight into a product you are trying to use. To prevent these losses and frustrations, and tohave access to technical resources, you must understand your support options. Thissection willreview AWS Support and AWS Support Plans available to you.

Support Plans:

- Basic Support

        - Resource center access
        - Service Health Dashboard
        - Product FAQs
        - 24/7 access to customer service, documentation, whitepapers, and support forums.
        - Access to six core Trusted Advisor checks.
        - Access to Personal Health Dashboard

`No case support`

- Developer Support

        - Support for early development on AWS
        -  Want access to guidance and technical support.
        - Are exploring how to quickly put AWS to work.
        - Use AWS for non-production workloads or applications

- Business Support

        - Customers running production workloads
        - Run one or more applications in production environments.
        - Have multiple services activated, or use key services extensively.
        - Depend on their business solutions to be available, scalable, and secure

- Enterprise Support

        - customer running business and mission-critical workloads
        - Focus on proactive management to increase efficiency and availability.
        - Build and operate workloads following AWS best practices.•Use AWS expertise to support launches and migrations.
        - Use a Technical Account Manager (TAM), who provides technical expertise for the full range of AWS services and
        obtains a detailed understanding of your use case and technology architecture. The Technical Account Manager is
        the primary point of contact for ongoing support needs.



Network Foundation 

A computer network is a collection of computing devices that are physically and logically connected to communicate and share resources.

A node refers to any device on a network, whereas a host typically refers to servers on the network.
A host is a device to which other computers (nodes) can connect to access data or other services.

A switch is a small hardware device that connects multiple devices in the same network. It directs data traffic from a source to a destination device by switching the data from the source to the destination device. 

Computing devices connect to a switch by using a network interface card (NIC) and a cable. You will learn more about network adapters, NICs, and cables in the Computer network connectivity lesson.

A router acts as a dispatcher as it decides which way to send each packet of data. A router is located at any gateway (where one network meets another). A router connects multiple switches, and their respective networks, to enable communication between the different networks.
A LAN connects devices in a limited geographical area such as a floor, building, or campus. LANs commonly use the Ethernet standard (which you will learn about later) for connecting devices, and usually have a high data-transfer rate. Wireless technology is also commonly used for a LAN.

A WAN connects devices in a large geographical area such as in multiple cities or countries. WANs are used to connect LANs and use technologies such as fiber-optic cables and satellites to transmit data. The internet is considered to be the largest WAN.
In a client-server network model, the data management and application hosting are centralized at the server and distributed to the clients. All clients on the network must use the designated server to access shared files and information that are stored on the serving computer. 

If the server goes down, no client is able to access the network until the server is restored. Examples of client-server models are:

File server and desktop clients
Print server and desktop clients

In a peer-to-peer network model, each node has its own data and applications, and is responsible for its own management and security.

The peer-to-peer model is a distributed architecture that shares tasks or workloads among peers. Peers are equally privileged participants in the architecture. For example, files can be shared directly between systems on the network without the need for a central server.

This model might be considered under the following conditions:

Users are responsible for backing up each node.
Security requirements are not restrictive.
A limited number of peers are used.

Network topologies

After you understand the different management models, you can make a better decision about how the nodes in your network might be connected. Computer networks use different topologies to share information. A topology is a pattern (or diagram) that shows how nodes connect to each other. Computer networks have both physical topologies and logical topologies.

Physical topology - Refers to the physical layout of wires in the network
Logical topology - Refers to how data moves through the network
This lesson presents some historical topologies such as bus and star, and modern topologies such as mesh and hybrid.

Bus 

Physical topology

A bus topology positions all the devices on a network along a single cable. They run in a single direction from one end of the network to the other. A bus topology is also called a line topology or backbone topology. 

Logical topology

The data flow on the network also follows the route of the cable, and moves in one direction. 

A bus topology is simple to configure. However, it allows only one computer to send a signal at a time, which can cause network collisions that bring down the network.

Star 

Physical topology

A star topology is set up so that every node in the network is directly connected to one central switch by using coaxial, twisted-pair, or fiber-optic cable. You will learn about the different types of cable later in this module.

Logical topology

This central switch manages data transmission. Data that is sent from any node on the network must pass through the central switch to reach its destination. The central switch can also function as a repeater to prevent data loss.

Mesh 

Physical topology

A mesh topology is a complex structure of connections similar to peer-to-peer, where the nodes are interconnected. Mesh networks can be full or partial mesh. In a partial mesh topology, all devices are connected to at least two other devices.

In a full-mesh topology, all nodes are interconnected. A full mesh topology provides full redundancy for the network. It is an expensive topology because it requires each node to have multiple network adapters and cables. You will most likely find a full mesh topology in a WAN.

Hybrid topology

A hybrid topology combines two or more different topology structures. They are usually found in large organizations where separate departments have personalized network topologies to accommodate their network usage and other requirements. 

The star-bus topology is the most common hybrid topology today.

Nice work! Time for a knowledge check.


On Promise and AWS cloud 

Router -> Internet Gateway
Switch -> ELB 
Computer -> EC2
peer to peer -> vpc peering 
Server -> ec2
storage(block) -> ebs
storage(object) -> s3 
storage(file-level) - efs

# IP address 

Special IP addresses

When network is assigned a range of IP addresses such as 10.0.0.01 - 10.255.255.255, a few addressses that have a special that have a special purpose and are not assigned as host addreses. 

- These adddress are the default router address and the broadcast address


Example: Suppose the range of IP addresses is 10.0.0.0–10.255.255.255.

- The default router address is typically the second address in the range: 10.0.0.1
The default router address is also known as the gateway address, and it is the IP address of the network router.
The broadcast address is the last address in the range: 10.255.255.255
The broadcast address is used to transmit to all devices that are connected to a network. If a message is sent to a broadcast address, then all hosts on the network can receive it.


IPv4 addresses

IPv4 addresses are represented in 32-bit notation that consists of four 8-bit parts (octets) that are separated by a period or decimal point

Dotted-decimal notation is used to express each 8-bit part (octet) as a decimal number. Each individual octet—which is also known as a byte—can have a value in the range of 0–255 ( 0–28).

`IPv4 address space` – Because IPv4 uses 32-bit addresses, its address space is limited to 4,294,967,296 (232) addresses. 

IPv6 addresses

IPv6 was designed because the number of available unregistered IPv4 addresses was reaching its limit. IPv6 uses a 128-bit addressing scheme, and therefore has more than 79 octillion (7.9 x 1029) times as many available addresses as IPv4.


Typically, an IPv6 address consists of two 64-bit parts.

Network prefix - The network prefix is the leftmost 64 bits. It is used for routing to different networks.
The network prefix has two sub-components: the global routing prefix and the subnet ID.
Interface ID - The interface ID is the rightmost 64 bits and is similar to the host ID for IPv4 addresses. 


5 addresses for AWS
    - Network Router 
    - VPC router 
    - DNS 
    - Reserved
    - Broadcast 


lab 5 

Things we didn't understand

Exercise 1 and 3
#22
 10.1 How do you know which IP address to look for? 
 10.2 
#30
#39


### DNS

The boundary between internal networks and external networks is located at some type of secure gateway, such as a firewall. Many organizations maintain a small network segment on the external side of a firewall. This small segment is sometimes called a `demilitarized zone` (DMZ) because it resembles the buffer space between two hostile opponents on a battlefield. In networking, the DMZ provides a high-security buffer between an organization's network and a potentially hostile network (usually malicious traffic from the internet). Systems that are intended to handle sessions that originate from external networks are hardened against malicious events. They are placed in the DMZ to limit the scope of network vulnerability if their security becomes compromised.



## Module 6 

Just random: CROPS(Cost Optimized, Reliability, Operational Excellence,Performance efficient, Security)
Are you Well-Architected?

The principles that help maintain a secure network are governed by the CIA triad 
 1. confidentiality: The primary purpose of encryption is to keep information secret or private.
 2. integrity: it also ensures that the message is whole and not missing any parts
 3. availability

`Repudiation is the ability to deny that someone did something`

Trust is a key concept that allows devices to communicate with each other. 
    
    Trust can be direct or indirect.

Securiry Controls:

They can be divided into three main categories:

`Security controls are best practices that help network administrators maximize the chances of keeping networks safe`

    ## Administrative

    1. Administrative policies include rules that a company can put into place to govern employees' use of critical information and sensitive data
        
        Preventing phishing 
        Using data with care 
        Prevention against insider threats 

    2. Governmental Regulations 

        Rules and laws that are issued by governmental organizations can also be considered as administrative controls.

        Like HIPAA (Health Insurance Portablity and Accountability Act)

    ## Physical

        Physical security controls are procedures and physical security devices that reduce the possibility of unauthorized physical access to facilities, systems, and data.

            - Controls to protect facilites 
            - controls to protect hardware and systems 



    ## Technical

    Technical security controls are also known as logical security controls.
    This type of security control includes hardware and software that are used by an organization to help ensure the security and privacy of sensitive information.

        Firewalls 
        Antivirus software programs
        MFA 


## Business Continuity 

`System availability` means that you can access the services or applications provided by a system,
and it's also referred to as uptime.

The period of time when you can't access a system is called downtime. 

`Resiliency` refers to the ability of a workload (such as a website or an application) to recover from
infrastructure or service disruptions, dynamically acquire computing resources to meet demand, 
and mitigate disruptions (such as misconfigurations or transient network issues).

Availability is both a commonly used metric to quantitatively measure resiliency, and a target objective for resiliency. 
It corresponds to the percentage of time that a workload is available for use.

To maximize uptime, two aspects should be considered to ensure business continuity and increase security

    - hight availabity: system redundancy to prevent complete failure.

        - This kind of design aims for an accelerated recovery of the outage and, in comparison, it doesn't need a high level of redundancy. If a network device fails, redundancy must only be high enough to allow failover to another device.

    - fault tolerance: fast network recovery if network outages occur.

        - Redundancy is key to keeping the network and services working. Partial redundancy ensures that services will continue to work even if they work at a slower rate.

`Fault-tolerant designs are usually more expensive than highly available ones.`

Remember that a highly available system is not necessarily `fault tolerant`. In contrast, a fault-tolerant system is always said to be `highly available`. 

## Disaster Recovery

`Disaster recovery (DR)` is a strategy for recovering a workload if a disaster occurs, whether it's a natural disaster, a large-scale technical failure, or a human threat (such as malicious intrusions or errors). 

    - Recovery Time Objective (RTO)

        - is defined by the organization. RTO is the maximum accpetable delay between the interruptions of a service and the restoration of service. This objective determines the acceptable amount of time for service to be unavailable. 

    - Recovery Point Objective (RPO)

        - RPO is the maximum acceptable amount of time since the last data recovery point (for example, the last backup). This objective determines the acceptable amount of data loss that occurs between the last recovery point and the interruption of service. 



## strategies to implement DR

- Cold standby(also called backup and restore)

    - you must regularly save backups of your data. this infrastructure is not used until a disaster occurs

- Pilot Light 

    - minimum infrastrucutre that your businesss needs to run(replica)
    - The second component started only if they are needed.

- Warm Standby 

    - For an on-premises infrastructure, warm standby requires a copy of the infrastructure. updated regularly. but it stays off most of the time.
    - In a cloud environment, warm standby requires a scaled-down, but fully functional, version of the workload that always runs.


- Hot Standby 

    - This strategy requires a complete duplicate of the infrastructure. This copy always runs, but it doesn't receive any production load until it's needed. When it's needed, the DR site can handle the entire load.

- Load Balancing 

    - the load is shared between the two copies. If one infrastructure goes down, the other infrastructure can handle the production load.



## Encryption and Tunneling 

Encryption is the process of converting an original message(plain text) into an encoded message(ciphertext). Decryption is the process of converting ciphertext back to its original plaintext.

`A cryptographic key` (or key) is some mathematical value that's provided to an encryption/decryption algorithm.

In symmetric key encryption (or symmetric encryption), the same key must be used to decrypt the ciphertext.

    - a message sender and receiver share the same key

In asymmetric key encryption (or asymmetric encryption), a different key—which is matched with the encryption key—must be used to decrypt the ciphertext.

    - Public key encryption is an example of an asymmetric encryption technique.

`One-way encryption` (or cryptographic hashing) converts plaintext of any size to a number with a fixed size. The cipher in one-way encryption is a mathematical function, called a cryptographic hash function or hash algorithm.

    
- `Encryption at rest and in transit. `

Envelope encryption is the practice of encrypting plaintext data with a data key, and then encrypting the data key under another key.

- Master key -> Data key -> Data 

### Tunneling 

Tunneling refers to hiding one data stream inside another. It's a form of data encapsulation.


`Social engineering,` which uses human psychology to trick or force a person into giving up sensitive information or making a financial payment. 

`Malware` is a broad term for malicious software that's intentionally designed to harm a computer, server, client, or network.

Types of malware include

    - viruses, 
    - Trojan horses - designed to mislead the user of its true intent 
    - ransomware: malware that threatens to block access or publish a user's data unless a payment is made to the attacker 
    - backdoors: A backdoor is a way for users to get around normal authentication and authorization for a computer, network, or service.

         Gaining unauthorized access. 

Phishing is a type of social engineering where an unauthorized user tries to get sensitive or personal information from a target by impersonating trusted organizations, companies, or people.

    
Spear Phishing toward a specific user, business, or organization. 


## Systems Security 

System hardening: 

    Defining the minimal system
    Locking down ports 
    patching 
    Using the principle of least privilage 
    changing default access 

Intrusion detection: 

    File signature database 
    Anomaly-based intrusion detection systems: uses AI to predict a model that corresponds to a normal situation for the system's activity. 

    Log analysis: to detect abnormal system activity. 


Gaining unauthorized acccess to a network is called `network intrusion`

## Firewalls 

a firewall is a special device that's placed on the boundary of a trusted network (which is also called a private network) to block undesired network traffic from a connected untrusted network (which is also called a public network).

    Filer Rules: allow some traffic to flow through it. 
    Deep Packet Inspection: 
    Stateful and stateless: 

An IDS(Intrusion Detection system) uses various monitoring and logging data to detect network intrusions. 
An IPS(Intrusion Prevention system) detects intrusion attempts, and also takes action to stop an intrusion attempt (and hopefully prevent the intrusion from succeeding).

## Network Address Translation(NAT)

     - maps an internal (or private) IP address to an external (or public) IP address. 
     - NAT can provide one-to-one mapping, or many-to-one mapping (multiple internal hosts using the same IP address, but at different times).

     - The primary purpose of NAT was to conserve IP address space. 

## Demilitarized Zone(DMZ)
    
    - When an organization needs to provide public-facing applications and services, these applications and services are often hosted in systems that reside in a small network segment on the external side of a firewall.

`DMZ acts as a high-security buffer space between a trusted network and an untrusted network`

## Bastion Host 
A bastion host is a system that enables a network administrator or systems administrator to access internal (or private) systems from an external (or public) network.

The ability to jump from the bastion host to another system is why a bastion host can also be called a jump box.

## Man-in-the-middle attack 

   - a type of attack where two parties believe that they are communicating directly with each other, but a malicious actor is intercepting the messages and injecting new ones.


POC Deliverable 

    Proof 
    - Login to instance and ping to another ec2 instance 
    - Diagram 
    - well architected framework 

## Secure Communication 

    PKI(Public key infrastructure)

        -  is used to encrypt and authenticate data transfers between a server and a client. 
        - it works by using one key for encryption and one key for decryption. 

    Pretty Good Privacy (PGP) is an encryption system that gives users the ability to communicate privately online

            Standard for email security. 

    Transport Layer Security (TLS) is a protocol that establishes encrypted sessions between applications across the internet.

            TLS accomplishes three main goals: encryption, authentication, and integrity.


    Internet Protocol Security (IPSec) is a set of protocols that are used together to secure data transmissions. 

            - It works at the Network Layer 
            - Encapsulating Security Payload (ESP) is a protocol header that protects the upper layer. ESP can be used to ensure confidentiality, authentication, and data integrity.


## Availability and Denial of service attacks

- `Availability` means that the applications and services of a business can be reached and used properly.

`Denial of service attack ` is when a malicious attempt that could lead to network downtime. 
When it's from multiple soureces at the same time it's referred to as Distributed denial of Service(DDOS)

    This attack is mainly on Layer 3, 4, 6 and 7. 
    Attack at the Infrastructure layer(3 and 4)
    At the application layer(6 and 7)

## Defenses against DDOS

    Redundancy and over provisioniing

    - Transit Capacity: ensure that you have ample redundant internet connectivity that enables you to handle large volumes of traffic.

    - Server Capacity: it's important for you to have sufficient compute resources.

        - use load balancer 

    - Rate Throttling is a way to slow traffic so that it doen'st exceed a defined limit. 


`Availability` is a key component for helping ensure that your business is secure. You should consider two aspects to ensure business availability: 

    - defending against malicious agents, and 
    - ensuring that the network infrastructure can manage traffic and requests if peak requests or system failures occur.

    Use a tool to connect to your devices and get responses from them to confirm that they are running. 

    Monitor traffic to your workload so that you can avoid exceeding the capacity of your system.


## Module 7


### Hardware Virtualization

    An OS is the system software that supports a computer's basic functions, such as scheduling tasks, running applications, and controlling peripherals. 

    An OS manages all of the software and hardware on the computer. 
    It manages:
        - CPU 
        - memory 
        - Storage
        - Networking 

`Hardware virtualization` is the virtualization of hardware, such as compute, storage, and networking resources. It refers to the process of making a virtual (as opposed to an actual) version of a hardware component. 

        - provides logical abstraction and isolatin, which makes it possible to run multiple copies of operating systems.

        - Hardware virtualization allows multiple operating systems to run on one physical server. 

`A Virtual Machine:` 

    A virtual machine (VM) is an emulation of a computer that is implemented with software, and provides the same functionality as a physical computer. 

Hypervisor 

    - Virtualization enables a single physical server to run several operating systems at the same time. 
    This setup requires another layer of computer software, known as a hypervisor, to manage the complex interactions between VMs and the physical server.

    Each Virtual machine is called a guest machine, and the operating system inside a virtual machine is called the guest OS. 


The advantages of Virtuatlization: separate computing environment from physical hardware, and run multiple operating systems. 

    - usefule for software development and testing
    - server consolidation 

Virtualization is a large part of the technology that makes cloud computing possible. 


Network Planes 

    1. Data plane: receive packet and forwards them to different network devices. 
    2. The control plane: determine how the entering packets will be handled and which devices they will be sent to.
    3. Management plane: The user interface used to monitor and configure a network device. 


### On Premises 

"A house or building, together with its land and outbuildings, occupied by a business or considered in an official context." according to Lexico.com

The term On premises usually described as customer's network or a elements of the customer network that are not running in AWS. 

Concerns on the on premise 

    - Network and system Security 
    - Secure disposal 
    - Security compliance 

`Procurement` is the process that businesses and organizations use to buy equipment and software.

`Provisioning` is the process of installing and configuring equipment, software, and services.

`Demand` describes the amount of a resource that's requested by one or more resource consumers over a specific amount of time.

`Capacity` describes the maximum amount of resource that a resource provider can provide.

`Load` measures how much resource is currently in use (or allocated) over a specific amount of time.

`Scalability` is a system's ability to grow to accommodate an increase in demand. Scalability is limited by hardware.

Business continuity is an organization's ability to maintain operations if a system failure, service outage, or disaster occurs

Workload: A set of components that together deliver business value. The workload is usually the level of detail that business and technology leaders communicate about. 

Reliability: The ability of a workload to perform its intended function correctly and consistently when it’s expected to.

Availability: The percentage of time that a workload is available for use, where available for use means that the workload performs its agreed function when required.

Resiliency: The ability of a workload to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions (such as misconfigurations or temporary network issues).

Fault tolerance: The ability of a workload to continue performing its intended function (uninterrupted) if an infrastructure failure or service disruption occurs.

    Fault tolerance differs from resiliency in that a resilient system might suffer an outage from an infrastructure failure, but recover quickly. 

 Disaster recovery (DR): The resources and procedures that enable the recovery or continued operation of core business functions. DR is similar in concept to network resiliency.


 Hardware, software, systems, and networks can (and do) fail at any time.    


Cost 

Most other concerns when you design a network can be translated into a monetary cost. 

    1. Equipment (including network hardware and hardware that doesn't support the network directly)
    2. Software 
    3. Network links and telecommunications services
    4. Personnel (including network operations staff, technicians, security guards, and cleaning staff)
    5. The building or facility
    6. Electricity
    7. Maintenance and repair of physical systems (both network hardware, and systems such as the air conditioning for the building)



    Whiteboarding

    name, date, contact info
    forcus on the customer's pain point 

    Bluescape: real-time collaboration, making it easy for people to create, interact with, and share content. 

        uses sticky note, callouts, and annotations to your board. 

    Rough calculation On premise data center calculation
    Arround 90k
        Servers: 13.3 k
        Switches:  1.3k
        Routers: 7k
        Racks: 10k
        HVAC: 4.8k
        UPS: 42k
        Security(physica):1k
        Space: 9.6k
        Cabling: 1.2k


## The AWS Well-Architected Framework 

- in the Traditional Environment, customers,

    - Had to guess infrastructure needs 
    - Could not afford to test at scale 
    - Had a fear of change 
    - Could not justify experiments 
    - Face architecture that was frozen in time 
    

    In the cloud environment 

    stop guessing capacity needs 
    Test at production scale 
    Make experimentation easier 
    Allow for architectures to evolve 
    Build data-driven architectures 
    Improve through Game days 

When architecting a solutions you should always have to have a good foundation. 

`Operational Excellence` Pillar: the ability to run and monitor systems to delliver business value and to continually improve supporting process and procedures. 

    - Organizational structure 
    - Prepare (review the rediness of your solution)
    - Operate
    - Evolve(learning from experience and making improvement) 

`Security`: to protect information, systems, and assets while delivering business valut throgh risk assessments and mitigatoin strategies. 

    - Identity and access management 
    - Detection 
    - Infrastructure protection 
    - Data protection 
    - Incident response 

`Reliability`: the ability to recover from failures and meet demand in the following areas 

    - Foundatoins 
    - Worklad architecture 
    - Change management 
    - Failure management 

`Performance Efficiency`: the ability to use your IT resources efficiently to meet the system requirements. It evolve 

    - Selection 
    - Review 
    - Monitoring 
    - Trade-offs 

`Cost Optimization` : The ability to achieve business outcomes at the lowest price point 

    - Practice Cloud Financial Management 
    - Expenditure and usage awareness 
    - Cost-effective resources 
    - Manage demand and suppply resources 
    - Optimize over time 


Common uses 

    - Learn how to build cloud-native architectures 
    - Build a backlog 
    - Use as a gating mechanism before launch 
    - Compare maturity of different teams
    - Perform due diligence for acquisitions(What state the architectures in)

It enable people to think cloud natively 


## Highly Available Web Applications


Amazon VPC is the networking layer for Amazon Elastic Compute Cloud (Amazon EC2). Amazon EC2 is a web service that provides secure, resizable compute capacity in the cloud.

Amazon EC2 virtual servers are called instances. Instances launch within subnets (smaller networks within the VPC). 

    - Public subnets are directly connected to the internet, and usually contain internet-accessible instances, such as web servers.
    - Private subnets do not have a direct connection to the internet. 

### Amazon VPC concepts 

    1. Subnet - A range of IP addresses in your VPC.
    2. Route table - A set of rules, which are called routes, that are used to determine where network traffic is directed.
    3. Internet gateway - A gateway that you attach to your VPC to enable communication between resources in your VPC and the internet.
    4. VPC endpoint - Use a VPC endpoint to privately connect your VPC to supported AWS services without using an internet connection. Traffic between your VPC and the other service does not leave the Amazon network. This feature can be helpful when regulatory requirements mandate that traffic must not cross the internet.
    5. Classless Inter-Domain Routing (CIDR) block - You associate a CIDR block with each VPC. All resources within the VPC use addresses from that block.

    
You cannot increase or decrease the size of an existing CIDR block.


Elastic Network Interface

An elastic network interface (sometimes referred to as a network interface) is a logical networking component in a VPC that represents a virtual network card. Each instance has a default network interface, which is called the primary network interface.

You cannot `detach a primary network interface` from an instance. You can create and attach additional network interfaces. 

When you move a network interface from one instance to another, network traffic is redirected to the new instance. 

### Route tables

A VPC is said to have an implicit router.
The routing rules are stored in tables, which are called route tables.

A target of `local` means that the destination network is inside the VPC

One route table can be used by multiple subnets. However, each subnet can be associated with only one route table.

The `internet gateway` is a VPC component that enables communication between your VPC and the internet. 
It appears as a single component in an architecture diagram. However, it represents infrastructure that is horizontally scaled (adapts to handle high bandwidth), redundant (provides fault tolerance for the internet connection), and highly available.

An internet gateway serves two purposes. One purpose is to provide a target in your VPC route tables for internet-routable traffic. The other purpose to perform network address translation (NAT) for instances that have been assigned public IPv4 addresses.

A subnet whose route table has a route to an internet gateway is called a public subnet. A subnet without a target as internet gateway is called a private subnet.

Elastic IP addresses are fixed, and they help you mask the failure of an instance by rapidly manually remapping the address to another instance.

A security group provides instance-level network. A network access control list (network ACL) provides subnet-level network security. Security groups and network ACLs also control traffic within the VPC.


### Security Group
A security group acts as a virtual firewall for your instance to control inbound and outbound traffic by using rules.

        - Security groups act at the elastic network interface level of an instance.
        - Up to five security groups can be assigned to a single instance.

        In a default security group, all incoming requests from any source that does not use the default security group are blocked. All outgoing requests are allowed. 

### Network ACL
A network ACL provides another layer of security for your VPC. It acts as a firewall for controlling traffic that moves into and out of one or more subnets.

        - The default network ACL allows all inbound and outbound traffic.
        - a subnet can be associated with only one network ACL at a time. 
        - When you associate a network ACL with a subnet, the previous association is automatically removed. By default, each custom network ACL denies all inbound and outbound traffic until you add rules.  



AWS Site-to-Site VPN supports two types of routing, depending on whether the customer gateway supports Border Gateway Protocol (BGP):

Dynamic routing (uses BGP): The customer gateway uses BGP to advertise routes to the virtual private gateway. 
Static routing (does not use BGP): You specify the routes (IP prefixes) for your network that should be communicated to the virtual private gateway.

        - To maintain high availability, you can set up redundant customer gateway devices.
        - 

### AWS Direct Connet 

AWS Direct Connect is a cloud service that facilitates establishing a dedicated network connection between your network and one of the AWS Direct Connect locations.

        - Using standard Ethernet fiber-optic cables (802.1q)

Use case 

        - Hybrid environment: Applications that require access to existing data center equipment, such as an on-premises database
        - Frequently transferring large datasets: Applications that operate on large datasets, such as high performance computing (HPC) applications, because
        - Network-sensitive applications:Applications that require predictable network performance, such as those applications that operate on real time data feeds (for example, audio or video streams) 
        - Security and compliance: Enterprise security or regulatory policies sometimes require that applications that are hosted in AWS can be accessed through private network circuits only 


Highly resilient, fault-tolerant network connections are key to a well-architected system. AWS recommends connecting from multiple data centers for physical location redundancy. When you design remote connections, consider using redundant hardware and telecommunications providers.

For critical production workloads that require high resiliency, AWS recommends that you have at least one connection at multiple Direct Connect locations. This topology helps to ensure resilience against connectivity failures because of a hardware failure or a complete location failure. 


Use AWS Direct Connect gateway to use a single AWS Direct Connect connection to connect to multiple VPCs. You associate an AWS Direct Connect gateway with either of the following gateways:

`Who and what when answering well architected framwork `

### Networking on AWS 

Traditional networking is difficult. It involves equipment, cabling, complex configurations, and specialist skills. Amazon Virtual Private Cloud (Amazon VPC) hides the complexity, and simplifies the deployment of secure private networks.

Traditional computing, or on-premises computing, can be expensive because it requires you to guess peak capacity needs for your workload. Guessing peak capacity requires substantial upfront investments to have your system ready to run. Additionally, traditional servers can take weeks to months to acquire and set up. Inevitably, servers will become outdated, and you will need to go through the process again to get newer servers.

## EC2 instance type families

General purpose instances provide a balance of compute, memory, and networking resources. 
(M, T, A, Mac)

Compute optimized instances are ideal for compute-bound applications that benefit from high performance processors. These instances are well suited for compute-intensive applications.

(C)

Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.

(R, X, U-, Z)

Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage.

(I, D, H)

Accelerated computing instances use hardware accelerators, or co-processors, to perform functions such as graphics processing or data pattern matching more efficiently using CPUs.

(P, Inf1, G, F)


## AWS Storage Services 


An `instance store` provides temporary block-level storage for your instance.
`Block storage `is a type of storage that emulates the behavior of regular hard disks for data storage. 
`File storage` is a method for storing unstructured data in the cloud that provides servers and applications shared access to data. This capability makes cloud file storage ideal for workloads that rely on shared file systems.
`Object storage` provides massively scalable, cost-effective storage to store any type of data in its native format. AWS object storage solutions Amazon S3 and Amazon S3 Glacier offer very high availability, durability, and scalability while providing security and compliance.

The CAP theorem: The CAP theorem describes a relationship between consistency, availability, and partition tolerance. The theorem says that it is not possible to provide all of the three concepts at the same time when working with distributed systems.

1. Consistency: it always receives the latest version of the data requested.  
2. Availability: the client always receives a response that is not an error. 
3. Partion tolerance: mean that the network can work despite communication errors. 

`Amazon S3 is strongly consistent`

AWS Storage Gateway 

A file gateway provides a file interface into Amazon S3 through a virtual software appliance.

A volume gateway provides cloud-backed storage volumes that you can mount as Internet Small Computer System Interface (iSCSI) devices from your on-premises application servers.


## Scaling in AWS


Cloud Watch 

Monitoring your system is essential to obtaining a reactive architecture. By closely monitoring your workload, you can track resource utilization and application performance so that your infrastructure is meeting demand.

CloudWatch provides you with data and actionable insights to help you monitor your applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health.

EventBridge is a serverless event bus (a shared channel that allows communication between defined sources and targets in a system) that makes it easier to build event-driven applications at scale using events generated from your applications, integrated software-as-a-service (SaaS) applications, and AWS services.

For a business, scalability is key to adapting to changing workloads. Scalability measures the ability to easily grow in size, capacity, or scope when required, particularly in response to demand.

An application running in the cloud is elastic, meaning you can add more resources (to scale out) or terminate resources (to scale in) if needed, which results in reduced costs.

Manual sclaing: Need constant EC2?
Scheduled scaling: Schedule based?
Use metrics: Target tracking scaling?
Predictive scaling: machine learning, fine tunning? 


## Elastic Load Balancing 

ELB automatically distributes your incoming traffic across multiple targets.uch targets might include Amazon Elastic Compute Cloud (Amazon EC2) instances, AWS Lambda, containers, and IP addresses in one or more Availability Zones. 

`Using a load balancer increases the availability and fault tolerance of your applications.`

The ELB service offers four types of load balancers:    
        
        - Application Load Balancer: layer 7 http/s
        with an Application Load Balancer, it is a requirement that you enable at least two or more Availability Zones.
        - Network Load Balancer: layer 4 network protocol and port number 
        - Gateway Load Balancer: a single entry/exit point and load balancing for virtual applicances. Examples include firewalls, intrusion detection and prevention systems (IDPS), and deep packet inspection systems.
        - Classic Load Balancer: Applications that run in an Amazon VPC should use the other types of load balancers.


A `load balancer` serves as the single point of contact for clients. The load balancer distributes incoming traffic across multiple targets, such as EC2 instances. This distribution increases the availability of your application. You add one or more listeners to your load balancer.

A `listener` checks for connection requests from clients by using the protocol and port that you configure. The rules that you define for a listener determine how the load balancer routes requests to its registered targets. Each rule consists of a priority, one or more actions, and one or more conditions.

Each `target group` routes requests to one or more registered targets, such as EC2 instances. It uses the TCP or UDP protocol and the port number that you specify.

Your load balancer periodically sends requests to its registered targets to test their status. These tests are called `health checks`.

How an Application Load Balancer works

After the load balancer receives a request, it evaluates the listener rules in priority order to determine which rule to apply.

Application Load Balancer pricing

You are charged for each hour or partial hour that an Application Load Balancer is running and the number of Load Balancer Capacity Units (LCUs) used per hour. An LCU is the highest single measure (average over an hour) of:


ALB pricing [Link](https://aws.amazon.com/elasticloadbalancing/pricing)
AWS Free Tier
Get started with Elastic Load Balancing for free with the AWS Free Tier. Upon sign-up, new AWS customers receive 750 hours per month shared between Classic and Application load balancers; 15 GB of data processing for Classic load balancers; and 15 LCUs for Application Load Balancers.

For Application Load Balancers in the AWS Region:

        $0.0225 per Application Load Balancer-hour (or partial hour)
        $0.008 per LCU-hour (or partial hour)
        For Application Load Balancers on Outposts:

        $0.0225 per Application Load Balancer-hour (or partial hour)
        $0.00 per LCU-hour (or partial hour)

NLB 
For TCP traffic, the load balancer selects a target based on the protocol, source IP address, source port, destination IP address, destination port, and TCP sequence number.

Network Load Balancer pricing

You are charged for each hour or partial hour that a Network Load Balancer is running and the number of Network Load Balancer Capacity Units (NLCU) used per hour. An NLCU is the highest single measure (averaged over an hour) of: 


Gateway Load Balancer pricing

You are charged for each hour or partial hour that a Gateway Load Balancer is running and the number of Gateway Load Balancer Capacity Units (GLCU) used per hour. A GLCU is the highest single measure (averaged over an hour) of:

        New connections or flows
        Active connections or flows
        Processed bytes

        Gateway Load Balancer uses Gateway Load Balancer Endpoint (GWLBE) to securely exchange traffic across VPC boundaries. GWLBE is priced and billed separately.



Analyzing the customer’s current architecture against the Well-Architected Framework leads to the following observations:

`Operational excellence`: Anticipating failure by testing failure scenarios provides few benefits. This architecture has two failure scenarios (loss of the single EC2 instance or loss of the single Availability Zone). Each scenario causes the application to be unavailable. The current architecture also lacks scalability. If the resources of the single EC2 instance are insufficient to handle application demand, performance, and availability could be affected.
`Security:` Users directly access the application by connecting to the EC2 instance by using a public subnet. This practice is contrary to the recommendation that architectures should reduce or eliminate the need for direct access to data.
`Reliability:` The current architecture lacks automatic recovery from failure. If the single EC2 instance or the Availability Zone fails, the application becomes unavailable until manual actions are taken to correct the failure.
`Performance efficiency: `Performance suffers if user traffic spikes to a level that exceeds the capacity of the single EC2 instance.
`Cost optimization:` The only way that the current architecture can meet the requirements for spikes in usage is to overprovision the single EC2 instance to meet estimated peak demands. As a result, it incurs unnecessary costs during non-peak periods.


This architecture delivers on the customer’s requirements and aligns with many of the pillars of the Well-Architected Framework:

`Operational excellence:` The EC2 Auto Scaling group automatically adds and removes application instances as needed. As soon as it’s configured, the Elastic Load Balancer is managed and maintained for you. Failure scenarios can be tested by terminating instances or simulating the loss of an Availability Zone. (`Gaining insight into their operations`)

    Tools to use
        CludWatch(x-ray)
        Cloud Trails



`Security:` The Elastic Load Balancer protects the application instances from direct access from the internet. The use of private subnets for the EC2 instances provides access control through the use of security groups and network ACLs. 

    Tools 
        SG's, ACLS, Private Subnets, encryptions, WAF

`Reliability:` The application can automatically recover from instance failure or Availability Zone failure by redirecting traffic to the surviving Availability Zone and instances. 

    Tools 
        Multible azs 
        Read replica 
        Autoscaling 
        Elastic Load balancers 
            Problem using Database on Instance is (installing database into servers may not go with the technology in hand(for management))
            Just do the homogenius migration using the aws Database Migration Service 

        Standby database 
        Backups 

`Performance efficiency:` The application will automatically scale in and out based on user demand. As `technologies evolve`

    Tools 
        right sizing, autoscaling 

`Cost optimization:` Additional resources are added only when needed, and they are automatically removed when demand drops.

    Tools 
        Cost explorer(to check and monitor their expenses)


## `Docker `

Containers are a method of operating system virtualization that you can use to run an application and its dependencies in resource-isolated processes.

        - A container is a lightweight, standalone software package.
        - It contains everything that a software application needs to run, such as the application code, runtime engine, system tools, system libraries, and configurations. 

Containers can help ensure that applications deploy quickly, reliably, and consistently, regardless of deployment environment. Containers also give you more granular control over resources, which improves the efficiency of your infrastructure.

A `container` is created from a read-only template that is called an image. Images are typically built from a Dockerfile, which is a plaintext file that specifies all the components that are included in the container.

## AWS RDS

AWS Responsibility

1. No ssh access for users 
2. No manual DB patching 
3. No manual OS patching 
4. No way audit the underlying instance 

Amazon RDS is a relational database service that provides cost-efficient and resizable capacity while automating administration tasks such as hardware provisioning, database setup, patching, and backups.

The code, applications, and tools that you use with your on-premises relational databases will work seamlessly with Amazon RDS when you migrate to the Amazon Web Services (AWS) cloud. You can migrate a database to Amazon RDS by using AWS Database Migration Service (AWS DMS). 

In addition, with Amazon RDS, you can use replication to enhance database `availability` and improve data `durability`.
Moreover, many Amazon RDS engine types offer encryption at rest and encryption in transit.

Because Amazon RDS is fully managed, you can focus on building and improving your applications. You can concentrate on getting faster results rather than spending time administrating your relational databases.

When thinking about your architecture, you should always keep in mind the Well-Architected Framework best practices. According to the Well-Architected Framework, your architecture should provide performance efficiency and should be reliable. The performance efficiency pillar focuses on using the resources efficiently.

Compute scaling

The DB instance class determines the computation and memory capacity of an Amazon RDS DB instance. 

    Amazon RDS offers three types of instance classes: standard, memory optimized, and burstable performance.

Storage scaling

Amazon RDS uses Amazon Elastic Block Store (Amazon EBS) volumes for database and log storage.

        Amazon RDS provides three storage types: General Purpose SSD, Provisioned IOPS SSD, and Magnetic (also known as standard).

Also, if you plan a Multi-AZ deployment (discussed later in this lesson), AWS recommends that you use provisioned IOPS SSD disks to reduce latency.

`Read replicas` are a special type of DB instance. Read replicas are created from a source DB instance. Amazon RDS takes a snapshot of the source instance and creates a `read-only` instance from the snapshot.

However, creating a cross-Region read replica isn't supported for SQL Server on Amazon RDS.

Automated backups

The automated backup feature of Amazon RDS enables point-in-time recovery of your DB instance. Amazon RDS provides backup storage of up to 100 percent of your provisioned database storage at no extra charge. 

Amazon RDS provides high availability and failover support for DB instances by using Multi-AZ deployments. Amazon RDS uses several different technologies to provide failover support.

In a Multi-AZ deployment, Amazon RDS automatically provisions and maintains a synchronous standby replica in a different Availability Zone. it provides data redundancy, eliminates I/O freezes, and minimizes latency spikes during system backups. 

However, DB instances that use Multi-AZ deployments can have increased write and commit latency compared to a Single-AZ deployment. This increase is due to the synchronous data replication that occurs. For production workloads, it is best to use Provisioned IOPS and DB instance classes that are optimized for Provisioned IOPS for fast, consistent performance. 


it is possible to modify it to a Multi-AZ deployment mode. 

    - First, Amazon RDS takes a snapshot of the primary DB instance from your deployment and 
    - then restores the snapshot into another Availability Zone. 
    - Amazon RDS then sets up synchronous replication between your primary DB instance and the new instance.

AWS CloudTrail: You can view a record of actions that are taken by a user, a role, or an AWS service in Amazon RDS. CloudTrail captures all API calls for Amazon RDS as events.


RDS Purchasing options 


`On-Demand Instances:` Pay by the hour for the DB instance hours that you use. Pricing is listed on a per-hour basis, but bills are calculated to the second and they show times in decimal form. Amazon RDS usage is now billed in 1-second increments, with a minimum of 10 minutes.

`Reserved Instances:` Reserve a DB instance for a 1-year or 3-year term and get a significant discount compared to the on-demand DB instance pricing. With Reserved Instance usage, you can launch, delete, start, or stop multiple instances within an hour and get the Reserved Instance benefit for all instances.

`Billig` 

DB instance hours (per hour): Based on the DB instance class of the DB instance (for example, db.t2.small or db.m4.large). Pricing is listed on a per-hour basis, but bills are calculated to the second and they show times in decimal form. Amazon RDS usage is billed in 1-second increments, with a minimum of 10 minutes.
Storage (per GB per month): Storage capacity that you have provisioned to your DB instance. If you scale your provisioned storage capacity within the month, your bill is prorated. 
I/O requests (per 1 million requests per month): Total number of storage I/O requests that you have made in a billing cycle, for Amazon RDS magnetic storage only.
Provisioned IOPS (per IOPS per month): Provisioned IOPS rate, regardless of IOPS consumed, for Amazon RDS Provisioned IOPS (SSD) storage only. Provisioned storage for EBS volumes is billed in 1-second increments, with a minimum of 10 minutes.
Backup storage (per GB per month): Backup storage is the storage that is associated with automated database backups and any active database snapshots that you have taken. Increasing your backup retention period or taking additional database snapshots increases the backup storage that your database consumes. Per-second billing doesn't apply to backup storage (metered in GB per month).
Data transfer (per GB): Data transfer in and out of your DB instance from or to the internet and other Regions.

## Amazon Aurora 

Amazon Aurora is a MySQL and PostgreSQL-compatible relational database that takes advantage of the strengths of the cloud.

Cookies are in client side, and session are in the server side. 

Client side (client side web browser)
Server side(web server and reverse proxy cache)

Caching in AWS(user -> internet/edge->web->app->database)
Amzon CloudFront -- AWS content delivery network 

    both for static and dynamic content 
    support websocket protocol()

Add session to the database so that you don't have to pay for read request(reduce cost)

## High Availability 

Saying that a system is available means that you can access the services or applications that this system provides. Uptime refers to the time when services are available. In contrast, downtime refers to a time when you can't access services.

Availability refers to the percentage of time that a system is available.

High availability: A measure of the time when your services are available for use.
With high availability, you might have downtime and data loss, but this loss is kept to a minimum.

Some metrics can be used to define the risk that you agree to take in terms of the amount of data that is lost. The `recovery point objective` (RPO) is the maximum acceptable amount of time since the last data recovery point. The RPO determines what is considered an acceptable loss of data between the last recovery point and the interruption of service. The `recovery time objective` (RTO) is the maximum acceptable delay between the interruption of service and restoration of service. The RTO determines what is considered an acceptable time window when service is unavailable.   

`Fault tolerance:` The ability for a system to remain in operation even if some of the components that were used to build the system fail. Fault tolerance does not take into account downtime or data loss.

`Scalability:` The ability of an application to accommodate growth without changing design.

`Elasticity:` The degree to which a system is able to adapt to workload changes by provisioning (or terminating) resources.


To be `highly available`, an architecture must be able to scale (vertically or horizontally) according to the demand.

To meet these requirements, you must implement a reactive system that is `elastic`, `resilient`, `responsive`, and `message` driven. A well-designed reactive architecture can save you money and provide a better experience for your users.

Cloud Architectural Principles 

`Design for failure:` using of application load balancer perform a health check the instances are working properly 
`Embrace elasticity` and automate: When building an architecture, you cannot assume that every component in the architecture will stay healthy. A common cause of failure in on-premises workloads is resource saturation, or when the demands that are placed on a workload exceed the capacity of that workload. Use cloud watch to monitor deman and workload utiliztioan. instead of overprovisioning or underprovisioning. Example `Auto scaling group`. 
`Loosely couple`; To achieve this loose coupling, the microservices in a system must communicate with each other. Separating processes into different pieces that are connected by messages in queues creates clear transaction boundaries and allows services to operate more independently. 
`Become stateless`: Being stateless has an advantage. If the server goes down and the traffic must be redirected to another EC2 instance, no interruption of the service will occur.
`Use parallelism`: With parallel configuration, the work would be completed more quickly and efficiently while maintaining the ability to manage and scale to capacity.
`Use appropriate storage options`

        Frequency of access (online, offline, archival)
        Frequency of update (write once ready many, dynamic)
        Availability and durability constrains

`Build security into every layer`: Security is key, and you should apply it everywhere in your architecture. 

    Encrypting it or by protecting the access to it. 
    Principle of least privilage.
    For example, you can prevent unplanned termination of your EC2 instances or restrict access to S3 buckets. 



Improving the architecture



Increasing redundancy:
Making the application ready for large traffic increases: Autoscaling group using cloudwatch metrics.
Amazon RDS read replicas. This technique helps to manage read-heavy workloads.

Disaster Recovery: They range from the low cost and low complexity of making backups to more complex strategies that use multiple active Regions:

Backup and restore: This approach is suitable for mitigating against data loss or corruption.
Pilot light:
Warm standby:
Multi-site:

![Graphic comparision](https://awsacademy.contentcontroller.com/vault/0c89efbe-dd11-4b33-b081-ca05f3169b9b/courses/5811ffc7-73d2-4c98-8b27-1fb41681183e/0/scormcontent/assets/BZ_zxbCf34iH18gp_1d1yF5-QlVcKGPOa.png)

Other features deliver scalability, service persistence, or failover when failures occur. Monitoring and alerting features also contribute to availability goals by enabling automation for enhancing overall availability.

![highly available apps](https://file%2B.vscode-resource.vscode-cdn.net/Users/gmekuriy/Desktop/Screen%20Shot%202022-08-11%20at%208.21.09%20PM.png?version%3D1660267303544)

![RDS](https://awsacademy.contentcontroller.com/vault/0c89efbe-dd11-4b33-b081-ca05f3169b9b/courses/5811ffc7-73d2-4c98-8b27-1fb41681183e/0/scormcontent/assets/TIzCQOkhggwiJiVE_kRI116vNDCqiLa9r.png)


RDS vs self-manage database

Self-managed databases offer the flexibility of using a database engine of your choosing. However, they also bring the responsibility of `performing backup`s and `managing patching`, `security`, and `performance` tuning. Fully managed databases from Amazon RDS manage these activities for you, and they provide additional scalability and availability options.

`Production environments `are the environments that host the real time, mission-critical business applications that deliver key business capabilities. 

Using Amazon CloudFront, you can  cache that content for faster retrieval by application users. 

Including Amazon Route 53, the highly available and scalable Domain Name System (DNS), provides additional performance efficiency. It manages traffic that comes into and out of the application by enabling geospecific delivery of cached content.

For example, a `retail website `might show every visitor the five top-selling products for that day. Caching this list of products prevents repeatedly querying the inventory database, which includes millions of products, for this information.

## Reliability 

Recover from infrastructure or service disruptions
Dynamically acquire computing resources to meet demand
Mitigate disruptions, which might include misconfigurations or transient network issues

Key Services for reliability 

![Services](https://awsacademy.contentcontroller.com/vault/fafb308d-01bc-460c-be67-3cec033742b9/courses/bfd9d720-ba22-4903-af8b-d449700ac939/0/scormcontent/assets/eTQO0gTxiAOltV1y_Zrz2dmzX19tnDQ8z.png)

### Foundational services

IAM: You can use IAM to securely control access to AWS services and resources. Limiting access to resources improves reliability by allowing only authorized users to create, modify, or remove services used in the application environment.

VPC: VPCs improve reliability by separating application resources into their own virtual network. You can use network access control lists (network ACLs) and security groups to control access to those resources.

Trusted Advisor: This service provides visibility and recommendations related to fault tolerance and services limits. 

AWS Shield: Managed service provides distributed denial of service (DDoS) protection.

    Shield Standard defends against the most common, frequently occurring network and transport layer DDoS attacks.

### `Change Management Services:`

AWS cloudTrail: This service records AWS application programming interface (API) calls into log files for your account. These log files improve reliability by providing a record of when, where, how, and by whom configuration changes are made in the application environment.

CoudWatch: This service provides you with data and actionable insights to monitor your applications, respond to system-wide performance changes, and optimize resource utilization.

Config: This service records details of changes to your AWS resources to provide you with a configuration history. This configuration history improves reliability because you can to obtain details of what a resource’s configuration looked like at any point in the past and to restore that configuration if a change has caused unexpected results.

Auto scaling: AWS Auto Scaling capabilities provide automated demand management for a deployed workload.


### `Failure management services `

AWS CloudFormation: This service provides a template-based mechanism for deploying AWS resources. This mechanism improves reliability by provisioning resources in an orderly and predictable fashion.

Amazon Simple Storage Service (Amazon S3) and Amazon Simple Storage Service Glacier: These services improve reliability by providing a highly durable location for storing backups of application data and code.

AWS Key Management Service (AWS KMS): This service provides a reliable management system for security encryption keys that integrates with many AWS services.


Reliability design principles

1. Automatically recover from failure

2. Test recovery procedures: This principle is the process of planning for the worst case, such as a serious system, service, or component failure.

3. Scale horizontally to increase aggregate workload availability

4. Stop guessing capacity

5. Manage change in automation

## Three Tier application 
The infrastructure you use to deploy a modern application often consists of a web tier to deliver the application content to the user, an application tier to perform the business logic functions of the application, and a database tier to store application data. Additionally, related infrastructure often exists to provide connectivity, security controls, and monitoring capabilities for the application.

CloudFormation: 

CloudFormation uses templates that describe all the AWS resources that you want, such as Amazon Elastic Compute Cloud (Amazon EC2) instances or Amazon Relational Database Service (Amazon RDS) database (DB) instances. Then, CloudFormation takes care of provisioning and configuring those resources for you. You can use CloudFormation to simplify infrastructure management, to quickly replicate your infrastructure, or to control and track changes that you make to your infrastructure.

3 Tier app

Presentation Layer(Frontend)

    Like the cloth and add to the cart 

Application Layer(bakend)

    Business logics you might have, the payment instructions and all that 
    the addresses so that you can use it for recommendatioin for new users 
    the login info and saving those saved items in the cart 

Database 

    storing those data and quriying 
    

    Remove the cloud benefit 
    no cost 
    Generalize the cost to avoid some of the questions 
    better graphics for shared responsibility model


    Amazon Relational Database Service (Amazon RDS) is a web service that makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while managing time-consuming database administration tasks, freeing you up to focus on your applications and business.

    Amazon RDS gives you access to the capabilities of a familiar MySQL, MariaDB, PostgreSQL, Oracle, Microsoft SQL Server, or Aurora database engine.
    Amazon RDS will make sure that the relational database software powering your deployment stays up-to-date with the latest patches.
    Turned on by default, the automated backup feature of Amazon RDS enables point-in-time recovery for your DB Instance.
    DB Snapshots: DB Snapshots are user-initiated backups of your DB Instance. 
    IOPS: Starting immediately, when you create new DB Instances using the AWS Management Console or the Amazon RDS APIs, you can provision from 1,000 IOPS to 10,000 IOPS with corresponding storage from 100GB to 1TB for MySQL and Oracle engines. You can start small and scale up in increments of 1,000 IOPS and 100GB of storage. If you are using SQL Server then the maximum IOPS you can provision is 7,000 IOPS.
    Automatic Host Replacement: Amazon RDS will automatically replace the compute instance powering your deployment in the event of a hardware failure.
    Isolation and Security: Using Amazon VPC, you can isolate your DB Instances in your own virtual network, and connect to your existing IT infrastructure using industry-standard encrypted IPsec VPN.


Presentation Session:
Stand/sit up right and relax
Relate to customers and actively listen 
Have a customer success story 
Understand your weakness for example your filler words 


Research and value mapping 
Invest time - set up pre-meetings/talk to staeholders(actively listen)

Who are the people? 

Delivery for POC2

    1, 5, 2, 7, 12, 6(ours), 15, 14, 9, 11, 8, 13, 4, 10, 3 



Web tier: Small burstable instance for front end (HTML, CSS, in browser javascript) maybe root volume 
App tier:  to interact with frontend and database (Elastic Block store)
Nat gateway for for outbound request. For patches and stuff 


#!/bin/bash
yum update -y 
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service 
echo "Hello there from $(hostname -f)" > /var/www/html/index.html


### Security at AWS

Security is the practice of protecting your intellectual property from unauthorized access, use, or modification.

Confidentiality: allow only authorized users to access to resources 
Integrity: Preserving data at rest and in trasit. Can we proof it's the original data. The accuracy and consistency or data over its enitre lifecycle. 
Avaialability: having access to information resources when needed

AWS `Config`: The visibility of data(what has changed, where is the evidence, what is in my environment, what impact did a particular action have)
AWS `CloudTrail`: Auditability(who, what, when, where). It's on by default. 
AWS `IAM`: Controllability(effectively manage users, temporary credentials)
AWS `CloudFormation`: Automation and Agility(ensuring high availability, can I apply securiyt checks ina reproducible manner)


AWS Shared Responsiblity Model

Security of the cloud: infrastracture security, compute storage, networking, Database, Avialability, Regions, Edge Locatoins 
Security in the cloud:SSE, CSE, Network Traffic Protection, OS network and firewall configuration. 

`AWS Cloud adoption framwork security perspective `

Directive 
    what are your security requirements(HIPPA compliance)
Detective 
    Looks for bad things happening anyway
Preventive 
    Stop bad things from happening(strong audit, authentication...)
Responsive 
    Fix or alert on bad things detected(intrusion)

Forensic Subnet(for analysis for any problem: Not trafic in no trafic out)

Common incidents

    Compromized user credentials
    Insufficient data integrity 
    Overly permissibe access 

ad hoc() one time analysis



What is DevOps?
    Continous Integration and Continous Delivery 
 
    A continous delivery model that is repeatable, reliable, stable, resilient, and secure, while improving operatinal efficiency. 

API calls are automatically signed when using AWS SDK, CLI, and the aws management console. 

Root access: unresticted access to AWS cloud 
IAM User: Restricted access to aws cloud  

POC3: Deliverable 

Scores for recommendations(practices into and descriptions)
Reports of the informations that's provided by the inspector???


The resource types that you can protect by using AWS WAF web ACLs are Amazon CloudFront distributions, Amazon API Gateway APIs, and Application Load Balancers. 

## Database 
Data is any bit of information that a system is accessing, using, or generating. To function, applications need a place where data from users, devices, and applications can be stored and from where it can be made available. Databases are the backend systems that provide or store data for applications of all types. These types of applications range from small mobile apps to enterprise applications that operate at internet scale. 

Types of applications that databases serve

Internet-scale applications 
Real-time application
Open-source applications 
Enterprise applications

Database types

Relational: Relational databases store data in tables with predefined schemas and relationships between them.

Key-value databases are nonrelational databases that store data as a collection of key-value pairs, in which a key serves as a unique identifier. 
Useful for: High-traffic web applications, ecommerce systems, and gaming applications

In-memory databases are used for applications that require real-time access to data.
Useful for: Caching, user session management, gaming leaderboards, and geospatial applications

A document database is designed to store semistructured data as JavaScript Object Notation (JSON)-like documents.
Useful for: Content management, catalogs, and user profiles

One-size fits all 

Large volume, broad variety, and rapid velocity define big data.
Big data can be described as data management challenges that—due to increasing volume, velocity, and variety of data—that organizations cannot solve by using traditional databases. Most definitions of big data include the concept of what is commonly known as the three Vs of big data

Volume: Big data typically ranges from terabytes to petabytes of data in size.
Variety: Big data includes a wide range of sources and formats (for example, web logs, social media interactions, and online ecommerce transactions).
Velocity: Big data often has specific requirements regarding the time between when data generation occurs and when actionable insights based on that data are delivered to users. Therefore, data must be collected, stored, processed, and analyzed within relatively short windows, which range from daily to real time.

AWS big data 

AWS provides a broad and fully integrated portfolio of cloud computing services to help an organization build, secure, and deploy all their big data applications. With AWS, organizations have no hardware to procure and no infrastructure to maintain and scale. Thus, organizations can instead focus internal resources on uncovering new insights from their data. Because AWS is constantly adding new capabilities and features, AWS customers are always able to use the latest technologies without making long-term investment commitments. Managing big data on AWS has several advantages, including immediate availability, ability to handle massive and changing workloads, strict security, and a strong partner community.