# Azure question bank
 
### Q1. Difference between private endpoint and service endpoint!

Ans. The following definition of Azure Private Endpoint has been taken from Microsoft Azure documentation:

**"Azure Private Endpoint is a network interface that connects you privately and securely to a service powered by Azure Private Link. Private Endpoint uses a private IP address from your VNet, effectively bringing the service into your VNet. The service could be an Azure service such as Azure Storage, Azure Cosmos DB, SQL, etc. or your own Private Link Service."**

Private endpoint enables connectivity between the consumers from the same VNet, regionally peered VNets, globally peered VNets and on premises using VPN or Express Route and services powered by Private Link.

*The private endpoint must be deployed in the same region as the virtual network*.
<hr/>

### Q2. What is a proximity group and in what scenario it is used?

<hr/>

### Q3. Difference between application gateway and load balancer!

<hr/>

### Q4. How to define gates in Azure devops release pipeline?

<hr/>

### Q5. What kinds of poilicies are there in Azure APIM?

<hr/>

### Q6. When do Azure APIM policies execute?

<hr/>

### Q7. What sort of database migration challenges have you faced ever?

<hr/>

### Q8. What services could be known as Azure native?

<hr/>

### Q9. What is Shared Access Signature and how to generate it?

<hr/>

### Q10. Difference between NIC and NSG?

<hr/>

### Q11. Name any 5 functionalities which could be offloaded to a gateway in Azure!

Ans.
1. SSL termination
2. Client rate limit (throttling) - limit the number of hits by a client in a given time.
3. Web application firewall (WAF)
4. Authentication
5. IP allow/block list

few more:

6. Logging and monitoring
7. Servicing static content
8. Gzip compression

<hr/>

### Q12. How to set NSG rules through Terraform?

<hr/>

### Q13. What is Azure Web Application Firewall and how does it used with Applicaiton Gateway, Front Door and CDN?

<hr/>

### Q14. What is a WAF policy and to whom it can be associated?

<hr/>

### Q15. What is a Mutex Lock and how does it work?

<hr/>

### Q16. How Api gateway vs Front Door

<hr/>

### Q17. How do you decide to go with SQL Server vs CosmosDB

<hr/>

### Q18. What is CAP theorem?

Ans. CAP theorem is also called Brewer’s theorem, named after the computer scientist, Eric Brewer.
We need to understand the distibuted system as it is base requirement of CAP.

**
CAP theorem stands for:

Consistency
Availability
Partition tolerance
**

Consistency means all the users can see the same data at same time.

Availability means the system continues to operate even in the presence of node failure.

Partition tolerance means the system continues to operate in spite of network failures.

<hr/>

### Q19. What are the power states of an Azure Virtual Machine?

Ans. 
There are total 7 power states
1. Starting: Indicates that the VM is being started.
2. Running: Indicates that the VM is running.
3. Stopping: Indicates that the VM is being stopped.
4. Stopped: Indicates that the VM is stopped. Note that VMs in the stopped state still incur compute charges.
5. Deallocating: Indicates that the VM is being deallocated.
6. Deallocated: Indicates that the VM is completely removed from the hypervisor but still available in the control plane. VMs in the deallocated state do not incur compute charges.
7. Unknown (-): Indicates that the power state of the VM is unknown. 
   
<hr/>

### Q20. What is profiling in Azure?

Ans. 
Profiling is only a procedure for measuring the performance analysis of an application. It is normally done to guarantee that the application is sufficiently steady and can maintain overwhelming traffic. Visual Studio gives us different tools to do it by gathering the performance information from the application that likewise helps in troubleshooting issues. Once the profiling wizard is run, it sets up the execution session and collects the data of the sample. The profiling reports help in: Deciding the longest running strategies inside the application Measuring the execution time of every strategy in the call stack Assessing memory allocation.

<hr/>

### Q21. Which load balancer should we use in what scenario?

Ans.
<ul><li>If you are looking to do DNS based global routing and do not have requirements for Transport Layer Security (TLS) protocol termination ("SSL offload"), per-HTTP/HTTPS request or application-layer processing, review Traffic Manager.</li></ul>
<li>If you want to load balance between your servers in a region at the application layer, review Application Gateway.</li>
<li>If you need to optimize global routing of your web traffic and optimize top-tier end-user performance and reliability through quick global failover, see Front Door.</li>
Source: https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview 

<hr/>

### Q22. Can the region be changed of an existing Azure Web App?

Ans.
App Service resources are region-specific and can't be moved across regions. You must create a copy of your existing App Service resources in the target region, then move your content over to the new app. 

<hr/>

### Q23. How can we use custom SSL certificates in Azure Function/App service?


<hr/>

### Q24. What is the strategy would you use to save the cost for using virtual machines?

Ans.
Using Azure virtual machine reservations for long term. You can save upto 72% cost if you choose 3 years reservation.

For more information : [link](https://docs.microsoft.com/en-in/azure/cost-management-billing/manage/understand-vm-reservation-charges?toc=/azure/cost-management-billing/reservations/toc.json)

<hr/>

### Q25. Can I create a single .gitignore file for all the repositories on my computer?

Ans.
Yes, it is possible to add a global <code>.gitignore</code> file to define a list of rules for ignoring files in each Git repository on my computer.

Follow the steps: 
1. open the git bash
2. Configure the git to use exclude file ~/.gitignore_global 

<code>$ git config --global core.excludesfile ~/.gitignore_global </code>

<hr/>

### Explain monitoring and analytics types and mention the services under each category!

Ans.
Azure monitoring and analytics services can be classified into following 3 categories:
* Core monitoring
  * Azure Monitor
  * Azure Advisor
  * Service Health
  * Activity log
* Deep infrastructure monitoring
  * Log Analytics
  * Management Solutions
  * Service Map
  * Network Monotoring
* Deep application monitoring
  * Application Insights

