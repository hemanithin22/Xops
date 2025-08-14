# terraform-xops-webserver

This project demonstrates how to provision and deploy a web server on AWS using **Terraform**. It sets up a full VPC infrastructure and launches an **Amazon Linux 2 EC2 instance** that automatically installs and serves a web page .

---

## 📌 Prerequisites

Before you begin, make sure you have the following:

- ✅ AWS Free Tier account → [Sign up here](https://aws.amazon.com/free)
- ✅ [Terraform CLI](https://developer.hashicorp.com/terraform/install)
- ✅ [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
- ✅ IAM user with:
  - `AmazonEC2FullAccess`
  - `AmazonVPCFullAccess`
- ✅ AWS credentials configured (`aws configure`)
- ✅ GitHub account (for storing your code and screenshots)

---

## 📁 Project Structure

```bash
terraform-xops-webserver/
├── main.tf         # All AWS resources
├── outputs.tf      # Prints EC2 public IP
├── variable.tf     # Input variables
├── README.md       # Project documentation
├── screenshots
        ├── awsconsole.png
        ├── terraform_cli.png
        └── website.png