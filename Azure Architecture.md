# 1. Azure Architecture Questions
- [1. Azure Architecture Questions](#1-azure-architecture-questions)
    - [1.0.1. Define cloud native!](#101-define-cloud-native)
    - [1.0.2. Explain cloud native foundational pillars!](#102-explain-cloud-native-foundational-pillars)
    - [1.0.3. What architecture would you recommend for a 3-tier or N-tier application?](#103-what-architecture-would-you-recommend-for-a-3-tier-or-n-tier-application)


### 1.0.1. Define cloud native!

Ans. The **Cloud Native Computing Foundation (CNCF)** provides an official definition:

*Cloud-native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach.

These techniques enable loosely coupled systems that are resilient, manageable, and observable. Combined with robust automation, they allow engineers to make high-impact changes frequently and predictably with minimal toil.*

Cloud native is about speed and agility.

### 1.0.2. Explain cloud native foundational pillars!

Ans. There are overall 6 cloud-native foundational pillars.
1. Cloud infrastructure - It is the a base for following 5 and would remain in center.
2. Modern design
3. Microservices
4. Containers
5. Backing Services
6. Automation

### 1.0.3. What architecture would you recommend for a 3-tier or N-tier application?

Ans. There is an architecture well defined in the Azure Docs. The architecture has considered the following factors:

1. Separation of resource groups so that the lifetime, ownership can be segregated.
2. Availability zones for high availability
3. Networking and load balancing:
   a. Vnet, Subnets, VMs
   b. Application Gateway
   c. Load balancer
   d. Network Security Groups
   e. DDos protection
   f. Azure DNS
   g. Cloud witness (storage account)
   h. SQL Server Always On availability group
   i. Jumpbox
   j. Azure AD Domain Service (AD DS)

   


https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/n-tier/n-tier-sql-server