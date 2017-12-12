![An Open Guide](figures/signpost-horiz1-1600.jpg)

The Open Guide to Amazon Web Services
=====================================

[![Slack Chat](https://img.shields.io/badge/Chat-Slack-ff69b4.svg "Join us. Anyone is welcome!")](https://og-aws-slack.lexikon.io/) ⇦ Join us!

[Credits](AUTHORS.md) ∙ [Contributing guidelines](CONTRIBUTING.md)

Table of Contents
-----------------

**Purpose**

-	[Why an Open Guide?](#why-an-open-guide)
-	[Scope](#scope)
-	[Legend](#legend)

**AWS in General**

-	[General Information](#general-information)
-	[Learning and Career Development](#learning-and-career-development)
-	[Managing AWS](#managing-aws)
-	[Managing Servers and Applications](#managing-servers-and-applications)

| Specific AWS Services                 | Basics                         | Tips                          | Gotchas                                        |
|---------------------------------------|--------------------------------|-------------------------------|------------------------------------------------|
| [Security and IAM](#security-and-iam) | [📗](#security-and-iam-basics) | [📘](#security-and-iam-tips) | [📙](#security-and-iam-gotchas-and-limitations) |
| [S3](#s3) | [📗](#s3-basics) | [📘](#s3-tips) | [📙](#s3-gotchas-and-limitations) |
| [EC2](#ec2) | [📗](#ec2-basics) | [📘](#ec2-tips) | [📙](#ec2-gotchas-and-limitations) |
| [CloudWatch](#cloudwatch) | [📗](#cloudwatch-basics) | [📘](#cloudwatch-tips) | [📙](#cloudwatch-gotchas-and-limitations) |
| [AMIs](#amis) | [📗](#ami-basics) | [📘](#ami-tips) | [📙](#ami-gotchas-and-limitations) |
| [Auto Scaling](#auto-scaling) | [📗](#auto-scaling-basics) | [📘](#auto-scaling-tips) | [📙](#auto-scaling-gotchas-and-limitations) |
| [EBS](#ebs) | [📗](#ebs-basics) | [📘](#ebs-tips) | [📙](#ebs-gotchas-and-limitations) |
| [EFS](#efs) | [📗](#efs-basics) | [📘](#efs-tips) | [📙](#efs-gotchas-and-limitations) |
| [Load Balancers](#load-balancers) | [📗](#load-balancer-basics) | [📘](#load-balancer-tips) | [📙](#load-balancer-gotchas-and-limitations) |
| [CLB (ELB)](#clb) | [📗](#clb-basics) | [📘](#clb-tips) | [📙](#clb-gotchas-and-limitations) |
| [ALB](#alb) | [📗](#alb-basics) | [📘](#alb-tips) | [📙](#alb-gotchas-and-limitations) |
| [Elastic IPs](#elastic-ips) | [📗](#elastic-ip-basics) | [📘](#elastic-ip-tips) | [📙](#elastic-ip-gotchas-and-limitations) |
| [Glacier](#glacier) | [📗](#glacier-basics) | [📘](#glacier-tips) | [📙](#glacier-gotchas-and-limitations) |
| [RDS](#rds) | [📗](#rds-basics) | [📘](#rds-tips) | [📙](#rds-gotchas-and-limitations) |
| [RDS MySQL and MariaDB](#rds-mysql-and-mariadb) | [📗](#rds-mysql-and-mariadb-basics) | [📘](#rds-mysql-and-mariadb-tips) | [📙](#rds-mysql-and-mariadb-gotchas-and-limitations) |
| [RDS Aurora](#rds-aurora) | [📗](#rds-aurora-basics) | [📘](#rds-aurora-tips) | [📙](#rds-aurora-gotchas-and-limitations) |
| [RDS SQL Server](#rds-sql-server) | [📗](#rds-sql-server-basics) | [📘](#rds-sql-server-tips) | [📙](#rds-sql-server-gotchas-and-limitations) |
| [DynamoDB](#dynamodb) | [📗](#dynamodb-basics) | [📘](#dynamodb-tips) | [📙](#dynamodb-gotchas-and-limitations) |
| [ElastiCache](#elasticache) | [📗](#elasticache-basics) | [📘](#elasticache-tips) | [📙](#elasticache-gotchas-and-limitations) |
| [ECS](#ecs) | [📗](#ecs-basics) | [📘](#ecs-tips) |  |
| [Lambda](#lambda) | [📗](#lambda-basics) | [📘](#lambda-tips) | [📙](#lambda-gotchas-and-limitations) |
| [API Gateway](#api-gateway) | [📗](#api-gateway-basics) | [📘](#api-gateway-tips) | [📙](#api-gateway-gotchas-and-limitations) |
| [Route 53](#route-53) | [📗](#route-53-basics) | [📘](#route-53-tips) |  |
| [CloudFormation](#cloudformation) | [📗](#cloudformation-basics) | [📘](#cloudformation-tips) | [📙](#cloudformation-gotchas-and-limitations) |
| [VPCs, Network Security, and Security Groups](#vpcs-network-security-and-security-groups) | [📗](#vpc-basics) | [📘](#vpc-and-network-security-tips) | [📙](#vpc-and-network-security-gotchas-and-limitations) |
| [KMS](#kms) | [📗](#kms-basics) | [📘](#kms-tips) |  |
| [CloudFront](#cloudfront) | [📗](#cloudfront-basics) | [📘](#cloudfront-tips) | [📙](#cloudfront-gotchas-and-limitations) |
| [DirectConnect](#directconnect) | [📗](#directconnect-basics) | [📘](#directconnect-tips) |  |
| [Redshift](#redshift) | [📗](#redshift-basics) | [📘](#redshift-tips) | [📙](#redshift-gotchas-and-limitations) |
| [EMR](#emr) | [📗](#emr-basics) | [📘](#emr-tips) | [📙](#emr-gotchas-and-limitations) |
| [Kinesis Streams](#kinesis-streams) | [📗](#kinesis-streams-basics) | [📘](#kinesis-streams-tips) | [📙](#kinesis-streams-gotchas-and-limitations) |
| [Kinesis Firehose](#kinesis-firehose) |  |  | [📙](#kinesis-firehose-gotchas-and-limitations) |
| [Device Farm](#device-farm) | [📗](#device-farm-basics) | [📘](#device-farm-tips) | [📙](#device-farm-gotchas-and-limitations) |
| [IoT](#iot) | [📗](#iot-basics) | [📘](#iot-tips) | [📙](#iot-gotchas-and-limitations) |
| [SES](#ses) | [📗](#ses-basics) | [📘](#ses-tips) | [📙](#ses-gotchas-and-limitations) |
| [Certificate Manager](#certificate-manager) | [📗](#certificate-manager-basics) | [📘](#certificate-manager-tips) | [📙](#certificate-manager-gotchas-and-limitations) |
| [WAF](#waf) | [📗](#waf-basics) | [📘](#waf-tips) | [📙](#waf-gotchas-and-limitations) |
| [OpsWorks](#opsworks) | [📗](#opsworks-basics) | [📘](#opsworks-tips) | [📙](#opsworks-gotchas-and-limitations) |
| [Batch](#batch) | [📗](#batch-basics) | [📘](#batch-tips) |
| [SQS](#sqs) | [📗](#sqs-basics) | [📘](#sqs-tips) | [📙](#sqs-gotchas-and-limitations) |
| [SNS](#sns) | [📗](#sns-basics) | [📘](#sns-tips) | [📙](#sns-gotchas-and-limitations) |

**Special Topics**

-	[High Availability](#high-availability)
-	[Billing and Cost Management](#billing-and-cost-management)
-	[Further Reading](#further-reading)

**Legal**

-	[Disclaimer](#disclaimer)
-	[License](#license)

**Figures and Tables**

[![Tools and Services Market Landscape](figures/aws-market-landscape-320px.png)](#tools-and-services-market-landscape) [![AWS Data Transfer Costs](figures/aws-data-transfer-costs-320px.png)](#aws-data-transfer-costs)

-	[Figure: Tools and Services Market Landscape](#tools-and-services-market-landscape): A selection of third-party companies/products
-	[Figure: AWS Data Transfer Costs](#aws-data-transfer-costs): Visual overview of data transfer costs
-	[Table: Service Matrix](#service-matrix): How AWS services compare to alternatives
-	[Table: AWS Product Maturity and Releases](#aws-product-maturity-and-releases): AWS product releases
-	[Table: Storage Durability, Availability, and Price](#storage-durability-availability-and-price): A quantitative comparison

Why an Open Guide?
------------------

A lot of information on AWS is already written. Most people learn AWS by reading a blog or a “[getting started guide](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html)” and referring to the [standard AWS references](https://aws.amazon.com/documentation/). Nonetheless, trustworthy and practical information and recommendations aren’t easy to come by. AWS’s own documentation is a great but sprawling resource few have time to read fully, and it doesn’t include anything but official facts, so omits experiences of engineers. The information in blogs or [Stack Overflow](http://stackoverflow.com/questions/tagged/amazon-web-services) is also not consistently up to date.

This guide is by and for engineers who use AWS. It aims to be a useful, living reference that consolidates links, tips, gotchas, and best practices. It arose from discussion and editing over beers by [several engineers](AUTHORS.md) who have used AWS extensively.

Before using the guide, please read the [**license**](#license) and [**disclaimer**](#disclaimer).

### Please help!

**This is an early in-progress draft!** It’s our first attempt at assembling this information, so is far from comprehensive still, and likely to have omissions or errors.

[![Slack Chat](https://img.shields.io/badge/Chat-Slack-ff69b4.svg "Join us. Anyone is welcome!")](https://og-aws-slack.lexikon.io/)

Please help by [**joining the Slack channel**](https://og-aws-slack.lexikon.io/) (we like to talk about AWS in general, even if you only have questions — discussion helps the community and guides improvements) and [**contributing to the guide**](CONTRIBUTING.md). This guide is *open to contributions*, so unlike a blog, it can keep improving. Like any open source effort, we combine efforts but also review to ensure high quality.

Scope
-----

-	Currently, this guide covers selected “core” services, such as EC2, S3, Load Balancers, EBS, and IAM, and partial details and tips around other services. We expect it to expand.
-	It is not a tutorial, but rather a collection of information you can read and return to. It is for both beginners and the experienced.
-	The goal of this guide is to be:
	-	**Brief:** Keep it dense and use links
	-	**Practical:** Basic facts, concrete details, advice, gotchas, and other “folk knowledge”
	-	**Current:** We can keep updating it, and anyone can contribute improvements
	-	**Thoughtful:** The goal is to be helpful rather than present dry facts. Thoughtful opinion with rationale is welcome. Suggestions, notes, and opinions based on real experience can be extremely valuable. (We believe this is both possible with a guide of this format, unlike in some [other venues](http://meta.stackexchange.com/questions/201994/is-there-a-place-to-ask-opinion-based-questions).)
-	This guide is not sponsored by AWS or AWS-affiliated vendors. It is written by and for engineers who use AWS.

Legend
------

-	📒 Marks standard/official AWS pages and docs
-	🔹 Important or often overlooked tip
-	❗ “Serious” gotcha (used where risks or time or resource costs are significant: critical security risks, mistakes with significant financial cost, or poor architectural choices that are fundamentally difficult to correct)
-	🔸 “Regular” gotcha, limitation, or quirk (used where consequences are things not working, breaking, or not scaling gracefully)
-	📜 Undocumented feature (folklore)
-	🐥 Relatively new (and perhaps immature) services or features
-	⏱ Performance discussions
-	⛓ Lock-in: Products or decisions that are likely to tie you to AWS in a new or significant way — that is, later moving to a non-AWS alternative would be costly in terms of engineering effort
-	🚪 Alternative non-AWS options
-	💸 Cost issues, discussion, and gotchas
-	🕍 A mild warning attached to “full solution” or opinionated frameworks that may take significant time to understand and/or might not fit your needs exactly; the opposite of a point solution (the cathedral is a nod to [Raymond’s metaphor](https://en.wikipedia.org/wiki/The_Cathedral_and_the_Bazaar)\)
-	📗📘📙 Colors indicate basics, tips, and gotchas, respectively.
-	🚧 Areas where correction or improvement are needed (possibly with link to an issue — do help!)

General Information
-------------------

### When to Use AWS

-	[AWS](https://en.wikipedia.org/wiki/Amazon_Web_Services) is the dominant public cloud computing provider.
	-	In general, “[cloud computing](https://en.wikipedia.org/wiki/Cloud_computing)” can refer to one of three types of cloud: “public,” “private,” and “hybrid.” AWS is a public cloud provider, since anyone can use it. Private clouds are within a single (usually large) organization. Many companies use a hybrid of private and public clouds.
	-	The core features of AWS are [infrastructure-as-a-service](https://en.wikipedia.org/wiki/Cloud_computing#Infrastructure_as_a_service_.28IaaS.29) (IaaS) — that is, virtual machines and supporting infrastructure. Other cloud service models include [platform-as-a-service](https://en.wikipedia.org/wiki/Cloud_computing#Platform_as_a_service_.28PaaS.29) (PaaS), which typically are more fully managed services that deploy customers’ applications, or [software-as-a-service](https://en.wikipedia.org/wiki/Cloud_computing#Software_as_a_service_.28SaaS.29) (SaaS), which are cloud-based applications. AWS does offer a few products that fit into these other models, too.
	-	In business terms, with infrastructure-as-a-service you have a variable cost model — it is [OpEx, not CapEx](http://www.investopedia.com/ask/answers/020915/what-difference-between-capex-and-opex.asp) (though some [pre-purchased contracts](https://aws.amazon.com/ec2/purchasing-options/reserved-instances/) are still CapEx).
-	AWS’s annual revenue was [**$12.21 billion**](http://services.corporate-ir.net/SEC.Enhanced/SecCapsule.aspx?c=97664&fid=14806946) as of 2016 according to their SEC 10-K filing, or roughly **8.9%** of Amazon.com’s total 2016 revenue.
-	**Main reasons to use AWS:**
	-	If your company is building systems or products that may need to scale
	-	and you have technical know-how
	-	and you want the most flexible tools
	-	and you’re not significantly tied into different infrastructure already
	-	and you don’t have internal, regulatory, or compliance reasons you can’t use a public cloud-based solution
	-	and you’re not on a Microsoft-first tech stack
	-	and you don’t have a specific reason to use Google Cloud
	-	and you can afford, manage, or negotiate its somewhat higher costs
	-	... then AWS is likely a good option for your company.
-	Each of those reasons above might point to situations where other services are preferable. In practice, many, if not most, tech startups as well as a number of modern large companies can or already do benefit from using AWS. Many large enterprises are partly migrating internal infrastructure to Azure, Google Cloud, and AWS.
-	**Costs:** Billing and cost management are such big topics that we have [an entire section on this](#billing-and-cost-management).
-	🔹**EC2 vs. other services:** Most users of AWS are most familiar with [EC2](#ec2), AWS’ flagship virtual server product, and possibly a few others like S3 and CLBs. But AWS products now extend far beyond basic IaaS, and often companies do not properly understand or appreciate all the many AWS services and how they can be applied, due to the [sharply growing](#which-services-to-use) number of services, their novelty and complexity, branding confusion, and fear of ⛓lock-in to proprietary AWS technology. Although a bit daunting, it’s important for technical decision-makers in companies to understand the breadth of the AWS services and make informed decisions. (We hope this guide will help.)
-	🚪**AWS vs. other cloud providers:** While AWS is the dominant IaaS provider (31% market share in [this 2016 estimate](https://www.srgresearch.com/articles/aws-remains-dominant-despite-microsoft-and-google-growth-surges)), there is significant competition and alternatives that are better suited to some companies. [This Gartner report](https://www.gartner.com/doc/reprints?id=1-2G2O5FC&ct=150519&st=sb) has a good overview of the major cloud players :
	-	[**Google Cloud Platform**](https://cloud.google.com/). GCP arrived later to market than AWS, but has vast resources and is now used widely by many companies, including a few large ones. It is gaining market share. Not all AWS services have similar or analogous services in GCP. And vice versa: In particular, GCP offers some more advanced machine learning-based services like the [Vision](https://cloud.google.com/vision/), [Speech](https://cloud.google.com/speech/), and [Natural Language](https://cloud.google.com/natural-language/) APIs. It’s not common to switch once you’re up and running, but it does happen: [Spotify migrated](http://www.wsj.com/articles/google-cloud-lures-amazon-web-services-customer-spotify-1456270951) from AWS to Google Cloud. There is more discussion [on Quora](https://www.quora.com/What-are-the-reasons-to-choose-AWS-over-Google-Cloud-or-vice-versa-for-a-high-traffic-web-application) about relative benefits. Of particular note is that VPCs in GCP are [global by default](https://cloud.google.com/vpc/) with subnetworks per region, while AWS’ VPCs have to live within a particular region. This gives GCP an edge if you’re designing applications with geo-replication from the beginning. It’s also possible to [share one GCP VPC](https://cloud.google.com/compute/docs/shared-vpc/) between multiple projects (roughly analogous to AWS accounts), while in AWS you’d have to peer them. It’s also possible to [peer GCP VPCs](https://cloud.google.com/compute/docs/vpc/vpc-peering) in a similar manner to how it’s done in AWS.
	-	[**Microsoft Azure**](https://azure.microsoft.com/en) is the de facto choice for companies and teams that are focused on a Microsoft stack, and it has now placed significant emphasis on Linux as well
	-	In **China**, AWS’ footprint is relatively small. The market is dominated by Alibaba’s [Aliyun](https://intl.aliyun.com/).
	-	Companies at (very) large scale may want to reduce costs by managing their own infrastructure. For example, [Dropbox migrated](https://news.ycombinator.com/item?id=11282948) to their own infrastructure.
	-	Other cloud providers such as [Digital Ocean](https://www.digitalocean.com/) offer similar services, sometimes with greater ease of use, more personalized support, or lower cost. However, none of these match the breadth of products, mind-share, and market domination AWS now enjoys.
	-	Traditional managed hosting providers such as [Rackspace](https://www.rackspace.com/) offer cloud solutions as well.
-	🚪**AWS vs. PaaS:** If your goal is just to put up a single service that does something relatively simple, and you’re trying to minimize time managing operations engineering, consider a [platform-as-a-service](https://en.wikipedia.org/wiki/Platform_as_a_service) such as [Heroku](https://www.heroku.com/). The AWS approach to PaaS, Elastic Beanstalk, is arguably more complex, especially for simple use cases.
-	🚪**AWS vs. web hosting:** If your main goal is to host a website or blog, and you don’t expect to be building an app or more complex service, you may wish consider one of the myriad [web hosting services](https://www.google.com/search?q=web+hosting).
-	🚪**AWS vs. managed hosting:** Traditionally, many companies pay [managed hosting](https://en.wikipedia.org/wiki/Dedicated_hosting_service) providers to maintain physical servers for them, then build and deploy their software on top of the rented hardware. This makes sense for businesses who want direct control over hardware, due to legacy, performance, or special compliance constraints, but is usually considered old fashioned or unnecessary by many developer-centric startups and younger tech companies.
-	**Complexity:** AWS will let you build and scale systems to the size of the largest companies, but the complexity of the services when used at scale requires significant depth of knowledge and experience. Even very simple use cases often require more knowledge to do “right” in AWS than in a simpler environment like Heroku or Digital Ocean. (This guide may help!)
-	**Geographic locations:** AWS has data centers in [over a dozen geographic locations](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions), known as **regions**, in Europe, East Asia, North and South America, and now Australia and India. It also has many more **edge locations** globally for reduced latency of services like CloudFront.
	-	See the [current list](https://aws.amazon.com/about-aws/global-infrastructure/) of regions and edge locations, including upcoming ones.
	-	If your infrastructure needs to be in close physical proximity to another service for latency or throughput reasons (for example, latency to an ad exchange), viability of AWS may depend on the location.
-	⛓**Lock-in:** As you use AWS, it’s important to be aware when you are depending on AWS services that do not have equivalents elsewhere.
	-	Lock-in may be completely fine for your company, or a significant risk. It’s important from a business perspective to make this choice explicitly, and consider the cost, operational, business continuity, and competitive risks of being tied to AWS. AWS is such a dominant and reliable vendor, many companies are comfortable with using AWS to its full extent. Others can tell stories about the [dangers of “cloud jail” when costs spiral](http://firstround.com/review/the-three-infrastructure-mistakes-your-company-must-not-make/).
	-	Generally, the more AWS services you use, the more lock-in you have to AWS — that is, the more engineering resources (time and money) it will take to change to other providers in the future.
	-	Basic services like virtual servers and standard databases are usually easy to migrate to other providers or on premises. Others like load balancers and IAM are specific to AWS but have close equivalents from other providers. The key thing to consider is whether engineers are architecting systems around specific AWS services that are not open source or relatively interchangeable. For example, Lambda, API Gateway, Kinesis, Redshift, and DynamoDB do not have substantially equivalent open source or commercial service equivalents, while EC2, RDS (MySQL or Postgres), EMR, and ElastiCache more or less do. (See more [below](#which-services-to-use), where these are noted with ⛓.)
-	**Combining AWS and other cloud providers:** Many customers combine AWS with other non-AWS services. For example, legacy systems or secure data might be in a managed hosting provider, while other systems are AWS. Or a company might only use S3 with another provider doing everything else. However small startups or projects starting fresh will typically stick to AWS or Google Cloud only.
-	**Hybrid cloud:** In larger enterprises, it is common to have [hybrid deployments](https://aws.amazon.com/enterprise/hybrid/) encompassing private cloud or on-premises servers and AWS — or other enterprise cloud providers like [IBM](https://www.ibm.com/cloud-computing/solutions/hybrid-cloud)/[Bluemix](http://www.ibm.com/cloud-computing/bluemix/hybrid/), [Microsoft](https://www.microsoft.com/en-us/cloud-platform/hybrid-cloud)/[Azure](https://azure.microsoft.com/en-us/overview/azure-stack/), [NetApp](http://www.netapp.com/us/solutions/cloud/hybrid-cloud/), or [EMC](http://www.emc.com/en-us/cloud/hybrid-cloud-computing/index.htm).
-	**Major customers:** Who uses AWS and Google Cloud?
	-	AWS’s [list of customers](https://aws.amazon.com/solutions/case-studies/) includes large numbers of mainstream online properties and major brands, such as Netflix, Pinterest, Spotify (moving to Google Cloud), Airbnb, Expedia, Yelp, Zynga, Comcast, Nokia, and Bristol-Myers Squibb.
        -	Azure’s [list of customers](https://azure.microsoft.com/en-us/case-studies/) includes companies such as NBC Universal, 3M and Honeywell Inc.
	-	Google Cloud’s [list of customers](https://cloud.google.com/customers/) is large as well, and includes a few mainstream sites, such as [Snapchat](http://www.businessinsider.com/snapchat-is-built-on-googles-cloud-2014-1), Best Buy, Domino’s, and Sony Music.

### Which Services to Use

-	AWS offers a *lot* of different services — [about a hundred](https://aws.amazon.com/products/) at last count.
-	Most customers use a few services heavily, a few services lightly, and the rest not at all. What services you’ll use depends on your use cases. Choices differ substantially from company to company.
-	**Immature and unpopular services:** Just because AWS has a service that sounds promising, it doesn’t mean you should use it. Some services are very narrow in use case, not mature, are overly opinionated, or have limitations, so building your own solution may be better. We try to give a sense for this by breaking products into categories.
-	**Must-know infrastructure:** Most typical small to medium-size users will focus on the following services first. If you manage use of AWS systems, you likely need to know at least a little about all of these. (Even if you don’t use them, you should learn enough to make that choice intelligently.)
	-	[IAM](#security-and-iam): User accounts and identities (you need to think about accounts early on!)
	-	[EC2](#ec2): Virtual servers and associated components, including:
		-	[AMIs](#amis): Machine Images
		-	[Load Balancers](#load-balancers): CLBs and ALBs
		-	[Autoscaling](#auto-scaling): Capacity scaling (adding and removing servers based on load)
		-	[EBS](#ebs): Network-attached disks
		-	[Elastic IPs](#elastic-ips): Assigned IP addresses
	-	[S3](#s3): Storage of files
	-	[Route 53](#route-53): DNS and domain registration
	-	[VPC](#vpcs-network-security-and-security-groups): Virtual networking, network security, and co-location; you automatically use
	-	[CloudFront](#cloudfront): CDN for hosting content
	-	[CloudWatch](#cloudwatch): Alerts, paging, monitoring
-	**Managed services:** Existing software solutions you could run on your own, but with managed deployment:
	-	[RDS](#rds): Managed relational databases (managed MySQL, Postgres, and Amazon’s own Aurora database)
	-	[EMR](#emr): Managed Hadoop
	-	[Elasticsearch](https://aws.amazon.com/elasticsearch-service/): Managed Elasticsearch
	-	[ElastiCache](https://aws.amazon.com/elasticache/): Managed Redis and Memcached
-	**Optional but important infrastructure:** These are key and useful infrastructure components that are less widely known and used. You may have legitimate reasons to prefer alternatives, so evaluate with care to be sure they fit your needs:
	-	⛓[Lambda](#lambda): Running small, fully managed tasks “serverless”
	-	[CloudTrail](https://aws.amazon.com/cloudtrail/): AWS API logging and audit (often neglected but important)
	-	⛓🕍[CloudFormation](#cloudformation): Templatized configuration of collections of AWS resources
	-	🕍[Elastic Beanstalk](https://aws.amazon.com/elasticbeanstalk/): Fully managed (PaaS) deployment of packaged Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker applications
	-	🐥[EFS](#efs): Network filesystem compatible with NFSv4.1
	-	⛓🕍[ECS](#ecs): Docker container/cluster management (note Docker can also be used directly, without ECS)
	-	⛓[ECR](https://aws.amazon.com/ecr/): Hosted private Docker registry
	-	🐥[Config](https://aws.amazon.com/config/): AWS configuration inventory, history, change notifications
	-	🐥[X-Ray](https://aws.amazon.com/xray/): Trace analysis and debugging for distributed applications such as microservices.
-	**Special-purpose infrastructure:** These services are focused on specific use cases and should be evaluated if they apply to your situation. Many also are proprietary architectures, so tend to tie you to AWS.
	-	⛓[DynamoDB](#dynamodb): Low-latency NoSQL key-value store
	-	⛓[Glacier](#glacier): Slow and cheap alternative to S3
	-	⛓[Kinesis](https://aws.amazon.com/kinesis/): Streaming (distributed log) service
	-	⛓[SQS](https://aws.amazon.com/sqs/): Message queueing service
	-	⛓[Redshift](#redshift): Data warehouse
	-	🐥[QuickSight](https://aws.amazon.com/quicksight/): Business intelligence service
	-	[SES](https://aws.amazon.com/ses/): Send and receive e-mail for marketing or transactions
	-	⛓[API Gateway](https://aws.amazon.com/api-gateway/): Proxy, manage, and secure API calls
	-	⛓[IoT](#iot): Manage bidirectional communication over HTTP, WebSockets, and MQTT between AWS and clients (often but not necessarily “things” like appliances or sensors)
	-	⛓[WAF](https://aws.amazon.com/waf/): Web firewall for CloudFront to deflect attacks
	-	⛓[KMS](#kms): Store and manage encryption keys securely
	-	[Inspector](https://aws.amazon.com/inspector/): Security audit
	-	[Trusted Advisor](https://aws.amazon.com/premiumsupport/trustedadvisor/): Automated tips on reducing cost or making improvements
	-	🐥[Certificate Manager](https://aws.amazon.com/certificate-manager/): Manage SSL/TLS certificates for AWS services
-	**Compound services:** These are similarly specific, but are full-blown services that tackle complex problems and may tie you in. Usefulness depends on your requirements. If you have large or significant need, you may have these already managed by in-house systems and engineering teams.
	-	[Machine Learning](https://aws.amazon.com/machine-learning/): Machine learning model training and classification
	-	[Lex](https://aws.amazon.com/lex/): Automatic speech recognition (ASR) and natural language understanding (NLU)
	-	[Polly](https://aws.amazon.com/polly/): Text-to-speech engine in the cloud
	-	[Rekognition](https://aws.amazon.com/rekognition/): Service for image recognition
	-	⛓🕍[Data Pipeline](https://aws.amazon.com/datapipeline/): Managed ETL service
	-	⛓🕍[SWF](https://aws.amazon.com/swf/): Managed state tracker for distributed polyglot job workflow
	-	⛓🕍[Lumberyard](https://aws.amazon.com/lumberyard/): 3D game engine
-	**Mobile/app development:**
	-	[SNS](https://aws.amazon.com/sns/): Manage app push notifications and other end-user notifications
	-	⛓🕍[Cognito](https://aws.amazon.com/cognito/): User authentication via Facebook, Twitter, etc.
	-	[Device Farm](https://aws.amazon.com/device-farm/): Cloud-based device testing
	-	[Mobile Analytics](https://aws.amazon.com/mobileanalytics/): Analytics solution for app usage
	-	🕍[Mobile Hub](https://aws.amazon.com/mobile/): Comprehensive, managed mobile app framework
-	**Enterprise services:** These are relevant if you have significant corporate cloud-based or hybrid needs. Many smaller companies and startups use other solutions, like Google Apps or Box. Larger companies may also have their own non-AWS IT solutions.
	-	[AppStream](https://aws.amazon.com/appstream/): Windows apps in the cloud, with access from many devices
	-	[Workspaces](https://aws.amazon.com/workspaces/): Windows desktop in the cloud, with access from many devices
	-	[WorkDocs](https://aws.amazon.com/workdocs/) (formerly Zocalo): Enterprise document sharing
	-	[WorkMail](https://aws.amazon.com/workmail/): Enterprise managed e-mail and calendaring service
	-	[Directory Service](https://aws.amazon.com/directoryservice/): Microsoft Active Directory in the cloud
	-	[Direct Connect](https://aws.amazon.com/directconnect/): Dedicated network connection between office or data center and AWS
	-	[Storage Gateway](https://aws.amazon.com/storagegateway/): Bridge between on-premises IT and cloud storage
	-	[Service Catalog](https://aws.amazon.com/servicecatalog/): IT service approval and compliance
-	**Probably-don't-need-to-know services:** Bottom line, our informal polling indicates these services are just not broadly used — and often for good reasons:
	-	[Snowball](https://aws.amazon.com/importexport/): If you want to ship petabytes of data into or out of Amazon using a physical appliance, read on.
	-	[Snowmobile](https://aws.amazon.com/snowmobile/): Appliances are great, but if you've got exabyte scale data to get into Amazon, nothing beats a tractor trailer full of drives.
	-	[CodeCommit](https://aws.amazon.com/codecommit/): Git service. You’re probably already using GitHub or your own solution ([Stackshare](http://stackshare.io/stackups/github-vs-bitbucket-vs-aws-codecommit) has informal stats).
	-	🕍[CodePipeline](https://aws.amazon.com/codepipeline/): Continuous integration. You likely have another solution already.
	-	🕍[CodeDeploy](https://aws.amazon.com/codedeploy/): Deployment of code to EC2 servers. Again, you likely have another solution.
	-	🕍[OpsWorks](https://aws.amazon.com/opsworks/): Management of your deployments using Chef or (as of November 2017) Puppet Enterprise. While Chef is popular, it seems few people use OpsWorks, since it involves going in on a whole different code deployment framework.
-	[AWS in Plain English](https://www.expeditedssl.com/aws-in-plain-english) offers more friendly explanation of what all the other different services are.

### Tools and Services Market Landscape

There are now enough cloud and “big data” enterprise companies and products that few can keep up with the market landscape. (See the [Big Data Evolving Landscape – 2016](https://practicalanalytics.co/2016/02/09/big-data-evolving-landscape-2016/) for one attempt at this.)

We’ve assembled a landscape of a few of the services. This is far from complete, but tries to emphasize services that are popular with AWS practitioners — services that specifically help with AWS, or a complementary, or tools almost anyone using AWS must learn.

![Popular Tools and Services for AWS Practitioners](figures/aws-market-landscape.png)

🚧 *Suggestions to improve this figure? Please [file an issue](CONTRIBUTING.md).*


### Common Concepts

-	📒 The AWS [**General Reference**](https://docs.aws.amazon.com/general/latest/gr/Welcome.html) covers a bunch of common concepts that are relevant for multiple services.
-	AWS allows deployments in [**regions**](https://docs.aws.amazon.com/general/latest/gr/rande.html), which are isolated geographic locations that help you reduce latency or offer additional redundancy. Regions contain availability zones(AZs), which are typically the first tool of choice for [high availability](#high-availability)). AZs are [physically separate from one another](https://www.youtube.com/watch?v=JIQETrFC_SQ&feature=youtu.be&t=1428) even within the same region, and [may span multiple physical data centers](https://blog.rackspace.com/aws-101-regions-availability-zones). While they are connected via low latency links, natural disasters afflicting one should not affect others.
-	Each service has API **endpoints** for each region. Endpoints differ from service to service and not all services are available in each region, as listed in [these tables](https://docs.aws.amazon.com/general/latest/gr/rande.html).
-	[**Amazon Resource Names (ARNs)**](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) are specially formatted identifiers for identifying resources. They start with 'arn:' and are used in many services, and in particular for IAM policies.

### Service Matrix

Many services within AWS can at least be compared with Google Cloud offerings or with internal Google services. And often times you could assemble the same thing yourself with open source software. This table is an effort at listing these rough correspondences. (Remember that this table is imperfect as in almost every case there are subtle differences of features!)

| Service                       | AWS                                                                          | Google Cloud                 | Google Internal | Microsoft Azure                    | Other providers                   | Open source “build your own”                               |
|-------------------------------|------------------------------------------------------------------------------|------------------------------|-----------------|------------------------------------|-----------------------------------|------------------------------------------------------------|
| Virtual server                | EC2                                                                          | Compute Engine (GCE)         |                 | Virtual Machine                    | DigitalOcean                      | OpenStack                                                  |
| PaaS                          | Elastic Beanstalk                                                            | App Engine                   | App Engine      | Web Apps                           | Heroku, AppFog, OpenShift | Meteor, AppScale, Cloud Foundry, Convox                    |
| Serverless, microservices     | Lambda, API Gateway                                                          | Functions                    |                 | Function Apps                      | PubNub Blocks, Auth0 Webtask      | Kong, Tyk                                                  |
| Container, cluster manager    | ECS                                                                          | Container Engine, Kubernetes | Borg or Omega   | Container Service                  |                                   | Kubernetes, Mesos, Aurora                                  |
| Object storage                  | S3                                                                           | Cloud Storage                | GFS             | Storage Account                    |                                   | Swift, HDFS                                                |
| Block storage                 | EBS                                                                          | Persistent Disk              |                 | Storage Account                    | DigitalOcean Volumes              | NFS                                                        |
| SQL datastore                 | RDS                                                                          | Cloud SQL                    |                 | SQL Database                       |                                   | MySQL, PostgreSQL                                          |
| Sharded RDBMS                 |                                                                              | Cloud Spanner                | F1, Spanner     |                                    |                                   | Crate.io, CockroachDB                                      |
| Bigtable                      |                                                                              | Cloud Bigtable               | Bigtable        |                                    |                                   | HBase                                                      |
| Key-value store, column store | DynamoDB                                                                     | Cloud Datastore              | Megastore       | Tables, DocumentDB                 |                                   | Cassandra, CouchDB, RethinkDB, Redis                       |
| Memory cache                  | ElastiCache                                                                  | App Engine Memcache          |                 | Redis Cache                        |                                   | Memcached, Redis                                           |
| Search                        | CloudSearch, Elasticsearch (managed)                                         |                              |                 | Search                             | Algolia, QBox, Elastic Cloud                     | Elasticsearch, Solr                                        |
| Data warehouse                | Redshift                                                                     | BigQuery                     | Dremel          | SQL Data Warehouse                 | Oracle, IBM, SAP, HP, many others | Greenplum                                                  |
| Business intelligence         | QuickSight                                                                   | Data Studio 360               |                 | Power BI                           | Tableau                           |                                                            |
| Lock manager                  | [DynamoDB (weak)](https://gist.github.com/ryandotsmith/c95fd21fab91b0823328) |                              | Chubby          | Lease blobs in Storage Account     |                                   | ZooKeeper, Etcd, Consul                                    |
| Message broker                | SQS, SNS, IoT                                                                | Pub/Sub                      | PubSub2         | Service Bus                        |                                   | RabbitMQ, Kafka, 0MQ                                       |
| Streaming, distributed log    | Kinesis                                                                      | Dataflow                     | PubSub2         | Event Hubs                         |                                   | Kafka Streams, Apex, Flink, Spark Streaming, Storm         |
| MapReduce                     | EMR                                                                          | Dataproc                     | MapReduce       | HDInsight, DataLake Analytics      | Qubole                            | Hadoop                                                     |
| Monitoring                    | CloudWatch                                                                   | Monitoring                   | Borgmon         | Monitor                            |                                   | Prometheus(?)                                              |
| Metric management             |                                                                              |                              | Borgmon, TSDB   | Application Insights               |                                   | Graphite, InfluxDB, OpenTSDB, Grafana, Riemann, Prometheus |
| CDN                           | CloudFront                                                                   | Cloud CDN                    |                 | CDN                                |  Akamai, Fastly, Cloudflare, Limelight Networks                                 | Apache Traffic Server                                      |
| Load balancer                 | CLB/ALB                                                                      | Load Balancing               | GFE             | Load Balancer, Application Gateway |                                   | nginx, HAProxy, Apache Traffic Server                      |
| DNS                           | Route53                                                                      | DNS                          |                 | DNS                                |                                   | bind                                                       |
| Email                         | SES                                                                          |                              |                 |                                    | Sendgrid, Mandrill, Postmark      |                                                            |
| Git hosting                   | CodeCommit                                                                   | Cloud Source Repositories    |                 | Visual Studio Team Services        | GitHub, BitBucket                 | GitLab                                                     |
| User authentication           | Cognito                                                                      |    Firebase Authentication                          |                 | Azure Active Directory             |                                   | oauth.io                                                   |
| Mobile app analytics          | Mobile Analytics                                                             | Firebase Analytics           |                 | HockeyApp                          | Mixpanel                          |                                                            |
| Mobile app testing            | Device Farm                                                                  | Firebase Test Lab            |                 | Xamarin Test Cloud                 | BrowserStack, Sauce Labs, Testdroid                                                            |
| Managing SSL/TLS certificates            | Certificate Manager                                                                  |                |                 |                 | Let's Encrypt, Comodo, Symantec, GlobalSign |
| Automatic speech recognition and natural language understanding            | Lex   | Cloud Speech API, Natural Language API             |                 | Cognitive services                | AYLIEN Text Analysis API, Ambiverse Natural Language Understanding API  |Stanford's Core NLP Suite, Apache OpenNLP, Apache UIMA, spaCy |
| Text-to-speech engine in the cloud            | Polly                                                                  |                |                 |                 |Nuance, Vocalware, IBM | Mimic, eSpeak, MaryTTS |
| Image recognition            | Rekognition                                                            |   Vision API              |                |Cognitive services                 | IBM Watson, Clarifai |TensorFlow, OpenCV |
| File Share and Sync          | WorkDocs                                                                   |   Google Docs                 |                 |OneDrive                  |       Dropbox, Box, Citrix File Share                  |ownCloud |



🚧 [*Please help fill this table in.*](CONTRIBUTING.md)

Selected resources with more detail on this chart:

-	Google internal: [MapReduce](http://research.google.com/archive/mapreduce.html), [Bigtable](http://research.google.com/archive/bigtable.html), [Spanner](http://research.google.com/archive/spanner.html), [F1 vs Spanner](http://highscalability.com/blog/2013/10/8/f1-and-spanner-holistically-compared.html), [Bigtable vs Megastore](http://perspectives.mvdirona.com/2008/07/google-megastore/)

### AWS Product Maturity and Releases

It’s important to know the maturity of each AWS product. Here is a mostly complete list of first release date, with links to the [release notes](https://aws.amazon.com/releasenotes/). Most recently released services are first. Not all services are available in all regions; see [this table](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/).

| Service                                                                                                    | Original release | Availability                                                                  | CLI Support | HIPAA Compliant | PCI-DSS Compliant |
|------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------|:-----------:|:---------------:|:-----------------:|
| 🐥[X-Ray](https://aws.amazon.com/releasenotes/AWS-X-Ray?browse=1)										  | 2016-12          | General																	  |✓            |                 |                   |
| 🐥[Lex](https://aws.amazon.com/releasenotes/Amazon-Lex?browse=1)                                           | 2016-11          | Preview                                                                       |             |                 |                   |
| 🐥[Polly](https://aws.amazon.com/releasenotes/Amazon-Polly?browse=1)                                       | 2016-11          | General                                                                       |✓            |                 |                   |
| 🐥[Rekognition](https://aws.amazon.com/releasenotes/Amazon-Rekognition?browse=1) 							 | 2016-11          | General                                                                       |✓            |					 |  				|
| 🐥[Athena](http://docs.aws.amazon.com/athena/latest/ug/what-is.html) 										 | 2016-11          | General                                                                       |✓             |                |					|
| 🐥[Batch](http://docs.aws.amazon.com/batch/latest/userguide/what-is-batch.html) 							 | 2016-11          | General                                                                       |✓             |				|					|
| 🐥[Database Migration Service](https://aws.amazon.com/releasenotes/AWS-Database-Migration-Service?browse=1) | 2016-03          | General                                                                      |              | ✓         		|	✓    			|
| 🐥[Certificate Manager](https://aws.amazon.com/blogs/aws/new-aws-certificate-manager-deploy-ssltls-based-apps-on-aws/) | 2016-01          | General                                                            | ✓		   |				|					|
| 🐥[IoT](https://aws.amazon.com/blogs/aws/aws-iot-now-generally-available/)                                  | 2015-08          | General                                                                       | ✓           |				|					|
| 🐥[WAF](https://aws.amazon.com/releasenotes/AWS-WAF?browse=1)                                               | 2015-10          | General                                                                       | ✓           | ✓         		|	✓    			|
| 🐥[Data Pipeline](https://aws.amazon.com/releasenotes/AWS-Data-Pipeline?browse=1)                           | 2015-10          | General                                                                       | ✓           |				|					|
| 🐥[Elasticsearch](https://aws.amazon.com/releasenotes/Amazon-Elasticsearch-Service?browse=1)                | 2015-10          | General                                                                       | ✓           |				|					|
| 🐥[Aurora](https://aws.amazon.com/releasenotes/2775579329314699)                                            | 2015-07          | General                                                                       | ✓           | ✓<sup>[3](#user-content-hipaa-aurora)</sup> |	✓<sup>[3](#user-content-hipaa-aurora)</sup>			|
| 🐥[Service Catalog](https://aws.amazon.com/releasenotes/AWS-Service-Catalog?browse=1)                       | 2015-07          | General                                                                       | ✓           |				|					|
| 🐥[Device Farm](https://aws.amazon.com/releasenotes/AWS-Device-Farm?browse=1)                         	  | 2015-07          | General                                                                       | ✓           |				|					|
| 🐥[CodePipeline](https://aws.amazon.com/releasenotes/AWS-CodePipeline?browse=1)                             | 2015-07          | General                                                                       | ✓           |				|					|
| 🐥[CodeCommit](https://aws.amazon.com/releasenotes/AWS-CodeCommit?browse=1)                                 | 2015-07          | General                                                                       | ✓           |				|					|
| 🐥[API Gateway](https://aws.amazon.com/releasenotes/Amazon-API-Gateway?browse=1)                            | 2015-07          | General                                                                       | ✓           | ✓<sup>[1](#user-content-hipaa-apigateway)</sup>  |	 ✓ 			|
| 🐥[Config](https://aws.amazon.com/releasenotes/AWS-Config?browse=1)                                         | 2015-06          | General                                                                       | ✓           |                 |  ✓              |
| 🐥[EFS](https://aws.amazon.com/releasenotes/Amazon-EFS?browse=1)                                            | 2015-05          | General                                                                       | ✓           |                 |                  |
| 🐥[Machine Learning](https://aws.amazon.com/releasenotes/AmazonML?browse=1)                                 | 2015-04          | General                                                                       | ✓           |                 |                  |
| [Lambda](https://aws.amazon.com/releasenotes/AWS-Lambda?browse=1)                                          | 2014-11          | General                                                                       | ✓           |                 |   ✓             |
| [ECS](https://aws.amazon.com/ecs/release-notes/)                                                           | 2014-11          | General                                                                       | ✓           | ✓         		|	✓   			|
| [KMS](https://aws.amazon.com/releasenotes/AWS-KMS?browse=1)                                                | 2014-11          | General                                                                       | ✓           |                 |   ✓             |
| [CodeDeploy](https://aws.amazon.com/releasenotes/AWS-CodeDeploy?browse=1)                                  | 2014-11          | General                                                                       | ✓           |                 |                  |
| [Kinesis](https://aws.amazon.com/releasenotes/Amazon-Kinesis?browse=1)                                     | 2013-12          | General                                                                       | ✓           |                 |   ✓<sup>[11](#user-content-pci-kinesis)</sup>    |
| [CloudTrail](https://aws.amazon.com/releasenotes/AWS-CloudTrail?browse=1)                                  | 2013-11          | General                                                                       | ✓           |                 |   ✓             |
| [AppStream](https://aws.amazon.com/releasenotes/Amazon-AppStream?browse=1)                                 | 2013-11          | Preview                                                                       |             |                 |                  |
| [CloudHSM](https://aws.amazon.com/releasenotes/AWS-CloudHSM?browse=1)                                      | 2013-03          | General                                                                       | ✓           |                 |   ✓            |
| [Silk](https://aws.amazon.com/releasenotes/Amazon-Silk?browse=1)                                           | 2013-03          | Obsolete?                                                                     |             |                 |                  |
| [OpsWorks](https://aws.amazon.com/releasenotes/AWS-OpsWorks?browse=1)                                      | 2013-02          | General                                                                       | ✓           |                 |   ✓             |
| [Redshift](https://aws.amazon.com/releasenotes/Amazon-Redshift?browse=1)                                   | 2013-02          | General                                                                       | ✓           | ✓         		|	✓   			|
| [Elastic Transcoder](https://aws.amazon.com/releasenotes/Amazon-Elastic-Transcoder?browse=1)               | 2013-01          | General                                                                       | ✓           |                 |                  |
| [Glacier](https://aws.amazon.com/releasenotes/Amazon-Glacier?browse=1)                                     | 2012-08          | General                                                                       | ✓           | ✓         		|	✓	    		|
| [CloudSearch](https://aws.amazon.com/releasenotes/Amazon-CloudSearch?browse=1)                             | 2012-04          | General                                                                       | ✓           |                 |                  |
| [SWF](https://aws.amazon.com/releasenotes/Amazon-SWF?browse=1)                                             | 2012-02          | General                                                                       | ✓           |                 | ✓                |
| [Storage Gateway](https://aws.amazon.com/releasenotes/AWS-Storage-Gateway?browse=1)                        | 2012-01          | General                                                                       | ✓           |                 |                  |
| [DynamoDB](https://aws.amazon.com/releasenotes/Amazon-DynamoDB?browse=1)                                   | 2012-01          | General                                                                       | ✓           | ✓         		|	  ✓  			|
| [DirectConnect](https://aws.amazon.com/releasenotes/AWS-Direct-Connect?browse=1)                           | 2011-08          | General                                                                       | ✓           | ✓         		|	✓   			|
| [ElastiCache](https://aws.amazon.com/releasenotes/Amazon-ElastiCache?browse=1)                             | 2011-08          | General                                                                       | ✓           |                 |                  |
| [CloudFormation](https://aws.amazon.com/releasenotes/AWS-CloudFormation?browse=1)                          | 2011-04          | General                                                                       | ✓           |                 |  ✓              |
| [SES](https://aws.amazon.com/releasenotes/Amazon-SES?browse=1)                                             | 2011-01          | General                                                                       | ✓           |                 |                  |
| [Elastic Beanstalk](https://aws.amazon.com/releasenotes/AWS-Elastic-Beanstalk?browse=1)                    | 2010-12          | General                                                                       | ✓           |                 |  ✓              |
| [Route 53](https://aws.amazon.com/releasenotes/Amazon-Route-53?browse=1)                                   | 2010-10          | General                                                                       | ✓           |                 | ✓               |
| [IAM](https://aws.amazon.com/releasenotes/AWS-Identity-and-Access-Management?browse=1)                     | 2010-09          | General                                                                       | ✓           |                 |  ✓              |
| [SNS](https://aws.amazon.com/releasenotes/Amazon-SNS?browse=1)                                             | 2010-04          | General                                                                       | ✓           | ✓         		|					|
| [EMR](https://aws.amazon.com/releasenotes/Elastic-MapReduce?browse=1)                                      | 2010-04          | General                                                                       | ✓           | ✓         		|	✓   			|
| [RDS](https://aws.amazon.com/releasenotes/Amazon-RDS?browse=1)                                             | 2009-12          | General                                                                       | ✓           |✓<sup>[2](#user-content-hipaa-rds)</sup>        |✓<sup>[9](#user-content-pci-rds)</sup>				|    
| [VPC](https://aws.amazon.com/releasenotes/Amazon-VPC?browse=1)                                             | 2009-08          | General                                                                       | ✓           | ✓         		|	✓   			|
| [Snowball](https://aws.amazon.com/releasenotes/AWS-ImportExport?browse=1)                                  | 2015-10          | General                                                                       | ✓           | ✓         		|					|
| [Snowmobile](https://aws.amazon.com/snowmobile/)                                                           | 2016-11          | General                                                                       |            |                 |                  |
| [CloudWatch](https://aws.amazon.com/releasenotes/CloudWatch?browse=1)                                      | 2009-05          | General                                                                       | ✓           |                 |  ✓               |
| [CloudFront](https://aws.amazon.com/releasenotes/CloudFront?browse=1)                                      | 2008-11          | General                                                                       | ✓           | ✓<sup>[4](#user-content-hipaa-cloudfront)</sup>        |  ✓				|
| [Fulfillment Web Service](https://aws.amazon.com/releasenotes/Amazon-FWS?browse=1)                         | 2008-03          | Obsolete?                                                                     |             |                 |                  |
| [SimpleDB](https://aws.amazon.com/releasenotes/Amazon-SimpleDB?browse=1)                                   | 2007-12          | ❗[Nearly obsolete](https://forums.aws.amazon.com/thread.jspa?threadID=121711) | ✓           |                 |  ✓              |
| [DevPay](https://aws.amazon.com/releasenotes/DevPay?browse=1)                                              | 2007-12          | General                                                                       |             |                 |                  |
| [Flexible Payments Service](https://aws.amazon.com/releasenotes/Amazon-FPS?browse=1)                       | 2007-08          | Retired                                                                       |             |                 |                  |
| [EC2](https://aws.amazon.com/releasenotes/Amazon-EC2?browse=1)                                             | 2006-08          | General                                                                       | ✓           | ✓<sup>[5](#user-content-hipaa-ec2sysmgr),[6](#user-content-hipaa-ec2ebs),[7](#user-content-hipaa-ec2elb)</sup>          |	✓<sup>[6](#user-content-hipaa-ec2ebs),[7](#user-content-hipaa-ec2elb),[10](#user-content-pci-asg)</sup>			|
| [SQS](https://aws.amazon.com/releasenotes/Amazon-SQS?browse=1)                                             | 2006-07          | General                                                                       | ✓           | ✓         		| ✓               |
| [S3](https://aws.amazon.com/releasenotes/Amazon-S3?browse=1)                                               | 2006-03          | General                                                                       | ✓           | ✓<sup>[8](#user-content-hipaa-s3)</sup>   |	✓   			|
| [Alexa Top Sites](https://aws.amazon.com/alexa-top-sites/)                                                 | 2006-01          | General ❗HTTP-only                                                            |             |                 |                  |
| [Alexa Web Information Service](https://aws.amazon.com/awis/)                                              | 2005-10          | General ❗HTTP-only                                                            |             |                 |                  |

##### Footnotes
<a name="user-content-hipaa-apigateway">**1**</a>: Excludes use of Amazon API Gateway caching<br />
<a name="user-content-hipaa-rds">**2**</a>: RDS MySQL, Oracle, and PostgreSQL engines only<br />
<a name="user-content-hipaa-aurora">**3**</a>: MySQL-compatible Aurora edition only<br />
<a name="user-content-hipaa-cloudfront">**4**</a>: Excludes Lambda@Edge<br />
<a name="user-content-hipaa-ec2sysmgr">**5**</a>: Includes EC2 Systems Manager<br />
<a name="user-content-hipaa-ec2ebs">**6**</a>: Includes Elastic Block Storage (EBS)<br />
<a name="user-content-hipaa-ec2elb">**7**</a>: Includes Elastic Load Balancing<br />
<a name="user-content-hipaa-s3">**8**</a>: Includes S3 Transfer Acceleration<br />
<a name="user-content-pci-rds">**9**</a>: Includes RDS MySQL, Oracle, PostgreSQL, SQL Server, and MariaDB</br>
<a name="user-content-pci-asg">**10**</a>: Includes Auto-Scaling</br>
<a name="user-content-pci-kinesis">**11**</a>: Streams only</br>


### Compliance

-	Many applications have strict requirements around reliability, security, or data privacy. The [AWS Compliance](https://aws.amazon.com/compliance/) page has details about AWS’s certifications, which include **PCI DSS Level 1**, **SOC 1,2, and 3**, **HIPAA**, and **ISO 9001**.
-	Security in the cloud is a complex topic, based on a [shared responsibility model](https://aws.amazon.com/compliance/shared-responsibility-model/), where some elements of compliance are provided by AWS, and some are provided by your company.
-	Several third-party vendors offer assistance with compliance, security, and auditing on AWS. If you have substantial needs in these areas, assistance is a good idea.
-	From inside **China**, AWS services outside China [are generally accessible](https://en.greatfire.org/aws.amazon.com), though there are at times breakages in service. There are also AWS services [inside China](https://www.amazonaws.cn/en/).

### Getting Help and Support

-	**Forums:** For many problems, it’s worth searching or asking for help in the [discussion forums](https://forums.aws.amazon.com/index.jspa) to see if it’s a known issue.
-	**Premium support:** AWS offers several levels of [premium support](https://aws.amazon.com/premiumsupport/).
	-	The first tier, called "Developer support" lets you file support tickets with 12 to 24 hour turnaround time, it starts at $29 but once your monthly spend reaches around $1000 it changes to a 3% surcharge on your bill.
	-	The higher-level support services are quite expensive — and increase your bill by up to 10%. Many large and effective companies never pay for this level of support. They are usually more helpful for midsize or larger companies needing rapid turnaround on deeper or more perplexing problems.
	-	Keep in mind, a flexible architecture can reduce need for support. You shouldn’t be relying on AWS to solve your problems often. For example, if you can easily re-provision a new server, it may not be urgent to solve a rare kernel-level issue unique to one EC2 instance. If your EBS volumes have recent snapshots, you may be able to restore a volume before support can rectify the issue with the old volume. If your services have an issue in one availability zone, you should in any case be able to rely on a redundant zone or migrate services to another zone.
	-	Larger customers also get access to AWS Enterprise support, with dedicated technical account managers (TAMs) and shorter response time SLAs.
	-	There is definitely some controversy about how useful the paid support is. The support staff don’t always seem to have the information and authority to solve the problems that are brought to their attention. Often your ability to have a problem solved may depend on your relationship with your account rep.
-	**Account manager:** If you are at significant levels of spend (thousands of US dollars plus per month), you may be assigned (or may wish to ask for) a dedicated account manager.
	-	These are a great resource, even if you’re not paying for premium support. Build a good relationship with them and make use of them, for questions, problems, and guidance.
	-	Assign a single point of contact on your company’s side, to avoid confusing or overwhelming them.
-	**Contact:** The main web contact point for AWS is [here](https://aws.amazon.com/contact-us/). Many technical requests can be made via these channels.
-	**Consulting and managed services:** For more hands-on assistance, AWS has established relationships with many [consulting partners](https://aws.amazon.com/partners/consulting/) and [managed service partners](https://aws.amazon.com/partners/msp/). The big consultants won’t be cheap, but depending on your needs, may save you costs long term by helping you set up your architecture more effectively, or offering specific expertise, e.g. security. Managed service providers provide longer-term full-service management of cloud resources.
-	**AWS Professional Services:** AWS provides [consulting services](https://aws.amazon.com/professional-services/) alone or in combination with partners.

### Restrictions and Other Notes

-	🔸Lots of resources in Amazon have [**limits**](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) on them. This is actually helpful, so you don’t incur large costs accidentally. You have to request that quotas be increased by opening support tickets. Some limits are easy to raise, and some are not. (Some of these are noted in sections below.)
	- **Obtaining Current Limits and Usage:** Limit information for a service may be available from the service API, Trusted Advisor, both or neither (in which case you'll need to contact Support). [This page](http://awslimitchecker.readthedocs.io/en/latest/limits.html) from the awslimitchecker tool's documentation provides a nice summary of available retrieval options for each limit. The [tool](https://github.com/jantman/awslimitchecker) itself is also valuable for automating limit checks.
-	🔸[**AWS terms of service**](https://aws.amazon.com/service-terms/) are extensive. Much is expected boilerplate, but it does contain important notes and restrictions on each service. In particular, there are restrictions against using many AWS services in **safety-critical systems**. (Those appreciative of legal humor may wish to review clause 57.10.)

### Related Topics

-	[OpenStack](https://www.openstack.org/) is a private cloud alternative to AWS used by large companies that wish to avoid public cloud offerings.

Learning and Career Development
-------------------------------

### Certifications

-	**Certifications:** AWS offers [**certifications**](https://aws.amazon.com/certification/) for IT professionals who want to demonstrate their knowledge.
  -	[Certified Solutions Architect Associate](https://aws.amazon.com/certification/certified-solutions-architect-associate/)
  -	[Certified Developer Associate](https://aws.amazon.com/certification/certified-developer-associate/)
  -	[Certified SysOps Administrator Associate](https://aws.amazon.com/certification/certified-sysops-admin-associate/)
  -	[Certified Solutions Architect Professional](https://aws.amazon.com/certification/certified-solutions-architect-professional/)
  -	[Certified DevOps Engineer Professional](https://aws.amazon.com/certification/certified-devops-engineer-professional/)
-	**Getting certified:** If you’re interested in studying for and getting certifications, [this practical overview](https://gist.github.com/leonardofed/bbf6459ad154ad5215d354f3825435dc) tells you a lot of what you need to know. The official page is [here](https://aws.amazon.com/training/) and there is an [FAQ](https://aws.amazon.com/certification/faqs/).
-	**Do you need a certification?** Especially in consulting companies or when working in key tech roles in large non-tech companies, certifications are important credentials. In others, including in many tech companies and startups, certifications are not common or considered necessary. (In fact, fairly or not, some Silicon Valley hiring managers and engineers see them as a “negative” signal on a resume.)

Managing AWS
------------

### Managing Infrastructure State and Change

A great challenge in using AWS to build complex systems (and with DevOps in general) is to manage infrastructure state effectively over time. In general, this boils down to three broad goals for the state of your infrastructure:

-	**Visibility**: Do you know the state of your infrastructure (what services you are using, and exactly how)? Do you also know when you — and anyone on your team — make changes? Can you detect misconfigurations, problems, and incidents with your service?
-	**Automation**: Can you reconfigure your infrastructure to reproduce past configurations or scale up existing ones without a lot of extra manual work, or requiring knowledge that’s only in someone’s head? Can you respond to incidents easily or automatically?
-	**Flexibility**: Can you improve your configurations and scale up in new ways without significant effort? Can you add more complexity using the same tools? Do you share, review, and improve your configurations within your team?

Much of what we discuss below is really about how to improve the answers to these questions.

There are several approaches to deploying infrastructure with AWS, from the console to complex automation tools, to third-party services, all of which attempt to help achieve visibility, automation, and flexibility.

### AWS Configuration Management

The first way most people experiment with AWS is via its web interface, the AWS Console. But using the Console is a highly manual process, and often works against automation or flexibility.

So if you’re not going to manage your AWS configurations manually, what should you do? Sadly, there are no simple, universal answers — each approach has pros and cons, and the approaches taken by different companies vary widely, and include directly using APIs (and building tooling on top yourself), using command-line tools, and using third-party tools and services.

### AWS Console

-	The [AWS Console](https://aws.amazon.com/console/) lets you control much (but not all) functionality of AWS via a web interface.
-	Ideally, you should only use the AWS Console in a few specific situations:
	-	It’s great for read-only usage. If you’re trying to understand the state of your system, logging in and browsing it is very helpful.
	-	It is also reasonably workable for very small systems and teams (for example, one engineer setting up one server that doesn’t change often).
	-	It can be useful for operations you’re only going to do rarely, like less than once a month (for example, a one-time VPC setup you probably won’t revisit for a year). In this case using the console can be the simplest approach.
-	❗**Think before you use the console:** The AWS Console is convenient, but also the enemy of automation, reproducibility, and team communication. If you’re likely to be making the same change multiple times, avoid the console. Favor some sort of automation, or at least have a path toward automation, as discussed next. Not only does using the console preclude automation, which wastes time later, but it prevents documentation, clarity, and standardization around processes for yourself and your team.

### Command-Line tools

-	The [**aws command-line interface**](https://aws.amazon.com/cli/) (CLI), used via the **aws** command, is the most basic way to save and automate AWS operations.
-	Don’t underestimate its power. It also has the advantage of being well-maintained — it covers a large proportion of all AWS services, and is up to date.
-	In general, whenever you can, prefer the command line to the AWS Console for performing operations.
-	🔹Even in the absence of fancier tools, you can **write simple Bash scripts** that invoke *aws* with specific arguments, and check these into Git. This is a primitive but effective way to document operations you’ve performed. It improves automation, allows code review and sharing on a team, and gives others a starting point for future work.
-	🔹For use that is primarily interactive (not scripted), consider instead using the [**aws-shell**](https://github.com/awslabs/aws-shell) tool from AWS. It is easier to use, with auto-completion and a colorful UI, but still works on the command line. If you’re using [SAWS](https://github.com/donnemartin/saws), a previous version of the program, [you should migrate to aws-shell](https://github.com/donnemartin/saws/issues/68#issuecomment-240067034).

### APIs and SDKs

-	**SDKs** for using AWS APIs are available in most major languages, with [Go](https://github.com/aws/aws-sdk-go), [iOS](https://github.com/aws/aws-sdk-ios), [Java](https://github.com/aws/aws-sdk-java), [JavaScript](https://github.com/aws/aws-sdk-js), [Python](https://github.com/boto/boto3), [Ruby](https://github.com/aws/aws-sdk-ruby), and [PHP](https://github.com/aws/aws-sdk-php) being most heavily used. AWS maintains [a short list](https://aws.amazon.com/tools/#sdk), but the [awesome-aws list](https://github.com/donnemartin/awesome-aws#sdks-and-samples) is the most comprehensive and current. Note [support for C++](https://github.com/donnemartin/awesome-aws#c-sdk) is [still new](https://aws.amazon.com/blogs/aws/introducing-the-aws-sdk-for-c/).
-	**Retry logic:** An important aspect to consider whenever using SDKs is error handling; under heavy use, a wide variety of failures, from programming errors to throttling to AWS-related outages or failures, can be expected to occur. SDKs typically implement [**exponential backoff**](https://docs.aws.amazon.com/general/latest/gr/api-retries.html) to address this, but this may need to be understood and adjusted over time for some applications. For example, it is often helpful to alert on some error codes and not on others.
-	❗Don’t use APIs directly. Although AWS documentation includes lots of API details, it’s better to use the SDKs for your preferred language to access APIs. SDKs are more mature, robust, and well-maintained than something you’d write yourself.

### Boto

-	A good way to automate operations in a custom way is [**Boto3**](https://github.com/boto/boto3), also known as the [Amazon SDK for Python](http://aws.amazon.com/sdk-for-python/). [**Boto2**](https://github.com/boto/boto), the previous version of this library, has been in wide use for years, but now there is a newer version with official support from Amazon, so prefer Boto3 for new projects.
-	Boto3 contains a variety of APIs that operate at either a high level or a low level, here some explanation of both:
	-	The low level APIs (Client APIs) are mapped to AWS Cloud service-specific APIs, and all service operations are supported by clients. Clients are generated from a JSON service definition file.
	-	The high level option, Resource APIs, allows you to avoid calling the network at the low level and instead provide an object-oriented way to interact with AWS Cloud services.
-	Boto3 has a lot of helpful [**features**](https://boto3.readthedocs.io/en/latest/guide/index.html#general-feature-guides) like *waiters*, which provide a structure that allows for code to wait for changes to occur in the cloud, for example, when you are creating an EC2 instance and need wait until the instance is running in order to perform another task.
-	If you find yourself writing a Bash script with more than one or two CLI commands, you’re probably doing it wrong. Stop, and consider writing a Boto script instead. This has the advantages that you can:
	-	Check return codes easily so success of each step depends on success of past steps.
	-	Grab interesting bits of data from responses, like instance ids or DNS names.
	-	Add useful environment information (for example, tag your instances with git revisions, or inject the latest build identifier into your initialization script).

### General Visibility

-	🔹[**Tagging resources**](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Using_Tags.html) is an essential practice, especially as organizations grow, to better understand your resource usage. For example, through automation or convention, you can add tags:
	-	For the org or developer that “owns” that resource
	-	For the product that resource supports
	-	To label lifecycles, such as temporary resources or one that should be deprovisioned in the future
	-	To distinguish production-critical infrastructure (e.g. serving systems vs backend pipelines)
	-	To distinguish resources with special security or compliance requirements
	-	For many years, there was a notorious 10 tag limit per resource, which could not be raised and caused many companies significant pain. As of 2016, this was [raised](https://aws.amazon.com/blogs/security/now-organize-your-aws-resources-by-using-up-to-50-tags-per-resource/) to 50 tags per resource.
	-	🔹In 2017, AWS introduced the ability to [enforce tagging](https://aws.amazon.com/blogs/aws/new-tag-ec2-instances-ebs-volumes-on-creation/) on instance and volume creation, deprecating portions of third party tools such as [Cloud Custodian](https://github.com/capitalone/cloud-custodian).

Managing Servers and Applications
---------------------------------

### AWS vs Server Configuration

This guide is about AWS, not DevOps or server configuration management in general. But before getting into AWS in detail, it’s worth noting that in addition to the configuration management for your AWS resources, there is the long-standing problem of configuration management for servers themselves.

### Philosophy

-	Heroku’s [**Twelve-Factor App**](http://12factor.net/) principles list some established general best practices for deploying applications.
-	**Pets vs cattle:** Treat servers [like cattle, not pets](https://blog.engineyard.com/2014/pets-vs-cattle). That is, design systems so infrastructure is disposable. It should be minimally worrisome if a server is unexpectedly destroyed.
-	The concept of [**immutable infrastructure**](http://radar.oreilly.com/2015/06/an-introduction-to-immutable-infrastructure.html) is an extension of this idea.
-	Minimize application state on EC2 instances. In general, instances should be able to be killed or die unexpectedly with minimal impact. State that is in your application should quickly move to RDS, S3, DynamoDB, EFS, or other data stores not on that instance. EBS is also an option, though it generally should not be the bootable volume, and EBS will require manual or automated re-mounting.

### Server Configuration Management

-	There is a [large set](https://en.wikipedia.org/wiki/Comparison_of_open-source_configuration_management_software) of open source tools for managing configuration of server instances.
-	These are generally not dependent on any particular cloud infrastructure, and work with any variety of Linux (or in many cases, a variety of operating systems).
-	Leading configuration management tools are [Puppet](https://github.com/puppetlabs/puppet), [Chef](https://github.com/chef/chef), [Ansible](https://github.com/ansible/ansible), and [Saltstack](https://github.com/saltstack/salt). These aren’t the focus of this guide, but we may mention them as they relate to AWS.

### Containers and AWS

-	[Docker](http://blog.scottlowe.org/2014/03/11/a-quick-introduction-to-docker/) and the containerization trend are changing the way many servers and services are deployed in general.
-	Containers are designed as a way to package up your application(s) and all of their dependencies in a known way. When you build a container, you are including every library or binary your application needs, outside of the kernel. A big advantage of this approach is that it’s easy to test and validate a container locally without worrying about some difference between your computer and the servers you deploy on.
-	A consequence of this is that you need fewer AMIs and boot scripts; for most deployments, the only boot script you need is a template that fetches an exported docker image and runs it.
-	Companies that are embracing [microservice architectures](http://martinfowler.com/articles/microservices.html) will often turn to container-based deployments.
-	AWS launched [ECS](https://aws.amazon.com/ecs/) as a service to manage clusters via Docker in late 2014, though many people still deploy Docker directly themselves. See the [ECS section](#ecs) for more details.

### Visibility

-	Store and track instance metadata (such as instance id, availability zone, etc.) and deployment info (application build id, Git revision, etc.) in your logs or reports. The [**instance metadata service**](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) can help collect some of the AWS data you’ll need.
-	**Use log management services:** Be sure to set up a way to view and manage logs externally from servers.
	-	Cloud-based services such as [Sumo Logic](https://www.sumologic.com/), [Splunk Cloud](http://www.splunk.com/en_us/cloud.html), [Scalyr](https://www.scalyr.com/), and [Loggly](https://www.loggly.com/) are the easiest to set up and use (and also the most expensive, which may be a factor depending on how much log data you have).
	-	Major open source alternatives include [Elasticsearch](https://github.com/elastic/elasticsearch), [Logstash](https://github.com/elastic/logstash), and [Kibana](https://github.com/elastic/kibana) (the “[Elastic Stack](https://www.elastic.co/webinars/introduction-elk-stack)”) and [Graylog](https://www.graylog.org/).
	-	If you can afford it (you have little data or lots of money) and don’t have special needs, it makes sense to use hosted services whenever possible, since setting up your own scalable log processing systems is notoriously time consuming.
-	**Track and graph metrics:** The AWS Console can show you simple graphs from CloudWatch, you typically will want to track and graph many kinds of metrics, from CloudWatch and your applications. Collect and export helpful metrics everywhere you can (and as long as volume is manageable enough you can afford it).
	-	Services like [Librato](https://www.librato.com/), [KeenIO](https://keen.io/), and [Datadog](https://www.datadoghq.com/) have fancier features or better user interfaces that can save a lot of time. (A more detailed comparison is [here](http://blog.takipi.com/production-tools-guide/visualization-and-metrics/).)
	-	Use [Prometheus](https://prometheus.io) or [Graphite](https://github.com/graphite-project/graphite-web) as timeseries databases for your metrics (both are open source).
	-	[Grafana](https://github.com/grafana/grafana) can visualize with dashboards the stored metrics of both timeseries databases (also open source).

### Tips for Managing Servers

-	❗**Timezone settings on servers**: unless *absolutely necessary*, always **set the timezone on servers to [UTC](https://en.wikipedia.org/wiki/Coordinated_Universal_Time)** (see instructions for your distribution, such as [Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-set-up-timezone-and-ntp-synchronization-on-ubuntu-14-04-quickstart), [CentOS](https://www.vultr.com/docs/setup-timezone-and-ntp-on-centos-6) or [Amazon](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/set-time.html) Linux). Numerous distributed systems rely on time for synchronization and coordination and UTC [provides](https://blog.serverdensity.com/set-your-server-timezone-to-utc/) the universal reference plane: it is not subject to  daylight savings changes and adjustments in local time. It will also save you a lot of headache debugging [elusive timezone issues](http://yellerapp.com/posts/2015-01-12-the-worst-server-setup-you-can-make.html) and provide coherent timeline of events in your logging and audit systems.
-	**NTP and accurate time:** If you are not using Amazon Linux (which comes preconfigured), you should confirm your servers [configure NTP correctly](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/set-time.html#configure_ntp), to avoid insidious time drift (which can then cause all sorts of issues, from breaking API calls to misleading logs). This should be part of your automatic configuration for every server. If time has already drifted substantially (generally >1000 seconds), remember NTP won’t shift it back, so you may need to remediate manually (for example, [like this](http://askubuntu.com/questions/254826/how-to-force-a-clock-update-using-ntp) on Ubuntu).
-	**Testing immutable infrastructure:** If you want to be proactive about testing your service’s ability to cope with instance termination or failure, it can be helpful to introduce random instance termination during business hours, which will expose any such issues at a time when engineers are available to identify and fix them. Netflix’s [Simian Army](https://github.com/Netflix/SimianArmy) (specifically, [Chaos Monkey](https://github.com/Netflix/SimianArmy/wiki/Chaos-Monkey)) is a popular tool for this. Alternatively, [chaos-lambda](https://github.com/bbc/chaos-lambda) by the BBC is a lightweight option which runs on AWS [Lambda](#lambda).

Security and IAM
----------------

We cover security basics first, since configuring user accounts is something you usually have to do early on when setting up your system.

### Security and IAM Basics

-	📒 IAM [Homepage](https://aws.amazon.com/iam/) ∙ [User guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) ∙ [FAQ](https://aws.amazon.com/iam/faqs/)
-	The [AWS Security Blog](https://blogs.aws.amazon.com/security) is one of the best sources of news and information on AWS security.
-	**IAM** is the service you use to manage accounts and permissioning for AWS.
-	Managing security and access control with AWS is critical, so every AWS administrator needs to use and understand IAM, at least at a basic level.
-	[IAM identities](https://docs.aws.amazon.com/IAM/latest/UserGuide/id.html) include users (people or services that are using AWS), groups (containers for sets of users and their permissions), and roles (containers for permissions assigned to AWS service instances). [Permissions](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_permissions.html) for these identities are governed by [policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html) You can use AWS pre-defined policies or custom policies that you create.
-	IAM manages various kinds of authentication, for both users and for software services that may need to authenticate with AWS, including:
	-	[**Passwords**](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_passwords.html) to log into the console. These are a username and password for real users.
	-	[**Access keys**](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html), which you may use with command-line tools. These are two strings, one the “id”, which is an upper-case alphabetic string of the form 'AXXXXXXXXXXXXXXXXXXX', and the other is the secret, which is a 40-character mixed-case base64-style string. These are often set up for services, not just users.
		-	📜 Access keys that start with AKIA are normal keys. Access keys that start with ASIA are session/temporary keys from STS, and will require an additional "SessionToken" parameter to be sent along with the id and secret.
	-	[**Multi-factor authentication (MFA)**](https://aws.amazon.com/iam/details/mfa/), which is the highly recommended practice of using a keychain fob or smartphone app as a second layer of protection for user authentication.
-	IAM allows complex and fine-grained control of permissions, dividing users into groups, assigning permissions to roles, and so on. There is a [policy language](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html) that can be used to customize security policies in a fine-grained way.
	-	An excellent high level overview of IAM policy concepts lives at [IAM Policies In A Nutshell](http://start.jcolemorrison.com/aws-iam-policies-in-a-nutshell/).
	-	🔸The policy language has a complex and error-prone JSON syntax that’s quite confusing, so unless you are an expert, it is wise to base yours off trusted examples or AWS’ own pre-defined [managed policies](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_managed-vs-inline.html).
-	At the beginning, IAM policy may be very simple, but for large systems, it will grow in complexity, and need to be managed with care.
	-	🔹Make sure one person (perhaps with a backup) in your organization is formally assigned ownership of managing IAM policies, make sure every administrator works with that person to have changes reviewed. This goes a long way to avoiding accidental and serious misconfigurations.
-	It is best to give each user or service the minimum privileges needed to perform their duties. This is the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege), one of the foundations of good security. Organize all IAM users and groups according to levels of access they need.
-	IAM has the [permission hierarchy](http://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_evaluation-logic.html) of:
	1. Explicit deny: The most restrictive policy wins.
	2. Explicit allow: Access permissions to any resource has to be explicitly given.
	3. Implicit deny: All permissions are implicitly denied by default.
-	You can test policy permissions via the AWS IAM [policy simulator tool tool](https://policysim.aws.amazon.com/home/index.jsp). This is particularly useful if you write custom policies.


### Security and IAM Tips

-	🔹Use IAM to create individual user accounts and **use IAM accounts for all users from the beginning**. This is slightly more work, but not that much.
	-	That way, you define different users, and groups with different levels of privilege (if you want, choose from Amazon’s default suggestions, of administrator, power user, etc.).
	-	This allows credential revocation, which is critical in some situations. If an employee leaves, or a key is compromised, you can revoke credentials with little effort.
	-	You can set up [Active Directory federation](https://blogs.aws.amazon.com/security/post/Tx71TWXXJ3UI14/Enabling-Federation-to-AWS-using-Windows-Active-Directory-ADFS-and-SAML-2-0) to use organizational accounts in AWS.
-	❗**Enable [MFA](https://aws.amazon.com/iam/details/mfa/)** on your account.
	-	You should always use MFA, and the sooner the better — enabling it when you already have many users is extra work.
	-	Unfortunately it can’t be enforced in software, so an administrative policy has to be established.
	-	Most users can use the Google Authenticator app (on [iOS](https://itunes.apple.com/us/app/google-authenticator/id388497605) or [Android](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)) to support two-factor authentication. For the root account, consider a hardware fob.
- ❗Restrict use of significant IAM credentials as much as possible. Remember that in the cloud, loss of a highly capable IAM credential could essentially mean “game over,” for your deployment, your users, or your whole company.
  -	**Do NOT use the [IAM Root User account](http://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html)** other than when you initially create your account.  Create custom IAM users and/or roles and use those for your applications instead.
	- Lock up access and use of the root credentials as much as possible. Ideally they should be effectively “offline.” For critical deployments, this means attached to an actual MFA device, physically secured and rarely used.
-	❗**Turn on CloudTrail:** One of the first things you should do is [enable CloudTrail](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-create-a-trail-using-the-console-first-time.html). Even if you are not a security hawk, there is little reason not to do this from the beginning, so you have data on what has been happening in your AWS account should you need that information. You’ll likely also want to set up a [log management service](#visibility) to search and access these logs.
-	🔹**Use IAM roles for EC2:** Rather than assign IAM users to applications like services and then sharing the sensitive credentials, [define and assign roles to EC2 instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html) and have applications retrieve credentials from the [instance metadata](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html).
-	Assign IAM roles by realm — for example, to development, staging, and production. If you’re setting up a role, it should be tied to a specific realm so you have clean separation. This prevents, for example, a development instance from connecting to a production database.
-	**Best practices:** AWS’ [list of best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) is worth reading in full up front.
-	**IAM Reference:** [This interactive reference for all IAM actions, effects, and resources](https://iam.cloudonaut.io/) is great to have open while writing new or trying to understand existing IAM policies.
-	**Multiple accounts:** Decide on whether you want to use multiple AWS accounts and [research](https://dab35129f0361dca3159-2fe04d8054667ffada6c4002813eccf0.ssl.cf1.rackcdn.com/downloads/pdfs/Rackspace%20Best%20Practices%20for%20AWS%20-%20Identity%20Managment%20-%20Billing%20-%20Auditing.pdf) how to organize access across them. Factors to consider:
	-	Number of users
	-	Importance of isolation
		-	Resource Limits
		-	Permission granularity
		-	Security
		-	API Limits
	-	Regulatory issues
	-	Workload
	-	Size of infrastructure
	-	Cost of multi-account “overhead”: Internal AWS service management tools may need to be custom built or adapted.
	-	🔹It can help to use separate AWS accounts for independent parts of your infrastructure if you expect a high rate of AWS API calls, since AWS [throttles calls](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/query-api-troubleshooting.html#api-request-rate) at the AWS account level.
-	[**Inspector**](https://aws.amazon.com/inspector/) is an automated security assessment service from AWS that helps identify common security risks. This allows validation that you adhere to certain security practices and may help with compliance.
-	[**Trusted Advisor**](https://aws.amazon.com/blogs/aws/trusted-advisor-console-basic/) addresses a variety of best practices, but also offers some basic security checks around IAM usage, security group configurations, and MFA. At paid support tiers, Trusted Advisor exposes additional checks around other areas, such as reserved instance optimization.
-	**Use KMS for managing keys**: AWS offers [KMS](#kms) for securely managing encryption keys, which is usually a far better option than handling key security yourself. See [below](#kms).
-	[**AWS WAF**](https://aws.amazon.com/waf) is a web application firewall to help you protect your applications from common attack patterns.
-	**Security auditing:**
	-	[Security Monkey](https://github.com/Netflix/security_monkey) is an open source tool that is designed to assist with security audits.
	-	[Scout2](https://github.com/nccgroup/Scout2) is an open source tool that uses AWS APIs to assess an environment’s security posture. Scout2 is stable and actively maintained.
	-	🔹**Export and audit security settings:** You can audit security policies simply by exporting settings using AWS APIs, e.g. using a Boto script like [SecConfig.py](https://gist.github.com/jlevy/cce1b44fc24f94599d0a4b3e613cc15d) (from [this 2013 talk](http://www.slideshare.net/AmazonWebServices/intrusion-detection-in-the-cloud-sec402-aws-reinvent-2013)) and then reviewing and monitoring changes manually or automatically.

### Security and IAM Gotchas and Limitations

-	❗**Don’t share user credentials:** It’s remarkably common for first-time AWS users to create one account and one set of credentials (access key or password), and then use them for a while, sharing among engineers and others within a company. This is easy. But *don’t do this*. This is an insecure practice for many reasons, but in particular, if you do, you will have reduced ability to revoke credentials on a per-user or per-service basis (for example, if an employee leaves or a key is compromised), which can lead to serious complications.
-	❗**Instance metadata throttling:** The [instance metadata service](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html) has rate limiting on API calls. If you deploy IAM roles widely (as you should!) and have lots of services, you may hit global account limits easily.
	-	One solution is to have code or scripts cache and reuse the credentials locally for a short period (say 2 minutes). For example, they can be put into the ~/.aws/credentials file but must also be refreshed automatically.
	-	But be careful not to cache credentials for too long, as [they expire](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/iam-roles-for-amazon-ec2.html#instance-metadata-security-credentials). (Note the other [dynamic metadata](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html#dynamic-data-categories) also changes over time and should not be cached a long time, either.)
-	🔸Some IAM operations are slower than other API calls (many seconds), since AWS needs to propagate these globally across regions.
-	❗The uptime of IAM’s API has historically been lower than that of the instance metadata API. Be wary of incorporating a dependency on IAM’s API into critical paths or subsystems — for example, if you validate a user’s IAM group membership when they log into an instance and aren’t careful about precaching group membership or maintaining a back door, you might end up locking users out altogether when the API isn’t available.
-	❗**Don't check in AWS credentials or secrets to a git repository.** There are bots that scan GitHub looking for credentials. Use scripts or tools, such as [git-secrets](https://github.com/awslabs/git-secrets) to prevent anyone on your team from checking in sensitive information to your git repositories.

S3
--

### S3 Basics

-	📒 [Homepage](https://aws.amazon.com/s3/) ∙ [Developer guide](https://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html) ∙ [FAQ](https://aws.amazon.com/s3/faqs/) ∙ [Pricing](https://aws.amazon.com/s3/pricing/)
-	**S3** (Simple Storage Service) is AWS’ standard cloud storage service, offering file (opaque “blob”) storage of arbitrary numbers of files of almost any size, from 0 to **5TB**. (Prior to [2011](https://aws.amazon.com/releasenotes/Amazon-S3/1917932037969964) the maximum size was 5 GB; larger sizes are now well supported via [multipart support](https://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html).)
-	Items, or **objects**, are placed into named **buckets** stored with names which are usually called **keys**. The main content is the **value**.
-	Objects are created, deleted, or updated. Large objects can be streamed, but you cannot access or modify parts of a value; you need to update the whole object.
-	Every object also has [**metadata**](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingMetadata.html), which includes arbitrary key-value pairs, and is used in a way similar to HTTP headers. Some metadata is system-defined, some are significant when serving HTTP content from buckets or CloudFront, and you can also define arbitrary metadata for your own use.
-	**S3 URIs:** Although often bucket and key names are provided in APIs individually, it’s also common practice to write an S3 location in the form 's3://bucket-name/path/to/key' (where the key here is 'path/to/key'). (You’ll also see 's3n://' and 's3a://' prefixes [in Hadoop systems](https://wiki.apache.org/hadoop/AmazonS3).)
-	**S3 vs Glacier, EBS, and EFS:** AWS offers many storage services, and several besides S3 offer file-type abstractions. [Glacier](#glacier) is for cheaper and infrequently accessed archival storage. [EBS](#ebs), unlike S3, allows random access to file contents via a traditional filesystem, but can only be attached to one EC2 instance at a time. [EFS](#efs) is a network filesystem many instances can connect to, but at higher cost. See the [comparison table](#storage-durability-availability-and-price).

### S3 Tips

-	For most practical purposes, you can consider S3 capacity unlimited, both in total size of files and number of objects. The number of objects in a bucket is essentially also unlimited. Customers routinely have millions of objects.
-   ❗**Permissions:**
    -   🔸If you're storing business data on Amazon S3, it’s important to manage permissions sensibly. In 2017 companies like [Dow Jones and Verizon](http://www.techrepublic.com/article/massive-amazon-s3-breaches-highlight-blind-spots-in-enterprise-race-to-the-cloud/) saw data breaches due to poorly-chosen S3 configuration for sensitive data. Fixing this later can be a difficult task if you have a lot of assets and internal users.
    -   🔸There are 3 different ways to grant permissions to access Amazon S3 content in your buckets.
        + **IAM policies** use the familiar [Identity and Authentication Management](#security-and-iam) permission scheme to control access to specific operations.
        + **Bucket policies** grant or deny permissions to an entire bucket. You might use this when hosting a website in S3, to make the bucket publicly readable, or to restrict access to a bucket by IP address. Amazon's [sample bucket policies](http://docs.aws.amazon.com/AmazonS3/latest/dev/example-bucket-policies.html) show a number of use cases where these policies come in handy.
        + **[Access Control Lists](http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html)** (ACLs) can also be applied to every bucket and object stored in S3. ACLs grant additional permissions beyond those specified in IAM or bucket policies. ACLs can be used to grant access to another AWS user, or to predefined groups like the general public. This is powerful but can be dangerous, because you need to inspect every object to see who has access.
    -   🔸AWS' [predefined access control groups](http://docs.aws.amazon.com/AmazonS3/latest/dev/acl-overview.html#specifying-grantee-predefined-groups)use names which may not match allow access that may not be what you'd expect from their names:
        +   **"All Users" grants permission to the general public**, not only to users defined in your own AWS account. If an object is available to All Users, then it can be retrieved with a simple HTTP request of the form `http://s3.amazonaws.com/bucket-name/filename`. No authorization or signature is required to access data in this category.
        +   **"Authenticated Users" grants permissions to anyone with an AWS account**, again not limited to your own users. Because anyone can sign up for AWS, for all intents and purposes **this is also open to the general public**.
            + A typical use case of this ACL is used in conjunction with the [requester pays](http://docs.aws.amazon.com/AmazonS3/latest/dev/RequesterPaysBuckets.html) functionality of S3.
    -   🐥In August 2017, AWS added [AWS Config rules to ensure your S3 buckets are secure](https://aws.amazon.com/blogs/aws/aws-config-update-new-managed-rules-to-secure-s3-buckets/).
        +    ❗These AWS Config rules only check the security of your bucket policy and bucket-level ACLs. You can still create object ACLs that grant additional permissions, including opening files to the whole world.
    -   🔹Do create new buckets if you have different types of data with different sensitivity levels. This is much less error prone than complex permissions rules. For example, if data is for administrators only, like log data, put it in a new bucket that only administrators can access.
    -   For more guidance, see:
        +   [How to Secure an Amazon S3 Bucket](https://read.acloud.guru/how-to-secure-an-s3-bucket-7e2dbd34e81b)
        +   [Deep dive into S3 access controls](https://labs.detectify.com/2017/07/13/a-deep-dive-into-aws-s3-access-controls-taking-full-control-over-your-assets/).
        +   [How do S3 permissions work?](https://brandonwamboldt.ca/understanding-s3-permissions-1662/).
-	**Bucket naming:** Buckets are chosen from a global namespace (across all regions, even though S3 itself stores data in [whichever S3 region](https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region) you select), so you’ll find many bucket names are already taken. Creating a bucket means taking ownership of the name until you delete it. Bucket names have [a few restrictions](https://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html) on them.
	-	Bucket names can be used as part of the hostname when accessing the bucket or its contents, like `<bucket_name>.s3-us-east-1.amazonaws.com`, as long as the name is [DNS compliant](http://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html).
	-	A common practice is to use the company name acronym or abbreviation to prefix (or suffix, if you prefer DNS-style hierarchy) all bucket names (but please, don’t use a check on this as a security measure — this is highly insecure and easily circumvented!).
	-	🔸Bucket names with '.' (periods) in them [can cause certificate mismatches](https://forums.aws.amazon.com/thread.jspa?threadID=169951) when used with SSL. Use '-' instead, since this then conforms with both SSL expectations and is DNS compliant.
-	**Versioning:** S3 has [optional versioning support](https://docs.aws.amazon.com/AmazonS3/latest/dev/ObjectVersioning.html), so that all versions of objects are preserved on a bucket. This is mostly useful if you want an archive of changes or the ability to back out mistakes (caution: it lacks the featureset of full version control systems like Git).
-	**Durability:** Durability of S3 is extremely high, since internally it keeps several replicas. If you don’t delete it by accident, you can count on S3 not losing your data. (AWS offers the seemingly improbable durability rate of [99.999999999%](https://aws.amazon.com/s3/faqs/#How_durable_is_Amazon_S3), but this is a mathematical calculation based on independent failure rates and levels of replication — not a true probability estimate. Either way, S3 has had [a very good record](https://www.quora.com/Has-Amazon-S3-ever-lost-data-permanently) of durability.) Note this is *much* higher durability than EBS!
-	💸**S3 pricing** depends on [storage, requests, and transfer](https://aws.amazon.com/s3/pricing/).
	-	For transfer, putting data into AWS is free, but you’ll pay on the way out. Transfer from S3 to EC2 in the *same region* is free. Transfer to other regions or the Internet in general is not free.
	-	Deletes are free.
-	**S3 Reduced Redundancy and Infrequent Access:** Most people use the Standard storage class in S3, but there are other storage classes with lower cost:
	-	🔸[Reduced Redundancy Storage (RRS)](https://aws.amazon.com/s3/reduced-redundancy/) has been [effectively deprecated](https://www.quinnadvisory.com/blog/2017/4/13/reduced-redundancy-s3-is-dead), and has lower durability (99.99%, so just four nines) than standard S3. Note that it no longer participates in S3 price reductions, so it offers worse redundancy for more money than standard S3. As a result, there's no reason to use it.
	-	[Infrequent Access (IA)](https://aws.amazon.com/s3/storage-classes/#Infrequent_Access) lets you get cheaper storage in exchange for more expensive access. This is great for archives like logs you already processed, but might want to look at later. To get an idea of the cost savings when using Infrequent Access (IA), you can use this [S3 Infrequent Access Calculator](http://www.gulamshakir.com/apps/s3calc/index.html).
	-	[Glacier](#glacier) is a third alternative discussed as a separate product.
	-	See [the comparison table](#storage-durability-availability-and-price).
-	⏱**Performance:** Maximizing S3 performance means improving overall throughput in terms of bandwidth and number of operations per second.
	-	S3 is highly scalable, so in principle you can get arbitrarily high throughput. (A good example of this is [S3DistCp](https://docs.aws.amazon.com/ElasticMapReduce/latest/ReleaseGuide/UsingEMR_s3distcp.html).)
	-	But usually you are constrained by the pipe between the source and S3 and/or the level of concurrency of operations.
	-	Throughput is of course highest from within AWS to S3, and between EC2 instances and S3 buckets that are in the same region.
	-	Bandwidth from EC2 depends on instance type. See the “Network Performance” column at [ec2instances.info](http://www.ec2instances.info/).
	-	Throughput of many objects is extremely high when data is accessed in a distributed way, from many EC2 instances. It’s possible to read or write objects from S3 from hundreds or thousands of instances at once.
	-	However, throughput is very limited when objects accessed sequentially from a single instance. Individual operations take many milliseconds, and bandwidth to and from instances is limited.
	-	Therefore, to perform large numbers of operations, it’s necessary to use multiple worker threads and connections on individual instances, and for larger jobs, multiple EC2 instances as well.
	-	**Multi-part uploads:** For large objects you want to take advantage of the multi-part uploading capabilities (starting with minimum chunk sizes of 5 MB).
	-	**Large downloads:** Also you can download chunks of a single large object in parallel by exploiting the HTTP GET range-header capability.
	-	🔸**List pagination:** Listing contents happens at 1000 responses per request, so for buckets with many millions of objects listings will take time.
	-	❗**Key prefixes:** In addition, latency on operations is [highly dependent on prefix similarities among key names](http://docs.aws.amazon.com/AmazonS3/latest/dev/request-rate-perf-considerations.html). If you have need for high volumes of operations, it is essential to consider naming schemes with more randomness early in the key name (first 6 or 8 characters) in order to avoid “hot spots”.
		-	We list this as a major gotcha since it’s often painful to do large-scale renames.
		-	🔸Note that sadly, the advice about random key names goes against having a consistent layout with common prefixes to manage data lifecycles in an automated way.
	-	For data outside AWS, [**DirectConnect**](https://aws.amazon.com/directconnect/) and [**S3 Transfer Acceleration**](https://aws.amazon.com/blogs/aws/aws-storage-update-amazon-s3-transfer-acceleration-larger-snowballs-in-more-regions/) can help. For S3 Transfer Acceleration, you [pay](https://aws.amazon.com/s3/pricing/) about the equivalent of 1-2 months of storage for the transfer in either direction for using nearer endpoints.
-	**Command-line applications:** There are a few ways to use S3 from the command line:
	-	Originally, [**s3cmd**](https://github.com/s3tools/s3cmd) was the best tool for the job. It’s still used heavily by many.
	-	The regular [**aws**](https://aws.amazon.com/cli/) command-line interface now supports S3 well, and is useful for most situations.
	-	[**s4cmd**](https://github.com/bloomreach/s4cmd) is a replacement, with greater emphasis on performance via multi-threading, which is helpful for large files and large sets of files, and also offers Unix-like globbing support.
-	**GUI applications:** You may prefer a GUI, or wish to support GUI access for less technical users. Some options:
	-	The [AWS Console](https://aws.amazon.com/console/) does offer a graphical way to use S3. Use caution telling non-technical people to use it, however, since without tight permissions, it offers access to many other AWS features.
	-	[Transmit](https://panic.com/transmit/) is a good option on macOS for most use cases.
	-	[Cyberduck](https://cyberduck.io/) is a good option on macOS and Windows with support for multipart uploads, ACLs, versioning, lifecycle configuration, storage classes and server side encryption (SSE-S3 and SSE-KMS).
-	**S3 and CloudFront:** S3 is tightly integrated with the CloudFront CDN. See the CloudFront section for more information, as well as [S3 transfer acceleration](https://docs.aws.amazon.com/AmazonS3/latest/dev/transfer-acceleration.html).
-	**Static website hosting:**
	-	S3 has a [static website hosting option](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteHosting.html) that is simply a setting that enables configurable HTTP index and error pages and [HTTP redirect support](http://docs.aws.amazon.com/AmazonS3/latest/dev/how-to-page-redirect.html) to [public content](http://docs.aws.amazon.com/AmazonS3/latest/dev/WebsiteAccessPermissionsReqd.html) in S3. It’s a simple way to host static assets or a fully static website.
	-	Consider using CloudFront in front of most or all assets:
		-	Like any CDN, CloudFront improves performance significantly.
		-	🔸SSL is only supported on the built-in amazonaws.com domain for S3. S3 supports serving these sites through a [custom domain](http://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html), but [not over SSL on a custom domain](http://stackoverflow.com/questions/11201316/how-to-configure-ssl-for-amazon-s3-bucket). However, [CloudFront allows you to serve a custom domain over https](http://docs.aws.amazon.com/acm/latest/userguide/gs-cf.html). Amazon provides free SNI SSL/TLS certificates via Amazon Certificate Manager. [SNI does not work on very outdated browsers/operating systems](https://en.wikipedia.org/wiki/Server_Name_Indication#Support). Alternatively, you can provide your own certificate to use on CloudFront to support all browsers/operating systems for a fee.
		-	🔸If you are including resources across domains, such as fonts inside CSS files, you may need to [configure CORS](https://docs.aws.amazon.com/AmazonS3/latest/dev/cors.html) for the bucket serving those resources.
		-	Since pretty much everything is moving to SSL nowadays, and you likely want control over the domain, you probably want to set up CloudFront with your own certificate in front of S3 (and to ignore the [AWS example on this](http://docs.aws.amazon.com/AmazonS3/latest/dev/website-hosting-custom-domain-walkthrough.html) as it is non-SSL only).
		-	That said, if you do, you’ll need to think through invalidation or updates on CloudFront. You may wish to [include versions or hashes in filenames](https://abhishek-tiwari.com/post/CloudFront-design-patterns-and-best-practices) so invalidation is not necessary.
-	**Data lifecycles:**
	-	When managing data, the understanding the lifecycle of the data is as important as understanding the data itself. When putting data into a bucket, think about its lifecycle — its end of life, not just its beginning.
	-	🔹In general, data with different expiration policies should be stored under separate prefixes at the top level. For example, some voluminous logs might need to be deleted automatically monthly, while other data is critical and should never be deleted. Having the former in a separate bucket or at least a separate folder is wise.
	-	🔸Thinking about this up front will save you pain. It’s very hard to clean up large collections of files created by many engineers with varying lifecycles and no coherent organization.
	-	Alternatively you can set a lifecycle policy to archive old data to Glacier. [Be careful](https://alestic.com/2012/12/s3-glacier-costs/) with archiving large numbers of small objects to Glacier, since it may actually cost more.
	-	There is also a storage class called [**Infrequent Access**](https://aws.amazon.com/s3/storage-classes/#Infrequent_Access) that has the same durability as Standard S3, but is discounted per GB. It is suitable for objects that are infrequently accessed.
-	**Data consistency:** Understanding [data consistency](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html#ConsistencyModel) is critical for any use of S3 where there are multiple producers and consumers of data.
	-	Creation and updates to individual objects in S3 are **atomic**, in that you’ll never upload a new object or change an object and have another client see only part half the change.
	- The uncertainty lies with *when* your clients and other clients see updates.
	-	**New objects:** If you create a new object, you’ll be able to read it instantly, which is called **read-after-write consistency**.
		-	Well, with the additional caveat that if you do a read on an object before it exists, then create it, [you get eventual consistency](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html#ConsistencyModel) (not read-after-write).
		-	This does not apply to any list operations; newly created objects are [not guaranteed to appear in a list operation right away](https://docs.aws.amazon.com/AmazonS3/latest/dev/Introduction.html#ConsistencyModel)
	-	**Updates to objects:** If you overwrite or delete an object, you’re only guaranteed **eventual consistency**, i.e. the change will happen but you have no guarantee of when.
	- 🔹For many use cases, treating S3 objects as **immutable** (i.e. deciding by convention they will be created or deleted but not updated) can greatly simplify the code that uses them, avoiding complex state management.
	-	🔹Note that [until 2015](https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/), 'us-standard' region had had a weaker eventual consistency model, and the other (newer) regions were read-after-write. This was finally corrected — but watch for many old blogs mentioning this!
	-	**Slow updates:** In practice, “eventual consistency” usually means within seconds, but expect rare cases of minutes or [hours](http://www.stackdriver.com/eventual-consistency-really-eventual/).
-	**S3 as a filesystem:**
	-	In general S3’s APIs have inherent limitations that make S3 hard to use directly as a POSIX-style filesystem while still preserving S3’s own object format. For example, appending to a file requires rewriting, which cripples performance, and atomic rename of directories, mutual exclusion on opening files, and hardlinks are impossible.
	-	[s3fs](https://github.com/s3fs-fuse/s3fs-fuse) is a FUSE filesystem that goes ahead and tries anyway, but it has performance limitations and surprises for these reasons.
	-	[Riofs](https://github.com/skoobe/riofs) (C) and [Goofys](https://github.com/kahing/goofys) (Go) are more recent efforts that attempt adopt a different data storage format to address those issues, and so are likely improvements on s3fs.
	-	[S3QL](https://github.com/s3ql/s3ql) ([discussion](https://news.ycombinator.com/item?id=10150684)) is a Python implementation that offers data de-duplication, snap-shotting, and encryption, but only one client at a time.
	-	[ObjectiveFS](https://objectivefs.com/) ([discussion](https://news.ycombinator.com/item?id=10117506)) is a commercial solution that supports filesystem features and concurrent clients.
-	If you are primarily using a VPC, consider setting up a [VPC Endpoint](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-endpoints.html) for S3 in order to allow your VPC-hosted resources to easily access it without the need for extra network configuration or hops.
-	**Cross-region replication:** S3 has [a feature](https://docs.aws.amazon.com/AmazonS3/latest/dev/crr.html) for replicating a bucket between one region and another. Note that S3 is already highly replicated within one region, so usually this isn’t necessary for durability, but it could be useful for compliance (geographically distributed data storage), lower latency, or as a strategy to reduce region-to-region bandwidth costs by mirroring heavily used data in a second region.
-	**IPv4 vs IPv6:** For a long time S3 only supported IPv4 at the default endpoint `https://BUCKET.s3.amazonaws.com`. However, [as of Aug 11, 2016](https://aws.amazon.com/blogs/aws/now-available-ipv6-support-for-amazon-s3/) it now supports both IPv4 & IPv6! To use both, you have to [enable dualstack](http://docs.aws.amazon.com/AmazonS3/latest/dev/dual-stack-endpoints.html) either in your preferred API client or by directly using this url scheme `https://BUCKET.s3.dualstack.REGION.amazonaws.com`. This extends to S3 Transfer Acceleration as well.
-	**S3 event notifications:** S3 can be configured to send an [SNS notification](https://aws.amazon.com/blogs/aws/introducing-the-amazon-simple-notification-service/), [SQS message](http://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/Welcome.html), or [AWS Lambda function](http://docs.aws.amazon.com/lambda/latest/dg/welcome.html) on [bucket events](http://docs.aws.amazon.com/AmazonS3/latest/dev/NotificationHowTo.html).
-   💸Limit your individual users (or IAM roles) to the minimal required S3 locations, and catalog the “approved” locations. Otherwise, S3 tends to become the dumping ground where people put data to random locations that are not cleaned up for years, costing you big bucks.

### S3 Gotchas and Limitations

-	🔸For many years, there was a notorious [**100-bucket limit**](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html#limits_s3) per account, which could not be raised and caused many companies significant pain. As of 2015, you can [request increases](https://aws.amazon.com/about-aws/whats-new/2015/08/amazon-s3-introduces-new-usability-enhancements/). You can ask to increase the limit, but it will still be capped (generally below ~1000 per account).
-	🔸Be careful not to make implicit assumptions about transactionality or sequencing of updates to objects. Never assume that if you modify a sequence of objects, the clients will see the same modifications in the same sequence, or if you upload a whole bunch of files, that they will all appear at once to all clients.
-	🔸S3 has an [**SLA**](https://aws.amazon.com/s3/sla/) with 99.9% uptime. If you use S3 heavily, you’ll inevitably see occasional error accessing or storing data as disks or other infrastructure fail. Availability is usually restored in seconds or minutes. Although availability is not extremely high, as mentioned above, durability is excellent.
-	🔸After uploading, any change that you make to the object causes a full rewrite of the object, so avoid appending-like behavior with regular files.
-	🔸Eventual data consistency, as discussed above, can be surprising sometimes. If S3 suffers from internal replication issues, an object may be visible from a subset of the machines, depending on which S3 endpoint they hit. Those usually resolve within seconds; however, we’ve seen isolated cases when the issue lingered for 20-30 hours.
-	🔸**MD5s and multi-part uploads:** In S3, the [ETag header in S3](http://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonResponseHeaders.html) is a hash on the object. And in many cases, it is the MD5 hash. However, this [is not the case in general](http://stackoverflow.com/questions/12186993/what-is-the-algorithm-to-compute-the-amazon-s3-etag-for-a-file-larger-than-5gb) when you use multi-part uploads. One workaround is to compute MD5s yourself and put them in a custom header (such as is done by [s4cmd](https://github.com/bloomreach/s4cmd)).
-	🔸**Incomplete multi-part upload costs:** Incomplete multi-part uploads accrue [storage charges](http://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html#mpuploadpricing) even if the upload fails and no S3 object is created. [Amazon](http://docs.aws.amazon.com/AmazonS3/latest/dev/mpuoverview.html#mpu-abort-incomplete-mpu-lifecycle-config) ([and](http://www.deplication.net/2016/06/aws-tip-save-s3-costs-with-abort.html) [others](https://www.sumologic.com/aws/s3/s3-cost-optimization/)) recommend using a lifecycle policy to clean up incomplete uploads and save on storage costs. Note that if you have many of these, it may be worth investigating whatever's failing regularly. 
-	🔸**US Standard region:** Previously, the us-east-1 region (also known as the US Standard region) was replicated across coasts, which led to greater variability of latency. Effective Jun 19, 2015 this is [no longer the case](https://forums.aws.amazon.com/ann.jspa?annID=3112). All Amazon S3 regions now support read-after-write consistency. Amazon S3 also renamed the US Standard region to the US East (N. Virginia) region to be consistent with AWS regional naming conventions.
- 🔸**S3 authentication versions and regions:** In newer regions, S3 [only supports the latest authentication](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingAWSSDK.html#specify-signature-version). If an S3 file operation using CLI or SDK doesn't work in one region, but works correctly in another region, make sure you are using the latest [authentication signature](https://docs.aws.amazon.com/AmazonS3/latest/API/sig-v4-authenticating-requests.html).

### Storage Durability, Availability, and Price

As an illustration of comparative features and price, the table below gives S3 Standard, RRS, IA, in comparison with [Glacier](#glacier), [EBS](#ebs), [EFS](#efs), and EC2 d2.xlarge instance store using **Virginia region** as of **Sept 2017**.

|                 | Durability (per year)  | Availability “designed” | Availability SLA | Storage (per TB per month)                                                                                               | GET or retrieve (per million) | Write or archive (per million) |
|-----------------|------------------------|-------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------|--------------------------------|
| **Glacier**     | Eleven 9s              | Sloooow                 | –                | $4                                                                                                                       | $50                           | $50                            |
| **S3 IA**       | Eleven 9s              | 99.9%                   | **99%**          | $12.50                                                                                                                   | $1                            | $10                            |
| ~~**S3 RRS**~~      | ~~**99.99%**~~             | ~~99.99%~~                  | ~~99.9%~~            | ~~$24 (first TB)~~                                                                                                                      | ~~$0.40~~                         | ~~$5~~                             |
| **S3 Standard** | Eleven 9s              | 99.99%                  | 99.9%            | $23                                                                                                                     | $0.40                         | $5                             |
| **EBS**         | **99.8%**              | Unstated                | 99.99%           | $25/$45/**$100**/$125+ ([sc1/st1/**gp2**/io1](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EBSVolumeTypes.html)\) |                               |                                |
| **EFS**         | “High”                 | “High”                  | –                | $300                                                                                                                     |                               |                                |
| **EC2 d2.xlarge instance store**  | Unstated | Unstated                | –                | $25.44                                                                                                                   | $0                            | $0                             |

Especially notable items are in **boldface**. Sources: [S3 pricing](https://aws.amazon.com/s3/pricing/), [S3 SLA](https://aws.amazon.com/s3/sla/), [S3 FAQ](https://aws.amazon.com/s3/faqs/), [RRS info](https://aws.amazon.com/s3/reduced-redundancy/) (note that this is considered deprecated), [Glacier pricing](https://aws.amazon.com/glacier/pricing/), [EBS availability and durability](https://aws.amazon.com/ebs/details/#Amazon_EBS_Availability_and_Durability), [EBS pricing](https://aws.amazon.com/ebs/pricing/), [EFS pricing](https://aws.amazon.com/efs/pricing/), [EC2 SLA](https://aws.amazon.com/ec2/sla/)

EC2
---

### EC2 Basics

-	📒 [Homepage](https://aws.amazon.com/ec2/) ∙ [Documentation](https://aws.amazon.com/documentation/ec2/) ∙ [FAQ](https://aws.amazon.com/ec2/faqs/) ∙ [Pricing](https://aws.amazon.com/ec2/pricing/) (see also [ec2instances.info](http://www.ec2instances.info/)\)
-	**EC2** (Elastic Compute Cloud) is AWS’ offering of the most fundamental piece of cloud computing: A [virtual private server](https://en.wikipedia.org/wiki/Virtual_private_server). These “instances” can run [most Linux, BSD, and Windows operating systems](https://aws.amazon.com/ec2/faqs/#What_operating_system_environments_are_supported). Internally, they've used a heavily modified[Xen](https://en.wikipedia.org/wiki/Xen) virtualization. That said, new instance classes are being introduced with a KVM derived hypervisor instead, called [Nitro](http://www.brendangregg.com/blog/2017-11-29/aws-ec2-virtualization-2017.html). So far, this is limited to the C5 and M5 instance types. Lastly, there's a "bare metal hypervisor" available for [i3.metal instances](https://aws.amazon.com/blogs/aws/new-amazon-ec2-bare-metal-instances-with-direct-access-to-hardware/) in a limited preview.
-	The term “EC2” is sometimes used to refer to the servers themselves, but technically refers more broadly to a whole collection of supporting services, too, like load balancing (CLBs/ALBs/NLBs), IP addresses (EIPs), bootable images (AMIs), security groups, and network drives (EBS) (which we discuss individually in this guide).
-	💸**[EC2 pricing](https://aws.amazon.com/ec2/pricing/)** and **[cost management](#ec2-cost-management)** is a complicated topic. It can range from free (on the [AWS free tier](https://aws.amazon.com/free/)) to a lot, depending on your usage. Pricing is by instance type, by second or hour, and changes depending on AWS region and whether you are purchasing your instances [On-Demand](https://aws.amazon.com/ec2/pricing/on-demand/), on the [Spot market](https://aws.amazon.com/ec2/spot/) or pre-purchasing ([Reserved Instances](https://aws.amazon.com/ec2/pricing/reserved-instances/)).
- **Network Performance:** For some instance types, AWS uses general terms like Low, Medium, and High to refer to network performance. Users have done [benchmarking](http://stackoverflow.com/questions/18507405/ec2-instance-typess-exact-network-performance) to provide expectations for what these terms can mean.

### EC2 Alternatives and Lock-In

-	Running EC2 is akin to running a set of physical servers, as long as you don’t do automatic scaling or tooled cluster setup. If you just run a set of static instances, migrating to another VPS or dedicated server provider should not be too hard.
-	🚪**Alternatives to EC2:** The direct alternatives are Google Cloud, Microsoft Azure, Rackspace, DigitalOcean, AWS's own Lightsail offering, and other VPS providers, some of which offer similar APIs for setting up and removing instances. (See the comparisons [above](#when-to-use-aws).)
-	**Should you use Amazon Linux?** AWS encourages use of their own [Amazon Linux](https://aws.amazon.com/amazon-linux-ami/), which is evolved from [Red Hat Enterprise Linux (RHEL)](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) and [CentOS](https://en.wikipedia.org/wiki/CentOS). It’s used by many, but [others are skeptical](https://www.exratione.com/2014/08/do-not-use-amazon-linux/). Whatever you do, think this decision through carefully. It’s true Amazon Linux is heavily tested and better supported in the unlikely event you have deeper issues with OS and virtualization on EC2. But in general, many companies do just fine using a standard, non-Amazon Linux distribution, such as Ubuntu or CentOS. Using a standard Linux distribution means you have an exactly replicable environment should you use another hosting provider instead of (or in addition to) AWS. It’s also helpful if you wish to test deployments on local developer machines running the same standard Linux distribution (a practice that’s getting more common with Docker, too. Amazon now supports an official [Amazon Linux Docker image](http://docs.aws.amazon.com/AmazonECR/latest/userguide/amazon_linux_container_image.html), aimed at assisting with local development on a comparable environment, though this is new enough that it should be considered experimental).
-	**EC2 costs:** See the [section on this](#ec2-cost-management).

### EC2 Tips

-	🔹**Picking regions:** When you first set up, consider which [regions](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html#concepts-available-regions) you want to use first. Many people in North America just automatically set up in the us-east-1 (N. Virginia) region, which is the default, but it’s worth considering if this is best up front. You'll want to evaluate service availability (some services [are not available in all regions](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/)), costing (baseline costs also [vary by region](https://aws.amazon.com/ec2/pricing/) by up to 10-30% (generally lowest in us-east-1 for comparison purposes)), and compliance (various countries have differing regulations with regard to data privacy, for example).
-	**Instance types:** EC2 instances come in many types, corresponding to the capabilities of the virtual machine in CPU architecture and speed, RAM, disk sizes and types (SSD or magnetic), and network bandwidth.
	-	Selecting instance types is complex since there are so many types. Additionally there are different generations, released [over the years](https://aws.amazon.com/blogs/aws/ec2-instance-history/).
	-	🔹Use the list at [**ec2instances.info**](http://www.ec2instances.info/) to review costs and features. [Amazon’s own list](https://aws.amazon.com/ec2/instance-types/) of instance types is hard to use, and doesn’t list features and price together, which makes it doubly difficult.
	-	Prices vary a lot, so use [**ec2instances.info**](http://www.ec2instances.info/) to determine the set of machines that meet your needs and [**ec2price.com**](http://ec2price.com/) to find the cheapest type in the region you’re working in. Depending on the timing and region, it might be much cheaper to rent an instance with *more* memory or CPU than the bare minimum.
  - **Turn off** your instances when they aren’t in use. For many situations such as testing or staging resources, you may not need your instances on 24/7, and you won’t need to pay EC2 running costs when they are suspended. Given that costs are calculated based on usage, this is a simple mechanism for cost savings. This can be achieved using [Lambda and CloudWatch](https://aws.amazon.com/premiumsupport/knowledge-center/start-stop-lambda-cloudwatch/), an open source option like [cloudcycler](https://github.com/fairfaxmedia/cloudcycler), or a SaaS provider like [GorillaStack](https://www.gorillastack.com). (Note: if you turn off instances with an ephemeral root volume, any state will be lost when the instance is turned off. Therefore, for stateful applications it is safer to turn off EBS backed instances).
-	[**Dedicated instances**](https://aws.amazon.com/ec2/purchasing-options/dedicated-instances/) and [**dedicated hosts**](https://aws.amazon.com/ec2/dedicated-hosts/) are assigned hardware, instead of usual virtual instances. They are more expensive than virtual instances but [can be preferable](https://aws.amazon.com/ec2/dedicated-hosts/) for performance, compliance, financial modeling, or licensing reasons.
-	**32 bit vs 64 bit:** A few micro, small, and medium instances are still available to use as 32-bit architecture. You’ll be using 64-bit EC2 (“amd64”) instances nowadays, though smaller instances still support 32 bit (“i386”). Use 64 bit unless you have legacy constraints or other good reasons to use 32.
-	**HVM vs PV:** There are two kinds of virtualization technology used by EC2, [hardware virtual machine (HVM) and paravirtual (PV)](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/virtualization_types.html). Historically, PV was the usual type, but [now HVM is becoming the standard](https://www.opswat.com/blog/aws-2015-why-you-need-switch-pv-hvm). If you want to use the newest instance types, you must use HVM. See the [instance type matrix](https://aws.amazon.com/amazon-linux-ami/instance-type-matrix/) for details.
-	**Operating system:** To use EC2, you’ll need to pick a base operating system. It can be Windows or Linux, such as Ubuntu or [Amazon Linux](https://aws.amazon.com/amazon-linux-ami/). You do this with AMIs, which are covered in more detail in their own section below.
-	**Limits:** You can’t create arbitrary numbers of instances. Default limits on numbers of EC2 instances per account vary by instance type, as described in [this list](http://aws.amazon.com/ec2/faqs/#How_many_instances_can_I_run_in_Amazon_EC2).
-	❗**Use termination protection:** For any instances that are important and long-lived (in particular, aren't part of auto-scaling), [enable termination protection](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/terminating-instances.html#Using_ChangingDisableAPITermination). This is an important line of defense against user mistakes, such as accidentally terminating many instances instead of just one due to human error.
-	**SSH key management:**
	-	When you start an instance, you need to have at least one [ssh key pair](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) set up, to bootstrap, i.e., allow you to ssh in the first time.
	-	Aside from bootstrapping, you should manage keys yourself on the instances, assigning individual keys to individual users or services as appropriate.
	-	Avoid reusing the original boot keys except by administrators when creating new instances.
	-	Avoid sharing keys and [add individual ssh keys](http://security.stackexchange.com/questions/87480/managing-multiple-ssh-private-keys-for-a-team) for individual users.
-	**GPU support:** You can rent GPU-enabled instances on EC2 for use in machine learning or graphics rendering workloads.

	-	There are [three generations](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using_cluster_computing.html) of GPU-enabled instances available:
		- Third generation P2 series offers NVIDIA K80 GPUs in 1, 8 and 16 GPU configurations targeting machine learning and scientific workloads.
		- Second generation G2 series offers NVIDIA K520 GPUs in 1 or 4 GPU configurations targeting graphics and video encoding.
		- First generation CG1 instances are still available in some regions in a single configuration with a NVIDIA M2050 GPU.
	-	⛓ AWS offers an [AMI](https://aws.amazon.com/marketplace/pp/B01M0AXXQB?qid=1475211685369&sr=0-1&ref_=srh_res_product_title) (based on Amazon Linux) with most NVIDIA drivers and ancillary software (CUDA, CUBLAS, CuDNN, TensorFlow) installed to lower the barrier to usage. Note, however, that this leads to lock-in due to Amazon Linux and the fact that you have no direct access to software configuration or versioning.
	-	🔹As with any expensive EC2 instance types, [Spot instances can offer significant savings](#ec2-cost-management) with GPU workloads when interruptions are tolerable.
- All current EC2 instance types can take advantage of IPv6 addressing, so long as they are launched in a subnet with an allocated CIDR range in an IPv6-enabled VPC.

### EC2 Gotchas and Limitations

-	❗Never use ssh passwords. Just don’t do it; they are too insecure, and consequences of compromise too severe. Use keys instead. [Read up on this](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2) and fully disable ssh password access to your ssh server by making sure 'PasswordAuthentication no' is in your /etc/ssh/sshd_config file. If you’re careful about managing ssh private keys everywhere they are stored, it is a major improvement on security over password-based authentication.
-	🔸For all [newer instance types](https://aws.amazon.com/amazon-linux-ami/instance-type-matrix/), when selecting the AMI to use, be sure you select the HVM AMI, or it just won’t work.
-	❗When creating an instance and using a new ssh key pair, [make sure the ssh key permissions are correct](http://stackoverflow.com/questions/1454629/aws-ssh-access-permission-denied-publickey-issue).
-	🔸Sometimes certain EC2 instances can get scheduled for retirement by AWS due to “detected degradation of the underlying hardware,” in which case you are given a couple of weeks to migrate to a new instance
 	-	If your instance root device is an EBS volume, you can typically stop and then start the instance which moves it to healthy host hardware, giving you control over timing of this event. Note however that you will lose any instance store volume data ([ephemeral drives](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/InstanceStorage.html)) if your instance type has instance store volumes.
 	-	The instance public IP (if it has one) will likely change unless you're using Elastic IPs. This could be a problem if other systems depend on the IP address.
-	🔸Periodically you may find that your server or load balancer is receiving traffic for (presumably) a previous EC2 server that was running at the same IP address that you are handed out now (this may not matter, or it can be fixed by migrating to another new instance).
-	❗If the EC2 API itself is a critical dependency of your infrastructure (e.g. for automated server replacement, custom scaling algorithms, etc.) and you are running at a large scale or making many EC2 API calls, make sure that you understand when they might fail (calls to it are [rate limited](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/query-api-troubleshooting.html#api-request-rate) and the limits are not published and subject to change) and code and test against that possibility.
-	❗Many newer EC2 instance types are EBS-only. Make sure to factor in EBS performance and costs when planning to use them.
-	❗⏱ Instances come in two types: **Fixed Performance Instances** (e.g. M3, C3, and R3) and [**Burstable Performance Instances**](https://aws.amazon.com/ec2/instance-types/#burst) (e.g. T2). A T2 instance receives CPU credits continuously, the rate of which depends on the instance size. T2 instances accrue CPU credits when they are idle, and use CPU credits when they are active. However, once an instance runs out of credits, you'll notice a severe degradation in performance. If you need consistently high CPU performance for applications such as video encoding, high volume websites or HPC applications, it is recommended to use Fixed Performance Instances.
-	Instance user-data is [limited to 16 KB](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html#instancedata-add-user-data). (This limit applies to the data in raw form, not base64-encoded form.) If more data is needed, it can be downloaded from S3 by a user-data script.
-	Very new accounts may not be able to launch some instance types, such as GPU instances, because of an initially imposed “soft limit” of zero. This limit can be raised by making a support request. See [AWS Service Limits](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) for the method to make the support request. Note that this limit of zero is [not currently documented](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html#limits_ec2).

CloudWatch
-------------------

### CloudWatch Basics

* 📒  [Homepage](https://aws.amazon.com/cloudwatch/) ∙ [Documentation](https://aws.amazon.com/documentation/cloudwatch/) ∙ [FAQ](https://aws.amazon.com/cloudwatch/faqs/) ∙ [Pricing](https://aws.amazon.com/cloudwatch/pricing/)
* **CloudWatch** monitors resources and applications, captures logs, and sends events.
* CloudWatch monitoring is the standard mechanism for keeping tabs on AWS resources. A wide range of  [**metrics and dimensions**](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CW_Support_For_AWS.html) are available via CloudWatch, allowing you to create time based graphs, **[alarms](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html)**, and **[dashboards](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Dashboards.html)**.
    * Alarms are the most practical use of CloudWatch, allowing you to trigger notifications from any given metric.
    * Alarms can trigger [SNS notifications](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ConsoleAlarms.html), [Auto Scaling actions](http://docs.aws.amazon.com/autoscaling/latest/userguide/policy_creating.html), or [EC2 actions](http://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/UsingAlarmActions.html).
    * Publish and share graphs of metrics by creating [customizable dashboard views](https://aws.amazon.com/blogs/aws/cloudwatch-dashboards-create-use-customized-metrics-views/).
		* Monitor and report on EC2 [instance system check failure alarms](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/monitoring-system-instance-status-check.html#creating_status_check_alarms).
* **Using CloudWatch Events:**
    * Events create a mechanism to automate actions in various services on AWS. You can create [event rules](http://docs.aws.amazon.com/AmazonCloudWatch/latest/events/EventTypes.html) from instance states, AWS APIs, Auto Scaling, Run commands, deployments or time-based schedules (think Cron).
    * [Triggered events](http://docs.aws.amazon.com/AmazonCloudWatch/latest/events/CWE_GettingStarted.html) can can invoke Lambda functions, send SNS/SQS/Kinesis messages, or perform instance actions (terminate, restart, stop, or snapshot volumes).
    * Custom payloads can be sent to targets in JSON format, this is especially useful when triggering Lambdas.
* **Using CloudWatch Logs:**
    * [CloudWatch Logs](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html) is a streaming log storage system. By storing logs within AWS you have access to unlimited paid storage, but you also have the option of streaming logs directly to ElasticSearch or custom Lambdas.
    * A [log agent installed](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/CWL_GettingStarted.html) on your servers will process logs over time and send them to CloudWatch Logs.
    * You can [export logged data to S3](http://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/S3Export.html) or stream results to other AWS services.
* **Detailed monitoring:** [Detailed monitoring](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-cloudwatch-new.html) for EC2 instances must be enabled to get granular metrics, and is [billed under CloudWatch](https://aws.amazon.com/cloudwatch/pricing/).

### CloudWatch Alternatives and Lock-In

* CloudWatch offers fairly basic functionality that doesn't create significant (additional) AWS lock-in. Most of the metrics provided by the service can be obtained through APIs that can be imported into other aggregation or visualization tools or services (many specifically provide CloudWatch data import services).
* 🚪 Alternatives to CloudWatch monitoring services include [NewRelic](http://newrelic.com/), [Datadog](http://datadog.com/), [Sumo Logic](http://sumologic.com/), [Zabbix](http://zabbix.com/), [Nagios](http://nagios.org/), [Ruxit](http://ruxit.com/), [Elastic Stack](https://www.elastic.co/v5), open source options such as [StatsD](https://github.com/etsy/statsd) or [collectd](https://collectd.org/) with [Graphite](https://graphiteapp.org/), and many others.
* 🚪 CloudWatch Log alternatives include [Splunk](http://splunk.com/), [Sumo Logic](http://sumologic.com/), [Loggly](http://loggly.com/), [Logstas
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc3NDY4Nzk2NF19
-->