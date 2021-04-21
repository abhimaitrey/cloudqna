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

