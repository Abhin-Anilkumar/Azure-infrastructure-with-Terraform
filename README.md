# Azure Infrastructure with Terraform

This repository contains Terraform modules for deploying various resources on Azure, including resource groups, storage accounts, service plans, application insights, and function apps. The modular design allows for easy reuse and customization for different environments.

## Prerequisites
- **Terraform:** Ensure you have Terraform installed on your machine. Visit [Terraform's website](https://www.terraform.io/downloads.html) for download instructions.
- **Azure CLI:** You must have the Azure CLI installed and configured. Install Azure CLI and log in using `az login`.
- **Azure Subscription:** You should have an active Azure subscription.

## Repository Structure
- **modules:** This directory contains reusable modules for each type of resource:
  - **Resource-group:** Module for creating resource groups.
  - **Storage-account:** Module for creating Azure storage accounts.
  - **Service-plan:** Module for creating service plans.
  - **Application-insight:** Module for configuring application insights.
  - **Function:** Module for creating Azure function apps.
- **main.tf:** Main Terraform configuration file that defines the module usage.
- **variables.tf:** Defines variables used across all modules.
- **outputs.tf:** Defines outputs from the modules.

## Usage
To use these Terraform modules to set up your Azure infrastructure, follow these steps:

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/Abhin86/Azure-terraform.git
    cd Azure-terraform
    cd environments
    cd <dev/prod/stage>
    ```

2. **Initialize Terraform:**
    ```bash
    terraform init
    ```

3. **Create a Terraform Plan:**
    ```bash
    terraform plan -out=tfplan
    ```

4. **Apply the Configuration:**
    ```bash
    terraform apply "tfplan"
    ```

## Customizing Your Deployment
Edit the `variables.tf` file to set default values or pass different values directly via the command line or through a `.tfvars` file to customize the deployment as per your requirements.
