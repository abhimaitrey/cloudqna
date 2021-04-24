# Azure Kubernetes Service (AKS) Questions

### How to create the AKS cluster?

Ans. The AKS cluster can be created using Azure portal. If you have valid Azure subscription, then go to the Azure portal and search for the *kubernetes service*. Fill out the required information in the whizard.
Important: You are not to be worried about the Master Node (Control Plane) becuase being a managed service, this will be managed by the Microsoft. You will be charged for the worker nodes.

### What other object would automatically be created when you create an AKS cluster?

Ans. 
1. VNet and default subnet
2. Public IP address
3. VMSS
4. Managed Identity
5. Load Balancer etc.

### How do you monitor the logs in Kubernetes?

Ans.

### How to ensure security in Azure Kubernetes Cluster?

Ans. 

### Is the AKS security managed by Azure AD or Kubernetes?

Ans.

### How do nodes ensure the transaction is complete otherwise roleback?

Ans.

### How does Managed Identity work for AKS?

Ans.

### Explain Kubernetes roles?

Ans.
The administrator has to define user permissions as **Role** before assigning permission to the users.  which can be set by Kubernetes RBAC and Azure RBAC. **ClusterRole** grants permission across the entire cluster or all the resources of a cluster even outside a given namespace.

### What types of services are there in Kubernetes/ AKS?

Ans.
Followings are the services in Kubernetes:
1. ClusterIP -  internal applications communication
2. Nodeport -
3. LoadBalancer - routing the request
4. Ingress - another kind of load balancer for more complex scenario
5. ExternalName - handles request from outside the cluster sources.


