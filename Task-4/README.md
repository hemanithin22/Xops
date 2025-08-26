# XOps Microchallenge #4 – Terraform + Ansible Web App

## Overview
Provision an AWS EC2 instance with Terraform, then configure and deploy a web app using Ansible.

## Prerequisites
- AWS account & credentials
- Terraform installed
- Ansible installed
- SSH key pair for EC2

## Steps

### 1. Provision EC2 with Terraform
```
terraform init
terraform apply
```
Note the public IP output.

### 2. Configure with Ansible
- Edit `inventory` and replace with your EC2 public IP and private key path.
- Run:
```
ansible-playbook -i inventory site.yml
```

### 3. Test Web App
- Open browser: `http://<EC2_PUBLIC_IP>`

### 4. Cleanup
```
terraform destroy
```
Terminate EC2 to avoid charges.

## Screenshots
Below are example screenshots placed in the `screenshots/` folder:

### EC2 WEBPAGE
![EC2 WEBPAGE](screenshots/ec2-webpage.png)

### Ansible Run Output
![Ansible Output](screenshots/ansible-output.png)

## Files
- `main.tf` – Terraform infra
- `inventory` – Ansible host file
- `site.yml` – Ansible playbook
- `index.html` – Web content
- `README.md` – Setup instructions
