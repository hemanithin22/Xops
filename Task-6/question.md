⚡ XOps Microchallenge #6 – “CI/CD + Kubernetes with GitHub Actions & Argo CD” ⚡
Hello XOps Team,
You’ve learned how to Dockerize apps, set up CI/CD pipelines, provision infra with Terraform & Ansible, and explore Kubernetes with kind.

Now it’s time to combine those skills into a real-world DevOps workflow: Deploying your app to Kubernetes using GitOps with Argo CD 🚀.
🎯 Objective
Build a CI/CD pipeline that:
Builds and pushes a Docker image of your app to Docker Hub
Updates Kubernetes manifests with the new image version
Uses Argo CD to automatically sync and deploy your app into your kind cluster
🔧 Step-by-Step Challenge
1. Prepare Your App Repo
Use the app from previous Microchallenges (static site / NGINX / simple web app)
Ensure you have a working Dockerfile
Push this app code to a GitHub repo
2. Build & Push with GitHub Actions
Create a GitHub Actions workflow that:
Builds your Docker image
Pushes it to Docker Hub
Store Docker Hub credentials (DOCKER_USERNAME, DOCKER_PASSWORD) in GitHub Secrets
3. Set Up Kubernetes Manifests Repo
Create a second repo (infra repo) to hold manifests:
/k8s
├── deployment.yaml
├── service.yaml
└── README.md
Configure your deployment.yaml to use the Docker Hub image
4. Install Argo CD on kind Cluster
Install Argo CD in your kind cluster (follow official docs)
Connect Argo CD to your manifests repo
Enable auto-sync for continuous delivery
5. Trigger Deployment
Push new code → GitHub Actions builds & pushes new image → updates infra repo manifests → Argo CD syncs → new version runs on Kubernetes 🎉
📂 Expected Repo Structure
App Repo (with pipeline):
/app-repo
├── Dockerfile
├── index.html / app.py / server.js
├── .github/workflows/cicd.yaml
└── README.md
Infra Repo (for Argo CD):
/infra-repo
└── k8s/
    ├── deployment.yaml
    ├── service.yaml
    └── README.md
✅ Submission Format
Share links to both repos in the Teams thread
Mention in your comment:

✅ GitHub Actions pipeline success

✅ Argo CD sync successful

✅ Screenshot of app running on Kubernetes
⏳ Timeline
Start Date: 26 August 2025 (Tuesday)
Deadline: 2 September 2025 (Tuesday)
Top 3 repos with neat automation + clear READMEs will get featured on the XOps Wall of DevOps Fame 🌟
 