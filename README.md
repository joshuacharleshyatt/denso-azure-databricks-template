# 🧱 Databricks Azure DevOps Template

This repository provides a Git template for deploying Databricks workloads (notebooks, jobs, libraries, etc.) using [Databricks Asset Bundles (DABs)](https://docs.databricks.com/dev-tools/bundles/index.html) and Azure DevOps Pipelines.

## 📦 Features

- 🚀 CI/CD pipeline integration with Azure DevOps
- 🔐 Secure authentication via Service Principal
- 🧪 Built-in testing support for notebooks and Python code
- 🧱 Asset Bundle-based deployments (`databricks.yaml`)
- 📁 Environment promotion across dev, staging, and production
- 🔍 Linting, validation, and approval gates


## 🚀 Getting Started

### Prerequisites

- Azure DevOps project with pipeline permissions
- Databricks workspace

### Setup

1. Import this Repo into Azure
2. Rename the repo
3. In databricks dev env, go to your workspace personal folder. 
4. clone the new azure repo
5. make code changes, commit as needed
6. When ready to deploy
    - Start a new pipeline and point to the azure_pipeline.yml file
    - modify the databricks.yml file for your project and job related resources
    - add job yamls to the resources folder. 
    - give permission to all of the required resources to the NA_sp ... service principle
7. Commit code (must be main) and watch pipeline and approve at any stage you have permission to do
8. On success, your code pushes move through dev -> staging -> prod

## 📄 License

This project is licensed under the [DENSO Internal Use License](./LICENSE) and may be used only by current employees of DENSO CORPORATION.
