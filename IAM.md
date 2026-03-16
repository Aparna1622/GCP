IAM:  
What is IAM:
Identity Access Management in GCP is a framework that controls 
- **Who** can do **What** on **Which** resources   
Formula: Who -> can do What -> on Which resources  
It is crucial for securely managing access in a cloud environment.  

**Core concepts:  **
| Component | Description |
|-----------|-------------|
| Identity | A user, group, domain, or service account |
| Role | A collection of permissions |
| Policy | A binding of identities to roles |
| Resource | Any GCP object like a project, VM, bucket, etc. |  

**Types of Roles**:  

| Role Type | Description | Example |
|-----------|-------------|---------|
| Basic Roles | Broad, legacy roles (not recommended) | Owner, Editor, Viewer |
| Predefined | Fine-grained, service-specific roles | `roles/storage.admin` |
| Custom | You define exact permissions | Only `compute.instances.start` |  

**IAM Policy Hierarchy:**  
IAM roles can be assigned at different levels:  

Organization  
Folder  
Project  
Resource  
Note: Permissions inherit from parent to child unless explicitly overridden.  

**Service Accounts**:  
- Service accounts are non-human identities used by apps, scripts, or pipelines.  
- Example: Cloud Build uses a service account to deploy apps to GKE.

**IAM Best Practices for DevOps**:  
Follow Least Privilege principle  
- Avoid Basic Roles (too broad)  
- Use Service Accounts for automation  
- Rotate keys/secrets regularly  
- Audit permissions frequently



