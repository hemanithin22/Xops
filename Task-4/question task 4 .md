🔥 XOps Microchallenge #4 – Infrastructure as Code + Configuration Management Combo! 🔥
"Provision + Configure a Web App with Terraform & Ansible"
 
Dear Learners,
 
Now it’s time to introduce a core DevOps concept that ties infra + app + automation together — but still simple enough to be achievable in a week. Please find below the interesting exercise.
 
Objective
Use Terraform to provision an AWS EC2 instance and then use Ansible to configure and deploy a simple web app on it (e.g., install NGINX, push HTML file, start service).
This challenge lets learners:
Reuse Terraform knowledge
Learn the basics of Ansible, a core DevOps config tool
Experience infra provisioning + software automation — together!
 
Challenge Steps
1. Provision Infra using Terraform
Launch a t2.micro EC2 instance in us-east-1
Use appropriate key pair and security group for SSH and HTTP
Use user_data to install python3 (Ansible needs it)
2. Write Ansible Playbook
From your local machine, use Ansible to:
SSH into EC2 (use private key)
Install and start NGINX
Copy a custom index.html to /usr/share/nginx/html/index.html
Ensure firewall (security group) allows access on port 80
3. Test Deployment
Hit the EC2 public IP in browser to confirm app is deployed
 
Expected Submission
✅ GitHub Repo with:
main.tf – Terraform infra
inventory – Ansible host file
site.yml – Ansible playbook
index.html – Web content
README.md – With clear setup instructions
Screenshot of:
EC2 instance
NGINX serving the custom page
Ansible run output
✅ Share repo link in this post thread (only) with ✅
⏰ Timeline
Submission Deadline: Sunday, 27 July 2025
Time expected: ~2–3 hours over the week
⚠️ Cleanup Reminder
Run terraform destroy after verifying output
Terminate EC2 to avoid AWS charges
Learning Outcomes
Deep dive into IaC + Config Mgmt
Understand agentless automation with Ansible
Real-world style infra + app setup using DevOps principles