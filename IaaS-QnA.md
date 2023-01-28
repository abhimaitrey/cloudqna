# Azure IaaS Questions

### How to assess the workload before migration on Azure?

Ans.

### Difference between Azure Firewall and NSG?

Ans. Azure Firewall and Network Security Group, both services are used for network security and can work great together. 

=> NSG can be associated with subnets | network interfaces, but not both at the same time.

=> Azure Firewall is managed service and it filters network and application level traffic.

=> NSG has least features than Firewall like the Firewall offers masking the source and destination network addresss, FQDN tags but NSG does not.

=> NSG works on OSI layers 3 and 4 but Firewall works on 3,4, and 7 layers


### What security tools can be used to protect to VNet?

Ans.

### How does AD and AAD integration happens?

Ans.

### Explain procedure to migrate VMWare and HyperV VMs to Azure?

Ans. 

### What tools do you use for migration to Azure?

Ans.

### What is Bastion Host and how does it work?

Ans.

### How do you decide server sizing while doing assessment?

Ans.

### What is Application Security Group and in which scenario it is used?

Ans.

### If there are Windows AD and Azure AD exist, which AD will you use for authentication?


### Can we record the ExpressRoute activities in Azure Monitor?

Ans. Yes, it is possible through ExpressRoute metrics withing the Express Route Circuit resource. There are 4 types of available matrics in ExpressRoute resource: 
1. Availability
2. Traffic
3. Performance
4. Physical Connectivity

### How to connect 2 VNets having the same CIDR address range?

Ans. There are 2 similar concepts, and I will address each one individually:

1) You can have VNETs with overlapping address space. You can make as many overlapping VNETS as you would like, and they can be in the same subscription and the same region. 

It is usually recommended not to because if you need the 2 VNETs to communicate via VNET Peering or S2S VPN, they cannot have overlapping address space. If the 2 VNETs will never need to interact in that way, they can have overlapping address space without an issue. 

2) Subnets cannot have overlapping address space within the VNET. In the example you gave above, both Subnets in both VNETs have the same address range - 10.0.1.0/24. 

A better way to design the address range in a VNET:

Vnet_A: 10.0.0.0/16   (10.0.0.0 - 10.0.255.255)
Subnet_a_1: 10.0.0.0/24  (10.0.0.0 - 10.0.0.255)

Subnet_a_2: 10.0.1.0/24  (10.0.1.0 - 10.0.1.255)

If VNET B needs to communicate with A at some point, we need to not have overlapping addresses. 

Vnet_B: 10.1.0.0/16  (10.1.0.0 - 10.1.255.255)

Subnet_b_1: 10.1.0.0/24  (10.1.0.0 - 10.1.0.255)

Subnet_b_2: 10.1.1.0/24  (10.1.1.0 - 10.1.1.255)

### Can two Vnets have same CIDR range? If yes, how the both VNets connect?

Ans.

### What is private end point and where does it use?

Ans. 

https://docs.microsoft.com/en-us/azure/private-link/private-endpoint-overview



