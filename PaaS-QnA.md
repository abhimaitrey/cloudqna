# Azure Platform as a Service (PaaS) Questions

### How can you use Key Vault in an Azure Web App service?

Ans.

### What are the key differences between Service Principal and Managed Identity? And which one would be recommended and why?

Ans.

### How does Application Gateway and Web Application Firewall works?

Ans.

### What is Active-Active and Active-Passive machenism and where do they use?

Ans.

### How to ensure high availabilty of Azure SQL Database and SQL Managed Instance?

Ans. Azure SQL Database and Azure SQL Managed Instance feature a built-in high availability solution, that is deeply integrated with the Azure platform. It is dependent on Service Fabric for failure detection and recovery, on Azure Blob storage for data protection, and on Availability Zones for higher fault tolerance (as mentioned earlier in document not applicable to Azure SQL Managed Instance yet). In addition, SQL Database and SQL Managed Instance leverage the Always On availability group technology from the SQL Server instance for replication and failover. The combination of these technologies enables applications to fully realize the benefits of a mixed storage model and support the most demanding SLAs.

https://docs.microsoft.com/en-us/azure/azure-sql/database/high-availability-sla
