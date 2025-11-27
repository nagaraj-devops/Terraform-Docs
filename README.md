# Terraform-Docs
Terraform-Docs

## What is terraform?
1. Terraform is an open-source infrastructure as code (IaC) tool created by HashiCorp.
2. It allows you to define and provision data center infrastructure using a high-level configuration language called HashiCorp Configuration Language (HCL), or optionally JSON.

## How Terraform Works
1. Terraform uses providers to interact with various cloud services (like AWS, Azure, Google Cloud) and other platforms (like Kubernetes, GitHub).


## When to Use Terraform
1. Terraform is best used whenever you need to reliably, repeatably, and safely manage infrastructure.
    a. Multi-cloud Deployment
    b. Environment Standardization & Replication
    c. Infrastructure Automation
    d. Infrastructure Versioning
    e. Resource Management and Scale

## Terrform Lifcycle / WorkFlow
1. Initialization - ```terraform init```
    - Sets up the working directory. It downloads the required providers (plugins for interacting with cloud APIs), sets up the backend (where the state file is stored), and initializes any modules.

2. Planning	- ```terraform plan```
    - Creates an execution plan. Terraform first refreshes the state (compares the state file to the real-world infrastructure), then compares the real state to your configuration files, and outputs exactly what actions (create, change, destroy) will be performed. This is a safe preview.

3. Application - ```terraform apply```
    - Executes the plan created in the previous step. It provisions or modifies the infrastructure resources in the correct order, handles dependencies, and updates the state file to reflect the new real-world infrastructure state.

4. Destruction - ```terraform destroy```
    - Removes all the infrastructure resources managed by the current Terraform configuration. It generates a destruction plan and executes it, completely deprovisioning the resources. This command should be used with extreme caution.


