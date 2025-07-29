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

### Command to know which cluster is working?

### How to authenticate AKS in Azure DevOps pipeline?

### How to migrate Jenkins jobs to Azure DevOps?

Ans. https://docs.microsoft.com/en-us/azure/devops/pipelines/migrate/from-jenkins?view=azure-devops

### What are Replica Set, Daemon Set?

## 🔧 Core Kubernetes
### How do you manage resource limits and requests in a Kubernetes cluster? Why are they important?

### Can you describe the difference between a Deployment and a StatefulSet?

### How would you upgrade a running Kubernetes cluster with zero downtime?

### What are the components of the Kubernetes control plane? What happens if the API server goes down?

### How do you troubleshoot a pod stuck in CrashLoopBackOff state?

## 🌐 Networking
### How does Kubernetes networking work? Can pods communicate across nodes by default?

### Which CNI plugin have you used in production (e.g., Calico or Cilium)? What are its pros and cons?

### How have you implemented Network Policies in Kubernetes? Provide an example scenario.

### What’s the difference between a ClusterIP, NodePort, and LoadBalancer service?

### How would you expose an internal microservice to an external user securely?

## 🔐 Security & Vulnerability Management
### How do you enforce security best practices in your Kubernetes clusters?

### What tools have you used for scanning container images and cluster security? How did you integrate them?

### What’s the purpose of RBAC in Kubernetes? How would you restrict access to only allow read access to Pods?

### How does Kyverno or OPA Gatekeeper work? Can you give a policy example you’ve implemented?

### What is the CIS benchmark and how do you apply it to Kubernetes (e.g., using kube-bench)?

## 🔁 CI/CD & GitOps
### How does Argo CD work? How is it different from Flux CD?

### How would you manage multi-environment deployments using Helm and Argo CD?

### Have you used Kustomize? How does it help in managing Kubernetes configurations?

### What challenges have you faced in GitOps deployments, and how did you solve them?

### Can you describe how you set up a GitOps workflow from scratch in your environment?

## 📊 Observability & Monitoring
### How did you set up Prometheus and Grafana for Kubernetes monitoring?

### What are kube-state-metrics and why are they important?

### How do you monitor Kubernetes cluster health and define alerts?

### Explain how you implemented centralized logging using ELK or Loki.

### Have you used tracing tools like Jaeger or OpenTelemetry? Describe your use case.

## 🔄 Autoscaling & Resource Optimization
### How do you implement autoscaling in Kubernetes? When would you use HPA vs VPA?

### What is KEDA, and how is it different from HPA?

### How do you right-size workloads before deploying to production?

### How do you optimize node and pod utilization in a cost-efficient way?

### How would you handle burst traffic in an e-commerce app hosted on Kubernetes?

## 💾 Storage, Backup & Disaster Recovery
### How do you manage persistent storage in Kubernetes?

### What is your experience with Rook, Longhorn, or CSI drivers?

### How do you backup and restore Kubernetes clusters using Velero?

### How would you ensure stateful applications (like databases) are resilient in Kubernetes?

### What’s the difference between emptyDir, hostPath, and persistentVolumeClaims (PVCs)?

## 🌍 Multi-Cloud & Cluster Management
### How do you manage Kubernetes clusters across multiple cloud providers?

### What experience do you have with tools like Rancher, Azure Arc, or Anthos?

### How do you centralize policy enforcement across multiple clusters?

### How do you monitor costs across clusters in different regions or providers?

### How do you manage secrets across multi-cloud Kubernetes clusters?

## 🤖 Advanced / AI & Dev Productivity
### How do you run AI/ML workloads on Kubernetes? What is Kubeflow?

### Have you used Tilt or Skaffold for developer workflows? How do they improve productivity?

### Can you explain a scenario where AI helped you in resource optimization in Kubernetes?

### What steps would you take to containerize a Jupyter Notebook environment on K8s?

### How do you manage ML model versioning and deployment in Kubernetes?

## ⚠️ Troubleshooting & Real-World Scenarios
### A pod is working in dev but failing in production. How would you investigate?

### A deployment rollout caused a service outage. How do you roll back safely using Argo CD?

### You're running out of IPs in your cluster. How do you fix this?

### A team is using hardcoded secrets in YAML. How do you improve this securely?

### How do you ensure application availability during node drain or node failure?


# ⭐️ Kubernetes STAR-Format Mock Interview Answers

## 🔐 Q1: How did you enforce security best practices in your Kubernetes clusters?

**Situation**: We were running Kubernetes workloads for multiple teams across dev, staging, and production clusters. Security audits revealed several misconfigurations and excessive permissions.

**Task**: I was tasked with designing and implementing a cluster-wide security framework to enforce least privilege and secure defaults.

