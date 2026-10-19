# LibreChatAzureDeployment
A Terraform setup to deploy [LibreChat](https://github.com/danny-avila/LibreChat) to Azure and setup all the necessary services.

## How to Set Up
You must have an existing Azure subscription for this to work.

1. Clone the repo
2. Open in VS-Code Devcontainer
3. In the Terminal inside of VS-Code, run ```az login```
4. [Optionally] edit terraform.tfvars to customize your deployment
5. In the Terminal inside of VS-Code, run ```terraform init```
6. In the Terminal inside of VS-Code, run ```terraform apply```

   To tear down your Azure ressources, run ```terraform destroy```

## CI
This repository is validated by the GitHub Actions workflow in [.github/workflows/ci.yml](.github/workflows/ci.yml). It runs on every pull request and on pushes to `main`, and it checks that the Terraform configuration is canonically formatted (`terraform fmt -check`), initializes without a backend (`terraform init -backend=false`), and passes `terraform validate`. The workflow does not deploy anything or use any credentials or secrets.
