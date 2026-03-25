## 🧱 What is Compute Engine?
- Compute Engine is GCP’s **IaaS (Infrastructure as a Service)** that lets you launch virtual machines (VMs) on demand.
- VMs are customizable by CPU, RAM, OS, boot disk, and networking.
- Supports automated provisioning, startup scripts, auto-healing, and custom images.

---

## ⚙️ Key Concepts

| Concept          | Description |
|-----------------|------------|
| Instance        | A VM (virtual server) that runs in a GCP zone |
| Zone            | A single data center in a GCP region |
| Machine Type    | Defines CPU, RAM (e.g., `e2-micro`, `n1-standard-1`) |
| Boot Disk       | Persistent disk attached to VM with OS |
| Startup Script  | Script that runs when the VM starts |
| Firewall Rule   | Controls allowed traffic to/from VM |

---

## 🧪 Hands-On Lab

### 🛠️ Launch a VM and Connect via SSH

```bash
gcloud compute instances create devops-vm \
  --zone=us-central1-a \
  --machine-type=e2-micro \
  --image-family=ubuntu-2004-lts \
  --image-project=ubuntu-os-cloud \
  --tags=http-server

# SSH into the instance
gcloud compute ssh devops-vm --zone=us-central1-a