**Action**:
- Integrated **RBAC** to restrict access based on user roles.
- Used **OPA Gatekeeper** to enforce custom policies.
- Implemented **Trivy** for container image scanning.
- Enabled **audit logging**, applied **PodSecurityStandards**, and encrypted all secrets with **Vault**.

**Result**:
- Reduced critical misconfigurations by **90%**.
- Passed the next security audit without exceptions.
- Received appreciation from InfoSec.

---

## 🌐 Q2: How have you implemented Network Policies in Kubernetes?

**Situation**: Our cluster had open inter-pod communication, raising compliance concerns.

**Task**: I needed to isolate sensitive microservices, like the authentication service.

**Action**:
- Implemented **Calico** CNI.
- Designed **NetworkPolicies** with labels/selectors.
- Validated using visualizer tools and simulated attacks.

**Result**:
- Isolated sensitive traffic securely.
- Reduced attack surface.
- Created reusable policy templates.

---

## 🔁 Q3: How did you set up a GitOps workflow using Argo CD?

**Situation**: Manual deployments caused drift between environments.

**Task**: I proposed and led the GitOps implementation.

**Action**:
- Installed **Argo CD** and used **Helm + Kustomize**.
- Configured **App Projects**, RBAC, and alerts.
- Integrated **Argo Image Updater** and Slack.

**Result**:
- Improved deployment consistency.
- Reduced MTTR by 40%.
- Enabled safe, self-service deployments.

---

## 📊 Q4: How did you implement monitoring with Prometheus and Grafana?

**Situation**: Workloads had performance issues, but no observability setup.

**Task**: Implement full monitoring and alerting.

**Action**:
- Deployed **Prometheus Operator** and **Grafana**.
- Added **kube-state-metrics**, node exporter, and custom metrics.
- Set up **Alertmanager** routing to Opsgenie.

**Result**:
- Detected and fixed a memory leak.
- Reduced P1s by 35%.
- Provided self-service dashboards.

---

## 🔄 Q5: How did you implement autoscaling with HPA and KEDA?

**Situation**: Real-time services struggled under burst traffic.

**Task**: Implement dynamic scaling.

**Action**:
- Used **HPA** for CPU/memory-based autoscaling.
- Added **KEDA** for Kafka event-based triggers.
- Tuned thresholds and cooldowns.

**Result**:
- Maintained 100% message SLA.
- Eliminated manual scaling.
- Rolled out to 10+ services.

---

## 🔐 Q6: How did you manage secrets securely in Kubernetes?

**Situation**: Developers hardcoded secrets in YAML.

**Task**: Secure secret management and enable rotation.

**Action**:
- Integrated **HashiCorp Vault** with Vault Agent Injector.
- Used **External Secrets Operator** and **Sealed Secrets**.
- Enabled periodic secret rotation.

**Result**:
- Achieved compliance (SOC2, GDPR).
- Eliminated hardcoded secrets.
- Scaled across 15+ microservices.

---

## 💾 Q7: How did you back up and restore workloads using Velero?

**Situation**: A namespace deletion incident impacted staging.

**Task**: Implement backup and disaster recovery.

**Action**:
- Deployed **Velero** with Azure Blob storage.
- Scheduled daily backups.
- Tested restores in isolated clusters.

**Result**:
- Recovered namespace in 15 minutes.
- Published DR runbooks.
- Protected 10+ stateful apps.

---

## 📦 Q8: How did you handle container image scanning in your CI/CD?

**Situation**: Security team mandated CVE scanning before deploy.

**Task**: Integrate scanning into CI pipelines.

**Action**:
- Used **Trivy** and **Aqua CLI**.
- Enforced policy in **GitHub Actions**.
- Integrated with Jira for tracking.

**Result**:
- Blocked 50+ risky builds.
- Reduced review time by 70%.
- Passed external penetration testing.

---

## 🧰 Q9: How did you troubleshoot a pod stuck in CrashLoopBackOff?

**Situation**: A production pod was repeatedly restarting.

**Task**: Identify and resolve the issue quickly.

**Action**:
- Used `kubectl logs` and `describe` to find OOMKilled error.
- Updated resource limits.
- Validated with **Prometheus** memory graphs.

**Result**:
- Resolved within 30 minutes.
- Documented RCA.
- Added memory alerting.

---

## ⚙️ Q10: How did you manage multi-cluster environments with Rancher or Azure Arc?

**Situation**: We had clusters across AWS, Azure, and on-prem.

**Task**: Centralize management and policy control.

**Action**:
- Used **Rancher** for governance.
- Integrated **Azure Arc** for visibility.
- Standardized monitoring and namespace provisioning.

**Result**:
- Cut cluster onboarding time by 50%.
- Achieved unified policy control.
- Enhanced audit and compliance posture.

---





