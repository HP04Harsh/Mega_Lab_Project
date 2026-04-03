<img width="1024" height="559" alt="image" src="https://github.com/user-attachments/assets/0fd49852-5c69-4e05-899c-3dfc6fc47b86" />


Azure Terraform Jenkins Pipeline
================================

This project demonstrates a complete **Infrastructure as Code (IaC)** and **Continuous Integration/Continuous Deployment (CI/CD)** workflow. It automates the lifecycle of a cloud-native application, from provisioning networking and compute resources on Microsoft Azure to deploying a live web server.

🏗️ Architecture
----------------

The automation workflow follows these core stages:

1.  **Infrastructure Provisioning:** Terraform creates the Azure VNet, Subnets, Network Security Groups (NSG), and Ubuntu Virtual Machines.
    
2.  **Configuration Management:** A startup script automatically installs and configures the Apache Web Server (HTTPD).
    
3.  **CI/CD Orchestration:** Jenkins handles the pipeline execution, triggered by GitHub webhooks, to apply infrastructure changes and deploy application code.
    

🛠️ Tech Stack
--------------

*   **Cloud Provider:** [Microsoft Azure](https://github.com/HP04Harsh/azure-cicd-terraform-pipeline)
    
*   **Infrastructure:** [Terraform (HCL)](https://github.com/HP04Harsh/azure-cicd-terraform-pipeline/tree/main/terraform)
    
*   **CI/CD Engine:** [Jenkins](https://github.com/HP04Harsh/azure-cicd-terraform-pipeline/blob/main/Jenkinsfile)
    
*   **Web Server:** Apache (HTTPD)
    
*   **Languages:** HTML, CSS, Shell Scripting
    

📂 Project Structure
--------------------
```
.
├── .github/workflows/ # GitHub Action configurations
├── app/               # Web application source code (HTML/CSS)
├── scripts/           # Automation and startup scripts
├── terraform/         # IaC configuration files (VNet, VM, NSG)
└── Jenkinsfile        # Jenkins pipeline definition

```

🚀 Quick Start
--------------

### Prerequisites

*   An active **Azure Subscription** with a Service Principal created.
    
*   **Jenkins** server with Terraform and SSH Agent plugins installed.
    
*   **Terraform CLI** configured on the Jenkins agent.
    

### Setup Instructions
```
1.  git clone https://github.com/HP04Harsh/azure-cicd-terraform-pipeline.git
    
2.  **Configure Credentials:** Add your Azure Client ID, Secret, and Tenant ID to your Jenkins credential store.
    
3.  **Run Pipeline:** Create a new Pipeline job in Jenkins pointing to the Jenkinsfile and click **Build Now**.
    
```
🔑 Key Features
---------------

*   **Zero-Touch Provisioning:** Fully automated cloud environment setup.
    
*   **Security Integration:** Automated NSG rule creation for restricted port access (80/22).
    
*   **State Management:** Robust infrastructure tracking via Terraform state.
